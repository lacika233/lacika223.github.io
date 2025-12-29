<html lang="hu">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Fortnite Secret Pro Hub - NVIDIA & CPU Guide</title>
    <style>
        :root {
            --nvidia-green: #76b900;
            --fn-blue: #007bff;
            --cpu-gold: #ff9d00;
            --checklist-red: #ff4444;
            --bg: #0d0d0d;
            --card: #1a1a1a;
            --text: #ffffff;
        }
        body {
            font-family: 'Segoe UI', Roboto, sans-serif;
            background-color: var(--bg);
            color: var(--text);
            margin: 0;
            padding: 20px;
            line-height: 1.5;
        }
        .container { max-width: 1100px; margin: auto; }
        header { text-align: center; padding: 40px 0; border-bottom: 3px solid var(--nvidia-green); margin-bottom: 30px; }
        h1 { font-size: 2.5em; margin: 0; color: var(--nvidia-green); text-transform: uppercase; }
        
        .section-header {
            background: linear-gradient(90deg, var(--nvidia-green), transparent);
            padding: 12px 20px;
            border-radius: 5px;
            margin-top: 50px;
            font-size: 1.6em;
            font-weight: bold;
            text-transform: uppercase;
        }
        
        .grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(320px, 1fr));
            gap: 15px;
            margin-top: 20px;
        }
        .item {
            background: var(--card);
            padding: 15px;
            border-radius: 8px;
            border-left: 4px solid var(--nvidia-green);
        }
        .item span { color: var(--nvidia-green); font-weight: bold; display: block; margin-bottom: 5px; }
        .val { color: #ffcc00; font-family: monospace; font-size: 1.1em; }
        .desc { font-size: 0.85em; color: #aaa; margin-top: 5px; display: block; }

        .fn-section .item { border-left-color: var(--fn-blue); }
        .fn-header { background: linear-gradient(90deg, var(--fn-blue), transparent); }
        
        .cpu-header { background: linear-gradient(90deg, var(--cpu-gold), transparent); }
        .cpu-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(300px, 1fr)); gap: 20px; margin-top: 20px; }
        .cpu-card { background: #222; padding: 20px; border-radius: 12px; border: 1px solid var(--cpu-gold); }
        .cpu-card h3 { color: var(--cpu-gold); margin-top: 0; }

        .list-header { background: linear-gradient(90deg, var(--checklist-red), transparent); }
        .check-list-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 20px;
            background: #111;
            padding: 20px;
            border-radius: 10px;
            margin-top: 20px;
            border: 1px solid #333;
        }
        .check-list-container h4 { color: var(--checklist-red); border-bottom: 1px solid #444; padding-bottom: 5px; }
        .check-list-container li { font-size: 0.85em; margin-bottom: 5px; color: #ddd; }
    </style>
</head>
<body>

<div class="container">
    <header>
        <h1>ULTRA LOW LATENCY HUB</h1>
        <p>Profi útmutató a maximális FPS és 0 késleltetés eléréséhez</p>
    </header>

    <div class="section-header">🛠️ NVIDIA Profile Inspector (30 Secret Beállítás)</div>
    <div class="grid">
        <div class="item"><span>1. Maximum Pre-rendered Frames</span><div class="val">1</div><small class="desc">Minimálisra csökkenti az egérkésleltetést.</small></div>
        <div class="item"><span>2. Power Management Mode</span><div class="val">Prefer Maximum Performance</div><small class="desc">A GPU mindig a legmagasabb órajelen pörög.</small></div>
        <div class="item"><span>3. Texture Filtering - Quality</span><div class="val">High Performance</div><small class="desc">Kikapcsolja a felesleges képjavítókat az FPS-ért.</small></div>
        <div class="item"><span>4. Vertical Sync</span><div class="val">Force Off</div><small class="desc">Megszünteti az input lagot okozó szinkronizációt.</small></div>
        <div class="item"><span>5. Threaded Optimization</span><div class="val">On</div><small class="desc">Segít a többmagos processzorok kihasználásában.</small></div>
        <div class="item"><span>6. Shader Cache Size</span><div class="val">Unlimited</div><small class="desc">Megakadályozza a játék alatti akadást (stuttering).</small></div>
        <div class="item"><span>7. Low Latency Mode</span><div class="val">Ultra</div><small class="desc">Azonnali válaszidő a GPU és CPU között.</small></div>
        <div class="item"><span>8. Triple Buffering</span><div class="val">Off</div><small class="desc">Kikapcsolva csökkenti a késleltetést.</small></div>
        <div class="item"><span>9. Ambient Occlusion</span><div class="val">Off</div><small class="desc">Több FPS és tisztább látási viszonyok.</small></div>
        <div class="item"><span>10. Antialiasing - Mode</span><div class="val">Override any setting</div><small class="desc">Felülbírálja a lassító élsimításokat.</small></div>
        <div class="item"><span>11. Antialiasing - Setting</span><div class="val">None / Off</div><small class="desc">Élesebb kép, kevesebb GPU terhelés.</small></div>
        <div class="item"><span>12. Gamma Correction</span><div class="val">Off</div><small class="desc">Kikapcsolásával nyerhetsz pár extra FPS-t.</small></div>
        <div class="item"><span>13. Transparency Multisampling</span><div class="val">Disabled</div><small class="desc">Átlátszó textúrák gyorsabb betöltése.</small></div>
        <div class="item"><span>14. CUDA - GPUs</span><div class="val">All</div><small class="desc">Biztosítja, hogy az összes magot használja a kártya.</small></div>
        <div class="item"><span>15. G-SYNC - Global Feature</span><div class="val">Off</div><small class="desc">A profi 0 delay setup alapköve.</small></div>
        <div class="item"><span>16. Preferred Refresh Rate</span><div class="val">Highest Available</div><small class="desc">A monitorod maximumát használja.</small></div>
        <div class="item"><span>17. SILK Smoothness</span><div class="val">Off</div><small class="desc">Kikapcsolja a simítást a nyers sebességért.</small></div>
        <div class="item"><span>18. Memory Allocation Policy</span><div class="val">Aggressive Pre-allocation</div><small class="desc">Gyorsabb memóriakezelés a GPU-nak.</small></div>
        <div class="item"><span>19. Ansel Flag</span><div class="val">Disallowed</div><small class="desc">Letiltja a háttérben futó fotó módot.</small></div>
        <div class="item"><span>20. Extension Limit</span><div class="val">Off</div><small class="desc">Régi korlát kikapcsolása.</small></div>
        <div class="item"><span>21. Texture Filtering - Sample Opt.</span><div class="val">On</div><small class="desc">Optimalizált textúra mintavételezés.</small></div>
        <div class="item"><span>22. Anisotropic Filtering Setting</span><div class="val">Off</div><small class="desc">Kevesebb részlet távolról, több FPS.</small></div>
        <div class="item"><span>23. Virtual Reality Pre-rendered Frames</span><div class="val">1</div><small class="desc">VR nélkül is segít a renderelési sorban.</small></div>
        <div class="item"><span>24. Multi-display Acceleration</span><div class="val">Single Display Perf Mode</div><small class="desc">Ha egy monitoron játszol, ez a leggyorsabb.</small></div>
        <div class="item"><span>25. FXAA Usage</span><div class="val">Disallowed</div><small class="desc">Letiltja az elmosódott élsimítást.</small></div>
        <div class="item"><span>26. Antialiasing - Transparency Supersampling</span><div class="val">Off</div><small class="desc">Extra GPU erőforrást szabadít fel.</small></div>
        <div class="item"><span>27. Texture Filtering - Anisotropic Opt.</span><div class="val">On</div><small class="desc">Gyorsítja a textúra szűrést.</small></div>
        <div class="item"><span>28. Frame Rate Limiter</span><div class="val">Off</div><small class="desc">A késleltetés miatt érdemes a játékon belül korlátozni.</small></div>
        <div class="item"><span>29. G-SYNC - Indicator Overlay</span><div class="val">Off</div><small class="desc">Felesleges vizuális elem eltávolítása.</small></div>
        <div class="item"><span>30. Toggle FXAA</span><div class="val">Off</div><small class="desc">Garantáltan kikapcsolt élsimítás.</small></div>
    </div>

    <div class="section-header fn-header">🎮 Fortnite Játékbeli Beállítások (Angol néven)</div>
    <div class="grid fn-section">
        <div class="item"><span>Display Mode</span><div class="val">Full Screen</div><small class="desc">Csak így lesz a legkisebb a késleltetés.</small></div>
        <div class="item"><span>Rendering Mode</span><div class="val">Performance (Alpha)</div><small class="desc">A legmagasabb FPS-t adó mód.</small></div>
        <div class="item"><span>NVIDIA Reflex</span><div class="val">On + Boost</div><small class="desc">Közvetlen kapcsolat a CPU és GPU között.</small></div>
        <div class="item"><span>Meshes</span><div class="val">Low</div><small class="desc">Mobil-szerű építmények a maximális átláthatóságért.</small></div>
        <div class="item"><span>Report Performance Stats</span><div class="val">Disabled</div><small class="desc">Titkos FPS gyilkos, kapcsold ki!</small></div>
        <div class="item"><span>Record Replays</span><div class="val">All Off</div><small class="desc">Sokat segít, ha nem kell a CPU-nak rögzítenie.</small></div>
    </div>

    <div class="section-header cpu-header">🧠 Milyen CPU kell a Fortnite-hoz?</div>
    <div class="cpu-grid">
        <div class="cpu-card"><h3>🥉 Budget (144 FPS)</h3><p>Ryzen 5 3600 / Intel i5-10400F. Belépő szintű stabil játékhoz.</p></div>
        <div class="cpu-card" style="border-width: 3px;"><h3>🥈 Mid-Range (240 FPS+)</h3><p>Ryzen 5 7600 / Intel i5-14400F. Versenyszintű teljesítmény.</p></div>
        <div class="cpu-card" style="background: #2a1a00;"><h3>🥇 Pro (540 FPS+)</h3><p><strong>Ryzen 7 7800X3D</strong> - Jelenleg ez a király a 3D Cache miatt.</p></div>
    </div>

    <div class="section-header list-header">🚀 70 Lépéses Ultimate FPS Lista</div>
    <div class="check-list-container">
        <div><h4>Rendszer (1-25)</h4><ul>
            <li>Game Mode: ON (Be)</li>
            <li>HAGS: ON (Be)</li>
            <li>Background Apps: OFF (Ki)</li>
            <li>Power Plan: Ultimate Performance</li>
            <li>Startup Apps: Minden felesleges OFF</li>
            <li>Transparency Effects: OFF</li>
            <li>Notifications: OFF</li>
            <li>UAC: OFF (Soha ne értesítsen)</li>
            <li>Delivery Optimization: OFF</li>
            <li>Windows Update: Done</li>
            <li>Game Bar: OFF</li>
            <li>Hibernation: OFF</li>
            <li>Storage Sense: OFF</li>
            <li>Visual Effects: Best Performance</li>
            <li>Core Parking: Disabled</li>
            <li>Disk Cleanup: Rendszerfájlok törlése</li>
            <li>Registry: NetworkThrottlingIndex ffffffff</li>
            <li>Registry: SystemResponsiveness 0</li>
            <li>High Precision Event Timer (HPET): OFF</li>
            <li>Search Indexing: OFF</li>
            <li>Telemetry: OFF</li>
            <li>OneDrive: Uninstall</li>
            <li>News and Interests: OFF</li>
            <li>Fast Boot: OFF</li>
            <li>Pointer Precision: OFF</li>
        </ul></div>
        <div><h4>Hálózat & Késleltetés (26-50)</h4><ul>
            <li>DNS: 1.1.1.1 (Cloudflare)</li>
            <li>IPv6: Disabled (Hálózati kártyánál)</li>
            <li>Energy Efficient Ethernet: OFF</li>
            <li>Green Ethernet: OFF</li>
            <li>Timer Resolution: 0.5ms (Fixálva)</li>
            <li>FSO: Disable (Fortnite.exe-n)</li>
            <li>High Priority: Fortnite.exe</li>
            <li>USB Power Saving: OFF</li>
            <li>Key Repeat Rate: Fast</li>
            <li>Filter Keys: OFF</li>
            <li>Discord Overlay: OFF</li>
            <li>Hardware Acceleration: OFF (Chrome/DC)</li>
            <li>NVIDIA Overlay: OFF</li>
            <li>Steam Overlay: OFF</li>
            <li>TCP No Delay: ON</li>
            <li>Interrupt Moderation: OFF</li>
            <li>Flow Control: OFF</li>
            <li>Jumbo Packet: OFF</li>
            <li>Speed & Duplex: 1.0 Gbps Full</li>
            <li>Flush DNS: Command Promptban</li>
            <li>WIFI helyett kábel (LAN)</li>
            <li>Router Firmware: Frissítve</li>
            <li>Background Downloads: Pause</li>
            <li>Limit Reserved Bandwidth: 0%</li>
            <li>Clear %temp% mappa</li>
        </ul></div>
        <div><h4>BIOS & Hardver (51-70)</h4><ul>
            <li>XMP / DOCP Profile: ON</li>
            <li>Resize BAR: ON</li>
            <li>Precision Boost Overdrive: Enabled</li>
            <li>C-States: OFF</li>
            <li>Monitor Overdrive: Fast</li>
            <li>Dual Channel RAM check</li>
            <li>PCIe Gen: Max</li>
            <li>GPU Driver: DDU Clean Install</li>
            <li>Fan Curve: Performance</li>
            <li>SATA Mode: AHCI</li>
            <li>BIOS Update: Latest</li>
            <li>Thermal Paste: Friss csere</li>
            <li>Dust: Portalanítás</li>
            <li>Keyboard Polling: 1000Hz+</li>
            <li>Mouse Polling: 1000-8000Hz</li>
            <li>Sound Quality: Low</li>
            <li>Replays: All OFF</li>
            <li>3D Res: 100%</li>
            <li>Visualize Sound: ON</li>
            <li>Verify Files: Epic Games</li>
        </ul></div>
    </div>

    <footer><p>© 2025 Fortnite Secret Pro Hub - Frissítve a legújabb szezonhoz</p></footer>
</div>
</body>
</html>
