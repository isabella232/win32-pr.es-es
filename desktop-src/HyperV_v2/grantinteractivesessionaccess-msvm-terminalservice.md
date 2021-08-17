---
description: Concede acceso a la sesión interactiva de la máquina virtual a la lista de administradores de confianza especificada.
ms.assetid: 8a82170d-067b-47e5-a15f-21d6c04128d2
title: Método GrantInteractiveSessionAccess de la Msvm_TerminalService clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_TerminalService.GrantInteractiveSessionAccess
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 39fd1e77eeea7429a2ef225226b964e44f1384295dc798c1b93611f282674fb2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119682335"
---
# <a name="grantinteractivesessionaccess-method-of-the-msvm_terminalservice-class"></a>Método GrantInteractiveSessionAccess de la clase TerminalService de Msvm \_

Concede acceso a la sesión interactiva de la máquina virtual a la lista de administradores de confianza especificada.

## <a name="syntax"></a>Sintaxis


```mof
uint32 GrantInteractiveSessionAccess(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  string                 Trustees[],
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ComputerSystem* \[ En\]
</dt> <dd>

Referencia a una instancia de la clase [**\_ ComputerSystem de Msvm**](msvm-computersystem.md) que representa la máquina virtual a la que se concederá acceso.

</dd> <dt>

*Administradores de confianza* \[ En\]
</dt> <dd>

Matriz de cadenas, cada una de las que identifica un administrador de confianza al que se le concederá acceso a la sesión interactiva de la máquina virtual. Los identificadores de administrador de confianza deben especificarse Windows formato compatible con SAM o Windows de cadena SID.

</dd> <dt>

*Trabajo* \[ out\]
</dt> <dd>

Si la operación se realiza de forma asincrónica, este método devolverá 4096 y este parámetro contendrá una referencia a un objeto derivado de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve uno de los valores siguientes.

<dl> <dt>

**Completado sin error** (0)
</dt> <dt>

**No compatible** (1)
</dt> <dt>

**Error** (2)
</dt> <dt>

**Tiempo de** espera (3)
</dt> <dt>

**Parámetro no válido** (4)
</dt> <dt>

**Estado no válido** (5)
</dt> <dt>

**Parámetros incompatibles** (6)
</dt> <dt>

**DMTF reservado** (..)
</dt> <dt>

**Parámetros de método comprobados: trabajo iniciado** (4096)
</dt> <dt>

**Método reservado** (4097..32767)
</dt> <dt>

**Específico del** proveedor (32768..65535)
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

[**TerminalService de Msvm \_**](msvm-terminalservice.md)
</dt> </dl>

 

