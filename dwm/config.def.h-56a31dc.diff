diff --git a/config.def.h b/config.def.h
index fd77a07..135d18f 100644
--- a/config.def.h
+++ b/config.def.h
@@ -1,21 +1,22 @@
 /* See LICENSE file for copyright and license details. */
 
 /* appearance */
-static const unsigned int borderpx  = 1;        /* border pixel of windows */
+static const unsigned int borderpx  = 3;        /* border pixel of windows */
 static const unsigned int snap      = 32;       /* snap pixel */
 static const int showbar            = 1;        /* 0 means no bar */
 static const int topbar             = 1;        /* 0 means bottom bar */
-static const char *fonts[]          = { "monospace:size=10" };
+static const char *fonts[]          = { "-*-terminus-medium-r-*-*-10-*-*-*-*-*-*-*" };
 static const char dmenufont[]       = "monospace:size=10";
 static const char col_gray1[]       = "#222222";
 static const char col_gray2[]       = "#444444";
 static const char col_gray3[]       = "#bbbbbb";
 static const char col_gray4[]       = "#eeeeee";
 static const char col_cyan[]        = "#005577";
+static const char col_selborder[]        = "#ff6633";
 static const char *colors[SchemeLast][3]      = {
 	/*               fg         bg         border   */
 	[SchemeNorm] = { col_gray3, col_gray1, col_gray2 },
-	[SchemeSel] =  { col_gray4, col_cyan,  col_cyan  },
+	[SchemeSel] =  { col_gray4, col_cyan,  col_selborder  },
 };
 
 /* tagging */
@@ -57,10 +58,12 @@ static const Layout layouts[] = {
 /* commands */
 static char dmenumon[2] = "0"; /* component of dmenucmd, manipulated in spawn() */
 static const char *dmenucmd[] = { "dmenu_run", "-m", dmenumon, "-fn", dmenufont, "-nb", col_gray1, "-nf", col_gray3, "-sb", col_cyan, "-sf", col_gray4, NULL };
-static const char *termcmd[]  = { "st", NULL };
+static const char *termcmd[]  = { "xterm", "-fa", "Mono", "-fs", "9",  NULL };
+static const char *slockcmd[]  = { "slock", NULL };
 
 static Key keys[] = {
 	/* modifier                     key        function        argument */
+	{ MODKEY,                       XK_q,      spawn,          {.v = slockcmd } },
 	{ MODKEY,                       XK_p,      spawn,          {.v = dmenucmd } },
 	{ MODKEY|ShiftMask,             XK_Return, spawn,          {.v = termcmd } },
 	{ MODKEY,                       XK_b,      togglebar,      {0} },
