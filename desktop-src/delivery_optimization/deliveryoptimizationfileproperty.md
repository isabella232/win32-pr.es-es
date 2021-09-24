---
title: Enumeración DeliveryOptimizationFileProperty (Deliveryoptimization.h)
description: La enumeración DeliveryOptimizationFileProperty especifica el identificador de una propiedad opcional para el Optimización de distribución archivo.
keywords:
- DeliveryOptimizationFileProperty (enumeración)
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
ms.openlocfilehash: 7c670118a66525c2a890a8c1ed96e4eefb5f5c28
ms.sourcegitcommit: 2c13d0f1620f7c089687ef1d97e8c1d22e5d537a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "128520257"
---
# <a name="deliveryoptimizationfileproperty-enumeration"></a>DeliveryOptimizationFileProperty (enumeración)

La enumeración DeliveryOptimizationFileProperty especifica el identificador de una propiedad opcional para el Optimización de distribución archivo. Esta enumeración se usa en la interfaz IDeliveryOptimizationFile2 donde se pasa el valor de propiedad de tipo VARIANT.

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

El DOFilePropertyId_DecryptionInfo de propiedad establece la información de descifrado en forma de cadena JSON. DOFilePropertyId_DecryptionInfo es una propiedad de solo escritura de tipo VT_BSTR.

</dd> <dt>

DOFilePropertyId_IntegrityCheckInfo
</dt> <dd>

El DOFilePropertyId_IntegrityCheckInfo propiedad establece la ubicación del archivo hash por fragmentos (PHF), que usa Optimización de distribución para realizar comprobaciones de integridad en tiempo de ejecución en el contenido descargado. DOFilePropertyId_IntegrityCheckInfo es una propiedad de solo escritura de tipo VT_BSTR.

</dd> <dt>

DOFilePropertyId_IntegrityCheckMandatory
</dt> <dd>

El DOFilePropertyId_IntegrityCheckMandatory de propiedad establece una marca booleana que indica si el uso de PHF es obligatorio. Si es TRUE, la descarga se anulará una vez que se haya fallado la comprobación de integridad. DOFilePropertyId_IntegrityCheckMandatory es una propiedad de lectura y escritura de tipo VT_BOOL.

</dd> <dt>

DOFilePropertyId_DownloadSinkFilePath
</dt> <dd>

El DOFilePropertyId_DownloadSinkFilePath de propiedad establece una ubicación completa del sistema de archivos donde Optimización de distribución almacenar las piezas descargadas. DOFilePropertyId_DownloadSinkFilePath es de tipo VT_BSTR.

</dd> <dt>

DOFilePropertyId_DownloadSinkMemoryStream
</dt> <dd>

El DOFilePropertyId_DownloadSinkMemoryStream de propiedad está en desuso. No debe usarse.

</dd> <dt>

DOFilePropertyId_TotalSizeBytes
</dt> <dd>

El DOFilePropertyId_TotalSizeBytes de propiedad especifica el tamaño total de descarga. DOFilePropertyId_TotalSizeBytes es de tipo VT_UI8.
</dd> </dl>

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|-------------------------------|----------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 10, solo aplicaciones de escritorio de la versión 1803 \[\]<br/>      |
| Servidor mínimo compatible<br/> | Windows Servidor, solo aplicaciones de escritorio de la versión 1709 \[\]<br/>  |
| Encabezado<br/>                   | <dl> <dt>Deliveryoptimization.h</dt> </dl>               |
