---
title: Network. setProxyPort (método)
description: El método setProxyPort especifica el puerto del proxy que se va a usar. | Network. setProxyPort (método)
ms.assetid: 09cfce4a-191c-4596-b678-15d9328d5c53
keywords:
- método setProxyPort de Windows Media Player
- método setProxyPort Windows Media Player, clase de red
- Clase de red Windows Media Player, método setProxyPort
topic_type:
- apiref
api_name:
- Network.setProxyPort
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2438688535e4727688ddbd5d67fd65cbed15864d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698496"
---
# <a name="networksetproxyport-method"></a>Network. setProxyPort (método)

El método **setProxyPort** especifica el puerto del proxy que se va a usar.

## <a name="syntax"></a>Sintaxis


```JScript
Network.setProxyPort(
  protocol,
  port
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Protocolo* \[ de de\]
</dt> <dd>

**Cadena** que especifica el nombre del protocolo. Para obtener una lista de protocolos admitidos, consulte [protocolos y tipos de archivo admitidos](supported-protocols-and-file-types.md).

</dd> <dt>

*Puerto* \[ de de\]
</dt> <dd>

**Número** (**largo**) que especifica el puerto del proxy que se va a usar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Este método no tiene ningún efecto a menos que **getProxySettings** devuelva un valor de 2 (use la configuración manual).

Este método produce un error a menos que la aplicación que realiza la llamada se ejecute en el equipo local o en la intranet.

**Windows Media Player 10 Mobile:** Este método no se admite.

## <a name="examples"></a>Ejemplos

En el siguiente ejemplo de JScript se usa *Network*. **setProxyPort** para especificar el número de puerto del proxy de Windows Media Player para el protocolo MMS. El número de puerto se recupera de un elemento de entrada HTML con ID = "PORT". El objeto **Player** se creó con ID = "Player".


```JScript
// Test whether proxy settings are manual.
if (Player.network.getProxySettings("MMS") == 2){

   // Store the port number specified by the user.
   var portnumber = PORT.value;

   // Set the port number for the MMS protocol.
   Player.network.setProxyPort("MMS", portnumber);
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

 

 





