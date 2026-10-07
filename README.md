<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Hafeez K S | CSE Student Portfolio</title>
<meta name="description" content="Portfolio of Hafeez K S - Computer Science Engineering Student specializing in software development, web technologies, and Arduino robotics.">

<!-- Google Fonts -->
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Plus+Jakarta+Sans:wght@300;400;500;600;700;800&family=Space+Grotesk:wght@500;700&display=swap" rel="stylesheet">

<style>
:root {
    --primary: #ff5a1f;
    --primary-hover: #ff7438;
    --primary-glow: rgba(255, 90, 31, 0.25);
    --bg-dark: #080808;
    --card-bg: #111111;
    --card-border: #222222;
    --card-hover-border: rgba(255, 90, 31, 0.5);
    --text-main: #f3f3f3;
    --text-muted: #9e9ea7;
    --font-heading: 'Space Grotesk', sans-serif;
    --font-body: 'Plus Jakarta Sans', sans-serif;
}

* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    scroll-behavior: smooth;
}

body {
    font-family: var(--font-body);
    background-color: var(--bg-dark);
    color: var(--text-main);
    line-height: 1.6;
    overflow-x: hidden;
    position: relative;
    background-image: 
        radial-gradient(circle at 15% 15%, rgba(255, 90, 31, 0.08) 0%, transparent 40%),
        radial-gradient(circle at 85% 65%, rgba(255, 90, 31, 0.05) 0%, transparent 40%);
}

a {
    color: inherit;
    text-decoration: none;
}

/* Scrollbar Styling */
::-webkit-scrollbar {
    width: 8px;
}
::-webkit-scrollbar-track {
    background: #0d0d0d;
}
::-webkit-scrollbar-thumb {
    background: #272727;
    border-radius: 4px;
}
::-webkit-scrollbar-thumb:hover {
    background: var(--primary);
}

/* Header & Navigation */
.navbar {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    z-index: 1000;
    padding: 18px 8%;
    display: flex;
    justify-content: space-between;
    align-items: center;
    background: rgba(8, 8, 8, 0.75);
    backdrop-filter: blur(16px);
    -webkit-backdrop-filter: blur(16px);
    border-bottom: 1px solid rgba(255, 255, 255, 0.06);
    transition: all 0.3s ease;
}

.navbar.scrolled {
    padding: 14px 8%;
    background: rgba(8, 8, 8, 0.92);
    border-bottom: 1px solid rgba(255, 90, 31, 0.15);
    box-shadow: 0 10px 30px rgba(0, 0, 0, 0.5);
}

.logo {
    font-family: var(--font-heading);
    font-size: 24px;
    font-weight: 800;
    letter-spacing: 1.5px;
    display: flex;
    align-items: center;
    gap: 2px;
}

.logo span,
.hero h1 span,
.section-title span {
    color: var(--primary);
    text-shadow: 0 0 25px rgba(255, 90, 31, 0.4);
}

.nav-links {
    display: flex;
    gap: 32px;
    list-style: none;
    align-items: center;
}

.nav-links a {
    color: var(--text-muted);
    font-size: 14px;
    font-weight: 500;
    letter-spacing: 0.5px;
    transition: all 0.25s ease;
    position: relative;
    padding: 4px 0;
}

.nav-links a:hover,
.nav-links a.active {
    color: #ffffff;
}

.nav-links a::after {
    content: '';
    position: absolute;
    bottom: -2px;
    left: 0;
    width: 0%;
    height: 2px;
    background: var(--primary);
    transition: width 0.3s ease;
    border-radius: 2px;
}

.nav-links a:hover::after,
.nav-links a.active::after {
    width: 100%;
}

.nav-contact-btn {
    padding: 8px 18px !important;
    background: rgba(255, 90, 31, 0.1);
    border: 1px solid rgba(255, 90, 31, 0.3);
    border-radius: 20px;
    color: var(--primary) !important;
    font-weight: 600;
}

.nav-contact-btn:hover {
    background: var(--primary) !important;
    color: #fff !important;
    transform: translateY(-2px);
    box-shadow: 0 4px 15px var(--primary-glow);
}

.nav-contact-btn::after {
    display: none !important;
}

.hamburger {
    display: none;
    cursor: pointer;
    flex-direction: column;
    gap: 6px;
    z-index: 1001;
}

.hamburger span {
    width: 25px;
    height: 2px;
    background: #fff;
    transition: 0.3s ease;
    border-radius: 2px;
}

.hamburger.active span:nth-child(1) {
    transform: rotate(45deg) translate(5px, 6px);
}

.hamburger.active span:nth-child(2) {
    opacity: 0;
}

.hamburger.active span:nth-child(3) {
    transform: rotate(-45deg) translate(6px, -6px);
}

/* Sections Common */
section {
    padding: 120px 8%;
    position: relative;
}

.small-title {
    color: var(--primary);
    font-size: 13px;
    font-weight: 700;
    letter-spacing: 4px;
    text-transform: uppercase;
    margin-bottom: 12px;
    display: flex;
    align-items: center;
    gap: 10px;
}

.small-title::before {
    content: '';
    width: 20px;
    height: 2px;
    background: var(--primary);
}

.section-title {
    font-family: var(--font-heading);
    font-size: clamp(38px, 5vw, 56px);
    line-height: 1.1;
    margin-bottom: 50px;
    letter-spacing: -1.5px;
    font-weight: 700;
}

/* Hero Section */
.hero {
    min-height: 100vh;
    display: grid;
    grid-template-columns: 1.2fr 0.8fr;
    align-items: center;
    gap: 60px;
    padding-top: 130px;
    position: relative;
}

.hero-badge {
    display: inline-flex;
    align-items: center;
    gap: 8px;
    padding: 6px 14px;
    border-radius: 30px;
    background: rgba(255, 90, 31, 0.08);
    border: 1px solid rgba(255, 90, 31, 0.25);
    color: var(--primary);
    font-size: 13px;
    font-weight: 600;
    margin-bottom: 22px;
}

.pulse-dot {
    width: 8px;
    height: 8px;
    background: #00ff88;
    border-radius: 50%;
    box-shadow: 0 0 10px #00ff88;
    animation: pulse 2s infinite;
}

@keyframes pulse {
    0% { transform: scale(0.95); opacity: 0.8; }
    50% { transform: scale(1.3); opacity: 1; }
    100% { transform: scale(0.95); opacity: 0.8; }
}

.hero h1 {
    font-family: var(--font-heading);
    font-size: clamp(52px, 8.5vw, 115px);
    line-height: 0.95;
    letter-spacing: -4px;
    margin-bottom: 20px;
    font-weight: 800;
}

.hero h2 {
    font-size: clamp(20px, 2.5vw, 26px);
    color: #d1d1d8;
    font-weight: 500;
    margin-bottom: 20px;
}

.hero p {
    max-width: 600px;
    color: var(--text-muted);
    font-size: 16px;
    line-height: 1.7;
    margin-bottom: 35px;
}

.buttons {
    display: flex;
    gap: 16px;
    flex-wrap: wrap;
    align-items: center;
}

.btn {
    padding: 14px 28px;
    border-radius: 30px;
    font-weight: 600;
    font-size: 14px;
    border: 1px solid #333;
    transition: all 0.3s cubic-bezier(0.16, 1, 0.3, 1);
    display: inline-flex;
    align-items: center;
    gap: 8px;
    cursor: pointer;
}

.btn-primary {
    background: var(--primary);
    border-color: var(--primary);
    color: #ffffff;
    box-shadow: 0 8px 25px var(--primary-glow);
}

.btn-primary:hover {
    background: var(--primary-hover);
    border-color: var(--primary-hover);
    transform: translateY(-3px);
    box-shadow: 0 12px 30px rgba(255, 90, 31, 0.4);
}

.btn-secondary {
    background: rgba(255, 255, 255, 0.03);
    border-color: #2e2e2e;
    color: #e0e0e0;
}

.btn-secondary:hover {
    border-color: #666;
    background: rgba(255, 255, 255, 0.08);
    transform: translateY(-3px);
    color: #fff;
}

.socials {
    display: flex;
    gap: 14px;
    margin-top: 30px;
}

.social {
    border: 1px solid #282828;
    padding: 9px 18px;
    border-radius: 20px;
    color: var(--text-muted);
    font-size: 13px;
    font-weight: 500;
    transition: all 0.3s ease;
    display: inline-flex;
    align-items: center;
    gap: 8px;
    background: rgba(20, 20, 20, 0.5);
}

.social:hover {
    color: #ffffff;
    border-color: var(--primary);
    background: rgba(255, 90, 31, 0.1);
    transform: translateY(-2px);
}

/* Profile Visual */
.profile {
    display: flex;
    justify-content: center;
    position: relative;
}

.profile-card-wrapper {
    position: relative;
}

.profile-card-wrapper::before {
    content: '';
    position: absolute;
    inset: -15px;
    border-radius: 40px;
    background: radial-gradient(circle, rgba(255, 90, 31, 0.22), transparent 70%);
    z-index: 0;
    filter: blur(10px);
}

.profile-box {
    position: relative;
    z-index: 1;
    width: 340px;
    height: 440px;
    border-radius: 30px;
    overflow: hidden;
    border: 1px solid rgba(255, 255, 255, 0.1);
    background: linear-gradient(145deg, #181818, #0b0b0b);
    box-shadow: 0 30px 80px rgba(0, 0, 0, 0.8);
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    transition: transform 0.4s ease, border-color 0.4s ease;
}

.profile-box:hover {
    transform: translateY(-6px);
    border-color: rgba(255, 90, 31, 0.4);
}

.profile-box img {
    width: 100%;
    height: 100%;
    object-fit: cover;
    object-position: top center;
}

.placeholder {
    width: 100%;
    height: 100%;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    background: radial-gradient(circle at center, #1f1410 0%, #0c0c0c 100%);
    gap: 12px;
}

.avatar-initial {
    font-family: var(--font-heading);
    font-size: 110px;
    font-weight: 900;
    color: var(--primary);
    line-height: 1;
    text-shadow: 0 0 40px rgba(255, 90, 31, 0.5);
}

.avatar-label {
    font-size: 14px;
    letter-spacing: 2px;
    color: var(--text-muted);
    font-weight: 600;
    text-transform: uppercase;
}

/* About Section */
.about-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 30px;
}

.card {
    background: var(--card-bg);
    border: 1px solid var(--card-border);
    border-radius: 24px;
    padding: 36px;
    transition: all 0.35s cubic-bezier(0.16, 1, 0.3, 1);
    position: relative;
    overflow: hidden;
}

.card::before {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background: radial-gradient(800px circle at var(--mouse-x, 0) var(--mouse-y, 0), rgba(255, 90, 31, 0.06), transparent 40%);
    pointer-events: none;
    opacity: 0;
    transition: opacity 0.4s;
}

.card:hover::before {
    opacity: 1;
}

.card:hover {
    transform: translateY(-6px);
    border-color: var(--card-hover-border);
    box-shadow: 0 20px 40px rgba(0, 0, 0, 0.4);
}

.card-icon {
    width: 48px;
    height: 48px;
    border-radius: 14px;
    background: rgba(255, 90, 31, 0.1);
    border: 1px solid rgba(255, 90, 31, 0.2);
    display: flex;
    align-items: center;
    justify-content: center;
    margin-bottom: 20px;
    color: var(--primary);
    font-size: 20px;
}

.card h3 {
    font-family: var(--font-heading);
    font-size: 24px;
    margin-bottom: 14px;
    font-weight: 700;
}

.card p {
    color: var(--text-muted);
    font-size: 15px;
    line-height: 1.7;
}

/* Skills Section */
.skills-container {
    display: flex;
    flex-direction: column;
    gap: 30px;
}

.skills-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(160px, 1fr));
    gap: 16px;
}

.skill {
    padding: 22px 18px;
    background: #111111;
    border: 1px solid #222222;
    border-radius: 18px;
    text-align: center;
    font-weight: 600;
    font-size: 15px;
    transition: all 0.3s cubic-bezier(0.16, 1, 0.3, 1);
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    gap: 10px;
    cursor: default;
}

.skill-icon {
    font-size: 24px;
    color: var(--primary);
    transition: transform 0.3s;
}

.skill:hover {
    background: linear-gradient(135deg, rgba(255, 90, 31, 0.15), rgba(255, 90, 31, 0.05));
    border-color: var(--primary);
    transform: translateY(-5px);
    box-shadow: 0 10px 25px rgba(255, 90, 31, 0.15);
}

.skill:hover .skill-icon {
    transform: scale(1.15);
}

/* Projects Section */
.projects {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    gap: 28px;
}

.project {
    min-height: 300px;
    position: relative;
    background: linear-gradient(160deg, #141414, #0b0b0b);
    display: flex;
    flex-direction: column;
    justify-content: space-between;
}

.project-top {
    margin-bottom: 25px;
}

.project-header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin-bottom: 20px;
}

.project-number {
    color: var(--primary);
    font-size: 13px;
    font-weight: 700;
    letter-spacing: 2px;
    background: rgba(255, 90, 31, 0.1);
    padding: 4px 12px;
    border-radius: 12px;
    border: 1px solid rgba(255, 90, 31, 0.2);
}

.project-badge {
    font-size: 12px;
    color: #999;
}

.project h3 {
    font-family: var(--font-heading);
    font-size: 26px;
    margin-bottom: 12px;
    font-weight: 700;
    line-height: 1.3;
}

.project p {
    color: var(--text-muted);
    font-size: 14px;
    line-height: 1.6;
}

.tags {
    display: flex;
    flex-wrap: wrap;
    gap: 8px;
    margin-top: 20px;
}

.tag {
    padding: 5px 12px;
    background: rgba(255, 255, 255, 0.04);
    border: 1px solid #282828;
    border-radius: 16px;
    font-size: 12px;
    color: #bbb;
    font-weight: 500;
    transition: 0.2s;
}

.project:hover .tag {
    border-color: rgba(255, 90, 31, 0.3);
}

/* Education Section */
.education {
    max-width: 900px;
}

.education-item {
    border-left: 2px solid var(--primary);
    padding: 0 0 45px 35px;
    position: relative;
}

.education-item::before {
    content: "";
    position: absolute;
    left: -8px;
    top: 2px;
    width: 14px;
    height: 14px;
    background: var(--primary);
    border-radius: 50%;
    box-shadow: 0 0 12px var(--primary);
}

.education-item h3 {
    font-family: var(--font-heading);
    font-size: 24px;
    font-weight: 700;
    margin-bottom: 4px;
}

.education-badge {
    display: inline-block;
    color: var(--primary);
    font-weight: 600;
    font-size: 14px;
    margin-bottom: 12px;
}

.education-item p {
    color: var(--text-muted);
    font-size: 15px;
    line-height: 1.7;
}

/* Focus Banner */
.focus-container {
    padding: 0 8%;
    margin: 40px 0 60px 0;
}

.focus {
    text-align: center;
    padding: 70px 6%;
    background: linear-gradient(135deg, #ff5a1f 0%, #b82d02 100%);
    border-radius: 30px;
    box-shadow: 0 25px 60px rgba(255, 90, 31, 0.25);
    color: #fff;
    position: relative;
    overflow: hidden;
}

.focus::after {
    content: '';
    position: absolute;
    top: -50%;
    right: -20%;
    width: 300px;
    height: 300px;
    background: rgba(255, 255, 255, 0.1);
    border-radius: 50%;
    pointer-events: none;
}

.focus h2 {
    font-family: var(--font-heading);
    font-size: clamp(32px, 4.5vw, 48px);
    margin-bottom: 16px;
    font-weight: 800;
    letter-spacing: -1px;
}

.focus p {
    max-width: 680px;
    margin: auto;
    color: #ffe6dc;
    font-size: 16px;
    line-height: 1.7;
}

/* Contact Section */
.contact {
    text-align: center;
}

.contact-card {
    max-width: 700px;
    margin: 0 auto;
    padding: 50px 40px;
    background: #101010;
    border: 1px solid #222;
    border-radius: 28px;
    box-shadow: 0 20px 50px rgba(0,0,0,0.5);
}

.contact p {
    color: var(--text-muted);
    margin-bottom: 25px;
    font-size: 16px;
}

.email-box {
    display: inline-flex;
    align-items: center;
    gap: 12px;
    background: rgba(255, 90, 31, 0.08);
    border: 1px dashed rgba(255, 90, 31, 0.4);
    padding: 12px 24px;
    border-radius: 30px;
    margin-bottom: 35px;
    transition: all 0.3s ease;
    cursor: pointer;
}

.email-box:hover {
    background: rgba(255, 90, 31, 0.15);
    border-color: var(--primary);
    transform: scale(1.02);
}

.email {
    font-family: var(--font-heading);
    font-size: clamp(16px, 2.5vw, 22px);
    font-weight: 600;
    color: var(--primary);
}

.copy-hint {
    font-size: 11px;
    color: #888;
    background: #1a1a1a;
    padding: 4px 8px;
    border-radius: 10px;
}

/* LinkedIn Follow Callout */
.linkedin-follow-card {
    margin-top: 30px;
    padding: 22px 26px;
    background: linear-gradient(135deg, rgba(10, 102, 194, 0.15) 0%, rgba(20, 20, 22, 0.95) 100%);
    border: 1px solid rgba(10, 102, 194, 0.35);
    border-radius: 20px;
    display: flex;
    align-items: center;
    justify-content: space-between;
    gap: 20px;
    text-align: left;
    transition: all 0.3s ease;
}

.linkedin-follow-card:hover {
    border-color: rgba(10, 102, 194, 0.7);
    box-shadow: 0 12px 35px rgba(10, 102, 194, 0.25);
    transform: translateY(-3px);
}

.linkedin-user-info {
    display: flex;
    align-items: center;
    gap: 15px;
}

.linkedin-avatar {
    width: 52px;
    height: 52px;
    border-radius: 50%;
    object-fit: cover;
    object-position: top center;
    border: 2px solid #0a66c2;
    box-shadow: 0 0 15px rgba(10, 102, 194, 0.4);
}

.linkedin-details h4 {
    font-size: 17px;
    font-weight: 700;
    color: #fff;
    display: flex;
    align-items: center;
    gap: 8px;
    margin-bottom: 2px;
}

.linkedin-badge {
    background: #0a66c2;
    color: #fff;
    font-size: 10px;
    font-weight: 800;
    padding: 2px 7px;
    border-radius: 6px;
    text-transform: uppercase;
    letter-spacing: 0.5px;
}

.linkedin-details p {
    font-size: 13px;
    color: #a5a5b2;
    margin: 0;
    line-height: 1.4;
}

.btn-linkedin-follow {
    background: #0a66c2;
    color: #ffffff !important;
    padding: 12px 22px;
    border-radius: 25px;
    font-weight: 700;
    font-size: 14px;
    display: inline-flex;
    align-items: center;
    gap: 8px;
    border: none;
    cursor: pointer;
    transition: all 0.25s ease;
    white-space: nowrap;
    box-shadow: 0 6px 20px rgba(10, 102, 194, 0.35);
}

.btn-linkedin-follow:hover {
    background: #004182;
    transform: translateY(-2px);
    box-shadow: 0 8px 25px rgba(10, 102, 194, 0.6);
}

/* Floating Follow Widget */
.floating-follow-widget {
    position: fixed;
    bottom: 25px;
    left: 25px;
    background: rgba(14, 14, 16, 0.95);
    backdrop-filter: blur(16px);
    -webkit-backdrop-filter: blur(16px);
    border: 1px solid rgba(10, 102, 194, 0.4);
    border-radius: 20px;
    padding: 14px 18px;
    display: flex;
    align-items: center;
    gap: 14px;
    box-shadow: 0 15px 40px rgba(0, 0, 0, 0.8), 0 0 20px rgba(10, 102, 194, 0.2);
    z-index: 1500;
    transform: translateY(140px);
    opacity: 0;
    transition: all 0.5s cubic-bezier(0.16, 1, 0.3, 1);
}

.floating-follow-widget.show {
    transform: translateY(0);
    opacity: 1;
}

.floating-close-btn {
    background: none;
    border: none;
    color: #888;
    cursor: pointer;
    font-size: 16px;
    padding: 4px;
    line-height: 1;
    transition: 0.2s;
    border-radius: 50%;
}

.floating-close-btn:hover {
    color: #fff;
    background: rgba(255, 255, 255, 0.1);
}

/* Footer */
footer {
    padding: 35px 8%;
    border-top: 1px solid #1a1a1a;
    display: flex;
    justify-content: space-between;
    align-items: center;
    color: #666;
    font-size: 14px;
    flex-wrap: wrap;
    gap: 15px;
}

.back-to-top {
    color: var(--primary);
    font-weight: 600;
    font-size: 13px;
    display: flex;
    align-items: center;
    gap: 4px;
}

.back-to-top:hover {
    text-decoration: underline;
}

/* Toast notification */
.toast {
    position: fixed;
    bottom: 30px;
    right: 30px;
    background: #1f1f1f;
    border: 1px solid var(--primary);
    color: #fff;
    padding: 12px 24px;
    border-radius: 12px;
    font-size: 14px;
    font-weight: 500;
    box-shadow: 0 10px 30px rgba(0,0,0,0.8);
    transform: translateY(100px);
    opacity: 0;
    transition: all 0.3s ease;
    z-index: 2000;
}

.toast.show {
    transform: translateY(0);
    opacity: 1;
}

/* Responsive Breakpoints */
@media(max-width: 992px) {
    .hero {
        grid-template-columns: 1fr;
        text-align: center;
        gap: 40px;
    }

    .small-title {
        justify-content: center;
    }

    .hero-badge {
        margin-left: auto;
        margin-right: auto;
    }

    .hero p {
        margin-left: auto;
        margin-right: auto;
    }

    .buttons,
    .socials {
        justify-content: center;
    }

    .profile {
        order: -1;
    }

    .profile-box {
        width: 280px;
        height: 360px;
    }

    .about-grid,
    .projects {
        grid-template-columns: 1fr;
    }
}

@media(max-width: 768px) {
    .hamburger {
        display: flex;
    }

    .nav-links {
        position: fixed;
        top: 0;
        right: -100%;
        width: 80%;
        max-width: 320px;
        height: 100vh;
        background: #0d0d0d;
        border-left: 1px solid #222;
        flex-direction: column;
        justify-content: center;
        padding: 40px;
        gap: 28px;
        transition: right 0.4s ease;
        box-shadow: -10px 0 30px rgba(0,0,0,0.8);
    }

    .nav-links.active {
        right: 0;
    }

    .nav-links a {
        font-size: 18px;
    }

    section {
        padding: 90px 6%;
    }

    .focus-container {
        padding: 0 6%;
    }
    
    footer {
        justify-content: center;
        text-align: center;
    }
}

@media(max-width: 480px) {
    .hero h1 {
        font-size: 56px;
        letter-spacing: -2px;
    }

    .skills-grid {
        grid-template-columns: repeat(2, 1fr);
    }

    .card {
        padding: 24px;
    }

    .contact-card {
        padding: 30px 20px;
    }

    .linkedin-follow-card {
        flex-direction: column;
        align-items: stretch;
        text-align: center;
        gap: 16px;
    }

    .linkedin-user-info {
        flex-direction: column;
        text-align: center;
    }

    .linkedin-details h4 {
        justify-content: center;
    }

    .btn-linkedin-follow {
        justify-content: center;
        width: 100%;
    }

    .floating-follow-widget {
        left: 15px;
        right: 15px;
        bottom: 15px;
        justify-content: space-between;
    }
}
</style>
</head>

<body>

<!-- Header / Navigation -->
<nav class="navbar" id="navbar">
    <div class="logo">HAFEEZ<span>.</span></div>

    <ul class="nav-links" id="navLinks">
        <li><a href="#about" class="nav-item">About</a></li>
        <li><a href="#skills" class="nav-item">Skills</a></li>
        <li><a href="#projects" class="nav-item">Projects</a></li>
        <li><a href="#education" class="nav-item">Education</a></li>
        <li><a href="#contact" class="nav-item nav-contact-btn">Contact</a></li>
    </ul>

    <div class="hamburger" id="hamburger" aria-label="Toggle menu">
        <span></span>
        <span></span>
        <span></span>
    </div>
</nav>

<!-- Hero Section -->
<section class="hero" id="home">
    <div>
        <div class="hero-badge">
            <span class="pulse-dot"></span>
            <span>Available for Opportunities & Projects</span>
        </div>

        <div class="small-title">HELLO, I'M</div>

        <h1>
            Hafeez<br>
            <span>K S</span>
        </h1>

        <h2>Computer Science Engineering Student</h2>

        <p>
            Passionate CSE undergraduate interested in software engineering, 
            modern web development, Arduino hardware robotics, and emerging technologies. 
            I enjoy transforming creative ideas into scalable, real-world solutions.
        </p>

        <div class="buttons">
            <a href="#projects" class="btn btn-primary">
                <svg width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="m9 18 6-6-6-6"/></svg>
                View My Projects
            </a>

            <a href="#contact" class="btn btn-secondary">
                <svg width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M22 16.92v3a2 2 0 0 1-2.18 2 19.79 19.79 0 0 1-8.63-3.07 19.5 19.5 0 0 1-6-6 19.79 19.79 0 0 1-3.07-8.67A2 2 0 0 1 4.11 2h3a2 2 0 0 1 2 1.72 12.84 12.84 0 0 0 .7 2.81 2 2 0 0 1-.45 2.11L8.09 9.91a16 16 0 0 0 6 6l1.27-1.27a2 2 0 0 1 2.11-.45 12.84 12.84 0 0 0 2.81.7A2 2 0 0 1 22 16.92z"/></svg>
                Contact Me
            </a>
        </div>

        <div class="socials">
            <a href="https://github.com/HAFEEZ-KS" target="_blank" rel="noopener noreferrer" class="social">
                <svg width="16" height="16" viewBox="0 0 24 24" fill="currentColor"><path d="M12 0c-6.626 0-12 5.373-12 12 0 5.302 3.438 9.8 8.207 11.387.599.111.793-.261.793-.577v-2.234c-3.338.726-4.033-1.416-4.033-1.416-.546-1.387-1.333-1.756-1.333-1.756-1.089-.745.083-.729.083-.729 1.205.084 1.839 1.237 1.839 1.237 1.07 1.834 2.807 1.304 3.492.997.107-.775.418-1.305.762-1.604-2.665-.305-5.467-1.334-5.467-5.931 0-1.311.469-2.381 1.236-3.221-.124-.303-.535-1.524.117-3.176 0 0 1.008-.322 3.301 1.23.957-.266 1.983-.399 3.003-.404 1.02.005 2.047.138 3.006.404 2.291-1.552 3.297-1.23 3.297-1.23.653 1.653.242 2.874.118 3.176.77.84 1.235 1.911 1.235 3.221 0 4.609-2.807 5.624-5.479 5.921.43.372.823 1.102.823 2.222v3.293c0 .319.192.694.801.576 4.765-1.589 8.199-6.086 8.199-11.386 0-6.627-5.373-12-12-12z"/></svg>
                GitHub
            </a>

            <a href="https://www.linkedin.com/in/hafeez-k-s-aa99b4388" target="_blank" rel="noopener noreferrer" class="social" style="border-color: rgba(10, 102, 194, 0.4); color: #fff;">
                <svg width="16" height="16" viewBox="0 0 24 24" fill="#0a66c2"><path d="M19 0h-14c-2.761 0-5 2.239-5 5v14c0 2.761 2.239 5 5 5h14c2.762 0 5-2.239 5-5v-14c0-2.761-2.238-5-5-5zm-11 19h-3v-11h3v11zm-1.5-12.268c-.966 0-1.75-.79-1.75-1.764s.784-1.764 1.75-1.764 1.75.79 1.75 1.764-.783 1.764-1.75 1.764zm13.5 12.268h-3v-5.604c0-3.368-4-3.113-4 0v5.604h-3v-11h3v1.765c1.396-2.586 7-2.777 7 2.476v6.759z"/></svg>
                Follow Us on LinkedIn
            </a>
        </div>
    </div>

    <div class="profile">
        <div class="profile-card-wrapper">
            <div class="profile-box">
                <img
                    src="profile.jpg"
                    alt="Hafeez K S"
                    onerror="this.style.display='none';this.nextElementSibling.style.display='flex';"
                >

                <div class="placeholder" style="display:none;">
                    <div class="avatar-initial">H</div>
                    <div class="avatar-label">Hafeez K S</div>
                </div>
            </div>
        </div>
    </div>
</section>

<!-- About Section -->
<section id="about">
    <div class="small-title">01 — ABOUT</div>

    <h2 class="section-title">
        About <span>Me</span>
    </h2>

    <div class="about-grid">
        <div class="card">
            <div class="card-icon">
                <svg width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M20 21v-2a4 4 0 0 0-4-4H8a4 4 0 0 0-4 4v2"></path><circle cx="12" cy="7" r="4"></circle></svg>
            </div>
            <h3>Who I Am</h3>
            <p>
                I am Hafeez K S, a Computer Science Engineering student passionate about 
                technology, problem solving, and building efficient solutions. 
                I am continuously honing my programming capabilities by developing practical, 
                functional applications.
            </p>
        </div>

        <div class="card">
            <div class="card-icon">
                <svg width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><polyline points="16 18 22 12 16 6"></polyline><polyline points="8 6 2 12 8 18"></polyline></svg>
            </div>
            <h3>What I Do</h3>
            <p>
                I specialize in programming with modern languages, web design, and 
                hardware prototyping with microcontrollers like Arduino. I enjoy constructing 
                systems that seamlessly merge software algorithms with embedded electronics.
            </p>
        </div>
    </div>
</section>

<!-- Skills Section -->
<section id="skills">
    <div class="small-title">02 — SKILLS</div>

    <h2 class="section-title">
        My <span>Skills</span>
    </h2>

    <div class="skills-grid">
        <div class="skill">
            <span class="skill-icon">⚡</span>
            <span>C</span>
        </div>
        <div class="skill">
            <span class="skill-icon">⚙️</span>
            <span>C++</span>
        </div>
        <div class="skill">
            <span class="skill-icon">☕</span>
            <span>Java</span>
        </div>
        <div class="skill">
            <span class="skill-icon">🐍</span>
            <span>Python</span>
        </div>
        <div class="skill">
            <span class="skill-icon">🌐</span>
            <span>HTML5</span>
        </div>
        <div class="skill">
            <span class="skill-icon">🎨</span>
            <span>CSS3</span>
        </div>
        <div class="skill">
            <span class="skill-icon">✨</span>
            <span>JavaScript</span>
        </div>
        <div class="skill">
            <span class="skill-icon">🤖</span>
            <span>Arduino</span>
        </div>
        <div class="skill">
            <span class="skill-icon">🐙</span>
            <span>Git & GitHub</span>
        </div>
        <div class="skill">
            <span class="skill-icon">🧠</span>
            <span>Problem Solving</span>
        </div>
    </div>
</section>

<!-- Projects Section -->
<section id="projects">
    <div class="small-title">03 — PROJECTS</div>

    <h2 class="section-title">
        Selected <span>Projects</span>
    </h2>

    <div class="projects">
        <div class="card project">
            <div class="project-top">
                <div class="project-header">
                    <div class="project-number">PROJECT 01</div>
                    <div class="project-badge">Robotics & IoT</div>
                </div>
                <h3>Bluetooth Obstacle Avoiding Car</h3>
                <p>
                    An Arduino-based smart robotic vehicle featuring dual operating modes: 
                    manual Bluetooth steering and autonomous obstacle avoidance using ultrasonic scanning with servo motors.
                </p>
            </div>
            <div class="tags">
                <span class="tag">Arduino</span>
                <span class="tag">C++</span>
                <span class="tag">HC-05</span>
                <span class="tag">HC-SR04</span>
                <span class="tag">Robotics</span>
            </div>
        </div>

        <div class="card project">
            <div class="project-top">
                <div class="project-header">
                    <div class="project-number">PROJECT 02</div>
                    <div class="project-badge">Web Application</div>
                </div>
                <h3>AI Interview Practice Platform</h3>
                <p>
                    An intelligent web platform designed to prepare students for technical job interviews through dynamic question prompts, evaluation feedback, and communication simulation.
                </p>
            </div>
            <div class="tags">
                <span class="tag">AI</span>
                <span class="tag">Web Development</span>
                <span class="tag">JavaScript</span>
                <span class="tag">Interview Prep</span>
            </div>
        </div>

        <div class="card project">
            <div class="project-top">
                <div class="project-header">
                    <div class="project-number">PROJECT 03</div>
                    <div class="project-badge">Frontend Design</div>
                </div>
                <h3>Personal Portfolio Website</h3>
                <p>
                    A fast, responsive, and visually aesthetic portfolio built to showcase technical projects, academic milestones, and engineering skills.
                </p>
            </div>
            <div class="tags">
                <span class="tag">HTML5</span>
                <span class="tag">CSS3</span>
                <span class="tag">JavaScript</span>
                <span class="tag">Responsive UI</span>
            </div>
        </div>

        <div class="card project">
            <div class="project-top">
                <div class="project-header">
                    <div class="project-number">PROJECT 04</div>
                    <div class="project-badge">In Development</div>
                </div>
                <h3>More Projects Coming Soon</h3>
                <p>
                    Actively architecting and implementing new projects in full-stack web development, intelligent automation, and IoT solutions.
                </p>
            </div>
            <div class="tags">
                <span class="tag">Innovation</span>
                <span class="tag">Algorithms</span>
                <span class="tag">Embedded Systems</span>
            </div>
        </div>
    </div>
</section>

<!-- Education Section -->
<section id="education">
    <div class="small-title">04 — EDUCATION</div>

    <h2 class="section-title">
        My <span>Education</span>
    </h2>

    <div class="education">
        <div class="education-item">
            <h3>Computer Science Engineering</h3>
            <div class="education-badge">B.Tech / Undergraduate Degree</div>
            <p>
                Pursuing comprehensive studies in Computer Science and Engineering. 
                Focusing on core computer science foundations, algorithms, object-oriented design, 
                web architectures, and hardware-software integration.
            </p>
        </div>
    </div>
</section>

<!-- Focus Section -->
<div class="focus-container">
    <section class="focus">
        <h2>Currently Focused On</h2>
        <p>
            Sharpening core algorithmic problem-solving, building production-grade software applications, 
            exploring AI integration in web tools, and preparing for engineering internship opportunities.
        </p>
    </section>
</div>

<!-- Contact Section -->
<section id="contact" class="contact">
    <div class="small-title">05 — CONTACT</div>

    <h2 class="section-title">
        Let's <span>Connect</span>
    </h2>

    <div class="contact-card">
        <p>
            Interested in collaborating on a project, exploring opportunities, or discussing ideas? 
            Feel free to reach out directly:
        </p>

        <div class="email-box" id="emailBox" title="Click to copy email">
            <svg width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="var(--primary)" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M4 4h16c1.1 0 2 .9 2 2v12c0 1.1-.9 2-2 2H4c-1.1 0-2-.9-2-2V6c0-1.1.9-2 2-2z"></path><polyline points="22,6 12,13 2,6"></polyline></svg>
            <span class="email" id="emailText">hafeez.k.s7612@gmail.com</span>
            <span class="copy-hint" id="copyHint">Click to copy</span>
        </div>

        <div class="buttons" style="justify-content: center;">
            <a href="https://github.com/HAFEEZ-KS" target="_blank" rel="noopener noreferrer" class="btn btn-secondary">
                <svg width="18" height="18" viewBox="0 0 24 24" fill="currentColor"><path d="M12 0c-6.626 0-12 5.373-12 12 0 5.302 3.438 9.8 8.207 11.387.599.111.793-.261.793-.577v-2.234c-3.338.726-4.033-1.416-4.033-1.416-.546-1.387-1.333-1.756-1.333-1.756-1.089-.745.083-.729.083-.729 1.205.084 1.839 1.237 1.839 1.237 1.07 1.834 2.807 1.304 3.492.997.107-.775.418-1.305.762-1.604-2.665-.305-5.467-1.334-5.467-5.931 0-1.311.469-2.381 1.236-3.221-.124-.303-.535-1.524.117-3.176 0 0 1.008-.322 3.301 1.23.957-.266 1.983-.399 3.003-.404 1.02.005 2.047.138 3.006.404 2.291-1.552 3.297-1.23 3.297-1.23.653 1.653.242 2.874.118 3.176.77.84 1.235 1.911 1.235 3.221 0 4.609-2.807 5.624-5.479 5.921.43.372.823 1.102.823 2.222v3.293c0 .319.192.694.801.576 4.765-1.589 8.199-6.086 8.199-11.386 0-6.627-5.373-12-12-12z"/></svg>
                GitHub Profile
            </a>

            <a href="https://www.linkedin.com/in/hafeez-k-s-aa99b4388" target="_blank" rel="noopener noreferrer" class="btn btn-primary">
                <svg width="18" height="18" viewBox="0 0 24 24" fill="currentColor"><path d="M19 0h-14c-2.761 0-5 2.239-5 5v14c0 2.761 2.239 5 5 5h14c2.762 0 5-2.239 5-5v-14c0-2.761-2.238-5-5-5zm-11 19h-3v-11h3v11zm-1.5-12.268c-.966 0-1.75-.79-1.75-1.764s.784-1.764 1.75-1.764 1.75.79 1.75 1.764-.783 1.764-1.75 1.764zm13.5 12.268h-3v-5.604c0-3.368-4-3.113-4 0v5.604h-3v-11h3v1.765c1.396-2.586 7-2.777 7 2.476v6.759z"/></svg>
                Follow Us on LinkedIn
            </a>
        </div>

        <!-- Featured LinkedIn Follow Callout -->
        <div class="linkedin-follow-card">
            <div class="linkedin-user-info">
                <img src="profile.jpg" alt="Hafeez K S" class="linkedin-avatar">
                <div class="linkedin-details">
                    <h4>Hafeez K S <span class="linkedin-badge">LinkedIn</span></h4>
                    <p>Follow us for tech posts, software projects & robotics insights.</p>
                </div>
            </div>
            <a href="https://www.linkedin.com/in/hafeez-k-s-aa99b4388" target="_blank" rel="noopener noreferrer" class="btn-linkedin-follow">
                <svg width="16" height="16" viewBox="0 0 24 24" fill="currentColor"><path d="M19 0h-14c-2.761 0-5 2.239-5 5v14c0 2.761 2.239 5 5 5h14c2.762 0 5-2.239 5-5v-14c0-2.761-2.238-5-5-5zm-11 19h-3v-11h3v11zm-1.5-12.268c-.966 0-1.75-.79-1.75-1.764s.784-1.764 1.75-1.764 1.75.79 1.75 1.764-.783 1.764-1.75 1.764zm13.5 12.268h-3v-5.604c0-3.368-4-3.113-4 0v5.604h-3v-11h3v1.765c1.396-2.586 7-2.777 7 2.476v6.759z"/></svg>
                + Follow Us on LinkedIn
            </a>
        </div>
    </div>
</section>

<!-- Footer -->
<footer>
    <div>
        © 2026 <strong>Hafeez K S</strong> — Computer Science Engineering
    </div>
    <a href="#home" class="back-to-top">
        Back to top
        <svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="m18 15-6-6-6 6"/></svg>
    </a>
</footer>

<!-- Floating LinkedIn Follow Prompt -->
<div class="floating-follow-widget" id="floatingFollow">
    <img src="profile.jpg" alt="Hafeez K S" style="width: 40px; height: 40px; border-radius: 50%; object-fit: cover; object-position: top center; border: 2px solid #0a66c2;">
    <div style="text-align: left;">
        <div style="font-size: 13px; font-weight: 700; color: #fff;">Connect with us on LinkedIn! 👋</div>
        <div style="font-size: 11px; color: #9e9ea7;">Follow us for tech & engineering updates</div>
    </div>
    <a href="https://www.linkedin.com/in/hafeez-k-s-aa99b4388" target="_blank" rel="noopener noreferrer" class="btn-linkedin-follow" style="padding: 7px 15px; font-size: 12px;">
        + Follow Us
    </a>
    <button class="floating-close-btn" id="closeFloatingFollow" aria-label="Close notification">✕</button>
</div>

<!-- Toast notification for actions -->
<div class="toast" id="toast">Email copied to clipboard!</div>

<script>
// Navbar background scroll behavior
const navbar = document.getElementById("navbar");
const navLinks = document.getElementById("navLinks");
const hamburger = document.getElementById("hamburger");
const navItems = document.querySelectorAll(".nav-item");

window.addEventListener("scroll", function() {
    if (window.scrollY > 40) {
        navbar.classList.add("scrolled");
    } else {
        navbar.classList.remove("scrolled");
    }

    // Scroll spy for active link highlight
    const sections = document.querySelectorAll("section[id]");
    const scrollY = window.pageYOffset;

    sections.forEach(section => {
        const sectionHeight = section.offsetHeight;
        const sectionTop = section.offsetTop - 120;
        const sectionId = section.getAttribute("id");

        if (scrollY > sectionTop && scrollY <= sectionTop + sectionHeight) {
            navItems.forEach(link => {
                link.classList.remove("active");
                if (link.getAttribute("href") === "#" + sectionId) {
                    link.classList.add("active");
                }
            });
        }
    });
});

// Mobile menu toggle
hamburger.addEventListener("click", () => {
    hamburger.classList.toggle("active");
    navLinks.classList.toggle("active");
});

// Close menu when clicking nav links
navItems.forEach(item => {
    item.addEventListener("click", () => {
        hamburger.classList.remove("active");
        navLinks.classList.remove("active");
    });
});

// Interactive mouse glow for cards
document.querySelectorAll(".card").forEach(card => {
    card.addEventListener("mousemove", e => {
        const rect = card.getBoundingClientRect();
        const x = e.clientX - rect.left;
        const y = e.clientY - rect.top;
        card.style.setProperty("--mouse-x", `${x}px`);
        card.style.setProperty("--mouse-y", `${y}px`);
    });
});

// Copy email to clipboard feature
const emailBox = document.getElementById("emailBox");
const toast = document.getElementById("toast");

emailBox.addEventListener("click", () => {
    const emailText = document.getElementById("emailText").textContent.trim();
    navigator.clipboard.writeText(emailText).then(() => {
        toast.classList.add("show");
        document.getElementById("copyHint").textContent = "Copied!";
        setTimeout(() => {
            toast.classList.remove("show");
            document.getElementById("copyHint").textContent = "Click to copy";
        }, 2500);
    });
});

// Floating LinkedIn Follow prompt
const floatingFollow = document.getElementById("floatingFollow");
const closeFloatingFollow = document.getElementById("closeFloatingFollow");

setTimeout(() => {
    if (!sessionStorage.getItem("dismissedLinkedInPrompt")) {
        floatingFollow.classList.add("show");
    }
}, 2200);

closeFloatingFollow.addEventListener("click", () => {
    floatingFollow.classList.remove("show");
    sessionStorage.setItem("dismissedLinkedInPrompt", "true");
});
</script>

</body>
</html>
