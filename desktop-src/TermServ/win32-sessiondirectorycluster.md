---
title: Win32_SessionDirectoryCluster (clase)
description: Proporciona propiedades para ver las propiedades de una granja en Conexión a Escritorio remoto Broker (agente de conexión a escritorio remoto).
ms.assetid: a4a924fd-88ea-46db-968e-378c3dc46cfc
ms.tgt_platform: multiple
keywords:
- Win32_SessionDirectoryCluster clase Servicios de Escritorio remoto
- Servicios de Escritorio remoto de Win32_SessionDirectoryCluster de clase, se describe
topic_type:
- apiref
api_name:
- Win32_SessionDirectoryCluster
- Win32_SessionDirectoryCluster.ClusterName
- Win32_SessionDirectoryCluster.NumberOfServers
- Win32_SessionDirectoryCluster.SingleSessionMode
api_location:
- TssdWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3979dbe5403ca8f18e941b01e95774dabefe3211
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490096"
---
# <a name="win32_sessiondirectorycluster-class"></a>\_Clase Win32 SessionDirectoryCluster

Proporciona propiedades para ver las propiedades de una granja en Conexión a Escritorio remoto Broker (agente de conexión a escritorio remoto).

> [!Note]  
> En Windows Server 2008 R2, el nombre de Terminal Services agente de sesión (agente de sesiones de TS) se cambió al agente de conexión a escritorio remoto. Estas propiedades se aplican a todos los sistemas operativos compatibles a menos que se indique lo contrario.

 

## <a name="syntax"></a>Sintaxis

``` syntax
[dynamic, provider("Win32_WIN32_SESSIONDIRECTORYCLUSTER_Prov"), AMENDMENT]
class Win32_SessionDirectoryCluster
{
  string ClusterName;
  uint32 NumberOfServers;
  uint32 SingleSessionMode;
};
```

## <a name="members"></a>Miembros

La **clase \_ SessionDirectoryCluster de Win32** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ SessionDirectoryCluster de Win32** tiene estas propiedades.

<dl> <dt>

**NombreDeClúster**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Nombre de la granja de servidores en el agente de conexión a escritorio remoto.

</dd> <dt>

**NumberOfServers**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Número de servidores de la granja en el agente de conexión a escritorio remoto.

</dd> <dt>

**SingleSessionMode**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Modo de sesión única de la granja de servidores en el agente de conexión a escritorio remoto.

<dt>

0
</dt> <dd>

La granja de servidores del agente de conexión a escritorio remoto no está en modo de sesión única.

</dd> <dt>

1
</dt> <dd>

La granja de servidores del agente de conexión a escritorio remoto está en modo de sesión única.

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

[**Win32 \_ SessionDirectoryServer**](win32-sessiondirectoryserver.md)
</dt> <dt>

[**Win32 \_ SessionDirectorySession**](win32-sessiondirectorysession.md)
</dt> </dl>

 

