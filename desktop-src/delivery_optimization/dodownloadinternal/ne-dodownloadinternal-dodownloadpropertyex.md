---
title: Enumeración DODownloadPropertyEx
description: Especifica el identificador de las propiedades extendidas para la operación de descarga.
keywords:
- Enumeración DODownloadPropertyEx, DODownloadPropertyEx
topic_type:
- apiref
api_name:
- DODownloadPropertyEx
api_location:
- deliveryoptimizationdownloadtypes.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/29/2019
ms.openlocfilehash: 5df0f53778d9059ef8767f5b8052940847e36c00
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905316"
---
# <a name="dodownloadpropertyex-enumeration"></a><span data-ttu-id="79acb-104">Enumeración DODownloadPropertyEx</span><span class="sxs-lookup"><span data-stu-id="79acb-104">DODownloadPropertyEx enumeration</span></span>

> [!IMPORTANT]
> <span data-ttu-id="79acb-105">La enumeración **DODownloadPropertyEx** está en desuso.</span><span class="sxs-lookup"><span data-stu-id="79acb-105">The **DODownloadPropertyEx** enumeration is deprecated.</span></span> <span data-ttu-id="79acb-106">En su lugar, use la enumeración [DODownloadProperty](../deliveryoptimizationdownloadtypes/ne-deliveryoptimizationdownloadtypes-dodownloadproperty.md) con [IDODownload:: GetProperty](../do/nf-do-idodownload-getproperty.md) y [IDODownload:: SetProperty](../do/nf-do-idodownload-setproperty.md).</span><span class="sxs-lookup"><span data-stu-id="79acb-106">Instead, use the [DODownloadProperty](../deliveryoptimizationdownloadtypes/ne-deliveryoptimizationdownloadtypes-dodownloadproperty.md) enumeration with [IDODownload::GetProperty](../do/nf-do-idodownload-getproperty.md) and [IDODownload::SetProperty](../do/nf-do-idodownload-setproperty.md).</span></span>

<span data-ttu-id="79acb-107">La enumeración **DODownloadPropertyEx** especifica el identificador de las propiedades extendidas para la operación de descarga.</span><span class="sxs-lookup"><span data-stu-id="79acb-107">The **DODownloadPropertyEx** enumeration specifies the ID of extended properties for the DO download operation.</span></span> <span data-ttu-id="79acb-108">Esta enumeración la usa la interfaz **IDODownloadInternal** y se utiliza un valor **Variant** para obtener y establecer el valor de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="79acb-108">This enumeration is used by the **IDODownloadInternal** interface, and a **VARIANT** value is used to get and set the property value.</span></span>

## <a name="syntax"></a><span data-ttu-id="79acb-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="79acb-109">Syntax</span></span>

```cpp
typedef enum _DODownloadPropertyEx
{
  DODownloadPropertyEx_UpdateId = 0,
  DODownloadPropertyEx_CorrelationVector,
  DODownloadPropertyEx_DecryptionInfo,    
  DODownloadPropertyEx_IntegrityCheckInfo,   
  DODownloadPropertyEx_IntegrityCheckMandatory, 
  DODownloadPropertyEx_TotalSizeBytes, 
  DODownloadPropertyEx_TempLocalFileUsage 
} DODownloadPropertyEx;
```
## <a name="constants"></a><span data-ttu-id="79acb-110">Constantes</span><span class="sxs-lookup"><span data-stu-id="79acb-110">Constants</span></span>

| <span data-ttu-id="79acb-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="79acb-111">Requirement</span></span> | <span data-ttu-id="79acb-112">Value</span><span class="sxs-lookup"><span data-stu-id="79acb-112">Value</span></span> |
|-|-|
| <span data-ttu-id="79acb-113">DODownloadPropertyEx_UpdateId</span><span class="sxs-lookup"><span data-stu-id="79acb-113">DODownloadPropertyEx_UpdateId</span></span> | <span data-ttu-id="79acb-114">Reservado.</span><span class="sxs-lookup"><span data-stu-id="79acb-114">Reserved.</span></span> <span data-ttu-id="79acb-115">No utilizar.</span><span class="sxs-lookup"><span data-stu-id="79acb-115">Do not use.</span></span> |
| <span data-ttu-id="79acb-116">DODownloadPropertyEx_CorrelationVector</span><span class="sxs-lookup"><span data-stu-id="79acb-116">DODownloadPropertyEx_CorrelationVector</span></span> | <span data-ttu-id="79acb-117">Opcional.</span><span class="sxs-lookup"><span data-stu-id="79acb-117">Optional.</span></span> <span data-ttu-id="79acb-118">Establece un vector de correlación específico para fines de telemetría.</span><span class="sxs-lookup"><span data-stu-id="79acb-118">Sets a specific correlation vector for telemetry purposes.</span></span> <span data-ttu-id="79acb-119">El tipo de variante es VT_BSTR.</span><span class="sxs-lookup"><span data-stu-id="79acb-119">VARIANT type is VT_BSTR.</span></span> |
| <span data-ttu-id="79acb-120">DODownloadPropertyEx_DecryptionInfo</span><span class="sxs-lookup"><span data-stu-id="79acb-120">DODownloadPropertyEx_DecryptionInfo</span></span> | <span data-ttu-id="79acb-121">Reservado.</span><span class="sxs-lookup"><span data-stu-id="79acb-121">Reserved.</span></span> <span data-ttu-id="79acb-122">No utilizar.</span><span class="sxs-lookup"><span data-stu-id="79acb-122">Do not use.</span></span> |
| <span data-ttu-id="79acb-123">DODownloadPropertyEx_IntegrityCheckInfo</span><span class="sxs-lookup"><span data-stu-id="79acb-123">DODownloadPropertyEx_IntegrityCheckInfo</span></span> | <span data-ttu-id="79acb-124">Opcional de solo escritura.</span><span class="sxs-lookup"><span data-stu-id="79acb-124">Optional write-only.</span></span> <span data-ttu-id="79acb-125">Establece la ubicación del archivo hash de elemento (PHF), que se usa para realizar comprobaciones de integridad en tiempo de ejecución en el contenido descargado.</span><span class="sxs-lookup"><span data-stu-id="79acb-125">Sets the piece hash file (PHF) location, which is used by DO to perform runtime integrity checks on the downloaded content.</span></span> <span data-ttu-id="79acb-126">El tipo de variante es VT_BSTR.</span><span class="sxs-lookup"><span data-stu-id="79acb-126">VARIANT type is VT_BSTR.</span></span> |
| <span data-ttu-id="79acb-127">DODownloadPropertyEx_IntegrityCheckMandatory</span><span class="sxs-lookup"><span data-stu-id="79acb-127">DODownloadPropertyEx_IntegrityCheckMandatory</span></span> | <span data-ttu-id="79acb-128">Opcional.</span><span class="sxs-lookup"><span data-stu-id="79acb-128">Optional.</span></span> <span data-ttu-id="79acb-129">Establece una marca booleana que indica si el uso del archivo hash de la pieza (PHF) es obligatorio.</span><span class="sxs-lookup"><span data-stu-id="79acb-129">Sets a boolean flag indicating whether usage of the piece hash file (PHF) is mandatory.</span></span> <span data-ttu-id="79acb-130">Si VARIANT_TRUE, la descarga se anulará cuando se haya producido un error en la comprobación de integridad.</span><span class="sxs-lookup"><span data-stu-id="79acb-130">If VARIANT_TRUE, the download will be aborted once the integrity check is failed.</span></span> <span data-ttu-id="79acb-131">El tipo de variante es VT_BOOL.</span><span class="sxs-lookup"><span data-stu-id="79acb-131">VARIANT type is VT_BOOL.</span></span> |
| <span data-ttu-id="79acb-132">DODownloadPropertyEx_TotalSizeBytes</span><span class="sxs-lookup"><span data-stu-id="79acb-132">DODownloadPropertyEx_TotalSizeBytes</span></span> | <span data-ttu-id="79acb-133">Reservado.</span><span class="sxs-lookup"><span data-stu-id="79acb-133">Reserved.</span></span> <span data-ttu-id="79acb-134">No utilizar.</span><span class="sxs-lookup"><span data-stu-id="79acb-134">Do not use.</span></span> |
| <span data-ttu-id="79acb-135">DODownloadPropertyEx_TempLocalFileUsage</span><span class="sxs-lookup"><span data-stu-id="79acb-135">DODownloadPropertyEx_TempLocalFileUsage</span></span> | <span data-ttu-id="79acb-136">Reservado.</span><span class="sxs-lookup"><span data-stu-id="79acb-136">Reserved.</span></span> <span data-ttu-id="79acb-137">No utilizar.</span><span class="sxs-lookup"><span data-stu-id="79acb-137">Do not use.</span></span> |

## <a name="requirements"></a><span data-ttu-id="79acb-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="79acb-138">Requirements</span></span>

| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="79acb-139">**Cliente mínimo compatible**</span><span class="sxs-lookup"><span data-stu-id="79acb-139">**Minimum supported client**</span></span> | <span data-ttu-id="79acb-140">Solo aplicaciones Win32 de Windows 10, versión 1809 \[\]</span><span class="sxs-lookup"><span data-stu-id="79acb-140">Windows 10, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="79acb-141">**Servidor mínimo compatible**</span><span class="sxs-lookup"><span data-stu-id="79acb-141">**Minimum supported server**</span></span> | <span data-ttu-id="79acb-142">Windows Server, versión 1809 \[ Win32 Applications Only\]</span><span class="sxs-lookup"><span data-stu-id="79acb-142">Windows Server, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="79acb-143">**Header**</span><span class="sxs-lookup"><span data-stu-id="79acb-143">**Header**</span></span> | <span data-ttu-id="79acb-144">DODownloadInternal. h</span><span class="sxs-lookup"><span data-stu-id="79acb-144">DODownloadInternal.h</span></span> |
