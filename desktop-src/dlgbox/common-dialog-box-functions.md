---
title: Funciones comunes de cuadros de diálogo
description: . | Funciones comunes de cuadros de diálogo
ms.assetid: 4a94330b-e0d5-48d7-80f3-86ba6ca1f0f9
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 109f0ca24f319bb27955ba117a8035df3042fb44
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105678757"
---
# <a name="common-dialog-box-functions"></a><span data-ttu-id="d1cd2-104">Funciones comunes de cuadros de diálogo</span><span class="sxs-lookup"><span data-stu-id="d1cd2-104">Common Dialog Box Functions</span></span>

## <a name="in-this-section"></a><span data-ttu-id="d1cd2-105">En esta sección</span><span class="sxs-lookup"><span data-stu-id="d1cd2-105">In this section</span></span>

-   [<span data-ttu-id="d1cd2-106">*CCHookProc*</span><span class="sxs-lookup"><span data-stu-id="d1cd2-106">*CCHookProc*</span></span>](/windows/win32/api/commdlg/nc-commdlg-lpcchookproc)
-   [<span data-ttu-id="d1cd2-107">*CFHookProc*</span><span class="sxs-lookup"><span data-stu-id="d1cd2-107">*CFHookProc*</span></span>](/windows/win32/api/commdlg/nc-commdlg-lpcfhookproc)
-   <span data-ttu-id="d1cd2-108">[**Las choosecolor.**](/previous-versions/windows/desktop/legacy/ms646912(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d1cd2-108">[**ChooseColor**](/previous-versions/windows/desktop/legacy/ms646912(v=vs.85))</span></span>
-   [<span data-ttu-id="d1cd2-109">**ChooseFont**</span><span class="sxs-lookup"><span data-stu-id="d1cd2-109">**ChooseFont**</span></span>](/windows/win32/api/commdlg/ns-commdlg-choosefonta)
-   [<span data-ttu-id="d1cd2-110">**CommDlgExtendedError**</span><span class="sxs-lookup"><span data-stu-id="d1cd2-110">**CommDlgExtendedError**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-commdlgextendederror)
-   [<span data-ttu-id="d1cd2-111">**FindText**</span><span class="sxs-lookup"><span data-stu-id="d1cd2-111">**FindText**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-findtexta)
-   [<span data-ttu-id="d1cd2-112">*FRHookProc*</span><span class="sxs-lookup"><span data-stu-id="d1cd2-112">*FRHookProc*</span></span>](/windows/win32/api/commdlg/nc-commdlg-lpfrhookproc)
-   [<span data-ttu-id="d1cd2-113">**GetFileTitle**</span><span class="sxs-lookup"><span data-stu-id="d1cd2-113">**GetFileTitle**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getfiletitlea)
-   [<span data-ttu-id="d1cd2-114">**GetOpenFileName**</span><span class="sxs-lookup"><span data-stu-id="d1cd2-114">**GetOpenFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
-   [<span data-ttu-id="d1cd2-115">**GetSaveFileName**</span><span class="sxs-lookup"><span data-stu-id="d1cd2-115">**GetSaveFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
-   [<span data-ttu-id="d1cd2-116">*OFNHookProc*</span><span class="sxs-lookup"><span data-stu-id="d1cd2-116">*OFNHookProc*</span></span>](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc)
-   <span data-ttu-id="d1cd2-117">[*OFNHookProcOldStyle*](/previous-versions/windows/desktop/legacy/ms646932(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d1cd2-117">[*OFNHookProcOldStyle*](/previous-versions/windows/desktop/legacy/ms646932(v=vs.85))</span></span>
-   [<span data-ttu-id="d1cd2-118">**PagePaintHook**</span><span class="sxs-lookup"><span data-stu-id="d1cd2-118">**PagePaintHook**</span></span>](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook)
-   <span data-ttu-id="d1cd2-119">[**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d1cd2-119">[**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85))</span></span>
-   [<span data-ttu-id="d1cd2-120">**PageSetupHook**</span><span class="sxs-lookup"><span data-stu-id="d1cd2-120">**PageSetupHook**</span></span>](/windows/win32/api/commdlg/nc-commdlg-lppagesetuphook)
-   <span data-ttu-id="d1cd2-121">[**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d1cd2-121">[**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85))</span></span>
-   <span data-ttu-id="d1cd2-122">[**PrintDlgEx**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d1cd2-122">[**PrintDlgEx**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85))</span></span>
-   [<span data-ttu-id="d1cd2-123">*PrintHookProc*</span><span class="sxs-lookup"><span data-stu-id="d1cd2-123">*PrintHookProc*</span></span>](/windows/win32/api/commdlg/nc-commdlg-lpprinthookproc)
-   [<span data-ttu-id="d1cd2-124">**ReplaceText**</span><span class="sxs-lookup"><span data-stu-id="d1cd2-124">**ReplaceText**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-replacetexta)
-   [<span data-ttu-id="d1cd2-125">*SetupHookProc*</span><span class="sxs-lookup"><span data-stu-id="d1cd2-125">*SetupHookProc*</span></span>](/windows/win32/api/commdlg/nc-commdlg-lpsetuphookproc)

 

 
