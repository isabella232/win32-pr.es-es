---
description: 'Método GetButtonState de Msvm_Ps2Mouse clase : recupera el estado actual del botón de dispositivo especificado.'
ms.assetid: 7772A3AC-1677-44A7-9E5E-D31E90988705
title: Método GetButtonState de la Msvm_Ps2Mouse clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Ps2Mouse.GetButtonState
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 160134a2ae48bb23dc525eeded70b483484e0b71
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108112203"
---
# <a name="getbuttonstate-method-of-the-msvm_ps2mouse-class"></a>Método GetButtonState de la clase \_ Ps2Mouse de Msvm

Recupera el estado actual del botón de dispositivo especificado.

## <a name="syntax"></a>Sintaxis


```mof
uint32 GetButtonState(
  [in]  uint32  buttonIndex,
  [out] boolean buttonState
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*buttonIndex* \[ En\]
</dt> <dd>

Tipo: **uint32**

Índice basado en 1 del botón que se consulta.

</dd> <dt>

*buttonState* \[ out\]
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

**El sistema no está disponible** (32777)
</dt> <dt>

**Memoria sin memoria** (32778)
</dt> </dl>

## <a name="remarks"></a>Comentarios

El acceso a [**la clase \_ Ps2Mouse de Msvm**](msvm-ps2mouse.md) puede estar restringido por el filtrado de UAC. Para obtener más información, vea [Control de cuentas de usuario y WMI.](/windows/desktop/WmiSdk/user-account-control-and-wmi)

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

[**Msvm \_ Ps2Mouse**](msvm-ps2mouse.md)
</dt> </dl>

 

