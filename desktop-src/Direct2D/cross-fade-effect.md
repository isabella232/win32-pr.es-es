---
title: Efecto de atenuación cruzada
description: Este efecto combina dos imágenes agregando píxeles ponderados a partir de imágenes de entrada. Tiene dos entradas, denominadas Destino y Origen.
ms.assetid: 5214b70a-d024-ba3e-771f-07d98d2278ba
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 904ac8e4e27efc646bb71b1766c8763bd64beb2d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127164166"
---
# <a name="cross-fade-effect"></a>Efecto de atenuación cruzada

Este efecto combina dos imágenes agregando píxeles ponderados a partir de imágenes de entrada. Tiene dos entradas, denominadas Destino y Origen.

La fórmula de atenuación cruzada es **output = weight Destination + \* (1 - weight) \* Source**.

El CLSID para este efecto es CLSID \_ D2D1CrossFade.

## <a name="effect-properties"></a>Propiedades de efecto

| Enumeración de nombre para mostrar e índice             | Tipo y valor predeterminado | Descripción                                                                                                                                                                                                                                                       |
|------------------------------------------------|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| WeightD2D1 \_ CROSSFADE \_ PROP \_ WEIGHT<br/> | FLOAT0.5f<br/>   | Cantidad de peso de los valores de color de la imagen de origen frente a la imagen de destino. El valor mínimo es 0,0f (use exclusivamente la imagen de destino para determinar la salida) y el valor máximo es 1,0f (use exclusivamente la imagen de origen para determinar la salida). |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------------|---------------------------------------------------|
| Cliente mínimo compatible | \[Windows 10 aplicaciones de escritorio \| Windows aplicaciones de la Tienda\] |
| Servidor mínimo compatible | \[Windows 10 aplicaciones de escritorio \| Windows aplicaciones de la Tienda\] |
| Encabezado                   | d2d1effects \_ 2.h                                  |
| Biblioteca                  | d2d1.lib, dxguid.lib                              |

## <a name="related-topics"></a>Temas relacionados

* [Interfaz ID2D1Effect](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
