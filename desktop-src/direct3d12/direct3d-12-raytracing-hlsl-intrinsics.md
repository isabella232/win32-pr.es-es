---
title: Funciones intrínsecas de HLSL de Direct3D 12 Raytracing
description: Los siguientes sombreadores HLSL admiten la canalización raytracing de Direct3D 12.
ms.assetid: ''
ms.localizationpriority: low
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b2e7cc7053705bd66b37d91f3ee06a6a1f249a2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105714189"
---
# <a name="raytracing-hlsl-intrinsics"></a>Intrínsecos de HLSL raytracing

Las siguientes funciones intrinisc de HLSL admiten la canalización raytracing de Direct3D 12. 

## <a name="in-this-section"></a>En esta sección



| Tema | Descripción |
|-|-|
| [**Función AcceptHitAndEndSearch**](accepthitandendsearch-function.md) | Se usa en cualquier sombreador de posicionamiento para confirmar el acierto actual y, a continuación, detener la búsqueda de más visitas para el rayo. |
| [**Función CallShader**](callshader-function.md) | Invoca otro sombreador desde dentro de un sombreador. |
| [**Función IgnoreHit**](ignorehit-function.md) | Se llama desde un sombreador de posicionamiento cualquiera para rechazar el acierto y finalizar el sombreador. |
| [**PrimitiveIndex función)**](primitiveindex.md) | Recupera el índice generado automáticamente de la primitiva dentro de la geometría dentro de la instancia de la estructura de aceleración de nivel inferior. |
| [**Función ReportHit**](reporthit-function.md) | Lo llama un sombreador de intersección para notificar una intersección de rayo. |
| [**Función TraceRay**](traceray-function.md) | Envía un rayo en una búsqueda de aciertos en una estructura de aceleración. |

## <a name="related-topics"></a>Temas relacionados

* [Referencia básica](direct3d-12-core-reference.md)
* [Referencia de Direct3D 12](direct3d-12-reference.md)
