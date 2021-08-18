---
title: Macros de vista de árbol
description: Macros de vista de árbol
ms.assetid: ee569a0e-21f3-4d46-ac7d-e152f8b35391
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c63ffb8c7e643daba2cb01d188c3d111179ba6441dde76f9ab0c08b41de703a2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117833086"
---
# <a name="tree-view-macros"></a>Macros de vista de árbol

## <a name="in-this-section"></a>En esta sección

-   [**TreeView \_ CreateDragImage**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_createdragimage)
-   [**TreeView \_ DeleteAllItems**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_deleteallitems)
-   [**TreeView \_ DeleteItem**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_deleteitem)
-   [**TreeView \_ EditLabel**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_editlabel)
-   [**TreeView \_ EndEditLabelNow**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_endeditlabelnow)
-   [**TreeView \_ EnsureVisible**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_ensurevisible)
-   [**TreeView \_ Expand**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_expand)
-   [**TreeView \_ GetBkColor**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getbkcolor)
-   [**TreeView \_ GetCheckState**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getcheckstate)
-   [**TreeView \_ GetChild**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getchild)
-   [**TreeView \_ GetCount**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getcount)
-   [**TreeView \_ GetDropHilight**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getdrophilight)
-   [**TreeView \_ GetEditControl**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_geteditcontrol)
-   [**TreeView \_ GetExtendedStyle**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getextendedstyle)
-   [**TreeView \_ GetFirstVisible**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getfirstvisible)
-   [**TreeView \_ GetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getimagelist)
-   [**TreeView \_ GetIndent**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getindent)
-   [**TreeView \_ GetInsertMarkColor**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getinsertmarkcolor)
-   [**TreeView \_ GetISearchString**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getisearchstring)
-   [**TreeView \_ GetItem**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getitem)
-   [**TreeView \_ GetItemHeight**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getitemheight)
-   [**TreeView \_ GetItemPartRect**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getitempartrect)
-   [**TreeView \_ GetItemRect**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getitemrect)
-   [**TreeView \_ GetItemState**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getitemstate)
-   [**TreeView \_ GetLastVisible**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getlastvisible)
-   [**TreeView \_ GetLineColor**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getlinecolor)
-   [**TreeView \_ GetNextItem**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getnextitem)
-   [**TreeView \_ GetNextSelected**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getnextselected)
-   [**TreeView \_ GetNextSibling**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getnextsibling)
-   [**TreeView \_ GetNextVisible**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getnextvisible)
-   [**TreeView \_ GetParent**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getparent)
-   [**TreeView \_ GetPrevSibling**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getprevsibling)
-   [**TreeView \_ GetPrevVisible**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getprevvisible)
-   [**TreeView \_ GetRoot**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getroot)
-   [**TreeView \_ GetScrollTime**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getscrolltime)
-   [**TreeView \_ GetSelectedCount**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getselectedcount)
-   [**TreeView \_ GetSelection**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getselection)
-   [**TreeView \_ GetTextColor**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_gettextcolor)
-   [**TreeView \_ GetToolTips**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_gettooltips)
-   [**TreeView \_ GetUnicodeFormat**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getunicodeformat)
-   [**TreeView \_ GetVisibleCount**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getvisiblecount)
-   [**TreeView \_ HitTest**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_hittest)
-   [**TreeView \_ InsertItem**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_insertitem)
-   [**TreeView \_ MapAccIDToHTREEITEM**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_mapaccidtohtreeitem)
-   [**TreeView \_ MapHTREEITEMtoAccID**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_maphtreeitemtoaccid)
-   [**TreeView \_ Select**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_select)
-   [**TreeView \_ SelectDropTarget**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_selectdroptarget)
-   [**TreeView \_ SelectItem**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_selectitem)
-   [**TreeView \_ SelectSetFirstVisible**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_selectsetfirstvisible)
-   [**TreeView \_ SetAutoScrollInfo**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setautoscrollinfo)
-   [**TreeView \_ SetBkColor**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setbkcolor)
-   [**TreeView \_ SetBorder**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setborder)
-   [**TreeView \_ SetCheckState**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setcheckstate)
-   [**TreeView \_ SetExtendedStyle**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setextendedstyle)
-   [**TreeView \_ SetHot**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_sethot)
-   [**TreeView \_ SetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setimagelist)
-   [**TreeView \_ SetIndent**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setindent)
-   [**TreeView \_ SetInsertMark**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setinsertmark)
-   [**TreeView \_ SetInsertMarkColor**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setinsertmarkcolor)
-   [**TreeView \_ SetItem**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setitem)
-   [**TreeView \_ SetItemHeight**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setitemheight)
-   [**TreeView \_ SetItemState**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setitemstate)
-   [**TreeView \_ SetLineColor**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setlinecolor)
-   [**TreeView \_ SetScrollTime**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setscrolltime)
-   [**TreeView \_ SetTextColor**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_settextcolor)
-   [**TreeView \_ SetToolTips**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_settooltips)
-   [**TreeView \_ SetUnicodeFormat**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setunicodeformat)
-   [**TreeView \_ ShowInfoTip**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_showinfotip)
-   [**TreeView \_ SortChildren**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_sortchildren)
-   [**TreeView \_ SortChildrenCB**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_sortchildrencb)

 

 




