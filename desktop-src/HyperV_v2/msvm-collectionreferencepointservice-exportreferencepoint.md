---
description: Exporta una colección de puntos de referencia a un archivo. La colección de puntos de referencia, sus opciones de configuración asociadas y sus valores de recursos asociados se conservarán en el archivo resultante.
ms.assetid: 0ed61ded-b4d6-40c5-98be-e192eb934387
title: Método ExportReferencePoint de la Msvm_CollectionReferencePointService clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionReferencePointService.ExportReferencePoint
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 3084cdecdd9a5c5808884a609b6bd91f4d50b814d64a96c8ea9e7470c9ece728
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119681905"
---
# <a name="exportreferencepoint-method-of-the-msvm_collectionreferencepointservice-class"></a>Método ExportReferencePoint de la clase CollectionReferencePointService de Msvm \_

Exporta una colección de puntos de referencia a un archivo. La colección de puntos de referencia, sus opciones de configuración asociadas y sus valores de recursos asociados se conservarán en el archivo resultante.

## <a name="syntax"></a>Sintaxis


```mof
uint32 ExportReferencePoint(
  [in]  CIM_Collection  REF ReferencePointCollection,
  [in]  string              ExportDirectory,
  [in]  string              ExportSettingData,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ReferencePointCollection* \[ En\]
</dt> <dd>

Referencia a una colección [**CIM \_ que**](cim-collection.md) representa la colección de puntos de referencia que se va a exportar.

</dd> <dt>

*ExportDirectory* \[ En\]
</dt> <dd>

Ruta de acceso completa del directorio al que se va a exportar la colección de puntos de referencia.

</dd> <dt>

*ExportSettingData* \[ En\]
</dt> <dd>

Instancia de [**Msvm \_ CollectionReferencePointExportSettingData**](msvm-collectionreferencepointexportsettingdata.md) que representa la configuración de la operación de exportación.

</dd> <dt>

*Trabajo* \[ out\]
</dt> <dd>

Referencia opcional que se devuelve si la operación se ejecuta de forma asincrónica. Si está presente, la referencia devuelta a una instancia de [**\_ CIM ConcreteJob**](cim-concretejob.md) se puede usar para supervisar el progreso y obtener el resultado del método .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se ejecuta sincrónicamente, devuelve 0 si se ejecuta correctamente. Si este método se ejecuta de forma asincrónica, devuelve 4096 y el parámetro de salida Job se puede usar para realizar un seguimiento del progreso de la operación asincrónica. Cualquier otro valor devuelto indica un error.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 10 solo aplicaciones de escritorio\]<br/>                                                             |
| Servidor mínimo compatible<br/> | Windows Server 2016<br/>                                                                          |
| Espacio de nombres<br/>                | Virtualización \\ raíz \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Msvm \_ CollectionReferencePointService**](msvm-collectionreferencepointservice.md)
</dt> </dl>

 

 




