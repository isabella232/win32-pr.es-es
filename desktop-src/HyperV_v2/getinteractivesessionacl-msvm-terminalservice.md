---
description: Recupera la lista de control de acceso discrecional (DACL) actual que controla el acceso a la sesión interactiva de una máquina virtual.
ms.assetid: 9b81f6d5-20fa-4277-b943-756d85359fd2
title: Método GetInteractiveSessionACL de la Msvm_TerminalService clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_TerminalService.GetInteractiveSessionACL
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 37f33ce16d0b5eb2b998f4f08a37a6e601f82d3aecf49a2e8e68b2a7f571a01e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119253725"
---
# <a name="getinteractivesessionacl-method-of-the-msvm_terminalservice-class"></a>Método GetInteractiveSessionACL de la clase TerminalService de Msvm \_

Recupera la lista de *control de acceso discrecional* (DACL) actual que controla el acceso a la sesión interactiva de una máquina virtual.

## <a name="syntax"></a>Sintaxis


```mof
uint32 GetInteractiveSessionACL(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [out] string                 AccessControlList[]
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ComputerSystem* \[ En\]
</dt> <dd>

Referencia a una instancia de la clase [**\_ ComputerSystem de Msvm**](msvm-computersystem.md) que representa la máquina virtual cuya DACL se recuperará.

</dd> <dt>

*AccessControlList* \[ out\]
</dt> <dd>

Matriz de cadenas, cada una de las que contiene una instancia incrustada de la clase [**\_ InteractiveSessionACE de Msvm**](msvm-interactivesessionace.md) que representa una entrada de *control* de acceso (ACE) en la sesión interactiva de máquina virtual DACL.

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

**Parámetros de método activados: trabajo iniciado** (4096)
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

 

 




