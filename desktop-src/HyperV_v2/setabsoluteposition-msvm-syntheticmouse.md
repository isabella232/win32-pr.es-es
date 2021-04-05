---
description: Establece la posición horizontal y vertical del cursor del mouse.
ms.assetid: 7845E10A-7F61-4134-BF81-AED5483F36AD
title: Método SetAbsolutePosition de la clase Msvm_SyntheticMouse (Dbdao. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SyntheticMouse.SetAbsolutePosition
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 4b8ffb3a4d415f76dedf30acba5869b4cc585eb5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909506"
---
# <a name="setabsoluteposition-method-of-the-msvm_syntheticmouse-class"></a>Método SetAbsolutePosition de la \_ clase SyntheticMouse de MSVM

Establece la posición horizontal y vertical del cursor del mouse.

## <a name="syntax"></a>Sintaxis


```mof
uint32 SetAbsolutePosition(
  [in] sint32 horizontalPosition,
  [in] sint32 verticalPosition
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*horizontalPosition* \[ de\]
</dt> <dd>

Tipo: **sint32**

Nueva posición horizontal del cursor del mouse, en píxeles.

</dd> <dt>

*verticalPosition* \[ de\]
</dt> <dd>

Tipo: **sint32**

Nueva posición vertical del cursor del mouse, en píxeles.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **UInt32**

Un valor devuelto de cero indica que se ha realizado correctamente. Un valor distinto de cero indica un error al modificar la posición de desplazamiento.

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

El acceso a la clase [**MSVM \_ SyntheticMouse**](msvm-syntheticmouse.md) puede estar restringido por el filtrado de UAC. Para obtener más información, vea [control de cuentas de usuario y WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 8 \[\]<br/>                                                              |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                                                    |
| Espacio de nombres<br/>                | \\Virtualización de raíz \\ V2<br/>                                                                     |
| Encabezado<br/>                   | <dl> <dt>Dbdao. h</dt> </dl>                      |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MSVM \_ SyntheticMouse**](msvm-syntheticmouse.md)
</dt> </dl>

 

