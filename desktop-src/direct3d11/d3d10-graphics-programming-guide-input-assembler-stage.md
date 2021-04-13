---
title: Fase del ensamblador de entrada
description: La API de Direct3D 10 y versiones posteriores separa las áreas funcionales de la canalización en fases; la primera fase de la canalización es la fase del ensamblador de entrada (IA).
ms.assetid: 71141a5e-2d79-4b02-8370-c0cbc8618908
keywords:
- fase del ensamblador de entrada (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 121d98ca66bbe42f6eaa3023150203ce0538445b
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/04/2020
ms.locfileid: "104421662"
---
# <a name="input-assembler-stage"></a>Fase del ensamblador de entrada

La API de Direct3D 10 y versiones posteriores separa las áreas funcionales de la canalización en fases; la primera fase de la canalización es la fase del ensamblador de entrada (IA).

El propósito de la fase del ensamblador de entrada es leer los datos primitivos (puntos, líneas o triángulos) de los búferes rellenados por el usuario y ensamblar los datos en primitivos que se usarán en las otras fases de canalización. La fase IA puede ensamblar vértices en varios [tipos primitivos](d3d10-graphics-programming-guide-primitive-topologies.md) diferentes (como listas de líneas, tiras de triángulos o primitivas con adyacencias). Se han agregado nuevos tipos primitivos (como una lista de líneas con adyacencias o una lista de triángulos con adyacencias) para admitir el sombreador de geometría.

La información de adyacencias solo es visible para una aplicación en un sombreador de geometría. Si se invocó un sombreador de geometría con un triángulo que incluye la adyacencia, por ejemplo, los datos de entrada contendrían 3 vértices para cada triángulo y 3 vértices para los datos de adyacencia por triángulo.

Cuando se solicita la etapa del ensamblador de entrada para generar datos de adyacencias, los datos de entrada deben incluir datos de adyacencia. Esto puede requerir que se proporcione un vértice ficticio (formando un triángulo degenerado) o quizás mediante la marcación de uno de los atributos de vértice si el vértice existe o no. Esto también debe detectarse y administrarse mediante un sombreador de geometría, aunque la selección de geometría degenerada se producirá en la fase de rasterizador.

Al ensamblar tipos primitivos, un propósito secundario del IA es adjuntar [valores generados](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics) por el sistema para ayudar a mejorar la eficacia de los sombreadores. Los valores generados por el sistema son cadenas de texto que también se denominan semánticas. Las tres fases del sombreador se construyen a partir de un núcleo de sombreador común y el núcleo del sombreador usa valores generados por el sistema (como un identificador primitivo, un identificador de instancia o un identificador de vértice) para que una fase del sombreador pueda reducir el procesamiento solo a las primitivas, instancias o vértices que aún no se han procesado.

Tal como se muestra en el [Diagrama de bloque de canalización](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-pipeline-stages), una vez que la fase IA Lee los datos de la memoria (ensambla los datos en primitivos y asocia los valores generados por el sistema), los datos se envían a la [fase del sombreador de vértices](/previous-versions//bb205146(v=vs.85)).


## <a name="in-this-section"></a>En esta sección



| Tema                                                                                                                                   | Descripción                                                                                                                                                                                                                                                                                                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Introducción con la fase de Input-Assembler](d3d10-graphics-programming-guide-input-assembler-stage-getting-started.md)<br/> | Hay algunos pasos necesarios para inicializar la fase del ensamblador de entrada (IA). Por ejemplo, debe crear recursos de búfer con los datos de vértice que necesita la canalización, indicar a la fase de IA dónde están los búferes y qué tipo de datos contienen, y especificar el tipo de primitivas que se van a ensamblar a partir de los datos.<br/> |
| [Topologías primitivas](d3d10-graphics-programming-guide-primitive-topologies.md)<br/>                                            | Direct3D 10 y versiones posteriores admiten varios tipos primitivos (o topologías) que están representados por el tipo enumerado de la [**topología de D3D \_ Primitive \_**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_primitive_topology) . Estos tipos definen cómo se interpretan y representan los vértices mediante la canalización.<br/>                                                          |
| [Usar la fase Input-Assembler sin búferes](d3d10-graphics-programming-guide-input-assembler-stage-no-buffers.md)<br/>     | No es necesario crear y enlazar búferes si los sombreadores no requieren búferes. Esta sección contiene un ejemplo de sombreadores de vértices y píxeles simples que dibujan un solo triángulo.<br/>                                                                                                                                  |
| [Usar valores System-Generated](d3d10-graphics-programming-guide-input-assembler-stage-using.md)<br/>                            | Los valores generados por el sistema se generan mediante la fase del IA (basada en la [semántica](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics)de entrada proporcionada por el usuario) para permitir ciertas eficiencias en las operaciones del sombreador. <br/>                                                                                                                         |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Canalización de gráficos](overviews-direct3d-11-graphics-pipeline.md)
</dt> <dt>

[Fases de canalización (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-pipeline-stages)
</dt> </dl>

 

