<script>
  import TopAppBar, { Row, Section, Title } from "@smui/top-app-bar";
  import IconButton from "@smui/icon-button";
  import Button from "@smui/button";
  import Card, {
    Content,
    PrimaryAction,
    Media,
    MediaContent,
    Actions,
    ActionButtons,
    ActionIcons,
  } from "@smui/card";
  let prominent = false;
  let dense = false;
  let secondaryColor = false;
  $: name = "Deniska";
</script>

<style>
  .top-app-bar-container {
    overflow: auto;
    display: inline-block;
  }
</style>

<main>
  <div class="top-app-bar-container flexor">
    <TopAppBar
      variant="static"
      {prominent}
      {dense}
      color={secondaryColor ? 'secondary' : 'primary'}>
      <Row>
        <Section>
          <IconButton class="material-icons">menu</IconButton>
          <Title>Flex Static</Title>
        </Section>
        <Section align="end" toolbar>
          <IconButton class="material-icons" aria-label="Download">
            file_download
          </IconButton>
          <IconButton class="material-icons" aria-label="Print this page">
            print
          </IconButton>
          <IconButton class="material-icons" aria-label="Bookmark this page">
            bookmark
          </IconButton>
        </Section>
      </Row>
    </TopAppBar>
  </div>
  <h1>Hello {name}!</h1>
  <Button>Click me!</Button>
  <div class="card-container">
    <Card style="width: 320px;">
      <Media class="card-media-square" aspectRatio="square">
        <div style="color: #000; position: absolute; bottom: 16px; left: 16px;">
          <h2 class="mdc-typography--headline6" style="margin: 0;">
            A card with square media.
          </h2>
          <h3 class="mdc-typography--subtitle2" style="margin: 0;">
            And a subtitle.
          </h3>
        </div>
      </Media>
    </Card>
  </div>
</main>
