---
title: Fase del ensamblador de entrada
description: La API de Direct3D 10 y superior separa las áreas funcionales de la canalización en fases. La primera fase de la canalización es la fase de ensamblador de entrada (IA).
ms.assetid: 71141a5e-2d79-4b02-8370-c0cbc8618908
keywords:
- fase del ensamblador de entrada (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e16a419dfe57dac5b16562b234a7a60d417c071fcd6214f3defa84bcbe8b4ab
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119408385"
---
# <a name="input-assembler-stage"></a>Fase del ensamblador de entrada

La API de Direct3D 10 y superior separa las áreas funcionales de la canalización en fases. La primera fase de la canalización es la fase de ensamblador de entrada (IA).

El propósito de la fase de ensamblador de entrada es leer datos primitivos (puntos, líneas o triángulos) de búferes rellenos por el usuario y ensamblar los datos en primitivos que usarán las otras fases de canalización. La fase IA puede ensamblar vértices en varios tipos primitivos [diferentes](d3d10-graphics-programming-guide-primitive-topologies.md) (como listas de líneas, franjas de triángulos o primitivas con adyacencia). Se han agregado nuevos tipos primitivos (como una lista de líneas con adyacencia o una lista de triángulos con adyacencia) para admitir el sombreador de geometría.

La información de adyacencia solo es visible para una aplicación en un sombreador de geometría. Si se invocó un sombreador de geometría con un triángulo que incluye la adyacencia, por ejemplo, los datos de entrada contendrán 3 vértices para cada triángulo y 3 vértices para los datos de adyacencia por triángulo.

Cuando se solicita la fase de ensamblador de entrada para generar datos de adyacencia, los datos de entrada deben incluir datos de adyacencia. Esto puede requerir proporcionar un vértice ficticio (formando un triángulo degenerado) o quizás marcando en uno de los atributos del vértice si el vértice existe o no. Esto también tendría que detectarse y controlarse mediante un sombreador de geometría, aunque la selección de geometría degenerada se realizará en la fase del rasterizador.

Al ensamblar primitivas, un propósito secundario del [](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics) IA es adjuntar valores generados por el sistema para ayudar a que los sombreadores sea más eficientes. Los valores generados por el sistema son cadenas de texto que también se denominan semánticas. Las tres fases del sombreador se construyen a partir de un núcleo de sombreador común y el núcleo del sombreador usa valores generados por el sistema (por ejemplo, un identificador primitivo, un identificador de instancia o un identificador de vértice) para que una fase del sombreador pueda reducir el procesamiento solo a los primitivos, instancias o vértices que aún no se han procesado.

Como se muestra en el diagrama de bloques de canalización [,](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-pipeline-stages)una vez que la fase IA lee los datos de la memoria (ensambla los datos en primitivos y adjunta los valores generados por el sistema), los datos se generan en la fase del sombreador de vértices [.](/previous-versions//bb205146(v=vs.85))


## <a name="in-this-section"></a>En esta sección



| Tema                                                                                                                                   | Descripción                                                                                                                                                                                                                                                                                                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Tareas iniciales con la Input-Assembler fase](d3d10-graphics-programming-guide-input-assembler-stage-getting-started.md)<br/> | Hay algunos pasos necesarios para inicializar la fase del ensamblador de entrada (IA). Por ejemplo, debe crear recursos de búfer con los datos de vértices que necesita la canalización, indicar a la fase de IA dónde están los búferes y qué tipo de datos contienen, y especificar el tipo de primitivas que se ensamblan a partir de los datos.<br/> |
| [Topologías primitivas](d3d10-graphics-programming-guide-primitive-topologies.md)<br/>                                            | Direct3D 10 y superior admite varios tipos primitivos (o topologías) representados por el tipo enumerado [**\_ \_ TOPOLOGÍA PRIMITIVA D3D.**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_primitive_topology) Estos tipos definen cómo la canalización interpreta y representa los vértices.<br/>                                                          |
| [Usar la fase Input-Assembler sin búferes](d3d10-graphics-programming-guide-input-assembler-stage-no-buffers.md)<br/>     | No es necesario crear y enlazar búferes si los sombreadores no requieren búferes. Esta sección contiene un ejemplo de sombreadores de vértices y píxeles simples que dibujan un único triángulo.<br/>                                                                                                                                  |
| [Uso de System-Generated valores](d3d10-graphics-programming-guide-input-assembler-stage-using.md)<br/>                            | Los valores generados por el sistema se generan mediante la fase IA (basada en la semántica de entrada proporcionada por el usuario) para permitir ciertas [eficiencias](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics)en las operaciones del sombreador. <br/>                                                                                                                         |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Canalización de gráficos](overviews-direct3d-11-graphics-pipeline.md)
</dt> <dt>

[Fases de canalización (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-pipeline-stages)
</dt> </dl>

 

