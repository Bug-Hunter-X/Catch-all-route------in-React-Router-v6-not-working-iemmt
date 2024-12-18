# React Router v6 Catch-all Route Issue

This repository demonstrates a common issue encountered when using catch-all routes (`/*`) in React Router v6.  The catch-all route, intended to handle any invalid routes and display a '404 - Not Found' page, is unexpectedly failing.  Instead of displaying the NotFound component, the application displays the home page.

## Problem Description

The provided code snippet shows a simple React Router setup. However, when navigating to a non-existent route, the application defaults to the home page instead of the intended `NotFound` component. This is likely due to an order of routes problem. 

## Solution

The solution involves correctly placing the catch-all route.  The catch-all route must always be placed last. If it is placed earlier, it will match all routes preventing the other routes from being matched.