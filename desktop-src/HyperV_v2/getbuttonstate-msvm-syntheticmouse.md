---
description: 'Método GetButtonState de Msvm_SyntheticMouse clase : recupera el estado actual del botón de dispositivo especificado.'
ms.assetid: 66363AF1-E360-478D-8E62-513DE66EF130
title: Método GetButtonState de la Msvm_SyntheticMouse clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SyntheticMouse.GetButtonState
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 7cc6e010f580318464b0f89cdace06050b201f53e84ad6aaea0684105a2ac0f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119682465"
---
# <a name="getbuttonstate-method-of-the-msvm_syntheticmouse-class"></a>Método GetButtonState de la clase \_ Msvm SyntheticMouse

Recupera el estado actual del botón de dispositivo especificado.

## <a name="syntax"></a>Sintaxis


```mof
uint32 GetButtonState(
  [in]  uint32  buttonIndex,
  [out] boolean isDown
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*buttonIndex* \[ En\]
</dt> <dd>

Tipo: **uint32**

Índice basado en 1 del botón que se consulta.

</dd> <dt>

*isDown* \[ out\]
</dt> <dd>

Tipo: **booleano**

Estado de apagado actual del botón. Un **valor True** significa que el botón está apagado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **uint32**

Un valor devuelto de cero indica que el resultado es correcto. Un valor distinto de cero indica un error de consulta.

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

El acceso a [**la clase \_ Msvm SyntheticMouse**](msvm-syntheticmouse.md) podría estar restringido por el filtrado de UAC. Para obtener más información, vea [Control de cuentas de usuario y WMI.](/windows/desktop/WmiSdk/user-account-control-and-wmi)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                                              |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                                    |
| Espacio de nombres<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Msvm \_ SyntheticMouse**](msvm-syntheticmouse.md)
</dt> </dl>

 

