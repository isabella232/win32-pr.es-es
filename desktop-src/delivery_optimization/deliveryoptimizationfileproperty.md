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
# <a name="deliveryoptimizationfileproperty-enumeration"></a>Enumeración DeliveryOptimizationFileProperty

La enumeración DeliveryOptimizationFileProperty especifica el identificador de una propiedad opcional para el archivo DO. Esta enumeración se usa en la interfaz IDeliveryOptimizationFile2 donde se pasa el valor de propiedad de tipo VARIANT.

## <a name="syntax"></a>Sintaxis

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

## <a name="constants"></a>Constantes

<dl> <dt>

DOFilePropertyId_DecryptionInfo
</dt> <dd>

El identificador de propiedad DOFilePropertyId_DecryptionInfo establece la información de descifrado en forma de cadena JSON. DOFilePropertyId_DecryptionInfo es una propiedad de solo escritura de tipo VT_BSTR.

</dd> <dt>

DOFilePropertyId_IntegrityCheckInfo
</dt> <dd>

El identificador de la propiedad DOFilePropertyId_IntegrityCheckInfo establece la ubicación del archivo hash de la pieza (PHF), que se usa para realizar comprobaciones de integridad en tiempo de ejecución en el contenido descargado. DOFilePropertyId_IntegrityCheckInfo es una propiedad de solo escritura de tipo VT_BSTR.

</dd> <dt>

DOFilePropertyId_IntegrityCheckMandatory
</dt> <dd>

El identificador de la propiedad DOFilePropertyId_IntegrityCheckMandatory establece una marca booleana que indica si el uso de PHF es obligatorio. Si es TRUE, la descarga se anulará cuando se haya producido un error en la comprobación de integridad. DOFilePropertyId_IntegrityCheckMandatory es una propiedad de lectura y escritura de tipo VT_BOOL.

</dd> <dt>

DOFilePropertyId_DownloadSinkFilePath
</dt> <dd>

El identificador de la propiedad DOFilePropertyId_DownloadSinkFilePath establece una ubicación completa del sistema de archivos donde debe almacenar las piezas descargadas. DOFilePropertyId_DownloadSinkFilePath es de tipo VT_BSTR.

</dd> <dt>

DOFilePropertyId_DownloadSinkMemoryStream
</dt> <dd>

El identificador de la propiedad DOFilePropertyId_DownloadSinkMemoryStream está en desuso. No debe usarse.

</dd> <dt>

DOFilePropertyId_TotalSizeBytes
</dt> <dd>

El identificador de la propiedad DOFilePropertyId_TotalSizeBytes especifica el tamaño total de la descarga. DOFilePropertyId_TotalSizeBytes es de tipo VT_UI8.
</dd> </dl>

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|-------------------------------|----------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 10, versión 1803 \[\]<br/>      |
| Servidor mínimo compatible<br/> | Windows Server, versión 1709 \[ solo para aplicaciones de escritorio\]<br/>  |
| Encabezado<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>               |
