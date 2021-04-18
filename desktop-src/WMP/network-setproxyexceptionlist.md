---
title: Network. setProxyExceptionList (método)
description: El método setProxyExceptionList especifica la lista de excepciones de proxy. | Network. setProxyExceptionList (método)
ms.assetid: c9eeb058-5ffb-4405-9bf2-776f120e2db4
keywords:
- método setProxyExceptionList de Windows Media Player
- método setProxyExceptionList Windows Media Player, clase de red
- Clase de red Windows Media Player, método setProxyExceptionList
topic_type:
- apiref
api_name:
- Network.setProxyExceptionList
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d1e48aa91ec4857181de5c607a586da42d6f2cb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698540"
---
# <a name="networksetproxyexceptionlist-method"></a>Network. setProxyExceptionList (método)

El método **setProxyExceptionList** especifica la lista de excepciones de proxy.

## <a name="syntax"></a>Sintaxis


```JScript
Network.setProxyExceptionList(
  protocol,
  list
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Protocolo* \[ de de\]
</dt> <dd>

**Cadena** que especifica el nombre del protocolo. Para obtener una lista de protocolos admitidos, consulte [protocolos y tipos de archivo admitidos](supported-protocols-and-file-types.md).

</dd> <dt>

*lista* \[ de de\]
</dt> <dd>

**Cadena** que especifica una lista delimitada por signos de punto y coma de hosts para los que se omite el servidor proxy.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Esta es una lista de equipos, dominios y/o direcciones que omitirán el servidor proxy cuando la parte del host de la dirección URL de destino coincida con una entrada de la lista.

El \* carácter se puede usar como comodín para enumerar entradas. Por ejemplo, \* . com coincidiría con todos los hosts del dominio com, mientras \* que 67. coincidiría con todos los hosts de la clase 67 A la subred.

Este método no tiene ningún efecto a menos que **getProxySettings** devuelva un valor de 2 (use la configuración manual).

Este método produce un error a menos que la aplicación que realiza la llamada se ejecute en el equipo local o en la intranet.

**Windows Media Player 10 Mobile:** Este método no se admite.

## <a name="examples"></a>Ejemplos

En el siguiente ejemplo de JScript se usa *Network*. **setProxyExceptionList** para especificar una lista de hosts para los que se omite el servidor proxy cuando se usa el protocolo MMS. La nueva lista se recupera de un elemento de texto HTML con ID = "XLIST". El objeto **Player** se creó con ID = "Player".


```JScript
// Test whether proxy settings are manual.
if (Player.network.getProxySettings("MMS") == 2){

   // Store the user's new exception list.
   var proxyxlist = XLIST.value;

   // Set the exception list.
   Player.network.setProxyExceptionList("MMS", proxyxlist);
}

else

// Warn that the proxy settings must be set to 2.
alert("Proxy settings must be manual!");

```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Windows Media Player versión 7,0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto de red**](network-object.md)
</dt> </dl>

 

 





