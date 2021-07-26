# VAST-2.0-spec
Vast 2.0 Proof of concept

# Testing

Listed below is the proof of concept VAST tag in correspondence with the VAST_2.0 spec sheet. Currently, I've found we can track activity via our image tags.
I'd advise we get in touch with the vendor serving the VAST tag if we want to integrate some javascript into it since some vendors allow us to add javascript
and some vendors do not.

The VAST_2.0 specification sheet is publicly available [here for reference](https://iabtechlab.com/wp-content/uploads/2016/04/VAST-2_0-FINAL.pdf)

## Copy the contents of `vast_2.0.xml`

For convenience, it will be below:

```xml
<VAST version="2.0">
	<Ad id="proof-of-concept">
		<InLine>
		<AdSystem>2.0</AdSystem>
		<AdTitle>420</AdTitle>
		<Impression id="Impression pixel">
		<![CDATA[
		https://collector.dmp.cnna.io/i?&e=pv&page=vast&url=vast&aid=vast&p=web&tv=no-js-0.1.0
		]]>
		</Impression>
		<Creatives>
			<Creative>
				<Linear>
					<Duration>00:00:30</Duration>
					<TrackingEvents></TrackingEvents>
					<VideoClicks>
					<ClickThrough id="mediajel">
					<![CDATA[ https://www.mediajel.com/]]>
					</ClickThrough>
					</VideoClicks>
					<MediaFiles>
						<MediaFile height="396" width="600" bitrate="496" type="video/mp4" delivery="progressive">
							<![CDATA[https://iab-publicfiles.s3.amazonaws.com/vast/VAST-4.0-Short-Intro.mp4]]>
						</MediaFile>
					</MediaFiles>
				</Linear>
			</Creative>
			<Creative>
			</Creative>
		</Creatives>
		</InLine>
	</Ad>
</VAST>
```

## Navigate to Testing site

- Go to http://tools.springserve.com/tagtest
- Paste the VAST_2.0.xml tag in the `tag to test` box
- Make sure `VAST` is selected as the ad type
- Click on `Submit`
