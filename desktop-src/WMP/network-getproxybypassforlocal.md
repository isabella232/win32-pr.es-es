---
title: Network. getProxyBypassForLocal (método)
description: El método getProxyBypassForLocal recupera un valor que indica si se omite el servidor proxy si el servidor de origen está en una red local.
ms.assetid: e5217d56-da22-4424-94b0-400369410b47
keywords:
- método getProxyBypassForLocal de Windows Media Player
- método getProxyBypassForLocal Windows Media Player, clase de red
- Clase de red Windows Media Player, método getProxyBypassForLocal
topic_type:
- apiref
api_name:
- Network.getProxyBypassForLocal
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c60b9248cd5a893496c2de88c5a5370dfb7bf82
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708806"
---
# <a name="networkgetproxybypassforlocal-method"></a>Network. getProxyBypassForLocal (método)

El método **getProxyBypassForLocal** recupera un valor que indica si se omite el servidor proxy si el servidor de origen está en una red local.

## <a name="syntax"></a>Sintaxis


```JScript
bRetVal = Network.getProxyBypassForLocal(
  protocol
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Protocolo* \[ de de\]
</dt> <dd>

**Cadena** que especifica el nombre del protocolo. Para obtener una lista de protocolos admitidos, consulte [protocolos y tipos de archivo admitidos](supported-protocols-and-file-types.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve un **valor booleano** que indica si se omite el servidor proxy. El valor devuelto solo es significativo cuando **getProxySettings** devuelve un valor de dos (use la configuración manual).

## <a name="remarks"></a>Observaciones

Este método produce un error a menos que la aplicación que realiza la llamada se ejecute en el equipo local o en la intranet.

**Windows Media Player 10 Mobile:** Este método no se admite.

## <a name="examples"></a>Ejemplos

En el siguiente ejemplo de JScript se usa *Network*. **getProxyBypassForLocal** para mostrar si Windows Media Player está configurado para omitir el servidor proxy para las direcciones locales. El objeto **Player** se creó con ID = "Player".


```JScript
// Test whether the HTTP proxy settings are manual.
if (Player.network.getProxySettings("HTTP") == 2)

   // Get the proxy bypass for local value for HTTP.
   var proxyBypassForLocalHTTP = Player.network.getProxyBypassForLocal("HTTP");

// Test whether the MMS proxy settings are manual.
if (Player.network.getProxySettings("MMS") == 2)

   // Get the proxy bypass for local value for MMS.
   var proxyBypassForLocalMMS = Player.network.getProxyBypassForLocal("MMS");

// Display the proxy bypass for local values in the browser client area.
// Unavailable proxy bypass for local values will display as "undefined".
document.write("The current HTTP proxy bypass for local value: " + proxyBypassForLocalHTTP);
document.write("<BR>");
document.write("The current MMS proxy bypass for local value: " + proxyBypassForLocalMMS);

```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Windows Media Player versión 7,0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto de red**](network-object.md)
</dt> <dt>

[**Network. getProxySettings**](network-getproxysettings.md)
</dt> </dl>

 

 





