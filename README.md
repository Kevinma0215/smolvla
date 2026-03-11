# Reading Note
```bash
lerobot-train \
  --policy.path=lerobot/smolvla_base \
  --policy.repo_id=CLM0215/smolvla_pick_cube \
  --dataset.repo_id=CLM0215/pick_cube_test2 \
  --batch_size=16 \
  --steps=20000 \
  --output_dir=outputs/train/smolvla_try4 \
  --job_name=smolvla_training \
  --policy.device=cuda \
  --wandb.enable=true \
  --policy.scheduler_decay_lr=1e-5 \
  --policy.empty_cameras=2 \
  --rename_map='{"observation.images.front":"observation.images.camera1"}'
  ```