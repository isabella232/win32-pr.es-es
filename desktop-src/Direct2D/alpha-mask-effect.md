---
title: Efecto de máscara alfa
description: Este efecto aplica una máscara alfa a una imagen. Tiene dos entradas, denominadas Destination y Mask. Los valores de color de la imagen de destino se multiplican por el canal alfa de la imagen mask.
ms.assetid: fddad107-ec70-3a24-f4ae-9dc4f3716536
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87669608ab75ab7a655c072e174dbcd19df4bb39
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127164258"
---
# <a name="alpha-mask-effect"></a>Efecto de máscara alfa

Este efecto aplica una máscara alfa a una imagen. Tiene dos entradas, denominadas Destination y Mask. Los valores de color de la imagen de destino se multiplican por el canal alfa de la imagen mask.

El CLSID para este efecto es CLSID \_ D2D1AlphaMask.

## <a name="effect-properties"></a>Propiedades de efecto

Este efecto no tiene propiedades específicas del efecto.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------------|---------------------------------------------------|
| Cliente mínimo compatible | \[Windows 10 aplicaciones de escritorio \| Windows store\] |
| Servidor mínimo compatible | \[Windows 10 aplicaciones de escritorio \| Windows store\] |
| Encabezado                   | d2d1effects \_ 2.h                                  |
| Biblioteca                  | d2d1.lib, dxguid.lib                              |

## <a name="related-topics"></a>Temas relacionados

* [Interfaz ID2D1Effect](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)

