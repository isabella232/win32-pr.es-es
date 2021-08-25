---
title: Win32_TSGatewayRADIUSServer clase
description: Describe un servidor Servicio de autenticación remota telefónica de usuario (RADIUS), que tiene un conjunto de directivas de autorización de Servicios de Escritorio remoto de conexión (RD \ 160; CAP).
ms.assetid: 40254354-f446-4e17-b7ec-649c98dd94f9
ms.tgt_platform: multiple
keywords:
- Win32_TSGatewayRADIUSServer clase Servicios de Escritorio remoto
- Win32_TSGatewayRADIUSServer clase Servicios de Escritorio remoto , descrita
topic_type:
- apiref
api_name:
- Win32_TSGatewayRADIUSServer
- Win32_TSGatewayRADIUSServer.Name
- Win32_TSGatewayRADIUSServer.Priority
- Win32_TSGatewayRADIUSServer.SharedSecret
api_location:
- AagWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9997494f9e93980ac4d6e4b1dcb9c95b0d7665a70226f77d1cd4c7ca3ad751d7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119769845"
---
# <a name="win32_tsgatewayradiusserver-class"></a>Clase \_ TSGatewayRADIUSServer de Win32

Describe un servidor Servicio de autenticación remota telefónica de usuario (RADIUS), que tiene un conjunto de directivas Servicios de Escritorio remoto de autorización de conexión (CAP de Escritorio remoto).

RADIUS es un protocolo estándar del sector que se usa para transmitir información de autenticación, autorización y configuración entre un equipo servidor y un servidor de autenticación, denominado servidor RADIUS, con una base de datos que almacena información de usuario. Para obtener más información, vea [Protocolo RADIUS.](/previous-versions/windows/it-pro/windows-server-2003/cc781821(v=ws.10))

## <a name="syntax"></a>Sintaxis

``` syntax
[dynamic, provider("AAGProvider"), AMENDMENT]
class Win32_TSGatewayRADIUSServer
{
  string Name;
  uint32 Priority;
  string SharedSecret;
};
```

## <a name="members"></a>Miembros

La **clase \_ TSGatewayRADIUSServer de Win32** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La **clase \_ TSGatewayRADIUSServer de Win32** tiene estos métodos.



| Método                                                                 | Descripción                                                                  |
|:-----------------------------------------------------------------------|:-----------------------------------------------------------------------------|
| [**Añadir**](win32-tsgatewayradiusserver-add.md)                         | Agrega un nuevo servidor RADIUS.<br/>                                         |
| [**MoveDown**](movedown-win32-tsgatewayradiusserver.md)               | Mueve este servidor RADIUS una posición hacia abajo en el orden de prioridad.<br/> |
| [**MoveUp**](moveup-win32-tsgatewayradiusserver.md)                   | Mueve este servidor RADIUS una posición hacia arriba en el orden de prioridad.<br/>   |
| [**Quitar**](win32-tsgatewayradiusserver-remove.md)                   | Quita el servidor RADIUS actual.<br/>                                |
| [**SetName**](setname-win32-tsgatewayradiusserver.md)                 | Establece la **propiedad Name** para este servidor RADIUS.<br/>                |
| [**SetSharedSecret**](setsharedsecret-win32-tsgatewayradiusserver.md) | Establece la **propiedad SharedSecret** para este servidor RADIUS.<br/>        |
| [**Actualizar**](update-win32-tsgatewayradiusserver.md)                   | Actualiza el servidor RADIUS actual.<br/>                                |



 

### <a name="properties"></a>Propiedades

La **clase \_ TSGatewayRADIUSServer de Win32** tiene estas propiedades.

<dl> <dt>

**Nombre**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Nombre del servidor RADIUS. Esta propiedad se puede cambiar con el [**método SetName.**](setname-win32-tsgatewayradiusserver.md)

</dd> <dt>

**Prioridad**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Prioridad del servidor RADIUS. El servidor de puerta de enlace de Escritorio remoto busca CAP de Escritorio remoto en servidores RADIUS en función de la prioridad. Esta propiedad se puede cambiar con los [**métodos MoveUp,**](moveup-win32-tsgatewayradiusserver.md) [**MoveDown,**](movedown-win32-tsgatewayradiusserver.md) [**Add**](win32-tsgatewayradiusserver-add.md) [**y Remove.**](win32-tsgatewayradiusserver-remove.md)

</dd> <dt>

**SharedSecret**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Secreto compartido para el servidor RADIUS. Esta propiedad se puede cambiar con el [**método SetSharedSecret.**](setsharedsecret-win32-tsgatewayradiusserver.md)

</dd> </dl>

## <a name="remarks"></a>Comentarios

Debe ser miembro del grupo Administradores para usar esta clase.

Managed Object Format (MOF) contienen las definiciones de las Windows instrumental de administración de administración (WMI). Los archivos MOF no se instalan como parte de Microsoft Windows Software Development Kit (SDK). Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información sobre los archivos MOF, [vea Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                           |
| Espacio de nombres<br/>                | Root \\ CIMv2 \\ TerminalServices<br/>                                                 |
| MOF<br/>                      | <dl> <dt>TSGateway.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**TSGatewayConnection de Win32 \_**](win32-tsgatewayconnection.md)
</dt> <dt>

[**Win32 \_ TSGatewayConnectionAuthorizationPolicy**](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> <dt>

[**Win32 \_ TSGatewayLoadBalancer**](win32-tsgatewayloadbalancer.md)
</dt> <dt>

[**Win32 \_ TSGatewayResourceAuthorizationPolicy**](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> <dt>

[**TSGatewayResourceGroup de Win32 \_**](win32-tsgatewayresourcegroup.md)
</dt> <dt>

[**TSGatewayServerSettings de Win32 \_**](win32-tsgatewayserversettings.md)
</dt> </dl>

 

