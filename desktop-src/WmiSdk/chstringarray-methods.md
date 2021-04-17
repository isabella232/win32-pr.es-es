---
description: La clase CHStringArray expone los métodos siguientes.
ms.assetid: AFE4306E-6BB1-4F1D-A301-CD5F05385466
ms.tgt_platform: multiple
title: Métodos CHStringArray
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8bfbe2afa9948e14362d05f5f90a2e375a9cffab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716766"
---
# <a name="chstringarray-methods"></a><span data-ttu-id="b658a-103">Métodos CHStringArray</span><span class="sxs-lookup"><span data-stu-id="b658a-103">CHStringArray Methods</span></span>

<span data-ttu-id="b658a-104">\[La clase [**CHStringArray**](/windows/desktop/api/ChStrArr/nl-chstrarr-chstringarray) forma parte del marco de trabajo del proveedor WMI, que ahora se considera en el estado final, y no habrá más desarrollo, mejoras o actualizaciones para problemas no relacionados con la seguridad que afecten a estas bibliotecas.</span><span class="sxs-lookup"><span data-stu-id="b658a-104">\[The [**CHStringArray**](/windows/desktop/api/ChStrArr/nl-chstrarr-chstringarray) class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.</span></span> <span data-ttu-id="b658a-105">Las [API de mi](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) deben usarse para todo el desarrollo nuevo.\]</span><span class="sxs-lookup"><span data-stu-id="b658a-105">The [MI APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) should be used for all new development.\]</span></span>

<span data-ttu-id="b658a-106">La clase [**CHStringArray**](/windows/desktop/api/ChStrArr/nl-chstrarr-chstringarray) expone los métodos siguientes.</span><span class="sxs-lookup"><span data-stu-id="b658a-106">The [**CHStringArray**](/windows/desktop/api/ChStrArr/nl-chstrarr-chstringarray) class exposes the following methods.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="b658a-107">En esta sección</span><span class="sxs-lookup"><span data-stu-id="b658a-107">In this section</span></span>

-   [<span data-ttu-id="b658a-108">**Add (método)**</span><span class="sxs-lookup"><span data-stu-id="b658a-108">**Add method**</span></span>](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-add)
-   [<span data-ttu-id="b658a-109">**Append (método)**</span><span class="sxs-lookup"><span data-stu-id="b658a-109">**Append method**</span></span>](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-append)
-   [<span data-ttu-id="b658a-110">**Método CHStringArray**</span><span class="sxs-lookup"><span data-stu-id="b658a-110">**CHStringArray method**</span></span>](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-chstringarray)
-   [<span data-ttu-id="b658a-111">**Copy (método)**</span><span class="sxs-lookup"><span data-stu-id="b658a-111">**Copy method**</span></span>](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-copy)
-   <span data-ttu-id="b658a-112">[**Método ElementAt**](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-elementat(int))</span><span class="sxs-lookup"><span data-stu-id="b658a-112">[**ElementAt method**](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-elementat(int))</span></span>
-   [<span data-ttu-id="b658a-113">**Método FreeExtra**</span><span class="sxs-lookup"><span data-stu-id="b658a-113">**FreeExtra method**</span></span>](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-freeextra)
-   <span data-ttu-id="b658a-114">[**GetAt (método)**](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-getat(int))</span><span class="sxs-lookup"><span data-stu-id="b658a-114">[**GetAt method**](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-getat(int))</span></span>
-   [<span data-ttu-id="b658a-115">**Método GetData**</span><span class="sxs-lookup"><span data-stu-id="b658a-115">**GetData method**</span></span>](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-getdata)
-   [<span data-ttu-id="b658a-116">**Método se obtiene**</span><span class="sxs-lookup"><span data-stu-id="b658a-116">**GetSize method**</span></span>](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-getsize)
-   [<span data-ttu-id="b658a-117">**Método GetUpperBound**</span><span class="sxs-lookup"><span data-stu-id="b658a-117">**GetUpperBound method**</span></span>](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-getupperbound)
-   <span data-ttu-id="b658a-118">[**Métodos Insertat (**](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-insertat(int_chstringarray))</span><span class="sxs-lookup"><span data-stu-id="b658a-118">[**InsertAt methods**](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-insertat(int_chstringarray))</span></span>
-   <span data-ttu-id="b658a-119">[**CHStringArray:: Operator \[\]**](chstringarray--operator-brackets.md)</span><span class="sxs-lookup"><span data-stu-id="b658a-119">[**CHStringArray::operator \[ \]**](chstringarray--operator-brackets.md)</span></span>
-   [<span data-ttu-id="b658a-120">**método RemoveAll**</span><span class="sxs-lookup"><span data-stu-id="b658a-120">**RemoveAll method**</span></span>](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-removeall)
-   [<span data-ttu-id="b658a-121">**método RemoveAt**</span><span class="sxs-lookup"><span data-stu-id="b658a-121">**RemoveAt method**</span></span>](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-removeat)
-   <span data-ttu-id="b658a-122">[**Método SetAt**](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-setat(int_lpcwstr))</span><span class="sxs-lookup"><span data-stu-id="b658a-122">[**SetAt method**](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-setat(int_lpcwstr))</span></span>
-   [<span data-ttu-id="b658a-123">**Método SetAtGrow**</span><span class="sxs-lookup"><span data-stu-id="b658a-123">**SetAtGrow method**</span></span>](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-setatgrow)
-   [<span data-ttu-id="b658a-124">**SetSize (método)**</span><span class="sxs-lookup"><span data-stu-id="b658a-124">**SetSize method**</span></span>](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-setsize)

 

 
