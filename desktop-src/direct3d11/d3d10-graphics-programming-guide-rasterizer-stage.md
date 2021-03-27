---
title: Etapa del rasterizador
description: La fase de rasterización convierte información de vectores (formada por formas o primitivas) en una imagen de trama (compuesta de píxeles) con el fin de mostrar gráficos 3D en tiempo real.
ms.assetid: efd3f819-7c63-4e1a-9923-8e7198354ec6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e746c5ace3512f36f9b9ad34d34a3ea578e1de36
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/04/2020
ms.locfileid: "103995762"
---
# <a name="rasterizer-stage"></a>Etapa del rasterizador

La fase de rasterización convierte información de vectores (formada por formas o primitivas) en una imagen de trama (compuesta de píxeles) con el fin de mostrar gráficos 3D en tiempo real.

Durante la rasterización, cada primitiva se convierte en píxeles, mientras que los valores de cada vértice se interpolan en cada primitiva. La rasterización incluye vértices de recorte para el frustum de la vista, que realiza una división por z para proporcionar perspectiva, asignar primitivos a una ventanilla 2D y determinar cómo invocar el sombreador de píxeles. Aunque el uso de un sombreador de píxeles es opcional, la fase de rasterizador siempre realiza el recorte, una división de perspectiva para transformar los puntos en un espacio homogéneo y asigna los vértices a la ventanilla.

Se supone que los vértices (x, y, z, w) que entran en la fase de rasterizador están en el espacio de recorte homogéneo. En este espacio de coordenadas, el eje X apunta hacia la derecha, y apunta hacia arriba y a la Z.

Puede deshabilitar la rasterización indicando a la canalización que no hay ningún sombreador de píxeles (establezca la fase del sombreador de píxeles en **null** con [**ID3D11DeviceContext::P ssetshader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-pssetshader)) y deshabilite la prueba de profundidad y estarcido (establezca **DepthEnable** y **StencilEnable** en **false** en [**D3D11 \_ Depth \_ estarcido \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencil_desc)). Mientras estén deshabilitadas, los contadores de la canalización relacionados con la rasterización no se actualizarán. También hay una descripción completa de las [reglas de rasterización](d3d10-graphics-programming-guide-rasterizer-stage-rules.md).

En el hardware que implementa las optimizaciones jerárquicas del búfer Z, puede habilitar la carga previa del búfer z Si establece la fase del sombreador de píxeles en **null** mientras habilita las pruebas de profundidad y estarcido.


## <a name="in-this-section"></a>En esta sección



| Tema                                                                                                                         | Descripción                                                                                                                                                                                                                                                                                                              |
|-------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Introducción con la fase de rasterizador](d3d10-graphics-programming-guide-rasterizer-stage-getting-started.md)<br/> | En esta sección se describe la configuración de la ventanilla, el rectángulo de tijeras, el estado de rasterizador y el muestreo múltiple.<br/>                                                                                                                                                                                                |
| [Reglas de rasterización](d3d10-graphics-programming-guide-rasterizer-stage-rules.md)<br/>                                 | Las reglas de rasterización definen cómo se asignan los datos vectoriales a los datos de tramas. Los datos de trama se ajustan a las ubicaciones de enteros que se seleccionan y recortan (para dibujar el número mínimo de píxeles), y los atributos por píxel se interpolan (a partir de los atributos por vértice) antes de que se pasen a un sombreador de píxeles.<br/> |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Canalización de gráficos](overviews-direct3d-11-graphics-pipeline.md)
</dt> <dt>

[Fases de canalización (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-pipeline-stages)
</dt> </dl>

 

