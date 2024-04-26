# CSE 168 HW2 extra credit

## Reduce Variance
- In order to reduce variance, we no longer choose random points but choos the center point of each stratum (except visibility), thus other variables involve the point on light will also change. It's hard to see on a sigle graph for the reduce variance, so below is the link of UCSD online that record our low variance graphs:
[UCSD online low variance](https://raviucsdgroup.s3.amazonaws.com/homework2/8f413eb1973ecc987b84bdeda0340468/20240426041609/index.html)
It shows that our variance is lower than the expected variance. (And can see there is a trade-off between bias and variance)





## Point Light
- For point light, we use the formula $L_d(\omega_o) = \frac{I}{R^2} f(\omega_i, \omega_o)(n · \omega_i)V(\omega_i)$
- It's basically similar to the formula of area light, but change the random point we choose from the area to the position of the point light, and thus the incident direction would change. And we no longer need to use N, since their units are different, we use the radiance over the square of distance to ligth.
- right below is the original graph and left below is the graph produced by the cornell.test with adding a pointlight
```
point 0 0.44 2 0.8 0.8 0.8
```
![Image](cornell_point.png)
![Image](cornell.png)

- We can see that there is a white point on the sphere, the entire scene became a bit brighter, and on the background there are light shadows of the sphere and cube.

## Directional Light
- For directional light, we use the formula $L_d(\omega_o) = E f(\omega_i, \omega_o)(n · \omega_i)V(\omega_i)$, where $E = L_i \Delta \omega$. This is also very similar to the area light but we do not use the area, and the incident direction became the opposite of direction of the light, and use the occulsion function of directional light.
- right below is the original graph and left below is the graph produced by the cornell.test with adding a directional light
```
directional -0.3 0.2 -0.5 0.8 0.9 0.3
```
![Image](cornell_directional.png)
![Image](cornell.png)
- We make the light color yellow so that we can clearly see the effect that the light project to the cube and sphere, and there are shadows on the background, and because of the direction of the light, the red wall became a bit brighter.
