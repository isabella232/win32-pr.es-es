---
title: Constantes D3DCOMPILE (D3DCompiler.h)
description: Las constantes D3DCOMPILE especifican cómo el compilador compila el código HLSL.
ms.assetid: 039627DD-D6A4-4EA3-8E91-D2A20770E6FF
topic_type:
- apiref
api_name:
- D3DCOMPILE_DEBUG
- D3DCOMPILE_SKIP_VALIDATION
- D3DCOMPILE_SKIP_OPTIMIZATION
- D3DCOMPILE_PACK_MATRIX_ROW_MAJOR
- D3DCOMPILE_PACK_MATRIX_COLUMN_MAJOR
- D3DCOMPILE_PARTIAL_PRECISION
- D3DCOMPILE_FORCE_VS_SOFTWARE_NO_OPT
- D3DCOMPILE_FORCE_PS_SOFTWARE_NO_OPT
- D3DCOMPILE_NO_PRESHADER
- D3DCOMPILE_AVOID_FLOW_CONTROL
- D3DCOMPILE_PREFER_FLOW_CONTROL
- D3DCOMPILE_ENABLE_STRICTNESS
- D3DCOMPILE_ENABLE_BACKWARDS_COMPATIBILITY
- D3DCOMPILE_IEEE_STRICTNESS
- D3DCOMPILE_OPTIMIZATION_LEVEL0
- D3DCOMPILE_OPTIMIZATION_LEVEL1
- D3DCOMPILE_OPTIMIZATION_LEVEL2
- D3DCOMPILE_OPTIMIZATION_LEVEL3
- D3DCOMPILE_WARNINGS_ARE_ERRORS
- D3DCOMPILE_RESOURCES_MAY_ALIAS
- D3DCOMPILE_ENABLE_UNBOUNDED_DESCRIPTOR_TABLES
- D3DCOMPILE_ALL_RESOURCES_BOUND
api_location:
- D3DCompiler.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: edb48a2293313ce8e29a4b1d16a56954e6baeff1c8467d63f3118327f81abde0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117908765"
---
# <a name="d3dcompile-constants"></a>Constantes D3DCOMPILE

Las constantes D3DCOMPILE especifican cómo el compilador compila el código HLSL.

<dl> <dt>

<span id="D3DCOMPILE_DEBUG"></span><span id="d3dcompile_debug"></span>**D3DCOMPILE \_ DEBUG**
</dt> <dd> <dl> <dt>

(1 << 0)
</dt> <dt>



Dirige al compilador para que inserte información de archivo de depuración, línea, tipo o símbolo en el código de salida.


</dt> </dl> </dd> <dt>

<span id="D3DCOMPILE_SKIP_VALIDATION"></span><span id="d3dcompile_skip_validation"></span>**D3DCOMPILE \_ OMITIR VALIDACIÓN \_**
</dt> <dd> <dl> <dt>

(1 << 1)
</dt> <dt>



Dirige al compilador a no validar el código generado con las funcionalidades y restricciones conocidas. Se recomienda usar esta constante solo con sombreadores que se han compilado correctamente en el pasado. DirectX siempre valida los sombreadores antes de establecerlos en un dispositivo.


</dt> </dl> </dd> <dt>

<span id="D3DCOMPILE_SKIP_OPTIMIZATION"></span><span id="d3dcompile_skip_optimization"></span>**OPTIMIZACIÓN DE SKIP DE D3DCOMPILE \_ \_**
</dt> <dd> <dl> <dt>

(1 << 2)
</dt> <dt>



Dirige al compilador a omitir los pasos de optimización durante la generación de código. Se recomienda establecer esta constante solo con fines de depuración.


</dt> </dl> </dd> <dt>

<span id="D3DCOMPILE_PACK_MATRIX_ROW_MAJOR"></span><span id="d3dcompile_pack_matrix_row_major"></span>**D3DCOMPILE \_ PACK \_ MATRIX \_ ROW \_ MAJOR**
</dt> <dd> <dl> <dt>

(1 << 3)
</dt> <dt>



Dirige al compilador a empaquetar matrices en orden de fila principal en la entrada y salida del sombreador.


</dt> </dl> </dd> <dt>

<span id="D3DCOMPILE_PACK_MATRIX_COLUMN_MAJOR"></span><span id="d3dcompile_pack_matrix_column_major"></span>**D3DCOMPILE \_ PACK \_ MATRIX \_ COLUMN \_ MAJOR**
</dt> <dd> <dl> <dt>

(1 << 4)
</dt> <dt>



Dirige al compilador a empaquetar matrices en orden de columna principal en la entrada y salida del sombreador. Este tipo de empaquetado suele ser más eficaz porque una serie de productos de puntos puede realizar la multiplicación de matrices vectoriales.


</dt> </dl> </dd> <dt>

<span id="D3DCOMPILE_PARTIAL_PRECISION"></span><span id="d3dcompile_partial_precision"></span>**D3DCOMPILE \_ PARTIAL \_ PRECISION**
</dt> <dd> <dl> <dt>

(1 << 5)
</dt> <dt>



Dirige al compilador para que realice todos los cálculos con precisión parcial. Si establece esta constante, el código compilado podría ejecutarse más rápido en algún hardware.


</dt> </dl> </dd> <dt>

<span id="D3DCOMPILE_FORCE_VS_SOFTWARE_NO_OPT"></span><span id="d3dcompile_force_vs_software_no_opt"></span>**D3DCOMPILE \_ FORCE \_ VS \_ SOFTWARE \_ NO \_ OPT**
</dt> <dd> <dl> <dt>

(1 << 6)
</dt> <dt>



Dirige al compilador para compilar un sombreador de vértices para el siguiente perfil de sombreador más alto. Esta constante activa la depuración y desactiva las optimizaciones.


</dt> </dl> </dd> <dt>

<span id="D3DCOMPILE_FORCE_PS_SOFTWARE_NO_OPT"></span><span id="d3dcompile_force_ps_software_no_opt"></span>**D3DCOMPILE \_ FORCE \_ PS \_ SOFTWARE \_ NO \_ OPT**
</dt> <dd> <dl> <dt>

(1 << 7)
</dt> <dt>



Dirige al compilador para compilar un sombreador de píxeles para el siguiente perfil de sombreador más alto. Esta constante también activa la depuración y desactiva las optimizaciones.


</dt> </dl> </dd> <dt>

<span id="D3DCOMPILE_NO_PRESHADER"></span><span id="d3dcompile_no_preshader"></span>**D3DCOMPILE \_ NO \_ PRESHADER**
</dt> <dd> <dl> <dt>

(1 << 8)
</dt> <dt>



Dirige al compilador a deshabilitar preshaders. Si establece esta constante, el compilador no extrae la expresión estática para la evaluación.


</dt> </dl> </dd> <dt>

<span id="D3DCOMPILE_AVOID_FLOW_CONTROL"></span><span id="d3dcompile_avoid_flow_control"></span>**D3DCOMPILE EVITE \_ EL \_ CONTROL DE \_ FLUJO**
</dt> <dd> <dl> <dt>

(1 << 9)
</dt> <dt>



Dirige al compilador para que no use construcciones de control de flujo siempre que sea posible.


</dt> </dl> </dd> <dt>

<span id="D3DCOMPILE_PREFER_FLOW_CONTROL"></span><span id="d3dcompile_prefer_flow_control"></span>**D3DCOMPILE PREFIERE \_ EL \_ CONTROL DE \_ FLUJO**
</dt> <dd> <dl> <dt>

(1 << 10)
</dt> <dt>



Dirige al compilador a usar construcciones de control de flujo siempre que sea posible.


</dt> </dl> </dd> <dt>

<span id="D3DCOMPILE_ENABLE_STRICTNESS"></span><span id="d3dcompile_enable_strictness"></span>**D3DCOMPILE \_ ENABLE \_ STRICTNESS**
</dt> <dd> <dl> <dt>

(1 << 11)
</dt> <dt>



Fuerza la compilación estricta, que podría no permitir la sintaxis heredada.

De forma predeterminada, el compilador deshabilita la estricta sintaxis en desuso.


</dt> </dl> </dd> <dt>

<span id="D3DCOMPILE_ENABLE_BACKWARDS_COMPATIBILITY"></span><span id="d3dcompile_enable_backwards_compatibility"></span>**D3DCOMPILE \_ HABILITACIÓN DE LA \_ COMPATIBILIDAD CON VERSIONES \_ ANTERIORES**
</dt> <dd> <dl> <dt>

(1 << 12)
</dt> <dt>



Dirige al compilador para permitir que los sombreadores más antiguos se compilen en 5 \_ 0 destinos.


</dt> </dl> </dd> <dt>

<span id="D3DCOMPILE_IEEE_STRICTNESS"></span><span id="d3dcompile_ieee_strictness"></span>**D3DCOMPILE \_ IEEE \_ STRICTNESS**
</dt> <dd> <dl> <dt>

(1 << 13)
</dt> <dt>



Fuerza la compilación estricta de IEEE.


</dt> </dl> </dd> <dt>

<span id="D3DCOMPILE_OPTIMIZATION_LEVEL0"></span><span id="d3dcompile_optimization_level0"></span>**D3DCOMPILE \_ OPTIMIZATION \_ LEVEL0**
</dt> <dd> <dl> <dt>

(1 << 14)
</dt> <dt>



Dirige al compilador para que use el nivel de optimización más bajo. Si establece esta constante, el compilador podría generar código más lento, pero lo genera más rápidamente. Establezca esta constante al desarrollar el sombreador de forma iterativa.


</dt> </dl> </dd> <dt>

<span id="D3DCOMPILE_OPTIMIZATION_LEVEL1"></span><span id="d3dcompile_optimization_level1"></span>**D3DCOMPILE \_ OPTIMIZATION \_ LEVEL1**
</dt> <dd> <dl> <dt>

0
</dt> <dt>



Dirige al compilador para que use el segundo nivel de optimización más bajo.


</dt> </dl> </dd> <dt>

<span id="D3DCOMPILE_OPTIMIZATION_LEVEL2"></span><span id="d3dcompile_optimization_level2"></span>**D3DCOMPILE \_ OPTIMIZATION \_ LEVEL2**
</dt> <dd> <dl> <dt>

((1 << 14) \| (1 << 15))
</dt> <dt>



Dirige al compilador para que use el segundo nivel de optimización más alto.


</dt> </dl> </dd> <dt>

<span id="D3DCOMPILE_OPTIMIZATION_LEVEL3"></span><span id="d3dcompile_optimization_level3"></span>**D3DCOMPILE \_ OPTIMIZATION \_ LEVEL3**
</dt> <dd> <dl> <dt>

(1 << 15)
</dt> <dt>



Dirige al compilador para que use el nivel de optimización más alto. Si establece esta constante, el compilador genera el mejor código posible, pero puede tardar mucho más tiempo en hacerlo. Establezca esta constante para las compilaciones finales de una aplicación cuando el rendimiento sea el factor más importante.


</dt> </dl> </dd> <dt>

<span id="D3DCOMPILE_WARNINGS_ARE_ERRORS"></span><span id="d3dcompile_warnings_are_errors"></span>**LAS ADVERTENCIAS DE D3DCOMPILE \_ \_ SON \_ ERRORES**
</dt> <dd> <dl> <dt>

(1 << 18)
</dt> <dt>



Dirige al compilador a tratar todas las advertencias como errores cuando compila el código del sombreador. Se recomienda usar esta constante para el nuevo código de sombreador, de modo que pueda resolver todas las advertencias y reducir el número de defectos de código difíciles de encontrar.


</dt> </dl> </dd> <dt>

<span id="D3DCOMPILE_RESOURCES_MAY_ALIAS"></span><span id="d3dcompile_resources_may_alias"></span>**LOS RECURSOS D3DCOMPILE \_ \_ PUEDEN SER \_ ALIAS**
</dt> <dd> <dl> <dt>

(1 << 19)
</dt> <dt>



Ordena al compilador que suponga que las vistas de acceso desordenado (UAV) y las vistas de recursos de sombreador (SRV) pueden tener alias para cs \_ 5 \_ 0.

> [!Note]  
> Esta constante del compilador es nueva a partir de D3dcompiler \_47.dll.

 


</dt> </dl> </dd> <dt>

<span id="D3DCOMPILE_ENABLE_UNBOUNDED_DESCRIPTOR_TABLES"></span><span id="d3dcompile_enable_unbounded_descriptor_tables"></span>**D3DCOMPILE \_ HABILITACIÓN \_ DE TABLAS DE DESCRIPTORES SIN \_ \_ ENLAZAR**
</dt> <dd> <dl> <dt>

(1 << 20)
</dt> <dt>



Dirige al compilador para habilitar las tablas de descriptores sin enlazar.

> [!Note]  
> Esta constante del compilador es nueva a partir de D3dcompiler \_47.dll.

 


</dt> </dl> </dd> <dt>

<span id="D3DCOMPILE_ALL_RESOURCES_BOUND"></span><span id="d3dcompile_all_resources_bound"></span>**D3DCOMPILE TODOS \_ LOS \_ RECURSOS \_ ENLAZADOS**
</dt> <dd> <dl> <dt>

(1 << 21)
</dt> <dt>



Dirige al compilador para asegurarse de que todos los recursos están enlazados.

> [!Note]  
> Esta constante del compilador es nueva a partir de D3dcompiler \_47.dll.

 


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3DCompiler.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Constantes D3DCompiler](dx-graphics-d3dcompiler-reference-constants.md)
</dt> </dl>

 

 





