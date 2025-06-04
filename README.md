# REVERSEBIAS
% Parameters
Is = 1e-12; % Saturation current (A)
n = 1.5;    % Ideality factor
Vt = 0.025; % Thermal voltage (V) at room temperature
V = -5:0.01:1; % Voltage range (V), emphasizing reverse bias (V < 0)

% Diode current using Shockley equation
I = Is * (exp(V / (n * Vt)) - 1);

% Plot I-V characteristics
figure;
plot(V, I, 'b', 'LineWidth', 2);
grid on;
title('Diode I-V Characteristics (Reverse and Forward Bias)');
xlabel('Voltage (V)');
ylabel('Current (A)');
xlim([-5 1]);
ylim([-1e-9 1e-3]); % Adjusted for visibility
set(gca, 'YScale', 'linear'); % Linear scale for clarity
