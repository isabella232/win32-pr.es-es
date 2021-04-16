---
description: Recupera el objeto de error para el trabajo de migración, si existe uno.
ms.assetid: 83a68ded-086a-42d9-b76d-e46af70d9b43
title: Método GetError de la clase Msvm_MigrationJob
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MigrationJob.GetError
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 6dce1cb3728c854b1dac742099a3ca035d4865a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666555"
---
# <a name="geterror-method-of-the-msvm_migrationjob-class"></a>Método GetError de la \_ clase MigrationJob de MSVM

Recupera el objeto de error para el trabajo de migración, si existe uno. Cuando el trabajo se está ejecutando o ha finalizado sin errores, este método no devuelve un objeto [**de \_ error de CIM**](/previous-versions//cc150671(v=vs.85)) . Sin embargo, si se ha producido un error en el trabajo debido a algún problema interno o porque el trabajo ha sido terminado por un cliente, se devuelve una instancia de **\_ error de CIM** .

## <a name="syntax"></a>Sintaxis


```mof
uint32 GetError(
  [out] string Error
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Error* \[ de enuncia\]
</dt> <dd>

Si el estado operativo del trabajo no es 2 (correcto), este método devuelve una instancia incrustada de la clase de [**\_ error MSVM**](msvm-error.md) , en formato CIM-XML. Si el estado operativo del trabajo es 2 (correcto), se devuelve **null** .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve uno de los valores siguientes.

<dl> <dt>

**Completado sin error** (0)
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
</dt> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 8 \[\]<br/>                                                              |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                                                    |
| Espacio de nombres<br/>                | \\Virtualización de raíz \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MSVM \_ MigrationJob**](msvm-migrationjob.md)
</dt> </dl>

 

