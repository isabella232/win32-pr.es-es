---
description: La clase WBEMTimeSpan expone los métodos siguientes.
ms.assetid: 7D450EE2-C52F-4B78-B6B1-9FD74394C3DE
ms.tgt_platform: multiple
title: Métodos WBEMTimeSpan
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d516f22a7ecd5468d53bda44ce47edbe4504d1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105717115"
---
# <a name="wbemtimespan-methods"></a><span data-ttu-id="7c0ca-103">Métodos WBEMTimeSpan</span><span class="sxs-lookup"><span data-stu-id="7c0ca-103">WBEMTimeSpan Methods</span></span>

<span data-ttu-id="7c0ca-104">\[La clase [**WBEMTimeSpan**](/windows/desktop/api/WbemTime/nl-wbemtime-wbemtimespan) forma parte del marco de trabajo del proveedor WMI, que ahora se considera en el estado final, y no habrá más desarrollo, mejoras o actualizaciones para problemas no relacionados con la seguridad que afecten a estas bibliotecas.</span><span class="sxs-lookup"><span data-stu-id="7c0ca-104">\[The [**WBEMTimeSpan**](/windows/desktop/api/WbemTime/nl-wbemtime-wbemtimespan) class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.</span></span> <span data-ttu-id="7c0ca-105">Las [API de mi](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) deben usarse para todo el desarrollo nuevo.\]</span><span class="sxs-lookup"><span data-stu-id="7c0ca-105">The [MI APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) should be used for all new development.\]</span></span>

<span data-ttu-id="7c0ca-106">La clase [**WBEMTimeSpan**](/windows/desktop/api/WbemTime/nl-wbemtime-wbemtimespan) expone los métodos siguientes.</span><span class="sxs-lookup"><span data-stu-id="7c0ca-106">The [**WBEMTimeSpan**](/windows/desktop/api/WbemTime/nl-wbemtime-wbemtimespan) class exposes the following methods.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="7c0ca-107">En esta sección</span><span class="sxs-lookup"><span data-stu-id="7c0ca-107">In this section</span></span>

-   <span data-ttu-id="7c0ca-108">[**Constructores WbemTimeSpan**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtimespan-wbemtimespan(constbstr))</span><span class="sxs-lookup"><span data-stu-id="7c0ca-108">[**WbemTimeSpan constructors**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtimespan-wbemtimespan(constbstr))</span></span>
-   [<span data-ttu-id="7c0ca-109">**Clear (método)**</span><span class="sxs-lookup"><span data-stu-id="7c0ca-109">**Clear method**</span></span>](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtimespan-clear)
-   [<span data-ttu-id="7c0ca-110">**GetBSTR (método)**</span><span class="sxs-lookup"><span data-stu-id="7c0ca-110">**GetBSTR method**</span></span>](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtimespan-getbstr)
-   [<span data-ttu-id="7c0ca-111">**GetTime (método)**</span><span class="sxs-lookup"><span data-stu-id="7c0ca-111">**GetTime method**</span></span>](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtimespan-gettime)
-   [<span data-ttu-id="7c0ca-112">**Método IsOk**</span><span class="sxs-lookup"><span data-stu-id="7c0ca-112">**IsOk method**</span></span>](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtimespan-isok)
-   <span data-ttu-id="7c0ca-113">[**Operator = (método)**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-operator-assign(constfiletime_))</span><span class="sxs-lookup"><span data-stu-id="7c0ca-113">[**operator= method**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-operator-assign(constfiletime_))</span></span>
-   [<span data-ttu-id="7c0ca-114">**Operator + (método)**</span><span class="sxs-lookup"><span data-stu-id="7c0ca-114">**operator+ method**</span></span>](/windows/win32/api/wbemtime/nf-wbemtime-wbemtimespan-operator-add)
-   [<span data-ttu-id="7c0ca-115">**Operator + = (método)**</span><span class="sxs-lookup"><span data-stu-id="7c0ca-115">**operator+= method**</span></span>](/windows/win32/api/wbemtime/nf-wbemtime-wbemtimespan-operator-add-assign)
-   [<span data-ttu-id="7c0ca-116">**Operator-(método)**</span><span class="sxs-lookup"><span data-stu-id="7c0ca-116">**operator- method**</span></span>](/windows/win32/api/wbemtime/nf-wbemtime-wbemtimespan-operator-sub)
-   [<span data-ttu-id="7c0ca-117">**Operator-= (método)**</span><span class="sxs-lookup"><span data-stu-id="7c0ca-117">**operator-= method**</span></span>](/windows/win32/api/wbemtime/nf-wbemtime-wbemtimespan-operator-sub-assign)
-   [<span data-ttu-id="7c0ca-118">**Operator = = (método)**</span><span class="sxs-lookup"><span data-stu-id="7c0ca-118">**operator == method**</span></span>](/windows/win32/api/wbemtime/nf-wbemtime-wbemtimespan-operator-equal-equal-to)
-   [<span data-ttu-id="7c0ca-119">**Operator! = (método)**</span><span class="sxs-lookup"><span data-stu-id="7c0ca-119">**operator != method**</span></span>](/windows/win32/api/wbemtime/nf-wbemtime-wbemtimespan-operator-not-equal-to)
-   [<span data-ttu-id="7c0ca-120">**Operator > método**</span><span class="sxs-lookup"><span data-stu-id="7c0ca-120">**operator > method**</span></span>](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-operator-greater-than)
-   [<span data-ttu-id="7c0ca-121">**Operator >= método**</span><span class="sxs-lookup"><span data-stu-id="7c0ca-121">**operator >= method**</span></span>](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-operator-greater-than-equal-to)
-   [<span data-ttu-id="7c0ca-122">**Operator < método**</span><span class="sxs-lookup"><span data-stu-id="7c0ca-122">**operator < method**</span></span>](/windows/win32/api/wbemtime/nf-wbemtime-wbemtimespan-operator-less-than)
-   [<span data-ttu-id="7c0ca-123">**Operator <= método**</span><span class="sxs-lookup"><span data-stu-id="7c0ca-123">**operator <= method**</span></span>](/windows/win32/api/wbemtime/nf-wbemtime-wbemtimespan-operator-less-than-equal-to)

 

 
