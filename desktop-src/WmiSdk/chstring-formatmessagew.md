---
description: El método sobrecargado FormatMessageW da formato a una cadena de mensaje.
audience: developer
ms.assetid: 45780467-d3aa-4927-aa53-60e5ee277c27
ms.tgt_platform: multiple
title: 'Métodos CHString:: FormatMessageW (ChString. h)'
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: a4f6be83c2cec8f3ae02cdbafac8a6c10ab72578
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716209"
---
# <a name="chstringformatmessagew-methods"></a><span data-ttu-id="66bcf-103">CHString:: FormatMessageW (métodos)</span><span class="sxs-lookup"><span data-stu-id="66bcf-103">CHString::FormatMessageW methods</span></span>

<span data-ttu-id="66bcf-104">\[La clase [**CHString**](chstring.md) forma parte del marco de trabajo del proveedor WMI, que ahora se considera en el estado final, y no habrá más desarrollo, mejoras o actualizaciones para problemas no relacionados con la seguridad que afecten a estas bibliotecas.</span><span class="sxs-lookup"><span data-stu-id="66bcf-104">\[The [**CHString**](chstring.md) class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.</span></span> <span data-ttu-id="66bcf-105">Las [API de mi](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) deben usarse para todo el desarrollo nuevo.\]</span><span class="sxs-lookup"><span data-stu-id="66bcf-105">The [MI APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) should be used for all new development.\]</span></span>

<span data-ttu-id="66bcf-106">El método sobrecargado **FormatMessageW** da formato a una cadena de mensaje.</span><span class="sxs-lookup"><span data-stu-id="66bcf-106">The overloaded **FormatMessageW** method formats a message string.</span></span>

### <a name="overload-list"></a><span data-ttu-id="66bcf-107">Lista de sobrecarga</span><span class="sxs-lookup"><span data-stu-id="66bcf-107">Overload list</span></span>



| <span data-ttu-id="66bcf-108">Método</span><span class="sxs-lookup"><span data-stu-id="66bcf-108">Method</span></span>                                                              | <span data-ttu-id="66bcf-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="66bcf-109">Description</span></span>                                                                                     |
|:--------------------------------------------------------------------|:------------------------------------------------------------------------------------------------|
| <span data-ttu-id="66bcf-110">[**FormatMessageW (UINT)**](/previous-versions/windows/desktop/legacy/aa385519(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="66bcf-110">[**FormatMessageW(UINT)**](/previous-versions/windows/desktop/legacy/aa385519(v=vs.85))</span></span>       | <span data-ttu-id="66bcf-111">Da formato a este mensaje de acuerdo con el identificador de recursos especificado por **uint**.</span><span class="sxs-lookup"><span data-stu-id="66bcf-111">Formats this message according to the resource identifier specified by the **UINT**.</span></span><br/> |
| <span data-ttu-id="66bcf-112">[**FormatMessageW (LPCWSTR)**](/windows/win32/api/chstring/nf-chstring-chstring-formatmessagew(lpcwstr_---))</span><span class="sxs-lookup"><span data-stu-id="66bcf-112">[**FormatMessageW(LPCWSTR)**](/windows/win32/api/chstring/nf-chstring-chstring-formatmessagew(lpcwstr_---))</span></span> | <span data-ttu-id="66bcf-113">Da formato a esta cadena de mensaje según el formato especificado por **LPCWSTR**.</span><span class="sxs-lookup"><span data-stu-id="66bcf-113">Formats this message string according to the format specified by the **LPCWSTR**.</span></span><br/>    |



## <a name="requirements"></a><span data-ttu-id="66bcf-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="66bcf-114">Requirements</span></span>



| <span data-ttu-id="66bcf-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="66bcf-115">Requirement</span></span> | <span data-ttu-id="66bcf-116">Value</span><span class="sxs-lookup"><span data-stu-id="66bcf-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="66bcf-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="66bcf-117">Minimum supported client</span></span><br/> | <span data-ttu-id="66bcf-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="66bcf-118">Windows�Vista</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="66bcf-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="66bcf-119">Minimum supported server</span></span><br/> | <span data-ttu-id="66bcf-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="66bcf-120">Windows Server�2008</span></span><br/>                                                                                                                                |
| <span data-ttu-id="66bcf-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="66bcf-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="66bcf-122"><dt>ChString. h (incluye FwCommon. h)</dt></span><span class="sxs-lookup"><span data-stu-id="66bcf-122"><dt>ChString.h (include FwCommon.h)</dt></span></span> </dl>                                                    |
| <span data-ttu-id="66bcf-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="66bcf-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="66bcf-124"><dt>FrameDyn. lib</dt></span><span class="sxs-lookup"><span data-stu-id="66bcf-124"><dt>FrameDyn.lib</dt></span></span> </dl>                                                                       |
| <span data-ttu-id="66bcf-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="66bcf-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="66bcf-126"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span><span class="sxs-lookup"><span data-stu-id="66bcf-126"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span></span> </dl> |



<span data-ttu-id="66bcf-127">�</span><span class="sxs-lookup"><span data-stu-id="66bcf-127">�</span></span>

<span data-ttu-id="66bcf-128">�</span><span class="sxs-lookup"><span data-stu-id="66bcf-128">�</span></span>
