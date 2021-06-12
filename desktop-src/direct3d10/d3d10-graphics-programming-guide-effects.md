---
description: Obtenga información sobre los efectos de Direct3D 10. Un efecto es el estado de canalización, establecido por expresiones escritas en HLSL y alguna sintaxis específica del marco de efectos.
ms.assetid: db4c7651-b6a1-4bc3-bcf8-a5cb56c7563e
title: Efectos (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70a9a863fd34c5bb99389139d09860812b16b4fa
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2021
ms.locfileid: "112010918"
---
# <a name="effects-direct3d-10"></a>Efectos (Direct3D 10)

Un efecto DirectX es una colección de estado de canalización, establecida por expresiones escritas en [HLSL](../direct3dhlsl/dx-graphics-hlsl-reference.md) y alguna sintaxis específica del marco de efectos. Después de compilar un efecto, use las API del marco de efectos para representar. La funcionalidad de efecto puede abarcar desde algo tan sencillo como un sombreador de vértices que transforma la geometría y un sombreador de píxeles que genera un color sólido, hasta una técnica de representación que requiere varios pasos, usa cada fase de la canalización de gráficos y manipula el estado del sombreador, así como el estado de canalización no asociado a los sombreadores programables.

El primer paso consiste en organizar el estado que desea controlar en un efecto. Esto incluye el estado del sombreador (sombreadores de vértices, geometría y píxeles), el estado de textura y muestreador usado por los sombreadores y otro estado de canalización no programable. Puede crear un efecto en la memoria como una cadena de texto, pero normalmente el tamaño es lo suficientemente grande como para que sea útil almacenar el estado del efecto en un archivo de efecto (un archivo de texto que termina en una extensión .fx). Para usar un efecto, debe compilarlo (para comprobar la sintaxis HLSL, así como la sintaxis del marco de trabajo del efecto), inicializar el estado del efecto a través de llamadas API y modificar el bucle de representación para llamar a las API de representación.

-   [Organización del estado en un efecto](d3d10-graphics-programming-guide-effects-organize.md)
-   [Interfaces del sistema de efecto](d3d10-graphics-programming-guide-effects-interfaces.md)
-   [Especialización de interfaces](d3d10-graphics-reference-effect-specializing.md)
-   [Representación de un efecto](d3d10-graphics-programming-guide-effects-render.md)

Un efecto encapsula todo el estado de representación requerido por un efecto determinado en una sola función de representación denominada técnica. Un paso es un subgrupo de una técnica que contiene el estado de representación. Para implementar un efecto de representación de varios pases, implemente uno o varios pases dentro de una técnica. Por ejemplo, diga que quiere representar algo de geometría con un conjunto de búferes de profundidad o galería de símbolos y, a continuación, dibujar algunos sprites encima de eso. Puede implementar la representación de geometría en el primer paso y el dibujo de sprite en el segundo paso. Para representar el efecto, basta con representar ambos pases en el bucle de representación. Puede implementar cualquier número de técnicas en un efecto. Por supuesto, cuanto mayor sea el número de técnicas, mayor será el tiempo de compilación para el efecto. Una manera de aprovechar esta funcionalidad es crear efectos con técnicas diseñadas para ejecutarse en hardware diferente. Esto permite a una aplicación degradar correctamente el rendimiento en función de las funcionalidades de hardware detectadas.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Guía de programación para Direct3D 10](d3d10-graphics-programming-guide.md)
</dt> </dl>

 

 
