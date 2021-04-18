---
title: Win32_SessionBrokerServiceProperties (clase)
description: Define la consulta para un servicio agente de sesiones.
ms.assetid: fe7a0317-8b52-4685-9d0d-2f81058b4561
ms.tgt_platform: multiple
keywords:
- Win32_SessionBrokerServiceProperties clase Servicios de Escritorio remoto
- Servicios de Escritorio remoto de Win32_SessionBrokerServiceProperties de clase, se describe
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
ms.openlocfilehash: 507c4211b9506e0635966e9541167d24495735ef
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535367"
---
# <a name="win32_sessionbrokerserviceproperties-class"></a>\_Clase Win32 SessionBrokerServiceProperties

Define la consulta para un servicio agente de sesiones.

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

La clase **Win32 \_ SessionBrokerServiceProperties** tiene estos métodos.



| Método                                                                                                | Descripción                                                                                                                                                                                                                          |
|:------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DeleteSBDbConnectionString**](win32-sessionbrokerserviceproperties-deletesbdbconnectionstring.md) | Elimina las cadenas de conexión de base de datos (principal y secundaria) del registro.<br/> **Windows server 2012 R2, Windows server 2012 y Windows server 2008 R2:** Este método no está disponible antes de Windows Server 2016<br/> |
| [**InstallBrokerDatabase**](win32-sessionbrokerserviceproperties-installbrokerdatabase.md)           | Instala la base de de agente de conexión a escritorio remoto en el centro de SQL Server<br/>                                                                                                                                                                    |
| [**IsDbReachable**](win32-sessionbrokerserviceproperties-isdbreachable.md)                           | Comprueba si se puede obtener acceso a la base de BD<br/>                                                                                                                                                                                                 |
| [**SetBrokerHAMode**](win32-sessionbrokerserviceproperties-setbrokerhamode.md)                       | Migra datos de la base de datos WID local a la nueva base de datos basada en el SQL Server. También configura el servidor de agente para usar el SQL Server central<br/>                                                                                        |
| [**SetBrokerNonHAMode**](win32-sessionbrokerserviceproperties-setbrokernonhamode.md)                 | Migra datos de la SQL Server central a la base de datos local. También configura el servidor de agente para usar la base de BD local.<br/>                                                                                                              |
| [**SetSBDbConnectionStrings**](win32-sessionbrokerserviceproperties-setsbdbconnectionstrings.md)     | Guarda las cadenas de conexión de base de datos (principal y secundaria) en el registro.<br/> **Windows server 2012 R2, Windows server 2012 y Windows server 2008 R2:** Este método no está disponible antes de Windows Server 2016<br/>     |



 

### <a name="properties"></a>Propiedades

La **clase \_ SessionBrokerServiceProperties de Win32** tiene estas propiedades.

<dl> <dt>

**SBDbConnectionString**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Cadena de conexión de base de datos usada por el servicio agente de sesiones.

**Windows Server 2008 R2:** Esta propiedad no está disponible antes de Windows Server 2012

</dd> <dt>

**SBDbSecondaryConnectionString**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Opcional. Cadena de conexión de base de datos secundaria, usada por el servicio agente de sesiones para admitir la expiración de contraseña.

**Windows server 2012 R2, Windows server 2012 y Windows server 2008 R2:** Esta propiedad no está disponible antes de Windows Server 2016

</dd> <dt>

**SBNetworkName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

El nombre de red que usa el servicio agente de sesiones.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                              |
| Servidor mínimo compatible<br/> | Windows Server 2008 R2<br/>                                                      |
| Espacio de nombres<br/>                | Raíz de \\ CIMv2 \\ TerminalServices<br/>                                               |
| MOF<br/>                      | <dl> <dt>TssdWmi. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>TssdWmi.dll</dt> </dl> |



 

