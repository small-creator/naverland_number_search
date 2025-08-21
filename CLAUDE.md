# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a single-page web application for checking Naver Real Estate property numbers. The project consists of a standalone HTML file that allows users to input a property number and directly navigate to the corresponding Naver Land property page.

## Architecture

**Technology Stack:**
- Vanilla HTML/CSS/JavaScript (no build tools or dependencies)
- Google Fonts (Noto Sans KR) for Korean typography
- Vercel Analytics integration for tracking

**File Structure:**
```
index.html - Complete self-contained web application
```

**Core Functionality:**
- Input validation for property numbers
- Direct URL construction to `https://fin.land.naver.com/articles/{itemNumber}`
- Responsive design with Korean language support
- Community link integration to KakaoTalk open chat

## Development

**No Build Process:** This is a static HTML file requiring no compilation, bundling, or dependency management.

**Local Development:**
- Open `index.html` directly in browser, or
- Serve via any static web server (e.g., `python -m http.server` or Live Server extension)

**Styling Architecture:**
- Embedded CSS with Naver brand colors (#03c75a green, #FFDE03 yellow)
- Google-inspired search box design
- Responsive layout using flexbox and percentage widths

**JavaScript Architecture:**
- Event-driven with DOM manipulation
- Input validation and URL generation
- Enter key support for form submission
- External link handling for community access

## Key Components

**Search Interface (`lines 29-112`):**
- Styled input field with search icon
- Integrated action button
- Hover states and transitions

**Validation Logic (`function openNaverLand`):**
- Checks for empty input
- Constructs Naver Land URL with property ID
- Opens result in new tab

**Analytics Integration (`lines 135-138`):**
- Vercel Analytics script for usage tracking
- Non-blocking deferred loading