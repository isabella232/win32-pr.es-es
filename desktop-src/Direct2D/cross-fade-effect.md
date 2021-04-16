---
title: Efecto de atenuación cruzada
description: Este efecto combina dos imágenes mediante la adición de píxeles ponderados de las imágenes de entrada. Tiene dos entradas, denominadas destino y origen.
ms.assetid: 5214b70a-d024-ba3e-771f-07d98d2278ba
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 904ac8e4e27efc646bb71b1766c8763bd64beb2d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534114"
---
# <a name="cross-fade-effect"></a>Efecto de atenuación cruzada

Este efecto combina dos imágenes mediante la adición de píxeles ponderados de las imágenes de entrada. Tiene dos entradas, denominadas destino y origen.

La fórmula de atenuación cruzada es **salida = destino de peso \* + (1-peso) \* origen**.

El CLSID para este efecto es CLSID \_ D2D1CrossFade.

## <a name="effect-properties"></a>Propiedades del efecto

| Enumeración de índice y nombre para mostrar             | Tipo y valor predeterminado | Descripción                                                                                                                                                                                                                                                       |
|------------------------------------------------|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Peso de la WeightD2D1 con \_ fundido cruzado \_ \_<br/> | FLOAT 0.5 f<br/>   | Cuántos pesan los valores de color de la imagen de origen frente a la imagen de destino. El valor mínimo es 0.0 f (usar exclusivamente la imagen de destino para determinar el resultado) y el valor máximo es 1.0 f (usar exclusivamente la imagen de origen para determinar la salida). |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------------|---------------------------------------------------|
| Cliente mínimo compatible | Aplicaciones de la tienda Windows de Windows 10 \[ Desktop apps \|\] |
| Servidor mínimo compatible | Aplicaciones de la tienda Windows de Windows 10 \[ Desktop apps \|\] |
| Encabezado                   | d2d1effects \_ 2. h                                  |
| Biblioteca                  | d2d1. lib, dxguid. lib                              |

## <a name="related-topics"></a>Temas relacionados

* [Interfaz ID2D1Effect](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
