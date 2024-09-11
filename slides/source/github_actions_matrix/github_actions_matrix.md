

# Github Actions Matrix

---
## 

<grid  drag="80 100" drop="center"  flow="col">
## Origin story

<p style="font-size:24px">
We found out about matrix option in Github actions by our sister company `NBCU` engineering team, when they opened up few PRs on mamba repo.
</p>

<p style="font-size:24px">
We were always duplicating some code to initialize, build and test for every jobs previously. We utilized `reusable workflows` and `global variables` for jobs.
</p>

<p style="font-size:24px">
But we still had code duplication where only 2 parameters were unique in our `n` number of jobs. 
</p>

- Scheme
- Device Type

</grid>

---

## 

<grid  drag="80 100" drop="center"  flow="col">

## Development

<p style="font-size:24px">
Matrix Strategy is just basic maths. eg. Input1 = [X, Y] Input2 = [1, 2, 3, 4]
Output: [
[X1, X2, X3, X4],
[Y1, Y2, Y3, Y4]
]
</p>

<p style="font-size:24px">
We made sure that the new improvements brought in with the PR, shouldn't lose us our previous functionalities. Most important one was `failable` restarts.
</p>

<p style="font-size:24px">
This is supported in Matrix by providing an extra parameter called 
`fail-fast: Bool`, which made sure all the other independent modules are still tested even if one fails.
</p>

[Github Docs | Matrix](https://docs.github.com/en/actions/writing-workflows/choosing-what-your-workflow-does/running-variations-of-jobs-in-a-workflow#using-a-matrix-strategy)


</grid>

---

## 

<grid drag="90 20" drop="5 30">

## Improvements

[CI Matrix PR](https://github.com/comcast-viper-player/nitro-player-apple/pull/205/files?diff=split&w=0)

- 194 LOC => 94 LOC

- Went from 5 to 9 Jobs

- Quick Glance of Jobs

</grid>


<grid drag="90 60" drop="5 60" style="font-size:18px">

![[Screenshot 2024-09-06 at 4.04.59 PM.png]]

</grid>







---

## Limitations

<p style="font-size:18px">
Even when we have enabled multi processing | parallelization on our CI jobs. Github doesn't provide support this feature for users utilizing one custom runner.
</p>


<p style="font-size:18px">
We can always pool our custom runners and utilize them to run parallel jobs but that would be competing over CI compute resources from other cross teams.
</p>

![[Screenshot 2024-09-11 at 11.29.51 AM.png]]
