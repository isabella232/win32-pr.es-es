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
ms.openlocfilehash: f1c24de6af571eec948a92f666a76df6b65187c6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127359513"
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

## <a name="remarks"></a>Observaciones

Este método copia solo los elementos activados en la lista de reproducción y funciona de la misma manera que en el panel Copiar desde **CD** en el modo completo de Reproductor de Windows Media. Para que este método funcione, un CD debe estar en la unidad de CD. Establezca el **atributo checkboxesVisible** en true para permitir a los usuarios seleccionar elementos individuales en un CD antes de copiarlos.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ELEMENTO PLAYLIST**](playlist-element.md)
</dt> <dt>

[**PLAYLIST.abortCopy**](playlist-abortcopy.md)
</dt> <dt>

[**PLAYLIST.copying**](playlist-copying.md)
</dt> </dl>

 

 





