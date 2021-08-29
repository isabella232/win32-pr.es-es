---
title: Método Network.getProxyPort
description: El método getProxyPort recupera el puerto proxy que se usa.
ms.assetid: 76771750-3763-4029-b194-d8567b5f365e
keywords:
- Método getProxyPort Reproductor de Windows Media
- Método getProxyPort Reproductor de Windows Media , clase Network
- Clase de red Reproductor de Windows Media , método getProxyPort
topic_type:
- apiref
api_name:
- Network.getProxyPort
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83937bcb5d8180085ab97bfd71a0cb1653a65e8bca8cead952e4bf24e10ee690
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119054593"
---
# <a name="networkgetproxyport-method"></a>Método Network.getProxyPort

El **método getProxyPort** recupera el puerto proxy que se usa.

## <a name="syntax"></a>Sintaxis


```JScript
retVal = Network.getProxyPort(
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

Este método devuelve un **valor Number** (**long**) que contiene el puerto proxy que se está utilizando. El valor devuelto es significativo solo cuando **getProxySettings** devuelve un valor de dos (use la configuración manual).

## <a name="remarks"></a>Comentarios

Este método produce un error a menos que la aplicación que realiza la llamada se ejecute en el equipo local o intranet.

**Reproductor de Windows Media 10 Mobile:** No se admite este método.

## <a name="examples"></a>Ejemplos

En el ejemplo JScript siguiente se usa *Network*. **getProxyPort para** mostrar los números de puerto Reproductor de Windows Media proxy actuales para los protocolos MMS y HTTP. El **objeto Player** se creó con id. = "Player".


```JScript
// Test whether the HTTP proxy settings are manual.
if (Player.network.getProxySettings("HTTP") == 2)

   // Get the proxy port number for HTTP.
   var proxyPortHTTP = Player.network.getProxyPort("HTTP");

// Test whether the MMS proxy settings are manual.
if (Player.network.getProxySettings("MMS") == 2)

   // Get the proxy port number for MMS.
   var proxyPortMMS = Player.network.getProxyPort("MMS");

// Display the port numbers in the browser client area.
// Unavailable port numbers will display as "undefined".
document.write("The current HTTP proxy port is: " + proxyPortHTTP);
document.write("<BR>");
document.write("The current MMS proxy port is: " + proxyPortMMS);

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

 

 





