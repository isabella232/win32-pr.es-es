---
description: Modifica una entrada de autorización para un servidor de recuperación.
ms.assetid: fbdf3ecd-42de-49a8-85b8-51fc9c9fcf26
title: Método ModifyAuthorizationEntry de la Msvm_ReplicationService clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.ModifyAuthorizationEntry
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: f1ae9dd28f59064702abc029f0d3bcc6b459eaa60071dfc14074634a5ed70096
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119694284"
---
# <a name="modifyauthorizationentry-method-of-the-msvm_replicationservice-class"></a>Método ModifyAuthorizationEntry de la clase ReplicationService de Msvm \_

Modifica una entrada de autorización para un servidor de recuperación.

## <a name="syntax"></a>Sintaxis


```mof
uint32 ModifyAuthorizationEntry(
  [in]  string              AuthorizationEntry,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*AuthorizationEntry* \[ En\]
</dt> <dd>

Representación de cadena de una instancia de la clase [**\_ ReplicationAuthorizationSettingData de Msvm**](msvm-replicationauthorizationsettingdata.md) que define la entrada de autorización que se va a modificar.

</dd> <dt>

*Trabajo* \[ out\]
</dt> <dd>

Si la operación se realiza de forma asincrónica, este método devolverá 4096 y este parámetro contendrá una referencia a un objeto derivado de [**\_ CIM ConcreteJob**](/previous-versions//cc136808(v=vs.85)).

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

**Sistema en uso** (32774)
</dt> <dt>

**Estado no válido para esta operación** (32775)
</dt> <dt>

**Tipo de datos incorrecto** (32776)
</dt> <dt>

**El sistema no está disponible** (32777)
</dt> <dt>

**Memoria sin memoria** (32778)
</dt> <dt>

**Archivo no encontrado** (32779)
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

[**AddAuthorizationEntry**](addauthorizationentry-msvm-replicationservice.md)
</dt> <dt>

[**RemoveAuthorizationEntry**](removeauthorizationentry-msvm-replicationservice.md)
</dt> <dt>

[**SetAuthorizationEntry**](setauthorizationentry-msvm-replicationservice.md)
</dt> <dt>

[**ReplicationService de Msvm \_**](msvm-replicationservice.md)
</dt> </dl>

 

