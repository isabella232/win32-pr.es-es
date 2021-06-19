---
title: Funciones intrínsecas de HLSL de Direct3D 12 Raytracing
description: Vea vínculos a artículos que describen funciones intrínsecas del lenguaje de sombreador de alto nivel (HLSL) que admiten la canalización de rayos de Direct3D 12.
ms.assetid: ''
ms.localizationpriority: low
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06687866354611f44f295ff4fe2cf171068e83c3
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396480"
---
# <a name="raytracing-hlsl-intrinsics"></a>Funciones intrínsecas de HLSL de raytracing

Las siguientes funciones intrinisc hlsl admiten la canalización de raytracing de Direct3D 12. 

## <a name="in-this-section"></a>En esta sección



| Tema | Descripción |
|-|-|
| [**Función AcceptHitAndEndSearch**](accepthitandendsearch-function.md) | Se usa en cualquier sombreador de aciertos para confirmar el acierto actual y, a continuación, dejar de buscar más aciertos para el rayo. |
| [**Función CallShader**](callshader-function.md) | Invoca otro sombreador desde dentro de un sombreador. |
| [**Función IgnoreHit**](ignorehit-function.md) | Se llama desde cualquier sombreador de llamadas para rechazar el objeto hit y finalizar el sombreador. |
| [**Función PrimitiveIndex**](primitiveindex.md) | Recupera el índice generado automáticamente de la primitiva dentro de la geometría dentro de la instancia de la estructura de aceleración de nivel inferior. |
| [**Función ReportHit**](reporthit-function.md) | Lo llama un sombreador de intersección para notificar una intersección de rayos. |
| [**Función TraceRay**](traceray-function.md) | Envía un rayo a una búsqueda de aciertos en una estructura de aceleración. |

## <a name="related-topics"></a>Temas relacionados

* [Referencia principal](direct3d-12-core-reference.md)
* [Referencia de Direct3D 12](direct3d-12-reference.md)
