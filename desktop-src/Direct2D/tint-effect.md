---
title: Efecto de tono
description: Este efecto marca la imagen de origen multiplicando la imagen de origen por el color especificado. Tiene una sola entrada.
ms.assetid: b0fd3598-26b6-faee-4f10-ebba96241bc8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f12e7593f9cb0695a6adb7b955fb66b13c8d00b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127162534"
---
# <a name="tint-effect"></a>Efecto de tono

Este efecto marca la imagen de origen multiplicando la imagen de origen por el color especificado. Tiene una sola entrada.

El CLSID para este efecto es CLSID \_ D2D1Tint.

## <a name="effect-properties"></a>Propiedades de efecto



| Enumeración de nombre para mostrar e índice                    | Tipo y valor predeterminado                              | Descripción                                                      |
|-------------------------------------------------------|-----------------------------------------------------|------------------------------------------------------------------|
| ColorD2D1 \_ TINT \_ PROP \_ COLOR<br/>               | D2D1 \_ VECTOR \_ 4F(1.0f, 1.0f, 1.0f, 1.0f)<br/> | Los colores de la imagen de origen se multiplican por este valor.       |
| Resultado de la fijación de la fijación de la propiedad de cierreoutputd2D1 \_ TINT \_ \_ \_<br/> | BOOLFALSE<br/>                                | Si se fijan o no los valores de salida en el \[ intervalo 0, 1 \] . |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------------|---------------------------------------------------|
| Cliente mínimo compatible | \[Windows 10 aplicaciones de escritorio \| Windows store\] |
| Servidor mínimo compatible | \[Windows 10 aplicaciones de escritorio \| Windows store\] |
| Encabezado                   | d2d1effects \_ 2.h                                  |
| Biblioteca                  | d2d1.lib, dxguid.lib                              |



 ## <a name="related-topics"></a>Temas relacionados

* [Interfaz ID2D1Effect](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
