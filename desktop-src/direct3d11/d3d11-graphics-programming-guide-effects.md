---
title: Efectos (Direct3D 11)
description: Obtenga información sobre los efectos de Direct3D 11. Un efecto es el estado de canalización, establecido por expresiones escritas en HLSL y alguna sintaxis específica del marco de efectos.
ms.assetid: d52a2cad-eac9-4442-9ee5-114bebe0f245
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 063b554e28786b48a467de12042bf6ada99645a9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127361287"
---
# <a name="effects-direct3d-11"></a>Efectos (Direct3D 11)

Un efecto DirectX es una colección de estado de canalización, establecida por expresiones escritas en [HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-reference) y alguna sintaxis específica del marco de efectos.

Después de compilar un efecto, use las API del marco de efectos para representar. La funcionalidad de efecto puede abarcar desde algo tan sencillo como un sombreador de vértices que transforma la geometría y un sombreador de píxeles que genera un color sólido, hasta una técnica de representación que requiere varios pasos, usa cada fase de la canalización de gráficos y manipula el estado del sombreador, así como el estado de canalización no asociado a los sombreadores programables.

El primer paso consiste en organizar el estado que desea controlar en un efecto. Esto incluye el estado del sombreador (vértice, casco, dominio, geometría, sombreadores de píxeles y de proceso), el estado de textura y muestreador usado por los sombreadores y otro estado de canalización no programable. Puede crear un efecto en la memoria como una cadena de texto, pero normalmente el tamaño es lo suficientemente grande como para que sea útil almacenar el estado del efecto en un archivo de efecto (un archivo de texto que termina en una extensión .fx). Para usar un efecto, debe compilarlo (para comprobar la sintaxis hlsl, así como la sintaxis del marco de trabajo del efecto), inicializar el estado del efecto a través de llamadas API y modificar el bucle de representación para llamar a las API de representación.

Un efecto encapsula todo el estado de representación requerido por un efecto determinado en una sola función de representación denominada técnica. Un paso es un subgrupo de una técnica que contiene el estado de representación. Para implementar un efecto de representación de varios pases, implemente uno o varios pases dentro de una técnica. Por ejemplo, diga que quiere representar algo de geometría con un conjunto de búferes de profundidad o galería de símbolos y, a continuación, dibujar algunos sprites encima de eso. Puede implementar la representación de geometría en el primer paso y el dibujo de sprite en el segundo paso. Para representar el efecto, basta con representar ambos pases en el bucle de representación. Puede implementar cualquier número de técnicas en un efecto. Por supuesto, cuanto mayor sea el número de técnicas, mayor será el tiempo de compilación para el efecto. Una manera de aprovechar esta funcionalidad es crear efectos con técnicas diseñadas para ejecutarse en hardware diferente. Esto permite a una aplicación degradar correctamente el rendimiento en función de las funcionalidades de hardware detectadas.

Un conjunto de técnicas se puede agrupar en un grupo (que usa la sintaxis "fxgroup"). Las técnicas se pueden agrupar de cualquier manera. Por ejemplo, se podrían crear varios grupos, uno por material; cada material podría tener una técnica para cada nivel de hardware; cada técnica tendría un conjunto de pasadas que definen el material en el hardware determinado.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                                                | Descripción                                                                                                                                                         |
|----------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Organización del estado en un efecto](d3d11-graphics-programming-guide-effects-organize.md)<br/>                    | Con Direct3D 11, el estado de efecto de determinadas fases de canalización se organiza por estructuras.<br/>                                                                   |
| [Interfaces del sistema de efecto](d3d11-graphics-programming-guide-effects-interfaces.md)<br/>                       | El sistema de efectos define varias interfaces para administrar el estado del efecto.<br/>                                                                                  |
| [Especialización de interfaces](d3d11-graphics-reference-effect-specializing.md)<br/>                               | [**ID3DX11EffectVariable tiene**](id3dx11effectvariable.md) una serie de métodos para convertir la interfaz en el tipo concreto de interfaz que necesita.<br/> |
| [Interfaces y clases en efectos](d3d11-graphics-programming-guide-effects-interfaces-and-classes.md)<br/>  | Hay muchas maneras de usar clases e interfaces en Efectos 11.<br/>                                                                                         |
| [Representación de un efecto](d3d11-graphics-programming-guide-effects-render.md)<br/>                                | Un efecto se puede usar para almacenar información o para representar mediante un grupo de estado.<br/>                                                                         |
| [Clonación de un efecto](d3d11-graphics-programming-guide-effects-cloning.md)<br/>                                 | La clonación de un efecto crea una segunda copia casi idéntica del efecto.<br/>                                                                                 |
| [Sintaxis de stream out](d3d11-graphics-reference-effect-streamout.md)<br/>                                        | Un sombreador de geometría con flujo de salida se declara con una sintaxis determinada.<br/>                                                                                  |
| [Diferencias entre los efectos 10 y 11](d3d11-graphics-programming-guide-effects-differences.md)<br/> | En este tema se muestran las diferencias entre Efectos 10 y Efectos 11.<br/>                                                                                      |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Programming Guide for Direct3D 11 (Guía de programación para Direct3D 11)](dx-graphics-overviews.md)
</dt> </dl>

 

