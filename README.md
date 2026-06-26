<html lang="bn">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Kiron-Tech - সম্পূর্ণ ফ্রি লাইভ স্ট্রিমিং</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://vjs.zencdn.net/8.3.0/video-js.css" rel="stylesheet" />
    <script src="https://vjs.zencdn.net/8.3.0/video.min.js"></script>
    <style>
        body { background-color: #0b0f19; color: #fff; }
        .hero-bg { background: linear-gradient(to bottom, rgba(11, 15, 25, 0.4), #0b0f19), url('https://photos.app.goo.gl/pszS45XEfzvFhjaY7') no-repeat center center/cover; }
        .channel-card:hover { transform: translateY(-5px); border-color: #10b981; }
    </style>
</head>
<body>

    <header class="sticky top-0 z-50 bg-[#0f172a]/90 backdrop-blur-md border-b border-gray-800">
        <div class="container mx-auto px-6 py-4 flex justify-between items-center">
            <a href="#" class="text-2xl font-black text-emerald-500">Kiron <span class="text-white">Tech</span></a>
            <span class="bg-emerald-600 px-4 py-1.5 rounded-full text-xs font-bold uppercase tracking-widest">সম্পূর্ণ ফ্রি</span>
        </div>
    </header>

    <section class="hero-bg py-12">
        <div class="container mx-auto px-6">
            <div class="max-w-4xl mx-auto">
                <div class="bg-gray-900/60 p-4 rounded-2xl border border-gray-800 shadow-2xl">
                    <video id="pstu-player" class="video-js vjs-big-play-centered w-full aspect-video rounded-xl" controls preload="auto" data-setup='{}'>
                        <source src="https://live.thebosstv.com:30443/dwlive/Somoy-TV/chunks.m3u8" type="application/x-mpegURL">
                    </video>
                </div>
                <div class="mt-4 text-center">
                    <h2 id="channel-title" class="text-xl font-bold text-emerald-400">বর্তমানে চলছে: Somoy TV</h2>
                </div>
            </div>
        </div>
    </section>

    <section class="py-12 bg-[#090d16]">
        <div class="container mx-auto px-6">
            <h2 class="text-2xl font-bold mb-8 border-l-4 border-emerald-500 pl-4">সকল চ্যানেল লিস্ট</h2>
            <div id="channel-grid" class="grid grid-cols-2 sm:grid-cols-3 md:grid-cols-4 lg:grid-cols-5 gap-4">
                </div>
        </div>
    </section>

    <footer clss="py-8 text-center text-gray-600 border-t border-gray-800">
        <p>&copy; 2026 Kiron. All Rights Reserved.</p>
    </footer>

    <script>
        // আপনার দেওয়া ৫টি লাইভ চ্যানেলের লিস্ট এখানে সাজানো হয়েছে
        const channels = [
        {
                id: 1,
                name: "BTV",
                streamUrl: "https://owrcovcrpy.gpcdn.net/bpk-tv/1709/output/1709-audio_113392_eng=113200-video=2202800.m3u8",
                logo: "https://images.seeklogo.com/logo-png/45/1/btv-bangladesh-television-logo-png_seeklogo-459657.png"
            },
            {
                id: 7,
                name: "Machranga HD",
                streamUrl: "https://owrcovcrpy.gpcdn.net/bpk-tv/1722/output/1722-audio_113522_eng=113200-video=2202800.m3u8",
                logo: "https://mail.maasranga.tv/public/customize/newImage/logo.png"
            },
            {
                id: 6,
                name: "Somoy TV",
                streamUrl: "https://live.thebosstv.com:30443/dwlive/Somoy-TV/chunks.m3u8",
                logo: "https://images.seeklogo.com/logo-png/53/1/somoy-tv-logo-png_seeklogo-536972.png" // এখানে লোগোর লিংক দিতে পারেন
            },
            {
                id: 15,
                name: "Deepto TV HD",
                streamUrl: "https://owrcovcrpy.gpcdn.net/bpk-tv/1711/output/1711-audio_113412_eng=113200-video=2202800.m3u8",
                logo: "https://images.seeklogo.com/logo-png/51/1/deepto-tv-logo-png_seeklogo-513994.png"
            },
       {
                id: 9,
                name: "Channel I HD",
                streamUrl: "https://owrcovcrpy.gpcdn.net/bpk-tv/1723/output/1723-audio_113532_eng=113200-video=2202800.m3u8",
                logo: "https://images.seeklogo.com/logo-png/42/1/channel-i-logo-png_seeklogo-427745.png"
            },
            {
                id: 2,
                name: "bein Sports",
                streamUrl: "https://cp11.adabmedia.com/hls2/sport.m3u8",
                logo: "https://images.seeklogo.com/logo-png/31/1/bein-sport-logo-png_seeklogo-314494.png"
            },
            {
                id: 3,
                name: "RTB Go",
                streamUrl: "https://d1211whpimeups.cloudfront.net/smil:rtbgo/chunklist.m3u8",
                logo: "https://via.placeholder.com/150?text=RTB+Go"
            },
            {
                id: 4,
                name: "Ten Sports 1",
                streamUrl: "https://1nyaler.streamhostingcdn.top/stream/23/index.m3u8",
                logo: "https://via.placeholder.com/150?text=Stream+4"
            },
            {
                id: 5,
                name: "Sony Sports 2 HD",
                streamUrl: "https://bldcmprod-cdn.toffeelive.com/cdn/live/sony_sports_2_hd/playlist.m3u8",
                logo: "https://e7.pngegg.com/pngimages/362/254/png-clipart-star-sports-3-logo-television-channel-star-india-news-live-television-text-thumbnail.png"
            },      
     
            {
                id: 16,
                name: "Independent TV HD",
                streamUrl: "https://owrcovcrpy.gpcdn.net/bpk-tv/1704/output/1704-audio_113342_eng=113200-video=1692000.m3u8",
                logo: "https://e7.pngegg.com/pngimages/969/124/png-clipart-logo-bangladesh-independent-television-television-channel-design-television-text-thumbnail.png"
            },
            {
                id: 17,
                name: "Channel 1 HD",
                streamUrl: "https://owrcovcrpy.gpcdn.net/bpk-tv/1702/output/1702-audio_113322_eng=113200-video=2202800.m3u8",
                logo: "https://via.placeholder.com/150?text=Sony+Sports+2"
            },
            {
                id: 18,
                name: "Channel 9 HD",
                streamUrl: "https://owrcovcrpy.gpcdn.net/bpk-tv/1729/output/1729-audio_113592_eng=113200-video=2202800.m3u8",
                logo: "https://via.placeholder.com/150?text=Sony+Sports+2"
            },
            {
                id: 19,
                name: "Global TV HD",
                streamUrl: "https://stream.ottplus.live/live/global_tv_abr/live/global_tv_hd_720/chunks.m3u8",
                logo: "https://via.placeholder.com/150?text=Sony+Sports+2"
            },
            {
                id: 9,
                name: "Sangeet Bangla HD",
                streamUrl: "https://cdn-4.pishow.tv/live/1143/master.m3u8",
                logo: "https://via.placeholder.com/150?text=Sony+Sports+2"
            },
            {
                id: 10,
                name: "Channel 24 HD",
                streamUrl: "https://owrcovcrpy.gpcdn.net/bpk-tv/1703/output/1703-audio_113332_eng=113200-video=2202800.m3u8",
                logo: "https://images.seeklogo.com/logo-png/42/1/channel-24-logo-png_seeklogo-424910.png"
            },
            {
                id: 11,
                name: "NTV HD",
                streamUrl: "https://owrcovcrpy.gpcdn.net/bpk-tv/1716/output/1716-audio_113462_eng=113200-video=2202800.m3u8",
                logo: "https://images.seeklogo.com/logo-png/39/1/ntv-channel-logo-png_seeklogo-396286.png"
            },
            {
                id: 12,
                name: "Star News HD",
                streamUrl: "https://owrcovcrpy.gpcdn.net/bpk-tv/1710/output/1710-audio_113402_eng=113200-video=3224800.m3u8",
                logo: "https://starnews.com.bd/image/mob_logo.png"
            },
            {
                id: 13,
                name: "T Sports HD",
                streamUrl: "https://trs1.aynaott.com/tsports/tracks-v1a1/mono.ts.m3u8",
                logo: "https://images.seeklogo.com/logo-png/64/1/t-sports-logo-png_seeklogo-640172.png"
            },
            {
                id: 14,
                name: "Ekattor TV HD",
                streamUrl: "https://owrcovcrpy.gpcdn.net/bpk-tv/1705/output/1705-audio_113352_eng=113200-video=2202800.m3u8",
                logo: "https://cdn.ekattorbd.com/contents/themes/public/style/images/logo.png"
            }
        ];

        const grid = document.getElementById('channel-grid');
        const player = videojs('pstu-player');

        // গ্রিড রেন্ডার করা
        channels.forEach(ch => {
            const card = document.createElement('div');
            card.className = "channel-card bg-[#0f172a] p-4 rounded-xl border border-gray-800 cursor-pointer text-center transition-all duration-200";
            card.innerHTML = `
                <img src="${ch.logo}" class="w-16 h-16 rounded-full mx-auto mb-3 object-cover border border-gray-700">
                <h3 class="font-bold text-sm text-gray-200">${ch.name}</h3>
            `;
            card.onclick = () => playStream(ch.streamUrl, ch.name);
            grid.appendChild(card);
        });

        // প্লেয়ার ফাংশন
        function playStream(url, name) {
            player.src({ src: url, type: 'application/x-mpegURL' });
            player.play();
            document.getElementById('channel-title').innerText = "বর্তমানে চলছে: " + name;
            window.scrollTo({ top: 0, behavior: 'smooth' });
        }
    </script>
</body>
</html>
