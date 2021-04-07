---
description: 'El método CInstance:: GetWBEMINT64 establece una propiedad de entero de 64 bits.'
audience: developer
ms.assetid: a1789091-ddb6-44f7-bc02-82e7c0209bf9
ms.tgt_platform: multiple
title: 'Métodos CInstance:: SetWBEMINT64 (Instance. h)'
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 3f83e39170125a07f28a25d594ad7203f44750a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002440"
---
# <a name="cinstancesetwbemint64-methods"></a><span data-ttu-id="ed99d-103">CInstance:: SetWBEMINT64 (métodos)</span><span class="sxs-lookup"><span data-stu-id="ed99d-103">CInstance::SetWBEMINT64 methods</span></span>

<span data-ttu-id="ed99d-104">\[La clase [**CInstance**](/windows/win32/api/instance/nl-instance-cinstance) forma parte del marco de trabajo del proveedor WMI, que ahora se considera en el estado final, y no habrá más desarrollo, mejoras o actualizaciones para problemas no relacionados con la seguridad que afecten a estas bibliotecas.</span><span class="sxs-lookup"><span data-stu-id="ed99d-104">\[The [**CInstance**](/windows/win32/api/instance/nl-instance-cinstance) class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.</span></span> <span data-ttu-id="ed99d-105">Las [API de mi](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) deben usarse para todo el desarrollo nuevo.\]</span><span class="sxs-lookup"><span data-stu-id="ed99d-105">The [MI APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) should be used for all new development.\]</span></span>

<span data-ttu-id="ed99d-106">El método [**CInstance:: GetWBEMINT64**](cinstance-getwbemint64.md) establece una propiedad de entero de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="ed99d-106">The [**CInstance::GetWBEMINT64**](cinstance-getwbemint64.md) method sets a 64-bit integer property.</span></span>

### <a name="overload-list"></a><span data-ttu-id="ed99d-107">Lista de sobrecarga</span><span class="sxs-lookup"><span data-stu-id="ed99d-107">Overload list</span></span>



| <span data-ttu-id="ed99d-108">Método</span><span class="sxs-lookup"><span data-stu-id="ed99d-108">Method</span></span>                                                                                               | <span data-ttu-id="ed99d-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="ed99d-109">Description</span></span>                                |
|:-----------------------------------------------------------------------------------------------------|:-------------------------------------------|
| <span data-ttu-id="ed99d-110">[**SetWBEMINT64 (LPCWSTR, const LONGLONG&)**](/windows/win32/api/instance/nf-instance-cinstance-setwbemint64(lpcwstr_constlonglong))</span><span class="sxs-lookup"><span data-stu-id="ed99d-110">[**SetWBEMINT64(LPCWSTR, const LONGLONG&)**](/windows/win32/api/instance/nf-instance-cinstance-setwbemint64(lpcwstr_constlonglong))</span></span>    | <span data-ttu-id="ed99d-111">Establece una propiedad de entero de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="ed99d-111">Sets a 64-bit integer property.</span></span><br/> |
| <span data-ttu-id="ed99d-112">[**SetWBEMINT64 (LPCWSTR, const WBEMINT64&)**](/windows/win32/api/instance/nf-instance-cinstance-setwbemint64(lpcwstr_constulonglong))</span><span class="sxs-lookup"><span data-stu-id="ed99d-112">[**SetWBEMINT64(LPCWSTR, const WBEMINT64&)**](/windows/win32/api/instance/nf-instance-cinstance-setwbemint64(lpcwstr_constulonglong))</span></span> | <span data-ttu-id="ed99d-113">Establece una propiedad de entero de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="ed99d-113">Sets a 64-bit integer property.</span></span><br/> |
| <span data-ttu-id="ed99d-114">[**SetWBEMINT64 (LPCWSTR, const ULONGLONG&)**](/windows/win32/api/instance/nf-instance-cinstance-setwbemint64(lpcwstr_constulonglong))</span><span class="sxs-lookup"><span data-stu-id="ed99d-114">[**SetWBEMINT64(LPCWSTR, const ULONGLONG&)**](/windows/win32/api/instance/nf-instance-cinstance-setwbemint64(lpcwstr_constulonglong))</span></span>  | <span data-ttu-id="ed99d-115">Establece una propiedad de entero de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="ed99d-115">Sets a 64-bit integer property.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="ed99d-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ed99d-116">Requirements</span></span>



| <span data-ttu-id="ed99d-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="ed99d-117">Requirement</span></span> | <span data-ttu-id="ed99d-118">Value</span><span class="sxs-lookup"><span data-stu-id="ed99d-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ed99d-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ed99d-119">Minimum supported client</span></span><br/> | <span data-ttu-id="ed99d-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ed99d-120">Windows�Vista</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="ed99d-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ed99d-121">Minimum supported server</span></span><br/> | <span data-ttu-id="ed99d-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ed99d-122">Windows Server�2008</span></span><br/>                                                                                                                                |
| <span data-ttu-id="ed99d-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ed99d-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="ed99d-124"><dt>Instancia. h (incluir FwCommon. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ed99d-124"><dt>Instance.h (include FwCommon.h)</dt></span></span> </dl>                                                    |
| <span data-ttu-id="ed99d-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ed99d-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="ed99d-126"><dt>FrameDyn. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ed99d-126"><dt>FrameDyn.lib</dt></span></span> </dl>                                                                       |
| <span data-ttu-id="ed99d-127">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ed99d-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ed99d-128"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ed99d-128"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ed99d-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="ed99d-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed99d-130">**CInstance**</span><span class="sxs-lookup"><span data-stu-id="ed99d-130">**CInstance**</span></span>](/windows/win32/api/instance/nl-instance-cinstance)
</dt> </dl>

<span data-ttu-id="ed99d-131">�</span><span class="sxs-lookup"><span data-stu-id="ed99d-131">�</span></span>

<span data-ttu-id="ed99d-132">�</span><span class="sxs-lookup"><span data-stu-id="ed99d-132">�</span></span>
