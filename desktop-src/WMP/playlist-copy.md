---
title: Lista de reproducción. copia
description: El método de copia inicia una operación de copia desde el CD.
ms.assetid: 7d919ae5-456b-4cb9-ad52-9396f5c867d6
keywords:
- Lista de reproducción. copiar Media Player de Windows
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708864"
---
# <a name="playlistcopy"></a>Lista de reproducción. copia

El método de **copia** inicia una operación de copia desde el CD.

``` syntax
        elementID.copy()
```

## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Este método solo copia los elementos activados en la lista de reproducción y funciona de la misma manera que en el panel **Copiar desde CD** en el modo completo de Windows Media Player. Para que este método funcione, debe haber un CD en la unidad de CD. Establezca el atributo **checkboxesVisible** en true para permitir que los usuarios seleccionen elementos individuales en un CD antes de la copia.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------|
| Versión<br/> | Windows Media Player versión 7,0 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Elemento PLAYLIST**](playlist-element.md)
</dt> <dt>

[**Lista de reproducción. abortCopy**](playlist-abortcopy.md)
</dt> <dt>

[**Lista de reproducción. copiando**](playlist-copying.md)
</dt> </dl>

 

 





