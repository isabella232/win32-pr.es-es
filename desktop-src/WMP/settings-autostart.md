---
title: Configuración.autoStart
description: La propiedad autoStart especifica o recupera un valor que indica si el elemento multimedia actual comienza a reproducirse automáticamente.
ms.assetid: 553f8534-9e3e-4fdc-bfc1-551939969289
keywords:
- Configuración.autoStart Reproductor de Windows Media
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
ms.openlocfilehash: 93a12d8cf63fdf4d9652bf895f9110e233fb3f3665314e81a9d5aa5c6e1516b8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120123105"
---
# <a name="settingsautostart"></a>Configuración.autoStart

La **propiedad autoStart** especifica o recupera un valor que indica si el elemento multimedia actual comienza a reproducirse automáticamente.

## <a name="syntax"></a>Syntax

player.settings.autoStart

## <a name="possible-values"></a>Valores posibles

Esta propiedad es un booleano de lectura **y escritura.**



| Value | Descripción                                                         |
|-------|---------------------------------------------------------------------|
| true  | Predeterminada. El elemento multimedia comienza a reproducirse automáticamente (vea Comentarios). |
| false | El elemento multimedia no comienza a reproducirse automáticamente.                |



 

## <a name="remarks"></a>Comentarios

Si **autoStart está** establecido en true, el elemento multimedia comenzará a reproducirse cuando *el reproductor .* **DIRECCIÓN URL,** *Player*. **currentPlaylist** o *Player*. **currentMedia** está establecido. De lo contrario, no se iniciará la reproducción hasta que *se controle*. Se llama al método **play.**

Dado que la **propiedad autoStart** para el modo completo de Reproductor de Windows Media se puede establecer globalmente mediante eventos externos (como cargar un CD), no hay ningún valor predeterminado confiable para máscaras y controles remotos del reproductor. Esto se debe a que el motor de reproducción del reproductor en modo completo se usa en ambos casos.

Debe establecer **autoStart en** false inmediatamente antes de establecer *Player*. **DIRECCIÓN URL,** *Player*. **currentPlaylist** o *Player*. **currentMedia** en máscaras y controles Reproductor de Windows Media remoto si desea asegurarse de que el elemento multimedia no se empieza a reproducir inmediatamente. Además, a menos que establezca **inicio** automático en true inmediatamente antes de especificar un elemento multimedia, no debe confiar en esta configuración como sustituto del uso de *los controles*. **método play.**

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se crea un elemento HTML CHECKBOX que permite al usuario especificar si el control Player reproduce automáticamente el elemento multimedia actual. El **objeto Player** se creó con id. = "Player".


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
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Player.currentMedia**](player-currentmedia.md)
</dt> <dt>

[**Player.URL**](player-url.md)
</dt> <dt>

[**Configuración Objeto**](settings-object.md)
</dt> </dl>

 

 





