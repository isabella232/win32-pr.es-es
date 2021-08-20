---
title: Win32_SessionDirectoryServer clase
description: Proporciona propiedades para ver las propiedades de un servidor Conexión a Escritorio remoto Broker (Agente de conexión a Escritorio remoto).
ms.assetid: 73017b71-eff9-4ef6-aba0-71ddb969491f
ms.tgt_platform: multiple
keywords:
- Win32_SessionDirectoryServer clase Servicios de Escritorio remoto
- Win32_SessionDirectoryServer clase Servicios de Escritorio remoto , descrita
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
ms.openlocfilehash: 702b56a9cf8aee2ab38ad9d6b3a0f2d270b2128ea46934cc1beb720c77400d07
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118127075"
---
# <a name="win32_sessiondirectoryserver-class"></a>Clase SessionDirectoryServer de Win32 \_

Proporciona propiedades para ver las propiedades de un servidor Conexión a Escritorio remoto Broker (Agente de conexión a Escritorio remoto).

> [!Note]  
> En Windows Server 2008 R2, el nombre del Agente de sesión de Terminal Services (TS Session Broker) se cambió a Agente de conexión a Escritorio remoto. Estas propiedades se aplican a todos los sistemas operativos compatibles, a menos que se indique lo contrario.

 

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

**ClusterName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Nombre de la granja que incluye el servidor.

</dd> <dt>

**LoadIndicator**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Número relativo que representa la carga del servidor host de sesión de Escritorio remoto cuando se usa el algoritmo de equilibrio de carga predeterminado. El *valor de la propiedad LoadIndicator* se basa en el número de sesiones, el número de solicitudes de redireccionamiento pendientes y el valor de peso del servidor.

</dd> <dt>

**NumberOfSessions**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Número de sesiones en el servidor del Agente de conexión a Escritorio remoto.

</dd> <dt>

**NumPendRedir**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Número de solicitudes de redireccionamiento pendientes.

</dd> <dt>

**ServerIPAddress**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Dirección IP del servidor del Agente de conexión a Escritorio remoto. Si el servidor está configurado para direcciones IPv4 e IPv6, contendrá la dirección IPv4.

</dd> <dt>

**ServerName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Nombre del servidor del Agente de conexión a Escritorio remoto.

</dd> <dt>

**ServerWeight**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Valor de peso del servidor, que se usa en el equilibrio de carga.

</dd> <dt>

**SingleSessionMode**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Configuración del modo de sesión única del servidor del Agente de conexión a Escritorio remoto.

<dt>

0
</dt> <dd>

La granja no está en modo de sesión única.

</dd> <dt>

1
</dt> <dd>

La granja de servidores de está en modo de sesión única.

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a>Comentarios

Managed Object Format (MOF) contienen las definiciones de las Windows instrumental de administración de administración (WMI). Los archivos MOF no se instalan como parte de Microsoft Windows Software Development Kit (SDK). Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información sobre los archivos MOF, [vea Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                              |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                         |
| Espacio de nombres<br/>                | Root\\CIMv2<br/>                                                                 |
| MOF<br/>                      | <dl> <dt>TssdWmi.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>TssdWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SessionDirectoryCluster de Win32 \_**](win32-sessiondirectorycluster.md)
</dt> <dt>

[**SessionDirectorySession de Win32 \_**](win32-sessiondirectorysession.md)
</dt> </dl>

 

