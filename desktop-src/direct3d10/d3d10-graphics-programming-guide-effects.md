---
description: Un efecto de DirectX es una colección de estado de canalización, establecida por expresiones escritas en HLSL y alguna sintaxis específica del marco de trabajo de efecto.
ms.assetid: db4c7651-b6a1-4bc3-bcf8-a5cb56c7563e
title: Efectos (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55e08d0c79a6f7f52982a74d5127da70d7b82f84
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677231"
---
# <a name="effects-direct3d-10"></a>Efectos (Direct3D 10)

Un efecto de DirectX es una colección de estado de canalización, establecida por expresiones escritas en [HLSL](../direct3dhlsl/dx-graphics-hlsl-reference.md) y alguna sintaxis específica del marco de trabajo de efecto. Después de compilar un efecto, use las API del marco de trabajo para representar. La funcionalidad de efectos puede abarcar desde algo tan sencillo como un sombreador de vértices que transforma la geometría y un sombreador de píxeles que da como resultado un color sólido, a una técnica de representación que requiere varios pases, usa todas las fases de la canalización de gráficos y manipula el estado del sombreador, así como el estado de la canalización que no está asociado a los sombrea

El primer paso es organizar el estado que desea controlar en un efecto. Esto incluye el estado del sombreador (vértices, sombreados y sombreadores de píxeles), la textura y el estado de muestra que usan los sombreadores y otro estado de canalización no programable. Puede crear un efecto en la memoria como una cadena de texto, pero normalmente el tamaño es lo suficientemente grande como para almacenar el estado del efecto en un archivo de efectos (un archivo de texto que finaliza en una extensión. FX). Para usar un efecto, debe compilarlo (para comprobar la sintaxis de HLSL y la sintaxis del marco de trabajo), inicializar el estado del efecto a través de las llamadas API y modificar el bucle de representación para llamar a las API de representación.

-   [Organización del estado en un efecto](d3d10-graphics-programming-guide-effects-organize.md)
-   [Interfaces del sistema de efectos](d3d10-graphics-programming-guide-effects-interfaces.md)
-   [Interfaces especializadas](d3d10-graphics-reference-effect-specializing.md)
-   [Representar un efecto](d3d10-graphics-programming-guide-effects-render.md)

Un efecto encapsula todo el estado de representación requerido por un efecto determinado en una sola función de representación denominada técnica. Un paso es un subconjunto de una técnica que contiene el estado de representación. Para implementar un efecto de representación de varios pasos, implemente uno o varios pases dentro de una técnica. Por ejemplo, suponga que desea representar alguna geometría con un conjunto de búferes de profundidad/estarcido y, a continuación, dibujar algunos sprites encima de ese. Podría implementar la representación de geometría en el primer paso y el dibujo de Sprite en el segundo paso. Para representar el efecto, simplemente se representan ambos pasos en el bucle de representación. Puede implementar cualquier número de técnicas en un efecto. Por supuesto, cuanto mayor sea el número de técnicas, mayor será el tiempo de compilación del efecto. Una manera de aprovechar esta funcionalidad es crear efectos con técnicas que están diseñadas para ejecutarse en hardware diferente. Esto permite a una aplicación degradar correctamente el rendimiento en función de las capacidades de hardware detectadas.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Guía de programación para Direct3D 10](d3d10-graphics-programming-guide.md)
</dt> </dl>

 

 
