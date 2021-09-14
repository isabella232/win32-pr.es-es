---
description: La clase WMIEvent es una clase base de la que se derivan todas las clases de eventos WMI.
ms.assetid: 0393d3fc-7566-4eda-940e-248d622a903a
title: Clase WMIEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WMIEvent
- WMIEvent.SECURITY_DESCRIPTOR
- WMIEvent.TIME_CREATED
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: 99f6804ef1dad4f37bd2727da2e91e801fb0ece2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127073095"
---
# <a name="wmievent-class"></a>Clase WMIEvent

La **clase WMIEvent** es una clase base de la que se derivan todas las clases de eventos WMI.

La sintaxis siguiente se simplifica a Managed Object Format (MOF) e incluye todas sus propiedades heredadas. Las propiedades y los métodos están en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[]
class WMIEvent : __ExtrinsicEvent
{
  uint8  SECURITY_DESCRIPTOR[];
  uint64 TIME_CREATED;
};
```

## <a name="members"></a>Members

La **clase WMIEvent** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase WMIEvent** tiene estas propiedades.

<dl> <dt>

**DESCRIPTOR \_ DE SEGURIDAD**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz uint8**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Descriptor utilizado por el proveedor de eventos para determinar qué usuarios pueden recibir el evento. Esta propiedad se hereda del [**\_ \_ evento**](/windows/desktop/WmiSdk/--event). Para obtener más información sobre las constantes usadas para establecer este descriptor de seguridad, vea [Constantes de seguridad wmi](/windows/desktop/WmiSdk/wmi-security-constants).

</dd> <dt>

**HORA \_ CREADA**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Valor único que indica la hora a la que se generó el evento. Se trata de un valor de 64 bits que representa el número de intervalos de 100 nanosegundos después del 1 de enero de 1601. La información está en formato de hora universal coordinada (UTC). Esta propiedad se hereda del [**\_ \_ evento**](/windows/desktop/WmiSdk/--event).

Para obtener más información sobre el **uso de valores uint64** en scripts, vea [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).

</dd> </dl>

## <a name="remarks"></a>Observaciones

La **clase WMIEvent** se deriva de [**\_ \_ ExtrinsicEvent**](/windows/desktop/WmiSdk/--extrinsicevent).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                                                                              |
| Servidor mínimo compatible<br/> | Windows Server 2003<br/>                                                                                                                        |
| Espacio de nombres<br/>                | \\WMI raíz<br/>                                                                                                                                  |
| MOF<br/>                      | <dl> <dt>Wmi.mof; </dt> <dt>WmiCore.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>WmiProv.dll</dt> </dl>                                                                |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Clases MSMCA](msmca-classes.md)
</dt> <dt>

[**\_\_ExtrinsicEvent**](/windows/desktop/WmiSdk/--extrinsicevent)
</dt> </dl>

 

