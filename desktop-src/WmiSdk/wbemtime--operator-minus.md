---
description: 'Operador de resta de clase WBEMTime (&\# 8211;) se ha sobrecargado a:'
audience: developer
ms.assetid: 0fa51aab-7ea2-4af7-bb12-1646388b0405
ms.tgt_platform: multiple
title: 'Operadores WBEMTime:: Operator-(WbemTime. h)'
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 39256ba9d922ea9d3eef8e442115e840b963ca71
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105717120"
---
# <a name="wbemtimeoperator--operators"></a><span data-ttu-id="ff25f-103">Operadores WBEMTime:: Operator-</span><span class="sxs-lookup"><span data-stu-id="ff25f-103">WBEMTime::operator- operators</span></span>

<span data-ttu-id="ff25f-104">\[La clase [**WBEMTime**](wbemtime.md) forma parte del marco de trabajo del proveedor WMI, que ahora se considera en el estado final, y no habrá más desarrollo, mejoras o actualizaciones para problemas no relacionados con la seguridad que afecten a estas bibliotecas.</span><span class="sxs-lookup"><span data-stu-id="ff25f-104">\[The [**WBEMTime**](wbemtime.md) class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.</span></span> <span data-ttu-id="ff25f-105">Las [API de mi](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) deben usarse para todo el desarrollo nuevo.\]</span><span class="sxs-lookup"><span data-stu-id="ff25f-105">The [MI APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) should be used for all new development.\]</span></span>

<span data-ttu-id="ff25f-106">El operador de resta de clase [**WBEMTime**](wbemtime.md) () se ha sobrecargado a:</span><span class="sxs-lookup"><span data-stu-id="ff25f-106">The [**WBEMTime**](wbemtime.md) class subtraction operator (�) has been overloaded to:</span></span>

-   <span data-ttu-id="ff25f-107">Resta un intervalo de tiempo de la hora de un objeto para generar un nuevo objeto Time que contiene la hora resultante.</span><span class="sxs-lookup"><span data-stu-id="ff25f-107">Subtract a time span from an object's time to produce a new time object that contains the resulting time.</span></span>
-   <span data-ttu-id="ff25f-108">Reste una hora del tiempo del objeto para generar un nuevo objeto de intervalo de tiempo que contiene la diferencia entre las dos horas.</span><span class="sxs-lookup"><span data-stu-id="ff25f-108">Subtract a time from the object's time to produce a new time span object that contains the difference between the two times.</span></span>

### <a name="overload-list"></a><span data-ttu-id="ff25f-109">Lista de sobrecarga</span><span class="sxs-lookup"><span data-stu-id="ff25f-109">Overload list</span></span>



| <span data-ttu-id="ff25f-110">Operator</span><span class="sxs-lookup"><span data-stu-id="ff25f-110">Operator</span></span>                                                                         | <span data-ttu-id="ff25f-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="ff25f-111">Description</span></span>                                                                      |
|:---------------------------------------------------------------------------------|:---------------------------------------------------------------------------------|
| [<span data-ttu-id="ff25f-112">**operador-(WBEMTime&)**</span><span class="sxs-lookup"><span data-stu-id="ff25f-112">**operator-(WBEMTime&)**</span></span>](/windows/win32/api/rrascfg/nf-rrascfg-ieapproviderconfig-initialize)         | <span data-ttu-id="ff25f-113">Resta un **WBEMTime** de un **WBEMTime**.</span><span class="sxs-lookup"><span data-stu-id="ff25f-113">Subtracts a **WBEMTime** from a **WBEMTime**.</span></span><br/>                         |
| <span data-ttu-id="ff25f-114">[**operador-(WBEMTimeSpan&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-operator-sub(constwbemtimespan_))</span><span class="sxs-lookup"><span data-stu-id="ff25f-114">[**operator-(WBEMTimeSpan&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-operator-sub(constwbemtimespan_))</span></span> | <span data-ttu-id="ff25f-115">Resta un [**WBEMTimeSpan**](/windows/win32/api/wbemtime/nl-wbemtime-wbemtimespan) de un **WBEMTime**.</span><span class="sxs-lookup"><span data-stu-id="ff25f-115">Subtracts a [**WBEMTimeSpan**](/windows/win32/api/wbemtime/nl-wbemtime-wbemtimespan) from a **WBEMTime**.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="ff25f-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ff25f-116">Requirements</span></span>



| <span data-ttu-id="ff25f-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="ff25f-117">Requirement</span></span> | <span data-ttu-id="ff25f-118">Value</span><span class="sxs-lookup"><span data-stu-id="ff25f-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ff25f-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ff25f-119">Minimum supported client</span></span><br/> | <span data-ttu-id="ff25f-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ff25f-120">Windows�Vista</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="ff25f-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ff25f-121">Minimum supported server</span></span><br/> | <span data-ttu-id="ff25f-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ff25f-122">Windows Server�2008</span></span><br/>                                                                                                                                |
| <span data-ttu-id="ff25f-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ff25f-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="ff25f-124"><dt>WbemTime. h</dt></span><span class="sxs-lookup"><span data-stu-id="ff25f-124"><dt>WbemTime.h</dt></span></span> </dl>                                                                         |
| <span data-ttu-id="ff25f-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ff25f-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ff25f-126"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ff25f-126"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span></span> </dl> |



<span data-ttu-id="ff25f-127">�</span><span class="sxs-lookup"><span data-stu-id="ff25f-127">�</span></span>

<span data-ttu-id="ff25f-128">�</span><span class="sxs-lookup"><span data-stu-id="ff25f-128">�</span></span>
