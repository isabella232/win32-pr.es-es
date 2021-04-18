---
description: Recupera una lista de cambios en la región especificada de un disco virtual desde el identificador de Change Tracking resistente o el identificador de la instantánea de VHDSet proporcionado.
ms.assetid: c1dac403-96e0-4c0d-ad71-858f04bf07cd
title: Método GetVirtualDiskChanges de la clase Msvm_ImageManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.GetVirtualDiskChanges
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 55a9cb9a63e05e002f99984a306566c50d9e1d7f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686940"
---
# <a name="getvirtualdiskchanges-method-of-the-msvm_imagemanagementservice-class"></a>Método GetVirtualDiskChanges de la \_ clase ImageManagementService de MSVM

Recupera una lista de cambios en la región especificada de un disco virtual desde el identificador de Change Tracking resistente o el identificador de la instantánea de VHDSet proporcionado.

## <a name="syntax"></a>Sintaxis


```mof
uint32 GetVirtualDiskChanges(
  [in]  string              Path,
  [in]  string              LimitId,
  [in]  string              TargetSnapshotId,
  [in]  uint64              ByteOffset,
  [in]  uint64              ByteLength,
  [out] uint64              ProcessedByteLength,
  [out] uint64              ChangedByteOffsets[],
  [out] uint64              ChangedByteLengths[],
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Ruta de acceso* \[ de\]
</dt> <dd>

Ruta de acceso completa que especifica la ubicación del archivo de disco duro virtual.

</dd> <dt>

*LimitId* \[ de\]
</dt> <dd>

Un identificador de Change Tracking resistente o un identificador de instantánea de conjunto de VHD que indica la línea de base de los cambios en el disco virtual.

</dd> <dt>

*TargetSnapshotId* \[ de\]
</dt> <dd>

Un identificador de instantánea de VHDSet que indica la instantánea que se va a comparar con la línea de base al detenerse los cambios en el disco duro virtual. Este parámetro solo es válido para los archivos de VHD set.

</dd> <dt>

*Byteoffset (* \[ de\]
</dt> <dd>

Desplazamiento de bytes de la región del disco virtual para el que se van a consultar los cambios.

</dd> <dt>

*ByteLength* \[ de\]
</dt> <dd>

Longitud de bytes de la región del disco virtual para la que se van a consultar los cambios. Debe ser menor que el tamaño del disco virtual.

</dd> <dt>

*ProcessedByteLength* \[ enuncia\]
</dt> <dd>

Longitud total de bytes que se procesó. Puede ser igual a ByteLength o Less.

</dd> <dt>

*ChangedByteOffsets* \[ enuncia\]
</dt> <dd>

La lista de desplazamientos de bytes en el disco virtual que indica el principio de cada intervalo modificado.

</dd> <dt>

*ChangedByteLengths* \[ enuncia\]
</dt> <dd>

La lista de longitudes de bytes de los intervalos modificados en el disco virtual.

</dd> <dt>

*Trabajo* \[ de enuncia\]
</dt> <dd>

Referencia al trabajo (puede ser null si se ha completado la tarea).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve uno de los siguientes valores:

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

**Estado desconocido** (32771)
</dt> <dt>

**Tiempo de espera** (32772)
</dt> <dt>

**Parámetro no válido** (32773)
</dt> <dt>

El **sistema está en uso** (32774)
</dt> <dt>

**Estado no válido para esta operación** (32775)
</dt> <dt>

**Tipo de datos incorrecto** (32776)
</dt> <dt>

El **sistema no está disponible** (32777)
</dt> <dt>

**Memoria insuficiente** (32778)
</dt> <dt>

**No se encontró el archivo** (32779)
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

[**MSVM \_ ImageManagementService**](msvm-imagemanagementservice.md)
</dt> </dl>

 

 




