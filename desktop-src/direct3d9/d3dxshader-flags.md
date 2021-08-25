---
description: Las marcas D3DXSHADER se usan para analizar, compilar o ensamblar sombreadores.
ms.assetid: 8558d0e9-d09f-4c62-bc89-6080f4e44ff8
title: Marcas D3DXSHADER (D3dx9shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHADER_PACKMATRIX_COLUMNMAJOR
- D3DXSHADER_PACKMATRIX_ROWMAJOR
- D3DXSHADER_AVOID_FLOW_CONTROL
- D3DXSHADER_DEBUG
- D3DXSHADER_ENABLE_BACKWARDS_COMPATIBILITY
- D3DXSHADER_FORCE_PS_SOFTWARE_NOOPT
- D3DXSHADER_FORCE_VS_SOFTWARE_NOOPT
- D3DXSHADER_IEEE_STRICTNESS
- D3DXSHADER_NO_PRESHADER
- D3DXSHADER_OPTIMIZATION_LEVEL0
- D3DXSHADER_OPTIMIZATION_LEVEL1
- D3DXSHADER_OPTIMIZATION_LEVEL2
- D3DXSHADER_OPTIMIZATION_LEVEL3
- D3DXSHADER_PARTIALPRECISION
- D3DXSHADER_PREFER_FLOW_CONTROL
- D3DXSHADER_SKIPOPTIMIZATION
- D3DXSHADER_SKIPVALIDATION
- D3DXSHADER_USE_LEGACY_D3DX9_31_DLL
- D3DXSHADER_DEBUG
- D3DXSHADER_FORCE_PS_SOFTWARE_NOOPT
- D3DXSHADER_FORCE_VS_SOFTWARE_NOOPT
- D3DXSHADER_SKIPVALIDATION
api_type:
- HeaderDef
api_location:
- d3dx9shader.h
ms.openlocfilehash: 031ae23301b78a9cced683551c9d7220aa66f7e0a48b504fe1a93721fd8d6a38
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119849785"
---
# <a name="d3dxshader-flags"></a>Marcas D3DXSHADER

Las **marcas D3DXSHADER** se usan para analizar, compilar o ensamblar sombreadores.

**Marcas del analizador**

Las marcas de tiempo de análisis solo las usa el sistema de efectos (antes de la compilación del efecto) al crear un compilador de efectos. Por ejemplo, podría crear un objeto de compilador con **D3DXSHADER \_ PACKMATRIX \_ COLUMNMAJOR** y, a continuación, usar ese objeto de compilador repetidamente con marcas de compilador diferentes para generar código especializado.



| Constante                                                                                                                                                                                                                   | Descripción                                                                                                                                                                                                                                                                                        |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="D3DXSHADER_PACKMATRIX_COLUMNMAJOR"></span><span id="d3dxshader_packmatrix_columnmajor"></span><dl> <dt>**D3DXSHADER \_ PACKMATRIX \_ COLUMNMAJOR**</dt> </dl> | A menos que se especifique explícitamente, las matrices se empaquetarán en orden de columna principal (cada vector estará en una sola columna) cuando se pasen a y desde el sombreador. Esto suele ser más eficaz porque permite que la multiplicación de matrices vectoriales se realice mediante una serie de productos de puntos.<br/> |
| <span id="D3DXSHADER_PACKMATRIX_ROWMAJOR"></span><span id="d3dxshader_packmatrix_rowmajor"></span><dl> <dt>**D3DXSHADER \_ PACKMATRIX \_ ROWMAJOR**</dt> </dl>          | A menos que se especifique explícitamente, las matrices se empaquetarán en orden de fila principal (cada vector estará en una sola fila) cuando se pasen a o desde el sombreador.<br/>                                                                                                                                        |



**Marcas del compilador**

El compilador HLSL de DirectX 10 es ahora el compilador predeterminado. Vea [Effect-Compiler Tool para](../direct3dtools/fxc.md) obtener más información.

En la tabla siguiente se detallan las marcas disponibles en Direct3D 9 y Direct3D 10. El valor de la marca es la opción fxc equivalente.



| Constante o valor                                                                                                                                                                                                                                                                                                | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="D3DXSHADER_AVOID_FLOW_CONTROL"></span><span id="d3dxshader_avoid_flow_control"></span><dl> <dt>**D3DXSHADER \_ AVOID \_ FLOW \_ CONTROL**</dt> <dt>/Gfa</dt> </dl>                                     | Se trata de una sugerencia al compilador para evitar el uso de instrucciones de control de flujo.<br/> Direct3D 9: sí<br/> Direct3D 10: sí<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="D3DXSHADER_DEBUG"></span><span id="d3dxshader_debug"></span><dl> <dt>**D3DXSHADER \_ DEBUG**</dt> <dt>/Zi</dt> </dl>                                                                               | Inserte el nombre de archivo de depuración, los números de línea y la información de tipo y símbolo durante la compilación del sombreador.<br/> Direct3D 9: sí<br/> Direct3D 10: sí<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span id="D3DXSHADER_ENABLE_BACKWARDS_COMPATIBILITY"></span><span id="d3dxshader_enable_backwards_compatibility"></span><dl> <dt>**D3DXSHADER \_ HABILITAR \_ COMPATIBILIDAD CON VERSIONES \_ ANTERIORES**</dt> <dt>/Gec</dt> </dl> | Compile ps \_ 1 \_ x shaders como ps \_ 2 \_ 0. En su lugar, los efectos que especifican destinos ps 1 x se compilarán en ps 2 0 destinos porque esta es la versión mínima del sombreador admitida por la versión del compilador de sombreador que se incluye \_ \_ con \_ \_ DirectX 10. Esta marca no tiene ningún efecto cuando se usa con destinos de compilación de nivel superior.<br/> Direct3D 9: no<br/> Direct3D 10: sí<br/>                                                                                                                                                                                                                                                                       |
| <span id="D3DXSHADER_FORCE_PS_SOFTWARE_NOOPT"></span><span id="d3dxshader_force_ps_software_noopt"></span><dl> <dt>**D3DXSHADER \_ FORCE \_ PS \_ SOFTWARE \_ NOOPT**</dt> <dt>N/A</dt> </dl>                      | Fuerce al compilador a compilar con el siguiente destino de software más alto disponible para los sombreadores de píxeles. Esta marca también desactiva las optimizaciones y la depuración.<br/> Direct3D 9: sí<br/> Direct3D 10: sí<br/>                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="D3DXSHADER_FORCE_VS_SOFTWARE_NOOPT"></span><span id="d3dxshader_force_vs_software_noopt"></span><dl> <dt>**D3DXSHADER \_ FORCE \_ VS \_ SOFTWARE \_ NOOPT**</dt> <dt>N/A</dt> </dl>                      | Fuerce al compilador a compilar con el siguiente destino de software más alto disponible para los sombreadores de vértices. Esta marca también desactiva las optimizaciones y la depuración.<br/> Direct3D 9: sí<br/> Direct3D 10: sí<br/>                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="D3DXSHADER_IEEE_STRICTNESS"></span><span id="d3dxshader_ieee_strictness"></span><dl> <dt>**D3DXSHADER \_ IEEE \_ STRICTNESS**</dt> <dt>/Gis</dt> </dl>                                               | Deshabilite las optimizaciones que pueden hacer que la salida de un programa de sombreador compilado se difiere de la salida de un programa compilado con el compilador de sombreadores DirectX 9 debido a pequeños errores de precisión en matemáticas de punto flotante.<br/> Direct3D 9: no<br/> Direct3D 10: sí<br/>                                                                                                                                                                                                                                                                                                                                                                |
| <span id="D3DXSHADER_NO_PRESHADER"></span><span id="d3dxshader_no_preshader"></span><dl> <dt>**D3DXSHADER \_ NO \_ PRESHADER**</dt> <dt>/Op</dt> </dl>                                                         | Deshabilita los preshaders. El compilador no extraerá expresiones estáticas para la evaluación en la CPU del host. Además, el compilador no almacenará ninguna expresión al compilar funciones independientes.<br/> Direct3D 9: sí<br/> Direct3D 10: sí<br/>                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="D3DXSHADER_OPTIMIZATION_LEVEL0"></span><span id="d3dxshader_optimization_level0"></span><dl> <dt>**D3DXSHADER \_ OPTIMIZATION \_ LEVEL0**</dt> <dt>/O0</dt> </dl>                                    | Nivel de optimización más bajo. Puede generar código más lento, pero lo hará más rápidamente. Esto puede ser útil en un ciclo de desarrollo de sombreador muy iterativo.<br/> Direct3D 9: no<br/> Direct3D 10: sí<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span id="D3DXSHADER_OPTIMIZATION_LEVEL1"></span><span id="d3dxshader_optimization_level1"></span><dl> <dt>**D3DXSHADER \_ OPTIMIZATION \_ LEVEL1**</dt> <dt>/O1</dt> </dl>                                    | Segundo nivel de optimización más bajo.<br/> Direct3D 9: no<br/> Direct3D 10: sí<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <span id="D3DXSHADER_OPTIMIZATION_LEVEL2"></span><span id="d3dxshader_optimization_level2"></span><dl> <dt>**D3DXSHADER \_ OPTIMIZATION \_ LEVEL2**</dt> <dt>/O2</dt> </dl>                                    | Segundo nivel de optimización más alto.<br/> Direct3D 9: no<br/> Direct3D 10: sí<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span id="D3DXSHADER_OPTIMIZATION_LEVEL3"></span><span id="d3dxshader_optimization_level3"></span><dl> <dt>**D3DXSHADER \_ OPTIMIZATION \_ LEVEL3**</dt> <dt>/O3</dt> </dl>                                    | Nivel de optimización más alto. Producirá el mejor código posible, pero puede tardar mucho más tiempo en hacerlo. Esto será útil para las compilaciones finales de una aplicación donde el rendimiento es el factor más importante.<br/> Direct3D 9: no<br/> Direct3D 10: sí<br/>                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="D3DXSHADER_PARTIALPRECISION"></span><span id="d3dxshader_partialprecision"></span><dl> <dt>**D3DXSHADER \_ PARTIALPRECISION**</dt> <dt>/Gpp</dt> </dl>                                             | Forzar que todos los cálculos del sombreador resultante se produzcan con precisión parcial. Esto puede dar lugar a una evaluación más rápida de los sombreadores en algún hardware.<br/> Direct3D 9: sí<br/> Direct3D 10: sí<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="D3DXSHADER_PREFER_FLOW_CONTROL"></span><span id="d3dxshader_prefer_flow_control"></span><dl> <dt>**D3DXSHADER \_ PREFER \_ FLOW \_ CONTROL**</dt> <dt>/Gfp</dt> </dl>                                  | Se trata de una sugerencia para que el compilador prefiera usar instrucciones de control de flujo.<br/> Direct3D 9: sí<br/> Direct3D 10: sí<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span id="D3DXSHADER_SKIPOPTIMIZATION"></span><span id="d3dxshader_skipoptimization"></span><dl> <dt>**D3DXSHADER \_ SKIPOPTIMIZATION**</dt> <dt>/Od</dt> </dl>                                              | Indique al compilador que omita los pasos de optimización durante la generación de código. A menos que intente aislar un problema en el código y sospeche que el compilador usa esta opción no se recomienda.<br/> Direct3D 9: sí<br/> Direct3D 10: sí<br/>                                                                                                                                                                                                                                                                                                                                                                               |
| <span id="D3DXSHADER_SKIPVALIDATION"></span><span id="d3dxshader_skipvalidation"></span><dl> <dt>**D3DXSHADER \_ SKIPVALIDATION**</dt> <dt>/Vd</dt> </dl>                                                    | No valide el código generado con las funcionalidades y restricciones conocidas. Esta opción solo se recomienda cuando se compilan sombreadores que se sabe que funcionan (es decir, los sombreadores que se han compilado antes sin esta opción). El tiempo de ejecución siempre valida los sombreadores antes de establecerse en el dispositivo.<br/> Direct3D 9: sí<br/> Direct3D 10: sí<br/>                                                                                                                                                                                                                                                                      |
| <span id="D3DXSHADER_USE_LEGACY_D3DX9_31_DLL"></span><span id="d3dxshader_use_legacy_d3dx9_31_dll"></span><dl> <dt>**D3DXSHADER \_ USE \_ \_ D3DX9 \_ 31 \_ DLL**</dt> <dt>/LD</dt> HEREDADO </dl>                     | Habilite el uso del compilador HLSL original de Direct3D 9. OCT2006 \_ d3dx9 \_ 31 \_x86.cab o OCT2006 \_ d3dx9 \_ 31 \_x64.cab deben incluirse como parte de la redist de aplicaciones. Esta marca es necesaria para compilar sombreadores ps \_ 1 \_ x sin usar la marca de promoción a ps \_ 2 \_ 0. La especificación de esta marca al obtener una interfaz [**ID3DXEffectCompiler**](id3dxeffectcompiler.md) hace que las llamadas posteriores a [**CompileEffect**](id3dxeffectcompiler--compileeffect.md) y [**CompileShader**](id3dxeffectcompiler--compileshader.md) a través de este objeto usen el compilador heredado.<br/> Direct3D 9: sí<br/> Direct3D 10: no<br/> |



**Marcas de ensamblador**

El sistema de efectos usa las marcas del ensamblador para optimizar el sombreador y el código de ensamblado de efecto.



| Constante                                                                                                                                                                                                                        | Descripción                                                                                                                                                                                                                                                                                                              |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="D3DXSHADER_DEBUG"></span><span id="d3dxshader_debug"></span><dl> <dt>**D3DXSHADER \_ DEBUG**</dt> </dl>                                                          | Inserte el nombre de archivo de depuración, los números de línea y el tipo y la información de símbolos durante la compilación del sombreador.<br/>                                                                                                                                                                                                                   |
| <span id="D3DXSHADER_FORCE_PS_SOFTWARE_NOOPT"></span><span id="d3dxshader_force_ps_software_noopt"></span><dl> <dt>**D3DXSHADER \_ FORCE \_ PS \_ SOFTWARE \_ NOOPT**</dt> </dl> | Fuerce al compilador a compilar con el siguiente destino de software más alto disponible para sombreadores de píxeles. Esta marca también desactiva las optimizaciones y activa la depuración.<br/>                                                                                                                                                  |
| <span id="D3DXSHADER_FORCE_VS_SOFTWARE_NOOPT"></span><span id="d3dxshader_force_vs_software_noopt"></span><dl> <dt>**D3DXSHADER \_ FORCE \_ VS \_ SOFTWARE \_ NOOPT**</dt> </dl> | Fuerce al compilador a compilar con el siguiente destino de software más alto disponible para sombreadores de vértices. Esta marca también desactiva las optimizaciones y activa la depuración.<br/>                                                                                                                                                 |
| <span id="D3DXSHADER_SKIPVALIDATION"></span><span id="d3dxshader_skipvalidation"></span><dl> <dt>**D3DXSHADER \_ SKIPVALIDATION**</dt> </dl>                               | No valide el código generado con las funcionalidades y restricciones conocidas. Esta opción solo se recomienda cuando se compilan sombreadores que se sabe que funcionan (es decir, los sombreadores que se han compilado antes sin esta opción). El tiempo de ejecución siempre valida los sombreadores antes de establecerse en el dispositivo.<br/> |



## <a name="remarks"></a>Comentarios

El sistema de efectos usará **marcas de analizador cuando** las llamen las funciones siguientes:

-   [**D3DXCompileShader**](d3dxcompileshader.md)
-   [**D3DXCompileShaderFromFile**](d3dxcompileshaderfromfile.md)
-   [**D3DXCompileShaderFromResource**](d3dxcompileshaderfromresource.md)
-   [**CompileEffect**](id3dxeffectcompiler--compileeffect.md)

El sistema de efectos usará **marcas del compilador cuando** las llamen las funciones siguientes:

-   [**D3DXCompileShader**](d3dxcompileshader.md) (o [**D3DXCompileShaderFromFile**](d3dxcompileshaderfromfile.md) o [**D3DXCompileShaderFromResource)**](d3dxcompileshaderfromresource.md)
-   [**CompileEffect**](id3dxeffectcompiler--compileeffect.md) (o [**CompileShader)**](id3dxeffectcompiler--compileshader.md)

Además, puede usar  marcas del compilador al crear un efecto llamando a [**D3DXCreateEffect**](d3dxcreateeffect.md) (o [**D3DXCreateEffectFromFile**](d3dxcreateeffectfromfile.md) o [**D3DXCreateEffectFromResource).**](d3dxcreateeffectfromresource.md)

-   Si pasa un archivo .fx no compilado, el sistema de efectos usará el parámetro de entrada de marca durante la compilación.
-   Si pasa un efecto compilado, el sistema de efectos omitirá las marcas del compilador, ya que no son necesarias para cargar el efecto.

El sistema de efectos usará **marcas de ensamblador cuando** las llamen las funciones siguientes:

-   [**D3DXAssembleShader**](d3dxassembleshader.md)
-   [**D3DXAssembleShaderFromFile**](d3dxassembleshaderfromfile.md)
-   [**D3DXAssembleShaderFromResource**](d3dxassembleshaderfromresource.md)

La aplicación **de marcas del compilador** o de **ensamblador** a la API incorrecta producirá un error en la validación del sombreador. Compruebe el valor devuelto del código de error de Direct3D de la función con la Herramienta de búsqueda de errores de DirectX (DXErr.exe) para ayudar a realizar el seguimiento de este error. Puede obtener información DXErr.exe y obtener información sobre él desde el SDK de DirectX. Para obtener información sobre el SDK de DirectX, [consulte ¿Dónde está el SDK de DirectX?](../directx-sdk--august-2009-.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx9shader.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Constantes D3DX](dx9-graphics-reference-d3dx-constants.md)
</dt> </dl>

 

 
