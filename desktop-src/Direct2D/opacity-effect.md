---
title: Efecto de opacidad
description: Este efecto ajusta la opacidad de una imagen multiplicando el canal alfa de la entrada por el valor de opacidad especificado. Tiene una sola entrada.
ms.assetid: a4995228-e08f-b543-0af1-e0eedfe8ecb2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58073e3b692b45f86f57c61571d81f5add47427c8a1a801ac43121b37aa43a67
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119636235"
---
# <a name="opacity-effect"></a>Efecto de opacidad

Este efecto ajusta la opacidad de una imagen multiplicando el canal alfa de la entrada por el valor de opacidad especificado. Tiene una sola entrada.

El CLSID para este efecto es CLSID \_ D2D1Opacity.

## <a name="effect-properties"></a>Propiedades de efecto



| Enumeración de nombre para mostrar e índice              | Tipo y valor predeterminado | Descripción                                                                                                 |
|-------------------------------------------------|------------------------|-------------------------------------------------------------------------------------------------------------|
| Opacidad D2D1 \_ OPACITY \_ PROP \_ OPACITY<br/> | FLOAT1.0f<br/>   | Multiplicador del canal alfa de la imagen de entrada. El valor mínimo es 0,0f y el valor máximo es 1,0f. |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------------|---------------------------------------------------|
| Cliente mínimo compatible | \[Windows 10 aplicaciones de escritorio \| Windows aplicaciones de la Tienda\] |
| Servidor mínimo compatible | \[Windows 10 aplicaciones de escritorio \| Windows aplicaciones de la Tienda\] |
| Header                   | d2d1effects \_ 2.h                                  |
| Biblioteca                  | d2d1.lib, dxguid.lib                              |


## <a name="related-topics"></a>Temas relacionados

* [Interfaz ID2D1Effect](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
