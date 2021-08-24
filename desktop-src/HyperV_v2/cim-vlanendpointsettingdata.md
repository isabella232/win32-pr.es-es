---
description: Representa los datos de configuración de un punto de conexión VLAN.
ms.assetid: 5ef3cc55-cf27-40b4-9e94-2e2b42ca41c5
title: CIM_VLANEndpointSettingData clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VLANEndpointSettingData
- CIM_VLANEndpointSettingData.PruneEligibleVLANList
- CIM_VLANEndpointSettingData.NativeVLAN
- CIM_VLANEndpointSettingData.DefaultVLAN
- CIM_VLANEndpointSettingData.TrunkedVLANList
- CIM_VLANEndpointSettingData.AccessVLAN
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 443d7b50ae8fe727a95464ec4e7fa589d7a08db770ce4c5090f37e5c988bfa4b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119682615"
---
# <a name="cim_vlanendpointsettingdata-class"></a>\_CIM VLANEndpointSettingData (clase)

Representa los datos de configuración de un punto de conexión VLAN.

## <a name="syntax"></a>Sintaxis

``` syntax
[Experimental, Abstract, Version("2.11.0"), UMLPackagePath("CIM::Network::VLAN")]
class CIM_VLANEndpointSettingData : CIM_SettingData
{
  uint16 PruneEligibleVLANList[];
  uint16 NativeVLAN;
  uint16 DefaultVLAN;
  uint16 TrunkedVLANList[];
  uint16 AccessVLAN;
};
```

## <a name="members"></a>Miembros

La **clase CIM \_ VLANEndpointSettingData** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase CIM \_ VLANEndpointSettingData** tiene estas propiedades.

<dl> <dt>

**AccessVLAN**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ VLANEndpoint**](cim-vlanendpoint.md).**OperationalEndpointMode**")
</dt> </dl>

VLAN de acceso para el punto de conexión.

</dd> <dt>

**DefaultVLAN**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ VLANEndpoint**](cim-vlanendpoint.md).**OperationalEndpointMode**")
</dt> </dl>

Valor predeterminado de la VLAN nativa en el punto de conexión del tronco.

> [!Note]  
> Esta propiedad solo se usa cuando el punto de conexión de VLAN funciona en modo de tronco, que se especifica en la **propiedad OperationalEndpointMode.**

 

</dd> <dt>

**NativeVLAN**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ VLANEndpoint**](cim-vlanendpoint.md).**OperationalEndpointMode**")
</dt> </dl>

Identificador de VLAN que se usa para etiquetar el tráfico sin etiquetar recibido en el punto de conexión del tronco.

> [!Note]  
> Esta propiedad solo se usa cuando el punto de conexión de VLAN funciona en modo de tronco, que se especifica en la **propiedad SwitchEndpointMode.**

 

</dd> <dt>

**PruneEligibleVLANList**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz uint16**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ VLANEndpoint**](cim-vlanendpoint.md).**OperationalEndpointMode**")
</dt> </dl>

Matriz que contiene los ID de VLAN que el sistema puede quitar del punto de conexión del tronco.

> [!Note]  
> Esta propiedad solo se usa cuando el punto de conexión de VLAN funciona en modo de tronco, que se especifica en la **propiedad OperationalEndpointMode.**

 

</dd> <dt>

**TrunkedVLANList**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz uint16**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ VLANEndpoint**](cim-vlanendpoint.md).**OperationalEndpointMode**")
</dt> </dl>

Matriz que contiene los identificadores de los puntos de conexión vlan con el enlace de tronco habilitado.

> [!Note]  
> Esta propiedad solo se usa cuando el punto de conexión de VLAN funciona en modo de tronco, que se especifica en la **propiedad OperationalEndpointMode.**

 

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 8.1<br/>                                                                                  |
| Servidor mínimo compatible<br/> | Windows Server 2012 R2<br/>                                                                       |
| Espacio de nombres<br/>                | Virtualización \\ raíz \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CIM \_ SettingData**](cim-settingdata.md)
</dt> </dl>

 

