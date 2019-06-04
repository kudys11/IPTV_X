# IPTV

Collection of 6000+ free IPTV channels from all over the world.

## Usage

### VLC Player

To open the playlist in VLC player you just need click `File` - > `Open Network...` and in the window that opens, insert a link to the playlist itself: `https://raw.githubusercontent.com/kudys11/IPTV_X/master/index.m3u`

![VLC Network Panel](https://github.com/freearhey/iptv/raw/master/preview.png)

then just press the 'Open' button

### Android

To watch IPTV on your Android device you can use any player with support M3U-playlists and this playlist: [https://raw.githubusercontent.com/freearhey/iptv/master/index.all.m3u](https://raw.githubusercontent.com/freearhey/iptv/master/index.all.m3u). Or select a playlist for a specific country from the list below.

### Plex App

In order to watch IPTV through Plex App, you can use the [Cigaras/IPTV.bundle](https://github.com/Cigaras/IPTV.bundle) plugin.


## Contribution

The easiest way to help the project is to sort channels by country. Specifically for this was created playlist `channels/unsorted.m3u` which contains channels that are not yet sorted by other playlists. If you recognize one of the channels in this playlist, just copy its title and link to the desired country playlist. That's it!

If you want to add new channel to the playlist you need add link to stream and some information about it. For example:

```xml
#EXTINF:-1 tvg-id="exampletv.us" tvg-name="Example TV" tvg-logo="http://example.com/channel-logo.png" group-title="News",Example TV
http://example.com/stream.m3u8
```

| Attribute   | Description
| ----------- | ---
| tvg-id      | Unique channel id that is used to load EPG. Here you can find id for most channels: https://xtream-editor.com/en/epg (optional)
| tvg-name    | Official channel name. In most cases, you can use the name listed here: https://xtream-editor.com/en/epg (optional)
| tvg-logo    | Logo of the channel from http://www.tv-logo.com/ (optional)
| group-title | One of the following categories: Auto, Business, CCTV, Entertainment, Food, General, Hobby, Kids, Local, Movies, Music, News, Religious, Shop, Sport, Travel, XXX (optional)

If you just found an error or have any suggestions on how to organize a playlist please send an [issue](https://github.com/freearhey/iptv/issues) or a [pull request](https://github.com/freearhey/iptv/pulls)


## Testing

```sh
npm run test
```

Be prepared test may take a long time. After the tests end all broken links will be saved to the file `error.log`.
