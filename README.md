# Vedubox Keepalive

Bu repo, Vedubox görev botunun Render.com servisini uyandırmak için kullanılan **yedek** keepalive repo'sudur. Birincil keepalive, SteadyCron üzerindeki 3 ücretsiz HTTP işidir (birleşince 5 dakikada bir).

- Botun asıl (private) repo'su ayrı tutulur.
- Render servisinin `/kontrol` adresi bu repoda **GitHub Actions secret** (`CRON_URL`) olarak saklanır; workflow dosyasında veya loglarda görünmez.
- `.github/workflows/keepalive.yml` her 5 dakikada bir isteği gönderir.
- GitHub Actions planlı işleri bazen saatlerce geciktirebilir veya yeni public repolarda hiç çalışmayabilir. Bu yüzden bu repo yalnızca yedektir; birincil katman SteadyCron'dur.

## Not

Bu repo public olduğu için GitHub Actions dakikaları ücretsizdir. İçinde şifre, bot token'ı veya görev verisi yoktur.
