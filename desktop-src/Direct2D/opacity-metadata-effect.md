---
title: Efecto de metadatos de opacidad
description: Puede usar este efecto para marcar un área de una imagen de entrada como opaca, por lo que es posible realizar optimizaciones de representación internas en el gráfico.
ms.assetid: 25B34A31-8533-4339-BBF7-2D7E5488E301
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d84d90ba1c4b1186e3e682ec94a0c9c17bdfc73e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150875"
---
# <a name="opacity-metadata-effect"></a>Efecto de metadatos de opacidad

Puede usar este efecto para marcar un área de una imagen de entrada como opaca, por lo que es posible realizar optimizaciones de representación internas en el gráfico.

> [!Note]  
> Este efecto no modifica la propia imagen para que sea opaca. Modifica los datos asociados a la imagen para que el representador asuma que la región especificada es opaca.

 

El CLSID para este efecto es CLSID \_ D2D1OpacityMetadata.

## <a name="effect-properties"></a>Propiedades del efecto



| Enumeración de índice y nombre para mostrar                                                 | Tipo y valor predeterminado                                                             | Descripción                                                                                       |
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| OutputRect<br/> D2D1 \_ OPACITYMETADATA \_ \_ opaco INPUT \_ \_ <br/> | D2D1 \_ Vector \_ 4F<br/> (-FLT \_ MAX,-FLT \_ Max, FLT \_ Max, FLT \_ Max) <br/> | Parte de la imagen de origen opaca. El valor predeterminado es toda la imagen de entrada.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible | Windows 8 y actualización de la plataforma para aplicaciones de escritorio de Windows 7 aplicaciones de la \[ \| tienda Windows\] |
| Servidor mínimo compatible | Windows 8 y actualización de la plataforma para aplicaciones de escritorio de Windows 7 aplicaciones de la \[ \| tienda Windows\] |
| Encabezado                   | d2d1effects. h                                                                      |
| Biblioteca                  | d2d1. lib, dxguid. lib                                                               |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

