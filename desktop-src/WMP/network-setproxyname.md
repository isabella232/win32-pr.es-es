---
title: Método Network.setProxyName
description: El método setProxyName especifica el nombre del servidor proxy que se usará. | Método Network.setProxyName
ms.assetid: dbcb2a00-4387-42af-8055-61d78d021ec7
keywords:
- Método setProxyName Reproductor de Windows Media
- Método setProxyName Reproductor de Windows Media , clase Network
- Clase de red Reproductor de Windows Media , método setProxyName
topic_type:
- apiref
api_name:
- Network.setProxyName
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9831b25e37fd6e19b70c1ee2589736394560c97f841b5d18c3a128a82997cc6d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119134928"
---
# <a name="networksetproxyname-method"></a>Método Network.setProxyName

El **método setProxyName** especifica el nombre del servidor proxy que se usará.

## <a name="syntax"></a>Sintaxis


```JScript
Network.setProxyName(
  protocol,
  name
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*protocolo* \[ En\]
</dt> <dd>

**Cadena** que especifica el nombre del protocolo. Para obtener una lista de los protocolos admitidos, vea [Protocolos y tipos de archivo admitidos.](supported-protocols-and-file-types.md)

</dd> <dt>

*name* \[ En\]
</dt> <dd>

**Cadena** que especifica el nombre del servidor proxy que se usará.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Este método no tiene ningún efecto a menos **que getProxySettings** devuelva un valor de 2 (use la configuración manual).

Este método produce un error a menos que la aplicación que realiza la llamada se ejecute en el equipo local o intranet.

**Reproductor de Windows Media 10 Mobile:** No se admite este método.

## <a name="examples"></a>Ejemplos

En el ejemplo JScript siguiente se usa *Network*. **setProxyName** para especificar el nombre del servidor Reproductor de Windows Media proxy para el protocolo MMS. El nuevo nombre se recupera de un elemento HTML TEXT con id. = "NAME". El **objeto Player** se creó con id. = "Player".


```JScript
// Test whether proxy settings are manual.
if (Player.network.getProxySettings("MMS") == 2){

   // Store the new proxy server name specified by the user.
   var proxyname = NAME.value;

   // Set the proxy server name.
   Player.network.setProxyName("MMS", proxyname);
}

else

// Warn that proxy settings must be set to 2.
alert("Proxy settings must be manual!");

```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto de red**](network-object.md)
</dt> </dl>

 

 





