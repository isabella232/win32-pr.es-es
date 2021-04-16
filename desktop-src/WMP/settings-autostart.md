---
title: Configuración. Inicio automático
description: La propiedad autoStart especifica o recupera un valor que indica si el elemento multimedia actual comienza a reproducirse automáticamente.
ms.assetid: 553f8534-9e3e-4fdc-bfc1-551939969289
keywords:
- Configuración. Inicio automático de Windows Media Player
topic_type:
- apiref
api_name:
- Settings.autoStart
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d08b8f84f4a0b51225ed5692a25fa41cab809ad
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649559"
---
# <a name="settingsautostart"></a>Configuración. Inicio automático

La propiedad **autoStart** especifica o recupera un valor que indica si el elemento multimedia actual comienza a reproducirse automáticamente.

## <a name="syntax"></a>Sintaxis

Player. Settings. autoStart

## <a name="possible-values"></a>Valores posibles

Esta propiedad es un **valor booleano** de lectura/escritura.



| Value | Descripción                                                         |
|-------|---------------------------------------------------------------------|
| true  | Predeterminada. El elemento multimedia comienza a reproducirse automáticamente (vea la sección comentarios). |
| false | El elemento multimedia no empieza a reproducirse automáticamente.                |



 

## <a name="remarks"></a>Observaciones

Si **autoStart** se establece en true, el elemento multimedia empezará a reproducirse cuando el *reproductor*. **Dirección URL**, *reproductor*. **currentPlaylist** o *Player*. **currentMedia** está establecido. De lo contrario, no empezará a reproducirse hasta que los *controles*. se llama al método **Play** .

Dado que la propiedad **autoStart** para el modo completo de Windows Media Player se puede establecer globalmente mediante eventos externos (como cargar un CD), no hay ningún valor predeterminado confiable para las máscaras y los controles del reproductor remoto. Esto se debe a que el motor de reproducción del reproductor en modo completo se usa en ambos casos.

Debe establecer **autoStart** en false inmediatamente antes de configurar el *reproductor*. **Dirección URL**, *reproductor*. **currentPlaylist** o *Player*. **currentMedia** en máscaras y controles de Windows Media Player remotos si desea asegurarse de que el elemento multimedia no empiece a reproducirse inmediatamente. Además, a menos que establezca **AutoStart** en true inmediatamente antes de especificar un elemento multimedia, no debe confiar en este valor como sustituto para usar los *controles*. método **Play** .

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se crea un elemento CHECKBOX HTML que permite al usuario especificar si el control Player reproduce automáticamente el elemento multimedia actual. El objeto **Player** se creó con ID = "Player".


```
<!-- Create an HTML CHECKBOX control. -->
<INPUT  TYPE = "CHECKBOX" ID = AS
              onClick = "
    /* Use the CHECKBOX state to specify the value 
       of the autoStart property. */
    Player.settings.autoStart = AS.checked;
"> 

```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Windows Media Player versión 7,0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Player. currentMedia**](player-currentmedia.md)
</dt> <dt>

[**Player. URL**](player-url.md)
</dt> <dt>

[**Objeto de configuración**](settings-object.md)
</dt> </dl>

 

 





