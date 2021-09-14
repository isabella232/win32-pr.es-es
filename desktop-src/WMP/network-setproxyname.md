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
ms.openlocfilehash: 5a34546a395d48e939c71a806d8125150fca0ff4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127243230"
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

## <a name="remarks"></a>Observaciones

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

 

 





