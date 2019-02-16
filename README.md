# Linernotes.club Mastodon Themes
Some themes commissioned for [linernotes.club](linernotes.club).

## Setup
quoted from https://github.com/skiant/mastodon-light-theme with some names changed
> ### Instance admins
> 1. Copy `linernotes_dark.scss`, `linernotes_dark`, and `mastodon_flat_css` into `app/javascript/styles`
> 2. Add the following line in `config/themes.yml`: `linernotes_dark: styles/linernotes_dark.scss`
> 3. Run `RAILS_ENV=production bundle exec rails assets:precompile`
> 4. Restart Mastodon
> 
> ### Regular users
> (assuming your instance admin installed the theme)
> 1. Go to your settings
> 2. Look for the `Site Theme` dropdown
> 3. Select the `linernotes_dark` theme if available

## Extensions
it's still mostly dedicated to linernotes.club but i've since made a few changes to make this more modular in case anyone else wants a custom theme based on mastodonFlat? the basic structure of the theme is something like this:
- themeName.scss = contains import statements for all base mastodon styles, with the following imports in order:
  - themeName/palette.scss -- defines color palette to be used by mfc base theme
  - mastodon_flat_css/mastodonFlat.scss -- applies mfc base theme using palette
  - themeName/overrides.scss -- misc tweaks on top of mfc

## Additional notes
Mostly based on https://github.com/trwnh/mastodon-flat-css
