---
description: On your way to creating your own unique challenges.
---

# Parameters

## For Moderators: Before you create your challenges, you must create a challenge set to group your challenges together!

Note that all event challenge sets will require approval from myst. Before approval, challenge sets are not visible to the public.

## Main Parameters

There can be no parameters to a module to make the challenge generic. Parameters are used to customize the conditions in which the challenge will progress.

* All parameters are optional
* Conditional parameters `;` are required where they are stated
* Separate with commas, no spaces allowed for each parameter
* Leave empty if there is no parameters
* Does not have to be in order, but `!NOT` weapons and weapon classes have to be after "IS USING" weapons and weapon classes

### Parameters Table

Note that **player** stated in the table is referring to the person completing the challenge.

{% tabs %}
{% tab title="Class" %}
### Player/Enemy Class

* When you indicate more than 1 class, it means **OR**.
  * Eg. `scout,soldier,demoman!ENEMY,heavy!ENEMY` means the player is either Scout or Soldier, and that the enemy is either Demoman or Heavy. 
* To indicate as the enemy, add `!ENEMY` behind the parameter.

| Parameter | Description |
| :--- | :--- |
| `scout` | is playing as Scout |
| `soldier` | is playing as Soldier |
| `pyro` | is playing as Pyro |
| `demoman` | is playing as Demoman |
| `heavy` | is playing as Heavy |
| `engineer` | is playing as Engineer |
| `medic` | is playing as Medic |
| `sniper` | is playing as Sniper |
| `spy` | is playing as Spy |
{% endtab %}

{% tab title="Team" %}
### Player/Enemy Team

* When you indicate more than 1 team, it means **OR**.
  * Eg. `red,blue,red!ENEMY,blue!ENEMY` means the player is either on BLUE team or RED team, and that the enemy is either on BLUE team or RED team.
  * Eg. `red,blue!ENEMY` means that the player has to be in RED team and the enemy must be in BLUE team. 
* To indicate as the enemy, add `!ENEMY` behind the parameter.

| Parameter | Description |
| :--- | :--- |
| `red` | is in RED team |
| `blue` | is in BLUE team |
| `spec` | is in SPECTATOR team |
{% endtab %}

{% tab title="State" %}
### State

* To indicate as the enemy, add `!ENEMY` behind the parameter.
* Eg. `alive;dead!ENEMY` means that the player is alive and the enemy is dead

| Parameter | Description |
| :--- | :--- |
| `alive` | The player is alive |
| `dead` | The player is dead |
{% endtab %}

{% tab title="Enemy Status" %}
### Enemy Status

<table>
  <thead>
    <tr>
      <th style="text-align:left">Parameter</th>
      <th style="text-align:left">Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left"><code>self</code>
      </td>
      <td style="text-align:left">
        <p>The enemy and the victim is the same</p>
        <p></p>
        <p>Examples</p>
        <ul>
          <li><b>Rocket and sticky jumping equals self damage</b>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>robot</code>
      </td>
      <td style="text-align:left">A non-human enemy, eg. the bots in Mann vs Machine (not inclusive of NPCs
        like the HHH, Merasmus, Monoculus and Skeletons)</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>sameteam</code>
      </td>
      <td style="text-align:left">The enemy is on the same team (team kill)
        <br />[<b>NOT RECOMMENDED</b>]</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>name;search</code>
      </td>
      <td style="text-align:left">
        <p>Match the enemies&apos; name
          <br />
        </p>
        <p><code>;search</code> is the matching term to search for</p>
        <ul>
          <li><code>*</code><em> </em>infront of a name if you want the challenge to
            match names <b>CONTAINING </b>that name.</li>
          <li>Otherwise, the challenge will match names with the exact naming.
            <br />
          </li>
          <li>If you include multiple name searches, it means <b>OR</b>.</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>dist;meters;e/m/l</code>
      </td>
      <td style="text-align:left">
        <p>How far away the enemy is from the player</p>
        <p></p>
        <p><code>;meters</code>is the number of meters away</p>
        <ul>
          <li><code>;e</code> is <b>exactly </b><code>;meters</code> away</li>
          <li><code>;m</code> is <b>more than or equals to</b>  <code>;meters</code>away</li>
          <li><code>;l</code> is <b>less than</b>  <b>or equals to</b><code>;meters</code> away</li>
        </ul>
        <p>If you include multiple distances, it means <b>OR</b>.</p>
      </td>
    </tr>
  </tbody>
</table>### Templates

| Description | Parameter List |
| :--- | :--- |
| `name;*Sentry Buster` | Sentry Busters |
| `name;*Giant,name;*Super,name;*Major,name;*Colonel,name;*Titan` | Giant Robots |
| `name;*Giant Medic` | Giant Medics |
| `name;*Super Scout` | Super Scouts |
| `name;*Extended Buff Soldier` | Extended Buffed Soldiers |
| `name;*Bowman` | Bowmans |
| `name;*Samurai` | Samurais |
| `name;*Deflector` | Deflectors |
| `name;*Demoknight` | Demoknights |
{% endtab %}

{% tab title="Team Status" %}
###  Team Status

* When you indicate more than 1 team, it means **AND**.
  * Eg. `redtotal;5,bluetotal;5` means that both BLUE and RED teams have exactly 5 players each.

<table>
  <thead>
    <tr>
      <th style="text-align:left">Parameter</th>
      <th style="text-align:left">Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left"><code>total;amount;e/m/l</code>
      </td>
      <td style="text-align:left">
        <p>The total number of players</p>
        <p></p>
        <p><code>;amount</code> is the number of players</p>
        <ul>
          <li><code>;e</code> is <b>exactly</b>  <code>;amount</code> of players</li>
          <li><code>;m</code> is <b>more than</b>  <b>or equals to </b><code>;amount</code>of
            players</li>
          <li><code>;l</code> is <b>less than</b>  <b>or equals to </b><code>;amount</code> of
            players</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>redtotal;amount;e/m/l</code>
      </td>
      <td style="text-align:left">
        <p>The total number of players in red team</p>
        <p></p>
        <p><code>;amount</code> is the number of players</p>
        <ul>
          <li><code>;e</code> is <b>exactly</b>  <code>;amount</code> of players</li>
          <li><code>;m</code> is <b>more than</b>  <b>or equals to </b><code>;amount</code>of
            players</li>
          <li><code>;l</code> is <b>less than</b>  <b>or equals to </b><code>;amount</code> of
            players</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>bluetotal;amount;e/m/l</code>
      </td>
      <td style="text-align:left">
        <p>The total number of players in blue team</p>
        <p></p>
        <p><code>;amount</code> is the number of players</p>
        <p></p>
        <p><code>;e</code> is <b>exactly</b>  <code>;amount</code> of players</p>
        <p><code>;m</code> is <b>more than</b>  <b>or equals to </b><code>;amount</code>of
          players</p>
        <p><code>;l</code> is <b>less than</b>  <b>or equals to </b><code>;amount</code> of
          players</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>totalalive;amount;e/m/l</code>
      </td>
      <td style="text-align:left">
        <p>The total number of players <b>alive</b>
        </p>
        <p></p>
        <p><code>;amount</code> is the number of players</p>
        <p>&#x200B;</p>
        <ul>
          <li><code>;e</code> is <b>exactly</b>  <code>;amount</code> of players</li>
          <li><code>;m</code> is <b>more than</b>  <b>or equals to </b><code>;amount</code>of
            players</li>
          <li><code>;l</code> is <b>less than</b>  <b>or equals to </b><code>;amount</code> of
            players</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>redalive;amount;e/m/l</code>
      </td>
      <td style="text-align:left">
        <p>The total number of players <b>alive</b> in red team</p>
        <p></p>
        <p><code>;amount</code> is the number of players</p>
        <ul>
          <li><code>;e</code> is <b>exactly</b>  <code>;amount</code> of players</li>
          <li><code>;m</code> is <b>more than</b>  <b>or equals to </b><code>;amount</code>of
            players</li>
          <li><code>;l</code> is <b>less than</b>  <b>or equals to </b><code>;amount</code> of
            players</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>bluealive;amount;e/m/l</code>
      </td>
      <td style="text-align:left">
        <p>The total number of players <b>alive</b> in blue team</p>
        <p></p>
        <p><code>;amount</code> is the number of players</p>
        <ul>
          <li><code>;e</code> is <b>exactly</b>  <code>;amount</code> of players</li>
          <li><code>;m</code> is <b>more than</b>  <b>or equals to </b><code>;amount</code>of
            players</li>
          <li><code>;l</code> is <b>less than</b>  <b>or equals to </b><code>;amount</code> of
            players</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>team;amount;e/m/l</code>
      </td>
      <td style="text-align:left">
        <p>The total number of players in the player&apos;s team</p>
        <p></p>
        <p><code>;amount</code> is the number of players</p>
        <ul>
          <li><code>;e</code> is <b>exactly</b>  <code>;amount</code> of players</li>
          <li><code>;m</code> is <b>more than</b>  <b>or equals to </b><code>;amount</code>of
            players</li>
          <li><code>;l</code> is <b>less than</b>  <b>or equals to </b><code>;amount</code> of
            players</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>enemyteam;amount;e/m/l</code>
      </td>
      <td style="text-align:left">
        <p>The total number of players in the enemy&apos;s team</p>
        <p></p>
        <p><code>;amount</code> is the number of players</p>
        <ul>
          <li><code>;e</code> is <b>exactly</b>  <code>;amount</code> of players</li>
          <li><code>;m</code> is <b>more than</b>  <b>or equals to </b><code>;amount</code>of
            players</li>
          <li><code>;l</code> is <b>less than</b>  <b>or equals to </b><code>;amount</code> of
            players</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>teamalive;amount;e/m/l</code>
      </td>
      <td style="text-align:left">
        <p>The total number of players <b>alive</b> in the player&apos;s team</p>
        <p></p>
        <p><code>;amount</code> is the number of players</p>
        <ul>
          <li><code>;e</code> is <b>exactly</b>  <code>;amount</code> of players</li>
          <li><code>;m</code> is <b>more than</b>  <b>or equals to </b><code>;amount</code>of
            players</li>
          <li><code>;l</code> is <b>less than</b>  <b>or equals to </b><code>;amount</code> of
            players</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>enemyteamalive;amount;e/m/l</code>
      </td>
      <td style="text-align:left">
        <p>The total number of players <b>alive</b> in enemy&apos;s team</p>
        <p></p>
        <p><code>;amount</code> is the number of players</p>
        <ul>
          <li><code>;e</code> is <b>exactly</b>  <code>;amount</code> of players</li>
          <li><code>;m</code> is <b>more than</b>  <b>or equals to </b><code>;amount</code>of
            players</li>
          <li><code>;l</code> is <b>less than</b>  <b>or equals to </b><code>;amount</code> of
            players</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>
{% endtab %}

{% tab title="One Chance" %}
### One Chance

Only one parameter is allowed from this category for each challenge.

<table>
  <thead>
    <tr>
      <th style="text-align:left">Parameter</th>
      <th style="text-align:left">Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left"><code>onelife;amount</code>
      </td>
      <td style="text-align:left">
        <p>Achieved in a single life.</p>
        <p><code>;amount</code> is the number of times the module is run before increasing
          the points by 1</p>
        <p></p>
        <p>Eg. <b>Deal 500 Damage in One Life [0/5]</b> uses <code>damage</code> module
          with 5 points and has parameters of <code>onelife;500</code>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>oneround;amount</code>
      </td>
      <td style="text-align:left">
        <p>Achieved in a single round.</p>
        <p><code>;amount</code> is the number of times the module is run before increasing
          the points by 1</p>
        <p></p>
        <p>Eg. <b>Walk 1000m in One Round [0/10]</b> uses <code>distance</code> module
          with 10 points and has parameters of <code>oneround;1000</code>
        </p>
      </td>
    </tr>
  </tbody>
</table>
{% endtab %}

{% tab title="Timers" %}
### Timers

Only one parameter is allowed from this category for each challenge.

<table>
  <thead>
    <tr>
      <th style="text-align:left">Parameter</th>
      <th style="text-align:left">Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left"><code>timer;amount;seconds</code>
      </td>
      <td style="text-align:left">
        <p>A timer run every second.</p>
        <p><code>;amount</code> is the number of times the module is run before increasing
          the points by 1</p>
        <p><code>;seconds</code> is the number of seconds that has passed before checking
          whether it should increase the points by 1</p>
        <p></p>
        <p>Examples</p>
        <ul>
          <li><b>Survive as the Last Man in Freak Fortress for 1 Minute [0/2]<br /></b>Module: <code>alive</code>
            <br
            />Points: <code>2</code>
            <br />Parameters: <code>redalive;1,timer;0;60</code><b><br /></b>
          </li>
          <li><b>Deal 250 Damage as the Last Man in Freak Fortress in 1:30  Minutes [0/5]<br /></b>Module: <code>damage</code>
            <br
            />Points: <code>5</code>
            <br />Parameters: <code>redalive;1,timer;250;90</code>
            <br />
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>stimer;amount;seconds</code>
      </td>
      <td style="text-align:left">
        <p>A timer run only once in the first x seconds of the round.</p>
        <p><code>;amount</code> is the number of times the module is run before increasing
          the points by 1</p>
        <p><code>;seconds</code> is the number of seconds that has passed before checking
          whether it should increase the points by 1</p>
        <p></p>
        <p>Examples</p>
        <ul>
          <li><b>Deal 250 Damage in the first 10 Seconds of a Round [0/2]<br /></b>Module: <code>damage</code>
            <br
            />Points: <code>2</code>
            <br />Parameters: <code>stimer;250;10</code>
            <br />
          </li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>
{% endtab %}

{% tab title="Conditions" %}
### Conditions

When you indicate more than 1 condition, it means **AND**.

<table>
  <thead>
    <tr>
      <th style="text-align:left">Parameter</th>
      <th style="text-align:left">Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left"><code>cond;tfcond</code>
      </td>
      <td style="text-align:left">
        <p>Whether the player is or isn&apos;t in a condition.
          <br />
          <br /><code>;tfcond</code><em> </em>is<em> </em>the matching condition</p>
        <ul>
          <li><a href="https://wiki.teamfortress.com/wiki/Cheats#addcond">List of Conditions</a>
            <br
            />Does not have to include TFCond_, only the text after that<b> (case sensitive)<br /></b>
          </li>
          <li>To indicate the player isn&apos;t in a condition, add <code>!NOT</code> behind
            the parameter.</li>
          <li>To indicate as the enemy, add <code>!ENEMY</code> behind the parameter.</li>
        </ul>
        <p>Examples</p>
        <ul></ul>
      </td>
    </tr>
  </tbody>
</table>
{% endtab %}

{% tab title="Weapons" %}
### Weapons

* When you indicate more than 1 weapon or weaponclass, it means **OR** for all the "is using" weapons and **AND** for all the "is not using" weapons.
  * The player can use **either one** of the weapons in the "IS USING" pool, and the player MUST NOT use **ANY** of the weapons in the "IS NOT USING `!NOT`" pool. 
  * Eg. `weapon;1071,weapon;423,weapon;221!NOT,weapon;264!NOT` means the player is either using a Golden Frying Pan or Saxxy but NOT a Holy Mackerel or normal Frying Pan. 
  * Eg. If you add `weapon;1071!ENEMY,weapon;423!ENEMY,weapon;221!ENEMY!NOT,weapon;264!ENEMY!NOT` to the above example, it means that BOTH the player and enemy are either using a Golden Frying Pan or Saxxy but NOT a Holy Mackerel or normal Frying Pan.
* To indicate as the enemy, add `!ENEMY` behind the parameter.

<table>
  <thead>
    <tr>
      <th style="text-align:left">Parameter</th>
      <th style="text-align:left">Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left"><code>weapon;weapon_index</code>
      </td>
      <td style="text-align:left">
        <p>The weapon index the player is using. Used for specific weapons.</p>
        <ul>
          <li>To indicate the player isn&apos;t this weapon, add <code>!NOT</code> behind
            the parameter.</li>
        </ul>
        <p>Examples</p>
        <ul>
          <li><b>Not using a Golden Fying Pan</b>
            <br />Parameters:<code>weapon;1071!NOT</code>
          </li>
        </ul>
        <p><a href="https://wiki.alliedmods.net/Team_Fortress_2_Item_Definition_Indexes">List of Weapon Indexes</a>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>weaponclass;tf_weaponclassname</code>
      </td>
      <td style="text-align:left">
        <p>The weapon classname the player is using. Used for a broad category of
          weapon types.</p>
        <ul>
          <li>To indicate the player isn&apos;t this weapon class, add <code>!NOT</code> behind
            the parameter.</li>
        </ul>
        <p>Examples</p>
        <ul>
          <li><b>Not using a weapon with tf_weapon_rocketlauncher classname<br />(does not include ALL rocket launchers such as the Cow Mangler 5000)<br /></b>Parameters: <code>weaponclass;tf_weapon_rocketlauncher!NOT</code>
          </li>
        </ul>
        <p><a href="https://wiki.alliedmods.net/Team_Fortress_2_Item_Definition_Indexes">List of Weapon Classnames</a>
        </p>
      </td>
    </tr>
  </tbody>
</table>### Templates

| Description | Parameter List |
| :--- | :--- |
| Using any of the explosive weapons | `weaponclass;tf_weapon_rocketlauncher,weaponclass;tf_weapon_rocketlauncher_directhit,weaponclass;tf_weapon_particle_cannon,weaponclass;tf_weapon_rocketlauncher_airstrike,weaponclass;tf_weapon_grenadelauncher,weaponclass;tf_weapon_cannon,weaponclass;tf_weapon_pipebomblauncher` |
{% endtab %}

{% tab title="Special" %}
### Special

These parameters are catered to the respective modules only.

#### `kill (Optional)`

<table>
  <thead>
    <tr>
      <th style="text-align:left">Parameter</th>
      <th style="text-align:left">Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left"><code>killtype;typeno</code>
      </td>
      <td style="text-align:left">
        <p>The type of kill on the enemy</p>
        <p></p>
        <p><code>;typeno</code><em> </em>is<em> </em>the matching kill type number</p>
        <ul>
          <li>Refer to the table below for the list of kill numbers</li>
          <li>To indicate it wasn&apos;t this type of kill, add <code>!NOT</code> behind
            the parameter.</li>
        </ul>
        <p>Examples</p>
        <ul>
          <li><b>Headshot But Not Suicide (somehow)</b>
            <br />Parameters: <code>killtype;HEADSHOT,killtype;6!NOT</code>
          </li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>| Kill Type | Type Number |
| :--- | :--- |
|  TF\_CUSTOM\_HEADSHOT | 1 |
|  TF\_CUSTOM\_BACKSTAB | 2 |
|  TF\_CUSTOM\_BURNING | 3 |
|  TF\_CUSTOM\_WRENCH\_FIX | 4 |
|  TF\_CUSTOM\_MINIGUN | 5 |
|  TF\_CUSTOM\_SUICIDE | 6 |
|  TF\_CUSTOM\_TAUNT\_HADOUKEN | 7 |
|  TF\_CUSTOM\_BURNING\_FLARE | 8 |
|  TF\_CUSTOM\_TAUNT\_HIGH\_NOON | 9 |
|  TF\_CUSTOM\_TAUNT\_GRAND\_SLAM | 10 |
|  TF\_CUSTOM\_PENETRATE\_MY\_TEAM | 11 |
|  TF\_CUSTOM\_PENETRATE\_ALL\_PLAYERS | 12 |
|  TF\_CUSTOM\_TAUNT\_FENCING | 13 |
|  TF\_CUSTOM\_PENETRATE\_HEADSHOT | 14 |
|  TF\_CUSTOM\_TAUNT\_ARROW\_STAB | 15 |
|  TF\_CUSTOM\_TELEFRAG | 16 |
|  TF\_CUSTOM\_BURNING\_ARROW | 17 |
|  TF\_CUSTOM\_FLYINGBURN | 18 |
|  TF\_CUSTOM\_PUMPKIN\_BOMB | 19 |
|  TF\_CUSTOM\_DECAPITATION | 20 |
|  TF\_CUSTOM\_TAUNT\_GRENADE | 21 |
|  TF\_CUSTOM\_BASEBALL | 22 |
|  TF\_CUSTOM\_CHARGE\_IMPACT | 23 |
|  TF\_CUSTOM\_TAUNT\_BARBARIAN\_SWING | 24 |
|  TF\_CUSTOM\_AIR\_STICKY\_BURST | 25 |
|  TF\_CUSTOM\_DEFENSIVE\_STICKY | 26 |
|  TF\_CUSTOM\_PICKAXE | 27 |
|  TF\_CUSTOM\_ROCKET\_DIRECTHIT | 28 |
|  TF\_CUSTOM\_TAUNT\_UBERSLICE | 29 |
|  TF\_CUSTOM\_PLAYER\_SENTRY | 30 |
|  TF\_CUSTOM\_STANDARD\_STICKY | 31 |
|  TF\_CUSTOM\_SHOTGUN\_REVENGE\_CRIT | 32 |
|  TF\_CUSTOM\_TAUNT\_ENGINEER\_SMASH | 33 |
|  TF\_CUSTOM\_BLEEDING | 34 |
|  TF\_CUSTOM\_GOLD\_WRENCH | 35 |
|  TF\_CUSTOM\_CARRIED\_BUILDING | 36 |
|  TF\_CUSTOM\_COMBO\_PUNCH | 37 |
|  TF\_CUSTOM\_TAUNT\_ENGINEER\_ARM | 38 |
|  TF\_CUSTOM\_FISH\_KILL | 39 |
|  TF\_CUSTOM\_TRIGGER\_HURT | 40 |
|  TF\_CUSTOM\_DECAPITATION\_BOSS | 41 |
|  TF\_CUSTOM\_STICKBOMB\_EXPLOSION | 42 |
|  TF\_CUSTOM\_AEGIS\_ROUND | 43 |
|  TF\_CUSTOM\_FLARE\_EXPLOSION | 44 |
|  TF\_CUSTOM\_BOOTS\_STOMP | 45 |
|  TF\_CUSTOM\_PLASMA | 46 |
|  TF\_CUSTOM\_PLASMA\_CHARGED | 47 |
|  TF\_CUSTOM\_PLASMA\_GIB | 48 |
|  TF\_CUSTOM\_PRACTICE\_STICKY | 49 |
|  TF\_CUSTOM\_EYEBALL\_ROCKET | 50 |
|  TF\_CUSTOM\_HEADSHOT\_DECAPITATION | 51 |
|  TF\_CUSTOM\_TAUNT\_ARMAGEDDON | 52 |
|  TF\_CUSTOM\_FLARE\_PELLET | 53 |
|  TF\_CUSTOM\_CLEAVER | 54 |
|  TF\_CUSTOM\_CLEAVER\_CRIT | 55 |
|  TF\_CUSTOM\_SAPPER\_RECORDER\_DEATH | 56 |
|  TF\_CUSTOM\_MERASMUS\_PLAYER\_BOMB | 57 |
|  TF\_CUSTOM\_MERASMUS\_GRENADE | 58 |
|  TF\_CUSTOM\_MERASMUS\_ZAP | 59 |
|  TF\_CUSTOM\_MERASMUS\_DECAPITATION | 60 |
|  TF\_CUSTOM\_CANNONBALL\_PUSH | 61 |
|  TF\_CUSTOM\_TAUNT\_ALLCLASS\_GUITAR\_RIFF | 62 |
|  TF\_CUSTOM\_THROWABLE | 63 |
|  TF\_CUSTOM\_THROWABLE\_KILL | 64 |
|  TF\_CUSTOM\_SPELL\_TELEPORT | 65 |
|  TF\_CUSTOM\_SPELL\_SKELETON | 66 |
|  TF\_CUSTOM\_SPELL\_MIRV | 67 |
|  TF\_CUSTOM\_SPELL\_METEOR | 68 |
|  TF\_CUSTOM\_SPELL\_LIGHTNING | 69 |
|  TF\_CUSTOM\_SPELL\_FIREBALL | 70 |
|  TF\_CUSTOM\_SPELL\_MONOCULUS | 71 |
|  TF\_CUSTOM\_SPELL\_BLASTJUMP | 72 |
|  TF\_CUSTOM\_SPELL\_BATS | 73 |
|  TF\_CUSTOM\_SPELL\_TINY | 74 |
|  TF\_CUSTOM\_KART | 75 |
|  TF\_CUSTOM\_GIANT\_HAMMER | 76 |
|  TF\_CUSTOM\_RUNE\_REFLECT | 77 |
|  TF\_CUSTOM\_DRAGONS\_FURY\_IGNITE | 78 |
|  TF\_CUSTOM\_DRAGONS\_FURY\_BONUS\_BURNING | 79 |
|  TF\_CUSTOM\_SLAP\_KILL | 80 |
|  TF\_CUSTOM\_CROC | 81 |
|  TF\_CUSTOM\_TAUNTATK\_GASBLAST | 82 |

#### `placement (Required)`

<table>
  <thead>
    <tr>
      <th style="text-align:left">Parameter</th>
      <th style="text-align:left">Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left"><code>placement;pos;all/my/other</code>
      </td>
      <td style="text-align:left">
        <p>Be the top X players left alive (usually for arena, no respawn gamemodes)</p>
        <p></p>
        <p><code>;pos</code> is the number of players left <b>(including the player)</b>
        </p>
        <ul>
          <li><code>;all</code> to check the number of players left alive in both teams</li>
          <li><code>;my</code> to check the number of players left alive in the player&apos;s
            team</li>
          <li><code>;other</code> to check the number of players left alive in the other
            team</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>
{% endtab %}
{% endtabs %}

## Other Parameters

To make things neater, maps and gamemodes function the same way but are separated from the main parameters.

### Gamemodes

* Separate with commas, spaces are allowed for each gamemode name. 
* `*` __infront of a name if you want the challenge to match gamemodes **CONTAINING** that name. Otherwise, the challenge will match gamemodes with the exact naming. 
* `#` at the end of a gamemode name if you want the challenge to match case-sensitively. 
* `!NOT` at the end of a gamemode name if you don't want the challenge to track in that gamemode.



### Maps

* Separate with commas, no spaces allowed for each map name. 
* `*` __infront of a name if you want the challenge to match maps **CONTAINING** that name. Otherwise, the challenge will match maps with the exact naming. 
* `#` at the end of a map name if you want the challenge to match case-sensitively. 
* `!NOT` at the end of a map name if you don't want the challenge to track in that map.

#### Mann vs Machine

* To indicate a Mann vs Machine mission, simply indicate its mission/popfile name after the map name. A mission called Ambush on mvm\_decoy, will be `mvm_decoy_Ambush`. 
* To indicate a specific wave of a mission, add `;wave<number>` behind the map \(map\_mission\) name. For example, `mvm_decoy_Ambush;wave3` to indicate the 3rd wave of Ambush mission on mvm\_decoy.

**Note that if you are indicating that a challenge can be done in any mission of a MvM map, it should include a `*` infront of the map name. Otherwise, it can only be done in the default mission of that map.**

