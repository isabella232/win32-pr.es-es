---
title: PLAYLIST.copy
description: El método de copia comienza una operación de copia desde el CD.
ms.assetid: 7d919ae5-456b-4cb9-ad52-9396f5c867d6
keywords:
- PLAYLIST.copy Reproductor de Windows Media
topic_type:
- apiref
api_name:
- PLAYLIST.copy
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 07b897d22c1aa8e666c5de40aecb8ef63d17384957e82eee8dc7d569f0e71f57
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120003195"
---
# <a name="playlistcopy"></a>PLAYLIST.copy

El **método de** copia comienza una operación de copia desde el CD.

``` syntax
        elementID.copy()
```

## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Este método copia solo los elementos activados en la lista de reproducción y funciona de la misma manera que en el panel Copiar desde **CD** en el modo completo de Reproductor de Windows Media. Para que este método funcione, un CD debe estar en la unidad de CD. Establezca el **atributo checkboxesVisible** en true para permitir que los usuarios seleccionen elementos individuales en un CD antes de copiar.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Elemento PLAYLIST**](playlist-element.md)
</dt> <dt>

[**PLAYLIST.abortCopy**](playlist-abortcopy.md)
</dt> <dt>

[**PLAYLIST.copying**](playlist-copying.md)
</dt> </dl>

 

 





