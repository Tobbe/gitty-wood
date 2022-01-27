# Gitty

- Gitty takes inspiration from Github.
- Gitty exists to help incentivize open source software development.
- Ethereum contracts seem to make it a lot easier to develop what Gitty is trying to do
- Specifically, Ethereum enables select equity holders to only increase the number of holders after they've voted... and handles a lot of that development work for you
- Gitty provides a means by which core contributors can have financial stake in their project
- When an individual has demonstrated to core contributors that they can offer technical, legal/administrative, or financial support to their project, the core developers can give them equity in their repo in exchange for their offered support
- This incentivizes stake holders to increase the value of the code... the code is an asset that offers utility, and that is how it derives it's value, even though it is free to use
- If one of afforementioned points proves to contribute to a poor incentive structure... it will be reavaluated

## Running locally

 1. Fork and clone this repo
 2. `yarn install`
 3. Create an empty .env file
 4. Create a project on Supabase so you can use auth
 5. Set up OAth with GitHub on Supabase following this guide:
    https://supabase.com/docs/guides/auth/auth-github
 6. Grab the keys you need from your Supabase account and add them to your .env
    file
 7. Create a new postgres database locally
    - I just had to run `psql -U postgres -c 'create database gitty;'` in my
      MacOS terminal
 8. Add this to your .env file:
   `DATABASE_URL=postgres://postgres:<password>@localhost:5432/gitty`
   (replacing `<password>` with your own actual password)
 9. `yarn rw prisma migrate dev`
10. `yarn rw dev`
