---
title: Método Network.setProxyPort
description: El método setProxyPort especifica el puerto proxy que se usará. | Método Network.setProxyPort
ms.assetid: 09cfce4a-191c-4596-b678-15d9328d5c53
keywords:
- Método setProxyPort Reproductor de Windows Media
- Método setProxyPort Reproductor de Windows Media , clase Network
- Clase de red Reproductor de Windows Media , método setProxyPort
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127243225"
---
# <a name="networksetproxyport-method"></a>Método Network.setProxyPort

El **método setProxyPort** especifica el puerto proxy que se usará.

## <a name="syntax"></a>Sintaxis


```JScript
Network.setProxyPort(
  protocol,
  port
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*protocolo* \[ En\]
</dt> <dd>

**Cadena** que especifica el nombre del protocolo. Para obtener una lista de los protocolos admitidos, vea [Protocolos y tipos de archivo admitidos.](supported-protocols-and-file-types.md)

</dd> <dt>

*puerto* \[ En\]
</dt> <dd>

**Number** (**long**) que especifica el puerto de proxy que se usará.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Este método no tiene ningún efecto a menos **que getProxySettings** devuelva un valor de 2 (use la configuración manual).

Este método produce un error a menos que la aplicación que realiza la llamada se ejecute en el equipo local o intranet.

**Reproductor de Windows Media 10 Mobile:** No se admite este método.

## <a name="examples"></a>Ejemplos

En el ejemplo JScript siguiente se usa *Network*. **setProxyPort para** especificar el número de puerto Reproductor de Windows Media proxy para el protocolo MMS. El número de puerto se recupera de un elemento HTML INPUT con id. = "PORT". El **objeto Player** se creó con id. = "Player".


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
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto de red**](network-object.md)
</dt> </dl>

 

 





