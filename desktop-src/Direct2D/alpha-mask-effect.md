---
title: Efecto de máscara alfa
description: Este efecto aplica una máscara alfa a una imagen. Tiene dos entradas, denominadas Destination y Mask. Los valores de color de la imagen de destino se multiplican por el canal alfa de la imagen de máscara.
ms.assetid: fddad107-ec70-3a24-f4ae-9dc4f3716536
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87669608ab75ab7a655c072e174dbcd19df4bb39
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151246"
---
# <a name="alpha-mask-effect"></a>Efecto de máscara alfa

Este efecto aplica una máscara alfa a una imagen. Tiene dos entradas, denominadas Destination y Mask. Los valores de color de la imagen de destino se multiplican por el canal alfa de la imagen de máscara.

El CLSID para este efecto es CLSID \_ D2D1AlphaMask.

## <a name="effect-properties"></a>Propiedades del efecto

Este efecto no tiene propiedades específicas del efecto.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------------|---------------------------------------------------|
| Cliente mínimo compatible | Aplicaciones de la tienda Windows de Windows 10 \[ Desktop apps \|\] |
| Servidor mínimo compatible | Aplicaciones de la tienda Windows de Windows 10 \[ Desktop apps \|\] |
| Encabezado                   | d2d1effects \_ 2. h                                  |
| Biblioteca                  | d2d1. lib, dxguid. lib                              |

## <a name="related-topics"></a>Temas relacionados

* [Interfaz ID2D1Effect](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)

