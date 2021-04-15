---
description: Las marcas D3DXSHADER se usan para analizar, compilar o ensamblar sombreadores.
ms.assetid: 8558d0e9-d09f-4c62-bc89-6080f4e44ff8
title: Marcas D3DXSHADER (D3dx9shader. h)
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
ms.openlocfilehash: 6f5d35f8c3bdf556e188c2cab8ff2684449b226f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105649405"
---
# <a name="d3dxshader-flags"></a>Marcas de D3DXSHADER

Las marcas **D3DXSHADER** se usan para analizar, compilar o ensamblar sombreadores.

**Marcas de analizador**

Las marcas de tiempo de análisis solo las usa el sistema de efectos (antes de la compilación de efectos) al crear un compilador de efectos. Por ejemplo, podría crear un objeto de compilador con **D3DXSHADER \_ PACKMATRIX \_ COLUMNMAJOR** y, a continuación, usar ese objeto de compilador varias veces con diferentes marcas de compilador para generar código especializado.



| Constante                                                                                                                                                                                                                   | Descripción                                                                                                                                                                                                                                                                                        |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="D3DXSHADER_PACKMATRIX_COLUMNMAJOR"></span><span id="d3dxshader_packmatrix_columnmajor"></span><dl> <dt>**D3DXSHADER \_ PACKMATRIX \_ COLUMNMAJOR**</dt> </dl> | A menos que se especifique explícitamente, las matrices se empaquetarán en el orden principal de la columna (cada vector estará en una sola columna) cuando se pasa a y desde el sombreador. Esto suele ser más eficaz, ya que permite realizar la multiplicación de matrices vectoriales mediante una serie de productos de punto.<br/> |
| <span id="D3DXSHADER_PACKMATRIX_ROWMAJOR"></span><span id="d3dxshader_packmatrix_rowmajor"></span><dl> <dt>**D3DXSHADER \_ PACKMATRIX \_ ROWMAJOR**</dt> </dl>          | A menos que se especifique explícitamente, las matrices se empaquetarán en orden principal de fila (cada vector estará en una sola fila) cuando se pasa a o desde el sombreador.<br/>                                                                                                                                        |



**Marcas del compilador**

El compilador de HLSL de DirectX 10 es ahora el compilador predeterminado. Consulte [herramienta de compilador de efectos](../direct3dtools/fxc.md) para más información.

En la tabla siguiente se detallan las marcas disponibles en Direct3D 9 y Direct3D 10. El valor de la marca es la opción FXC equivalente.



| Constante o valor                                                                                                                                                                                                                                                                                                | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="D3DXSHADER_AVOID_FLOW_CONTROL"></span><span id="d3dxshader_avoid_flow_control"></span><dl> <dt>**D3DXSHADER \_ EVITAR \_ el \_ control de flujo**</dt> <dt>/GFA</dt> </dl>                                     | Esta es una sugerencia para el compilador para evitar el uso de instrucciones de control de flujo.<br/> Direct3D 9: sí<br/> Direct3D 10: sí<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="D3DXSHADER_DEBUG"></span><span id="d3dxshader_debug"></span><dl> <dt>**D3DXSHADER \_ Depurar**</dt> <dt>/Zi</dt> </dl>                                                                               | Inserte el nombre de archivo de depuración, los números de línea y el tipo y la información de símbolos durante la compilación del sombreador.<br/> Direct3D 9: sí<br/> Direct3D 10: sí<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span id="D3DXSHADER_ENABLE_BACKWARDS_COMPATIBILITY"></span><span id="d3dxshader_enable_backwards_compatibility"></span><dl> <dt>**D3DXSHADER \_ HABILITAR \_ la \_ compatibilidad con versiones anteriores**</dt> <dt>/GEC</dt> </dl> | Compile los \_ \_ sombreadores de PS 1 x como PS \_ 2 \_ 0. En su lugar, los efectos que especifican \_ \_ los destinos PS 1 x se compilarán en los \_ destinos PS 2 0, ya que \_ es la versión de sombreador mínima admitida por la versión del compilador de sombreador incluida con DirectX 10. Esta marca no tiene ningún efecto cuando se usa con destinos de compilación de nivel superior.<br/> Direct3D 9: no<br/> Direct3D 10: sí<br/>                                                                                                                                                                                                                                                                       |
| <span id="D3DXSHADER_FORCE_PS_SOFTWARE_NOOPT"></span><span id="d3dxshader_force_ps_software_noopt"></span><dl> <dt>**D3DXSHADER \_ FORZAr el \_ \_ \_ NOOPT de software PS**</dt> <dt>N/A</dt> </dl>                      | Obligue al compilador a compilar con el siguiente destino de software disponible más alto para los sombreadores de píxeles. Esta marca también desactiva las optimizaciones y la depuración.<br/> Direct3D 9: sí<br/> Direct3D 10: sí<br/>                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="D3DXSHADER_FORCE_VS_SOFTWARE_NOOPT"></span><span id="d3dxshader_force_vs_software_noopt"></span><dl> <dt>**D3DXSHADER \_ FORZAr \_ \_ \_ NOOPT de vs software**</dt> <dt>N/A</dt> </dl>                      | Obligue al compilador a compilar con el siguiente destino de software disponible más alto para los sombreadores de vértices. Esta marca también desactiva las optimizaciones y la depuración.<br/> Direct3D 9: sí<br/> Direct3D 10: sí<br/>                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="D3DXSHADER_IEEE_STRICTNESS"></span><span id="d3dxshader_ieee_strictness"></span><dl> <dt>**D3DXSHADER \_ /GIS de \_ restricción IEEE**</dt> <dt></dt> </dl>                                               | Deshabilite las optimizaciones que pueden hacer que la salida de un programa de sombreador compilado difiera de la salida de un programa compilado con el compilador de sombreador de DirectX 9 debido a los errores de precisión pequeños en matemáticas de punto flotante.<br/> Direct3D 9: no<br/> Direct3D 10: sí<br/>                                                                                                                                                                                                                                                                                                                                                                |
| <span id="D3DXSHADER_NO_PRESHADER"></span><span id="d3dxshader_no_preshader"></span><dl> <dt>**D3DXSHADER \_ NO hay ningún \_ sombreador**</dt> <dt>/OP</dt> </dl>                                                         | Deshabilita los sombreadores. El compilador no extraerá las expresiones estáticas para la evaluación en la CPU del host. Además, el compilador no Loft ninguna expresión al compilar funciones independientes.<br/> Direct3D 9: sí<br/> Direct3D 10: sí<br/>                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="D3DXSHADER_OPTIMIZATION_LEVEL0"></span><span id="d3dxshader_optimization_level0"></span><dl> <dt>**D3DXSHADER \_ \_LEVEL0 de optimización**</dt> <dt>/O0</dt> </dl>                                    | Nivel de optimización más bajo. Puede generar código más lento, pero lo hará más rápidamente. Esto puede resultar útil en un ciclo de desarrollo de sombreador muy iterativo.<br/> Direct3D 9: no<br/> Direct3D 10: sí<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span id="D3DXSHADER_OPTIMIZATION_LEVEL1"></span><span id="d3dxshader_optimization_level1"></span><dl> <dt>**D3DXSHADER \_ \_Level1 de optimización**</dt> <dt>/O1</dt> </dl>                                    | Segundo nivel de optimización inferior.<br/> Direct3D 9: no<br/> Direct3D 10: sí<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <span id="D3DXSHADER_OPTIMIZATION_LEVEL2"></span><span id="d3dxshader_optimization_level2"></span><dl> <dt>**D3DXSHADER \_ \_LEVEL2 de optimización**</dt> <dt>/O2</dt> </dl>                                    | Segundo nivel de optimización más alto.<br/> Direct3D 9: no<br/> Direct3D 10: sí<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span id="D3DXSHADER_OPTIMIZATION_LEVEL3"></span><span id="d3dxshader_optimization_level3"></span><dl> <dt>**D3DXSHADER \_ \_Level3 de optimización**</dt> <dt>/O3</dt> </dl>                                    | Nivel de optimización más alto. Producirá el mejor código posible, pero puede tardar mucho más tiempo en hacerlo. Esto será útil para las compilaciones finales de una aplicación donde el rendimiento es el factor más importante.<br/> Direct3D 9: no<br/> Direct3D 10: sí<br/>                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="D3DXSHADER_PARTIALPRECISION"></span><span id="d3dxshader_partialprecision"></span><dl> <dt>**D3DXSHADER \_ PARTIALPRECISION**</dt> <dt>/GPP</dt> </dl>                                             | Fuerce que todos los cálculos del sombreador resultante se produzcan en una precisión parcial. Esto puede dar lugar a una evaluación más rápida de los sombreadores en algún hardware.<br/> Direct3D 9: sí<br/> Direct3D 10: sí<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="D3DXSHADER_PREFER_FLOW_CONTROL"></span><span id="d3dxshader_prefer_flow_control"></span><dl> <dt>**D3DXSHADER \_ PREFERIr \_ \_ control de flujo**</dt> <dt>/GFP</dt> </dl>                                  | Esta es una sugerencia para el compilador para preferir el uso de instrucciones de control de flujo.<br/> Direct3D 9: sí<br/> Direct3D 10: sí<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span id="D3DXSHADER_SKIPOPTIMIZATION"></span><span id="d3dxshader_skipoptimization"></span><dl> <dt>**D3DXSHADER \_ SKIPOPTIMIZATION**</dt> <dt>/OD</dt> </dl>                                              | Indique al compilador que omita los pasos de optimización durante la generación de código. A menos que intente aislar un problema en el código y sospeche el compilador, no se recomienda usar esta opción.<br/> Direct3D 9: sí<br/> Direct3D 10: sí<br/>                                                                                                                                                                                                                                                                                                                                                                               |
| <span id="D3DXSHADER_SKIPVALIDATION"></span><span id="d3dxshader_skipvalidation"></span><dl> <dt>**D3DXSHADER \_ SKIPVALIDATION**</dt> <dt>/Vd</dt> </dl>                                                    | No valide el código generado con respecto a las capacidades y restricciones conocidas. Esta opción solo se recomienda cuando se compilan los sombreadores que se sabe que funcionan (es decir, los sombreadores que se han compilado antes sin esta opción). Los sombreadores siempre se validan mediante el tiempo de ejecución antes de que se establezcan en el dispositivo.<br/> Direct3D 9: sí<br/> Direct3D 10: sí<br/>                                                                                                                                                                                                                                                                      |
| <span id="D3DXSHADER_USE_LEGACY_D3DX9_31_DLL"></span><span id="d3dxshader_use_legacy_d3dx9_31_dll"></span><dl> <dt>**D3DXSHADER \_ USE \_ Legacy \_ D3DX9 \_ 31 \_ dll**</dt> <dt>/LD</dt> </dl>                     | Habilite el uso del compilador HLSL de Direct3D 9 original. OCT2006 \_ d3dx9 \_ 31 \_x86.cab o OCT2006 \_ d3dx9 \_ 31 \_x64.cab deben incluirse como parte de las aplicaciones Redist. Esta marca es necesaria para compilar \_ \_ los sombreadores de PS 1 x sin usar la marca de promoción para PS \_ 2 \_ 0. Al especificar esta marca al obtener una interfaz [**ID3DXEffectCompiler**](id3dxeffectcompiler.md) , se producen llamadas subsiguientes a [**CompileEffect**](id3dxeffectcompiler--compileeffect.md) y [**CompileShader**](id3dxeffectcompiler--compileshader.md) a través de este objeto para usar el compilador heredado.<br/> Direct3D 9: sí<br/> Direct3D 10-no<br/> |



**Marcas de ensamblador**

El sistema de efectos utiliza las marcas de ensamblador para optimizar el sombreador y el código de ensamblado de efecto.



| Constante                                                                                                                                                                                                                        | Descripción                                                                                                                                                                                                                                                                                                              |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="D3DXSHADER_DEBUG"></span><span id="d3dxshader_debug"></span><dl> <dt>**Depuración de D3DXSHADER \_**</dt> </dl>                                                          | Inserte el nombre de archivo de depuración, los números de línea y el tipo y la información de símbolos durante la compilación del sombreador.<br/>                                                                                                                                                                                                                   |
| <span id="D3DXSHADER_FORCE_PS_SOFTWARE_NOOPT"></span><span id="d3dxshader_force_ps_software_noopt"></span><dl> <dt>**D3DXSHADER \_ Force \_ PS \_ software \_ NOOPT**</dt> </dl> | Obligue al compilador a compilar con el siguiente destino de software disponible más alto para los sombreadores de píxeles. Esta marca también desactiva las optimizaciones y la depuración.<br/>                                                                                                                                                  |
| <span id="D3DXSHADER_FORCE_VS_SOFTWARE_NOOPT"></span><span id="d3dxshader_force_vs_software_noopt"></span><dl> <dt>**D3DXSHADER \_ Force \_ vs \_ software \_ NOOPT**</dt> </dl> | Obligue al compilador a compilar con el siguiente destino de software disponible más alto para los sombreadores de vértices. Esta marca también desactiva las optimizaciones y la depuración.<br/>                                                                                                                                                 |
| <span id="D3DXSHADER_SKIPVALIDATION"></span><span id="d3dxshader_skipvalidation"></span><dl> <dt>**D3DXSHADER \_ SKIPVALIDATION**</dt> </dl>                               | No valide el código generado con respecto a las capacidades y restricciones conocidas. Esta opción solo se recomienda cuando se compilan los sombreadores que se sabe que funcionan (es decir, los sombreadores que se han compilado antes sin esta opción). Los sombreadores siempre se validan mediante el tiempo de ejecución antes de que se establezcan en el dispositivo.<br/> |



## <a name="remarks"></a>Observaciones

El sistema del efecto usará **marcas de analizador** cuando las llamen las siguientes funciones:

-   [**D3DXCompileShader**](d3dxcompileshader.md)
-   [**D3DXCompileShaderFromFile**](d3dxcompileshaderfromfile.md)
-   [**D3DXCompileShaderFromResource**](d3dxcompileshaderfromresource.md)
-   [**CompileEffect**](id3dxeffectcompiler--compileeffect.md)

El sistema del efecto usará las **marcas del compilador** cuando las llamen las siguientes funciones:

-   [**D3DXCompileShader**](d3dxcompileshader.md) (o [**D3DXCompileShaderFromFile**](d3dxcompileshaderfromfile.md) o [**D3DXCompileShaderFromResource**](d3dxcompileshaderfromresource.md))
-   [**CompileEffect**](id3dxeffectcompiler--compileeffect.md) (o [**CompileShader**](id3dxeffectcompiler--compileshader.md))

Además, puede usar marcas de **compilador** al crear un efecto llamando [**a D3DXCreateEffect**](d3dxcreateeffect.md) (o [**D3DXCreateEffectFromFile**](d3dxcreateeffectfromfile.md) o [**D3DXCreateEffectFromResource**](d3dxcreateeffectfromresource.md)).

-   Si pasa un archivo. FX sin compilar, el sistema de efectos usará el parámetro de entrada de marca durante la compilación.
-   Si pasa un efecto compilado, el sistema de efectos omitirá las marcas de compilador, ya que no son necesarias para cargar el efecto.

El sistema de efectos utilizará **marcas de ensamblador** cuando las llamen las siguientes funciones:

-   [**D3DXAssembleShader**](d3dxassembleshader.md)
-   [**D3DXAssembleShaderFromFile**](d3dxassembleshaderfromfile.md)
-   [**D3DXAssembleShaderFromResource**](d3dxassembleshaderfromresource.md)

La aplicación de **marcas de compilador** o de **ensamblador** a la API incorrecta producirá un error en la validación del sombreador. Compruebe el valor devuelto por el código de error de Direct3D de la función con la herramienta de búsqueda de errores de DirectX (DXErr.exe) para ayudar a realizar un seguimiento de este error. Puede obtener DXErr.exe y obtener información sobre él desde el SDK de DirectX. Para obtener información sobre el SDK de DirectX, vea [¿Dónde está el SDK de DirectX?](../directx-sdk--august-2009-.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx9shader. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Constantes de D3DX](dx9-graphics-reference-d3dx-constants.md)
</dt> </dl>

 

 
