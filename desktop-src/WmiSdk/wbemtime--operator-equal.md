---
description: Los operadores de asignación de clase WBEMTime se sobrecargan para facilitar las conversiones entre diversos formatos de tiempo de ejecución de Windows y ANSI C. A continuación se enumeran las diversas firmas sobrecargadas.
audience: developer
ms.assetid: 47978056-d46f-4f8f-99cb-8463b44da7cf
ms.tgt_platform: multiple
title: 'WBEMTime:: Operator = Operators (WbemTime. h)'
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 637cc76e776060a4c36a12a9b26bd09a6c231a08
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361521"
---
# <a name="wbemtimeoperator-operators"></a><span data-ttu-id="3ccd3-104">Operadores WBEMTime:: Operator =</span><span class="sxs-lookup"><span data-stu-id="3ccd3-104">WBEMTime::operator= operators</span></span>

<span data-ttu-id="3ccd3-105">\[La clase [**WBEMTime**](wbemtime.md) forma parte del marco de trabajo del proveedor WMI, que ahora se considera en el estado final, y no habrá más desarrollo, mejoras o actualizaciones para problemas no relacionados con la seguridad que afecten a estas bibliotecas.</span><span class="sxs-lookup"><span data-stu-id="3ccd3-105">\[The [**WBEMTime**](wbemtime.md) class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.</span></span> <span data-ttu-id="3ccd3-106">Las [API de mi](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) deben usarse para todo el desarrollo nuevo.\]</span><span class="sxs-lookup"><span data-stu-id="3ccd3-106">The [MI APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) should be used for all new development.\]</span></span>

<span data-ttu-id="3ccd3-107">Los operadores de asignación de clase [**WBEMTime**](wbemtime.md) se sobrecargan para facilitar las conversiones entre diversos formatos de tiempo de ejecución de Windows y ANSI C.</span><span class="sxs-lookup"><span data-stu-id="3ccd3-107">The [**WBEMTime**](wbemtime.md) class assignment operators are overloaded to facilitate conversions between various Windows and ANSI C run-time time formats.</span></span> <span data-ttu-id="3ccd3-108">A continuación se enumeran las diversas firmas sobrecargadas.</span><span class="sxs-lookup"><span data-stu-id="3ccd3-108">The various overloaded signatures are listed below.</span></span>

### <a name="overload-list"></a><span data-ttu-id="3ccd3-109">Lista de sobrecarga</span><span class="sxs-lookup"><span data-stu-id="3ccd3-109">Overload list</span></span>



| <span data-ttu-id="3ccd3-110">Operator</span><span class="sxs-lookup"><span data-stu-id="3ccd3-110">Operator</span></span>                                                                     | <span data-ttu-id="3ccd3-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="3ccd3-111">Description</span></span>                                                    |
|:-----------------------------------------------------------------------------|:---------------------------------------------------------------|
| <span data-ttu-id="3ccd3-112">[**Operator = (BSTR)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-operator-assign(constbstr))</span><span class="sxs-lookup"><span data-stu-id="3ccd3-112">[**operator=(BSTR)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-operator-assign(constbstr))</span></span>               | <span data-ttu-id="3ccd3-113">Convierte un **BSTR** en el formato **WBEMTime** .</span><span class="sxs-lookup"><span data-stu-id="3ccd3-113">Converts a **BSTR** to **WBEMTime** format.</span></span><br/>         |
| <span data-ttu-id="3ccd3-114">[**Operator = (Time \_ t&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-operator-assign(consttime_t_))</span><span class="sxs-lookup"><span data-stu-id="3ccd3-114">[**operator=(time\_t&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-operator-assign(consttime_t_))</span></span>        | <span data-ttu-id="3ccd3-115">Convierte la **hora \_ t** al formato **WBEMTime** .</span><span class="sxs-lookup"><span data-stu-id="3ccd3-115">Converts **time\_t** to **WBEMTime** format.</span></span><br/>        |
| <span data-ttu-id="3ccd3-116">[**operador = (& FILETIME)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-operator-assign(constfiletime_))</span><span class="sxs-lookup"><span data-stu-id="3ccd3-116">[**operator=(FILETIME&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-operator-assign(constfiletime_))</span></span>     | <span data-ttu-id="3ccd3-117">Convierte **FILETIME** en formato **WBEMTime** .</span><span class="sxs-lookup"><span data-stu-id="3ccd3-117">Converts **FILETIME** to **WBEMTime** format.</span></span><br/>       |
| <span data-ttu-id="3ccd3-118">[**Operator = (struct TM&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-operator-assign(consttm_))</span><span class="sxs-lookup"><span data-stu-id="3ccd3-118">[**operator=(struct tm&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-operator-assign(consttm_))</span></span>   | <span data-ttu-id="3ccd3-119">Convierte una estructura **TM** en el formato **WBEMTime** .</span><span class="sxs-lookup"><span data-stu-id="3ccd3-119">Converts a **tm** structure to **WBEMTime** format.</span></span><br/> |
| <span data-ttu-id="3ccd3-120">[**operador = (& SYSTEMTIME)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-operator-assign(constsystemtime_))</span><span class="sxs-lookup"><span data-stu-id="3ccd3-120">[**operator=(SYSTEMTIME&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-operator-assign(constsystemtime_))</span></span> | <span data-ttu-id="3ccd3-121">Convierte **SYSTEMTIME** en formato **WBEMTime** .</span><span class="sxs-lookup"><span data-stu-id="3ccd3-121">Converts **SYSTEMTIME** to **WBEMTime** format.</span></span><br/>     |



## <a name="requirements"></a><span data-ttu-id="3ccd3-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3ccd3-122">Requirements</span></span>



| <span data-ttu-id="3ccd3-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="3ccd3-123">Requirement</span></span> | <span data-ttu-id="3ccd3-124">Value</span><span class="sxs-lookup"><span data-stu-id="3ccd3-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3ccd3-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3ccd3-125">Minimum supported client</span></span><br/> | <span data-ttu-id="3ccd3-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3ccd3-126">Windows�Vista</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="3ccd3-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3ccd3-127">Minimum supported server</span></span><br/> | <span data-ttu-id="3ccd3-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3ccd3-128">Windows Server�2008</span></span><br/>                                                                                                                                |
| <span data-ttu-id="3ccd3-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3ccd3-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="3ccd3-130"><dt>WbemTime. h</dt></span><span class="sxs-lookup"><span data-stu-id="3ccd3-130"><dt>WbemTime.h</dt></span></span> </dl>                                                                         |
| <span data-ttu-id="3ccd3-131">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3ccd3-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3ccd3-132"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3ccd3-132"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span></span> </dl> |



<span data-ttu-id="3ccd3-133">�</span><span class="sxs-lookup"><span data-stu-id="3ccd3-133">�</span></span>

<span data-ttu-id="3ccd3-134">�</span><span class="sxs-lookup"><span data-stu-id="3ccd3-134">�</span></span>
