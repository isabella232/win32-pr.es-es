---
title: Funciones de recursos (menús y otros recursos)
description: Funciones de recursos (menús y otros recursos)
ms.assetid: dfeaaf01-f947-453e-946e-65ad9ec40958
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd8e550bd42afcb98d2a1d7b1117c6c93d19529c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117533"
---
# <a name="resource-functions-menus-and-other-resources"></a><span data-ttu-id="f1699-103">Funciones de recursos (menús y otros recursos)</span><span class="sxs-lookup"><span data-stu-id="f1699-103">Resource Functions (Menus and Other Resources)</span></span>

## <a name="in-this-section"></a><span data-ttu-id="f1699-104">En esta sección</span><span class="sxs-lookup"><span data-stu-id="f1699-104">In This Section</span></span>

-   [<span data-ttu-id="f1699-105">**BeginUpdateResource**</span><span class="sxs-lookup"><span data-stu-id="f1699-105">**BeginUpdateResource**</span></span>](/windows/desktop/api/Winbase/nf-winbase-beginupdateresourcea)
-   [<span data-ttu-id="f1699-106">**CopyImage**</span><span class="sxs-lookup"><span data-stu-id="f1699-106">**CopyImage**</span></span>](/windows/desktop/api/Winuser/nf-winuser-copyimage)
-   [<span data-ttu-id="f1699-107">**EndUpdateResource**</span><span class="sxs-lookup"><span data-stu-id="f1699-107">**EndUpdateResource**</span></span>](/windows/desktop/api/Winbase/nf-winbase-endupdateresourcea)
-   <span data-ttu-id="f1699-108">[*EnumResLangProc*](/previous-versions/windows/desktop/legacy/ms648033(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f1699-108">[*EnumResLangProc*](/previous-versions/windows/desktop/legacy/ms648033(v=vs.85))</span></span>
-   [<span data-ttu-id="f1699-109">*EnumResNameProc*</span><span class="sxs-lookup"><span data-stu-id="f1699-109">*EnumResNameProc*</span></span>](/windows/win32/api/libloaderapi/nc-libloaderapi-enumresnameproca)
-   [<span data-ttu-id="f1699-110">**EnumResourceLanguages**</span><span class="sxs-lookup"><span data-stu-id="f1699-110">**EnumResourceLanguages**</span></span>](/windows/desktop/api/Winbase/nf-winbase-enumresourcelanguagesa)
-   [<span data-ttu-id="f1699-111">**EnumResourceLanguagesEx**</span><span class="sxs-lookup"><span data-stu-id="f1699-111">**EnumResourceLanguagesEx**</span></span>](/windows/win32/api/libloaderapi/nf-libloaderapi-enumresourcelanguagesexa)
-   [<span data-ttu-id="f1699-112">**EnumResourceNames**</span><span class="sxs-lookup"><span data-stu-id="f1699-112">**EnumResourceNames**</span></span>](/windows/desktop/api/Winbase/nf-winbase-enumresourcenamesa)
-   [<span data-ttu-id="f1699-113">**EnumResourceNamesEx**</span><span class="sxs-lookup"><span data-stu-id="f1699-113">**EnumResourceNamesEx**</span></span>](/windows/win32/api/libloaderapi/nf-libloaderapi-enumresourcenamesexa)
-   [<span data-ttu-id="f1699-114">**EnumResourceTypes**</span><span class="sxs-lookup"><span data-stu-id="f1699-114">**EnumResourceTypes**</span></span>](/windows/desktop/api/Winbase/nf-winbase-enumresourcetypesa)
-   [<span data-ttu-id="f1699-115">**EnumResourceTypesEx**</span><span class="sxs-lookup"><span data-stu-id="f1699-115">**EnumResourceTypesEx**</span></span>](/windows/win32/api/libloaderapi/nf-libloaderapi-enumresourcetypesexa)
-   [<span data-ttu-id="f1699-116">*EnumResTypeProc*</span><span class="sxs-lookup"><span data-stu-id="f1699-116">*EnumResTypeProc*</span></span>](/windows/win32/api/libloaderapi/nc-libloaderapi-enumrestypeproca)
-   [<span data-ttu-id="f1699-117">**FindResource**</span><span class="sxs-lookup"><span data-stu-id="f1699-117">**FindResource**</span></span>](/windows/desktop/api/Winbase/nf-winbase-findresourcea)
-   [<span data-ttu-id="f1699-118">**FindResourceEx**</span><span class="sxs-lookup"><span data-stu-id="f1699-118">**FindResourceEx**</span></span>](/windows/desktop/api/Winbase/nf-winbase-findresourceexa)
-   [<span data-ttu-id="f1699-119">**FreeResource**</span><span class="sxs-lookup"><span data-stu-id="f1699-119">**FreeResource**</span></span>](/windows/win32/api/libloaderapi/nf-libloaderapi-freeresource)
-   [<span data-ttu-id="f1699-120">**LoadImage**</span><span class="sxs-lookup"><span data-stu-id="f1699-120">**LoadImage**</span></span>](/windows/desktop/api/Winuser/nf-winuser-loadimagea)
-   [<span data-ttu-id="f1699-121">**LoadResource**</span><span class="sxs-lookup"><span data-stu-id="f1699-121">**LoadResource**</span></span>](/windows/win32/api/libloaderapi/nf-libloaderapi-loadresource)
-   [<span data-ttu-id="f1699-122">**LockResource**</span><span class="sxs-lookup"><span data-stu-id="f1699-122">**LockResource**</span></span>](/windows/win32/api/libloaderapi/nf-libloaderapi-lockresource)
-   [<span data-ttu-id="f1699-123">**SizeofResource**</span><span class="sxs-lookup"><span data-stu-id="f1699-123">**SizeofResource**</span></span>](/windows/win32/api/libloaderapi/nf-libloaderapi-sizeofresource)
-   [<span data-ttu-id="f1699-124">**UpdateResource**</span><span class="sxs-lookup"><span data-stu-id="f1699-124">**UpdateResource**</span></span>](/windows/desktop/api/Winbase/nf-winbase-updateresourcea)

 

 
