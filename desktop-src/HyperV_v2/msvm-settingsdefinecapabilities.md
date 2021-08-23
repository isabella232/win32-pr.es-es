---
description: Proporciona un vínculo entre la instancia de funcionalidades y la configuración mínima, máxima, incremental y predeterminada de un recurso.
ms.assetid: 3B09ED8A-D4D0-41E2-B807-96AD8E990773
title: Msvm_SettingsDefineCapabilities clase
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
ms.openlocfilehash: 7194632af7bc1154e6a9bbca1dd5ef0bcca0fb46ab13693d20160ea404068adf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118950474"
---
# <a name="msvm_settingsdefinecapabilities-class"></a>Clase Msvm \_ SettingsDefineCapabilities

Proporciona un vínculo entre la instancia de funcionalidades y la configuración mínima, máxima, incremental y predeterminada de un recurso.

La sintaxis siguiente se simplifica Managed Object Format (MOF) e incluye todas las propiedades heredadas.

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

La **clase Msvm \_ SettingsDefineCapabilities** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase Msvm \_ SettingsDefineCapabilities** tiene estas propiedades.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Tipo de datos: **[ **Funcionalidades cim \_**](/previous-versions//cc136806(v=vs.85))**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Instancia de funcionalidades. Esta propiedad se hereda de [**la \_ configuración de CIMDefineCapabilities.**](/previous-versions//cc136913(v=vs.85))

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Tipo de datos: **[ **CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Una configuración que se usa para definir la instancia de funcionalidades asociada. Esta propiedad se hereda de [**la \_ configuración de CIMDefineCapabilities.**](/previous-versions//cc136913(v=vs.85))

</dd> <dt>

**PropertyPolicy**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si las propiedades no null y no clave de la instancia de datos de configuración asociada se tratan de forma independiente o como un conjunto correlacionado. Esta propiedad se hereda de [**la \_ configuración de CIMDefineCapabilities**](/previous-versions//cc136913(v=vs.85)) y siempre se establece en 0 (independiente).

</dd> <dt>

**SupportStatement**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Identifica la instrucción de compatibilidad.

> [!Note]  
> Esta propiedad se agregó en Windows 10, versión 1703.

 

<dt>

<span id="Production"></span><span id="production"></span><span id="PRODUCTION"></span>

<span id="Production"></span><span id="production"></span><span id="PRODUCTION"></span>**Producción** (0)


</dt> <dd></dd> <dt>

<span id="Prerelease"></span><span id="prerelease"></span><span id="PRERELEASE"></span>

<span id="Prerelease"></span><span id="prerelease"></span><span id="PRERELEASE"></span>**Versión preliminar** (1)


</dt> <dd>

> [!Note]  
> Era **NonProduction** en Windows 10, versión 1703.

 

</dd> <dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>**Reservado** (..).


</dt> <dd></dd> </dl>

</dd> <dt>

**ValueRange**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Cualquier semántica adicional sobre la interpretación de todas las propiedades no null y no clave de los datos de configuración. Esta propiedad se hereda de [**la \_ configuración de CIMDefineCapabilities.**](/previous-versions//cc136913(v=vs.85))

</dd> <dt>

**ValueRole**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Cualquier semántica adicional sobre la interpretación de las propiedades no null y no clave de los datos de configuración. Esta propiedad se hereda de [**la \_ configuración de CIMDefineCapabilities.**](/previous-versions//cc136913(v=vs.85))

</dd> </dl>

## <a name="remarks"></a>Comentarios

Los valores de las **propiedades ValueRole** y **ValueRange** se usan en los pares siguientes:

-   Punto/valor predeterminado (0/0)
-   Mínimos/Admitidos (1/3)
-   Máximos/admitidos (2/3)
-   Incrementos/admitidos (3/3).

"Point" significa que cada una de las propiedades del **objeto PartComponent** representa el valor predeterminado de la plataforma.

"Mínimos" y "Máximos" significan que cada una de las propiedades del objeto **PartComponent** representa los valores más pequeños y mayores posibles para estas propiedades que son compatibles con la plataforma en función de la configuración del equipo actual.

"Incrementos" indica la granularidad con la que puede aumentar o disminuir la configuración.

El acceso a la **clase Msvm \_ SettingsDefineCapabilities** puede estar restringido por el filtrado de UAC. Para obtener más información, vea [Control de cuentas de usuario y WMI.](/windows/desktop/WmiSdk/user-account-control-and-wmi)

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

[**Configuración \_ de CIMDefineCapabilities**](cim-settingsdefinecapabilities.md)
</dt> <dt>

[**Configuración \_ de CIMDefineCapabilities**](/previous-versions//cc136913(v=vs.85))
</dt> <dt>

[**Configuración de \_ MsvmDefineCapabilities (V1)**](/previous-versions/windows/desktop/virtual/msvm-settingsdefinecapabilities)
</dt> <dt>

[Clases de administración de recursos](resource-management-classes.md)
</dt> </dl>

 

