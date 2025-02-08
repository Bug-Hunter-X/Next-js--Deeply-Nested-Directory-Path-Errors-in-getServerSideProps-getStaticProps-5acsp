# Next.js Deeply Nested Directory Path Issue

This repository demonstrates an uncommon bug in Next.js related to deeply nested directory structures when utilizing `getServerSideProps` or `getStaticProps`.  Under certain conditions, Next.js may fail to correctly resolve file paths within exceptionally deep or oddly-named directories, leading to unexpected 404 errors or the failure to fetch data.

## Steps to Reproduce

1. Clone the repository.
2. Run `npm install`.
3. Run `npm run dev`.
4. Navigate to the problematic nested page (indicated in `broken-navigation.js`).  You'll likely encounter a 404 or an issue where data isn't fetched.

## Solution

The solution involves refactoring the directory structure to be less deeply nested and avoiding unusual characters in directory names. The `fixed-navigation.js` example demonstrates this change.