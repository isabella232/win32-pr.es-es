---
title: Network. getProxySettings (método)
description: El método getProxySettings recupera la configuración del proxy para un protocolo determinado.
ms.assetid: a7b21eab-93e1-458b-aab0-60fd298cce44
keywords:
- método getProxySettings de Windows Media Player
- método getProxySettings Windows Media Player, clase de red
- Clase de red Windows Media Player, método getProxySettings
topic_type:
- apiref
api_name:
- Network.getProxySettings
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 44a306fca1e671e7e5b3a89c0da952e5c81ba20e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649845"
---
# <a name="networkgetproxysettings-method"></a>Network. getProxySettings (método)

El método **getProxySettings** recupera la configuración del proxy para un protocolo determinado.

## <a name="syntax"></a>Sintaxis


```JScript
retVal = Network.getProxySettings(
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

Este método devuelve un **número** (**Long**) que contiene uno de los valores siguientes.



| Value | Descripción                                                                      |
|-------|----------------------------------------------------------------------------------|
| 0     | No se utiliza un servidor proxy.                                                |
| 1     | Se está usando la configuración de proxy del explorador actual (solo es válida para HTTP). |
| 2     | Se usa la configuración de proxy especificada manualmente.                            |
| 3     | La configuración de proxy se detecta automáticamente.                                      |



 

## <a name="remarks"></a>Observaciones

Este método produce un error a menos que la aplicación que realiza la llamada se ejecute en el equipo local o en la intranet.

**Windows Media Player 10 Mobile:** Este método no se admite.

## <a name="examples"></a>Ejemplos

En el siguiente ejemplo de JScript se usa *Network*. **getProxySettings** para mostrar un mensaje que proporciona información sobre la configuración del proxy actual del reproductor, en la ventana del explorador. El objeto **Player** se creó con ID = "Player".


```JScript
// Retrieve a number representing the current proxy settings.
var proxySetting = Player.network.getProxySettings("MMS");

// Display the message the corresponds to the current settings.
switch(proxySetting){

   case 0:
     document.write("A proxy server is not being used");
     break;

   case 1: 
     document.write("The proxy settings for the current browser are being used.");
     break;

   case 2:
     document.write("The manually specified proxy settings are being used.");
     break;

case 3:
     document.write("The proxy settings are being auto-detected.");
     break;

   default:
     document.write("Unable to determine proxy setting, try again.");
}

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

 

 





