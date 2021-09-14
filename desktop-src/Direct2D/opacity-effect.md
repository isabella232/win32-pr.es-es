---
title: Efecto de opacidad
description: Este efecto ajusta la opacidad de una imagen multiplicando el canal alfa de la entrada por el valor de opacidad especificado. Tiene una sola entrada.
ms.assetid: a4995228-e08f-b543-0af1-e0eedfe8ecb2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfdc12aa8545f2742561490a3ddce799d6a1aa62
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127162670"
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
| Encabezado                   | d2d1effects \_ 2.h                                  |
| Biblioteca                  | d2d1.lib, dxguid.lib                              |


## <a name="related-topics"></a>Temas relacionados

* [Interfaz ID2D1Effect](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
