---
title: Win32_TSGatewayLoadBalancer clase
description: Describe un conjunto de servidores de equilibrio de carga Escritorio remoto Gateway (Puerta de enlace de Escritorio remoto). Se usan para equilibrar la carga de las conexiones de puerta de enlace de Escritorio remoto en varios servidores.
ms.assetid: aa7e7b77-7233-4c6a-8f41-cc332fa509d5
ms.tgt_platform: multiple
keywords:
- Win32_TSGatewayLoadBalancer clase Servicios de Escritorio remoto
- Win32_TSGatewayLoadBalancer clase Servicios de Escritorio remoto , descrita
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126890689"
---
# <a name="win32_tsgatewayloadbalancer-class"></a>Clase \_ TSGatewayLoadBalancer de Win32

Describe un conjunto de servidores de equilibrio de carga Escritorio remoto Gateway (Puerta de enlace de Escritorio remoto). Se usan para equilibrar la carga de las conexiones de puerta de enlace de Escritorio remoto en varios servidores.

## <a name="syntax"></a>Sintaxis

``` syntax
[dynamic, provider("AAGProvider"), AMENDMENT]
class Win32_TSGatewayLoadBalancer
{
  string Servers;
};
```

## <a name="members"></a>Members

La **clase \_ TSGatewayLoadBalancer de Win32** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La **clase \_ TSGatewayLoadBalancer de Win32** tiene estos métodos.



| Método                                                                             | Descripción                                                                                                      |
|:-----------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------|
| [**AddServers**](addservers-win32-tsgatewayloadbalancer.md)                       | Agrega servidores a la **propiedad Servidores.**<br/>                                                             |
| [**DeleteAllServers**](deleteallservers-win32-tsgatewayloadbalancer.md)           | Elimina todos los servidores de equilibrio de carga de puerta de enlace de Escritorio remoto que participan en la granja de equilibrio de carga.<br/>               |
| [**DeleteServers**](deleteservers-win32-tsgatewayloadbalancer.md)                 | Elimina servidores de la **propiedad Servidores.**<br/>                                                        |
| [**IsLoadBalancingServer**](win32-tsgatewayloadbalancer-isloadbalancingserver.md) | Determina si el servidor puede realizar el equilibrio de carga.<br/>                                             |
| [**SetServers**](setservers-win32-tsgatewayloadbalancer.md)                       | Establece la **propiedad Servidores** con la lista separada por punto y coma de los servidores de equilibrio de carga de puerta de enlace de Escritorio remoto.<br/> |



 

### <a name="properties"></a>Propiedades

La **clase \_ TSGatewayLoadBalancer de Win32** tiene estas propiedades.

<dl> <dt>

**Servidores**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **key**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Lista separada por punto y coma de servidores de equilibrio de carga de puerta de enlace de Escritorio remoto. Esta propiedad se puede cambiar con los [**métodos SetServers**](setservers-win32-tsgatewayloadbalancer.md), [**AddServers,**](addservers-win32-tsgatewayloadbalancer.md) [**DeleteServers**](deleteservers-win32-tsgatewayloadbalancer.md)y [**DeleteAllServers.**](deleteallservers-win32-tsgatewayloadbalancer.md)

</dd> </dl>

## <a name="remarks"></a>Observaciones

Debe ser miembro del grupo Administradores para usar esta clase.

Managed Object Format (MOF) contienen las definiciones de las Windows instrumental de administración de recursos (WMI). Los archivos MOF no se instalan como parte de Microsoft Windows Software Development Kit (SDK). Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información sobre los archivos MOF, [vea Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                           |
| Espacio de nombres<br/>                | \\TerminalServices de CIMv2 \\ raíz<br/>                                                 |
| MOF<br/>                      | <dl> <dt>TSGateway.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



## <a name="see-also"></a>Consulte también

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

 

