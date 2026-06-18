# AGENTS.md — CPoW World

**Not a game.** Data-creation autonomous simulation (CPoW). See `docs/CPOW_ARCHITECTURE.md`.

**Canonical repo:** https://github.com/weed97/cpow_world

## Layout

| Path | Role |
|------|------|
| `cpow_engine/` | Physics, CPoW, areas, governance, `world/` (biomes, mining) |
| `cpow_api/` | FastAPI — `/v1/areas/*`, `/v1/world/*`, auth |
| `cpow_client/unity/` | **Unity 2022.3+** 3D client — chunk streaming |
| `cpow_client/godot/` | Legacy Godot prototype |

## Commands

```bash
pip install -r requirements-api.txt
python3 -m cpow_engine.demo --areas
uvicorn cpow_api.server:app --host 127.0.0.1 --port 8765
bash scripts/verify.sh
```

Unity: open `cpow_client/unity/CPoWWorld` (API server required).
