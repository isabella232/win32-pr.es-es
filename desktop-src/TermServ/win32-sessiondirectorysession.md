---
title: Win32_SessionDirectorySession clase
description: Proporciona propiedades para ver las propiedades de una sesión Conexión a Escritorio remoto Broker (Agente de conexión a Escritorio remoto).
ms.assetid: 34b5a898-3952-493c-ba62-dd0d298b0600
ms.tgt_platform: multiple
keywords:
- Win32_SessionDirectorySession clase Servicios de Escritorio remoto
- Win32_SessionDirectorySession clase Servicios de Escritorio remoto , descrita
topic_type:
- apiref
api_name:
- Win32_SessionDirectorySession
- Win32_SessionDirectorySession.ServerName
- Win32_SessionDirectorySession.SessionID
- Win32_SessionDirectorySession.UserName
- Win32_SessionDirectorySession.DomainName
- Win32_SessionDirectorySession.ServerIPAddress
- Win32_SessionDirectorySession.TSProtocol
- Win32_SessionDirectorySession.ApplicationType
- Win32_SessionDirectorySession.ResolutionWidth
- Win32_SessionDirectorySession.ResolutionHeight
- Win32_SessionDirectorySession.ColorDepth
- Win32_SessionDirectorySession.CreateTime
- Win32_SessionDirectorySession.DisconnectTime
- Win32_SessionDirectorySession.SessionState
api_location:
- TssdWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0a7d883d3b356713f2f9c3d2b1f9de76676e845020b211ee8a600604a674c54
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118848206"
---
# <a name="win32_sessiondirectorysession-class"></a>Clase SessionDirectorySession de Win32 \_

Proporciona propiedades para ver las propiedades de una sesión Conexión a Escritorio remoto Broker (Agente de conexión a Escritorio remoto).

> [!Note]  
> En Windows Server 2008 R2, el nombre del Agente de sesión de Terminal Services (TS Session Broker) se cambió a Agente de conexión a Escritorio remoto. Estas propiedades se aplican a todos los sistemas operativos compatibles, a menos que se indique lo contrario.

 

## <a name="syntax"></a>Sintaxis

``` syntax
[dynamic, provider("Win32_WIN32_SESSIONDIRECTORYSESSION_Prov"), AMENDMENT]
class Win32_SessionDirectorySession
{
  string   ServerName;
  uint32   SessionID;
  string   UserName;
  string   DomainName;
  string   ServerIPAddress;
  uint32   TSProtocol;
  string   ApplicationType;
  uint32   ResolutionWidth;
  uint32   ResolutionHeight;
  uint32   ColorDepth;
  DateTime CreateTime;
  DateTime DisconnectTime;
  uint32   SessionState;
};
```

## <a name="members"></a>Miembros

La **clase \_ SessionDirectorySession de Win32** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ SessionDirectorySession de Win32** tiene estas propiedades.

<dl> <dt>

**ApplicationType**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

La aplicación se inició con esta sesión. Esto es igual que la **propiedad StartProgram** de [**IMsTscSecuredSettings**](imstscsecuredsettings-interface.md).

</dd> <dt>

**Colordepth**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Profundidad de color de la sesión, medida en bits por píxel.

</dd> <dt>

**CreateTime**
</dt> <dd> <dl> <dt>

Tipo de datos: **DateTime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Fecha y hora en que se creó la sesión. Este valor no se restablece cuando una sesión se desconecta y se vuelve a conectar.

</dd> <dt>

**DisconnectTime**
</dt> <dd> <dl> <dt>

Tipo de datos: **DateTime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Fecha y hora en que se desconectó la sesión (si procede).

</dd> <dt>

**DomainName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Nombre de dominio del usuario que inició sesión en esta sesión.

</dd> <dt>

**ResolutionHeight**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Alto de la sesión, en píxeles, para esta sesión.

</dd> <dt>

**ResolutionWidth**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Ancho de la sesión, en píxeles, para esta sesión.

</dd> <dt>

**ServerIPAddress**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Dirección IP del servidor del Agente de conexión a Escritorio remoto para esta sesión.

</dd> <dt>

**ServerName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **key**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Nombre del servidor del Agente de conexión a Escritorio remoto para esta sesión.

</dd> <dt>

**SessionID**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **key**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Identificador de sesión de esta sesión.

</dd> <dt>

**SessionState**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Estado de esta sesión.

<dt>

0
</dt> <dd>

La sesión está activa.

</dd> <dt>

1
</dt> <dd>

La sesión está desconectada.

</dd> </dl>

</dd> <dt>

**TSProtocol**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Protocolo para esta sesión.

<dt>

0
</dt> <dd>

Esta sesión se ejecuta en una consola física.

</dd> <dt>

1
</dt> <dd>

Para esta sesión se usa un protocolo de terceros propietario.

</dd> <dt>

2
</dt> <dd>

Protocolo de escritorio remoto (RDP) se usa para esta sesión.

</dd> </dl>

</dd> <dt>

**UserName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Nombre de usuario del usuario que inició sesión en esta sesión.

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

[**SessionDirectoryCluster de Win32 \_**](win32-sessiondirectorycluster.md)
</dt> <dt>

[**SessionDirectoryServer de Win32 \_**](win32-sessiondirectoryserver.md)
</dt> </dl>

 

