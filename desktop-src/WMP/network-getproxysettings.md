---
title: Método Network.getProxySettings
description: El método getProxySettings recupera la configuración de proxy para un protocolo determinado.
ms.assetid: a7b21eab-93e1-458b-aab0-60fd298cce44
keywords:
- Método getProxySettings Reproductor de Windows Media
- Método getProxySettings Reproductor de Windows Media , clase Network
- Clase de red Reproductor de Windows Media método , getProxySettings
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
ms.openlocfilehash: e142e7366c9e2b03e55dbd3768ee9c4fb41f30266d221a2ac5ac80019d5a7b3e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119647445"
---
# <a name="networkgetproxysettings-method"></a>Método Network.getProxySettings

El **método getProxySettings** recupera la configuración de proxy para un protocolo determinado.

## <a name="syntax"></a>Sintaxis


```JScript
retVal = Network.getProxySettings(
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

Este método devuelve un **valor Number** (**long**) que contiene uno de los valores siguientes.



| Valor | Descripción                                                                      |
|-------|----------------------------------------------------------------------------------|
| 0     | No se usa un servidor proxy.                                                |
| 1     | Se está utilizando la configuración de proxy para el explorador actual (solo es válida para HTTP). |
| 2     | Se usa la configuración de proxy especificada manualmente.                            |
| 3     | La configuración del proxy se detecta automáticamente.                                      |



 

## <a name="remarks"></a>Comentarios

Se produce un error en este método a menos que la aplicación que realiza la llamada se ejecute en el equipo local o intranet.

**Reproductor de Windows Media 10 Mobile:** No se admite este método.

## <a name="examples"></a>Ejemplos

En el ejemplo JScript siguiente se usa *Network*. **getProxySettings** para mostrar un mensaje, que proporciona información sobre la configuración de proxy actual del reproductor, en la ventana del explorador. El **objeto Player** se creó con id. = "Player".


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



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Objeto de red**](network-object.md)
</dt> </dl>

 

 





