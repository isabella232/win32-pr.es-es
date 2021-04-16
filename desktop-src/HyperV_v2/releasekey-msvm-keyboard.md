---
description: Simula una versión de clave.
ms.assetid: EAE84BD5-ECEA-44E7-A7AB-CD18299DF2FE
title: Método ReleaseKey de la clase Msvm_Keyboard
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
ms.openlocfilehash: 2193a4b78128ff3f65e98b4425528a51f6cf5916
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104546827"
---
# <a name="releasekey-method-of-the-msvm_keyboard-class"></a>Método ReleaseKey de la \_ clase de teclado MSVM

Simula una versión de clave. Cuando se realice correctamente, la clave estará en estado activo.

## <a name="syntax"></a>Sintaxis


```mof
uint32 ReleaseKey(
  [in] uint32 keyCode
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*KeyCode* \[ de\]
</dt> <dd>

Tipo: **UInt32**

Código de tecla virtual de la clave que se va a liberar. Para obtener la lista de códigos de tecla virtual, consulte [**códigos de tecla virtual**](../inputdev/virtual-key-codes.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **UInt32**

Un valor devuelto de cero indica que se ha realizado correctamente. Un valor distinto de cero indica un error al modificar el estado de la clave.

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

El método **ReleaseKey** asigna referencias a los **\_ menús VK** (18), **VK \_ (** 17) y **VK \_ Shift** (16) a **VK \_ LMENU** (164), **VK \_ LCONTROL** (162) y **VK \_ LSHIFT** (160), respectivamente, ya que el **\_ menú VK**, el **\_ control VK** y los códigos de tecla virtual **\_ Shift de VK** no representan claves reales en un teclado.

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

 

