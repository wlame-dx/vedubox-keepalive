# Vedubox Keepalive

Bu repo, Vedubox görev botunun Render.com servisini 5 dakikada bir uyandırmak için kullanılan **yardımcı** repodur.

- Botun asıl (private) repo'su ayrı tutulur.
- Render servisinin `/kontrol` adresi bu repoda **GitHub Actions secret** (`CRON_URL`) olarak saklanır; workflow dosyasında veya loglarda görünmez.
- `.github/workflows/keepalive.yml` her 5 dakikada bir isteği gönderir.
- GitHub Actions planlı işleri bazen birkaç dakika geciktirebilir. Daha kesin zamanlama için cron-job.org gibi bir servis de kullanılabilir.

## Not

Bu repo public olduğu için GitHub Actions dakikaları ücretsizdir. İçinde şifre, bot token'ı veya görev verisi yoktur.
