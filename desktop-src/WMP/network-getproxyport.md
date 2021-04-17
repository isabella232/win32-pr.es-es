---
title: Network. getProxyPort (método)
description: El método getProxyPort recupera el puerto del proxy que se está usando.
ms.assetid: 76771750-3763-4029-b194-d8567b5f365e
keywords:
- método getProxyPort de Windows Media Player
- método getProxyPort Windows Media Player, clase de red
- Clase de red Windows Media Player, método getProxyPort
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
ms.openlocfilehash: 3114b2188c0ccb0f6c260df33461fb117e7851e7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708656"
---
# <a name="networkgetproxyport-method"></a>Network. getProxyPort (método)

El método **getProxyPort** recupera el puerto del proxy que se está usando.

## <a name="syntax"></a>Sintaxis


```JScript
retVal = Network.getProxyPort(
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

Este método devuelve un **número** (**largo**) que contiene el puerto del proxy que se está usando. El valor devuelto solo es significativo cuando **getProxySettings** devuelve un valor de dos (use la configuración manual).

## <a name="remarks"></a>Observaciones

Este método produce un error a menos que la aplicación que realiza la llamada se ejecute en el equipo local o en la intranet.

**Windows Media Player 10 Mobile:** Este método no se admite.

## <a name="examples"></a>Ejemplos

En el siguiente ejemplo de JScript se usa *Network*. **getProxyPort** para mostrar los números de puerto de proxy de Windows Media Player actuales para los protocolos MMS y http. El objeto **Player** se creó con ID = "Player".


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

 

 





