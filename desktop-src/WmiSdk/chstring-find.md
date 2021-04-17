---
description: El método Find busca en una cadena la primera coincidencia de una subcadena.
audience: developer
ms.assetid: 98a7c5ad-5bc7-4918-b978-45d2b439f250
ms.tgt_platform: multiple
title: 'CHString:: Find (método) (ChString. h)'
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 5996ca5c06e2101fad834ce2e37df31ee435fbb3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105717207"
---
# <a name="chstringfind-methods"></a><span data-ttu-id="c0cc5-103">CHString:: Find (métodos)</span><span class="sxs-lookup"><span data-stu-id="c0cc5-103">CHString::Find methods</span></span>

<span data-ttu-id="c0cc5-104">\[La clase [**CHString**](chstring.md) forma parte del marco de trabajo del proveedor WMI, que ahora se considera en el estado final, y no habrá más desarrollo, mejoras o actualizaciones para problemas no relacionados con la seguridad que afecten a estas bibliotecas.</span><span class="sxs-lookup"><span data-stu-id="c0cc5-104">\[The [**CHString**](chstring.md) class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.</span></span> <span data-ttu-id="c0cc5-105">Las [API de mi](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) deben usarse para todo el desarrollo nuevo.\]</span><span class="sxs-lookup"><span data-stu-id="c0cc5-105">The [MI APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) should be used for all new development.\]</span></span>

<span data-ttu-id="c0cc5-106">El método **Find** busca en una cadena la primera coincidencia de una subcadena.</span><span class="sxs-lookup"><span data-stu-id="c0cc5-106">The **Find** method searches a string for the first match of a substring.</span></span>

### <a name="overload-list"></a><span data-ttu-id="c0cc5-107">Lista de sobrecarga</span><span class="sxs-lookup"><span data-stu-id="c0cc5-107">Overload list</span></span>



| <span data-ttu-id="c0cc5-108">Método</span><span class="sxs-lookup"><span data-stu-id="c0cc5-108">Method</span></span>                                          | <span data-ttu-id="c0cc5-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="c0cc5-109">Description</span></span>                                             |
|:------------------------------------------------|:--------------------------------------------------------|
| <span data-ttu-id="c0cc5-110">[**Buscar (WCHAR)**](/windows/win32/api/chstring/nf-chstring-chstring-find(lpcwstr))</span><span class="sxs-lookup"><span data-stu-id="c0cc5-110">[**Find(WCHAR)**](/windows/win32/api/chstring/nf-chstring-chstring-find(lpcwstr))</span></span>     | <span data-ttu-id="c0cc5-111">Busca el **WSTR** en esta cadena.</span><span class="sxs-lookup"><span data-stu-id="c0cc5-111">Searches for the **WSTR** in this string.</span></span><br/>    |
| <span data-ttu-id="c0cc5-112">[**Buscar (LPCWSTR)**](/windows/win32/api/chstring/nf-chstring-chstring-find(lpcwstr))</span><span class="sxs-lookup"><span data-stu-id="c0cc5-112">[**Find(LPCWSTR)**](/windows/win32/api/chstring/nf-chstring-chstring-find(lpcwstr))</span></span> | <span data-ttu-id="c0cc5-113">Busca el **LPCWSTR** en esta cadena.</span><span class="sxs-lookup"><span data-stu-id="c0cc5-113">Searches for the **LPCWSTR** in this string.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="c0cc5-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c0cc5-114">Requirements</span></span>



| <span data-ttu-id="c0cc5-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="c0cc5-115">Requirement</span></span> | <span data-ttu-id="c0cc5-116">Value</span><span class="sxs-lookup"><span data-stu-id="c0cc5-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c0cc5-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c0cc5-117">Minimum supported client</span></span><br/> | <span data-ttu-id="c0cc5-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c0cc5-118">Windows�Vista</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="c0cc5-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c0cc5-119">Minimum supported server</span></span><br/> | <span data-ttu-id="c0cc5-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c0cc5-120">Windows Server�2008</span></span><br/>                                                                                                                                |
| <span data-ttu-id="c0cc5-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c0cc5-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="c0cc5-122"><dt>ChString. h (incluye FwCommon. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c0cc5-122"><dt>ChString.h (include FwCommon.h)</dt></span></span> </dl>                                                    |
| <span data-ttu-id="c0cc5-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c0cc5-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="c0cc5-124"><dt>FrameDyn. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c0cc5-124"><dt>FrameDyn.lib</dt></span></span> </dl>                                                                       |
| <span data-ttu-id="c0cc5-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c0cc5-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c0cc5-126"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c0cc5-126"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span></span> </dl> |



<span data-ttu-id="c0cc5-127">�</span><span class="sxs-lookup"><span data-stu-id="c0cc5-127">�</span></span>

<span data-ttu-id="c0cc5-128">�</span><span class="sxs-lookup"><span data-stu-id="c0cc5-128">�</span></span>
