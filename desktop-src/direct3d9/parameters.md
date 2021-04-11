---
description: Los parámetros son variables de efecto.
ms.assetid: vs|directx_sdk|~\parameters.htm
title: Parámetros (Direct3D 9)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e5c78a4f6c0518c99b61be10b721d98b17630ab
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104152690"
---
# <a name="parameters-direct3d-9"></a>Parámetros (Direct3D 9)

Los parámetros son variables de efecto.

## <a name="syntax"></a>Sintaxis

*ID. de tipo de uso* \[ : expresión *semántica* \] \[ < *(s)* > \] \[ =   \] ;

Los parámetros se pueden leer y escribir en la aplicación con [**ID3DXEffect**](id3dxeffect.md) o [**ID3DXEffectCompiler**](id3dxeffectcompiler.md).

Se puede hacer referencia a los parámetros en funciones y en técnicas (concretamente, en el lado derecho de las asignaciones de estado).



| Elemento                                                                                 | Descripción                                                                                                                                                     |
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="usage"></span><span id="USAGE"></span>*uso*<br/>                   | Ámbito del parámetro. Vea [usos y literales (Direct3D 9)](usages-and-literals.md).<br/>                                                             |
| <span id="type"></span><span id="TYPE"></span>*automáticamente*<br/>                      | Cualquier [referencia válida para](../direct3dhlsl/dx-graphics-hlsl-reference.md) el tipo HLSL.<br/>                                                                        |
| <span id="ID"></span><span id="id"></span>*SESIÓN*<br/>                            | Un nombre único.<br/>                                                                                                                                       |
| <span id="semantic"></span><span id="SEMANTIC"></span>*semántica*<br/>          | Una etiqueta que sigue las reglas de identificador que normalmente indica el uso del parámetro. Debe ser un tipo determinado.<br/>                                     |
| <span id="annotations"></span><span id="ANNOTATIONS"></span>*anotaciones*<br/> | Cero o más partes de la información específica del usuario. Puede ser cualquier tipo. Consulte [Agregar información a los parámetros de efectos con anotaciones](using-an-effect.md).<br/> |
| <span id="expression"></span><span id="EXPRESSION"></span>*Expresiones*<br/>    | Inicializa el valor del parámetro. Vea [expresiones (Direct3D 9)](expressions.md).<br/>                                                                  |



 

Los parámetros se pueden inicializar en cualquier [referencia válida de](../direct3dhlsl/dx-graphics-hlsl-reference.md) la expresión HLSL que se reduzca a un valor literal.

Los valores de parámetro no cambian en la ejecución de las llamadas de función o de asignación de estado.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Formato de efecto](dx9-graphics-reference-effects-file-format.md)
</dt> </dl>

 

 
