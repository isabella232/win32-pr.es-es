---
title: Constantes D3DCOMPILE (D3DCompiler. h)
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
ms.openlocfilehash: dfd396eef06260ae879a3bb816d0bd89a078ea53
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104280259"
---
# <a name="d3dcompile-constants"></a>Constantes de D3DCOMPILE

Las constantes D3DCOMPILE especifican cómo el compilador compila el código HLSL.

<dl> <dt>

<span id="D3DCOMPILE_DEBUG"></span><span id="d3dcompile_debug"></span>**Depuración de D3DCOMPILE \_**
</dt> <dd> <dl> <dt>

(1 << 0)
</dt> <dt>



Indica al compilador que inserte información de archivo/línea/tipo/símbolo de depuración en el código de salida.


</dt> </dl> </dd> <dt>

<span id="D3DCOMPILE_SKIP_VALIDATION"></span><span id="d3dcompile_skip_validation"></span>**D3DCOMPILE \_ omitir \_ validación**
</dt> <dd> <dl> <dt>

(1 << 1)
</dt> <dt>



Indica al compilador que no valide el código generado con respecto a las capacidades y restricciones conocidas. Se recomienda usar esta constante solo con los sombreadores que se hayan compilado correctamente en el pasado. DirectX siempre valida los sombreadores antes de que los establezca en un dispositivo.


</dt> </dl> </dd> <dt>

<span id="D3DCOMPILE_SKIP_OPTIMIZATION"></span><span id="d3dcompile_skip_optimization"></span>**D3DCOMPILE \_ omitir \_ optimización**
</dt> <dd> <dl> <dt>

(1 << 2)
</dt> <dt>



Indica al compilador que omita los pasos de optimización durante la generación de código. Se recomienda establecer esta constante solo con fines de depuración.


</dt> </dl> </dd> <dt>

<span id="D3DCOMPILE_PACK_MATRIX_ROW_MAJOR"></span><span id="d3dcompile_pack_matrix_row_major"></span>**\_ \_ \_ Fila \_ principal de la matriz de D3DCOMPILE Pack**
</dt> <dd> <dl> <dt>

(1 << 3)
</dt> <dt>



Indica al compilador que empaquete las matrices en orden de fila principal en la entrada y la salida del sombreador.


</dt> </dl> </dd> <dt>

<span id="D3DCOMPILE_PACK_MATRIX_COLUMN_MAJOR"></span><span id="d3dcompile_pack_matrix_column_major"></span>**Columna de matriz de D3DCOMPILE \_ Pack \_ \_ \_ principal**
</dt> <dd> <dl> <dt>

(1 << 4)
</dt> <dt>



Indica al compilador que empaquete las matrices en el orden principal de la columna en la entrada y la salida del sombreador. Este tipo de empaquetado suele ser más eficaz porque una serie de productos punto puede realizar la multiplicación de matrices vectoriales.


</dt> </dl> </dd> <dt>

<span id="D3DCOMPILE_PARTIAL_PRECISION"></span><span id="d3dcompile_partial_precision"></span>**\_Precisión parcial de D3DCOMPILE \_**
</dt> <dd> <dl> <dt>

(1 << 5)
</dt> <dt>



Indica al compilador que realice todos los cálculos con precisión parcial. Si establece esta constante, el código compilado puede ejecutarse más rápido en el hardware.


</dt> </dl> </dd> <dt>

<span id="D3DCOMPILE_FORCE_VS_SOFTWARE_NO_OPT"></span><span id="d3dcompile_force_vs_software_no_opt"></span>**D3DCOMPILE \_ Force \_ vs \_ software \_ no \_ OPT**
</dt> <dd> <dl> <dt>

(1 << 6)
</dt> <dt>



Indica al compilador que compile un sombreador de vértices para el siguiente perfil de sombreador más alto. Esta constante activa y desactiva la depuración.


</dt> </dl> </dd> <dt>

<span id="D3DCOMPILE_FORCE_PS_SOFTWARE_NO_OPT"></span><span id="d3dcompile_force_ps_software_no_opt"></span>**D3DCOMPILE \_ Force \_ PS \_ software \_ no \_ OPT**
</dt> <dd> <dl> <dt>

(1 << 7)
</dt> <dt>



Indica al compilador que compile un sombreador de píxeles para el siguiente perfil del sombreador más alto. Esta constante también activa y desactiva la depuración.


</dt> </dl> </dd> <dt>

<span id="D3DCOMPILE_NO_PRESHADER"></span><span id="d3dcompile_no_preshader"></span>**D3DCOMPILE \_ sin \_ sombreador**
</dt> <dd> <dl> <dt>

(1 << 8)
</dt> <dt>



Indica al compilador que deshabilite los sombreadores. Si establece esta constante, el compilador no extrae la expresión estática para la evaluación.


</dt> </dl> </dd> <dt>

<span id="D3DCOMPILE_AVOID_FLOW_CONTROL"></span><span id="d3dcompile_avoid_flow_control"></span>**D3DCOMPILE \_ evitar \_ el \_ control de flujo**
</dt> <dd> <dl> <dt>

(1 << 9)
</dt> <dt>



Indica al compilador que no use construcciones de control de flujo siempre que sea posible.


</dt> </dl> </dd> <dt>

<span id="D3DCOMPILE_PREFER_FLOW_CONTROL"></span><span id="d3dcompile_prefer_flow_control"></span>**D3DCOMPILE \_ preferida ( \_ control de flujo) \_**
</dt> <dd> <dl> <dt>

(1 << 10)
</dt> <dt>



Indica al compilador que use construcciones de control de flujo siempre que sea posible.


</dt> </dl> </dd> <dt>

<span id="D3DCOMPILE_ENABLE_STRICTNESS"></span><span id="d3dcompile_enable_strictness"></span>**D3DCOMPILE \_ Habilitar la \_ rigurosidad**
</dt> <dd> <dl> <dt>

(1 << 11)
</dt> <dt>



Fuerza la compilación estricta, que podría no permitir la sintaxis heredada.

De forma predeterminada, el compilador deshabilita la rigurosidad en la sintaxis desusada.


</dt> </dl> </dd> <dt>

<span id="D3DCOMPILE_ENABLE_BACKWARDS_COMPATIBILITY"></span><span id="d3dcompile_enable_backwards_compatibility"></span>**D3DCOMPILE \_ habilitar \_ compatibilidad con versiones anteriores \_**
</dt> <dd> <dl> <dt>

(1 << 12)
</dt> <dt>



Indica al compilador que permita a los sombreadores más antiguos compilar en 5 \_ 0 destinos.


</dt> </dl> </dd> <dt>

<span id="D3DCOMPILE_IEEE_STRICTNESS"></span><span id="d3dcompile_ieee_strictness"></span>**\_Restricción IEEE \_ D3DCOMPILE**
</dt> <dd> <dl> <dt>

(1 << 13)
</dt> <dt>



Fuerza la compilación IEEE STRICT.


</dt> </dl> </dd> <dt>

<span id="D3DCOMPILE_OPTIMIZATION_LEVEL0"></span><span id="d3dcompile_optimization_level0"></span>**D3DCOMPILE \_ optimización de \_ LEVEL0**
</dt> <dd> <dl> <dt>

(1 << 14)
</dt> <dt>



Indica al compilador que use el nivel de optimización más bajo. Si establece esta constante, el compilador puede generar código más lento, pero genera el código más rápidamente. Establezca esta constante cuando desarrolle el sombreador de forma iterativa.


</dt> </dl> </dd> <dt>

<span id="D3DCOMPILE_OPTIMIZATION_LEVEL1"></span><span id="d3dcompile_optimization_level1"></span>**D3DCOMPILE \_ optimización de \_ Level1**
</dt> <dd> <dl> <dt>

0
</dt> <dt>



Indica al compilador que use el segundo nivel de optimización más bajo.


</dt> </dl> </dd> <dt>

<span id="D3DCOMPILE_OPTIMIZATION_LEVEL2"></span><span id="d3dcompile_optimization_level2"></span>**D3DCOMPILE \_ optimización de \_ LEVEL2**
</dt> <dd> <dl> <dt>

((1 << 14) \| (1 << 15))
</dt> <dt>



Indica al compilador que use el segundo nivel de optimización más alto.


</dt> </dl> </dd> <dt>

<span id="D3DCOMPILE_OPTIMIZATION_LEVEL3"></span><span id="d3dcompile_optimization_level3"></span>**D3DCOMPILE \_ optimización de \_ level3**
</dt> <dd> <dl> <dt>

(1 << 15)
</dt> <dt>



Indica al compilador que use el nivel de optimización más alto. Si establece esta constante, el compilador genera el mejor código posible, pero podría tardar mucho más tiempo en hacerlo. Establezca esta constante para las compilaciones finales de una aplicación cuando el rendimiento sea el factor más importante.


</dt> </dl> </dd> <dt>

<span id="D3DCOMPILE_WARNINGS_ARE_ERRORS"></span><span id="d3dcompile_warnings_are_errors"></span>**Las \_ advertencias de D3DCOMPILE \_ son \_ errores**
</dt> <dd> <dl> <dt>

(1 << 18)
</dt> <dt>



Indica al compilador que trate todas las advertencias como errores al compilar el código del sombreador. Se recomienda usar esta constante para el nuevo código de sombreador, de modo que pueda resolver todas las advertencias y reducir el número de defectos de código difíciles de encontrar.


</dt> </dl> </dd> <dt>

<span id="D3DCOMPILE_RESOURCES_MAY_ALIAS"></span><span id="d3dcompile_resources_may_alias"></span>**\_Los recursos de D3DCOMPILE \_ pueden tener \_ alias**
</dt> <dd> <dl> <dt>

(1 << 19)
</dt> <dt>



Indica al compilador que asuma que las vistas de acceso desordenados (UAVs) y las vistas de recursos del sombreador (SRVs) pueden tener alias para CS \_ 5 \_ 0.

> [!Note]  
> Esta constante del compilador es nueva empezando por el \_47.dll D3dcompiler.

 


</dt> </dl> </dd> <dt>

<span id="D3DCOMPILE_ENABLE_UNBOUNDED_DESCRIPTOR_TABLES"></span><span id="d3dcompile_enable_unbounded_descriptor_tables"></span>**D3DCOMPILE \_ habilitar \_ \_ tablas de DESCRIPTOres sin enlazar \_**
</dt> <dd> <dl> <dt>

(1 << 20)
</dt> <dt>



Indica al compilador que habilite las tablas de descriptores sin enlazar.

> [!Note]  
> Esta constante del compilador es nueva empezando por el \_47.dll D3dcompiler.

 


</dt> </dl> </dd> <dt>

<span id="D3DCOMPILE_ALL_RESOURCES_BOUND"></span><span id="d3dcompile_all_resources_bound"></span>**D3DCOMPILE \_ todos \_ los recursos \_ enlazados**
</dt> <dd> <dl> <dt>

(1 << 21)
</dt> <dt>



Dirige el compilador para asegurarse de que todos los recursos están enlazados.

> [!Note]  
> Esta constante del compilador es nueva empezando por el \_47.dll D3dcompiler.

 


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3DCompiler. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Constantes de D3DCompiler](dx-graphics-d3dcompiler-reference-constants.md)
</dt> </dl>

 

 





