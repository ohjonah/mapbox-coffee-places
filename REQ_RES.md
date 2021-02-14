## Response:

Hi Mittens,

Thanks for reaching out and thanks for your patience.

I have seen this come up before and I can help you out! I took a look at your site and it looks like you’re using Mapbox GL JS. Sometimes when a map is hidden, it may have some sizing problems when it becomes revealed.

All you have to do is tell the map to resize when you click the button. You can do this by calling `map.resize();` in your mapExpand function.

*Example*
```js
function mapExpand() {
    var myMap = document.getElementById('map');
    myMap.setAttribute("style", "height:200px");
    map.resize();
}
```

If you’d like to learn more about resizing or any other Mapbox GL JS functions, I have found that our official documentation can be a great resource. See [Official Mapbox Docs](https://docs.mapbox.com/mapbox-gl-js/api/map/#map#resize).


Let me know if anything else comes up and I’ll be happy to help.

Best,

Jonah


## Reflection

#### Describe your approach to finding the answer.

I clicked the link to see what challenge our customer was facing. When I clicked the button, I saw a portion of the map, but not the rest of the map tiles. I opened the console to see if there were any network issues and saw that there were all at 200 status. Coincidentally, when I opened the console, it resized my browser screen and the rest of the map showed up. So I thought it could be a rendering issue.

I started first by trying to replicate Mitten’s issue. I started here because if there was no replicable issue, I would have to dig deeper and ask questions to see the issue Mitten’s was seeing. After verifying the issue, I started in the browser console because it gives me quick visibility into the type of requests Mitten’s is making and something like an access token or failed requests could pinpoint me faster to a root cause.

I went to the docs page and clicked on troubleshooting. I thought there would be a FAQ for common problems. I then clicked on the Blank or Missing Map Tiles article since that seemed to be akin to the issue that was plighting Mittens. Even though I saw that the network requests were returning valid JSON, I tested the Style ID, Tileset ID, and Access Token. Then I saw the “Your map is hidden” header.

I quickly went back to the browser console, checked Mitten’s index/html file and saw that I could call Mitten’s map object. Since I saw that we were calling out to the Mapbox GL JS library, I called map.resize() after clicking the button, and the map re-rendered correctly.

#### Which resources did you include in your response and why?

I included the Mapbox GL JS API Reference documentation to the id attribute `#map#resize`. When I went to search for keywords in “Troubleshoot”, I saw that I could narrow by product scope, but it seemed that the articles were tagged by product rather than have it troubleshoot by product, so I included the API Reference docs to help Mitten’s expand map utilities. I saw that Mitten’s had already added a custom cat marker and was able to set the access token, styles, et al. Being able to reference documentation could help Mitten’s take maps to the next level.

#### Describe the tone you used in your response and why you decided to use it.

I tried to mimic Mitten’s tone in urgency. I opened with thankfulness to acknowledge any sort of wait time, proceeded with an exclamatory call to action (I can help!), and tried to be concise by explaining the issue and coding out an example. I ended the conversation by pointing to documentation and a callback to reach out if there were any other issues, hopefully eliminating any concern that Mapbox wouldn’t be able to support our customers.

I think the tone was kind, concise in its diagnoses, and reassuring in a supportive way. I used this tone because our customer had many terse, declarative, observational sentences, e.g. Here’s my map! There’s nothing there! Here’s a screenshot! Have you seen this? I’m not sure!. I wanted to give a calm, collected answer that was affirming, yet supportive.