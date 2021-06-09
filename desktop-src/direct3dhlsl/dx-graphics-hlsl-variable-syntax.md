---
title: Sintaxis de variables
description: Use las siguientes reglas de sintaxis para declarar variables HLSL.
ms.assetid: 684c42d1-2dd4-42e1-9cff-580edb5c6bcd
keywords:
- extern, sintaxis de variables (HLSL de DirectX)
- nointerpolation, sintaxis de variables (HLSL de DirectX)
- shared, Sintaxis de variables (HLSL de DirectX)
- groupshared, sintaxis de variables (HLSL de DirectX)
- static, sintaxis variable (HLSL de DirectX)
- sintaxis uniforme de variables (HLSL de DirectX)
- volatile, variable syntax (DirectX HLSL)
- sintaxis precisa de variables (HLSL de DirectX)
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 446444e09b0b6aff3e0ba8ca8b12cfbf6dc94128
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/09/2021
ms.locfileid: "111826073"
---
# <a name="variable-syntax"></a><span data-ttu-id="acc60-111">Sintaxis de variables</span><span class="sxs-lookup"><span data-stu-id="acc60-111">Variable Syntax</span></span>

<span data-ttu-id="acc60-112">Use las siguientes reglas de sintaxis para declarar variables HLSL.</span><span class="sxs-lookup"><span data-stu-id="acc60-112">Use the following syntax rules to declare HLSL variables.</span></span>

<span data-ttu-id="acc60-113">\[*Almacenamiento \_ Class* \] \[ *Type \_ Modifier* \] *Type Name* \[ *Index* \] \[ *: Semantic*: \] \[ *Packoffset*: \] \[ *Register* \] ;    \[  \] Anotaciones \[ *= Inicial \_ Valor*                    \]</span><span class="sxs-lookup"><span data-stu-id="acc60-113">\[*Storage\_Class*\] \[*Type\_Modifier*\] *Type Name*\[*Index*\]     \[*: Semantic*\]     \[*: Packoffset*\]     \[*: Register*\];    \[*Annotations*\]     \[*= Initial\_Value*\]</span></span>



 

## <a name="parameters"></a><span data-ttu-id="acc60-114">Parámetros</span><span class="sxs-lookup"><span data-stu-id="acc60-114">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="acc60-115"><span id="Storage_Class_"></span><span id="storage_class_"></span><span id="STORAGE_CLASS_"></span>*Clase de \_ almacenamiento*</span><span class="sxs-lookup"><span data-stu-id="acc60-115"><span id="Storage_Class_"></span><span id="storage_class_"></span><span id="STORAGE_CLASS_"></span>*Storage\_Class*</span></span> 
</dt> <dd>

<span data-ttu-id="acc60-116">Modificadores opcionales de clase de almacenamiento que dan al compilador sugerencias sobre el ámbito y la duración de las variables; Los modificadores se pueden especificar en cualquier orden.</span><span class="sxs-lookup"><span data-stu-id="acc60-116">Optional storage-class modifiers that give the compiler hints about variable scope and lifetime; the modifiers can be specified in any order.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="acc60-117">Valor</span><span class="sxs-lookup"><span data-stu-id="acc60-117">Value</span></span></th>
<th><span data-ttu-id="acc60-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="acc60-118">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="acc60-119"><strong>extern</strong></span><span class="sxs-lookup"><span data-stu-id="acc60-119"><strong>extern</strong></span></span></td>
<td><span data-ttu-id="acc60-120">Marcar una variable global como una entrada externa al sombreador; este es el marcado predeterminado para todas las variables globales.</span><span class="sxs-lookup"><span data-stu-id="acc60-120">Mark a global variable as an external input to the shader; this is the default marking for all global variables.</span></span> <span data-ttu-id="acc60-121">No se puede combinar con <strong>estático.</strong></span><span class="sxs-lookup"><span data-stu-id="acc60-121">Cannot be combined with <strong>static</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="acc60-122"><strong>nointerpolation</strong></span><span class="sxs-lookup"><span data-stu-id="acc60-122"><strong>nointerpolation</strong></span></span></td>
<td><span data-ttu-id="acc60-123">No interpola las salidas de un sombreador de vértices antes de pasarlas a un sombreador de píxeles.</span><span class="sxs-lookup"><span data-stu-id="acc60-123">Do not interpolate the outputs of a vertex shader before passing them to a pixel shader.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="acc60-124"><strong>Precisa</strong></span><span class="sxs-lookup"><span data-stu-id="acc60-124"><strong>precise</strong></span></span></td>
<td><span data-ttu-id="acc60-125">La <strong>palabra</strong> clave precisa cuando se aplica a una variable restringirá los cálculos usados para generar el valor asignado a esa variable de las maneras siguientes:</span><span class="sxs-lookup"><span data-stu-id="acc60-125">The <strong>precise</strong> keyword when applied to a variable will restrict any calculations used to produce the value assigned to that variable in the following ways:</span></span>

*   <span data-ttu-id="acc60-126">Las operaciones independientes se mantienen independientes.</span><span class="sxs-lookup"><span data-stu-id="acc60-126">Separate operations are kept separate.</span></span> <span data-ttu-id="acc60-127">Por ejemplo, cuando una operación mul y add se podrían haber fusionado en una operación loca, <strong>la</strong> precisión obliga a que las operaciones permanezcan independientes.</span><span class="sxs-lookup"><span data-stu-id="acc60-127">For example, where a mul and add operation might have been fused into a mad operation, <strong>precise</strong> forces the operations to remain separate.</span></span> <span data-ttu-id="acc60-128">En su lugar, debe usar explícitamente la función intrínseca loca.</span><span class="sxs-lookup"><span data-stu-id="acc60-128">Instead, you must explicitly use the mad intrinsic function.</span></span>
*   <span data-ttu-id="acc60-129">Se mantiene el orden de las operaciones.</span><span class="sxs-lookup"><span data-stu-id="acc60-129">Order of operations are maintained.</span></span> <span data-ttu-id="acc60-130">Cuando el orden de las instrucciones podría haber sido aleatorio para mejorar el rendimiento, <strong>la</strong> precisión garantiza que el compilador conserva el orden tal y como está escrito.</span><span class="sxs-lookup"><span data-stu-id="acc60-130">Where the order of instructions might have been shuffled to improve performance, <strong>precise</strong> ensures that the compiler preserves the order as written.</span></span>
*   <span data-ttu-id="acc60-131">Las operaciones ieee no seguras están restringidas.</span><span class="sxs-lookup"><span data-stu-id="acc60-131">IEEE unsafe operations are restricted.</span></span> <span data-ttu-id="acc60-132">Cuando el compilador podría haber usado operaciones matemáticas rápidas que no tienen en cuenta <strong></strong> los valores NaN (no un número) e INF (infinito), la precisión obliga a respetar los requisitos ieee relativos a los valores NaN e INF.</span><span class="sxs-lookup"><span data-stu-id="acc60-132">Where the compiler might have used fast math operations that don't account for NaN (not a number) and INF (infinite) values, <strong>precise</strong> forces IEEE requirements concerning NaN and INF values to be respected.</span></span> <span data-ttu-id="acc60-133">Sin <strong>precisión,</strong>estas optimizaciones y operaciones matemáticas no son seguras para IEEE.</span><span class="sxs-lookup"><span data-stu-id="acc60-133">Without <strong>precise</strong>, these optimizations and mathematical operations are not IEEE safe.</span></span>
*   <span data-ttu-id="acc60-134">Calificar una variable <strong>precisa</strong> no realiza operaciones que usan la variable <strong>precisa.</strong></span><span class="sxs-lookup"><span data-stu-id="acc60-134">Qualifying a variable <strong>precise</strong> doesn't make operations that use the variable <strong>precise</strong>.</span></span> <span data-ttu-id="acc60-135">Dado <strong></strong> que la precisión solo se propaga a las <strong></strong>operaciones que contribuyen a los valores asignados a la variable precisa- calificado, realizar correctamente los <strong>cálculos</strong> deseados con precisión puede ser complicado, por lo que se recomienda marcar las <strong>salidas</strong> del sombreador directamente donde se declaran, ya sea en un campo de estructura, en un parámetro de salida o en el tipo de valor devuelto de la función de entrada.</span><span class="sxs-lookup"><span data-stu-id="acc60-135">Since <strong>precise</strong> propagates only to operations that contribute to the values that are assigned to the <strong>precise</strong>-qualified variable, correctly making desired calculations <strong>precise</strong> can be tricky, so we recommended that you mark the shader outputs <strong>precise</strong> directly where you declare them, whether that's on a structure field, or on an output parameter, or the return type of the entry function.</span></span>

<span data-ttu-id="acc60-136">La capacidad de controlar las optimizaciones de esta manera mantiene la invariable de resultados para la variable de salida modificada al deshabilitar las optimizaciones que podrían afectar a los resultados finales debido a diferencias en las diferencias de precisión acumuladas.</span><span class="sxs-lookup"><span data-stu-id="acc60-136">The ability to control optimizations in this way maintains result invariance for the modified output variable by disabling optimizations that might affect final results due to differences in accumulated precision differences.</span></span> <span data-ttu-id="acc60-137">Resulta útil cuando se desea que los sombreadores para la teselación mantengan las juntas de revisión estrechas al agua o coincidan con los valores de profundidad en varios pases.</span><span class="sxs-lookup"><span data-stu-id="acc60-137">It is useful when you want shaders for tessellation to maintain water-tight patch seams or match depth values over multiple passes.</span></span>

<span data-ttu-id="acc60-138">[Código de ejemplo:](https://github.com/microsoft/DirectXShaderCompiler/blob/master/tools/clang/test/HLSLFileCheck/hlsl/types/modifiers/precise/precise4.hlsl)</span><span class="sxs-lookup"><span data-stu-id="acc60-138">[Sample code](https://github.com/microsoft/DirectXShaderCompiler/blob/master/tools/clang/test/HLSLFileCheck/hlsl/types/modifiers/precise/precise4.hlsl):</span></span> 
```HLSL
matrix g_mWorldViewProjection;
void main(in float3 InPos : Position, out precise float4 OutPos : SV_Position)
{
  // operation is precise because it contributes to the precise parameter OutPos
  OutPos = mul( float4( InPos, 1.0 ), g_mWorldViewProjection );
}
```
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="acc60-139"><strong>Compartido</strong></span><span class="sxs-lookup"><span data-stu-id="acc60-139"><strong>shared</strong></span></span></td>
<td><span data-ttu-id="acc60-140">Marcar una variable para compartir entre efectos; se trata de una sugerencia para el compilador.</span><span class="sxs-lookup"><span data-stu-id="acc60-140">Mark a variable for sharing between effects; this is a hint to the compiler.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="acc60-141"><strong>groupshared</strong></span><span class="sxs-lookup"><span data-stu-id="acc60-141"><strong>groupshared</strong></span></span></td>
<td><span data-ttu-id="acc60-142">Marque una variable para la memoria compartida de grupo de subprocesos para sombreadores de proceso.</span><span class="sxs-lookup"><span data-stu-id="acc60-142">Mark a variable for thread-group-shared memory for compute shaders.</span></span> <span data-ttu-id="acc60-143">En D3D10, el tamaño total máximo de todas las variables con la clase de almacenamiento groupshared es de 16 kb, en D3D11 el tamaño máximo es de 32 kb.</span><span class="sxs-lookup"><span data-stu-id="acc60-143">In D3D10 the maximum total size of all variables with the groupshared storage class is 16kb, in D3D11 the maximum size is 32kb.</span></span> <span data-ttu-id="acc60-144">Consulte los ejemplos.</span><span class="sxs-lookup"><span data-stu-id="acc60-144">See examples.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="acc60-145"><strong>static</strong></span><span class="sxs-lookup"><span data-stu-id="acc60-145"><strong>static</strong></span></span></td>
<td><span data-ttu-id="acc60-146">Marque una variable local para que se inicialice una vez y persista entre las llamadas de función.</span><span class="sxs-lookup"><span data-stu-id="acc60-146">Mark a local variable so that it is initialized one time and persists between function calls.</span></span> <span data-ttu-id="acc60-147">Si la declaración no incluye un inicializador, el valor se establece en cero.</span><span class="sxs-lookup"><span data-stu-id="acc60-147">If the declaration does not include an initializer, the value is set to zero.</span></span> <span data-ttu-id="acc60-148">Una variable global marcada <strong>como estática</strong> no es visible para una aplicación.</span><span class="sxs-lookup"><span data-stu-id="acc60-148">A global variable marked <strong>static</strong> is not visible to an application.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="acc60-149"><strong>uniforme</strong></span><span class="sxs-lookup"><span data-stu-id="acc60-149"><strong>uniform</strong></span></span></td>
<td><span data-ttu-id="acc60-150">Marcar una variable cuyos datos son constantes durante la ejecución de un sombreador (por ejemplo, un color de material en un sombreador de vértices); Las variables globales se consideran <strong>uniformes de</strong> forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="acc60-150">Mark a variable whose data is constant throughout the execution of a shader (such as a material color in a vertex shader); global variables are considered <strong>uniform</strong> by default.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="acc60-151"><strong>volatile</strong></span><span class="sxs-lookup"><span data-stu-id="acc60-151"><strong>volatile</strong></span></span></td>
<td><span data-ttu-id="acc60-152">Marcar una variable que cambia con frecuencia; se trata de una sugerencia para el compilador.</span><span class="sxs-lookup"><span data-stu-id="acc60-152">Mark a variable that changes frequently; this is a hint to the compiler.</span></span> <span data-ttu-id="acc60-153">Este modificador de clase de almacenamiento solo se aplica a una variable local.</span><span class="sxs-lookup"><span data-stu-id="acc60-153">This storage class modifier only applies to a local variable.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="acc60-154">El compilador HLSL omite actualmente este modificador de clase de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="acc60-154">The HLSL compiler currently ignores this storage class modifier.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span data-ttu-id="acc60-155"><span id="Type_Modifier"></span><span id="type_modifier"></span><span id="TYPE_MODIFIER"></span>*Modificador de \_ tipo*</span><span class="sxs-lookup"><span data-stu-id="acc60-155"><span id="Type_Modifier"></span><span id="type_modifier"></span><span id="TYPE_MODIFIER"></span>*Type\_Modifier*</span></span>
</dt> <dd>

<span data-ttu-id="acc60-156">Modificador de tipo variable opcional.</span><span class="sxs-lookup"><span data-stu-id="acc60-156">Optional variable-type modifier.</span></span>



| <span data-ttu-id="acc60-157">Valor</span><span class="sxs-lookup"><span data-stu-id="acc60-157">Value</span></span>             | <span data-ttu-id="acc60-158">Descripción</span><span class="sxs-lookup"><span data-stu-id="acc60-158">Description</span></span>                                                                                                                                                                                                                                  |
|-------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="acc60-159">**const**</span><span class="sxs-lookup"><span data-stu-id="acc60-159">**const**</span></span>         | <span data-ttu-id="acc60-160">Marque una variable que un sombreador no pueda cambiar; por lo tanto, debe inicializarse en la declaración de variable.</span><span class="sxs-lookup"><span data-stu-id="acc60-160">Mark a variable that cannot be changed by a shader, therefore, it must be initialized in the variable declaration.</span></span> <span data-ttu-id="acc60-161">Las variables globales se consideran **const** de forma predeterminada (suprima este comportamiento al proporcionar la marca /Gec al compilador).</span><span class="sxs-lookup"><span data-stu-id="acc60-161">Global variables are considered **const** by default (suppress this behavior by supplying the /Gec flag to the compiler).</span></span> |
| <span data-ttu-id="acc60-162">**fila \_ principal**</span><span class="sxs-lookup"><span data-stu-id="acc60-162">**row\_major**</span></span>    | <span data-ttu-id="acc60-163">Marque una variable que almacene cuatro componentes en una sola fila para que se puedan almacenar en un único registro constante.</span><span class="sxs-lookup"><span data-stu-id="acc60-163">Mark a variable that stores four components in a single row so they can be stored in a single constant register.</span></span>                                                                                                                             |
| <span data-ttu-id="acc60-164">**columna \_ principal**</span><span class="sxs-lookup"><span data-stu-id="acc60-164">**column\_major**</span></span> | <span data-ttu-id="acc60-165">Marque una variable que almacena 4 componentes en una sola columna para optimizar los cálculos matemáticos de matriz.</span><span class="sxs-lookup"><span data-stu-id="acc60-165">Mark a variable that stores 4 components in a single column to optimize matrix math.</span></span>                                                                                                                                                         |



 

> [!Note]  
> <span data-ttu-id="acc60-166">Si no especifica un valor de modificador de tipo, el compilador usa la columna **\_ principal** como valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="acc60-166">If you do not specify a type-modifier value, the compiler uses **column\_major** as the default value.</span></span>

 

</dd> <dt>

<span data-ttu-id="acc60-167"><span id="Type"></span><span id="type"></span><span id="TYPE"></span>*Tipo*</span><span class="sxs-lookup"><span data-stu-id="acc60-167"><span id="Type"></span><span id="type"></span><span id="TYPE"></span>*Type*</span></span>
</dt> <dd>

<span data-ttu-id="acc60-168">Cualquier tipo HLSL enumerado en [Tipos de datos (HlSL de DirectX)](dx-graphics-hlsl-data-types.md).</span><span class="sxs-lookup"><span data-stu-id="acc60-168">Any HLSL type listed in [Data Types (DirectX HLSL)](dx-graphics-hlsl-data-types.md).</span></span>

</dd> <dt>

<span data-ttu-id="acc60-169"><span id="Name_Index_"></span><span id="name_index_"></span><span id="NAME_INDEX_"></span>*Nombre* \[ *Índice*\]</span><span class="sxs-lookup"><span data-stu-id="acc60-169"><span id="Name_Index_"></span><span id="name_index_"></span><span id="NAME_INDEX_"></span>*Name*\[*Index*\]</span></span>
</dt> <dd>

<span data-ttu-id="acc60-170">Cadena ASCII que identifica de forma única una variable de sombreador.</span><span class="sxs-lookup"><span data-stu-id="acc60-170">ASCII string that uniquely identifies a shader variable.</span></span> <span data-ttu-id="acc60-171">Para definir una matriz opcional, use **index para** el tamaño de la matriz, que es un entero positivo = 1.</span><span class="sxs-lookup"><span data-stu-id="acc60-171">To define an optional array, use **index** for the array size, which is a positive integer = 1.</span></span>

</dd> <dt>

<span data-ttu-id="acc60-172"><span id="Semantic"></span><span id="semantic"></span><span id="SEMANTIC"></span>*Semántica*</span><span class="sxs-lookup"><span data-stu-id="acc60-172"><span id="Semantic"></span><span id="semantic"></span><span id="SEMANTIC"></span>*Semantic*</span></span>
</dt> <dd>

<span data-ttu-id="acc60-173">Información de uso de parámetros opcional, utilizada por el compilador para vincular entradas y salidas del sombreador.</span><span class="sxs-lookup"><span data-stu-id="acc60-173">Optional parameter-usage information, used by the compiler to link shader inputs and outputs.</span></span> <span data-ttu-id="acc60-174">Hay varias semánticas [predefinidas para sombreadores](dx-graphics-hlsl-semantics.md) de vértices y píxeles.</span><span class="sxs-lookup"><span data-stu-id="acc60-174">There are several predefined [semantics](dx-graphics-hlsl-semantics.md) for vertex and pixel shaders.</span></span> <span data-ttu-id="acc60-175">El compilador omite la semántica a menos que se declaren en una variable global o un parámetro pasado a un sombreador.</span><span class="sxs-lookup"><span data-stu-id="acc60-175">The compiler ignores semantics unless they are declared on a global variable, or a parameter passed into a shader.</span></span>

</dd> <dt>

<span data-ttu-id="acc60-176"><span id="Packoffset"></span><span id="packoffset"></span><span id="PACKOFFSET"></span>*Packoffset*</span><span class="sxs-lookup"><span data-stu-id="acc60-176"><span id="Packoffset"></span><span id="packoffset"></span><span id="PACKOFFSET"></span>*Packoffset*</span></span>
</dt> <dd>

<span data-ttu-id="acc60-177">Palabra clave opcional para empaquetar manualmente las constantes del sombreador.</span><span class="sxs-lookup"><span data-stu-id="acc60-177">Optional keyword for manually packing shader constants.</span></span> <span data-ttu-id="acc60-178">Consulte [packoffset (DirectX HLSL).](dx-graphics-hlsl-variable-packoffset.md)</span><span class="sxs-lookup"><span data-stu-id="acc60-178">See [packoffset (DirectX HLSL)](dx-graphics-hlsl-variable-packoffset.md).</span></span>

</dd> <dt>

<span data-ttu-id="acc60-179"><span id="Register"></span><span id="register"></span><span id="REGISTER"></span>*Registro*</span><span class="sxs-lookup"><span data-stu-id="acc60-179"><span id="Register"></span><span id="register"></span><span id="REGISTER"></span>*Register*</span></span>
</dt> <dd>

<span data-ttu-id="acc60-180">Palabra clave opcional para asignar manualmente una variable de sombreador a un registro determinado.</span><span class="sxs-lookup"><span data-stu-id="acc60-180">Optional keyword for manually assigning a shader variable to a particular register.</span></span> <span data-ttu-id="acc60-181">Vea [register (DirectX HLSL).](dx-graphics-hlsl-variable-register.md)</span><span class="sxs-lookup"><span data-stu-id="acc60-181">See [register (DirectX HLSL)](dx-graphics-hlsl-variable-register.md).</span></span>

</dd> <dt>

<span data-ttu-id="acc60-182"><span id="Annotation_s_"></span><span id="annotation_s_"></span><span id="ANNOTATION_S_"></span>*Anotaciones*</span><span class="sxs-lookup"><span data-stu-id="acc60-182"><span id="Annotation_s_"></span><span id="annotation_s_"></span><span id="ANNOTATION_S_"></span>*Annotation(s)*</span></span>
</dt> <dd>

<span data-ttu-id="acc60-183">Metadatos opcionales, en forma de cadena, asociados a una variable global.</span><span class="sxs-lookup"><span data-stu-id="acc60-183">Optional metadata, in the form of a string, attached to a global variable.</span></span> <span data-ttu-id="acc60-184">La plataforma de efectos usa una anotación y HLSL la omite; Para ver una sintaxis más detallada, consulte la [sintaxis de anotación](/windows/desktop/direct3d10/d3d10-effect-annotation-syntax).</span><span class="sxs-lookup"><span data-stu-id="acc60-184">An annotation is used by the effect framework and ignored by HLSL; to see more detailed syntax, see [annotation syntax](/windows/desktop/direct3d10/d3d10-effect-annotation-syntax).</span></span>

</dd> <dt>

<span data-ttu-id="acc60-185"><span id="Initial_Value"></span><span id="initial_value"></span><span id="INITIAL_VALUE"></span>*Valor \_ inicial*</span><span class="sxs-lookup"><span data-stu-id="acc60-185"><span id="Initial_Value"></span><span id="initial_value"></span><span id="INITIAL_VALUE"></span>*Initial\_Value*</span></span>
</dt> <dd>

<span data-ttu-id="acc60-186">Valores iniciales opcionales; el número de valores debe coincidir con el número de componentes de *Tipo*.</span><span class="sxs-lookup"><span data-stu-id="acc60-186">Optional initial value(s); the number of values should match the number of components in *Type*.</span></span> <span data-ttu-id="acc60-187">Cada variable global marcada **como extern** debe inicializarse con un valor literal; cada variable marcada **como estática** debe inicializarse con una constante.</span><span class="sxs-lookup"><span data-stu-id="acc60-187">Each global variable marked **extern** must be initialized with a literal value; each variable marked **static** must be initialized with a constant.</span></span>

<span data-ttu-id="acc60-188">Las variables globales que no están marcadas **como static** o **extern** no se compilan en el sombreador.</span><span class="sxs-lookup"><span data-stu-id="acc60-188">Global variables that are not marked **static** or **extern** are not compiled into the shader.</span></span> <span data-ttu-id="acc60-189">El compilador no establece automáticamente los valores predeterminados para las variables globales y no puede usarlos en las optimizaciones.</span><span class="sxs-lookup"><span data-stu-id="acc60-189">The compiler does not automatically set default values for global variables and cannot use them in optimizations.</span></span> <span data-ttu-id="acc60-190">Para inicializar este tipo de variable global, use la reflexión para obtener su valor y, a continuación, copie el valor en un búfer constante.</span><span class="sxs-lookup"><span data-stu-id="acc60-190">To initialize this type of global variable, use reflection to get its value and then copy the value to a constant buffer.</span></span> <span data-ttu-id="acc60-191">Por ejemplo, puede usar el método [**ID3D11ShaderReflection::GetVariableByName**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11shaderreflection-getvariablebyname) para obtener la variable, usar el método [**ID3D11ShaderReflectionVariable::GetDesc**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11shaderreflectionvariable-getdesc) para obtener la descripción de la variable de sombreador y obtener el valor inicial del miembro **DefaultValue** de la estructura [**D3D11 \_ SHADER VARIABLE \_ \_ DESC.**](/windows/desktop/api/d3d11shader/ns-d3d11shader-d3d11_shader_variable_desc)</span><span class="sxs-lookup"><span data-stu-id="acc60-191">For example, you can use the [**ID3D11ShaderReflection::GetVariableByName**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11shaderreflection-getvariablebyname) method to get the variable, use the [**ID3D11ShaderReflectionVariable::GetDesc**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11shaderreflectionvariable-getdesc) method to get the shader-variable description, and get the initial value from the **DefaultValue** member of the [**D3D11\_SHADER\_VARIABLE\_DESC**](/windows/desktop/api/d3d11shader/ns-d3d11shader-d3d11_shader_variable_desc) structure.</span></span> <span data-ttu-id="acc60-192">Para copiar el valor en el búfer constante, debe asegurarse de que el búfer se creó con acceso de escritura de CPU [**(D3D11 \_ CPU \_ ACCESS \_ WRITE**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_cpu_access_flag)).</span><span class="sxs-lookup"><span data-stu-id="acc60-192">To copy the value to the constant buffer, you must ensure that the buffer was created with CPU write access ([**D3D11\_CPU\_ACCESS\_WRITE**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_cpu_access_flag)).</span></span> <span data-ttu-id="acc60-193">Para obtener más información sobre cómo crear un búfer constante, [vea Cómo: Crear un búfer constante.](/windows/desktop/direct3d11/overviews-direct3d-11-resources-buffers-constant-how-to)</span><span class="sxs-lookup"><span data-stu-id="acc60-193">For more information about how to create a constant buffer, see [How to: Create a Constant Buffer](/windows/desktop/direct3d11/overviews-direct3d-11-resources-buffers-constant-how-to).</span></span>

<span data-ttu-id="acc60-194">También puede usar el marco [de efectos para](../direct3d11/d3d11-graphics-programming-guide-effects.md) procesar automáticamente el reflejo y establecer el valor inicial.</span><span class="sxs-lookup"><span data-stu-id="acc60-194">You can also use the [effects framework](../direct3d11/d3d11-graphics-programming-guide-effects.md) to automatically process the reflecting and setting the initial value.</span></span> <span data-ttu-id="acc60-195">Por ejemplo, puede usar el [**método ID3DX11EffectPass::Apply.**](/windows/desktop/direct3d11/id3dx11effectpass-apply)</span><span class="sxs-lookup"><span data-stu-id="acc60-195">For example, you can use the [**ID3DX11EffectPass::Apply**](/windows/desktop/direct3d11/id3dx11effectpass-apply) method.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="acc60-196">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="acc60-196">Examples</span></span>

<span data-ttu-id="acc60-197">Estos son varios ejemplos de declaraciones de variable de sombreador.</span><span class="sxs-lookup"><span data-stu-id="acc60-197">Here are several examples of shader-variable declarations.</span></span>


```
float fVar;
```




```
float4 color;
float fVar = 3.1f;

int iVar[3];

int iVar[3] = {1,2,3};

uniform float4 position : SV_POSITION; 
const float4 lightDirection = {0,0,1};
      
```



### <a name="group-shared"></a><span data-ttu-id="acc60-198">Grupo compartido</span><span class="sxs-lookup"><span data-stu-id="acc60-198">Group Shared</span></span>

<span data-ttu-id="acc60-199">HLSL permite a los subprocesos de un sombreador de proceso intercambiar valores a través de memoria compartida.</span><span class="sxs-lookup"><span data-stu-id="acc60-199">HLSL enables threads of a compute shader to exchange values via shared memory.</span></span> <span data-ttu-id="acc60-200">HLSL proporciona primitivas de barrera como [**GroupMemoryBarhlWithGroupSync,**](groupmemorybarrierwithgroupsync.md)y así sucesivamente para garantizar el orden correcto de las lecturas y escrituras en la memoria compartida en el sombreador y evitar carreras de datos.</span><span class="sxs-lookup"><span data-stu-id="acc60-200">HLSL provides barrier primitives such as [**GroupMemoryBarrierWithGroupSync**](groupmemorybarrierwithgroupsync.md), and so on to ensure the correct ordering of reads and writes to shared memory in the shader and to avoid data races.</span></span>

> [!Note]  
> <span data-ttu-id="acc60-201">El hardware ejecuta subprocesos en grupos (deformes o frentes de onda), y la sincronización de barreras a veces se puede omitir para aumentar el rendimiento cuando solo la sincronización de subprocesos que pertenecen al mismo grupo es correcta.</span><span class="sxs-lookup"><span data-stu-id="acc60-201">Hardware executes threads in groups (warps or wave-fronts), and barrier synchronization can sometimes be omitted to increase performance when only synchronizing threads that belong to the same group is correct.</span></span> <span data-ttu-id="acc60-202">Pero se desaconseja esta omisión por estos motivos:</span><span class="sxs-lookup"><span data-stu-id="acc60-202">But we highly discourage this omission for these reasons:</span></span>
>
> -   <span data-ttu-id="acc60-203">Esta omisión da como resultado código no portátil, que podría no funcionar en algún hardware y no funciona en rasterizadores de software que normalmente ejecutan subprocesos en grupos más pequeños.</span><span class="sxs-lookup"><span data-stu-id="acc60-203">This omission results in non-portable code, which might not work on some hardware and doesn't work on software rasterizers that typically execute threads in smaller groups.</span></span>
> -   <span data-ttu-id="acc60-204">Las mejoras de rendimiento que podría lograr con esta omisión serán menores en comparación con el uso de la barrera de todos los subprocesos.</span><span class="sxs-lookup"><span data-stu-id="acc60-204">The performance improvements that you might achieve with this omission will be minor compared to using all-thread barrier.</span></span>

 

<span data-ttu-id="acc60-205">En Direct3D 10 no hay ninguna sincronización de subprocesos al escribir en **groupshared,** por lo que esto significa que cada subproceso se limita a una sola ubicación en una matriz para escribir.</span><span class="sxs-lookup"><span data-stu-id="acc60-205">In Direct3D 10 there is no synchronization of threads when writing to **groupshared**, so this means that each thread is limited to a single location in an array for writing.</span></span> <span data-ttu-id="acc60-206">Use el [valor del \_ sistema GroupIndex](dx-graphics-hlsl-semantics.md) de SV para indexar en esta matriz al escribir para asegurarse de que no pueden colisionar dos subprocesos.</span><span class="sxs-lookup"><span data-stu-id="acc60-206">Use the [SV\_GroupIndex](dx-graphics-hlsl-semantics.md) system value to index into this array when writing to ensure that no two threads can collide.</span></span> <span data-ttu-id="acc60-207">En términos de lectura, todos los subprocesos tienen acceso a toda la matriz para su lectura.</span><span class="sxs-lookup"><span data-stu-id="acc60-207">In terms of reading, all threads have access to the entire array for reading.</span></span>


```
struct GSData
{
    float4 Color;
    float Factor;
}

groupshared GSData data[5*5*1];

[numthreads(5,5,1)]
void main( uint index : SV_GroupIndex )
{
    data[index].Color = (float4)0;
    data[index].Factor = 2.0f;
    GroupMemoryBarrierWithGroupSync();
    ...
}
```



### <a name="packing"></a><span data-ttu-id="acc60-208">Embalaje</span><span class="sxs-lookup"><span data-stu-id="acc60-208">Packing</span></span>

<span data-ttu-id="acc60-209">Empaquetar subcomponentes de vectores y escalares cuyo tamaño es lo suficientemente grande como para evitar el cruce de límites de registro.</span><span class="sxs-lookup"><span data-stu-id="acc60-209">Pack subcomponents of vectors and scalars whose size is large enough to prevent crossing register boundarys.</span></span> <span data-ttu-id="acc60-210">Por ejemplo, todos son válidos:</span><span class="sxs-lookup"><span data-stu-id="acc60-210">For example, these are all valid:</span></span>


```
cbuffer MyBuffer
{
    float4 Element1 : packoffset(c0);
    float1 Element2 : packoffset(c1);
    float1 Element3 : packoffset(c1.y);
}
        
```



<span data-ttu-id="acc60-211">No se pueden mezclar tipos de empaquetado.</span><span class="sxs-lookup"><span data-stu-id="acc60-211">Cannot mix packing types.</span></span>

<span data-ttu-id="acc60-212">Al igual que la palabra clave register, un packoffset puede ser específico del destino.</span><span class="sxs-lookup"><span data-stu-id="acc60-212">Like the register keyword, a packoffset can be target specific.</span></span> <span data-ttu-id="acc60-213">El empaquetado de subcomponentes solo está disponible con la palabra clave packoffset, no con la palabra clave register.</span><span class="sxs-lookup"><span data-stu-id="acc60-213">Subcomponent packing is only available with the packoffset keyword, not the register keyword.</span></span> <span data-ttu-id="acc60-214">Dentro de una declaración de cbuffer, la palabra clave register se omite para los destinos de Direct3D 10, ya que se supone que es para la compatibilidad multiplataforma.</span><span class="sxs-lookup"><span data-stu-id="acc60-214">Inside a cbuffer declaration, the register keyword is ignored for Direct3D 10 targets as it is assumed to be for cross-platform compatibility.</span></span>

<span data-ttu-id="acc60-215">Los elementos empaquetados pueden superponerse y el compilador no producirá ningún error ni advertencia.</span><span class="sxs-lookup"><span data-stu-id="acc60-215">Packed elements may overlap and the compiler will give no error or warning.</span></span> <span data-ttu-id="acc60-216">En este ejemplo, Element2 y Element3 se superponerán con Element1.x y Element1.y.</span><span class="sxs-lookup"><span data-stu-id="acc60-216">In this example, Element2 and Element3 will overlap with Element1.x and Element1.y.</span></span>


```
cbuffer MyBuffer
{
    float4 Element1 : packoffset(c0);
    float1 Element2 : packoffset(c0);
    float1 Element3 : packoffset(c0.y);
}
        
```



<span data-ttu-id="acc60-217">Un ejemplo que usa packoffset es: [EJEMPLO HLSLWithoutFX10](https://msdn.microsoft.com/library/Ee416414(v=VS.85).aspx).</span><span class="sxs-lookup"><span data-stu-id="acc60-217">A sample that uses packoffset is: [HLSLWithoutFX10 Sample](https://msdn.microsoft.com/library/Ee416414(v=VS.85).aspx).</span></span>

## <a name="related-topics"></a><span data-ttu-id="acc60-218">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="acc60-218">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="acc60-219">Variables (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="acc60-219">Variables (DirectX HLSL)</span></span>](dx-graphics-hlsl-variables.md)
</dt> </dl>

 

