---
description: 'El método CInstance:: SetCHString establece una propiedad de cadena.'
ms.assetid: a75b574d-9ee7-4930-a003-5d71c5f1d687
ms.tgt_platform: multiple
title: 'Métodos CInstance:: SetCHString (Instance. h)'
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
ms.openlocfilehash: 187c07b5cf0f867ee838f2f3725d6a82319d4634
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105659927"
---
# <a name="cinstancesetchstring-methods"></a><span data-ttu-id="9e615-103">CInstance:: SetCHString (métodos)</span><span class="sxs-lookup"><span data-stu-id="9e615-103">CInstance::SetCHString methods</span></span>

<span data-ttu-id="9e615-104">\[La clase [**CInstance**](/windows/desktop/api/Instance/nl-instance-cinstance) forma parte del marco de trabajo del proveedor WMI, que ahora se considera en el estado final, y no habrá más desarrollo, mejoras o actualizaciones para problemas no relacionados con la seguridad que afecten a estas bibliotecas.</span><span class="sxs-lookup"><span data-stu-id="9e615-104">\[The [**CInstance**](/windows/desktop/api/Instance/nl-instance-cinstance) class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.</span></span> <span data-ttu-id="9e615-105">Las [API de mi](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) deben usarse para todo el desarrollo nuevo.\]</span><span class="sxs-lookup"><span data-stu-id="9e615-105">The [MI APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) should be used for all new development.\]</span></span>

<span data-ttu-id="9e615-106">El método **CInstance:: SetCHString** establece una propiedad de cadena.</span><span class="sxs-lookup"><span data-stu-id="9e615-106">The **CInstance::SetCHString** method sets a string property.</span></span>

### <a name="overload-list"></a><span data-ttu-id="9e615-107">Lista de sobrecarga</span><span class="sxs-lookup"><span data-stu-id="9e615-107">Overload list</span></span>



| <span data-ttu-id="9e615-108">Método</span><span class="sxs-lookup"><span data-stu-id="9e615-108">Method</span></span>                                                                                           | <span data-ttu-id="9e615-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="9e615-109">Description</span></span>                        |
|:-------------------------------------------------------------------------------------------------|:-----------------------------------|
| <span data-ttu-id="9e615-110">[**SetCHString (LPCWSTR, LPCSTR)**](/windows/desktop/api/Instance/nf-instance-cinstance-setchstring(lpcwstr_lpcstr))</span><span class="sxs-lookup"><span data-stu-id="9e615-110">[**SetCHString(LPCWSTR, LPCSTR)**](/windows/desktop/api/Instance/nf-instance-cinstance-setchstring(lpcwstr_lpcstr))</span></span>                   | <span data-ttu-id="9e615-111">Establece una propiedad de cadena.</span><span class="sxs-lookup"><span data-stu-id="9e615-111">Sets a string property.</span></span><br/> |
| <span data-ttu-id="9e615-112">[**SetCHString (LPCWSTR, const CHString&)**](/windows/win32/api/instance/nf-instance-cinstance-setchstring(lpcwstr_constchstring_))</span><span class="sxs-lookup"><span data-stu-id="9e615-112">[**SetCHString(LPCWSTR, const CHString&)**](/windows/win32/api/instance/nf-instance-cinstance-setchstring(lpcwstr_constchstring_))</span></span> | <span data-ttu-id="9e615-113">Establece una propiedad de cadena.</span><span class="sxs-lookup"><span data-stu-id="9e615-113">Sets a string property.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="9e615-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9e615-114">Requirements</span></span>



| <span data-ttu-id="9e615-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="9e615-115">Requirement</span></span> | <span data-ttu-id="9e615-116">Value</span><span class="sxs-lookup"><span data-stu-id="9e615-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9e615-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9e615-117">Minimum supported client</span></span><br/> | <span data-ttu-id="9e615-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9e615-118">Windows Vista</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="9e615-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9e615-119">Minimum supported server</span></span><br/> | <span data-ttu-id="9e615-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9e615-120">Windows Server 2008</span></span><br/>                                                                                                                                |
| <span data-ttu-id="9e615-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9e615-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="9e615-122"><dt>Instancia. h (incluir FwCommon. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9e615-122"><dt>Instance.h (include FwCommon.h)</dt></span></span> </dl>                                                    |
| <span data-ttu-id="9e615-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9e615-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="9e615-124"><dt>FrameDyn. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9e615-124"><dt>FrameDyn.lib</dt></span></span> </dl>                                                                       |
| <span data-ttu-id="9e615-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="9e615-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9e615-126"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9e615-126"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9e615-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="9e615-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e615-128">**CInstance**</span><span class="sxs-lookup"><span data-stu-id="9e615-128">**CInstance**</span></span>](/windows/desktop/api/Instance/nl-instance-cinstance)
</dt> </dl>

 

