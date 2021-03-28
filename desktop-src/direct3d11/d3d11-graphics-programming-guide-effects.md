---
title: Efectos (Direct3D 11)
description: Un efecto de DirectX es una colección de estado de canalización, establecida por expresiones escritas en HLSL y alguna sintaxis específica del marco de trabajo de efecto.
ms.assetid: d52a2cad-eac9-4442-9ee5-114bebe0f245
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8952a35e1212f7d50956cc54e7a046db9f87b3b6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792448"
---
# <a name="effects-direct3d-11"></a>Efectos (Direct3D 11)

Un efecto de DirectX es una colección de estado de canalización, establecida por expresiones escritas en [HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-reference) y alguna sintaxis específica del marco de trabajo de efecto.

Después de compilar un efecto, use las API del marco de trabajo para representar. La funcionalidad de efectos puede abarcar desde algo tan sencillo como un sombreador de vértices que transforma la geometría y un sombreador de píxeles que da como resultado un color sólido, a una técnica de representación que requiere varios pases, usa todas las fases de la canalización de gráficos y manipula el estado del sombreador, así como el estado de la canalización que no está asociado a los sombrea

El primer paso es organizar el estado que desea controlar en un efecto. Esto incluye el estado del sombreador (vértices, casco, dominio, geometría, píxeles y sombreadores de cálculo), el estado de la textura y el muestreador que usan los sombreadores y otro estado de canalización no programable. Puede crear un efecto en la memoria como una cadena de texto, pero normalmente el tamaño es lo suficientemente grande como para almacenar el estado del efecto en un archivo de efectos (un archivo de texto que finaliza en una extensión. FX). Para usar un efecto, debe compilarlo (para comprobar la sintaxis de HLSL y la sintaxis del marco de trabajo), inicializar el estado del efecto a través de las llamadas API y modificar el bucle de representación para llamar a las API de representación.

Un efecto encapsula todo el estado de representación requerido por un efecto determinado en una sola función de representación denominada técnica. Un paso es un subconjunto de una técnica que contiene el estado de representación. Para implementar un efecto de representación de varios pasos, implemente uno o varios pases dentro de una técnica. Por ejemplo, suponga que desea representar alguna geometría con un conjunto de búferes de profundidad/estarcido y, a continuación, dibujar algunos sprites encima de ese. Podría implementar la representación de geometría en el primer paso y el dibujo de Sprite en el segundo paso. Para representar el efecto, simplemente se representan ambos pasos en el bucle de representación. Puede implementar cualquier número de técnicas en un efecto. Por supuesto, cuanto mayor sea el número de técnicas, mayor será el tiempo de compilación del efecto. Una manera de aprovechar esta funcionalidad es crear efectos con técnicas que están diseñadas para ejecutarse en hardware diferente. Esto permite a una aplicación degradar correctamente el rendimiento en función de las capacidades de hardware detectadas.

Se puede agrupar un conjunto de técnicas en un grupo (que usa la sintaxis "fxgroup"). Las técnicas se pueden agrupar de cualquier manera. Por ejemplo, se pueden crear varios grupos, uno por materia; cada material puede tener una técnica para cada nivel de hardware. cada técnica tendría un conjunto de pasadas que definen el material en el hardware determinado.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                                                | Descripción                                                                                                                                                         |
|----------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Organización del estado en un efecto](d3d11-graphics-programming-guide-effects-organize.md)<br/>                    | Con Direct3D 11, el estado del efecto para ciertas fases de canalización se organiza por estructuras.<br/>                                                                   |
| [Interfaces del sistema de efectos](d3d11-graphics-programming-guide-effects-interfaces.md)<br/>                       | El sistema de efectos define varias interfaces para administrar el estado del efecto.<br/>                                                                                  |
| [Interfaces especializadas](d3d11-graphics-reference-effect-specializing.md)<br/>                               | [**ID3DX11EffectVariable**](id3dx11effectvariable.md) tiene una serie de métodos para convertir la interfaz en el tipo de interfaz concreto que necesita.<br/> |
| [Interfaces y clases en efectos](d3d11-graphics-programming-guide-effects-interfaces-and-classes.md)<br/>  | Hay muchas maneras de usar clases e interfaces en los efectos 11.<br/>                                                                                         |
| [Representar un efecto](d3d11-graphics-programming-guide-effects-render.md)<br/>                                | Se puede usar un efecto para almacenar información o para representar mediante un grupo de estado.<br/>                                                                         |
| [Clonar un efecto](d3d11-graphics-programming-guide-effects-cloning.md)<br/>                                 | La clonación de un efecto crea una segunda copia prácticamente idéntica del efecto.<br/>                                                                                 |
| [Sintaxis de Stream out](d3d11-graphics-reference-effect-streamout.md)<br/>                                        | Un sombreador de geometría con Stream out se declara con una sintaxis determinada.<br/>                                                                                  |
| [Diferencias entre efectos 10 y efectos 11](d3d11-graphics-programming-guide-effects-differences.md)<br/> | En este tema se muestran las diferencias entre los efectos 10 y 11.<br/>                                                                                      |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Programming Guide for Direct3D 11 (Guía de programación para Direct3D 11)](dx-graphics-overviews.md)
</dt> </dl>

 

