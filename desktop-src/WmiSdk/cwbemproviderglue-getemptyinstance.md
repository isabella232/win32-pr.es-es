---
description: El método GetEmptyInstance recupera una única instancia sin rellenar de la clase especificada.
audience: developer
ms.assetid: 2873b466-3782-4d63-a777-5b25e3fb7615
ms.tgt_platform: multiple
title: 'Métodos CWbemProviderGlue:: GetEmptyInstance (WbemGlue. h)'
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 853afbf3789969fbfca66d5f9cb40f41eadf7630
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105706168"
---
# <a name="cwbemprovidergluegetemptyinstance-methods"></a><span data-ttu-id="164a3-103">CWbemProviderGlue:: GetEmptyInstance (métodos)</span><span class="sxs-lookup"><span data-stu-id="164a3-103">CWbemProviderGlue::GetEmptyInstance methods</span></span>

<span data-ttu-id="164a3-104">\[La clase [**CWbemProviderGlue**](/windows/win32/api/wbemglue/nl-wbemglue-cwbemproviderglue) forma parte del marco de trabajo del proveedor WMI, que ahora se considera en el estado final, y no habrá más desarrollo, mejoras o actualizaciones para problemas no relacionados con la seguridad que afecten a estas bibliotecas.</span><span class="sxs-lookup"><span data-stu-id="164a3-104">\[The [**CWbemProviderGlue**](/windows/win32/api/wbemglue/nl-wbemglue-cwbemproviderglue) class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.</span></span> <span data-ttu-id="164a3-105">Las [API de mi](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) deben usarse para todo el desarrollo nuevo.\]</span><span class="sxs-lookup"><span data-stu-id="164a3-105">The [MI APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) should be used for all new development.\]</span></span>

<span data-ttu-id="164a3-106">El método **GetEmptyInstance** recupera una única instancia sin rellenar de la clase especificada.</span><span class="sxs-lookup"><span data-stu-id="164a3-106">The **GetEmptyInstance** method retrieves a single unpopulated instance of the specified class.</span></span>

### <a name="overload-list"></a><span data-ttu-id="164a3-107">Lista de sobrecarga</span><span class="sxs-lookup"><span data-stu-id="164a3-107">Overload list</span></span>



| <span data-ttu-id="164a3-108">Método</span><span class="sxs-lookup"><span data-stu-id="164a3-108">Method</span></span>                                                                                                                                            | <span data-ttu-id="164a3-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="164a3-109">Description</span></span>                                                                |
|:--------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------|
| <span data-ttu-id="164a3-110">[**GetEmptyInstance (LPCWSTR, CInstance, LPCWSTR)**](/windows/win32/api/wbemglue/nf-wbemglue-cwbemproviderglue-getemptyinstance(methodcontext_lpcwstr_cinstance_lpcwstr))</span><span class="sxs-lookup"><span data-stu-id="164a3-110">[**GetEmptyInstance(LPCWSTR,CInstance,LPCWSTR)**](/windows/win32/api/wbemglue/nf-wbemglue-cwbemproviderglue-getemptyinstance(methodcontext_lpcwstr_cinstance_lpcwstr))</span></span>                            | <span data-ttu-id="164a3-111">Recupera una única instancia sin rellenar de la clase especificada.</span><span class="sxs-lookup"><span data-stu-id="164a3-111">Retrieves a single unpopulated instance of the specified class.</span></span><br/> |
| <span data-ttu-id="164a3-112">[**GetEmptyInstance (MethodContext, LPCWSTR, CInstance, LPCWSTR)**](/windows/win32/api/wbemglue/nf-wbemglue-cwbemproviderglue-getemptyinstance(methodcontext_lpcwstr_cinstance_lpcwstr))</span><span class="sxs-lookup"><span data-stu-id="164a3-112">[**GetEmptyInstance(MethodContext,LPCWSTR,CInstance,LPCWSTR)**](/windows/win32/api/wbemglue/nf-wbemglue-cwbemproviderglue-getemptyinstance(methodcontext_lpcwstr_cinstance_lpcwstr))</span></span> | <span data-ttu-id="164a3-113">Recupera una única instancia sin rellenar de la clase especificada.</span><span class="sxs-lookup"><span data-stu-id="164a3-113">Retrieves a single unpopulated instance of the specified class.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="164a3-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="164a3-114">Requirements</span></span>



| <span data-ttu-id="164a3-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="164a3-115">Requirement</span></span> | <span data-ttu-id="164a3-116">Value</span><span class="sxs-lookup"><span data-stu-id="164a3-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="164a3-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="164a3-117">Minimum supported client</span></span><br/> | <span data-ttu-id="164a3-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="164a3-118">Windows�Vista</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="164a3-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="164a3-119">Minimum supported server</span></span><br/> | <span data-ttu-id="164a3-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="164a3-120">Windows Server�2008</span></span><br/>                                                                                                                                |
| <span data-ttu-id="164a3-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="164a3-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="164a3-122"><dt>WbemGlue. h (incluye FwCommon. h)</dt></span><span class="sxs-lookup"><span data-stu-id="164a3-122"><dt>WbemGlue.h (include FwCommon.h)</dt></span></span> </dl>                                                    |
| <span data-ttu-id="164a3-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="164a3-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="164a3-124"><dt>FrameDyn. lib</dt></span><span class="sxs-lookup"><span data-stu-id="164a3-124"><dt>FrameDyn.lib</dt></span></span> </dl>                                                                       |
| <span data-ttu-id="164a3-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="164a3-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="164a3-126"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span><span class="sxs-lookup"><span data-stu-id="164a3-126"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span></span> </dl> |



<span data-ttu-id="164a3-127">�</span><span class="sxs-lookup"><span data-stu-id="164a3-127">�</span></span>

<span data-ttu-id="164a3-128">�</span><span class="sxs-lookup"><span data-stu-id="164a3-128">�</span></span>
