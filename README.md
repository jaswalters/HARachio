# HARachio
I created a lovelace frontend with a node red flow that handles quick runs for the Rachio sprinkler controller. With this setup you can start or stop the sprinklers from within HA or the Rachio app and HA will stay in sync. You can even start running a zone in the Rachio app and stop it from within HA.


When a zone is started the buttons will be disabled for 10 seconds to prevent any interruptions to the node red flow.

You do not have to stop a zone to start another one as the node red flow will handle this.

Prereqs:
Button Card:
https://github.com/custom-cards/button-card#installation

Fold Entity Row:
https://github.com/thomasloven/lovelace-fold-entity-row

State Switch:
https://github.com/thomasloven/lovelace-state-switch

HUI Element:
https://github.com/thomasloven/lovelace-hui-element

Node Red Secrets Node:
https://github.com/shanemadden/node-red-contrib-secret

Webhook setup using Rachio API:
Rachio Bearer Token
Rachio Person ID
https://rachio.readme.io

Custom integration between Node Red and HA will need to be installed:
https://github.com/zachowj/hass-node-red

Node red websocket:
https://github.com/zachowj/node-red-contrib-home-assistant-websocket

After you have obtained your Bearer token and Person ID from Rachio you will need to place them in the two Secret nodes.

In the webhook node you will need to generate an ID which will create a webhook in HA for that node.

Hope this helps someone with Rachio or at least gives you some ideas of how to set yours up.
