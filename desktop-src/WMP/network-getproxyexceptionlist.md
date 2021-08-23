---
title: Método Network.getProxyExceptionList
description: El método getProxyExceptionList recupera la lista de excepciones de proxy.
ms.assetid: f81d8c0f-cc75-470c-9c24-ceaf8a4b6f97
keywords:
- Método getProxyExceptionList Reproductor de Windows Media
- Método getProxyExceptionList Reproductor de Windows Media , clase Network
- Clase de red Reproductor de Windows Media , método getProxyExceptionList
topic_type:
- apiref
api_name:
- Network.getProxyExceptionList
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2becc6c74a5ada575f1bfa85473bd3204bf53a4a739640149cffdd57e3facf2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119054582"
---
# <a name="networkgetproxyexceptionlist-method"></a>Método Network.getProxyExceptionList

El **método getProxyExceptionList** recupera la lista de excepciones de proxy.

## <a name="syntax"></a>Sintaxis


```JScript
strRetVal = Network.getProxyExceptionList(
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

Este método devuelve una **cadena que** especifica una lista delimitada por punto y coma de hosts para los que se omite el servidor proxy. El valor devuelto es significativo solo cuando **getProxySettings** devuelve un valor de dos (use la configuración manual).

## <a name="remarks"></a>Comentarios

Se trata de una lista de equipos, dominios o direcciones que omitirán el servidor proxy cuando la parte del host de la dirección URL de destino coincida con una entrada de la lista.

El \* carácter se puede usar como carácter comodín para enumerar entradas. Por ejemplo, .com coincidiría con todos los hosts del dominio com, mientras que 67. coincidiría con todos los hosts de la \* subred de la clase A \* 67.

Este método produce un error a menos que la aplicación que realiza la llamada se ejecute en el equipo local o intranet.

**Reproductor de Windows Media 10 Mobile:** No se admite este método.

## <a name="examples"></a>Ejemplos

En el ejemplo JScript siguiente se usa *Network*. **getProxyExceptionList para** mostrar las listas de servidores proxy omitido para los protocolos MMS y HTTP. El **objeto Player** se creó con id. = "Player".


```JScript
// Test whether the HTTP proxy settings are manual.
if (Player.network.getProxySettings("HTTP") == 2)

   // Get the proxy exception list for HTTP.
   var proxyExceptionListHTTP = Player.network.getProxyExceptionList("HTTP");

// Test whether the MMS proxy settings are manual.
if (Player.network.getProxySettings("MMS") == 2)

   // Get the proxy exception list for MMS.
   var proxyExceptionListMMS = Player.network.getProxyExceptionList("MMS");

// Display the proxy exception lists in the browser client area.
// Unavailable proxy exception lists will display as "undefined".
document.write("The current HTTP proxy exception list: " + proxyExceptionListHTTP);
document.write("<BR>");
document.write("The current MMS proxy exception list: " + proxyExceptionListMMS);

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

 

 





