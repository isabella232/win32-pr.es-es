---
title: Enumeración DeliveryOptimizationFileProperty (Deliveryoptimization. h)
description: La enumeración DeliveryOptimizationFileProperty especifica el identificador de una propiedad opcional para el archivo DO.
keywords:
- Enumeración DeliveryOptimizationFileProperty
topic_type:
- apiref
api_name:
- DeliveryOptimizationFileProperty
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 01/18/2019
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 238ad815149f7d40dd1902b991608e0a3005eb35
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105714579"
---
# <a name="deliveryoptimizationfileproperty-enumeration"></a><span data-ttu-id="9f348-104">Enumeración DeliveryOptimizationFileProperty</span><span class="sxs-lookup"><span data-stu-id="9f348-104">DeliveryOptimizationFileProperty enumeration</span></span>

<span data-ttu-id="9f348-105">La enumeración DeliveryOptimizationFileProperty especifica el identificador de una propiedad opcional para el archivo DO.</span><span class="sxs-lookup"><span data-stu-id="9f348-105">The DeliveryOptimizationFileProperty enumeration specifies the ID of an optional property for the DO file.</span></span> <span data-ttu-id="9f348-106">Esta enumeración se usa en la interfaz IDeliveryOptimizationFile2 donde se pasa el valor de propiedad de tipo VARIANT.</span><span class="sxs-lookup"><span data-stu-id="9f348-106">This enumeration is used in the IDeliveryOptimizationFile2 interface where the property value of type VARIANT is passed</span></span>

## <a name="syntax"></a><span data-ttu-id="9f348-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9f348-107">Syntax</span></span>

```C++
typedef enum _DeliveryOptimizationFileProperty {  
  DOFilePropertyId_DecryptionInfo,
  DOFilePropertyId_IntegrityCheckInfo,
  DOFilePropertyId_IntegrityCheckMandatory,
  DOFilePropertyId_DownloadSinkInterface,
  DOFilePropertyId_DownloadSinkFilePath,
  DOFilePropertyId_DownloadSinkMemoryStream,
  DOFilePropertyId_TotalSizeBytes
} DOFilePropertyId;
```

## <a name="constants"></a><span data-ttu-id="9f348-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="9f348-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="9f348-109">DOFilePropertyId_DecryptionInfo</span><span class="sxs-lookup"><span data-stu-id="9f348-109">DOFilePropertyId_DecryptionInfo</span></span>
</dt> <dd>

<span data-ttu-id="9f348-110">El identificador de propiedad DOFilePropertyId_DecryptionInfo establece la información de descifrado en forma de cadena JSON.</span><span class="sxs-lookup"><span data-stu-id="9f348-110">The DOFilePropertyId_DecryptionInfo property ID sets decryption information in the form of a JSON string.</span></span> <span data-ttu-id="9f348-111">DOFilePropertyId_DecryptionInfo es una propiedad de solo escritura de tipo VT_BSTR.</span><span class="sxs-lookup"><span data-stu-id="9f348-111">DOFilePropertyId_DecryptionInfo is a Write only property of type VT_BSTR.</span></span>

</dd> <dt>

<span data-ttu-id="9f348-112">DOFilePropertyId_IntegrityCheckInfo</span><span class="sxs-lookup"><span data-stu-id="9f348-112">DOFilePropertyId_IntegrityCheckInfo</span></span>
</dt> <dd>

<span data-ttu-id="9f348-113">El identificador de la propiedad DOFilePropertyId_IntegrityCheckInfo establece la ubicación del archivo hash de la pieza (PHF), que se usa para realizar comprobaciones de integridad en tiempo de ejecución en el contenido descargado.</span><span class="sxs-lookup"><span data-stu-id="9f348-113">The DOFilePropertyId_IntegrityCheckInfo property ID sets the piece hash file (PHF) location, which is used by DO to perform runtime integrity checks on the downloaded content.</span></span> <span data-ttu-id="9f348-114">DOFilePropertyId_IntegrityCheckInfo es una propiedad de solo escritura de tipo VT_BSTR.</span><span class="sxs-lookup"><span data-stu-id="9f348-114">DOFilePropertyId_IntegrityCheckInfo is a Write only property of type VT_BSTR.</span></span>

</dd> <dt>

<span data-ttu-id="9f348-115">DOFilePropertyId_IntegrityCheckMandatory</span><span class="sxs-lookup"><span data-stu-id="9f348-115">DOFilePropertyId_IntegrityCheckMandatory</span></span>
</dt> <dd>

<span data-ttu-id="9f348-116">El identificador de la propiedad DOFilePropertyId_IntegrityCheckMandatory establece una marca booleana que indica si el uso de PHF es obligatorio.</span><span class="sxs-lookup"><span data-stu-id="9f348-116">The DOFilePropertyId_IntegrityCheckMandatory property ID sets a boolean flag indicating whether usage of the PHF is mandatory.</span></span> <span data-ttu-id="9f348-117">Si es TRUE, la descarga se anulará cuando se haya producido un error en la comprobación de integridad.</span><span class="sxs-lookup"><span data-stu-id="9f348-117">If TRUE, the download will be aborted once the integrity check is failed.</span></span> <span data-ttu-id="9f348-118">DOFilePropertyId_IntegrityCheckMandatory es una propiedad de lectura y escritura de tipo VT_BOOL.</span><span class="sxs-lookup"><span data-stu-id="9f348-118">DOFilePropertyId_IntegrityCheckMandatory is a Read/Write property of type VT_BOOL.</span></span>

</dd> <dt>

<span data-ttu-id="9f348-119">DOFilePropertyId_DownloadSinkFilePath</span><span class="sxs-lookup"><span data-stu-id="9f348-119">DOFilePropertyId_DownloadSinkFilePath</span></span>
</dt> <dd>

<span data-ttu-id="9f348-120">El identificador de la propiedad DOFilePropertyId_DownloadSinkFilePath establece una ubicación completa del sistema de archivos donde debe almacenar las piezas descargadas.</span><span class="sxs-lookup"><span data-stu-id="9f348-120">The DOFilePropertyId_DownloadSinkFilePath property ID sets a fully qualified file system location where DO should store the downloaded pieces.</span></span> <span data-ttu-id="9f348-121">DOFilePropertyId_DownloadSinkFilePath es de tipo VT_BSTR.</span><span class="sxs-lookup"><span data-stu-id="9f348-121">DOFilePropertyId_DownloadSinkFilePath is of type VT_BSTR.</span></span>

</dd> <dt>

<span data-ttu-id="9f348-122">DOFilePropertyId_DownloadSinkMemoryStream</span><span class="sxs-lookup"><span data-stu-id="9f348-122">DOFilePropertyId_DownloadSinkMemoryStream</span></span>
</dt> <dd>

<span data-ttu-id="9f348-123">El identificador de la propiedad DOFilePropertyId_DownloadSinkMemoryStream está en desuso.</span><span class="sxs-lookup"><span data-stu-id="9f348-123">The DOFilePropertyId_DownloadSinkMemoryStream property ID is deprecated.</span></span> <span data-ttu-id="9f348-124">No debe usarse.</span><span class="sxs-lookup"><span data-stu-id="9f348-124">Do not use.</span></span>

</dd> <dt>

<span data-ttu-id="9f348-125">DOFilePropertyId_TotalSizeBytes</span><span class="sxs-lookup"><span data-stu-id="9f348-125">DOFilePropertyId_TotalSizeBytes</span></span>
</dt> <dd>

<span data-ttu-id="9f348-126">El identificador de la propiedad DOFilePropertyId_TotalSizeBytes especifica el tamaño total de la descarga.</span><span class="sxs-lookup"><span data-stu-id="9f348-126">The DOFilePropertyId_TotalSizeBytes property ID specifies the total download size.</span></span> <span data-ttu-id="9f348-127">DOFilePropertyId_TotalSizeBytes es de tipo VT_UI8.</span><span class="sxs-lookup"><span data-stu-id="9f348-127">DOFilePropertyId_TotalSizeBytes is of type VT_UI8.</span></span>
</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9f348-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9f348-128">Requirements</span></span>

| <span data-ttu-id="9f348-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="9f348-129">Requirement</span></span> | <span data-ttu-id="9f348-130">Value</span><span class="sxs-lookup"><span data-stu-id="9f348-130">Value</span></span> |
|-------------------------------|----------------------------------------------------------|
| <span data-ttu-id="9f348-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9f348-131">Minimum supported client</span></span><br/> | <span data-ttu-id="9f348-132">Solo aplicaciones de escritorio de Windows 10, versión 1803 \[\]</span><span class="sxs-lookup"><span data-stu-id="9f348-132">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>      |
| <span data-ttu-id="9f348-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9f348-133">Minimum supported server</span></span><br/> | <span data-ttu-id="9f348-134">Windows Server, versión 1709 \[ solo para aplicaciones de escritorio\]</span><span class="sxs-lookup"><span data-stu-id="9f348-134">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>  |
| <span data-ttu-id="9f348-135">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9f348-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="9f348-136"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="9f348-136"><dt>Deliveryoptimization.h</dt></span></span> </dl>               |
