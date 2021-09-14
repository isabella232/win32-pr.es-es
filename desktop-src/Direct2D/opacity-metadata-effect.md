---
title: Efecto de metadatos de opacidad
description: Puede usar este efecto para marcar un área de una imagen de entrada como opaca, por lo que es posible realizar optimizaciones de representación interna en el gráfico.
ms.assetid: 25B34A31-8533-4339-BBF7-2D7E5488E301
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d84d90ba1c4b1186e3e682ec94a0c9c17bdfc73e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127162658"
---
# <a name="opacity-metadata-effect"></a>Efecto de metadatos de opacidad

Puede usar este efecto para marcar un área de una imagen de entrada como opaca, por lo que es posible realizar optimizaciones de representación interna en el gráfico.

> [!Note]  
> Este efecto no modifica la propia imagen para que sea opaca. Modifica los datos asociados a la imagen, por lo que el representador asume que la región especificada es opaca.

 

El CLSID para este efecto es CLSID \_ D2D1OpacityMetadata.

## <a name="effect-properties"></a>Propiedades de efecto



| Enumeración de nombre para mostrar e índice                                                 | Tipo y valor predeterminado                                                             | Descripción                                                                                       |
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| OutputRect<br/> D2D1 \_ OPACITYMETADATA \_ PROP \_ INPUT \_ OPAQUE \_ RECT <br/> | D2D1 \_ VECTOR \_ 4F<br/> (-FLT \_ MAX, -FLT \_ MAX, FLT \_ MAX, FLT \_ MAX) <br/> | Parte de la imagen de origen opaca. El valor predeterminado es toda la imagen de entrada.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible | Windows 8 y actualización de plataforma para Windows 7 aplicaciones \[ de escritorio \| Windows Store\] |
| Servidor mínimo compatible | Windows 8 y actualización de plataforma para Windows 7 aplicaciones \[ de escritorio \| Windows Store\] |
| Encabezado                   | d2d1effects.h                                                                      |
| Biblioteca                  | d2d1.lib, dxguid.lib                                                               |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

