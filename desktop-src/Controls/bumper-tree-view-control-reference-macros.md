---
title: Macros de la vista de árbol
description: Macros de la vista de árbol
ms.assetid: ee569a0e-21f3-4d46-ac7d-e152f8b35391
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc69c9ebc400975bba1d9e43c820b6a7314981c7
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104280202"
---
# <a name="tree-view-macros"></a><span data-ttu-id="b3aab-103">Macros de la vista de árbol</span><span class="sxs-lookup"><span data-stu-id="b3aab-103">Tree View Macros</span></span>

## <a name="in-this-section"></a><span data-ttu-id="b3aab-104">En esta sección</span><span class="sxs-lookup"><span data-stu-id="b3aab-104">In This Section</span></span>

-   [<span data-ttu-id="b3aab-105">**CreateDragImage de TreeView \_**</span><span class="sxs-lookup"><span data-stu-id="b3aab-105">**TreeView\_CreateDragImage**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_createdragimage)
-   [<span data-ttu-id="b3aab-106">**DeleteAllItems de TreeView \_**</span><span class="sxs-lookup"><span data-stu-id="b3aab-106">**TreeView\_DeleteAllItems**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_deleteallitems)
-   [<span data-ttu-id="b3aab-107">**Vista de árbol \_ DeleteItem**</span><span class="sxs-lookup"><span data-stu-id="b3aab-107">**TreeView\_DeleteItem**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_deleteitem)
-   [<span data-ttu-id="b3aab-108">**EditLabel de TreeView \_**</span><span class="sxs-lookup"><span data-stu-id="b3aab-108">**TreeView\_EditLabel**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_editlabel)
-   [<span data-ttu-id="b3aab-109">**EndEditLabelNow de TreeView \_**</span><span class="sxs-lookup"><span data-stu-id="b3aab-109">**TreeView\_EndEditLabelNow**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_endeditlabelnow)
-   [<span data-ttu-id="b3aab-110">**Vista de árbol \_ ensureVisible**</span><span class="sxs-lookup"><span data-stu-id="b3aab-110">**TreeView\_EnsureVisible**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_ensurevisible)
-   [<span data-ttu-id="b3aab-111">**\_Expandir TreeView**</span><span class="sxs-lookup"><span data-stu-id="b3aab-111">**TreeView\_Expand**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_expand)
-   [<span data-ttu-id="b3aab-112">**GetBkColor de TreeView \_**</span><span class="sxs-lookup"><span data-stu-id="b3aab-112">**TreeView\_GetBkColor**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getbkcolor)
-   [<span data-ttu-id="b3aab-113">**GetCheckState de TreeView \_**</span><span class="sxs-lookup"><span data-stu-id="b3aab-113">**TreeView\_GetCheckState**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getcheckstate)
-   [<span data-ttu-id="b3aab-114">**GetChild de TreeView \_**</span><span class="sxs-lookup"><span data-stu-id="b3aab-114">**TreeView\_GetChild**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getchild)
-   [<span data-ttu-id="b3aab-115">**\_GetCount (getCount)**</span><span class="sxs-lookup"><span data-stu-id="b3aab-115">**TreeView\_GetCount**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getcount)
-   [<span data-ttu-id="b3aab-116">**GetDropHilight de TreeView \_**</span><span class="sxs-lookup"><span data-stu-id="b3aab-116">**TreeView\_GetDropHilight**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getdrophilight)
-   [<span data-ttu-id="b3aab-117">**GetEditControl de TreeView \_**</span><span class="sxs-lookup"><span data-stu-id="b3aab-117">**TreeView\_GetEditControl**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_geteditcontrol)
-   [<span data-ttu-id="b3aab-118">**GetExtendedStyle de TreeView \_**</span><span class="sxs-lookup"><span data-stu-id="b3aab-118">**TreeView\_GetExtendedStyle**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getextendedstyle)
-   [<span data-ttu-id="b3aab-119">**GetFirstVisible de TreeView \_**</span><span class="sxs-lookup"><span data-stu-id="b3aab-119">**TreeView\_GetFirstVisible**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getfirstvisible)
-   [<span data-ttu-id="b3aab-120">**GetImageList de TreeView \_**</span><span class="sxs-lookup"><span data-stu-id="b3aab-120">**TreeView\_GetImageList**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getimagelist)
-   [<span data-ttu-id="b3aab-121">**GetIndent de TreeView \_**</span><span class="sxs-lookup"><span data-stu-id="b3aab-121">**TreeView\_GetIndent**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getindent)
-   [<span data-ttu-id="b3aab-122">**GetInsertMarkColor de TreeView \_**</span><span class="sxs-lookup"><span data-stu-id="b3aab-122">**TreeView\_GetInsertMarkColor**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getinsertmarkcolor)
-   [<span data-ttu-id="b3aab-123">**GetISearchString de TreeView \_**</span><span class="sxs-lookup"><span data-stu-id="b3aab-123">**TreeView\_GetISearchString**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getisearchstring)
-   [<span data-ttu-id="b3aab-124">**GetItem de TreeView \_**</span><span class="sxs-lookup"><span data-stu-id="b3aab-124">**TreeView\_GetItem**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getitem)
-   [<span data-ttu-id="b3aab-125">**GetItemHeight de TreeView \_**</span><span class="sxs-lookup"><span data-stu-id="b3aab-125">**TreeView\_GetItemHeight**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getitemheight)
-   [<span data-ttu-id="b3aab-126">**GetItemPartRect de TreeView \_**</span><span class="sxs-lookup"><span data-stu-id="b3aab-126">**TreeView\_GetItemPartRect**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getitempartrect)
-   [<span data-ttu-id="b3aab-127">**GetItemRect de TreeView \_**</span><span class="sxs-lookup"><span data-stu-id="b3aab-127">**TreeView\_GetItemRect**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getitemrect)
-   [<span data-ttu-id="b3aab-128">**GetItemState de TreeView \_**</span><span class="sxs-lookup"><span data-stu-id="b3aab-128">**TreeView\_GetItemState**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getitemstate)
-   [<span data-ttu-id="b3aab-129">**GetLastVisible de TreeView \_**</span><span class="sxs-lookup"><span data-stu-id="b3aab-129">**TreeView\_GetLastVisible**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getlastvisible)
-   [<span data-ttu-id="b3aab-130">**GetLineColor de TreeView \_**</span><span class="sxs-lookup"><span data-stu-id="b3aab-130">**TreeView\_GetLineColor**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getlinecolor)
-   [<span data-ttu-id="b3aab-131">**GetNextItem de TreeView \_**</span><span class="sxs-lookup"><span data-stu-id="b3aab-131">**TreeView\_GetNextItem**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getnextitem)
-   [<span data-ttu-id="b3aab-132">**GetNextSelected de TreeView \_**</span><span class="sxs-lookup"><span data-stu-id="b3aab-132">**TreeView\_GetNextSelected**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getnextselected)
-   [<span data-ttu-id="b3aab-133">**GetNextSibling de TreeView \_**</span><span class="sxs-lookup"><span data-stu-id="b3aab-133">**TreeView\_GetNextSibling**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getnextsibling)
-   [<span data-ttu-id="b3aab-134">**GetNextVisible de TreeView \_**</span><span class="sxs-lookup"><span data-stu-id="b3aab-134">**TreeView\_GetNextVisible**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getnextvisible)
-   [<span data-ttu-id="b3aab-135">**TreeView \_ GetParent**</span><span class="sxs-lookup"><span data-stu-id="b3aab-135">**TreeView\_GetParent**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getparent)
-   [<span data-ttu-id="b3aab-136">**GetPrevSibling de TreeView \_**</span><span class="sxs-lookup"><span data-stu-id="b3aab-136">**TreeView\_GetPrevSibling**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getprevsibling)
-   [<span data-ttu-id="b3aab-137">**GetPrevVisible de TreeView \_**</span><span class="sxs-lookup"><span data-stu-id="b3aab-137">**TreeView\_GetPrevVisible**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getprevvisible)
-   [<span data-ttu-id="b3aab-138">**GetRoot de TreeView \_**</span><span class="sxs-lookup"><span data-stu-id="b3aab-138">**TreeView\_GetRoot**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getroot)
-   [<span data-ttu-id="b3aab-139">**GetScrollTime de TreeView \_**</span><span class="sxs-lookup"><span data-stu-id="b3aab-139">**TreeView\_GetScrollTime**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getscrolltime)
-   [<span data-ttu-id="b3aab-140">**GetSelectedCount de TreeView \_**</span><span class="sxs-lookup"><span data-stu-id="b3aab-140">**TreeView\_GetSelectedCount**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getselectedcount)
-   [<span data-ttu-id="b3aab-141">**GetSelection de TreeView \_**</span><span class="sxs-lookup"><span data-stu-id="b3aab-141">**TreeView\_GetSelection**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getselection)
-   [<span data-ttu-id="b3aab-142">**GetTextColor de TreeView \_**</span><span class="sxs-lookup"><span data-stu-id="b3aab-142">**TreeView\_GetTextColor**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_gettextcolor)
-   [<span data-ttu-id="b3aab-143">**GetToolTips de TreeView \_**</span><span class="sxs-lookup"><span data-stu-id="b3aab-143">**TreeView\_GetToolTips**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_gettooltips)
-   [<span data-ttu-id="b3aab-144">**GetUnicodeFormat de TreeView \_**</span><span class="sxs-lookup"><span data-stu-id="b3aab-144">**TreeView\_GetUnicodeFormat**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getunicodeformat)
-   [<span data-ttu-id="b3aab-145">**GetVisibleCount de TreeView \_**</span><span class="sxs-lookup"><span data-stu-id="b3aab-145">**TreeView\_GetVisibleCount**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getvisiblecount)
-   [<span data-ttu-id="b3aab-146">**TreeView \_ HitTest**</span><span class="sxs-lookup"><span data-stu-id="b3aab-146">**TreeView\_HitTest**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_hittest)
-   [<span data-ttu-id="b3aab-147">**InsertItem de TreeView \_**</span><span class="sxs-lookup"><span data-stu-id="b3aab-147">**TreeView\_InsertItem**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_insertitem)
-   [<span data-ttu-id="b3aab-148">**MapAccIDToHTREEITEM de TreeView \_**</span><span class="sxs-lookup"><span data-stu-id="b3aab-148">**TreeView\_MapAccIDToHTREEITEM**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_mapaccidtohtreeitem)
-   [<span data-ttu-id="b3aab-149">**MapHTREEITEMtoAccID de TreeView \_**</span><span class="sxs-lookup"><span data-stu-id="b3aab-149">**TreeView\_MapHTREEITEMtoAccID**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_maphtreeitemtoaccid)
-   [<span data-ttu-id="b3aab-150">**\_Seleccionar TreeView**</span><span class="sxs-lookup"><span data-stu-id="b3aab-150">**TreeView\_Select**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_select)
-   [<span data-ttu-id="b3aab-151">**SelectDropTarget de TreeView \_**</span><span class="sxs-lookup"><span data-stu-id="b3aab-151">**TreeView\_SelectDropTarget**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_selectdroptarget)
-   [<span data-ttu-id="b3aab-152">**SelectItem de TreeView \_**</span><span class="sxs-lookup"><span data-stu-id="b3aab-152">**TreeView\_SelectItem**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_selectitem)
-   [<span data-ttu-id="b3aab-153">**SelectSetFirstVisible de TreeView \_**</span><span class="sxs-lookup"><span data-stu-id="b3aab-153">**TreeView\_SelectSetFirstVisible**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_selectsetfirstvisible)
-   [<span data-ttu-id="b3aab-154">**SetAutoScrollInfo de TreeView \_**</span><span class="sxs-lookup"><span data-stu-id="b3aab-154">**TreeView\_SetAutoScrollInfo**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setautoscrollinfo)
-   [<span data-ttu-id="b3aab-155">**SetBkColor de TreeView \_**</span><span class="sxs-lookup"><span data-stu-id="b3aab-155">**TreeView\_SetBkColor**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setbkcolor)
-   [<span data-ttu-id="b3aab-156">**SetBorder de TreeView \_**</span><span class="sxs-lookup"><span data-stu-id="b3aab-156">**TreeView\_SetBorder**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setborder)
-   [<span data-ttu-id="b3aab-157">**SetCheckState de TreeView \_**</span><span class="sxs-lookup"><span data-stu-id="b3aab-157">**TreeView\_SetCheckState**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setcheckstate)
-   [<span data-ttu-id="b3aab-158">**SetExtendedStyle de TreeView \_**</span><span class="sxs-lookup"><span data-stu-id="b3aab-158">**TreeView\_SetExtendedStyle**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setextendedstyle)
-   [<span data-ttu-id="b3aab-159">**Vista de árbol \_ SetHot**</span><span class="sxs-lookup"><span data-stu-id="b3aab-159">**TreeView\_SetHot**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_sethot)
-   [<span data-ttu-id="b3aab-160">**SetImageList de TreeView \_**</span><span class="sxs-lookup"><span data-stu-id="b3aab-160">**TreeView\_SetImageList**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setimagelist)
-   [<span data-ttu-id="b3aab-161">**SetIndent de TreeView \_**</span><span class="sxs-lookup"><span data-stu-id="b3aab-161">**TreeView\_SetIndent**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setindent)
-   [<span data-ttu-id="b3aab-162">**SetInsertMark de TreeView \_**</span><span class="sxs-lookup"><span data-stu-id="b3aab-162">**TreeView\_SetInsertMark**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setinsertmark)
-   [<span data-ttu-id="b3aab-163">**SetInsertMarkColor de TreeView \_**</span><span class="sxs-lookup"><span data-stu-id="b3aab-163">**TreeView\_SetInsertMarkColor**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setinsertmarkcolor)
-   [<span data-ttu-id="b3aab-164">**SetItem de TreeView \_**</span><span class="sxs-lookup"><span data-stu-id="b3aab-164">**TreeView\_SetItem**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setitem)
-   [<span data-ttu-id="b3aab-165">**SetItemHeight de TreeView \_**</span><span class="sxs-lookup"><span data-stu-id="b3aab-165">**TreeView\_SetItemHeight**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setitemheight)
-   [<span data-ttu-id="b3aab-166">**SetItemState de TreeView \_**</span><span class="sxs-lookup"><span data-stu-id="b3aab-166">**TreeView\_SetItemState**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setitemstate)
-   [<span data-ttu-id="b3aab-167">**SetLineColor de TreeView \_**</span><span class="sxs-lookup"><span data-stu-id="b3aab-167">**TreeView\_SetLineColor**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setlinecolor)
-   [<span data-ttu-id="b3aab-168">**SetScrollTime de TreeView \_**</span><span class="sxs-lookup"><span data-stu-id="b3aab-168">**TreeView\_SetScrollTime**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setscrolltime)
-   [<span data-ttu-id="b3aab-169">**SetTextColor de TreeView \_**</span><span class="sxs-lookup"><span data-stu-id="b3aab-169">**TreeView\_SetTextColor**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_settextcolor)
-   [<span data-ttu-id="b3aab-170">**SetToolTips de TreeView \_**</span><span class="sxs-lookup"><span data-stu-id="b3aab-170">**TreeView\_SetToolTips**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_settooltips)
-   [<span data-ttu-id="b3aab-171">**SetUnicodeFormat de TreeView \_**</span><span class="sxs-lookup"><span data-stu-id="b3aab-171">**TreeView\_SetUnicodeFormat**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setunicodeformat)
-   [<span data-ttu-id="b3aab-172">**ShowInfoTip de TreeView \_**</span><span class="sxs-lookup"><span data-stu-id="b3aab-172">**TreeView\_ShowInfoTip**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_showinfotip)
-   [<span data-ttu-id="b3aab-173">**SortChildren de TreeView \_**</span><span class="sxs-lookup"><span data-stu-id="b3aab-173">**TreeView\_SortChildren**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_sortchildren)
-   [<span data-ttu-id="b3aab-174">**SortChildrenCB de TreeView \_**</span><span class="sxs-lookup"><span data-stu-id="b3aab-174">**TreeView\_SortChildrenCB**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_sortchildrencb)

 

 




