# Intuitive IPC

## Main idea

Model the distance threshold/tolerance where the IPC barrier functions kick in as a deformation response to objects with finite thickness

## 2D Simple
 
Consider a line segment

The "true" geometry is a rectangle with some thickness `r`

Consider the endpoint of another line segment approaching the middle of the segment.  That point deforms the rectangle by "notching" it

If the distance from the endpoint to the line is `d` (ie the min distance between the 2 segments is `d`) then the boundary of the segment of interest is 2 line segments whose heights vary linearly from `r` to `d` over some distance.  Call the barycentric coordinate of the notch `s`

Consider the energy density as $$1/h(\alpha)$$ where `h` is the "height" and "alpha" is the barycentric coordinate along that line

The energy of one of those segments is:

$$
\int_0^s 1/(r - \alpha(r-d)/s) d\alpha
$$

$$
= -log(r - \alpha(r - d)/s)/((r - d)/s) 
$$

evaluated at $0, s$

$$
= s*log(r/d)/(r - d)
$$

Which is quite similar to the IPC barrier functions!