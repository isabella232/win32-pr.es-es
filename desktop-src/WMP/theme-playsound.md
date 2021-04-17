---
title: THEME. playSound
description: El método playSound reproduce el archivo de sonido especificado.
ms.assetid: 42675a66-0139-4e74-9abe-1b42017fc6fe
keywords:
- Media Player de Windows THEME. playSound
topic_type:
- apiref
api_name:
- THEME.playSound
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8ceb30e5c47632a1358262019124fceae056294d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690451"
---
# <a name="themeplaysound"></a>THEME. playSound

El método **playSound** reproduce el archivo de sonido especificado.

``` syntax
        theme.playSound(soundFile)
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="soundFile"></span><span id="soundfile"></span><span id="SOUNDFILE"></span>*soundFile*
</dt> <dd>

**Cadena** que especifica el nombre del archivo de sonido que se va a reproducir.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Este método permite agregar efectos de sonido a una máscara, por ejemplo, cuando se hace clic en los botones. El sistema operativo reproduce el sonido directamente y no lo hace Windows Media Player. Esto significa que no se puede controlar el sonido con los métodos y la configuración de Windows Media Player, pero se puede reproducir mientras Windows Media Player está reproduciendo otro archivo multimedia digital.

Este método solo admite archivos WAV.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------|
| Versión<br/> | Windows Media Player 9 series o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Elemento THEME**](theme-element.md)
</dt> </dl>

 

 





