---
title: Network. setProxyBypassForLocal (método)
description: El método setProxyBypassForLocal especifica un valor que indica si se omite el servidor proxy si el servidor de origen está en una red local.
ms.assetid: 3023a561-f3b7-45c8-a432-baadd795aaa6
keywords:
- método setProxyBypassForLocal de Windows Media Player
- método setProxyBypassForLocal Windows Media Player, clase de red
- Clase de red Windows Media Player, método setProxyBypassForLocal
topic_type:
- apiref
api_name:
- Network.setProxyBypassForLocal
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9426c310c8977317cf5a8415fd19966b8dfc8fd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699744"
---
# <a name="networksetproxybypassforlocal-method"></a>Network. setProxyBypassForLocal (método)

El método **setProxyBypassForLocal** especifica un valor que indica si se omite el servidor proxy si el servidor de origen está en una red local.

## <a name="syntax"></a>Sintaxis


```JScript
Network.setProxyBypassForLocal(
  protocol,
  bypass
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Protocolo* \[ de de\]
</dt> <dd>

**Cadena** que especifica el nombre del protocolo. Para obtener una lista de protocolos admitidos, consulte [protocolos y tipos de archivo admitidos](supported-protocols-and-file-types.md).

</dd> <dt>

*omitir* \[ de\]
</dt> <dd>

**Valor booleano** que especifica si se omite el servidor proxy.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Este método no tiene ningún efecto a menos que **getProxySettings** devuelva un valor de 2 (use la configuración manual).

Este método produce un error a menos que la aplicación que realiza la llamada se ejecute en el equipo local o en la intranet.

**Windows Media Player 10 Mobile:** Este método no se admite.

## <a name="examples"></a>Ejemplos

En el siguiente ejemplo de JScript se usa *Network*. **setProxyBypassForLocal** para especificar si se omite el servidor proxy de Windows Media Player, cuando se usa el protocolo MMS, si el servidor de origen está en una red local. El objeto **Player** se creó con ID = "Player".


```JScript
// Test whether the proxy settings are manual.
if (Player.network.getProxySettings("MMS") == 2){

   // Prompt the user for a setting. Store the response in a variable.
   var proxybypass = confirm("Bypass proxy server for local addresses? \n OK = Yes \n Cancel = No");

   // Set the proxy bypass value using the user input.
   Player.network.setProxyBypassForLocal("MMS", proxybypass);
}

else

// Warn that proxy settings must be set to 2.
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

 

 





