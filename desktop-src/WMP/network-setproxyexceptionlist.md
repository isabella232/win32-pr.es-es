---
title: Método Network.setProxyExceptionList
description: El método setProxyExceptionList especifica la lista de excepciones de proxy. | Método Network.setProxyExceptionList
ms.assetid: c9eeb058-5ffb-4405-9bf2-776f120e2db4
keywords:
- Método setProxyExceptionList Reproductor de Windows Media
- Método setProxyExceptionList Reproductor de Windows Media , clase Network
- Clase de red Reproductor de Windows Media método , setProxyExceptionList
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
ms.openlocfilehash: cf72d9c35778e965021ec31671e4e345ec2d8e281d18f9fcb16c8f2ff04d4722
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119647305"
---
# <a name="networksetproxyexceptionlist-method"></a>Método Network.setProxyExceptionList

El **método setProxyExceptionList** especifica la lista de excepciones de proxy.

## <a name="syntax"></a>Sintaxis


```JScript
Network.setProxyExceptionList(
  protocol,
  list
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*protocolo* \[ En\]
</dt> <dd>

**Cadena** que especifica el nombre del protocolo. Para obtener una lista de los protocolos admitidos, vea [Protocolos y tipos de archivo admitidos.](supported-protocols-and-file-types.md)

</dd> <dt>

*list* \[ En\]
</dt> <dd>

**Cadena** que especifica una lista delimitada por punto y coma de hosts para los que se omite el servidor proxy.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Se trata de una lista de equipos, dominios o direcciones que omitirán el servidor proxy cuando la parte del host de la dirección URL de destino coincida con una entrada de la lista.

El \* carácter se puede usar como carácter comodín para enumerar las entradas. Por ejemplo, .com coincidiría con todos los hosts del dominio com, mientras que 67. coincidiría con todos los hosts de la \* subred de la clase A \* 67.

Este método no tiene ningún efecto a menos **que getProxySettings** devuelva un valor de 2 (use la configuración manual).

Este método produce un error a menos que la aplicación que realiza la llamada se ejecute en el equipo local o intranet.

**Reproductor de Windows Media 10 Mobile:** No se admite este método.

## <a name="examples"></a>Ejemplos

En el ejemplo JScript siguiente se usa *Network*. **setProxyExceptionList** para especificar una lista de hosts para los que se omite el servidor proxy cuando se usa el protocolo MMS. La nueva lista se recupera de un elemento HTML TEXT con id. = "XLIST". El **objeto Player** se creó con id. = "Player".


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



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto de red**](network-object.md)
</dt> </dl>

 

 





