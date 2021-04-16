---
title: Description (atributo, WMP SDK)
description: El atributo Description es una descripción del contenido.
ms.assetid: 8bf76bf5-2bba-4ceb-bc98-f8b8ab2c8b6f
keywords:
- Media Player atributo de descripción de Windows
topic_type:
- apiref
api_name:
- Description
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78c4bc3562e7b807dc0e333c887aad1550d05b0b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699425"
---
# <a name="description-attribute"></a>Descripción (atributo)

El atributo **Description** es una descripción del contenido.

## <a name="applies-to"></a>Se aplica a

-   [Archivos de música](music-file-attributes.md)

## <a name="remarks"></a>Observaciones

Este atributo se almacena en archivos de música, no en la biblioteca.

Este atributo puede tener varios valores. Para recuperar todos los valores de un atributo con varios valores, debe utilizar los *medios*. método **getItemInfoByType** , no el método *media*. getItemInfo.

La constante del SDK de Windows Media Format para este atributo es g \_ wszWMDescription.

Para determinar si puede cambiar el valor de este atributo, use el método [media. isReadOnlyItem](media-isreadonlyitem.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------|
| Versión<br/> | Windows Media Player 9 series o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Referencia de atributo**](attribute-reference.md)
</dt> </dl>

 

 





