---
title: Atributos con varios valores (Reproductor de Windows Media SDK)
description: Obtenga información sobre los atributos con varios valores en Reproductor de Windows Media SDK. Algunos atributos de elementos multimedia pueden tener varios valores.
ms.assetid: 8405481c-47f5-4752-9dab-d3c84711fbb4
keywords:
- Reproductor de Windows Media,attributes para elementos multimedia
- Reproductor de Windows Media modelo de objetos, atributos para elementos multimedia
- modelo de objetos, atributos para elementos multimedia
- Reproductor de Windows Media Móvil, atributos para elementos multimedia
- Reproductor de Windows Media ActiveX control,atributos para elementos multimedia
- Reproductor de Windows Media Control de ActiveX móviles, atributos para elementos multimedia
- ActiveX control,atributos para elementos multimedia
- Reproductor de Windows Media biblioteca, atributos para elementos multimedia
- library,attributes para elementos multimedia
- attributes,multiple values
- varios valores de atributo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0b029589444525ae3e0ea699cb12c72bcf900b1107556151c01b7b93434a0c4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120098925"
---
# <a name="attributes-with-multiple-values-windows-media-player-sdk"></a>Atributos con varios valores (Reproductor de Windows Media SDK)

Algunos atributos de elementos multimedia pueden tener varios valores. Por ejemplo, los **atributos Author**, **WM/Composer** y **WM/Genre** pueden tener más de un valor. El tipo de datos de estos atributos es **una cadena de varios valores.**

En Reproductor de Windows Media, la biblioteca muestra varios valores en un solo campo, separando los valores con punto y coma. Sin embargo, cada valor es realmente un atributo independiente en el Windows elemento Multimedia.

Puede escribir código que determine si un atributo determinado tiene varios valores y, a continuación, recuperar todos esos valores. Debe usar *Media*. **getItemInfoByType**. Si usa media *.* **Método getItemInfo** para recuperar un atributo de varios valores; solo recuperará el primer valor.

En el ejemplo final del tema [Leer valores de atributo](reading-attribute-values.md) se muestra el uso de *media*. **getAttributeCountByType** y *Media*. **Métodos getItemInfoByType** para recuperar varios valores para un atributo determinado.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Atributos de elementos multimedia**](media-item-attributes.md)
</dt> <dt>

[**Objeto multimedia**](media-object.md)
</dt> <dt>

[**Lectura de valores de atributo desde un CD o DVD**](reading-attribute-values-from-a-cd-or-dvd.md)
</dt> </dl>

 

 




