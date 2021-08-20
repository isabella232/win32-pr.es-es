---
title: Win32_SessionDirectoryCluster clase
description: Proporciona propiedades para ver las propiedades de una granja en Conexión a Escritorio remoto Broker (Agente de conexión a Escritorio remoto).
ms.assetid: a4a924fd-88ea-46db-968e-378c3dc46cfc
ms.tgt_platform: multiple
keywords:
- Win32_SessionDirectoryCluster clase Servicios de Escritorio remoto
- Win32_SessionDirectoryCluster clase Servicios de Escritorio remoto , descrita
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
ms.openlocfilehash: 8f1dba262ddb332f03c7f398c4f205e73a9c9e94054d4164fb94c8c01dc8b505
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118127085"
---
# <a name="win32_sessiondirectorycluster-class"></a>Clase SessionDirectoryCluster de Win32 \_

Proporciona propiedades para ver las propiedades de una granja en Conexión a Escritorio remoto Broker (Agente de conexión a Escritorio remoto).

> [!Note]  
> En Windows Server 2008 R2, el nombre del Agente de sesión de Terminal Services (TS Session Broker) se cambió a Agente de conexión a Escritorio remoto. Estas propiedades se aplican a todos los sistemas operativos compatibles, a menos que se indique lo contrario.

 

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

**ClusterName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **key**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Nombre de la granja en agente de conexión a Escritorio remoto.

</dd> <dt>

**NumberOfServers**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Número de servidores de la granja en agente de conexión a Escritorio remoto.

</dd> <dt>

**SingleSessionMode**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Modo de sesión única de la granja en agente de conexión a Escritorio remoto.

<dt>

0
</dt> <dd>

La granja de servidores del Agente de conexión a Escritorio remoto no está en modo de sesión única.

</dd> <dt>

1
</dt> <dd>

La granja de servidores del Agente de conexión a Escritorio remoto está en modo de sesión única.

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a>Comentarios

Managed Object Format (MOF) contienen las definiciones de las Windows instrumental de administración de recursos (WMI). Los archivos MOF no se instalan como parte del Kit de desarrollo de software (SDK) de Microsoft Windows. Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información sobre los archivos MOF, [vea Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                              |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                         |
| Espacio de nombres<br/>                | Root\\CIMv2<br/>                                                                 |
| MOF<br/>                      | <dl> <dt>TssdWmi.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>TssdWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SessionDirectoryServer de Win32 \_**](win32-sessiondirectoryserver.md)
</dt> <dt>

[**SessionDirectorySession de Win32 \_**](win32-sessiondirectorysession.md)
</dt> </dl>

 

