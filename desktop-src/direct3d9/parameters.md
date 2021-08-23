---
description: Los parámetros son variables de efecto.
ms.assetid: vs|directx_sdk|~\parameters.htm
title: Parámetros (Direct3D 9)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fc28d1410180aac54daf306fe586694cfa1b7f4123403efc606a77385d088326
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119606685"
---
# <a name="parameters-direct3d-9"></a>Parámetros (Direct3D 9)

Los parámetros son variables de efecto.

## <a name="syntax"></a>Syntax

*identificador de tipo de uso:* expresión de anotaciones \[  \] \[ <  > \] \[ =  *semánticas* \] ;

La aplicación puede leer y escribir parámetros en con [**ID3DXEffect**](id3dxeffect.md) o [**ID3DXEffectCompiler.**](id3dxeffectcompiler.md)

Se puede hacer referencia a los parámetros en funciones y en técnicas (específicamente, en el lado derecho de las asignaciones de estado).



| Elemento                                                                                 | Descripción                                                                                                                                                     |
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="usage"></span><span id="USAGE"></span>*Uso*<br/>                   | Ámbito del parámetro. Vea [Usages and Literals (Direct3D 9) (Usos y literales [Direct3D 9]).](usages-and-literals.md)<br/>                                                             |
| <span id="type"></span><span id="TYPE"></span>*Tipo*<br/>                      | Cualquier referencia [válida para el tipo HLSL.](../direct3dhlsl/dx-graphics-hlsl-reference.md)<br/>                                                                        |
| <span id="ID"></span><span id="id"></span>*Id*<br/>                            | Un nombre único.<br/>                                                                                                                                       |
| <span id="semantic"></span><span id="SEMANTIC"></span>*Semántica*<br/>          | Etiqueta que sigue a las reglas de identificador que normalmente indica el uso del parámetro . Debe ser un tipo determinado.<br/>                                     |
| <span id="annotations"></span><span id="ANNOTATIONS"></span>*Anotaciones*<br/> | Cero o más fragmentos de información específica del usuario. Puede ser cualquier tipo. Vea [Agregar información para hacer efecto a los parámetros con anotaciones](using-an-effect.md).<br/> |
| <span id="expression"></span><span id="EXPRESSION"></span>*Expresión*<br/>    | Inicializa el valor del parámetro. Vea [Expresiones (Direct3D 9).](expressions.md)<br/>                                                                  |



 

Los parámetros se pueden inicializar en cualquier [referencia válida para la expresión HLSL](../direct3dhlsl/dx-graphics-hlsl-reference.md) que se reduzca a un valor literal.

Los valores de parámetro no se modifican mediante la ejecución de llamadas de función o asignación de estado.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Formato de efecto](dx9-graphics-reference-effects-file-format.md)
</dt> </dl>

 

 
