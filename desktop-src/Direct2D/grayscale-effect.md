---
title: Efecto de escala de grises
description: Convierte una imagen a gris monocromático.
ms.assetid: 4e0b26ed-ba71-5f8f-db1e-f1b4e28fbd11
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03b74e553074b3ee0c9ad4e0d5121b9b084884ddb030c75308eb9964531fc6b7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119075343"
---
# <a name="grayscale-effect"></a>Efecto de escala de grises

Convierte una imagen a gris monocromático.

La escala de grises usa el efecto de matriz de colores para convertir a escala de grises, mediante la siguiente matriz:

![Matriz de conversión](images/grayscale-effect-matrix.png)

El CLSID para este efecto es CLSID \_ D2D1Grayscale.

-   [Imagen de ejemplo](#example-image)
-   [Propiedades de efecto](#effect-properties)
-   [Requisitos](#requirements)
-   [Temas relacionados](#related-topics)

## <a name="example-image"></a>Imagen de ejemplo

![ejemplo de salida de efecto](images/grayscale-effect.png)

## <a name="effect-properties"></a>Propiedades de efecto

Este efecto no tiene propiedades.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------------|---------------------------------------------------|
| Cliente mínimo compatible | \[Windows 10 aplicaciones de escritorio \| Windows store\] |
| Servidor mínimo compatible | \[Windows 10 aplicaciones de escritorio \| Windows store\] |
| Header                   | d2d1effects \_ 2.h                                  |
| Biblioteca                  | d2d1.lib, dxguid.lib                              |


## <a name="related-topics"></a>Temas relacionados

* [Interfaz ID2D1Effect](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
