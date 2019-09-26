<template>
    <div class="container">
        <div class="row">
            <div class="group col-lg-10 col-md-10 col-sm-12 col-xs-12 col-centered"><p class="title">IKARIAM MILITARY
                CALCULATOR</p>
                <p style="text-align:center"></p></div>
        </div>
        <div class="row">
            <div class="group col-lg-10 col-md-10 col-sm-12 col-xs-12 col-centered">
                <div class="group-col col-lg-6 col-md-6 col-sm-12 col-xs-12"><p class="sub-title">Ground troops</p>
                    <table class="goundU">
                        <thead>
                        <tr>
                            <th>Unit</th>
                            <th>Count</th>
                            <th>Generals</th>
                        </tr>
                        </thead>
                        <tbody>
                        <tr>
                            <td><img src="../assets/images/ground/Hoplite.png"></td>
                            <td><input id="hoplite" class="units" type="text" v-on:keyup="updateGenerals"></td>
                            <td class="generals">{{init.hoplite}}</td>
                        </tr>
                        <tr>
                            <td><img src="../assets/images/ground/Steam_Giant.png"></td>
                            <td><input id="steam_giant" class="units" type="text" v-on:keyup="updateGenerals"></td>
                            <td class="generals">{{init.steam_giant}}</td>
                        </tr>
                        <tr>
                            <td><img src="../assets/images/ground/Spearman.png"></td>
                            <td><input id="spearman" class="units" type="text" v-on:keyup="updateGenerals"></td>
                            <td class="generals">{{init.spearman}}</td>
                        </tr>
                        <tr>
                            <td><img src="../assets/images/ground/Swordsman.png"></td>
                            <td><input id="swordsman" class="units" type="text" v-on:keyup="updateGenerals"></td>
                            <td class="generals">{{init.swordsman}}</td>
                        </tr>
                        <tr>
                            <td><img src="../assets/images/ground/Slinger.png"></td>
                            <td><input id="slinger" class="units" type="text" v-on:keyup="updateGenerals"></td>
                            <td class="generals">{{init.slinger}}</td>
                        </tr>
                        <tr>
                            <td><img src="../assets/images/ground/Archer.png"></td>
                            <td><input id="archer" class="units" type="text" v-on:keyup="updateGenerals"></td>
                            <td class="generals">{{init.archer}}</td>
                        </tr>
                        <tr>
                            <td><img src="../assets/images/ground/Sulphur_Carabineer.png"></td>
                            <td><input id="sulphur_carabineer" class="units" type="text" v-on:keyup="updateGenerals">
                            </td>
                            <td class="generals">{{init.sulphur_carabineer}}</td>
                        </tr>
                        <tr>
                            <td><img src="../assets/images/ground/Ram.png"></td>
                            <td><input id="ram" class="units" type="text" v-on:keyup="updateGenerals"></td>
                            <td class="generals">{{init.ram}}</td>
                        </tr>
                        <tr>
                            <td><img src="../assets/images/ground/Catapult.png"></td>
                            <td><input id="catapult" class="units" type="text" v-on:keyup="updateGenerals"></td>
                            <td class="generals">{{init.catapult}}</td>
                        </tr>
                        <tr>
                            <td><img src="../assets/images/ground/Mortar.png"></td>
                            <td><input id="mortar" class="units" type="text" v-on:keyup="updateGenerals"></td>
                            <td class="generals">{{init.mortar}}</td>
                        </tr>
                        <tr>
                            <td><img src="../assets/images/ground/Gyrocopter.png"></td>
                            <td><input id="gyrocopter" class="units" type="text" v-on:keyup="updateGenerals"></td>
                            <td class="generals">{{init.gyrocopter}}</td>
                        </tr>
                        <tr>
                            <td><img src="../assets/images/ground/Balloon-Bombardier.png"></td>
                            <td><input id="balloon_bombardier" class="units" type="text" v-on:keyup="updateGenerals">
                            </td>
                            <td class="generals">{{init.balloon_bombardier}}</td>
                        </tr>
                        <tr>
                            <td><img src="../assets/images/ground/Cook.png"></td>
                            <td><input id="cook" class="units" type="text" v-on:keyup="updateGenerals"></td>
                            <td class="generals">{{init.cook}}</td>
                        </tr>
                        <tr>
                            <td><img src="../assets/images/ground/Doctor.png"></td>
                            <td><input id="doctor" class="units" type="text" v-on:keyup="updateGenerals"></td>
                            <td class="generals">{{init.doctor}}</td>
                        </tr>
                        <tr>
                            <td>Sum</td>
                            <td id="unit-sum">0</td>
                            <td id="generals-sum">{{generalSum}}</td>
                        </tr>
                        </tbody>
                    </table>
                    <button class="button clearGround" @click.prevent="resetUnits">Clear</button>
                </div>
                <div class="group-col col-lg-6 col-md-6 col-sm-12 col-xs-12"><p class="sub-title">Fleet</p>
                    <table class="fleetU">
                        <thead>
                        <tr>
                            <th>Unit</th>
                            <th>Count</th>
                            <th>Generals</th>
                        </tr>
                        </thead>
                        <tbody>
                        <tr>
                            <td><img src="../assets/images/fleet/Fire_Ship.png"></td>
                            <td><input id="fire_ship" class="funits" type="text" v-on:keyup="updateGeneralsFleet"></td>
                            <td class="generals">{{initFleet.fire_ship}}</td>
                        </tr>
                        <tr>
                            <td><img src="../assets/images/fleet/Steam_Ram.png"></td>
                            <td><input id="steam_ram" class="funits" type="text" v-on:keyup="updateGeneralsFleet"></td>
                            <td class="generals">{{initFleet.steam_ram}}</td>
                        </tr>
                        <tr>
                            <td><img src="../assets/images/fleet/Ram_Ship.png"></td>
                            <td><input id="ram_ship" class="funits" type="text" v-on:keyup="updateGeneralsFleet"></td>
                            <td class="generals">{{initFleet.ram_ship}}</td>
                        </tr>
                        <tr>
                            <td><img src="../assets/images/fleet/Ballista_Ship.png"></td>
                            <td><input id="ballista_ship" class="funits" type="text" v-on:keyup="updateGeneralsFleet">
                            </td>
                            <td class="generals">{{initFleet.ballista_ship}}</td>
                        </tr>
                        <tr>
                            <td><img src="../assets/images/fleet/Catapult_Ship.png"></td>
                            <td><input id="catapult_ship" class="funits" type="text" v-on:keyup="updateGeneralsFleet">
                            </td>
                            <td class="generals">{{initFleet.catapult_ship}}</td>
                        </tr>
                        <tr>
                            <td><img src="../assets/images/fleet/Mortar_Ship.png"></td>
                            <td><input id="mortar_ship" class="funits" type="text" v-on:keyup="updateGeneralsFleet">
                            </td>
                            <td class="generals">{{initFleet.mortar_ship}}</td>
                        </tr>
                        <tr>
                            <td><img src="../assets/images/fleet/Diving_Boat.png"></td>
                            <td><input id="diving_boat" class="funits" type="text" v-on:keyup="updateGeneralsFleet">
                            </td>
                            <td class="generals">{{initFleet.diving_boat}}</td>
                        </tr>
                        <tr>
                            <td><img src="../assets/images/fleet/Rocket_Ship.png"></td>
                            <td><input id="rocket_ship" class="funits" type="text" v-on:keyup="updateGeneralsFleet">
                            </td>
                            <td class="generals">{{initFleet.rocket_ship}}</td>
                        </tr>
                        <tr>
                            <td><img src="../assets/images/fleet/Paddle_Speedboat.png"></td>
                            <td><input id="paddle_speedboat" class="funits" type="text"
                                       v-on:keyup="updateGeneralsFleet">
                            </td>
                            <td class="generals">{{initFleet.paddle_speedboat}}</td>
                        </tr>
                        <tr>
                            <td><img src="../assets/images/fleet/Ballon_Carrier.png"></td>
                            <td><input id="balloon_carrier" class="funits" type="text" v-on:keyup="updateGeneralsFleet">
                            </td>
                            <td class="generals">{{initFleet.balloon_carrier}}</td>
                        </tr>
                        <tr>
                            <td><img src="../assets/images/fleet/Tender.png"></td>
                            <td><input id="tender" class="funits" type="text" v-on:keyup="updateGeneralsFleet"></td>
                            <td class="generals">{{initFleet.tender}}</td>
                        </tr>
                        <tr>
                            <td>Sum</td>
                            <td id="funit-sum">0</td>
                            <td id="generals-sum">{{generalSumFleet}}</td>
                        </tr>
                        </tbody>
                    </table>
                    <button class="button clearFleet" @click.prevent="resetFleet">Clear</button>
                </div>
            </div>
        </div>
        <div class="row">
            <div class="col-lg-12 col-md-12 col-sm-12 col-xs-12 col-centered footer"> Copyright disclaimer: I do NOT own
                any
                images featured on this website. All rights belong to it's rightful owner/owner's. No copyright
                infringement
                intended.
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        name: 'Home',
        data() {
            return {
                ground: {
                    hoplite: 1.4,
                    steam_giant: 6.2,
                    swordsman: 1.2,
                    spearman: 0.6,
                    sulphur_carabineer: 4,
                    archer: 1.1,
                    slinger: 0.4,
                    mortar: 31,
                    catapult: 11.2,
                    ram: 4.4,
                    balloon_bombardier: 5.8,
                    gyrocopter: 2.5,
                    cook: 4,
                    doctor: 10
                },
                fleet: {
                    steam_ram: 24,
                    fire_ship: 6.2,
                    ram_ship: 5,
                    ballista_ship: 6.8,
                    catapult_ship: 6.4,
                    mortar_ship: 22.4,
                    diving_boat: 20.2,
                    rocket_ship: 28,
                    balloon_carrier: 28,
                    paddle_speedboat: 6.4,
                    tender: 16
                },
                init: {
                    hoplite: 0,
                    steam_giant: 0,
                    swordsman: 0,
                    spearman: 0,
                    sulphur_carabineer: 0,
                    archer: 0,
                    slinger: 0,
                    mortar: 0,
                    catapult: 0,
                    ram: 0,
                    balloon_bombardier: 0,
                    gyrocopter: 0,
                    cook: 0,
                    doctor: 0
                },
                initFleet: {
                    steam_ram: 0,
                    fire_ship: 0,
                    ram_ship: 0,
                    ballista_ship: 0,
                    catapult_ship: 0,
                    mortar_ship: 0,
                    diving_boat: 0,
                    rocket_ship: 0,
                    balloon_carrier: 0,
                    paddle_speedboat: 0,
                    tender: 0
                },
                unitSum: 0,
                generalSum: 0,
                unitSumFleet: 0,
                generalSumFleet: 0
            }
        },
        methods: {
            updateGenerals: function (event) {
                let generalsValue = this.ground[event.target.id];
                let inputValue = event.target.value;
                let generals = inputValue * generalsValue;
                this.init[event.target.id] = Math.round(generals * 100) / 100;
                this.generalSum = this.generalSumCalc()
            },
            generalSumCalc() {
                let total = 0;
                for (let property in this.init) {
                    total += this.init[property]
                }
                return total
            },
            updateGeneralsFleet: function (event) {
                let generalsValue = this.fleet[event.target.id];
                let inputValue = event.target.value;
                let generals = inputValue * generalsValue;
                this.initFleet[event.target.id] = Math.round(generals * 100) / 100;
                this.generalSumFleet = this.generalSumCalcFleet()
            },
            generalSumCalcFleet() {
                let total = 0;
                for (let property in this.initFleet) {
                    total += this.initFleet[property]
                }

                return total
            },
            resetUnits() {
                for (let property in this.init) {
                    this.init[property] = 0
                }
                this.generalSum = 0
            },
            resetFleet() {
                for (let property in this.initFleet) {
                    this.initFleet[property] = 0
                }
                this.generalSumFleet = 0
            },
        }
    }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
    @import '../assets/css/app.css';

    table {
        font-family: 'Open Sans', sans-serif;
        border-collapse: collapse;
        border: 3px solid #44475c;
        margin: 10px 10px 0;
        margin: 10px auto
    }

    table th {
        text-transform: uppercase;
        text-align: center;
        background: #44475c;
        color: #fff;
        padding: 8px;
        min-width: 30px
    }

    table td {
        text-align: center;
        width: 3rem;
        padding: .2rem;
        border-right: 2px solid #7d82a8
    }

    table td:last-child {
        border-right: none
    }

    table tbody tr:nth-child(2n) td {
        background: #d4d8f9
    }

    tbody img {
        max-width: 4rem
    }

    .group {
        margin: 0 auto
    }

    .group-col {
        float: left;
        text-align: center
    }

    .col-centered {
        float: none;
        margin: 0 auto
    }

    .footer {
        text-align: center;
        padding-top: 3rem;
        padding-bottom: 3rem;
        font-weight: 500;
        font-family: "Arial Rounded MT Bold"
    }

    .sub-title {
        padding: 2rem;
        font-weight: 500;
        font-family: "Arial Rounded MT Bold"
    }

    .title {
        text-align: center;
        padding: 2rem 0 0;
        font-weight: 500;
        font-family: "Arial Rounded MT Bold";
        font-size: 2.5rem
    }

    .button {
        margin: 0 auto;
        margin-top: 2rem;
        background-color: #44475c;
        font-weight: 700;
        color: #fff;
        border: none;
        padding: .5rem
    }

    @media screen and (max-width: 768px) {
        table td {
            width: 100%
        }

        table td input {
            width: 10rem
        }
    }
</style>
