---
description: Exporta una colección de puntos de referencia a un archivo. La colección de puntos de referencia, sus valores de configuración asociados y su configuración de recursos asociada se conservarán en el archivo resultante.
ms.assetid: 0ed61ded-b4d6-40c5-98be-e192eb934387
title: Método ExportReferencePoint de la clase Msvm_CollectionReferencePointService
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
ms.openlocfilehash: 49517da44cc7955d825792afcc475c56e37fad37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688717"
---
# <a name="exportreferencepoint-method-of-the-msvm_collectionreferencepointservice-class"></a>Método ExportReferencePoint de la \_ clase CollectionReferencePointService de MSVM

Exporta una colección de puntos de referencia a un archivo. La colección de puntos de referencia, sus valores de configuración asociados y su configuración de recursos asociada se conservarán en el archivo resultante.

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

*ReferencePointCollection* \[ de\]
</dt> <dd>

Referencia a una [**\_ colección CIM**](cim-collection.md) que representa la colección de puntos de referencia que se va a exportar.

</dd> <dt>

*ExportDirectory* \[ de\]
</dt> <dd>

Ruta de acceso completa del directorio al que se va a exportar la colección de puntos de referencia.

</dd> <dt>

*ExportSettingData* \[ de\]
</dt> <dd>

Instancia de [**MSVM \_ CollectionReferencePointExportSettingData**](msvm-collectionreferencepointexportsettingdata.md) que representa la configuración de la operación de exportación.

</dd> <dt>

*Trabajo* \[ de enuncia\]
</dt> <dd>

Referencia opcional que se devuelve si la operación se ejecuta de forma asincrónica. Si está presente, la referencia devuelta a una instancia de [**CIM \_ ConcreteJob**](cim-concretejob.md) se puede usar para supervisar el progreso y obtener el resultado del método.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se ejecuta sincrónicamente, devuelve 0 si se realiza correctamente. Si este método se ejecuta de forma asincrónica, devuelve 4096 y el parámetro de salida del trabajo se puede usar para realizar el seguimiento del progreso de la operación asincrónica. Cualquier otro valor devuelto indica un error.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 10 \[\]<br/>                                                             |
| Servidor mínimo compatible<br/> | Windows Server 2016<br/>                                                                          |
| Espacio de nombres<br/>                | \\Virtualización de raíz \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MSVM \_ CollectionReferencePointService**](msvm-collectionreferencepointservice.md)
</dt> </dl>

 

 




