---
description: 'Método RemoveAssociatedData de la clase Msvm_VirtualSystemReferencePointService: quita el registro de datos asociado al punto de referencia.'
ms.assetid: b6206bda-c195-4c6f-9b80-508c20b53ce5
title: Método RemoveAssociatedData de la Msvm_VirtualSystemReferencePointService clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemReferencePointService.RemoveAssociatedData
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 3f8cef79e55379df1f91a0e1291144a7f4fdf92378e44cd9ed3588c83b3a3d4a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119147908"
---
# <a name="removeassociateddata-method-of-the-msvm_virtualsystemreferencepointservice-class"></a>Método RemoveAssociatedData de la clase Msvm \_ VirtualSystemReferencePointService

Quita el registro de datos asociado al punto de referencia.

## <a name="syntax"></a>Sintaxis


```mof
uint32 RemoveAssociatedData(
  [in]  Msvm_VirtualSystemReferencePoint REF AffectedReferencePoint,
  [out] CIM_ConcreteJob                  REF Job
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*AffectedReferencePoint* \[ En\]
</dt> <dd>

Referencia a la instancia [**de Msvm \_ VirtualSystemReferencePoint**](msvm-virtualsystemreferencepoint.md) que representa el punto de referencia que se va a quitar.

</dd> <dt>

*Trabajo* \[ out\]
</dt> <dd>

Parámetro opcional para supervisar el progreso de la operación, que se usa si el método no se pudo ejecutar sincrónicamente. Si la operación se ejecuta de forma asincrónica, el valor devuelto es 4096.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si se ejecuta correctamente, devuelve 0 (completado sin error) o 4096 (trabajo iniciado); de lo contrario, devuelva un error.

<dl> <dt>

**Completado sin error** (0)
</dt> <dt>

**Parámetros de método comprobados: trabajo iniciado** (4096)
</dt> <dt>

**Error** (32768)
</dt> <dt>

**Acceso denegado** (32769)
</dt> <dt>

**No compatible** (32770)
</dt> <dt>

**El estado es desconocido** (32771)
</dt> <dt>

**Tiempo de** espera (32772)
</dt> <dt>

**Parámetro no** válido (32773)
</dt> <dt>

**El sistema está en uso** (32774)
</dt> <dt>

**Estado no válido para esta operación** (32775)
</dt> <dt>

**Tipo de datos incorrecto** (32776)
</dt> <dt>

**El sistema no está disponible** (32777)
</dt> <dt>

**Memoria sin memoria** (32778)
</dt> </dl>

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

[**Msvm \_ VirtualSystemReferencePointService**](msvm-virtualsystemreferencepointservice.md)
</dt> </dl>

 

 




