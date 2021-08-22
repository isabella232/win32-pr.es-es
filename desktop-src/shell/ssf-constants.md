---
description: Usado por la función SHGetSetSettings para especificar qué miembros de su estructura SHELLSTATE se deben establecer o volver a derivar.
title: Constantes SSF (Shlobj.h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 2a883110-fdc3-4451-9e47-e58894600e3b
api_name:
- SSF_SHOWALLOBJECTS
- SSF_SHOWEXTENSIONS
- SSF_HIDDENFILEEXTS
- SSF_SERVERADMINUI
- SSF_SHOWCOMPCOLOR
- SSF_SORTCOLUMNS
- SSF_SHOWSYSFILES
- SSF_DOUBLECLICKINWEBVIEW
- SSF_SHOWATTRIBCOL
- SSF_DESKTOPHTML
- SSF_WIN95CLASSIC
- SSF_DONTPRETTYPATH
- SSF_MAPNETDRVBUTTON
- SSF_SHOWINFOTIP
- SSF_HIDEICONS
- SSF_NOCONFIRMRECYCLE
- SSF_FILTER
- SSF_WEBVIEW
- SSF_SHOWSUPERHIDDEN
- SSF_SEPPROCESS
- SSF_NONETCRAWLING
- SSF_STARTPANELON
- SSF_SHOWSTARTPAGE
- SSF_AUTOCHECKSELECT
- SSF_ICONSONLY
- SSF_SHOWTYPEOVERLAY
- SSF_SHOWSTATUSBAR
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: c022b1d93cb411f0cce73822a47f2d8f85b30e8093bbe2064fb3c50eab5c4870
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118967944"
---
# <a name="ssf-constants"></a>Constantes de SSF

Usado por la [**función SHGetSetSettings**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetsetsettings) para especificar qué miembros de su [**estructura SHELLSTATE**](/windows/win32/api/shlobj_core/ns-shlobj_core-shellstatea) se deben establecer o volver a derivar.

<dl> <dt>

<span id="SSF_SHOWALLOBJECTS"></span><span id="ssf_showallobjects"></span>**SSF \_ SHOWALLOBJECTS**
</dt> <dd> <dl> <dt>

0x00000001
</dt> <dt>



Se solicita el miembro **fShowAllObjects.**


</dt> </dl> </dd> <dt>

<span id="SSF_SHOWEXTENSIONS"></span><span id="ssf_showextensions"></span>**SHOWEXTENSIONS DE SSF \_**
</dt> <dd> <dl> <dt>

0x00000002
</dt> <dt>



Se **solicita el miembro fShowExtensions.**


</dt> </dl> </dd> <dt>

<span id="SSF_HIDDENFILEEXTS"></span><span id="ssf_hiddenfileexts"></span>**SSF \_ HIDDENFILEEXTS**
</dt> <dd> <dl> <dt>

0x00000004
</dt> <dt>



No se usa.


</dt> </dl> </dd> <dt>

<span id="SSF_SERVERADMINUI"></span><span id="ssf_serveradminui"></span>**SSF \_ SERVERADMINUI**
</dt> <dd> <dl> <dt>

0x00000004
</dt> <dt>



No se usa.


</dt> </dl> </dd> <dt>

<span id="SSF_SHOWCOMPCOLOR"></span><span id="ssf_showcompcolor"></span>**SSF \_ SHOWCOMPCOLOR**
</dt> <dd> <dl> <dt>

0x00000008
</dt> <dt>



Se solicita el miembro **fShowCompColor.**


</dt> </dl> </dd> <dt>

<span id="SSF_SORTCOLUMNS"></span><span id="ssf_sortcolumns"></span>**SORTCOLUMNS de SSF \_**
</dt> <dd> <dl> <dt>

0x00000010
</dt> <dt>



Se solicitan los miembros **lParamSort** **e iSortDirection.**


</dt> </dl> </dd> <dt>

<span id="SSF_SHOWSYSFILES"></span><span id="ssf_showsysfiles"></span>**SHOWSYSFILES DE SSF \_**
</dt> <dd> <dl> <dt>

0x00000020
</dt> <dt>



Se **solicita el miembro fShowSysFiles.**


</dt> </dl> </dd> <dt>

<span id="SSF_DOUBLECLICKINWEBVIEW"></span><span id="ssf_doubleclickinwebview"></span>**SSF \_ DOUBLECLICKINWEBVIEW**
</dt> <dd> <dl> <dt>

0x00000080
</dt> <dt>



Se **solicita el miembro fDoubleClickInWebView.**


</dt> </dl> </dd> <dt>

<span id="SSF_SHOWATTRIBCOL"></span><span id="ssf_showattribcol"></span>**SSF \_ SHOWATTRIBCOL**
</dt> <dd> <dl> <dt>

0x00000100
</dt> <dt>



Se solicita el miembro **fShowAttribCol.**

**Windows Vista:** No se usa.


</dt> </dl> </dd> <dt>

<span id="SSF_DESKTOPHTML"></span><span id="ssf_desktophtml"></span>**SSF \_ DESKTOPHTML**
</dt> <dd> <dl> <dt>

0x00000200
</dt> <dt>



Se solicita el miembro **fDesktopHTML.** El conjunto no está disponible. En su lugar, para las versiones de Windows anteriores a Windows XP, habilite HTML de escritorio de [**IActiveDesktop**](/windows/win32/api/shlobj_core/nn-shlobj_core-iactivedesktop). Sin embargo, el uso de **IActiveDesktop** para este propósito no se recomienda para Windows XP y versiones posteriores de Windows, y está en desuso en Windows Vista.


</dt> </dl> </dd> <dt>

<span id="SSF_WIN95CLASSIC"></span><span id="ssf_win95classic"></span>**SSF \_ WIN95CLASSIC**
</dt> <dd> <dl> <dt>

0x00000400
</dt> <dt>



Se solicita el miembro **fWin95Classic.**


</dt> </dl> </dd> <dt>

<span id="SSF_DONTPRETTYPATH"></span><span id="ssf_dontprettypath"></span>**SSF \_ DONTPRETTYPATH**
</dt> <dd> <dl> <dt>

0x00000800
</dt> <dt>



Se **solicita el miembro fDontPrettyPath.**


</dt> </dl> </dd> <dt>

<span id="SSF_MAPNETDRVBUTTON"></span><span id="ssf_mapnetdrvbutton"></span>**MAPNETDRVBUTTON de SSF \_**
</dt> <dd> <dl> <dt>

0x00001000
</dt> <dt>



Se **solicita el miembro fMapNetDrvBtn.**


</dt> </dl> </dd> <dt>

<span id="SSF_SHOWINFOTIP"></span><span id="ssf_showinfotip"></span>**SSF \_ SHOWINFOTIP**
</dt> <dd> <dl> <dt>

0x00002000
</dt> <dt>



Se solicita el miembro **fShowInfoTip.**


</dt> </dl> </dd> <dt>

<span id="SSF_HIDEICONS"></span><span id="ssf_hideicons"></span>**HIDEICONS de SSF \_**
</dt> <dd> <dl> <dt>

0x00004000
</dt> <dt>



Se solicita el miembro **fHideIcons.**


</dt> </dl> </dd> <dt>

<span id="SSF_NOCONFIRMRECYCLE"></span><span id="ssf_noconfirmrecycle"></span>**SSF \_ NOCONFIRMRECYCLE**
</dt> <dd> <dl> <dt>

0x00008000
</dt> <dt>



Se **solicita el miembro fNoConfirmRecycle.**


</dt> </dl> </dd> <dt>

<span id="SSF_FILTER"></span><span id="ssf_filter"></span>**FILTRO \_ SSF**
</dt> <dd> <dl> <dt>

0x00010000
</dt> <dt>



Se solicita el miembro **fFilter.**

**Windows Vista:** No se usa.


</dt> </dl> </dd> <dt>

<span id="SSF_WEBVIEW"></span><span id="ssf_webview"></span>**SSF \_ WEBVIEW**
</dt> <dd> <dl> <dt>

0x00020000
</dt> <dt>



Se solicita el miembro **fWebView.**


</dt> </dl> </dd> <dt>

<span id="SSF_SHOWSUPERHIDDEN"></span><span id="ssf_showsuperhidden"></span>**SSF \_ SHOWSUPERHIDDEN**
</dt> <dd> <dl> <dt>

0x00040000
</dt> <dt>



Se **solicita el miembro fShowSuperHidden.**


</dt> </dl> </dd> <dt>

<span id="SSF_SEPPROCESS"></span><span id="ssf_sepprocess"></span>**SSF \_ SEPPROCESS**
</dt> <dd> <dl> <dt>

0x00080000
</dt> <dt>



Se **solicita el miembro fSepProcess.**


</dt> </dl> </dd> <dt>

<span id="SSF_NONETCRAWLING"></span><span id="ssf_nonetcrawling"></span>**SSF \_ NONETCRAWLING**
</dt> <dd> <dl> <dt>

0x00100000
</dt> <dt>



**Windows XP y versiones posteriores.** Se solicita el miembro **fNoNetCrawling.**


</dt> </dl> </dd> <dt>

<span id="SSF_STARTPANELON"></span><span id="ssf_startpanelon"></span>**SSF \_ STARTPANELON**
</dt> <dd> <dl> <dt>

0x00200000
</dt> <dt>



**Windows XP y versiones posteriores.** Se solicita el miembro **fStartPanelOn.**


</dt> </dl> </dd> <dt>

<span id="SSF_SHOWSTARTPAGE"></span><span id="ssf_showstartpage"></span>**SSF \_ SHOWSTARTPAGE**
</dt> <dd> <dl> <dt>

0x00400000
</dt> <dt>



No se usa.


</dt> </dl> </dd> <dt>

<span id="SSF_AUTOCHECKSELECT"></span><span id="ssf_autocheckselect"></span>**SSF \_ AUTOCHECKSELECT**
</dt> <dd> <dl> <dt>

0x00800000
</dt> <dt>



**Windows Vista y versiones posteriores.** Se solicita el miembro **fAutoCheckSelect.**


</dt> </dl> </dd> <dt>

<span id="SSF_ICONSONLY"></span><span id="ssf_iconsonly"></span>**ICONOS DE \_ SSFONLY**
</dt> <dd> <dl> <dt>

0x01000000
</dt> <dt>



**Windows Vista y versiones posteriores.** Se solicita el miembro **fIconsOnly.**


</dt> </dl> </dd> <dt>

<span id="SSF_SHOWTYPEOVERLAY"></span><span id="ssf_showtypeoverlay"></span>**SSF \_ SHOWTYPEOVERLAY**
</dt> <dd> <dl> <dt>

0x02000000
</dt> <dt>



**Windows Vista y versiones posteriores.** Se solicita el miembro **fShowTypeOverlay.**


</dt> </dl> </dd> <dt>

<span id="SSF_SHOWSTATUSBAR"></span><span id="ssf_showstatusbar"></span>**SSF \_ SHOWSTATUSBAR**
</dt> <dd> <dl> <dt>

0x04000000
</dt> <dt>



**Windows 8 y versiones posteriores:** se solicita el **miembro fShowStatusBar.**


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Shlobj.h</dt> </dl> |



 

 
