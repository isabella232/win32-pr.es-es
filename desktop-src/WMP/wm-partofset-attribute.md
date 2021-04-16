---
title: Atributo WM/PartOfSet
description: El atributo WM/PartOfSet es el número de pieza y el número total de partes del conjunto al que pertenece el elemento.
ms.assetid: c6827c31-c625-4283-a50d-f08eccf87271
keywords:
- Media Player de Windows de atributos de WM/PartOfSet
topic_type:
- apiref
api_name:
- WM/PartOfSet
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c27d6297931c503c95c8ef0462bf7b119a0ffb75
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718924"
---
# <a name="wmpartofset-attribute"></a>Atributo WM/PartOfSet

El atributo **WM/PartOfSet** es el número de pieza y el número total de partes del conjunto al que pertenece el elemento.

## <a name="applies-to"></a>Se aplica a

-   [Archivos de música](music-file-attributes.md)

## <a name="remarks"></a>Observaciones

Este atributo solo se almacena en un archivo de música que no está en la biblioteca.

La constante del SDK de Windows Media Format para este atributo es g \_ wszWMPartOfSet.

Para determinar si puede cambiar el valor de este atributo, use el método [media. isReadOnlyItem](media-isreadonlyitem.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------|
| Versión<br/> | Windows Media Player 9 series o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Referencia de atributo**](attribute-reference.md)
</dt> </dl>

 

 





