---
description: El método Format da formato y almacena una serie de caracteres y valores en una cadena CHString.
audience: developer
ms.assetid: 95d24b0e-3580-4a5d-8dad-50d44ef1ca39
ms.tgt_platform: multiple
title: 'Métodos CHString:: Format (ChString. h)'
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 7187d2c691c6efb2054d766ae432c55be893cd05
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716208"
---
# <a name="chstringformat-methods"></a><span data-ttu-id="bc8c3-103">CHString:: Format (métodos)</span><span class="sxs-lookup"><span data-stu-id="bc8c3-103">CHString::Format methods</span></span>

<span data-ttu-id="bc8c3-104">\[La clase [**CHString**](chstring.md) forma parte del marco de trabajo del proveedor WMI, que ahora se considera en el estado final, y no habrá más desarrollo, mejoras o actualizaciones para problemas no relacionados con la seguridad que afecten a estas bibliotecas.</span><span class="sxs-lookup"><span data-stu-id="bc8c3-104">\[The [**CHString**](chstring.md) class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.</span></span> <span data-ttu-id="bc8c3-105">Las [API de mi](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) deben usarse para todo el desarrollo nuevo.\]</span><span class="sxs-lookup"><span data-stu-id="bc8c3-105">The [MI APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) should be used for all new development.\]</span></span>

<span data-ttu-id="bc8c3-106">El método **Format** da formato y almacena una serie de caracteres y valores en una cadena [**CHString**](chstring.md) .</span><span class="sxs-lookup"><span data-stu-id="bc8c3-106">The **Format** method formats and stores a series of characters and values in a [**CHString**](chstring.md) string.</span></span>

### <a name="overload-list"></a><span data-ttu-id="bc8c3-107">Lista de sobrecarga</span><span class="sxs-lookup"><span data-stu-id="bc8c3-107">Overload list</span></span>



| <span data-ttu-id="bc8c3-108">Método</span><span class="sxs-lookup"><span data-stu-id="bc8c3-108">Method</span></span>                                              | <span data-ttu-id="bc8c3-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="bc8c3-109">Description</span></span>                                                                                      |
|:----------------------------------------------------|:-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bc8c3-110">[**Formato (UINT)**](/previous-versions/windows/desktop/legacy/aa385532(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="bc8c3-110">[**Format(UINT)**](/previous-versions/windows/desktop/legacy/aa385532(v=vs.85))</span></span>       | <span data-ttu-id="bc8c3-111">Da formato a este CHString según el identificador de recursos especificado por **uint**.</span><span class="sxs-lookup"><span data-stu-id="bc8c3-111">Formats this CHString according to the resource identifier specified by the **UINT**.</span></span><br/> |
| <span data-ttu-id="bc8c3-112">[**Formato (LPCWSTR)**](/windows/win32/api/chstring/nf-chstring-chstring-format(lpcwstr_---))</span><span class="sxs-lookup"><span data-stu-id="bc8c3-112">[**Format(LPCWSTR)**](/windows/win32/api/chstring/nf-chstring-chstring-format(lpcwstr_---))</span></span> | <span data-ttu-id="bc8c3-113">Da formato a este CHString según el formato especificado por **LPCWSTR**.</span><span class="sxs-lookup"><span data-stu-id="bc8c3-113">Formats this CHString according to the format specified by the **LPCWSTR**.</span></span><br/>           |



## <a name="requirements"></a><span data-ttu-id="bc8c3-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bc8c3-114">Requirements</span></span>



| <span data-ttu-id="bc8c3-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="bc8c3-115">Requirement</span></span> | <span data-ttu-id="bc8c3-116">Value</span><span class="sxs-lookup"><span data-stu-id="bc8c3-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bc8c3-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bc8c3-117">Minimum supported client</span></span><br/> | <span data-ttu-id="bc8c3-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bc8c3-118">Windows�Vista</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="bc8c3-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bc8c3-119">Minimum supported server</span></span><br/> | <span data-ttu-id="bc8c3-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bc8c3-120">Windows Server�2008</span></span><br/>                                                                                                                                |
| <span data-ttu-id="bc8c3-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bc8c3-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="bc8c3-122"><dt>ChString. h (incluye FwCommon. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bc8c3-122"><dt>ChString.h (include FwCommon.h)</dt></span></span> </dl>                                                    |
| <span data-ttu-id="bc8c3-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="bc8c3-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="bc8c3-124"><dt>FrameDyn. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bc8c3-124"><dt>FrameDyn.lib</dt></span></span> </dl>                                                                       |
| <span data-ttu-id="bc8c3-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="bc8c3-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bc8c3-126"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bc8c3-126"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span></span> </dl> |



<span data-ttu-id="bc8c3-127">�</span><span class="sxs-lookup"><span data-stu-id="bc8c3-127">�</span></span>

<span data-ttu-id="bc8c3-128">�</span><span class="sxs-lookup"><span data-stu-id="bc8c3-128">�</span></span>
