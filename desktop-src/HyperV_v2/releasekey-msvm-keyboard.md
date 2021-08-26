---
description: Simula una versión de clave.
ms.assetid: EAE84BD5-ECEA-44E7-A7AB-CD18299DF2FE
title: Método ReleaseKey de la Msvm_Keyboard clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Keyboard.ReleaseKey
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 1038838ad7ab0c483dd23e77a716da3ffd2474f7a9e8b4fb311b4a141c1ababb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119980135"
---
# <a name="releasekey-method-of-the-msvm_keyboard-class"></a>Método ReleaseKey de la clase Msvm \_ Keyboard

Simula una versión de clave. Cuando se realiza correctamente, la clave estará en estado up.

## <a name="syntax"></a>Sintaxis


```mof
uint32 ReleaseKey(
  [in] uint32 keyCode
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*keyCode* \[ En\]
</dt> <dd>

Tipo: **uint32**

Código de clave virtual de la clave que se liberará. Para obtener la lista de códigos de clave virtual, vea [**Códigos de clave virtual**](../inputdev/virtual-key-codes.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **uint32**

Un valor devuelto de cero indica que se ha correcto. Un valor distinto de cero indica un error al modificar el estado de la clave.

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

El método **ReleaseKey** asigna referencias al menú de **VK \_** (18), **\_ VK CONTROL** (17) y **VK \_ SHIFT** (16) a **\_ VK LMENU** (164), **VK \_ LCONTROL** (162) y **VK \_ LSHIFT** (160), respectivamente, porque los códigos de clave virtual **VK \_ MENU,** **VK \_ CONTROL** y **VK \_ MAYÚS** no representan claves reales en un teclado.

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

 

