---
title: Win32_TSGatewayRADIUSServer (clase)
description: Describe un servidor Servicio de autenticación remota telefónica de usuario (RADIUS), que tiene un conjunto de directivas de autorización de conexión Servicios de Escritorio remoto (RD \ 160; Cap).
ms.assetid: 40254354-f446-4e17-b7ec-649c98dd94f9
ms.tgt_platform: multiple
keywords:
- Win32_TSGatewayRADIUSServer clase Servicios de Escritorio remoto
- Servicios de Escritorio remoto de Win32_TSGatewayRADIUSServer de clase, se describe
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
ms.openlocfilehash: 4157d89dc942a1c2f8ff7d778f9f8048971902ba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490277"
---
# <a name="win32_tsgatewayradiusserver-class"></a>\_Clase Win32 TSGatewayRADIUSServer

Describe un servidor Servicio de autenticación remota telefónica de usuario (RADIUS), que tiene un conjunto de Servicios de Escritorio remoto directivas de autorización de conexión (Cap de RD).

RADIUS es un protocolo estándar del sector que se usa para transmitir información de autenticación, autorización y configuración entre un equipo servidor y un servidor de autenticación, denominado servidor RADIUS, con una base de datos que almacena información de usuario. Para obtener más información, vea [protocolo RADIUS](/previous-versions/windows/it-pro/windows-server-2003/cc781821(v=ws.10)).

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

La clase **Win32 \_ TSGatewayRADIUSServer** tiene estos métodos.



| Método                                                                 | Descripción                                                                  |
|:-----------------------------------------------------------------------|:-----------------------------------------------------------------------------|
| [**Agréguela**](win32-tsgatewayradiusserver-add.md)                         | Agrega un nuevo servidor RADIUS.<br/>                                         |
| [**Bajar**](movedown-win32-tsgatewayradiusserver.md)               | Mueve el servidor RADIUS una posición hacia abajo en el orden de prioridad.<br/> |
| [**MoveUp**](moveup-win32-tsgatewayradiusserver.md)                   | Mueve el servidor RADIUS una posición hacia arriba en el orden de prioridad.<br/>   |
| [**Retirar**](win32-tsgatewayradiusserver-remove.md)                   | Quita el servidor RADIUS actual.<br/>                                |
| [**SetName**](setname-win32-tsgatewayradiusserver.md)                 | Establece la propiedad de **nombre** para este servidor RADIUS.<br/>                |
| [**SetSharedSecret**](setsharedsecret-win32-tsgatewayradiusserver.md) | Establece la propiedad **SharedSecret** para este servidor RADIUS.<br/>        |
| [**Update**](update-win32-tsgatewayradiusserver.md)                   | Actualiza el servidor RADIUS actual.<br/>                                |



 

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

Nombre del servidor RADIUS. Esta propiedad se puede cambiar con el método [**setName**](setname-win32-tsgatewayradiusserver.md) .

</dd> <dt>

**Prioridad**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Prioridad del servidor RADIUS. El servidor de puerta de enlace de escritorio remoto busca Cap de RD en servidores RADIUS según la prioridad. Esta propiedad se puede cambiar con los métodos [**moveUp**](moveup-win32-tsgatewayradiusserver.md), [**moveDown**](movedown-win32-tsgatewayradiusserver.md), [**Add**](win32-tsgatewayradiusserver-add.md)y [**Remove**](win32-tsgatewayradiusserver-remove.md) .

</dd> <dt>

**SharedSecret**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Secreto compartido para el servidor RADIUS. Esta propiedad se puede cambiar con el método [**SetSharedSecret**](setsharedsecret-win32-tsgatewayradiusserver.md) .

</dd> </dl>

## <a name="remarks"></a>Observaciones

Para usar esta clase, debe ser miembro del grupo administradores.

Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI). Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows. Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                           |
| Espacio de nombres<br/>                | Raíz de \\ CIMv2 \\ TerminalServices<br/>                                                 |
| MOF<br/>                      | <dl> <dt>TSGateway. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Win32 \_ TSGatewayConnection**](win32-tsgatewayconnection.md)
</dt> <dt>

[**Win32 \_ TSGatewayConnectionAuthorizationPolicy**](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> <dt>

[**Win32 \_ TSGatewayLoadBalancer**](win32-tsgatewayloadbalancer.md)
</dt> <dt>

[**Win32 \_ TSGatewayResourceAuthorizationPolicy**](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> <dt>

[**Win32 \_ TSGatewayResourceGroup**](win32-tsgatewayresourcegroup.md)
</dt> <dt>

[**Win32 \_ TSGatewayServerSettings**](win32-tsgatewayserversettings.md)
</dt> </dl>

 

