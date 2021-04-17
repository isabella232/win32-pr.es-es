---
description: El constructor de clase WBEMTime facilita las conversiones entre diversos formatos de tiempo de ejecución de Windows y ANSI C.
audience: developer
ms.assetid: 8b0ce221-2186-4aed-a474-00f88cef6350
ms.tgt_platform: multiple
title: 'Constructores WBEMTime:: WBEMTime (WbemTime. h)'
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 778b9af2e732b3d294b0348ff2d2b91b60518d45
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105717117"
---
# <a name="wbemtimewbemtime-constructors"></a><span data-ttu-id="7a42b-103">Constructores WBEMTime:: WBEMTime</span><span class="sxs-lookup"><span data-stu-id="7a42b-103">WBEMTime::WBEMTime constructors</span></span>

<span data-ttu-id="7a42b-104">\[La clase [**WBEMTime**](wbemtime.md) forma parte del marco de trabajo del proveedor WMI, que ahora se considera en el estado final, y no habrá más desarrollo, mejoras o actualizaciones para problemas no relacionados con la seguridad que afecten a estas bibliotecas.</span><span class="sxs-lookup"><span data-stu-id="7a42b-104">\[The [**WBEMTime**](wbemtime.md) class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.</span></span> <span data-ttu-id="7a42b-105">Las [API de mi](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) deben usarse para todo el desarrollo nuevo.\]</span><span class="sxs-lookup"><span data-stu-id="7a42b-105">The [MI APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) should be used for all new development.\]</span></span>

<span data-ttu-id="7a42b-106">El constructor de clase **WBEMTime** facilita las conversiones entre diversos formatos de tiempo de ejecución de Windows y ANSI C.</span><span class="sxs-lookup"><span data-stu-id="7a42b-106">The **WBEMTime** class constructor facilitates conversions between various Windows and ANSI C run-time time formats.</span></span>

### <a name="overload-list"></a><span data-ttu-id="7a42b-107">Lista de sobrecarga</span><span class="sxs-lookup"><span data-stu-id="7a42b-107">Overload list</span></span>



| <span data-ttu-id="7a42b-108">Constructor</span><span class="sxs-lookup"><span data-stu-id="7a42b-108">Constructor</span></span>                                                                 | <span data-ttu-id="7a42b-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="7a42b-109">Description</span></span>                                                               |
|:----------------------------------------------------------------------------|:--------------------------------------------------------------------------|
| <span data-ttu-id="7a42b-110">[**WBEMTime()**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-wbemtime(constbstr))</span><span class="sxs-lookup"><span data-stu-id="7a42b-110">[**WBEMTime()**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-wbemtime(constbstr))</span></span>                                   | <span data-ttu-id="7a42b-111">Crea un objeto de hora no inicializado.</span><span class="sxs-lookup"><span data-stu-id="7a42b-111">Creates an uninitialized time object.</span></span><br/>                          |
| <span data-ttu-id="7a42b-112">[**WBEMTime (BSTR)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-wbemtime(constbstr))</span><span class="sxs-lookup"><span data-stu-id="7a42b-112">[**WBEMTime(BSTR)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-wbemtime(constbstr))</span></span>                           | <span data-ttu-id="7a42b-113">Inicializa el nuevo objeto de hora en el valor del parámetro.</span><span class="sxs-lookup"><span data-stu-id="7a42b-113">Initializes the new time object to the value in the parameter.</span></span><br/> |
| <span data-ttu-id="7a42b-114">[**WBEMTime (const Time \_ t&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-wbemtime(consttime_t_))</span><span class="sxs-lookup"><span data-stu-id="7a42b-114">[**WBEMTime(const time\_t&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-wbemtime(consttime_t_))</span></span>        | <span data-ttu-id="7a42b-115">Inicializa el nuevo objeto de hora en el valor del parámetro.</span><span class="sxs-lookup"><span data-stu-id="7a42b-115">Initializes the new time object to the value in the parameter.</span></span><br/> |
| <span data-ttu-id="7a42b-116">[**WBEMTime (const struct TM)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-wbemtime(consttm_))</span><span class="sxs-lookup"><span data-stu-id="7a42b-116">[**WBEMTime(const struct tm)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-wbemtime(consttm_))</span></span>    | <span data-ttu-id="7a42b-117">Inicializa el nuevo objeto de hora en el valor del parámetro.</span><span class="sxs-lookup"><span data-stu-id="7a42b-117">Initializes the new time object to the value in the parameter.</span></span><br/> |
| <span data-ttu-id="7a42b-118">[**WBEMTime (const FILETIME&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-wbemtime(constfiletime_))</span><span class="sxs-lookup"><span data-stu-id="7a42b-118">[**WBEMTime(const FILETIME&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-wbemtime(constfiletime_))</span></span>     | <span data-ttu-id="7a42b-119">Inicializa el nuevo objeto de hora en el valor del parámetro.</span><span class="sxs-lookup"><span data-stu-id="7a42b-119">Initializes the new time object to the value in the parameter.</span></span><br/> |
| <span data-ttu-id="7a42b-120">[**WBEMTime (const SYSTEMTIME&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-wbemtime(constsystemtime_))</span><span class="sxs-lookup"><span data-stu-id="7a42b-120">[**WBEMTime(const SYSTEMTIME&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-wbemtime(constsystemtime_))</span></span> | <span data-ttu-id="7a42b-121">Inicializa el nuevo objeto de hora en el valor del parámetro.</span><span class="sxs-lookup"><span data-stu-id="7a42b-121">Initializes the new time object to the value in the parameter.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="7a42b-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7a42b-122">Requirements</span></span>



| <span data-ttu-id="7a42b-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="7a42b-123">Requirement</span></span> | <span data-ttu-id="7a42b-124">Value</span><span class="sxs-lookup"><span data-stu-id="7a42b-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7a42b-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7a42b-125">Minimum supported client</span></span><br/> | <span data-ttu-id="7a42b-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7a42b-126">Windows�Vista</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="7a42b-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7a42b-127">Minimum supported server</span></span><br/> | <span data-ttu-id="7a42b-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7a42b-128">Windows Server�2008</span></span><br/>                                                                                                                                |
| <span data-ttu-id="7a42b-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7a42b-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="7a42b-130"><dt>WbemTime. h</dt></span><span class="sxs-lookup"><span data-stu-id="7a42b-130"><dt>WbemTime.h</dt></span></span> </dl>                                                                         |
| <span data-ttu-id="7a42b-131">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="7a42b-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7a42b-132"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7a42b-132"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span></span> </dl> |



<span data-ttu-id="7a42b-133">�</span><span class="sxs-lookup"><span data-stu-id="7a42b-133">�</span></span>

<span data-ttu-id="7a42b-134">�</span><span class="sxs-lookup"><span data-stu-id="7a42b-134">�</span></span>
