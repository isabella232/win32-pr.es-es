---
title: Win32_SessionBrokerServiceProperties clase
description: Define la consulta para un servicio de agente de sesión.
ms.assetid: fe7a0317-8b52-4685-9d0d-2f81058b4561
ms.tgt_platform: multiple
keywords:
- Win32_SessionBrokerServiceProperties clase Servicios de Escritorio remoto
- Win32_SessionBrokerServiceProperties clase Servicios de Escritorio remoto , descrita
topic_type:
- apiref
api_name:
- Win32_SessionBrokerServiceProperties
- Win32_SessionBrokerServiceProperties.SBNetworkName
- Win32_SessionBrokerServiceProperties.SBDbConnectionString
- Win32_SessionBrokerServiceProperties.SBDbSecondaryConnectionString
api_location:
- TssdWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3f095272ee0d836e77542e20badbe5bb1169206cc6b0e87d742e3fbd235acd52
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119656185"
---
# <a name="win32_sessionbrokerserviceproperties-class"></a>Clase \_ SessionBrokerServiceProperties de Win32

Define la consulta para un servicio de agente de sesión.

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[dynamic, singleton, provider("Win32_WIN32_SESSIONBROKERSERVICEPROPERTIES_Prov"), AMENDMENT]
class Win32_SessionBrokerServiceProperties
{
  string SBNetworkName;
  string SBDbConnectionString;
  string SBDbSecondaryConnectionString;
};
```

## <a name="members"></a>Miembros

La **clase \_ SessionBrokerServiceProperties de Win32** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](/windows)

### <a name="methods"></a>Métodos

La **clase \_ SessionBrokerServiceProperties de Win32** tiene estos métodos.



| Método                                                                                                | Descripción                                                                                                                                                                                                                          |
|:------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DeleteSBDbConnectionString**](win32-sessionbrokerserviceproperties-deletesbdbconnectionstring.md) | Elimina las cadenas de conexión de base de datos (principal y secundaria) del Registro.<br/> **Windows Server 2012 R2, Windows Server 2012 y Windows Server 2008 R2:** Este método no está disponible antes de Windows Server 2016<br/> |
| [**InstallBrokerDatabase**](win32-sessionbrokerserviceproperties-installbrokerdatabase.md)           | Instala la base de datos del Agente de conexión a Escritorio remoto en el SQL Server<br/>                                                                                                                                                                    |
| [**IsDbReachable**](win32-sessionbrokerserviceproperties-isdbreachable.md)                           | Comprueba si la base de datos es accesible<br/>                                                                                                                                                                                                 |
| [**SetBrokerHAMode**](win32-sessionbrokerserviceproperties-setbrokerhamode.md)                       | Migra datos de la base de datos WID local a la nueva base SQL Server base de datos basada en clústeres. También configura el servidor de agente para que use el servidor central SQL Server<br/>                                                                                        |
| [**SetBrokerNonHAMode**](win32-sessionbrokerserviceproperties-setbrokernonhamode.md)                 | Migra datos de la base de SQL Server a la base de datos local. También configura el servidor de agente para que use la base de datos local.<br/>                                                                                                              |
| [**SetSBDbConnectionStrings**](win32-sessionbrokerserviceproperties-setsbdbconnectionstrings.md)     | Guarda las cadenas de conexión de base de datos (principal y secundaria) en el Registro.<br/> **Windows Server 2012 R2, Windows Server 2012 y Windows Server 2008 R2:** Este método no está disponible antes de Windows Server 2016<br/>     |



 

### <a name="properties"></a>Propiedades

La **clase \_ SessionBrokerServiceProperties de Win32** tiene estas propiedades.

<dl> <dt>

**SBDbConnectionString**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Cadena de conexión de base de datos utilizada por el servicio Session Broker.

**Windows Server 2008 R2:** Esta propiedad no está disponible antes de Windows Server 2012

</dd> <dt>

**SBDbSecondaryConnectionString**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Opcional. Cadena de conexión de base de datos secundaria, utilizada por el servicio Session Broker para admitir la expiración de contraseñas.

**Windows Server 2012 R2, Windows Server 2012 y Windows Server 2008 R2:** Esta propiedad no está disponible antes de Windows Server 2016

</dd> <dt>

**SBNetworkName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Nombre de red utilizado por el servicio de agente de sesión.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                              |
| Servidor mínimo compatible<br/> | Windows Server 2008 R2<br/>                                                      |
| Espacio de nombres<br/>                | Root \\ CIMv2 \\ TerminalServices<br/>                                               |
| MOF<br/>                      | <dl> <dt>TssdWmi.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>TssdWmi.dll</dt> </dl> |



 

