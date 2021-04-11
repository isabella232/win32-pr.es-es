---
description: Recupera el estado de clave de una clave.
ms.assetid: 4AEB732D-274E-42BB-AA97-9E4D30B81338
title: Método IsKeyPressed de la clase Msvm_Keyboard
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Keyboard.IsKeyPressed
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 44af7a3dc82c0d4d20a2e4c6aff21f7a47837490
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275937"
---
# <a name="iskeypressed-method-of-the-msvm_keyboard-class"></a>Método IsKeyPressed de la \_ clase de teclado MSVM

Recupera el estado de clave de una clave.

## <a name="syntax"></a>Sintaxis


```mof
uint32 IsKeyPressed(
  [in]  uint32  keyCode,
  [out] boolean keyState
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*KeyCode* \[ de\]
</dt> <dd>

Tipo: **UInt32**

Código de tecla virtual de la clave que se va a consultar. Para obtener la lista de códigos de tecla virtual, consulte [**códigos de tecla virtual**](../inputdev/virtual-key-codes.md).

</dd> <dt>

*keyState* \[ enuncia\]
</dt> <dd>

Tipo: **booleano**

El estado actual de la clave. Un valor **true** significa que la tecla está inactiva.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **UInt32**

Un valor devuelto de cero indica que se ha realizado correctamente. Un valor distinto de cero indica un error al consultar el estado de la clave.

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
</dt> </dl>

## <a name="remarks"></a>Observaciones

El método **IsKeyPressed** siempre devolverá **false** para **el \_ menú VK** (18), el **\_ control VK** (17) y el **\_ desplazamiento de VK** (16) porque no son claves reales en un teclado. Estos códigos de tecla virtual siempre se asignan a **VK \_ LMENU** (164), **VK \_ LCONTROL** (162) y **VK \_ LSHIFT** (160), respectivamente, por los métodos [**PressKey**](presskey-msvm-keyboard.md) y [**ReleaseKey**](releasekey-msvm-keyboard.md) .

El acceso a la clase de [**\_ teclado MSVM**](msvm-keyboard.md) puede estar restringido por el filtrado de UAC. Para obtener más información, vea [control de cuentas de usuario y WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

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

[**\_Teclado MSVM**](msvm-keyboard.md)
</dt> <dt>

[**Códigos de tecla virtual**](../inputdev/virtual-key-codes.md)
</dt> </dl>

 

