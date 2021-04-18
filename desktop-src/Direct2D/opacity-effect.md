---
title: Efecto opacidad
description: Este efecto ajusta la opacidad de una imagen multiplicando el canal alfa de la entrada por el valor de opacidad especificado. Tiene una sola entrada.
ms.assetid: a4995228-e08f-b543-0af1-e0eedfe8ecb2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfdc12aa8545f2742561490a3ddce799d6a1aa62
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686092"
---
# <a name="opacity-effect"></a>Efecto opacidad

Este efecto ajusta la opacidad de una imagen multiplicando el canal alfa de la entrada por el valor de opacidad especificado. Tiene una sola entrada.

El CLSID para este efecto es CLSID \_ D2D1Opacity.

## <a name="effect-properties"></a>Propiedades del efecto



| Enumeración de índice y nombre para mostrar              | Tipo y valor predeterminado | Descripción                                                                                                 |
|-------------------------------------------------|------------------------|-------------------------------------------------------------------------------------------------------------|
| Opacidad D2D1 opacidad opacidad \_ \_ prop. \_<br/> | FLOAT 1.0 f<br/>   | Multiplicador del canal alfa de la imagen de entrada. El valor mínimo es 0,0 f y el valor máximo es 1,0 f. |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------------|---------------------------------------------------|
| Cliente mínimo compatible | Aplicaciones de la tienda Windows de Windows 10 \[ Desktop apps \|\] |
| Servidor mínimo compatible | Aplicaciones de la tienda Windows de Windows 10 \[ Desktop apps \|\] |
| Encabezado                   | d2d1effects \_ 2. h                                  |
| Biblioteca                  | d2d1. lib, dxguid. lib                              |


## <a name="related-topics"></a>Temas relacionados

* [Interfaz ID2D1Effect](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
