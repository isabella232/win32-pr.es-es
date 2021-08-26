---
title: THEME.playSound
description: El método play Sound reproduce el archivo de sonido especificado.
ms.assetid: 42675a66-0139-4e74-9abe-1b42017fc6fe
keywords:
- THEME.playSound Reproductor de Windows Media
topic_type:
- apiref
api_name:
- THEME.playSound
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e9e6ac0cb7bdf4f8951bafbc89a0a41bf368afcd1021666eb7875739d1cd912e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120001755"
---
# <a name="themeplaysound"></a>THEME.playSound

El **método playSound** reproduce el archivo de sonido especificado.

``` syntax
        theme.playSound(soundFile)
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="soundFile"></span><span id="soundfile"></span><span id="SOUNDFILE"></span>*soundFile*
</dt> <dd>

Cadena **que** especifica el nombre del archivo de sonido que se reproducirá.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Este método permite agregar efectos de sonido a una máscara, por ejemplo, cuando se hace clic en los botones. El sistema operativo reproduce el sonido directamente y no Reproductor de Windows Media. Esto significa que el sonido no se puede controlar con Reproductor de Windows Media y métodos, pero se puede reproducir mientras Reproductor de Windows Media está reproduciendo otro archivo multimedia digital.

Este método solo admite archivos WAV.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media serie 9 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ELEMENTO THEME**](theme-element.md)
</dt> </dl>

 

 





