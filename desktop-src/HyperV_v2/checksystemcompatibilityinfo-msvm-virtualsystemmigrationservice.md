---
description: Comprueba la compatibilidad de la información de compatibilidad con el sistema del equipo host.
ms.assetid: 1991c58e-2d0b-4fc3-a04a-c18f358451f6
title: Método CheckSystemCompatibilityInfo de la Msvm_VirtualSystemMigrationService clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemMigrationService.CheckSystemCompatibilityInfo
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 7492d3f7dcdc20abca5cd574d1006b5e2090d02d28f7446dd94ec7b777541b39
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120041985"
---
# <a name="checksystemcompatibilityinfo-method-of-the-msvm_virtualsystemmigrationservice-class"></a>Método CheckSystemCompatibilityInfo de la clase Msvm \_ VirtualSystemMigrationService

Comprueba la compatibilidad de la información de compatibilidad con el sistema del equipo host.

## <a name="syntax"></a>Sintaxis


```mof
uint32 CheckSystemCompatibilityInfo(
  [in]  uint8  CompatibilityInfo[],
  [out] string Reasons[]
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*CompatibilityInfo* \[ En\]
</dt> <dd>

Blob de datos obtenido mediante una llamada al [**método GetSystemCompatibilityInfo**](getsystemcompatibilityinfo-msvm-virtualsystemmigrationservice.md) en el sistema de equipo host.

</dd> <dt>

*Motivos* \[ out\]
</dt> <dd>

Matriz de cadenas que recibe las instancias incrustadas de la clase Error de [**Msvm \_**](msvm-error.md) que representan advertencias o errores.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve uno de los valores siguientes.

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
</dt> <dt>

**No compatible** (32784)
</dt> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                                              |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                                    |
| Espacio de nombres<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Msvm \_ VirtualSystemMigrationService**](msvm-virtualsystemmigrationservice.md)
</dt> </dl>

 

 




