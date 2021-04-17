---
description: Convertir una instantánea del sistema virtual existente en un punto de referencia. La instantánea se elimina como un efecto secundario. Solo las instantáneas de recuperación se pueden convertir en puntos de referencia.
ms.assetid: c634d749-e18f-4a11-a574-2aee705c0722
title: Método ConvertToReferencePoint de la clase Msvm_VirtualSystemSnapshotService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemSnapshotService.ConvertToReferencePoint
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 18eecc1677abaec5893b3749b4ee82f757cbe93e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666320"
---
# <a name="converttoreferencepoint-method-of-the-msvm_virtualsystemsnapshotservice-class"></a>Método ConvertToReferencePoint de la \_ clase VirtualSystemSnapshotService de MSVM

Convertir una instantánea del sistema virtual existente en un punto de referencia. La instantánea se elimina como un efecto secundario. Solo las instantáneas de recuperación se pueden convertir en puntos de referencia.

## <a name="syntax"></a>Sintaxis


```mof
uint32 ConvertToReferencePoint(
  [in]      CIM_VirtualSystemSettingData     REF AffectedSnapshot,
  [in]      string                               ReferencePointSettings,
  [in, out] Msvm_VirtualSystemReferencePoint REF ResultingReferencePoint,
  [out]     CIM_ConcreteJob                  REF Job
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*AffectedSnapshot* \[ de\]
</dt> <dd>

Referencia a la instantánea del sistema virtual afectada.

</dd> <dt>

*ReferencePointSettings* \[ de\]
</dt> <dd>

Configuración de parámetros.

</dd> <dt>

*ResultingReferencePoint* \[ in, out\]
</dt> <dd>

Punto de referencia del sistema virtual resultante

</dd> <dt>

*Trabajo* \[ de enuncia\]
</dt> <dd>

Si la operación es de larga ejecución, opcionalmente se puede devolver un trabajo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve uno de los valores siguientes:

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

[**MSVM \_ VirtualSystemSnapshotService**](msvm-virtualsystemsnapshotservice.md)
</dt> </dl>

 

 




