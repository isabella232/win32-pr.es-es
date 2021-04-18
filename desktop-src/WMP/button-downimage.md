---
title: BUTTON. downImage
description: El atributo downImage especifica o recupera la imagen que representa el estado inactivo del botón.
ms.assetid: 18149668-5be6-4b64-8adf-8904585ff0be
keywords:
- BUTTON. downImage Windows Media Player
topic_type:
- apiref
api_name:
- BUTTON.downImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca7a405a5df20a04ae9d093f2b28ee4c68cab67d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698614"
---
# <a name="buttondownimage"></a>BUTTON. downImage

El atributo **downImage** especifica o recupera la imagen que representa el estado inactivo del **botón**.

``` syntax
        elementID.downImage
```

## <a name="possible-values"></a>Valores posibles

Este atributo es una **cadena** de lectura/escritura que contiene el nombre del archivo de imagen.

## <a name="remarks"></a>Observaciones

Los formatos de imagen admitidos son BMP, JPG, PNG y GIF.

La imagen predeterminada es la especificada en el atributo de **imagen** o su valor predeterminado.

Si la imagen hacia abajo es mayor que la región definida en el atributo ambiente, se recortará la imagen hacia abajo.

Si no se puede recuperar la imagen, se muestra una imagen predeterminada (la imagen roja x).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------|
| Versión<br/> | Windows Media Player versión 7,0 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Elemento BUTTON**](button-element.md)
</dt> <dt>

[**BOTÓN. abajo**](button-down.md)
</dt> <dt>

[**BOTÓN. imagen**](button-image.md)
</dt> </dl>

 

 





