# noise.dog
A noise generator that runs in the browser. 
- no ads, upsells, or tracking
- keyboard controls
- multiple ambient presets
- cool dog

Available online for free at [noise.dog](https://noise.dog).

Developed by [fancymatt](https://fancyma.tt)

---

## Development

This is a static site — one `index.html` + `images/`. No build step.

**Local dev setup:**
```bash
git clone git@github.com:fancymatt/noise.dog.git
cd noise.dog
# Open index.html in a browser — no server required for basic dev.
# For AudioContext to work, serve locally:
npx serve . # or python3 -m http.server 8080
```

## Deploy

**Workflow: local → GitHub → Yaguchi**

1. Make changes locally in `/home/fancymatt/noise.dog`
2. Test in browser before committing
3. Commit and push to GitHub:
   ```bash
   git add -A
   git commit -m "your message"
   git push origin main
   ```
4. Deploy to production (Yaguchi):
   ```bash
   ssh root@146.190.2.164 'cd /var/www/noise.dog && git pull origin main'
   ```

**Do not edit files directly on the server.**

Production server: Yaguchi (146.190.2.164), nginx, `/var/www/noise.dog/`
