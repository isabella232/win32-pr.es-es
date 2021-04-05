---
title: Efecto de matiz
description: Este efecto tiñe la imagen de origen multiplicando la imagen de origen por el color especificado. Tiene una sola entrada.
ms.assetid: b0fd3598-26b6-faee-4f10-ebba96241bc8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f12e7593f9cb0695a6adb7b955fb66b13c8d00b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996321"
---
# <a name="tint-effect"></a>Efecto de matiz

Este efecto tiñe la imagen de origen multiplicando la imagen de origen por el color especificado. Tiene una sola entrada.

El CLSID para este efecto es CLSID \_ D2D1Tint.

## <a name="effect-properties"></a>Propiedades del efecto



| Enumeración de índice y nombre para mostrar                    | Tipo y valor predeterminado                              | Descripción                                                      |
|-------------------------------------------------------|-----------------------------------------------------|------------------------------------------------------------------|
| COLOR de la ColorD2D1 de \_ tinte \_ \_<br/>               | D2D1 \_ Vector \_ 4F (1.0 f, 1.0 f, 1.0 f, 1.0 f)<br/> | Los colores de la imagen de origen se multiplican por este valor.       |
| Salida de la abrazadera de propiedades de \_ matiz ClampOutputD2D1 \_ \_ \_<br/> | BOOLFALSE<br/>                                | Indica si se deben fijar o no los valores de salida en el intervalo \[ 0, 1 \] . |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------------|---------------------------------------------------|
| Cliente mínimo compatible | Aplicaciones de la tienda Windows de Windows 10 \[ Desktop apps \|\] |
| Servidor mínimo compatible | Aplicaciones de la tienda Windows de Windows 10 \[ Desktop apps \|\] |
| Encabezado                   | d2d1effects \_ 2. h                                  |
| Biblioteca                  | d2d1. lib, dxguid. lib                              |



 ## <a name="related-topics"></a>Temas relacionados

* [Interfaz ID2D1Effect](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
