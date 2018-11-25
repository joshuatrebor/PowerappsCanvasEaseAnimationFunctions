# Ease In Quad
Power([Timer's Value]/[Timer's Duration],2)*([Max Target]-[Min Target])+[Min Target]

# Ease Out Quad
(1-Power(1-[Timer's Value]/[Timer's Duration],2))*([Max Target]-[Min Target])+[Min Target]

# Ease Out Elastic
(Power(2,-10*[Timer's Value]/[Timer's Duration]) * Sin(([Timer's Value]/[Timer's Duration]-.3/4)*(2*Pi())/.3) + 1)*([Max Target]-[Min Target])+[Min Target]

# Ease In Circle
(1-Sqrt( 1 - ([Timer's Value]/[Timer's Duration])*([Timer's Value]/[Timer's Duration])))*([Max Target]-[Min Target])+[Min Target]

# Ease Out Back
(1 + ([Timer's Value]/[Timer's Duration]-1)*([Timer's Value]/[Timer's Duration]-1)*(([Timer's Value]/[Timer's Duration]-1)*(1.70158+1) + 1.70158))*([Max Target]-[Min Target])+tmin

# Ease Out Bounce
(If(([Timer's Value]/[Timer's Duration])<1/2.75,7.5625*([Timer's Value]/[Timer's Duration])*([Timer's Value]/[Timer's Duration]),If(([Timer's Value]/[Timer's Duration])<2*1/2.75,7.5625*(([Timer's Value]/[Timer's Duration])-1.5*1/2.75)*(([Timer's Value]/[Timer's Duration])-1.5*1/2.75)+.75,If(([Timer's Value]/[Timer's Duration])<2.5*1/2.75,7.5625*(([Timer's Value]/[Timer's Duration])-2.25*1/2.75)*(([Timer's Value]/[Timer's Duration])-2.25*1/2.75)+0.9375,7.5625 * (([Timer's Value]/[Timer's Duration])-2.625*1/2.75)*(([Timer's Value]/[Timer's Duration])-2.625*1/2.75)+0.984375))))*([Max Target]-[Min Target])+[MinTarget]
