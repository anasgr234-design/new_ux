# new_ux
<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>المركز الوطني للنخيل والتمور</title>
<link href="https://fonts.googleapis.com/css2?family=Cairo:wght@300;400;600;700;900&family=Tajawal:wght@300;400;500;700;800&display=swap" rel="stylesheet">
<style>
:root {
  --ncpd-green:   #1a6b3a;
  --ncpd-dark:    #0f4224;
  --ncpd-mid:     #2d8a52;
  --ncpd-light:   #4db876;
  --ncpd-glow:    #a8f0c6;
  --nama-gold:    #c9a040;
  --nama-gold-lt: #f0d080;
  --cream:        #f8f5ef;
  --parch:        #ede8de;
  --white:        #ffffff;
  --ink:          #0d1f14;
  --ink2:         #1e3a28;
  --muted:        #5a7a65;
  --border:       rgba(26,107,58,.13);
  --red:          #c0392b;
  --amber:        #d4973a;
}
*,*::before,*::after{box-sizing:border-box;margin:0;padding:0;}
html{scroll-behavior:smooth;}
body{font-family:'Tajawal',sans-serif;background:var(--cream);color:var(--ink);min-height:100vh;overflow-x:hidden;}

/* ══ TOP INFO BAR ══ */
.info-bar{background:var(--ncpd-dark);padding:.35rem 2rem;display:flex;justify-content:space-between;align-items:center;font-size:.72rem;}
.info-bar a{color:rgba(255,255,255,.55);text-decoration:none;display:flex;align-items:center;gap:.3rem;}
.info-bar a:hover{color:var(--ncpd-glow);}
.verify-badge{display:flex;align-items:center;gap:.5rem;color:rgba(255,255,255,.5);}
.verify-badge img{width:16px;height:11px;object-fit:cover;}

/* ══ MAIN HEADER ══ */
.main-header{background:var(--white);border-bottom:3px solid var(--ncpd-green);position:sticky;top:0;z-index:500;box-shadow:0 2px 20px rgba(15,66,36,.1);}
.header-inner{max-width:1400px;margin:0 auto;padding:0 2rem;height:74px;display:flex;align-items:center;justify-content:space-between;gap:1rem;}

.logo-block{display:flex;align-items:center;gap:1rem;}
.logo-emblem{width:54px;height:54px;position:relative;}
.logo-emblem svg{width:100%;height:100%;}
.logo-text-block{line-height:1.2;}
.logo-ar{font-family:'Cairo',sans-serif;font-size:.95rem;font-weight:900;color:var(--ncpd-dark);}
.logo-en{font-size:.6rem;color:var(--muted);font-weight:500;letter-spacing:.04em;}

.header-nav{display:flex;align-items:center;gap:.25rem;}
.nav-item{padding:.5rem .8rem;border-radius:6px;font-size:.82rem;font-weight:600;color:var(--ink2);cursor:pointer;transition:all .2s;border:none;background:transparent;font-family:'Tajawal',sans-serif;white-space:nowrap;}
.nav-item:hover{background:rgba(26,107,58,.07);color:var(--ncpd-green);}
.nav-item.active{background:var(--ncpd-green);color:var(--white);}
.nav-item.has-arrow::after{content:' ▾';font-size:.65rem;}

.header-actions{display:flex;align-items:center;gap:.75rem;}
.lang-btn{background:transparent;border:1px solid var(--border);color:var(--muted);padding:.3rem .75rem;border-radius:6px;font-size:.78rem;cursor:pointer;font-family:'Tajawal',sans-serif;transition:all .2s;}
.lang-btn:hover{border-color:var(--ncpd-green);color:var(--ncpd-green);}

/* ── NAMA LOGIN BUTTON ── */
.nama-login-btn{
  display:flex;align-items:center;gap:.5rem;
  background:linear-gradient(135deg,var(--nama-gold),#a07828);
  color:var(--white);
  padding:.38rem 1rem;border-radius:8px;
  font-family:'Cairo',sans-serif;font-size:.8rem;font-weight:700;
  cursor:pointer;border:none;
  box-shadow:0 3px 12px rgba(201,160,64,.35);
  transition:all .2s;
  white-space:nowrap;
}
.nama-login-btn:hover{box-shadow:0 5px 20px rgba(201,160,64,.5);transform:translateY(-1px);}
.nama-icon{font-size:.9rem;}

/* ══ BREADCRUMB ══ */
.breadcrumb-bar{background:var(--ncpd-green);padding:.55rem 2rem;}
.breadcrumb-inner{max-width:1400px;margin:0 auto;display:flex;align-items:center;gap:.5rem;font-size:.75rem;color:rgba(255,255,255,.7);}
.breadcrumb-inner a{color:rgba(255,255,255,.7);text-decoration:none;}
.breadcrumb-inner a:hover{color:var(--white);}
.bc-sep{opacity:.4;}
.bc-current{color:var(--white);font-weight:600;}

/* ══ VIEWS ══ */
.view{display:none;}
.view.active{display:block;}

/* ══ ─────────── SERVICES VIEW ─────────── ══ */

/* hero section */
.services-hero{
  background:linear-gradient(135deg, var(--ncpd-dark) 0%, var(--ncpd-green) 60%, var(--ncpd-mid) 100%);
  padding:3rem 2rem 2.5rem;
  position:relative;overflow:hidden;
}
.services-hero::before{
  content:'';position:absolute;inset:0;
  background:url("data:image/svg+xml,%3Csvg width='60' height='60' viewBox='0 0 60 60' xmlns='http://www.w3.org/2000/svg'%3E%3Cg fill='none' fill-rule='evenodd'%3E%3Cg fill='%23ffffff' fill-opacity='0.03'%3E%3Cpath d='M36 34v-4h-2v4h-4v2h4v4h2v-4h4v-2h-4zm0-30V0h-2v4h-4v2h4v4h2V6h4V4h-4zM6 34v-4H4v4H0v2h4v4h2v-4h4v-2H6zM6 4V0H4v4H0v2h4v4h2V6h4V4H6z'/%3E%3C/g%3E%3C/g%3E%3C/svg%3E");
}
.services-hero-inner{max-width:1400px;margin:0 auto;position:relative;z-index:1;}
.hero-eyebrow{font-size:.72rem;font-weight:700;letter-spacing:.1em;color:var(--ncpd-glow);text-transform:uppercase;margin-bottom:.5rem;}
.hero-title{font-family:'Cairo',sans-serif;font-size:2rem;font-weight:900;color:var(--white);margin-bottom:.4rem;}
.hero-sub{color:rgba(255,255,255,.6);font-size:.88rem;}
.hero-count{display:inline-flex;align-items:center;gap:.4rem;background:rgba(255,255,255,.1);border:1px solid rgba(255,255,255,.15);color:rgba(255,255,255,.8);padding:.28rem .8rem;border-radius:100px;font-size:.78rem;font-weight:600;margin-top:.75rem;}

/* search + filter bar */
.search-filter-bar{background:var(--white);border-bottom:1px solid var(--border);padding:1.25rem 2rem;position:sticky;top:74px;z-index:400;box-shadow:0 2px 12px rgba(0,0,0,.06);}
.search-filter-inner{max-width:1400px;margin:0 auto;display:flex;align-items:center;gap:1rem;flex-wrap:wrap;}

.search-wrap{flex:1;min-width:220px;position:relative;}
.search-input{
  width:100%;padding:.65rem 1rem .65rem 3rem;
  border:1.5px solid var(--border);border-radius:10px;
  font-family:'Tajawal',sans-serif;font-size:.88rem;color:var(--ink);
  background:var(--cream);
  transition:all .2s;outline:none;
}
.search-input:focus{border-color:var(--ncpd-green);background:var(--white);box-shadow:0 0 0 3px rgba(26,107,58,.1);}
.search-icon{position:absolute;left:1rem;top:50%;transform:translateY(-50%);color:var(--muted);font-size:1rem;pointer-events:none;}
.search-hint{position:absolute;top:calc(100% + 4px);right:0;left:0;background:var(--white);border:1px solid var(--border);border-radius:10px;box-shadow:0 8px 28px rgba(0,0,0,.1);z-index:99;display:none;overflow:hidden;}
.search-hint.show{display:block;}
.hint-item{padding:.65rem 1rem;font-size:.82rem;cursor:pointer;display:flex;align-items:center;gap:.6rem;transition:background .15s;}
.hint-item:hover{background:rgba(26,107,58,.06);}
.hint-item .hint-tag{background:rgba(26,107,58,.08);color:var(--ncpd-green);font-size:.68rem;font-weight:700;padding:.1rem .4rem;border-radius:4px;}
.hint-no-results{padding:.75rem 1rem;font-size:.82rem;color:var(--muted);text-align:center;}

.filter-pills{display:flex;gap:.5rem;flex-wrap:wrap;}
.filter-pill{
  padding:.38rem .85rem;border-radius:100px;
  font-size:.76rem;font-weight:600;cursor:pointer;
  border:1.5px solid var(--border);
  color:var(--muted);background:transparent;
  font-family:'Tajawal',sans-serif;
  transition:all .2s;white-space:nowrap;
}
.filter-pill:hover{border-color:var(--ncpd-green);color:var(--ncpd-green);}
.filter-pill.active{background:var(--ncpd-green);color:var(--white);border-color:var(--ncpd-green);}

/* main grid layout */
.services-layout{max-width:1400px;margin:0 auto;padding:2rem 2rem;display:grid;grid-template-columns:240px 1fr;gap:2rem;}
.sidebar-filters{position:sticky;top:145px;height:fit-content;}
.sidebar-section{background:var(--white);border:1px solid var(--border);border-radius:12px;padding:1.2rem;margin-bottom:1rem;}
.sidebar-title{font-family:'Cairo',sans-serif;font-size:.82rem;font-weight:800;color:var(--ink2);margin-bottom:.9rem;border-bottom:1px solid var(--border);padding-bottom:.6rem;}
.filter-check{display:flex;align-items:center;gap:.5rem;padding:.3rem 0;cursor:pointer;}
.filter-check input{accent-color:var(--ncpd-green);width:14px;height:14px;cursor:pointer;}
.filter-check label{font-size:.8rem;color:var(--ink2);cursor:pointer;}
.filter-check label span{font-size:.7rem;color:var(--muted);margin-right:.3rem;}

/* services grid */
.svc-count-bar{display:flex;align-items:center;justify-content:space-between;margin-bottom:1.2rem;}
.svc-count-text{font-size:.82rem;color:var(--muted);}
.svc-count-text strong{color:var(--ink);font-weight:700;}
.sort-select{border:1px solid var(--border);border-radius:7px;padding:.3rem .7rem;font-family:'Tajawal',sans-serif;font-size:.78rem;color:var(--ink2);background:var(--white);cursor:pointer;outline:none;}

.services-grid{display:grid;grid-template-columns:repeat(auto-fill,minmax(270px,1fr));gap:1.1rem;}

/* service card */
.svc-card{
  background:var(--white);border:1px solid var(--border);border-radius:14px;
  overflow:hidden;display:flex;flex-direction:column;
  transition:transform .22s,box-shadow .22s;
  cursor:pointer;
  animation:cardIn .35s ease both;
}
.svc-card:hover{transform:translateY(-4px);box-shadow:0 12px 36px rgba(15,66,36,.1);}
@keyframes cardIn{from{opacity:0;transform:translateY(10px)}to{opacity:1;transform:translateY(0)}}
.svc-card:nth-child(1){animation-delay:.05s}.svc-card:nth-child(2){animation-delay:.1s}
.svc-card:nth-child(3){animation-delay:.15s}.svc-card:nth-child(4){animation-delay:.2s}
.svc-card:nth-child(5){animation-delay:.25s}.svc-card:nth-child(6){animation-delay:.3s}

.card-top{padding:1.3rem 1.3rem 1rem;flex:1;display:flex;flex-direction:column;gap:.6rem;}
.card-icon-area{width:44px;height:44px;border-radius:12px;background:rgba(26,107,58,.08);display:flex;align-items:center;justify-content:center;font-size:1.4rem;}
.card-audience{display:inline-flex;align-items:center;gap:.3rem;background:rgba(26,107,58,.07);color:var(--ncpd-green);padding:.18rem .55rem;border-radius:5px;font-size:.68rem;font-weight:700;width:fit-content;}
.card-title{font-family:'Cairo',sans-serif;font-size:.9rem;font-weight:800;color:var(--ink2);line-height:1.4;}
.card-desc{font-size:.78rem;color:var(--muted);line-height:1.7;flex:1;}

/* highlight matched text */
.highlight{background:rgba(201,160,64,.25);color:#6b4a00;border-radius:2px;padding:0 1px;}

.card-foot{padding:.9rem 1.3rem;border-top:1px solid var(--border);display:flex;gap:.6rem;}
.btn-details{flex:1;padding:.5rem;border-radius:8px;background:transparent;border:1.5px solid var(--border);color:var(--ink2);font-family:'Tajawal',sans-serif;font-size:.8rem;font-weight:600;cursor:pointer;transition:all .2s;}
.btn-details:hover{border-color:var(--ncpd-green);color:var(--ncpd-green);}
.btn-apply{flex:1;padding:.5rem;border-radius:8px;background:var(--ncpd-green);border:none;color:var(--white);font-family:'Tajawal',sans-serif;font-size:.8rem;font-weight:700;cursor:pointer;transition:all .2s;}
.btn-apply:hover{background:var(--ncpd-dark);}

.no-results{text-align:center;padding:4rem 2rem;color:var(--muted);}
.no-results h3{font-size:1.1rem;font-weight:700;margin-bottom:.5rem;color:var(--ink2);}

/* ══ ─────────── DETAIL VIEW ─────────── ══ */
.detail-layout{max-width:1400px;margin:0 auto;padding:2rem;display:grid;grid-template-columns:1fr 320px;gap:2rem;align-items:start;}

.detail-main{}
.detail-header{margin-bottom:1.5rem;}
.detail-audience-tag{display:inline-flex;align-items:center;gap:.3rem;background:rgba(26,107,58,.08);color:var(--ncpd-green);padding:.22rem .65rem;border-radius:6px;font-size:.72rem;font-weight:700;margin-bottom:.75rem;}
.detail-title{font-family:'Cairo',sans-serif;font-size:1.6rem;font-weight:900;color:var(--ink);margin-bottom:.75rem;}
.detail-apply-btn{
  display:inline-flex;align-items:center;gap:.5rem;
  background:var(--ncpd-green);color:var(--white);
  padding:.65rem 1.8rem;border-radius:10px;
  font-family:'Cairo',sans-serif;font-size:.92rem;font-weight:700;
  cursor:pointer;border:none;
  box-shadow:0 4px 16px rgba(26,107,58,.3);
  transition:all .2s;
}
.detail-apply-btn:hover{background:var(--ncpd-dark);box-shadow:0 6px 24px rgba(26,107,58,.4);}

.detail-desc-box{background:var(--white);border:1px solid var(--border);border-radius:14px;padding:1.5rem;margin-bottom:1.5rem;font-size:.88rem;color:var(--ink2);line-height:1.85;}

/* tabs */
.detail-tabs{display:flex;gap:0;border-bottom:2px solid var(--border);margin-bottom:1.5rem;}
.tab-btn2{padding:.7rem 1.2rem;background:transparent;border:none;border-bottom:3px solid transparent;margin-bottom:-2px;font-family:'Tajawal',sans-serif;font-size:.85rem;font-weight:600;color:var(--muted);cursor:pointer;transition:all .2s;white-space:nowrap;}
.tab-btn2:hover{color:var(--ink2);}
.tab-btn2.active{color:var(--ncpd-green);border-bottom-color:var(--ncpd-green);font-weight:700;}

.tab-content{display:none;}
.tab-content.active{display:block;animation:fadeUp .3s ease both;}
@keyframes fadeUp{from{opacity:0;transform:translateY(6px)}to{opacity:1;transform:translateY(0)}}

/* steps tab */
.steps-list{display:flex;flex-direction:column;gap:1rem;}
.step-item{background:var(--white);border:1px solid var(--border);border-radius:12px;padding:1.2rem 1.4rem;display:flex;gap:1rem;align-items:flex-start;}
.step-num{width:32px;height:32px;border-radius:50%;background:var(--ncpd-green);color:var(--white);display:flex;align-items:center;justify-content:center;font-family:'Cairo',sans-serif;font-size:.85rem;font-weight:800;flex-shrink:0;}
.step-body{}
.step-title{font-weight:700;font-size:.88rem;color:var(--ink);margin-bottom:.3rem;}
.step-desc{font-size:.8rem;color:var(--muted);line-height:1.65;}
.step-action{margin-top:.6rem;display:flex;flex-wrap:wrap;gap:.5rem;}

.step-link{
  display:inline-flex;align-items:center;gap:.35rem;
  padding:.3rem .75rem;border-radius:7px;font-size:.75rem;font-weight:600;
  text-decoration:none;cursor:pointer;transition:all .2s;border:none;
  font-family:'Tajawal',sans-serif;
}
.step-link.green{background:rgba(26,107,58,.09);color:var(--ncpd-green);border:1px solid rgba(26,107,58,.2);}
.step-link.green:hover{background:var(--ncpd-green);color:var(--white);}
.step-link.gold{background:rgba(201,160,64,.1);color:#8a6200;border:1px solid rgba(201,160,64,.3);}
.step-link.gold:hover{background:var(--nama-gold);color:var(--white);}

.video-placeholder{background:var(--ncpd-dark);border-radius:10px;padding:2rem;text-align:center;color:rgba(255,255,255,.7);margin-top:.75rem;cursor:pointer;transition:all .2s;border:2px dashed rgba(255,255,255,.15);}
.video-placeholder:hover{border-color:var(--ncpd-light);color:var(--white);}
.video-icon{font-size:2.5rem;margin-bottom:.5rem;}
.video-label{font-size:.8rem;}

/* conditions tab */
.cond-list-detail{display:flex;flex-direction:column;gap:.75rem;}
.cond-item{background:var(--white);border:1px solid var(--border);border-radius:11px;padding:1.1rem 1.3rem;}
.cond-header{display:flex;align-items:flex-start;gap:.75rem;}
.cond-check{width:26px;height:26px;border-radius:7px;background:rgba(26,107,58,.1);display:flex;align-items:center;justify-content:center;color:var(--ncpd-green);font-size:.85rem;flex-shrink:0;}
.cond-body{flex:1;}
.cond-name{font-size:.86rem;font-weight:700;color:var(--ink);margin-bottom:.25rem;}
.cond-desc{font-size:.78rem;color:var(--muted);line-height:1.6;margin-bottom:.5rem;}
.cond-links{display:flex;flex-wrap:wrap;gap:.4rem;}
.cond-link{display:inline-flex;align-items:center;gap:.3rem;padding:.25rem .65rem;border-radius:6px;font-size:.72rem;font-weight:600;text-decoration:none;transition:all .2s;}
.cond-link.platform{background:rgba(26,107,58,.09);color:var(--ncpd-green);border:1px solid rgba(26,107,58,.2);}
.cond-link.platform:hover{background:var(--ncpd-green);color:var(--white);}
.cond-link.whatsapp{background:rgba(37,211,102,.1);color:#1a7a40;border:1px solid rgba(37,211,102,.25);}
.cond-link.whatsapp:hover{background:#25d366;color:var(--white);}
.cond-link.phone{background:rgba(41,98,255,.08);color:#1a50cc;border:1px solid rgba(41,98,255,.2);}

/* documents tab */
.doc-list{display:flex;flex-direction:column;gap:.75rem;}
.doc-item{background:var(--white);border:1px solid var(--border);border-radius:11px;padding:1.1rem 1.3rem;display:flex;align-items:flex-start;gap:.9rem;}
.doc-icon{width:38px;height:38px;border-radius:9px;background:rgba(26,107,58,.08);display:flex;align-items:center;justify-content:center;font-size:1.2rem;flex-shrink:0;}
.doc-body{flex:1;}
.doc-name{font-size:.86rem;font-weight:700;color:var(--ink);margin-bottom:.2rem;}
.doc-source{font-size:.76rem;color:var(--muted);margin-bottom:.4rem;}
.doc-badge{display:inline-flex;align-items:center;gap:.25rem;padding:.15rem .5rem;border-radius:5px;font-size:.68rem;font-weight:700;}
.doc-badge.from-platform{background:rgba(26,107,58,.08);color:var(--ncpd-green);}
.doc-badge.from-govt{background:rgba(212,151,58,.1);color:#7a5000;}
.doc-badge.personal{background:rgba(100,100,200,.08);color:#3a4acc;}
.doc-link{display:inline-flex;align-items:center;gap:.25rem;margin-top:.4rem;font-size:.74rem;font-weight:600;color:var(--ncpd-green);text-decoration:none;cursor:pointer;}
.doc-link:hover{text-decoration:underline;}

/* ══ DETAIL SIDEBAR ══ */
.detail-sidebar{display:flex;flex-direction:column;gap:1rem;}
.sidebar-card{background:var(--white);border:1px solid var(--border);border-radius:12px;padding:1.2rem;}
.sidebar-card-title{font-family:'Cairo',sans-serif;font-size:.8rem;font-weight:800;color:var(--muted);letter-spacing:.05em;text-transform:uppercase;margin-bottom:.9rem;border-bottom:1px solid var(--border);padding-bottom:.6rem;}
.meta-row{display:flex;align-items:flex-start;gap:.75rem;padding:.5rem 0;border-bottom:1px solid rgba(0,0,0,.04);}
.meta-row:last-child{border-bottom:none;}
.meta-icon{width:30px;height:30px;border-radius:7px;background:rgba(26,107,58,.07);display:flex;align-items:center;justify-content:center;font-size:.9rem;flex-shrink:0;}
.meta-key{font-size:.7rem;color:var(--muted);margin-bottom:.1rem;}
.meta-val{font-size:.82rem;font-weight:700;color:var(--ink2);}

/* nama auth card in sidebar */
.nama-auth-card{
  background:linear-gradient(135deg,var(--ink2) 0%,var(--ncpd-dark) 100%);
  border-radius:12px;padding:1.3rem;
  position:relative;overflow:hidden;
}
.nama-auth-card::before{content:'🌴';position:absolute;left:1rem;top:50%;transform:translateY(-50%);font-size:5rem;opacity:.06;}
.nama-auth-title{font-family:'Cairo',sans-serif;font-size:.88rem;font-weight:800;color:var(--white);margin-bottom:.3rem;}
.nama-auth-desc{font-size:.75rem;color:rgba(255,255,255,.55);margin-bottom:1rem;line-height:1.6;}
.nama-auth-btn{
  display:flex;align-items:center;justify-content:center;gap:.5rem;
  background:linear-gradient(135deg,var(--nama-gold),#9a7820);
  color:var(--white);padding:.55rem;border-radius:8px;
  font-family:'Cairo',sans-serif;font-size:.82rem;font-weight:700;
  cursor:pointer;border:none;width:100%;
  box-shadow:0 3px 12px rgba(201,160,64,.3);
  transition:all .2s;
}
.nama-auth-btn:hover{box-shadow:0 5px 20px rgba(201,160,64,.5);transform:translateY(-1px);}

.contact-row{display:flex;align-items:center;gap:.6rem;padding:.45rem 0;font-size:.8rem;color:var(--ink2);}
.contact-row a{color:var(--ncpd-green);text-decoration:none;font-weight:600;}
.contact-row a:hover{text-decoration:underline;}

/* ══ NAMA LOGIN MODAL ══ */
.modal-backdrop{
  position:fixed;inset:0;z-index:900;
  background:rgba(10,25,16,.65);backdrop-filter:blur(4px);
  display:none;align-items:center;justify-content:center;
  padding:1rem;
}
.modal-backdrop.open{display:flex;}
.modal-box{
  background:var(--white);border-radius:20px;
  width:100%;max-width:440px;
  box-shadow:0 24px 80px rgba(0,0,0,.25);
  animation:modalIn .3s ease both;
  overflow:hidden;
}
@keyframes modalIn{from{opacity:0;transform:scale(.95) translateY(12px)}to{opacity:1;transform:scale(1) translateY(0)}}
.modal-header{
  background:linear-gradient(135deg,var(--ncpd-dark),var(--ncpd-green));
  padding:1.5rem 2rem;
  display:flex;align-items:center;justify-content:space-between;
}
.modal-brand{display:flex;align-items:center;gap:.75rem;}
.modal-logo-circle{
  width:44px;height:44px;border-radius:12px;
  background:linear-gradient(135deg,var(--nama-gold),#9a7820);
  display:flex;align-items:center;justify-content:center;font-size:1.3rem;
  box-shadow:0 3px 12px rgba(201,160,64,.35);
}
.modal-title{font-family:'Cairo',sans-serif;font-size:1rem;font-weight:900;color:var(--white);}
.modal-sub{font-size:.7rem;color:rgba(255,255,255,.6);}
.modal-close{background:rgba(255,255,255,.12);border:none;color:rgba(255,255,255,.8);width:30px;height:30px;border-radius:8px;cursor:pointer;font-size:1rem;display:flex;align-items:center;justify-content:center;transition:all .2s;}
.modal-close:hover{background:rgba(255,255,255,.25);color:var(--white);}

.modal-body{padding:1.8rem 2rem;}
.modal-desc{font-size:.82rem;color:var(--muted);line-height:1.65;margin-bottom:1.4rem;text-align:center;}

.field-group{margin-bottom:1rem;}
.field-label{font-size:.78rem;font-weight:700;color:var(--ink2);margin-bottom:.4rem;display:block;}
.field-input{
  width:100%;padding:.6rem 1rem;
  border:1.5px solid var(--border);border-radius:9px;
  font-family:'Tajawal',sans-serif;font-size:.88rem;color:var(--ink);
  background:var(--cream);transition:all .2s;outline:none;
}
.field-input:focus{border-color:var(--ncpd-green);background:var(--white);box-shadow:0 0 0 3px rgba(26,107,58,.1);}
.field-input::placeholder{color:rgba(0,0,0,.3);}

.modal-submit{
  width:100%;padding:.7rem;border-radius:10px;
  background:var(--ncpd-green);color:var(--white);border:none;
  font-family:'Cairo',sans-serif;font-size:.9rem;font-weight:700;
  cursor:pointer;transition:all .2s;margin-top:.5rem;
  box-shadow:0 4px 14px rgba(26,107,58,.3);
}
.modal-submit:hover{background:var(--ncpd-dark);box-shadow:0 6px 20px rgba(26,107,58,.4);}

.modal-divider{display:flex;align-items:center;gap:.75rem;margin:1rem 0;color:var(--muted);font-size:.75rem;}
.modal-divider::before,.modal-divider::after{content:'';flex:1;height:1px;background:var(--border);}

.nafaz-btn{
  width:100%;padding:.6rem;border-radius:10px;
  background:var(--cream);border:1.5px solid var(--border);
  color:var(--ink2);font-family:'Tajawal',sans-serif;font-size:.84rem;font-weight:600;
  cursor:pointer;transition:all .2s;display:flex;align-items:center;justify-content:center;gap:.5rem;
}
.nafaz-btn:hover{border-color:var(--ncpd-green);background:rgba(26,107,58,.04);}

/* ══ RESPONSIVE ══ */
@media(max-width:1100px){
  .services-layout{grid-template-columns:1fr;}
  .sidebar-filters{display:none;}
  .detail-layout{grid-template-columns:1fr;}
}
@media(max-width:768px){
  .header-nav{display:none;}
  .main-header .header-inner{padding:0 1rem;}
  .services-layout,.detail-layout{padding:1.2rem 1rem;}
  .detail-title{font-size:1.2rem;}
  .filter-pills{display:none;}
}
</style>
</head>
<body>

<!-- ══ INFO BAR ══ -->
<div class="info-bar">
  <div class="verify-badge">
    <span>🇸🇦</span>
    <span>موقع حكومي رسمي تابع لحكومة المملكة العربية السعودية</span>
    <a href="#">كيف تتحقق؟ ▾</a>
  </div>
  <div style="display:flex;gap:1.5rem;">
    <a href="#" style="color:rgba(255,255,255,.5);text-decoration:none;font-size:.72rem;">بوابة مزارع الإلكترونية 🌾</a>
  </div>
</div>

<!-- ══ MAIN HEADER ══ -->
<header class="main-header">
  <div class="header-inner">
    <!-- Logo -->
    <div class="logo-block">
      <div class="logo-emblem">
        <svg viewBox="0 0 54 54" fill="none" xmlns="http://www.w3.org/2000/svg">
          <rect width="54" height="54" rx="8" fill="#1a6b3a"/>
          <text x="27" y="38" text-anchor="middle" font-size="28" fill="white">🌴</text>
        </svg>
      </div>
      <div class="logo-text-block">
        <div class="logo-ar">المركز الوطني للنخيل والتمور</div>
        <div class="logo-en">NATIONAL CENTRE FOR PALMS & DATES</div>
      </div>
    </div>

    <!-- Nav -->
    <nav class="header-nav">
      <div class="nav-item has-arrow">عن المركز</div>
      <div class="nav-item">البرامج والمبادرات</div>
      <div class="nav-item has-arrow">الإعلام</div>
      <div class="nav-item active" onclick="showView('services')">الخدمات</div>
      <div class="nav-item">مركز الدعم</div>
      <div class="nav-item">الفرع الإلكتروني</div>
    </nav>

    <!-- Actions -->
    <div class="header-actions">
      <button class="lang-btn">English</button>
      <button class="nama-login-btn" onclick="openModal()">
        <span class="nama-icon">🌱</span>
        تسجيل الدخول عبر نما
      </button>
    </div>
  </div>
</header>

<!-- ══ SERVICES VIEW ══ -->
<div class="view active" id="view-services">

  <!-- Hero -->
  <div class="services-hero">
    <div class="services-hero-inner">
      <div class="breadcrumb-inner" style="padding:0;margin-bottom:1rem;background:transparent;">
        <span style="color:rgba(255,255,255,.5)">الرئيسية</span>
        <span class="bc-sep">›</span>
        <span class="bc-current">الخدمات</span>
      </div>
      <div class="hero-eyebrow">الخدمات الإلكترونية</div>
      <div class="hero-title">اطّلع على خدمات المركز</div>
      <div class="hero-sub">خدمات متكاملة لمزارعي النخيل والتمور في المملكة العربية السعودية</div>
      <div class="hero-count">📋 كل الخدمات (8)</div>
    </div>
  </div>

  <!-- Search & Filter Bar -->
  <div class="search-filter-bar">
    <div class="search-filter-inner">
      <div class="search-wrap">
        <span class="search-icon">🔍</span>
        <input class="search-input" id="mainSearch" type="text" placeholder="ابحث عن خدمة... مثال: شراء، دعم، علامة، تصدير"
          oninput="handleSearch(this.value)" onblur="setTimeout(()=>hideHints(),200)" onfocus="handleSearch(this.value)">
        <div class="search-hint" id="searchHints"></div>
      </div>
      <div class="filter-pills">
        <button class="filter-pill active" onclick="filterByAudience('all',this)">الكل</button>
        <button class="filter-pill" onclick="filterByAudience('مزارعين',this)">المزارعين</button>
        <button class="filter-pill" onclick="filterByAudience('تجار',this)">التجار والمصانع</button>
        <button class="filter-pill" onclick="filterByAudience('جمعيات',this)">الجمعيات</button>
      </div>
    </div>
  </div>

  <!-- Layout -->
  <div class="services-layout">
    <!-- Sidebar -->
    <aside class="sidebar-filters">
      <div class="sidebar-section">
        <div class="sidebar-title">تصفية حسب الفئة</div>
        <label class="filter-check"><input type="checkbox" checked onchange="renderCards()"><label>المزارعين <span>(5)</span></label></label>
        <label class="filter-check"><input type="checkbox" checked onchange="renderCards()"><label>التجار والمصانع <span>(2)</span></label></label>
        <label class="filter-check"><input type="checkbox" checked onchange="renderCards()"><label>الجمعيات الزراعية <span>(1)</span></label></label>
        <label class="filter-check"><input type="checkbox" checked onchange="renderCards()"><label>الباحثين <span>(1)</span></label></label>
      </div>
      <div class="sidebar-section">
        <div class="sidebar-title">تصفية حسب التكلفة</div>
        <label class="filter-check"><input type="checkbox" checked><label>مجاني</label></label>
        <label class="filter-check"><input type="checkbox" checked><label>برسوم</label></label>
      </div>
      <div class="sidebar-section">
        <div class="sidebar-title">مدة الخدمة</div>
        <label class="filter-check"><input type="checkbox" checked><label>فوري</label></label>
        <label class="filter-check"><input type="checkbox" checked><label>خلال أيام</label></label>
      </div>
    </aside>

    <!-- Cards -->
    <div>
      <div class="svc-count-bar">
        <div class="svc-count-text">عرض <strong id="shownCount">8</strong> من أصل <strong>8</strong> خدمات</div>
        <select class="sort-select"><option>الأحدث أولاً</option><option>الأكثر طلباً</option></select>
      </div>
      <div class="services-grid" id="servicesGrid"></div>
      <div class="no-results" id="noResults" style="display:none;">
        <div style="font-size:3rem;margin-bottom:1rem;">🔍</div>
        <h3>لا توجد نتائج مطابقة</h3>
        <p>جرّب البحث بكلمات أخرى مثل: دعم، شراء، علامة، تصدير</p>
      </div>
    </div>
  </div>
</div>

<!-- ══ DETAIL VIEW ══ -->
<div class="view" id="view-detail">
  <div class="breadcrumb-bar">
    <div class="breadcrumb-inner">
      <a href="#" onclick="showView('services')">الرئيسية</a>
      <span class="bc-sep">›</span>
      <a href="#" onclick="showView('services')">الخدمات</a>
      <span class="bc-sep">›</span>
      <span class="bc-current" id="detailBreadcrumb">تفاصيل الخدمة</span>
    </div>
  </div>

  <div class="detail-layout">
    <div class="detail-main" id="detailMain"></div>
    <div class="detail-sidebar" id="detailSidebar"></div>
  </div>
</div>

<!-- ══ NAMA LOGIN MODAL ══ -->
<div class="modal-backdrop" id="namaModal" onclick="handleModalClick(event)">
  <div class="modal-box">
    <div class="modal-header">
      <div class="modal-brand">
        <div class="modal-logo-circle">🌱</div>
        <div>
          <div class="modal-title">تسجيل الدخول عبر منصة نما</div>
          <div class="modal-sub">الدخول الموحد للخدمات الزراعية</div>
        </div>
      </div>
      <button class="modal-close" onclick="closeModal()">✕</button>
    </div>
    <div class="modal-body">
      <p class="modal-desc">سجّل دخولك عبر منصة <strong>نما</strong> للاستفادة من تحليل الأهلية التلقائي وتقديم الطلبات مباشرةً دون إعادة إدخال البيانات.</p>

      <div class="field-group">
        <label class="field-label">رقم الهوية الوطنية / الإقامة</label>
        <input class="field-input" type="text" placeholder="10XXXXXXXX" maxlength="10">
      </div>
      <div class="field-group">
        <label class="field-label">كلمة المرور</label>
        <input class="field-input" type="password" placeholder="••••••••">
      </div>
      <button class="modal-submit">دخول عبر منصة نما 🌱</button>

      <div class="modal-divider">أو</div>
      <button class="nafaz-btn">
        <span>🔐</span> تسجيل الدخول عبر نفاذ (الهوية الرقمية)
      </button>

      <div style="text-align:center;margin-top:1rem;font-size:.75rem;color:var(--muted);">
        ليس لديك حساب؟ <a href="#" style="color:var(--ncpd-green);font-weight:700;">إنشاء حساب جديد</a>
      </div>
    </div>
  </div>
</div>

<script>
/* ════════════════════════════════════════
   SERVICES DATA
════════════════════════════════════════ */
const SERVICES = [
  {
    id: 1,
    icon: '🤝',
    audience: 'مزارعين',
    title: 'تقديم طلب دعم الإعانة الزراعية لصغار المزارعين',
    titleShort: 'الإعانة الزراعية لصغار المزارعين',
    desc: 'خدمة تتيح لصغار مزارعي النخيل التقديم على دعم مادي غير مباشر يُضاف إلى دعم محفظة المزارع لاستخدامه عبر منصة "مزارع" لشراء المدخلات والمستلزمات الزراعية.',
    keywords: ['دعم','إعانة','مزارع','صغار','نخيل','مالي'],
    duration: 'فوري', cost: 'مجاني', channel: 'الويب',
    steps: [
      { title:'تسجيل الدخول عبر منصة نما', desc:'اضغط على زر "طلب الخدمة" وسيتم توجيهك لتسجيل الدخول عبر منصة نما أو نفاذ.', links:[{label:'منصة نما',type:'gold',href:'#'},{label:'فرع إلكتروني للمساعدة',type:'green',href:'#'}], video:true },
      { title:'التحقق التلقائي من الأهلية', desc:'يقوم النظام تلقائياً بسحب بياناتك من منصات حصر وري ونما والتحقق من استيفاء الشروط.', links:[], video:false },
      { title:'تعبئة نموذج الطلب', desc:'أدخل بيانات المزرعة ومعلومات الموسم الزراعي وقم بإرفاق المستندات المطلوبة.', links:[{label:'الفرع الإلكتروني',type:'green',href:'#'}], video:false },
      { title:'مراجعة الطلب والموافقة', desc:'يتم مراجعة الطلب خلال مدة قصيرة وإرسال إشعار بالنتيجة على جوالك.', links:[], video:false },
    ],
    conditions: [
      { name:'شهادة ري سارية من منصة ري', desc:'يجب أن يكون لديك شهادة ري صادرة وسارية المفعول من منصة ري الوطنية.',
        links:[{label:'منصة ري',type:'platform',href:'https://ri.gov.sa'},{label:'واتساب ري',type:'whatsapp',href:'https://wa.me/966XXXXXXXX'},{label:'920XXXXXX',type:'phone'}] },
      { name:'رخصة ممارسة الأنشطة الزراعية من منصة نما', desc:'استخرج رخصة ممارسة الأنشطة من منصة نما قبل التقديم.',
        links:[{label:'منصة نما — استخراج رخصة',type:'platform',href:'#'},{label:'واتساب نما',type:'whatsapp',href:'https://wa.me/966XXXXXXXX'}] },
      { name:'مساحة المزرعة لا تتجاوز ٥٠ دونماً', desc:'يجب أن تكون المساحة المسوحة في منصة حصر ٥٠ دونماً أو أقل.',
        links:[{label:'منصة حصر — تحديث المساحة',type:'platform',href:'#'},{label:'تواصل مع حصر',type:'whatsapp',href:'https://wa.me/966XXXXXXXX'}] },
      { name:'عدد النخيل لا يتجاوز ٥٠٠ نخلة', desc:'الخدمة مخصصة لصغار المزارعين بحد أقصى ٥٠٠ نخلة مسجلة.',
        links:[{label:'تحديث بيانات النخيل في حصر',type:'platform',href:'#'}] },
    ],
    docs: [
      { icon:'🪪', name:'صورة الهوية الوطنية', source:'وثيقة شخصية', badge:'personal', badgeLabel:'وثيقة شخصية', where:'يُقدم من قبل المتقدم' },
      { icon:'💧', name:'شهادة ري سارية', source:'منصة ري الوطنية', badge:'from-platform', badgeLabel:'من منصة ري', where:'يمكن استخراجها من منصة ري على ri.gov.sa', link:'#' },
      { icon:'🌾', name:'رخصة ممارسة الأنشطة الزراعية', source:'منصة نما', badge:'from-platform', badgeLabel:'من منصة نما', where:'يمكن استخراجها من منصة نما', link:'#' },
      { icon:'🗺', name:'مستخرج بيانات المزرعة من حصر', source:'منصة حصر الوطنية', badge:'from-govt', badgeLabel:'من منصة حصر', where:'يمكن استخراجه من منصة حصر الوطنية', link:'#' },
    ],
  },
  {
    id: 2,
    icon: '🌴',
    audience: 'مزارعين',
    title: 'حجز موعد توريد التمور (ممتازة / عادية)',
    titleShort: 'حجز موعد توريد وشراء التمور',
    desc: 'تمكّنك هذه الخدمة من حجز موعد لتوريد التمور ضمن الفئات المتاحة: ممتازة وعادية. تضمن الخدمة شراء المنتج بأسعار مضمونة ومحددة مسبقاً.',
    keywords: ['شراء','تمور','توريد','حجز','موعد','بيع','تسويق'],
    duration: 'فوري', cost: 'مجاني', channel: 'الويب',
    steps: [
      { title:'الدخول وإثبات الهوية', desc:'سجّل دخولك عبر منصة نما للتحقق التلقائي من تسجيلك كمنتج تمور مؤهل.', links:[{label:'منصة نما',type:'gold',href:'#'}], video:true },
      { title:'اختيار نوع التمور والموعد', desc:'حدد فئة التمور (ممتازة/عادية) والكمية المتوقعة وتاريخ التوريد المناسب.', links:[], video:false },
      { title:'تأكيد الحجز واستلام الرقم المرجعي', desc:'يصلك رقم مرجعي على جوالك ورسالة تأكيد تتضمن موقع مركز الاستلام.', links:[{label:'الفرع الإلكتروني',type:'green',href:'#'}], video:false },
    ],
    conditions: [
      { name:'شهادة ري سارية', desc:'يجب توفر شهادة ري سارية من منصة ري.',
        links:[{label:'منصة ري',type:'platform',href:'#'},{label:'واتساب ري',type:'whatsapp',href:'#'}] },
      { name:'رخصة ممارسة الأنشطة من نما', desc:'رخصة ممارسة النشاط الزراعي من منصة نما.',
        links:[{label:'استخراج رخصة نما',type:'platform',href:'#'}] },
      { name:'عدد النخيل لا يتجاوز ٥٠٠ نخلة', desc:'حد أقصى للخدمة ٥٠٠ نخلة مسجلة في منصة حصر.',
        links:[{label:'منصة حصر',type:'platform',href:'#'}] },
      { name:'مساحة المزرعة لا تتجاوز ٥٠ دونماً', desc:'المساحة المسوحة يجب ألا تتجاوز ٥٠ دونماً.',
        links:[{label:'تحديث في حصر',type:'platform',href:'#'},{label:'واتساب حصر',type:'whatsapp',href:'#'}] },
    ],
    docs: [
      { icon:'🪪', name:'الهوية الوطنية', source:'وثيقة شخصية', badge:'personal', badgeLabel:'وثيقة شخصية', where:'يُقدم من قبل المتقدم' },
      { icon:'💧', name:'شهادة ري', source:'منصة ري', badge:'from-platform', badgeLabel:'من منصة ري', where:'ri.gov.sa', link:'#' },
      { icon:'🌱', name:'رخصة نما', source:'منصة نما', badge:'from-platform', badgeLabel:'من منصة نما', where:'منصة نما', link:'#' },
    ],
  },
  {
    id: 3,
    icon: '🏅',
    audience: 'مزارعين',
    title: 'فحص علامة التمور السعودية',
    titleShort: 'فحص علامة التمور السعودية',
    desc: 'خدمة للتحقق من استيفاء المنتج لمعايير علامة التمور السعودية ومنح الاعتماد اللازم للتسويق المحلي والتصدير.',
    keywords: ['علامة','تمور','سعودية','جودة','اعتماد','فحص'],
    duration: 'خلال أيام', cost: 'برسوم', channel: 'الويب',
    steps: [
      { title:'تسجيل الدخول وتقديم الطلب', desc:'سجّل دخولك عبر نما وتقدم بطلب فحص المنتج مع إرفاق عينات.', links:[{label:'منصة نما',type:'gold',href:'#'}], video:true },
      { title:'إرسال العينات للمختبر', desc:'يصلك عنوان المختبر المعتمد وطريقة إرسال العينات بعد تأكيد الطلب.', links:[], video:false },
      { title:'استلام شهادة الفحص', desc:'تصدر نتيجة الفحص خلال ٥ أيام عمل وترسل إلكترونياً.', links:[{label:'الفرع الإلكتروني',type:'green',href:'#'}], video:false },
    ],
    conditions: [
      { name:'تسجيل المزرعة في منصة نما', desc:'يجب أن تكون المزرعة مسجلة ولديها رخصة نشاط سارية.',
        links:[{label:'منصة نما',type:'platform',href:'#'}] },
      { name:'مطابقة المواصفات القياسية للجودة', desc:'يجب أن تستوفي التمور معايير SASO للجودة والسلامة الغذائية.',
        links:[{label:'موقع SASO',type:'platform',href:'https://saso.gov.sa'},{label:'800 244 7444',type:'phone'}] },
    ],
    docs: [
      { icon:'🪪', name:'الهوية الوطنية', source:'وثيقة شخصية', badge:'personal', badgeLabel:'وثيقة شخصية', where:'يُقدم من قبل المتقدم' },
      { icon:'📄', name:'سجل تجاري / رخصة نشاط', source:'وزارة التجارة / نما', badge:'from-govt', badgeLabel:'من الجهات الحكومية', where:'منصة نما أو وزارة التجارة', link:'#' },
    ],
  },
  {
    id: 4,
    icon: '🚢',
    audience: 'تجار',
    title: 'إصدار شهادة المنشأ والتصدير للتمور',
    titleShort: 'شهادة المنشأ والتصدير',
    desc: 'تمكّن هذه الخدمة المصدّرين من استخراج شهادات المنشأ المعتمدة للتمور السعودية لتسهيل عمليات التصدير للأسواق الدولية.',
    keywords: ['تصدير','شهادة','منشأ','تمور','دولي','أسواق'],
    duration: 'خلال أيام', cost: 'برسوم', channel: 'الويب',
    steps: [
      { title:'الدخول وتقديم الطلب', desc:'قدّم طلب شهادة المنشأ مع بيانات الشحنة والمستورد.', links:[{label:'منصة نما',type:'gold',href:'#'},{label:'الفرع الإلكتروني',type:'green',href:'#'}], video:true },
      { title:'مراجعة الوثائق', desc:'يراجع فريق المركز وثائق المنتج والشحنة خلال يومي عمل.', links:[], video:false },
      { title:'استلام الشهادة إلكترونياً', desc:'تُصدر الشهادة إلكترونياً وبإمكانك طباعتها أو مشاركتها رقمياً.', links:[], video:false },
    ],
    conditions: [
      { name:'سجل تجاري ساري', desc:'يجب توفر سجل تجاري ساري المفعول.',
        links:[{label:'وزارة التجارة',type:'platform',href:'https://mc.gov.sa'}] },
      { name:'شهادة علامة التمور السعودية', desc:'يجب الحصول على شهادة العلامة أولاً.',
        links:[{label:'خدمة فحص العلامة',type:'platform',href:'#'}] },
    ],
    docs: [
      { icon:'📄', name:'السجل التجاري', source:'وزارة التجارة', badge:'from-govt', badgeLabel:'من وزارة التجارة', where:'منصة Maroof أو وزارة التجارة', link:'https://mc.gov.sa' },
      { icon:'🏅', name:'شهادة العلامة السعودية', source:'المركز الوطني للنخيل', badge:'from-platform', badgeLabel:'من المركز', where:'بعد إتمام خدمة الفحص', link:'#' },
      { icon:'📦', name:'بيانات الشحنة (نوع، كمية، وجهة)', source:'وثيقة تجارية', badge:'personal', badgeLabel:'وثيقة تجارية', where:'يُقدم من قبل المتقدم' },
    ],
  },
  {
    id: 5,
    icon: '🌾',
    audience: 'مزارعين',
    title: 'خدمة تنظيف وتشويك رأس النخلة',
    titleShort: 'تنظيف وتشويك رأس النخلة',
    desc: 'خدمة تنظيف رأس النخلة وإزالة الجريد الجاف والتشويك وخدمات العناية بالنخلة تُقدّمها فرق متخصصة معتمدة من المركز.',
    keywords: ['تنظيف','تشويك','نخلة','جريد','خدمة','عناية'],
    duration: 'خلال أيام', cost: 'برسوم', channel: 'الويب',
    steps: [
      { title:'تحديد موقع المزرعة والنخيل', desc:'أدخل بيانات المزرعة وعدد النخيل المراد خدمتها.', links:[{label:'منصة نما',type:'gold',href:'#'}], video:false },
      { title:'تحديد الموعد المناسب', desc:'اختر الموعد المناسب من المواعيد المتاحة في منطقتك.', links:[], video:false },
      { title:'تنفيذ الخدمة واستلام التقرير', desc:'تُنفَّذ الخدمة من فريق متخصص ويُرسل تقرير حالة النخيل.', links:[{label:'الفرع الإلكتروني',type:'green',href:'#'}], video:true },
    ],
    conditions: [
      { name:'تسجيل المزرعة في نما أو مزارع', desc:'يجب أن تكون المزرعة مسجلة في منصة نما أو البوابة الزراعية.',
        links:[{label:'منصة نما',type:'platform',href:'#'},{label:'بوابة مزارع',type:'platform',href:'#'}] },
    ],
    docs: [
      { icon:'🪪', name:'الهوية الوطنية', source:'وثيقة شخصية', badge:'personal', badgeLabel:'وثيقة شخصية', where:'يُقدم من قبل المتقدم' },
      { icon:'🗺', name:'تفاصيل موقع المزرعة (إحداثيات / حصر)', source:'منصة حصر', badge:'from-govt', badgeLabel:'من منصة حصر', where:'منصة حصر الوطنية', link:'#' },
    ],
  },
  {
    id: 6,
    icon: '🔄',
    audience: 'تجار',
    title: 'تقديم طلب الانضمام لمصانع إعادة التدوير القائمة',
    titleShort: 'الانضمام لمصانع إعادة التدوير',
    desc: 'تسجيل مصانع إعادة تدوير متبقيات النخيل وعرضها على موقع المركز لتوصيلها بالمزارعين والموردين.',
    keywords: ['تدوير','مصانع','متبقيات','نخيل','انضمام','صناعة'],
    duration: 'خلال أيام', cost: 'مجاني', channel: 'الويب',
    steps: [
      { title:'تقديم الطلب إلكترونياً', desc:'سجّل بيانات المصنع وطاقته الاستيعابية وأنواع المخلفات المقبولة.', links:[{label:'الفرع الإلكتروني',type:'green',href:'#'}], video:false },
      { title:'مراجعة ومعاينة المصنع', desc:'تُجري لجنة من المركز معاينة ميدانية للمصنع خلال أسبوعين.', links:[], video:false },
    ],
    conditions: [
      { name:'سجل تجاري ساري للمصنع', desc:'يجب أن يكون المصنع مرخصاً ولديه سجل تجاري ساري.',
        links:[{label:'وزارة التجارة',type:'platform',href:'https://mc.gov.sa'}] },
      { name:'رخصة البلدية للنشاط الصناعي', desc:'رخصة نشاط من البلدية أو الهيئة السعودية للمدن الصناعية.',
        links:[{label:'موقع مدن',type:'platform',href:'https://modon.gov.sa'}] },
    ],
    docs: [
      { icon:'📄', name:'السجل التجاري', source:'وزارة التجارة', badge:'from-govt', badgeLabel:'من وزارة التجارة', where:'منصة Maroof', link:'https://mc.gov.sa' },
      { icon:'🏭', name:'رخصة النشاط الصناعي', source:'البلدية / مدن', badge:'from-govt', badgeLabel:'من الجهات البلدية', where:'البلدية المختصة أو موقع مدن', link:'#' },
    ],
  },
  {
    id: 7,
    icon: '🌲',
    audience: 'مزارعين',
    title: 'خدمة نقل نوائج النخيل الثانوية من المزارع',
    titleShort: 'نقل نوائج النخيل الثانوية',
    desc: 'خدمة تُمكّن المزارعين من طلب نقل النوائج (الفسائل) الثانوية من مزارعهم إلى مواقع الزراعة المعتمدة أو الباحثين.',
    keywords: ['نوائج','فسائل','نخيل','نقل','مزارع'],
    duration: 'خلال أيام', cost: 'مجاني', channel: 'الويب',
    steps: [
      { title:'تقديم الطلب وتحديد الكمية', desc:'أدخل عدد النوائج المراد نقلها وموقع المزرعة.', links:[{label:'منصة نما',type:'gold',href:'#'}], video:false },
      { title:'جدولة النقل', desc:'يتم التواصل معك لتحديد موعد النقل المناسب.', links:[], video:false },
    ],
    conditions: [
      { name:'تسجيل المزرعة في منصة حصر', desc:'يجب أن تكون المزرعة وبياناتها مسجلة في منصة حصر.',
        links:[{label:'منصة حصر',type:'platform',href:'#'},{label:'واتساب حصر',type:'whatsapp',href:'#'}] },
    ],
    docs: [
      { icon:'🪪', name:'الهوية الوطنية', source:'وثيقة شخصية', badge:'personal', badgeLabel:'وثيقة شخصية', where:'يُقدم من قبل المتقدم' },
      { icon:'🗺', name:'مستخرج تسجيل المزرعة من حصر', source:'منصة حصر', badge:'from-govt', badgeLabel:'من منصة حصر', where:'منصة حصر الوطنية', link:'#' },
    ],
  },
  {
    id: 8,
    icon: '🔬',
    audience: 'جمعيات',
    title: 'تقديم طلب اعتماد مركز تبخير للتمور',
    titleShort: 'اعتماد مركز تبخير للتمور',
    desc: 'خدمة لاعتماد مراكز تبخير التمور وضمان مطابقتها للاشتراطات الصحية والمعايير الدولية لتصدير التمور.',
    keywords: ['تبخير','اعتماد','مركز','جودة','صحي','تصدير'],
    duration: 'خلال أيام', cost: 'برسوم', channel: 'الويب',
    steps: [
      { title:'تقديم الطلب مع الوثائق', desc:'ارفق الوثائق المطلوبة وبيانات المركز وموقعه.', links:[{label:'الفرع الإلكتروني',type:'green',href:'#'}], video:false },
      { title:'معاينة ميدانية', desc:'تُجرى معاينة ميدانية من قبل فريق المركز خلال أسبوعين.', links:[], video:false },
      { title:'إصدار شهادة الاعتماد', desc:'تُصدر شهادة الاعتماد لمدة سنة قابلة للتجديد.', links:[], video:false },
    ],
    conditions: [
      { name:'سجل تجاري للمنشأة', desc:'وجود سجل تجاري ساري للمنشأة.',
        links:[{label:'وزارة التجارة',type:'platform',href:'https://mc.gov.sa'}] },
      { name:'استيفاء اشتراطات الهيئة الغذائية', desc:'يجب مطابقة اشتراطات الهيئة العامة للغذاء والدواء.',
        links:[{label:'موقع SFDA',type:'platform',href:'https://sfda.gov.sa'}] },
    ],
    docs: [
      { icon:'📄', name:'السجل التجاري', source:'وزارة التجارة', badge:'from-govt', badgeLabel:'من وزارة التجارة', where:'منصة Maroof', link:'https://mc.gov.sa' },
      { icon:'🏭', name:'مخططات المنشأة المعتمدة', source:'وثيقة مهنية', badge:'personal', badgeLabel:'وثيقة مهنية', where:'مكتب هندسي معتمد' },
      { icon:'🔬', name:'تقرير السلامة الغذائية', source:'SFDA', badge:'from-govt', badgeLabel:'من SFDA', where:'موقع الهيئة العامة للغذاء والدواء', link:'https://sfda.gov.sa' },
    ],
  },
];

/* ════════════════════════════════════════
   STATE
════════════════════════════════════════ */
let currentQuery = '';
let currentAudience = 'all';

/* ════════════════════════════════════════
   SEARCH
════════════════════════════════════════ */
function handleSearch(q) {
  currentQuery = q.trim().toLowerCase();
  const hintsEl = document.getElementById('searchHints');

  if (!currentQuery) { hideHints(); renderCards(); return; }

  const matches = SERVICES.filter(s =>
    s.title.includes(currentQuery) ||
    s.keywords.some(k => k.includes(currentQuery)) ||
    s.desc.includes(currentQuery)
  );

  if (matches.length === 0) {
    hintsEl.innerHTML = `<div class="hint-no-results">لا توجد نتائج لـ "${currentQuery}"</div>`;
  } else {
    hintsEl.innerHTML = matches.slice(0,5).map(s => `
      <div class="hint-item" onclick="selectHint('${s.title}',${s.id})">
        <span>${s.icon}</span>
        <span>${highlightText(s.titleShort, currentQuery)}</span>
        <span class="hint-tag">${s.audience}</span>
      </div>`).join('');
  }
  hintsEl.classList.add('show');
  renderCards();
}

function selectHint(title, id) {
  document.getElementById('mainSearch').value = '';
  currentQuery = '';
  hideHints();
  showDetail(id);
}

function hideHints() {
  document.getElementById('searchHints').classList.remove('show');
}

function highlightText(text, query) {
  if (!query) return text;
  const re = new RegExp(`(${query})`, 'gi');
  return text.replace(re, '<span class="highlight">$1</span>');
}

/* ════════════════════════════════════════
   FILTER
════════════════════════════════════════ */
function filterByAudience(aud, btn) {
  currentAudience = aud;
  document.querySelectorAll('.filter-pill').forEach(p => p.classList.remove('active'));
  btn.classList.add('active');
  renderCards();
}

/* ════════════════════════════════════════
   RENDER CARDS
════════════════════════════════════════ */
function renderCards() {
  const grid = document.getElementById('servicesGrid');
  const noRes = document.getElementById('noResults');

  let filtered = SERVICES;
  if (currentAudience !== 'all') {
    filtered = filtered.filter(s => s.audience.includes(currentAudience));
  }
  if (currentQuery) {
    filtered = filtered.filter(s =>
      s.title.includes(currentQuery) ||
      s.keywords.some(k => k.includes(currentQuery)) ||
      s.desc.includes(currentQuery)
    );
  }

  document.getElementById('shownCount').textContent = filtered.length;

  if (filtered.length === 0) {
    grid.innerHTML = '';
    noRes.style.display = 'block';
    return;
  }
  noRes.style.display = 'none';

  grid.innerHTML = filtered.map((s, i) => `
    <div class="svc-card" style="animation-delay:${i*.07}s" onclick="showDetail(${s.id})">
      <div class="card-top">
        <div class="card-icon-area">${s.icon}</div>
        <div class="card-audience">👤 ${s.audience}</div>
        <div class="card-title">${highlightText(s.title, currentQuery)}</div>
        <div class="card-desc">${s.desc.substring(0,100)}...</div>
      </div>
      <div class="card-foot">
        <button class="btn-details" onclick="event.stopPropagation();showDetail(${s.id})">التفاصيل</button>
        <button class="btn-apply" onclick="event.stopPropagation();openModal()">طلب الخدمة</button>
      </div>
    </div>`).join('');
}

/* ════════════════════════════════════════
   DETAIL PAGE
════════════════════════════════════════ */
function showDetail(id) {
  const s = SERVICES.find(x => x.id === id);
  if (!s) return;

  document.getElementById('detailBreadcrumb').textContent = s.titleShort;

  /* build steps */
  const stepsHtml = s.steps.map((step, i) => {
    const linksHtml = step.links.map(l =>
      `<a class="step-link ${l.type}" href="${l.href||'#'}" target="_blank">${l.label}</a>`
    ).join('');
    const videoHtml = step.video ? `
      <div class="video-placeholder" onclick="alert('سيتم تشغيل الفيديو التوضيحي')">
        <div class="video-icon">▶️</div>
        <div class="video-label">شاهد فيديو شرح الخطوة</div>
      </div>` : '';
    return `
    <div class="step-item">
      <div class="step-num">${i+1}</div>
      <div class="step-body">
        <div class="step-title">${step.title}</div>
        <div class="step-desc">${step.desc}</div>
        <div class="step-action">${linksHtml}</div>
        ${videoHtml}
      </div>
    </div>`;
  }).join('');

  /* build conditions */
  const condsHtml = s.conditions.map(c => {
    const linksHtml = c.links.map(l => {
      if (l.type === 'phone') return `<span class="cond-link phone">📞 ${l.label}</span>`;
      return `<a class="cond-link ${l.type}" href="${l.href||'#'}" target="_blank">${l.type==='whatsapp'?'💬':l.type==='platform'?'🔗':''} ${l.label}</a>`;
    }).join('');
    return `
    <div class="cond-item">
      <div class="cond-header">
        <div class="cond-check">✓</div>
        <div class="cond-body">
          <div class="cond-name">${c.name}</div>
          <div class="cond-desc">${c.desc}</div>
          <div class="cond-links">${linksHtml}</div>
        </div>
      </div>
    </div>`;
  }).join('');

  /* build docs */
  const docsHtml = s.docs.map(d => {
    const linkHtml = d.link ? `<a class="doc-link" href="${d.link}" target="_blank">🔗 اذهب للمصدر</a>` : '';
    return `
    <div class="doc-item">
      <div class="doc-icon">${d.icon}</div>
      <div class="doc-body">
        <div class="doc-name">${d.name}</div>
        <div class="doc-source">📍 المصدر: ${d.where}</div>
        <span class="doc-badge ${d.badge}">${d.badgeLabel}</span>
        ${linkHtml}
      </div>
    </div>`;
  }).join('');

  document.getElementById('detailMain').innerHTML = `
    <div class="detail-header">
      <div class="detail-audience-tag">👤 ${s.audience}</div>
      <div class="detail-title">${s.title}</div>
      <button class="detail-apply-btn" onclick="openModal()">طلب الخدمة ←</button>
    </div>
    <div class="detail-desc-box">${s.desc}</div>
    <div class="detail-tabs">
      <button class="tab-btn2 active" onclick="switchTab('steps',this)">الخطوات</button>
      <button class="tab-btn2" onclick="switchTab('conditions',this)">شروط الاستخدام</button>
      <button class="tab-btn2" onclick="switchTab('docs',this)">المستندات المطلوبة</button>
      <button class="tab-btn2" onclick="switchTab('faq',this)">الأسئلة الشائعة</button>
    </div>
    <div class="tab-content active" id="tab-steps">
      <div class="steps-list">${stepsHtml}</div>
    </div>
    <div class="tab-content" id="tab-conditions">
      <div class="cond-list-detail">${condsHtml}</div>
    </div>
    <div class="tab-content" id="tab-docs">
      <div class="doc-list">${docsHtml}</div>
    </div>
    <div class="tab-content" id="tab-faq">
      <div style="color:var(--muted);padding:2rem;text-align:center;font-size:.88rem;">
        🔗 للاطلاع على الأسئلة الشائعة تفضل بزيارة <a href="https://ncpd.gov.sa/ar/faqs" target="_blank" style="color:var(--ncpd-green);font-weight:700;">صفحة الأسئلة الشائعة</a>
        أو تواصل معنا على <strong style="color:var(--ink);">8003010055</strong>
      </div>
    </div>
  `;

  document.getElementById('detailSidebar').innerHTML = `
    <div class="nama-auth-card">
      <div class="nama-auth-title">سجّل دخولك عبر منصة نما</div>
      <div class="nama-auth-desc">للاستفادة من التحليل التلقائي للأهلية وتقديم الطلبات فوراً دون إعادة إدخال البيانات.</div>
      <button class="nama-auth-btn" onclick="openModal()"><span>🌱</span> دخول عبر منصة نما</button>
    </div>
    <div class="sidebar-card">
      <div class="sidebar-card-title">معلومات الخدمة</div>
      <div class="meta-row"><div class="meta-icon">⏱</div><div><div class="meta-key">مدة الخدمة</div><div class="meta-val">${s.duration}</div></div></div>
      <div class="meta-row"><div class="meta-icon">💰</div><div><div class="meta-key">تكلفة الخدمة</div><div class="meta-val">${s.cost}</div></div></div>
      <div class="meta-row"><div class="meta-icon">💻</div><div><div class="meta-key">قنوات الخدمة</div><div class="meta-val">${s.channel}</div></div></div>
      <div class="meta-row"><div class="meta-icon">👤</div><div><div class="meta-key">الفئة المستهدفة</div><div class="meta-val">${s.audience}</div></div></div>
    </div>
    <div class="sidebar-card">
      <div class="sidebar-card-title">تواصل معنا</div>
      <div class="contact-row">📞 <a href="tel:8003010055">8003010055</a></div>
      <div class="contact-row">✉️ <a href="mailto:info@ncpd.gov.sa">info@ncpd.gov.sa</a></div>
      <div class="contact-row">💬 <a href="https://wa.me/966XXXXXXXX" target="_blank">واتساب المركز</a></div>
      <div class="contact-row">🌐 <a href="https://ncpd.gov.sa/ar/faqs" target="_blank">الأسئلة الشائعة</a></div>
    </div>
    <div class="sidebar-card">
      <div class="sidebar-card-title">الفرع الإلكتروني</div>
      <div style="font-size:.8rem;color:var(--muted);line-height:1.65;margin-bottom:.75rem;">تحتاج مساعدة في إتمام طلبك؟ تواصل مع موظفي الفرع الإلكتروني مباشرة.</div>
      <a class="step-link green" href="#" style="display:inline-flex;width:100%;justify-content:center;text-decoration:none;">🖥 الفرع الإلكتروني</a>
    </div>
  `;

  showView('detail');
  window.scrollTo({top:0,behavior:'smooth'});
}

function switchTab(tabId, btn) {
  document.querySelectorAll('.tab-btn2').forEach(b => b.classList.remove('active'));
  document.querySelectorAll('.tab-content').forEach(c => c.classList.remove('active'));
  btn.classList.add('active');
  document.getElementById(`tab-${tabId}`).classList.add('active');
}

/* ════════════════════════════════════════
   VIEWS
════════════════════════════════════════ */
function showView(name) {
  document.querySelectorAll('.view').forEach(v => v.classList.remove('active'));
  document.getElementById(`view-${name}`).classList.add('active');
}

/* ════════════════════════════════════════
   MODAL
════════════════════════════════════════ */
function openModal() {
  document.getElementById('namaModal').classList.add('open');
  document.body.style.overflow = 'hidden';
}
function closeModal() {
  document.getElementById('namaModal').classList.remove('open');
  document.body.style.overflow = '';
}
function handleModalClick(e) {
  if (e.target === document.getElementById('namaModal')) closeModal();
}
document.addEventListener('keydown', e => { if(e.key==='Escape') closeModal(); });

/* ════════════════════════════════════════
   INIT
════════════════════════════════════════ */
renderCards();
</script>
</body>
</html>
