---
title: Settings. defaultFrame
description: La propiedad defaultFrame especifica o recupera el nombre del marco que se usa para mostrar una dirección URL que se recibe en un evento comando.
ms.assetid: c2edb253-a545-4820-85aa-8fb7badf4d81
keywords:
- Settings. defaultFrame Windows Media Player
topic_type:
- apiref
api_name:
- Settings.defaultFrame
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6182a635e4bd73a946c3cf85efb7d39966c0007
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649811"
---
# <a name="settingsdefaultframe"></a>Settings. defaultFrame

La propiedad **defaultFrame** especifica o recupera el nombre del marco que se usa para mostrar una dirección URL que se recibe en un evento **comando** .

## <a name="syntax"></a>Sintaxis

Player. Settings. defaultFrame

## <a name="possible-values"></a>Valores posibles

Esta propiedad es una **cadena** de lectura/escritura que corresponde al valor del atributo **Name** del elemento de marco de destino.

## <a name="remarks"></a>Observaciones

Si se especifica un marco de destino en el propio evento **comando** , se omite esta propiedad.

Esta propiedad se omite cuando se usa el applet Java de Netscape Navigator. En el navegador, cada comando de script de dirección URL recibido muestra la dirección URL en una nueva ventana del explorador, independientemente del valor de *configuración*. **defaultFrame**.

**Windows Media Player 10 Mobile**: esta propiedad es de solo lectura y siempre devuelve una cadena vacía.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Windows Media Player versión 7,0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Evento Player. comando**](player-player-scriptcommand.md)
</dt> <dt>

[**Objeto de configuración**](settings-object.md)
</dt> <dt>

[**Uso del Reproductor de Windows Media con Netscape 7.1**](using-windows-media-player-with-netscape-7-1.md)
</dt> </dl>

 

 





