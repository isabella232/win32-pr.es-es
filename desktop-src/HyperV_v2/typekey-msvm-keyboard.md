---
description: Simula una secuencia de teclas de liberación de presión.
ms.assetid: 4166BA71-315D-41BD-857C-48AFB702911E
title: Método TypeKey de la Msvm_Keyboard clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Keyboard.TypeKey
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: d387e1b0d0d939d997589c90195b4a50427f1973eaf46520a0fa70caf62c610b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119068355"
---
# <a name="typekey-method-of-the-msvm_keyboard-class"></a>Método TypeKey de la clase Msvm \_ Keyboard

Simula una secuencia de teclas de liberación de presión. Esto equivale a llamar [**a PressKey**](presskey-msvm-keyboard.md) seguido de [**ReleaseKey**](releasekey-msvm-keyboard.md).

## <a name="syntax"></a>Sintaxis


```mof
uint32 TypeKey(
  [in] uint32 keyCode
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*keyCode* \[ En\]
</dt> <dd>

Tipo: **uint32**

Código de clave virtual de la tecla que se debe presionar. Para obtener la lista de códigos de clave virtual, [**vea Códigos de clave virtual**](../inputdev/virtual-key-codes.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **uint32**

Un valor devuelto de cero indica que el resultado es correcto. Un valor distinto de cero indica un error al modificar el estado de la clave.

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

**El sistema no está** disponible (32777)
</dt> <dt>

**Memoria sin memoria** (32778)
</dt> </dl>

## <a name="remarks"></a>Comentarios

El acceso a [**la clase Msvm \_ Keyboard**](msvm-keyboard.md) podría estar restringido por el filtrado de UAC. Para obtener más información, vea [Control de cuentas de usuario y WMI.](/windows/desktop/WmiSdk/user-account-control-and-wmi)

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

[**Teclado de \_ Msvm**](msvm-keyboard.md)
</dt> <dt>

[**Códigos de clave virtual**](../inputdev/virtual-key-codes.md)
</dt> </dl>

 

