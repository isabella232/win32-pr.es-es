---
title: Win32_SessionDirectoryServer (clase)
description: Proporciona propiedades para ver las propiedades de un servidor de Conexión a Escritorio remoto Broker (agente de conexión a escritorio remoto).
ms.assetid: 73017b71-eff9-4ef6-aba0-71ddb969491f
ms.tgt_platform: multiple
keywords:
- Win32_SessionDirectoryServer clase Servicios de Escritorio remoto
- Servicios de Escritorio remoto de Win32_SessionDirectoryServer de clase, se describe
topic_type:
- apiref
api_name:
- Win32_SessionDirectoryServer
- Win32_SessionDirectoryServer.ServerName
- Win32_SessionDirectoryServer.ServerIPAddress
- Win32_SessionDirectoryServer.ClusterName
- Win32_SessionDirectoryServer.NumberOfSessions
- Win32_SessionDirectoryServer.SingleSessionMode
- Win32_SessionDirectoryServer.ServerWeight
- Win32_SessionDirectoryServer.NumPendRedir
- Win32_SessionDirectoryServer.LoadIndicator
api_location:
- TssdWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9e96efb19e4db56e582cd44d05f3e9865e5282c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996249"
---
# <a name="win32_sessiondirectoryserver-class"></a>\_Clase Win32 SessionDirectoryServer

Proporciona propiedades para ver las propiedades de un servidor de Conexión a Escritorio remoto Broker (agente de conexión a escritorio remoto).

> [!Note]  
> En Windows Server 2008 R2, el nombre de Terminal Services agente de sesión (agente de sesiones de TS) se cambió al agente de conexión a escritorio remoto. Estas propiedades se aplican a todos los sistemas operativos compatibles a menos que se indique lo contrario.

 

## <a name="syntax"></a>Sintaxis

``` syntax
[dynamic, provider("Win32_WIN32_SESSIONDIRECTORYSERVER_Prov"), AMENDMENT]
class Win32_SessionDirectoryServer
{
  string ServerName;
  string ServerIPAddress;
  string ClusterName;
  uint32 NumberOfSessions;
  uint32 SingleSessionMode;
  uint32 ServerWeight;
  uint32 NumPendRedir;
  uint32 LoadIndicator;
};
```

## <a name="members"></a>Miembros

La **clase \_ SessionDirectoryServer de Win32** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ SessionDirectoryServer de Win32** tiene estas propiedades.

<dl> <dt>

**NombreDeClúster**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Nombre de la granja de servidores que incluye el servidor.

</dd> <dt>

**LoadIndicator**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Número relativo que representa el servidor host de sesión de escritorio remoto que se carga cuando se usa el algoritmo de equilibrio de carga predeterminado. El valor de la propiedad *LoadIndicator* se basa en el número de sesiones, el número de solicitudes de redirección pendientes y el valor de peso del servidor.

</dd> <dt>

**NumberOfSessions**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Número de sesiones en el servidor de agente de conexión a escritorio remoto.

</dd> <dt>

**NumPendRedir**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Número de solicitudes de redirección pendientes.

</dd> <dt>

**ServerIPAddress**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Dirección IP del servidor de agente de conexión a escritorio remoto. Si el servidor está configurado para direcciones IPv4 e IPv6, este contendrá la dirección IPv4.

</dd> <dt>

**ServerName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Nombre del servidor de agente de conexión a escritorio remoto.

</dd> <dt>

**ServerWeight**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Valor de peso del servidor, que se usa en el equilibrio de carga.

</dd> <dt>

**SingleSessionMode**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Configuración del modo de sesión única del servidor de agente de conexión a escritorio remoto.

<dt>

0
</dt> <dd>

La granja de servidores no está en modo de sesión única.

</dd> <dt>

1
</dt> <dd>

La granja de servidores de está en modo de sesión única.

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a>Observaciones

Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI). Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows. Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                              |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                         |
| Espacio de nombres<br/>                | Root\\CIMv2<br/>                                                                 |
| MOF<br/>                      | <dl> <dt>TssdWmi. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>TssdWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Win32 \_ SessionDirectoryCluster**](win32-sessiondirectorycluster.md)
</dt> <dt>

[**Win32 \_ SessionDirectorySession**](win32-sessiondirectorysession.md)
</dt> </dl>

 

