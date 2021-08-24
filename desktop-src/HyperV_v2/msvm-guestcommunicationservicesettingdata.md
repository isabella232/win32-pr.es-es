---
description: Representa la configuración del servicio de comunicación de invitado.
ms.assetid: c36d3002-d43e-4284-b765-2795c941f023
title: Msvm_GuestCommunicationServiceSettingData clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_GuestCommunicationServiceSettingData
- Msvm_GuestCommunicationServiceSettingData.Name
- Msvm_GuestCommunicationServiceSettingData.EnabledStatePolicy
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 67026a1dd7e605effb923305c45d329e7a2a502fe0324f00d2ddcf346c899778
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118148054"
---
# <a name="msvm_guestcommunicationservicesettingdata-class"></a>Clase \_ GuestCommunicationServiceSettingData de Msvm

Representa la configuración del servicio de comunicación de invitado.

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_GuestCommunicationServiceSettingData : CIM_SettingData
{
  string Name;
  uint16 EnabledStatePolicy;
};
```

## <a name="members"></a>Miembros

La **clase \_ GuestCommunicationServiceSettingData de Msvm** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ GuestCommunicationServiceSettingData de Msvm** tiene estas propiedades.

<dl> <dt>

**EnabledStatePolicy**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

EnabledStatePolicy es una enumeración de enteros que indica el estado habilitado, deshabilitado o predeterminado de **Msvm \_ GuestCommunicationServiceSettingData**.

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (2)


</dt> <dd>

El servicio de comunicación se establece en el estado habilitado.

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deshabilitado** (3)


</dt> <dd>

El servicio de comunicación se establece en el estado deshabilitado.

</dd> <dt>

<span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span>

<span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span>**Aplazado** (8)


</dt> <dd>

El estado del servicio de comunicación depende **de DefaultEnabledStatePolicy** en **Msvm \_ GuestCommunicationServiceSettingData**.

</dd> </dl>

</dd> <dt>

**Nombre**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

GUID del servicio.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 10 solo aplicaciones de escritorio\]<br/>                                                             |
| Servidor mínimo compatible<br/> | Windows Server 2016<br/>                                                                          |
| Espacio de nombres<br/>                | Virtualización \\ raíz \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CIM \_ SettingData**](cim-settingdata.md)
</dt> </dl>

 

 




