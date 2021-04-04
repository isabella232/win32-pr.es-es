---
title: Efecto de escala de grises
description: Convierte una imagen a gris monocromático.
ms.assetid: 4e0b26ed-ba71-5f8f-db1e-f1b4e28fbd11
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0dc3cb6a807d282649a2826713cdf48fa966d9f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802629"
---
# <a name="grayscale-effect"></a>Efecto de escala de grises

Convierte una imagen a gris monocromático.

Escala de grises utiliza el efecto de la matriz de colores para convertir a escala de grises mediante la siguiente matriz:

![matriz de conversión](images/grayscale-effect-matrix.png)

El CLSID para este efecto es CLSID \_ D2D1Grayscale.

-   [Imagen de ejemplo](#example-image)
-   [Propiedades del efecto](#effect-properties)
-   [Requisitos](#requirements)
-   [Temas relacionados](#related-topics)

## <a name="example-image"></a>Imagen de ejemplo

![ejemplo de resultado de efecto](images/grayscale-effect.png)

## <a name="effect-properties"></a>Propiedades del efecto

Este efecto no tiene propiedades.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------------|---------------------------------------------------|
| Cliente mínimo compatible | Aplicaciones de la tienda Windows de Windows 10 \[ Desktop apps \|\] |
| Servidor mínimo compatible | Aplicaciones de la tienda Windows de Windows 10 \[ Desktop apps \|\] |
| Encabezado                   | d2d1effects \_ 2. h                                  |
| Biblioteca                  | d2d1. lib, dxguid. lib                              |


## <a name="related-topics"></a>Temas relacionados

* [Interfaz ID2D1Effect](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
