---
title: Atributos con varios valores (SDK de Windows Media Player)
description: Atributos con varios valores
ms.assetid: 8405481c-47f5-4752-9dab-d3c84711fbb4
keywords:
- Windows Media Player, atributos para elementos multimedia
- Modelo de objetos de Windows Media Player, atributos para elementos multimedia
- modelo de objetos, atributos para elementos multimedia
- Windows Media Player Mobile, atributos para elementos multimedia
- Control ActiveX de Windows Media Player, atributos para elementos multimedia
- Control ActiveX móvil de Windows Media Player, atributos para elementos multimedia
- Control ActiveX, atributos para elementos multimedia
- Biblioteca de Media Player de Windows, atributos para elementos multimedia
- Biblioteca, atributos para elementos multimedia
- atributos, varios valores
- varios valores de atributo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad93c4025d09a234b1834a32e4ca3789bcaa4a35
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104421843"
---
# <a name="attributes-with-multiple-values-windows-media-player-sdk"></a>Atributos con varios valores (SDK de Windows Media Player)

Algunos atributos de elemento multimedia pueden tener varios valores. Por ejemplo, los atributos **Author**, **WM/Composer** y **WM/Genre** pueden tener más de un valor. El tipo de datos de estos atributos es **una cadena multivalor**.

En Windows Media Player, la biblioteca muestra varios valores en un único campo, separando los valores con puntos y comas. Sin embargo, cada valor es en realidad un atributo independiente en el elemento de Windows Media.

Puede escribir código que determine si un atributo determinado tiene varios valores y, a continuación, recupere todos esos valores. Debe usar *medios*. **getItemInfoByType**. Si utiliza los *medios*. método **getItemInfo** para recuperar un atributo con varios valores, solo se recuperará el primer valor.

En el ejemplo final del tema [leer valores de atributo](reading-attribute-values.md) se muestra el uso de los *medios*. **getAttributeCountByType** y *multimedia*. métodos **getItemInfoByType** para recuperar varios valores para un atributo determinado.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Atributos de elemento multimedia**](media-item-attributes.md)
</dt> <dt>

[**Objeto multimedia**](media-object.md)
</dt> <dt>

[**Leer valores de atributo de un CD o DVD**](reading-attribute-values-from-a-cd-or-dvd.md)
</dt> </dl>

 

 




