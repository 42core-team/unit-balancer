<script lang="ts">
    let units = [
        {
            id: 1,
            name: "Warrior",
            img: "images/skeleton_basic_idle__0.png",
            cost: 100,
            health: 200,
            damage: 50,
        },
        {
            id: 2,
            name: "Miner",
            img: "images/skeleton_basic_idle__0.png",
            cost: 80,
            health: 150,
            damage: 70,
        },
        {
            id: 3,
            name: "Archer",
            img: "images/skeleton_archer_idle__0.png",
            cost: 80,
            health: 150,
            damage: 70,
        },
        {
            id: 4,
            name: "Healer",
            img: "images/skeleton_healer_idle__0.png",
            cost: 80,
            health: 150,
            damage: 70,
        },
        {
            id: 5,
            name: "Tank",
            img: "images/skeleton_tank_idle__0.png",
            cost: 80,
            health: 150,
            damage: 70,
        },
    ];
</script>

<img src="core-logo.png" alt="Logo" />
<h1>Unit Balancer</h1>

<div class="unit-list">
    {#each units as unit (unit.id)}
        <div class="unit">
            <img src={unit.img} alt={unit.name} />
            <h3>{unit.name}</h3>
            <p>
                Cost: <input
                    type="range"
                    min="0"
                    max="500"
                    bind:value={unit.cost}
                />
                {unit.cost}
            </p>
            <p>
                Health: <input
                    type="range"
                    min="0"
                    max="500"
                    bind:value={unit.health}
                />
                {unit.health}
            </p>
            <p>
                Damage: <input
                    type="range"
                    min="0"
                    max="200"
                    bind:value={unit.damage}
                />
                {unit.damage}
            </p>
        </div>
    {/each}
</div>

<style>
    .unit-list {
        display: flex;
        flex-wrap: wrap;
        gap: 1rem;
    }
    .unit {
        padding: 1rem;
        box-shadow: 0 0 10px rgba(0, 0, 0, 0.4);
        text-align: center;
        background-image: url("images/ground_cracked.png");
        background-blend-mode: 1;
        background-repeat: repeat;
        background-position: center;
        background-size: auto;
        background-clip: border-box;
        background-origin: padding-box;
    }
    .unit p {
        box-shadow: 0 0 10px rgba(0, 0, 0, 0.2);
    }
    img {
        cursor: pointer;
        width: 100px;
        height: auto;
    }
</style>
