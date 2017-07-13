# fsmlib -- a Python-based finite state machine library

```python
simple_fsm = FSM(
  'idle',
  {('idle', 'start'): 'running', ('running', 'stop'): 'idle'}
)

next_event = get_random_next_event(simple_fsm)
simple_fsm.advance(next_event)
