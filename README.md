# fsmlib

A simple Python-based finite state machine library.

Example of a two-state FSM with random event choice:

```python
from fsmlib import FSM
from fsmlib import get_random_next_event

simple_fsm = FSM(
  'idle',
  {('idle', 'start'): 'running', ('running', 'stop'): 'idle'}
)

next_event = get_random_next_event(simple_fsm)
simple_fsm.advance(next_event)
```
