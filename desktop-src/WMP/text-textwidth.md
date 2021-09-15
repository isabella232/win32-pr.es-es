---
title: TEXT.textWidth
description: El atributo textWidth recupera el ancho en píxeles del texto contenido en el atributo value.
ms.assetid: 46c34659-f441-467c-8846-45785f7a2736
keywords:
- TEXT.textWidth Reproductor de Windows Media
topic_type:
- apiref
api_name:
- TEXT.textWidth
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17ce93517837aecf737336137df3cf5d8bf292dd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127467925"
---
# <a name="texttextwidth"></a>TEXT.textWidth

El **atributo textWidth** recupera el ancho en píxeles del texto contenido en el **atributo value.**

``` syntax
        elementID.textWidth
```

## <a name="possible-values"></a>Valores posibles

Este atributo es un número de solo **lectura** (**int**).

## <a name="remarks"></a>Observaciones

El valor devuelto se basa en los atributos **fontFace**, **fontSize** y **fontStyle,** así como en los caracteres reales de la cadena **de** atributo value.

Vea el [atributo value](text-value.md) para obtener un ejemplo que ilustra cómo se usan los atributos del **elemento TEXT.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Elemento TEXT**](text-element.md)
</dt> <dt>

[**TEXT.fontFace**](text-fontface.md)
</dt> <dt>

[**TEXT.fontSize**](text-fontsize.md)
</dt> <dt>

[**TEXT.fontStyle**](text-fontstyle.md)
</dt> <dt>

[**TEXT.value**](text-value.md)
</dt> </dl>

 

 





