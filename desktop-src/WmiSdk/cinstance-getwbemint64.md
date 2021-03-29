---
description: 'El método CInstance:: GetWBEMINT64 recupera una propiedad de entero de 64 bits.'
ms.assetid: b51d0c51-3b72-4358-8fc3-d1dbc298b4d9
ms.tgt_platform: multiple
title: 'Métodos CInstance:: GetWBEMINT64 (Instance. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name: ''
api_type:
- DllExport
api_location:
- FrameDynOS.dll
- FrameDyn.dll
ms.openlocfilehash: 3d7b7a9f4091125bd722aea197c1670defb0c21b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104360954"
---
# <a name="cinstancegetwbemint64-methods"></a><span data-ttu-id="3ea24-103">CInstance:: GetWBEMINT64 (métodos)</span><span class="sxs-lookup"><span data-stu-id="3ea24-103">CInstance::GetWBEMINT64 methods</span></span>

<span data-ttu-id="3ea24-104">\[La clase [**CInstance**](/windows/desktop/api/Instance/nl-instance-cinstance) forma parte del marco de trabajo del proveedor WMI, que ahora se considera en el estado final, y no habrá más desarrollo, mejoras o actualizaciones para problemas no relacionados con la seguridad que afecten a estas bibliotecas.</span><span class="sxs-lookup"><span data-stu-id="3ea24-104">\[The [**CInstance**](/windows/desktop/api/Instance/nl-instance-cinstance) class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.</span></span> <span data-ttu-id="3ea24-105">Las [API de mi](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) deben usarse para todo el desarrollo nuevo.\]</span><span class="sxs-lookup"><span data-stu-id="3ea24-105">The [MI APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) should be used for all new development.\]</span></span>

<span data-ttu-id="3ea24-106">El método **CInstance:: GetWBEMINT64** recupera una propiedad de entero de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="3ea24-106">The **CInstance::GetWBEMINT64** method retrieves a 64-bit integer property.</span></span>

### <a name="overload-list"></a><span data-ttu-id="3ea24-107">Lista de sobrecarga</span><span class="sxs-lookup"><span data-stu-id="3ea24-107">Overload list</span></span>



| <span data-ttu-id="3ea24-108">Método</span><span class="sxs-lookup"><span data-stu-id="3ea24-108">Method</span></span>                                                                                   | <span data-ttu-id="3ea24-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="3ea24-109">Description</span></span>                                     |
|:-----------------------------------------------------------------------------------------|:------------------------------------------------|
| <span data-ttu-id="3ea24-110">[**GetWBEMINT64 (LPCWSTR, LONGLONG&)**](/windows/win32/api/instance/nf-instance-cinstance-getwbemint64(lpcwstr_longlong_))</span><span class="sxs-lookup"><span data-stu-id="3ea24-110">[**GetWBEMINT64(LPCWSTR, LONGLONG&)**](/windows/win32/api/instance/nf-instance-cinstance-getwbemint64(lpcwstr_longlong_))</span></span>   | <span data-ttu-id="3ea24-111">Recupera una propiedad de entero de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="3ea24-111">Retrieves a 64-bit integer property.</span></span><br/> |
| <span data-ttu-id="3ea24-112">[**GetWBEMINT64 (LPCWSTR, WBEMINT64&)**](/windows/win32/api/instance/nf-instance-cinstance-getwbemint64(lpcwstr_ulonglong_))</span><span class="sxs-lookup"><span data-stu-id="3ea24-112">[**GetWBEMINT64(LPCWSTR, WBEMINT64&)**](/windows/win32/api/instance/nf-instance-cinstance-getwbemint64(lpcwstr_ulonglong_))</span></span> | <span data-ttu-id="3ea24-113">Recupera una propiedad de entero de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="3ea24-113">Retrieves a 64-bit integer property.</span></span><br/> |
| <span data-ttu-id="3ea24-114">[**GetWBEMINT64 (LPCWSTR, ULONGLONG&)**](/windows/win32/api/instance/nf-instance-cinstance-getwbemint64(lpcwstr_ulonglong_))</span><span class="sxs-lookup"><span data-stu-id="3ea24-114">[**GetWBEMINT64(LPCWSTR, ULONGLONG&)**](/windows/win32/api/instance/nf-instance-cinstance-getwbemint64(lpcwstr_ulonglong_))</span></span> | <span data-ttu-id="3ea24-115">Recupera una propiedad de entero de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="3ea24-115">Retrieves a 64-bit integer property.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="3ea24-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3ea24-116">Requirements</span></span>



| <span data-ttu-id="3ea24-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="3ea24-117">Requirement</span></span> | <span data-ttu-id="3ea24-118">Value</span><span class="sxs-lookup"><span data-stu-id="3ea24-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3ea24-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3ea24-119">Minimum supported client</span></span><br/> | <span data-ttu-id="3ea24-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3ea24-120">Windows Vista</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="3ea24-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3ea24-121">Minimum supported server</span></span><br/> | <span data-ttu-id="3ea24-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3ea24-122">Windows Server 2008</span></span><br/>                                                                                                                                |
| <span data-ttu-id="3ea24-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3ea24-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="3ea24-124"><dt>Instancia. h (incluir FwCommon. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3ea24-124"><dt>Instance.h (include FwCommon.h)</dt></span></span> </dl>                                                    |
| <span data-ttu-id="3ea24-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3ea24-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="3ea24-126"><dt>FrameDyn. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3ea24-126"><dt>FrameDyn.lib</dt></span></span> </dl>                                                                       |
| <span data-ttu-id="3ea24-127">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3ea24-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3ea24-128"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3ea24-128"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3ea24-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="3ea24-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ea24-130">**CInstance**</span><span class="sxs-lookup"><span data-stu-id="3ea24-130">**CInstance**</span></span>](/windows/desktop/api/Instance/nl-instance-cinstance)
</dt> </dl>

 

