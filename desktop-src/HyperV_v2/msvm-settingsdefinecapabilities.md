---
description: Proporciona un vínculo entre la instancia de Capabilities y los valores mínimo, máximo, incremental y predeterminados para un recurso.
ms.assetid: 3B09ED8A-D4D0-41E2-B807-96AD8E990773
title: Msvm_SettingsDefineCapabilities (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SettingsDefineCapabilities
- Msvm_SettingsDefineCapabilities.SupportStatement
- Msvm_SettingsDefineCapabilities.GroupComponent
- Msvm_SettingsDefineCapabilities.PartComponent
- Msvm_SettingsDefineCapabilities.PropertyPolicy
- Msvm_SettingsDefineCapabilities.ValueRole
- Msvm_SettingsDefineCapabilities.ValueRange
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7a312d3453b783c3d72f909ec6cb0b37d83feb9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687005"
---
# <a name="msvm_settingsdefinecapabilities-class"></a>MSVM \_ SettingsDefineCapabilities (clase)

Proporciona un vínculo entre la instancia de Capabilities y los valores mínimo, máximo, incremental y predeterminados para un recurso.

La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SettingsDefineCapabilities : CIM_SettingsDefineCapabilities
{
  uint16               SupportStatement;
  CIM_Capabilities REF GroupComponent;
  CIM_SettingData  REF PartComponent;
  uint16               PropertyPolicy = 0;
  uint16               ValueRole = 3;
  uint16               ValueRange = 0;
};
```

## <a name="members"></a>Miembros

La clase **MSVM \_ SettingsDefineCapabilities** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **MSVM \_ SettingsDefineCapabilities** tiene estas propiedades.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Tipo de datos: **[ **\_ capacidades de CIM**](/previous-versions//cc136806(v=vs.85))**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Instancia de Capabilities. Esta propiedad se hereda de [**\_ SettingsDefineCapabilities CIM**](/previous-versions//cc136913(v=vs.85)).

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Tipo de datos: **[ **\_ SettingData de CIM**](/previous-versions//cc136911(v=vs.85))**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Un valor de configuración que se usa para definir la instancia de Capabilities asociada. Esta propiedad se hereda de [**\_ SettingsDefineCapabilities CIM**](/previous-versions//cc136913(v=vs.85)).

</dd> <dt>

**PropertyPolicy**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si las propiedades que no son NULL y que no son de clave de la instancia de datos de configuración asociada se tratan de forma independiente o como un conjunto correlacionado. Esta propiedad se hereda de [**\_ SettingsDefineCapabilities CIM**](/previous-versions//cc136913(v=vs.85)) y siempre está establecida en 0 (independiente).

</dd> <dt>

**SupportStatement**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Identifica la instrucción de soporte técnico.

> [!Note]  
> Esta propiedad se agregó en la versión 1703 de Windows 10.

 

<dt>

<span id="Production"></span><span id="production"></span><span id="PRODUCTION"></span>

<span id="Production"></span><span id="production"></span><span id="PRODUCTION"></span>**Producción** (0)


</dt> <dd></dd> <dt>

<span id="Prerelease"></span><span id="prerelease"></span><span id="PRERELEASE"></span>

<span id="Prerelease"></span><span id="prerelease"></span><span id="PRERELEASE"></span>**Versión preliminar** (1)


</dt> <dd>

> [!Note]  
> No era de **producción** en la versión 1703 de Windows 10.

 

</dd> <dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>**Reservado** (..)


</dt> <dd></dd> </dl>

</dd> <dt>

**ValueRange**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Cualquier semántica adicional en la interpretación de todas las propiedades no clave no nulas de los datos de configuración. Esta propiedad se hereda de [**\_ SettingsDefineCapabilities CIM**](/previous-versions//cc136913(v=vs.85)).

</dd> <dt>

**ValueRole**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Cualquier semántica adicional en la interpretación de las propiedades no clave no nulas de los datos de configuración. Esta propiedad se hereda de [**\_ SettingsDefineCapabilities CIM**](/previous-versions//cc136913(v=vs.85)).

</dd> </dl>

## <a name="remarks"></a>Observaciones

Los valores de las propiedades **ValueRole** y **ValueRange** se usan en los siguientes pares:

-   Punto/valor predeterminado (0/0)
-   Mínimos/admitidos (1/3)
-   Máximos/admitidos (2/3)
-   Incrementos/admitidos (3/3).

"Point" significa que cada una de las propiedades del objeto **PartComponent** representa el valor predeterminado de la plataforma.

"Mínimo" y "máximo" significan que cada una de las propiedades del objeto **PartComponent** representa los valores posibles más pequeños y más grandes para estas propiedades que son compatibles con la plataforma en función de la configuración actual del equipo.

"Incrementos" indica la granularidad con la que puede aumentar o disminuir la configuración.

El acceso a la clase **MSVM \_ SettingsDefineCapabilities** puede estar restringido por el filtrado de UAC. Para obtener más información, vea [control de cuentas de usuario y WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

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

[**\_SETTINGSDEFINECAPABILITIES CIM**](cim-settingsdefinecapabilities.md)
</dt> <dt>

[**\_SETTINGSDEFINECAPABILITIES CIM**](/previous-versions//cc136913(v=vs.85))
</dt> <dt>

[**MSVM \_ SettingsDefineCapabilities (V1)**](/previous-versions/windows/desktop/virtual/msvm-settingsdefinecapabilities)
</dt> <dt>

[Clases de administración de recursos](resource-management-classes.md)
</dt> </dl>

 

