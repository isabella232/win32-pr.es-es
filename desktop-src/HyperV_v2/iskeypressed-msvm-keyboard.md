---
description: Recupera el estado de clave de una clave.
ms.assetid: 4AEB732D-274E-42BB-AA97-9E4D30B81338
title: Método IsKeyPressed de la Msvm_Keyboard clase
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
ms.openlocfilehash: bb8b4e2da0a6f1cd3c30e3d65404ecf308c71e88483e322193497216586b20b0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118392448"
---
# <a name="iskeypressed-method-of-the-msvm_keyboard-class"></a>Método IsKeyPressed de la clase Msvm \_ Keyboard

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

*keyCode* \[ En\]
</dt> <dd>

Tipo: **uint32**

Código de clave virtual de la clave que se consulta. Para obtener la lista de códigos de clave virtual, vea [**Códigos de clave virtual**](../inputdev/virtual-key-codes.md).

</dd> <dt>

*keyState* \[ out\]
</dt> <dd>

Tipo: **booleano**

Estado actual hacia abajo de la clave. Un **valor True** significa que la clave está abajo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **uint32**

Un valor devuelto de cero indica que se ha correcto. Un valor distinto de cero indica un error al consultar el estado de la clave.

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
</dt> </dl>

## <a name="remarks"></a>Comentarios

El **método IsKeyPressed** siempre devolverá **False** para el menú de **VK \_** (18), **\_ VK CONTROL** (17) y **VK \_ MAYÚS** (16) porque no son claves reales en un teclado. Estos códigos de clave virtual siempre se asignan a **VK \_ LMENU** (164), **VK \_ LCONTROL** (162) y **VK \_ LSHIFT** (160), respectivamente, mediante los métodos [**PressKey**](presskey-msvm-keyboard.md) y [**ReleaseKey.**](releasekey-msvm-keyboard.md)

El acceso a [**la clase Msvm \_ Keyboard**](msvm-keyboard.md) podría estar restringido por el filtrado de UAC. Para obtener más información, vea [Control de cuentas de usuario y WMI.](/windows/desktop/WmiSdk/user-account-control-and-wmi)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                                              |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                                    |
| Espacio de nombres<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Teclado de \_ Msvm**](msvm-keyboard.md)
</dt> <dt>

[**Códigos de clave virtual**](../inputdev/virtual-key-codes.md)
</dt> </dl>

 

