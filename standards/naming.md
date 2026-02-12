# Rockwell Tag Naming Conventions

## General Rules
- Use PascalCase with underscores between logical segments: `Motor_1_Running`
- Maximum 40 characters
- Start with a letter, not a number
- No spaces or special characters except underscores
- Be descriptive but concise

## Tag Name Structure

```
[Area]_[Equipment]_[Number]_[Function]
```

### Examples
| Tag Name | Meaning |
|----------|---------|
| `Motor_1_Running` | Motor 1 run status |
| `Motor_1_Start_PB` | Motor 1 start pushbutton |
| `Motor_1_Stop_PB` | Motor 1 stop pushbutton |
| `Motor_1_Overload` | Motor 1 overload fault |
| `Conv_1_Speed_SP` | Conveyor 1 speed setpoint |
| `Conv_1_Speed_PV` | Conveyor 1 speed process value |
| `Tank_1_Level_HH` | Tank 1 level high-high alarm |
| `Tank_1_Level_LL` | Tank 1 level low-low alarm |
| `Pump_1_Auto_Mode` | Pump 1 automatic mode |
| `Valve_1_Open_FB` | Valve 1 open feedback |

## Common Suffixes
| Suffix | Meaning | Data Type |
|--------|---------|-----------|
| `_PB` | Pushbutton | BOOL |
| `_FB` | Feedback | BOOL |
| `_SP` | Setpoint | REAL/DINT |
| `_PV` | Process Value | REAL |
| `_HH` | High-High Alarm | BOOL |
| `_H` | High Alarm | BOOL |
| `_L` | Low Alarm | BOOL |
| `_LL` | Low-Low Alarm | BOOL |
| `_TMR` | Timer | TIMER |
| `_CTR` | Counter | COUNTER |
| `_CMD` | Command | BOOL |
| `_STS` | Status | BOOL |
| `_FLT` | Fault | BOOL |
| `_EN` | Enable | BOOL |
| `_DN` | Done | BOOL |

## Scope Guidelines
- **Controller scope**: Tags shared across programs, I/O tags, HMI tags
- **Program scope**: Tags local to a single program's logic
- Prefer program scope when the tag is only used within one program

## Anti-Patterns (Avoid)
- `Tag1`, `Tag2`, `Tag3` — not descriptive
- `temp`, `x`, `flag` — too generic
- `Motor_Running_Status_Bit_For_Motor_1` — too long
- `motorRunning` — wrong case convention (use PascalCase with underscores)
- `MOTOR_RUNNING` — ALL_CAPS reserved for constants only
