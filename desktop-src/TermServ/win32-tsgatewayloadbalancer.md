---
title: Win32_TSGatewayLoadBalancer (clase)
description: Describe un conjunto de servidores de equilibrio de carga de puerta de enlace de Escritorio remoto (puerta de enlace de escritorio remoto). Se usan para equilibrar la carga de las conexiones de puerta de enlace de escritorio remoto entre varios servidores.
ms.assetid: aa7e7b77-7233-4c6a-8f41-cc332fa509d5
ms.tgt_platform: multiple
keywords:
- Win32_TSGatewayLoadBalancer clase Servicios de Escritorio remoto
- Servicios de Escritorio remoto de Win32_TSGatewayLoadBalancer de clase, se describe
topic_type:
- apiref
api_name:
- Win32_TSGatewayLoadBalancer
- Win32_TSGatewayLoadBalancer.Servers
api_location:
- AagWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4956ed4dc9536ff6f7e3263071a2a477cb0f515
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802089"
---
# <a name="win32_tsgatewayloadbalancer-class"></a>\_Clase Win32 TSGatewayLoadBalancer

Describe un conjunto de servidores de equilibrio de carga de puerta de enlace de Escritorio remoto (puerta de enlace de escritorio remoto). Se usan para equilibrar la carga de las conexiones de puerta de enlace de escritorio remoto entre varios servidores.

## <a name="syntax"></a>Sintaxis

``` syntax
[dynamic, provider("AAGProvider"), AMENDMENT]
class Win32_TSGatewayLoadBalancer
{
  string Servers;
};
```

## <a name="members"></a>Miembros

La **clase \_ TSGatewayLoadBalancer de Win32** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La clase **Win32 \_ TSGatewayLoadBalancer** tiene estos métodos.



| Método                                                                             | Descripción                                                                                                      |
|:-----------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------|
| [**AddServers**](addservers-win32-tsgatewayloadbalancer.md)                       | Agrega servidores a la propiedad **servidores** .<br/>                                                             |
| [**DeleteAllServers**](deleteallservers-win32-tsgatewayloadbalancer.md)           | Elimina todos los servidores de equilibrio de carga de puerta de enlace de escritorio remoto que participan en la granja de equilibrio de carga.<br/>               |
| [**DeleteServers**](deleteservers-win32-tsgatewayloadbalancer.md)                 | Elimina los servidores de la propiedad **servidores** .<br/>                                                        |
| [**IsLoadBalancingServer**](win32-tsgatewayloadbalancer-isloadbalancingserver.md) | Determina si el servidor puede realizar el equilibrio de carga.<br/>                                             |
| [**SetServers**](setservers-win32-tsgatewayloadbalancer.md)                       | Establece la propiedad **servidores** con la lista separada por punto y coma de servidores de equilibrio de carga de puerta de enlace de escritorio remoto.<br/> |



 

### <a name="properties"></a>Propiedades

La **clase \_ TSGatewayLoadBalancer de Win32** tiene estas propiedades.

<dl> <dt>

**Servidores**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Lista separada por punto y coma de servidores de equilibrio de carga de puerta de enlace de escritorio remoto. Esta propiedad se puede cambiar con los métodos [**SetServers**](setservers-win32-tsgatewayloadbalancer.md), [**AddServers**](addservers-win32-tsgatewayloadbalancer.md), [**DeleteServers**](deleteservers-win32-tsgatewayloadbalancer.md)y [**DeleteAllServers**](deleteallservers-win32-tsgatewayloadbalancer.md) .

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

[**Win32 \_ TSGatewayRADIUSServer**](win32-tsgatewayradiusserver.md)
</dt> <dt>

[**Win32 \_ TSGatewayResourceAuthorizationPolicy**](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> <dt>

[**Win32 \_ TSGatewayResourceGroup**](win32-tsgatewayresourcegroup.md)
</dt> <dt>

[**Win32 \_ TSGatewayServerSettings**](win32-tsgatewayserversettings.md)
</dt> </dl>

 

