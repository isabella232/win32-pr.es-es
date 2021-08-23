---
title: Método Network.getProxyName
description: El método getProxyName recupera el nombre del servidor proxy que se está utilizando.
ms.assetid: 273b1f7d-84b7-4e50-9f80-9fd1978e7528
keywords:
- Método getProxyName Reproductor de Windows Media
- Método getProxyName Reproductor de Windows Media , clase Network
- Clase de red Reproductor de Windows Media , método getProxyName
topic_type:
- apiref
api_name:
- Network.getProxyName
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43f40eb7eb695376768cd8168e1eb1d1916c8e84e6ede8ef93251df6097a15d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119647455"
---
# <a name="networkgetproxyname-method"></a>Método Network.getProxyName

El **método getProxyName** recupera el nombre del servidor proxy que se está utilizando.

## <a name="syntax"></a>Sintaxis


```JScript
strRetVal = Network.getProxyName(
  protocol
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*protocolo* \[ En\]
</dt> <dd>

**Cadena** que especifica el nombre del protocolo. Para obtener una lista de los protocolos admitidos, vea [Protocolos y tipos de archivo admitidos.](supported-protocols-and-file-types.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve una **cadena que** contiene el nombre del servidor proxy que se está utilizando. El valor devuelto es significativo solo cuando **getProxySettings** devuelve un valor de 2 (use la configuración manual).

## <a name="remarks"></a>Comentarios

Este método produce un error a menos que la aplicación que realiza la llamada se ejecute en el equipo local o intranet.

**Reproductor de Windows Media 10 Mobile:** No se admite este método.

## <a name="examples"></a>Ejemplos

En el ejemplo JScript siguiente se usa *Network*. **getProxyName para** mostrar los nombres Reproductor de Windows Media servidor proxy para los protocolos HTTP y MMS. El **objeto Player** se creó con id. = "Player".


```JScript
// Test whether the HTTP proxy settings are manual.
if (Player.network.getProxySettings("HTTP") == 2)

   // Get the proxy server name for HTTP.
   var proxyNameHTTP = Player.network.getProxyName("HTTP");

// Test whether the MMS proxy settings are manual.
if (Player.network.getProxySettings("MMS") == 2)

   // Get the proxy server name for MMS.
   var proxyNameMMS = Player.network.getProxyName("MMS");

// Display the proxy server names in the browser client area.
// Unavailable proxy server names will display as "undefined".
document.write("The current HTTP proxy server name is: " + proxyNameHTTP);
document.write("<BR>");
document.write("The current MMS proxy server name is: " + proxyNameMMS);

```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto de red**](network-object.md)
</dt> <dt>

[**Network.getProxySettings**](network-getproxysettings.md)
</dt> </dl>

 

 





