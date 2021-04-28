---
description: 'Método SetButtonState de la Msvm_SyntheticMouse : establece el estado actual del botón de dispositivo especificado.'
ms.assetid: 942DB31C-09A2-43B6-A666-267AF6A84E0E
title: Método SetButtonState de la Msvm_SyntheticMouse clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SyntheticMouse.SetButtonState
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 161520ac1b7e9dba1a084a8fb3c623155aa135fe
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109213"
---
# <a name="setbuttonstate-method-of-the-msvm_syntheticmouse-class"></a>Método SetButtonState de la clase \_ Msvm SyntheticMouse

Establece el estado actual del botón de dispositivo especificado.

## <a name="syntax"></a>Sintaxis


```mof
uint32 SetButtonState(
  [in] uint32  buttonIndex,
  [in] boolean isDown
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*buttonIndex* \[ En\]
</dt> <dd>

Tipo: **uint32**

Índice basado en 1 del botón que se modificará.

</dd> <dt>

*isDown* \[ En\]
</dt> <dd>

Tipo: **booleano**

Nuevo estado hacia abajo del botón. Un **valor True** significa que el botón está apagado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **uint32**

Los valores distintos de cero indican un error al modificar el estado del botón.

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

El acceso a [**la clase \_ Msvm SyntheticMouse**](msvm-syntheticmouse.md) podría estar restringido por el filtrado de UAC. Para obtener más información, vea [Control de cuentas de usuario y WMI.](/windows/desktop/WmiSdk/user-account-control-and-wmi)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 8 solo \[ aplicaciones de escritorio\]<br/>                                                              |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                                                    |
| Espacio de nombres<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Msvm \_ SyntheticMouse**](msvm-syntheticmouse.md)
</dt> </dl>

 

