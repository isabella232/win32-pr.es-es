---
description: Marcas de capacidad de coordenadas de textura del controlador.
ms.assetid: b15509b4-7db1-429a-9468-be7a11dee505
title: D3DTSS_TCI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4973e045decd393be2f8a6d340f369761a411a44
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000777"
---
# <a name="d3dtss_tci"></a>D3DTSS \_ TCI

Marcas de capacidad de coordenadas de textura del controlador.



|                                          |             |                                                                                                                                                                                                                      |
|------------------------------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \#define                                 | Value       | Descripción                                                                                                                                                                                                          |
| D3DTSS \_ TCI \_ PASSTHRU                    | 0x00000000L | Usar las coordenadas de textura especificadas contenidas en el formato de vértices. Este valor se resuelve como cero.                                                                                                               |
| D3DTSS \_ TCI \_ CAMERASPACENORMAL           | 0x00010000L | Use el vértice normal, transformado en el espacio de la cámara, como coordenadas de textura de entrada para la transformación de textura de esta fase.                                                                                        |
| D3DTSS \_ TCI \_ CAMERASPACEPOSITION         | 0x00020000L | Use la posición del vértice, transformada en el espacio de la cámara, como coordenadas de textura de entrada para la transformación de textura de esta fase.                                                                                      |
| D3DTSS \_ TCI \_ CAMERASPACEREFLECTIONVECTOR | 0x00030000L | Use el vector de reflexión, transformado en el espacio de la cámara, como la coordenada de textura de entrada para la transformación de textura de esta fase. El vector de reflexión se calcula a partir de la posición del vértice de entrada y del vector normal. |
| D3DTSS \_ TCI \_ SPHEREMAP                   | 0x00040000L | Usar las coordenadas de textura especificadas para la asignación de esferas.                                                                                                                                                            |



 

D3DTSS TEXCOORDINDEX usa estas constantes \_ .

## <a name="constant-information"></a>Información constante



|                          |            |
|--------------------------|------------|
| Encabezado                   | d3d9caps. h |
| Sistema operativo mínimo | Windows 98 |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Constantes de Direct3D](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 



