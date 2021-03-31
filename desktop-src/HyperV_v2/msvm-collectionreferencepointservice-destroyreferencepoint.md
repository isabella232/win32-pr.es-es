---
description: Destruye una colección de puntos de referencia existente. Este método puede ser un efecto secundario de la destrucción de otros puntos de referencia que dependen de la colección de puntos de referencia afectados.
ms.assetid: 72c116f4-f844-494c-96ea-e97c49a2af7e
title: Método DestroyReferencePoint de la clase Msvm_CollectionReferencePointService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionReferencePointService.DestroyReferencePoint
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: d7fb3fd9168778854518022744f1a0c5ba3c5f79
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104156861"
---
# <a name="destroyreferencepoint-method-of-the-msvm_collectionreferencepointservice-class"></a>Método DestroyReferencePoint de la \_ clase CollectionReferencePointService de MSVM

Destruye una colección de puntos de referencia existente. Este método puede ser un efecto secundario de la destrucción de otros puntos de referencia que dependen de la colección de puntos de referencia afectados.

## <a name="syntax"></a>Sintaxis


```mof
uint32 DestroyReferencePoint(
  [in]  CIM_Collection  REF AffectedReferencePointCollection,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*AffectedReferencePointCollection* \[ de\]
</dt> <dd>

Referencia a la colección de puntos de referencia del sistema virtual afectada.

</dd> <dt>

*Trabajo* \[ de enuncia\]
</dt> <dd>

Si la operación es de larga ejecución, opcionalmente se puede devolver un trabajo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si se realiza correctamente, devuelve 0 (sin errores) o 4096 (se inició el trabajo). de lo contrario, devuelve un error.

<dl> <dt>

**Completado sin error** (0)
</dt> <dt>

**No compatible** (1)
</dt> <dt>

**Error** (2)
</dt> <dt>

**Tiempo de espera** (3)
</dt> <dt>

**Parámetro no válido** (4)
</dt> <dt>

**Estado no válido** (5)
</dt> <dt>

**Tipo no válido** (6)
</dt> <dt>

**DMTF reservado** (..)
</dt> <dt>

**Parámetros de método comprobados: trabajo iniciado** (4096)
</dt> <dt>

**Método reservado** (de no.. 32767)
</dt> <dt>

**Específico del proveedor** (32768... 65535)
</dt> </dl>

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

 

 




