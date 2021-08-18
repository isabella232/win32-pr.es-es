---
description: Simula un clic del botón de dispositivo especificado.
ms.assetid: 77CFA2E9-E422-464C-B124-6F7D3D56BA4C
title: Método ClickButton de la Msvm_Ps2Mouse clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Ps2Mouse.ClickButton
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 8209e12d6bef02a048b783c98a0299a32ec5ffb96e964ebb7d776e351daecedb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119254505"
---
# <a name="clickbutton-method-of-the-msvm_ps2mouse-class"></a>Método ClickButton de la clase \_ Ps2Mouse de Msvm

Simula un clic del botón de dispositivo especificado. Esto equivale a llamar a [**SetButtonState dos**](setbuttonstate-msvm-syntheticmouse.md) veces, primero para presionar el botón y de nuevo para liberarlo.

## <a name="syntax"></a>Sintaxis


```mof
uint32 ClickButton(
  [in] uint32 buttonIndex
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*buttonIndex* \[ En\]
</dt> <dd>

Tipo: **uint32**

Índice basado en 1 del botón.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **uint32**

Un valor devuelto de cero indica que se ha correcto. Un valor distinto de cero indica un error al modificar el estado del botón.

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

## <a name="remarks"></a>Observaciones

El acceso a [**la clase \_ Ps2Mouse de Msvm**](msvm-ps2mouse.md) podría estar restringido por el filtrado de UAC. Para obtener más información, vea [Control de cuentas de usuario y WMI.](/windows/desktop/WmiSdk/user-account-control-and-wmi)

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

[**Msvm \_ Ps2Mouse**](msvm-ps2mouse.md)
</dt> </dl>

 

