---
title: Descriptores de correlación
description: Un descriptor de correlación es una cadena de formato que describe una expresión basada en un argumento relacionado con otro argumento.
ms.assetid: 9f5f5077-d6a9-4253-bddf-b8cd0c868973
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35f13f0793b99b80b7abb0b493c249b30ad53d76
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103904791"
---
# <a name="correlation-descriptors"></a><span data-ttu-id="b5b1b-103">Descriptores de correlación</span><span class="sxs-lookup"><span data-stu-id="b5b1b-103">Correlation Descriptors</span></span>

<span data-ttu-id="b5b1b-104">Un descriptor de correlación es una cadena de formato que describe una expresión basada en un argumento relacionado con otro argumento.</span><span class="sxs-lookup"><span data-stu-id="b5b1b-104">A correlation descriptor is a format string that describes an expression based on one argument related to another argument.</span></span> <span data-ttu-id="b5b1b-105">Un descriptor de correlación es necesario para administrar la semántica relacionada con atributos como \[ **el tamaño \_ es ()** \] , la \[ **longitud \_ es ()** \] , el \[ **modificador \_ es ()** \] y \[ **IID \_ es ()** \] .</span><span class="sxs-lookup"><span data-stu-id="b5b1b-105">A correlation descriptor is needed for handling semantics related to attributes like \[**size\_is()**\], \[**length\_is()**\], \[**switch\_is()**\] and \[**iid\_is()**\].</span></span> <span data-ttu-id="b5b1b-106">Los descriptores de correlación se utilizan con matrices, punteros de tamaño, uniones y punteros de interfaz.</span><span class="sxs-lookup"><span data-stu-id="b5b1b-106">Correlation descriptors are used with arrays, sized pointers, unions, and interface pointers.</span></span> <span data-ttu-id="b5b1b-107">El valor de la expresión final puede ser un tamaño, una longitud, un discriminante de unión o un puntero a un IID, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="b5b1b-107">The eventual expression value can be a size, a length, a union discriminant, or a pointer to an IID, respectively.</span></span> <span data-ttu-id="b5b1b-108">En cuanto a las cadenas de formato, los descriptores de correlación se utilizan con matrices, uniones y punteros de interfaz.</span><span class="sxs-lookup"><span data-stu-id="b5b1b-108">In terms of format strings, correlation descriptors are used with arrays, unions, and interface pointers.</span></span> <span data-ttu-id="b5b1b-109">Un puntero de tamaño se describe en cadenas de formato como un puntero a una matriz.</span><span class="sxs-lookup"><span data-stu-id="b5b1b-109">A sized pointer is described in format strings as a pointer to an array.</span></span>

<span data-ttu-id="b5b1b-110">Hay dos rutinas que realizan cálculos de expresiones básicas: NdrpComputeConformance se usa para tamaños, modificadores y IID, \* mientras que NdrpComputeVariance se usa para longitudes.</span><span class="sxs-lookup"><span data-stu-id="b5b1b-110">There are two routines performing basic expression calculations: NdrpComputeConformance is used for sizes, switches and IID\* while NdrpComputeVariance is used for lengths.</span></span> <span data-ttu-id="b5b1b-111">También hay una rutina única para realizar una validación del valor de correlación para la funcionalidad de denegación de ataque.</span><span class="sxs-lookup"><span data-stu-id="b5b1b-111">There is also a single routine to perform a correlation value validation for denial-of-attack functionality.</span></span>

<span data-ttu-id="b5b1b-112">Los descriptores de correlación se han diseñado para admitir solo expresiones muy limitadas.</span><span class="sxs-lookup"><span data-stu-id="b5b1b-112">Correlation descriptors have been designed to support only very limited expressions.</span></span> <span data-ttu-id="b5b1b-113">En situaciones complicadas, el compilador genera una rutina de evaluación de expresión a la que llamará el motor cuando sea necesario.</span><span class="sxs-lookup"><span data-stu-id="b5b1b-113">For complicated situations, the compiler generates an expression evaluation routine to be called by the engine when needed.</span></span>

<span data-ttu-id="b5b1b-114">Un descriptor de correlación tiene el siguiente formato:</span><span class="sxs-lookup"><span data-stu-id="b5b1b-114">A correlation descriptor has the following format:</span></span>

``` syntax
correlation_type<1>
correlation_operator<1>
offset<2>
[robust_flags<2>]
```

<span data-ttu-id="b5b1b-115">El tipo de correlación del descriptor \_ de correlación<1> consta de dos recortes: los 4 bits superiores describen dónde se puede encontrar la expresión y los 4 bits inferiores describen el tipo del valor de la expresión.</span><span class="sxs-lookup"><span data-stu-id="b5b1b-115">The correlation descriptor correlation\_type<1> consists of two nibbles: the upper 4 bits describe where the expression can be found and the lower 4 bits describe the type of the expression value.</span></span>

<span data-ttu-id="b5b1b-116">El recorte superior puede tener uno de estos cinco valores:</span><span class="sxs-lookup"><span data-stu-id="b5b1b-116">The upper nibble can have one of these five values:</span></span>

``` syntax
00  FC_NORMAL_CONFORMANCE
10  FC_POINTER_CONFORMANCE
20  FC_TOP_LEVEL_CONFORMANCE
80  FC_TOP_LEVEL_MULTID_CONFORMANCE
40  FC_CONSTANT_CONFORMANCE
```

<dl> <dt>

<span data-ttu-id="b5b1b-117"><span id="FC_NORMAL_CONFORMANCE"></span><span id="fc_normal_conformance"></span>COMPATIBILIDAD con FC \_ normal \_</span><span class="sxs-lookup"><span data-stu-id="b5b1b-117"><span id="FC_NORMAL_CONFORMANCE"></span><span id="fc_normal_conformance"></span>FC\_NORMAL\_CONFORMANCE</span></span>
</dt> <dd>

<span data-ttu-id="b5b1b-118">Un caso normal de conformidad, como el que se describe en un campo de una estructura.</span><span class="sxs-lookup"><span data-stu-id="b5b1b-118">A normal case of conformance, such as that described in a field of a structure.</span></span>

</dd> <dt>

<span data-ttu-id="b5b1b-119"><span id="FC_POINTER_CONFORMANCE"></span><span id="fc_pointer_conformance"></span>CONFORMIDAD con el \_ puntero FC \_</span><span class="sxs-lookup"><span data-stu-id="b5b1b-119"><span id="FC_POINTER_CONFORMANCE"></span><span id="fc_pointer_conformance"></span>FC\_POINTER\_CONFORMANCE</span></span>
</dt> <dd>

<span data-ttu-id="b5b1b-120">En el caso de los punteros con atributos (**el tamaño \_ es ()**, la **longitud \_ es ()**), que son campos en una estructura.</span><span class="sxs-lookup"><span data-stu-id="b5b1b-120">For attributed pointers (**size\_is()**, **length\_is()**) which are fields in a structure.</span></span> <span data-ttu-id="b5b1b-121">Esto afecta a la manera en que se establece el puntero de memoria base.</span><span class="sxs-lookup"><span data-stu-id="b5b1b-121">This affects the way the base memory pointer is set.</span></span>

</dd> <dt>

<span data-ttu-id="b5b1b-122"><span id="FC_TOP_LEVEL_CONFORMANCE"></span><span id="fc_top_level_conformance"></span>\_conformidad de \_ nivel \_ superior de FC</span><span class="sxs-lookup"><span data-stu-id="b5b1b-122"><span id="FC_TOP_LEVEL_CONFORMANCE"></span><span id="fc_top_level_conformance"></span>FC\_TOP\_LEVEL\_CONFORMANCE</span></span>
</dt> <dd>

<span data-ttu-id="b5b1b-123">Para el cumplimiento de nivel superior descrito por otro parámetro.</span><span class="sxs-lookup"><span data-stu-id="b5b1b-123">For top-level conformance described by another parameter.</span></span>

</dd> <dt>

<span data-ttu-id="b5b1b-124"><span id="FC_TOP_LEVEL_MULTID_CONFORMANCE"></span><span id="fc_top_level_multid_conformance"></span>\_conformidad con \_ \_ múltiples niveles \_ de FC superior</span><span class="sxs-lookup"><span data-stu-id="b5b1b-124"><span id="FC_TOP_LEVEL_MULTID_CONFORMANCE"></span><span id="fc_top_level_multid_conformance"></span>FC\_TOP\_LEVEL\_MULTID\_CONFORMANCE</span></span>
</dt> <dd>

<span data-ttu-id="b5b1b-125">Para la conformidad de nivel superior de una matriz multidimensional descrita por otro parámetro.</span><span class="sxs-lookup"><span data-stu-id="b5b1b-125">For top-level conformance of a multidimensional array described by another parameter.</span></span>

> [!Note]  
> <span data-ttu-id="b5b1b-126">Las matrices y punteros de tamaño multidimensional desencadenan un cambio a [**– Oicf**](/windows/desktop/Midl/-oi).</span><span class="sxs-lookup"><span data-stu-id="b5b1b-126">Multidimensional sized arrays and pointers trigger a switch to [**–Oicf**](/windows/desktop/Midl/-oi).</span></span>

 

</dd> <dt>

<span data-ttu-id="b5b1b-127"><span id="FC_CONSTANT_CONFORMANCE"></span><span id="fc_constant_conformance"></span>CONFORMIDAD de FC \_ Constant \_</span><span class="sxs-lookup"><span data-stu-id="b5b1b-127"><span id="FC_CONSTANT_CONFORMANCE"></span><span id="fc_constant_conformance"></span>FC\_CONSTANT\_CONFORMANCE</span></span>
</dt> <dd>

<span data-ttu-id="b5b1b-128">Para un valor constante.</span><span class="sxs-lookup"><span data-stu-id="b5b1b-128">For a constant value.</span></span> <span data-ttu-id="b5b1b-129">El compilador calcula el valor de una expresión constante proporcionada por el usuario.</span><span class="sxs-lookup"><span data-stu-id="b5b1b-129">The compiler precalculates the value from a constant expression supplied by the user.</span></span> <span data-ttu-id="b5b1b-130">En este caso, los 3 bytes siguientes en la descripción del cumplimiento contienen los 3 bytes inferiores de un largo que describe el tamaño del cumplimiento.</span><span class="sxs-lookup"><span data-stu-id="b5b1b-130">When this is the case, the subsequent 3 bytes in the conformance description contain the lower 3 bytes of a long describing the conformance size.</span></span> <span data-ttu-id="b5b1b-131">No es necesario realizar ningún cálculo adicional.</span><span class="sxs-lookup"><span data-stu-id="b5b1b-131">No further computation is required.</span></span>

</dd> </dl>

<span data-ttu-id="b5b1b-132">El recorte inferior proporciona el tipo de valor que debe extraerse de la memoria:</span><span class="sxs-lookup"><span data-stu-id="b5b1b-132">The lower nibble gives the type of the value that needs to be extracted from memory:</span></span>

``` syntax
FC_LONG | FC_ULONG | 
FC_SHORT | FC_USHORT | 
FC_SMALL | FC_USMALL | 
FC_HYPER
```

> [!Note]
> <span data-ttu-id="b5b1b-133">no se admiten las expresiones de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="b5b1b-133">64-bit expressions are not supported.</span></span> <span data-ttu-id="b5b1b-134">FC \_ Hyper solo se usa para **IID \_ es ()** en plataformas de 64 bits para extraer el valor de puntero para IID \* .</span><span class="sxs-lookup"><span data-stu-id="b5b1b-134">FC\_HYPER is used only for **iid\_is()** on 64-bit platforms to extract the pointer value for IID\*.</span></span>
>
> <span data-ttu-id="b5b1b-135">El compilador establece el tipo Nibble en cero para los siguientes casos: expresión constante mencionada anteriormente y cuando es necesario llamar a la rutina de expresión de evaluación, por ejemplo, cuando \_ se utiliza el cumplimiento de la constante FC \_ y la devolución de llamada de FC \_ .</span><span class="sxs-lookup"><span data-stu-id="b5b1b-135">The compiler sets the type nibble to zero for the following cases: constant expression mentioned above and when evaluation expression routine needs to be called, for example, when FC\_CONSTANT\_CONFORMANCE and FC\_CALLBACK are used.</span></span>

 

<span data-ttu-id="b5b1b-136">El tamaño \_ es \_ OP<1> campo permite aplicar una de las siguientes operaciones a la variable de conformidad:</span><span class="sxs-lookup"><span data-stu-id="b5b1b-136">The size\_is\_op<1> field allows for one of the following operations to be applied to the conformance variable:</span></span>

``` syntax
FC_DEREFERENCE | 
FC_DIV_2 | FC_MULT_2 | FC_SUB_1 | FC_ADD_1 | 
FC_CALLBACK
```

<span data-ttu-id="b5b1b-137">La \_ constante de DESreferencia de FC se usa para que la correlación sea un puntero, como para **\[ el tamaño \_ es ( \* PL) \]**.</span><span class="sxs-lookup"><span data-stu-id="b5b1b-137">The FC\_DEREFERENCE constant is used for correlation being a pointee, like for **\[size\_is(\*pL)\]**.</span></span> <span data-ttu-id="b5b1b-138">Los operadores aritméticos solo usan la constante indicada.</span><span class="sxs-lookup"><span data-stu-id="b5b1b-138">Arithmetic operators just use the indicated constant.</span></span> <span data-ttu-id="b5b1b-139">La constante de devolución de llamada de FC \_ indica que es necesario llamar a una rutina de evaluación de expresión.</span><span class="sxs-lookup"><span data-stu-id="b5b1b-139">The FC\_CALLBACK constant indicates that an expression evaluation routine needs to be called.</span></span>

<span data-ttu-id="b5b1b-140">El campo offset<2> es normalmente un desplazamiento de memoria relativa a la variable de argumento Expression.</span><span class="sxs-lookup"><span data-stu-id="b5b1b-140">The offset<2> field is typically a relative memory offset to the expression argument variable.</span></span> <span data-ttu-id="b5b1b-141">También puede ser una evaluación de expresión: índice de rutina.</span><span class="sxs-lookup"><span data-stu-id="b5b1b-141">It can also be an expression evaluation–routine index.</span></span> <span data-ttu-id="b5b1b-142">Como se mencionó anteriormente en este documento, para las expresiones constantes forma parte del valor de la expresión final real.</span><span class="sxs-lookup"><span data-stu-id="b5b1b-142">As mentioned previously in this document, for constant expressions it is a part of actual, final expression value.</span></span>

<span data-ttu-id="b5b1b-143">La interpretación del campo offset<2> como desplazamiento de memoria depende de la complejidad de la expresión, la ubicación de la variable Expression y, en el caso de una matriz, si la matriz es realmente un puntero con atributo.</span><span class="sxs-lookup"><span data-stu-id="b5b1b-143">The interpretation of the offset<2> field as memory offset depends on the complexity of the expression, the location of the expression variable, and in the case of an array, whether the array is actually an attributed pointer.</span></span>

<span data-ttu-id="b5b1b-144">Si la matriz es un puntero con atributos y la variable de conformidad es un campo de una estructura, el campo de desplazamiento contiene el desplazamiento desde el principio de la estructura hasta el campo conformidad-Descripción.</span><span class="sxs-lookup"><span data-stu-id="b5b1b-144">If the array is an attributed pointer and the conformance variable is a field in a structure, the offset field contains the offset from the beginning of the structure to the conformance-describing field.</span></span> <span data-ttu-id="b5b1b-145">Si la matriz no es un puntero con atributos y la variable de conformidad es un campo de una estructura, el campo de desplazamiento contiene el desplazamiento desde el final de la parte no conforme de la estructura hasta el campo conformidad-Descripción.</span><span class="sxs-lookup"><span data-stu-id="b5b1b-145">If the array is not an attributed pointer and the conformance variable is a field in a structure, the offset field contains the offset from the end of the nonconformant part of the structure to the conformance-describing field.</span></span> <span data-ttu-id="b5b1b-146">Normalmente, la matriz compatible está al final de la estructura.</span><span class="sxs-lookup"><span data-stu-id="b5b1b-146">Typically, the conformant array is at the end of the structure.</span></span>

<span data-ttu-id="b5b1b-147">En el caso del cumplimiento de nivel superior, el campo de desplazamiento contiene el desplazamiento desde la ubicación del primer parámetro del código auxiliar en la pila hasta el parámetro que describe la conformidad.</span><span class="sxs-lookup"><span data-stu-id="b5b1b-147">For top-level conformance, the offset field contains the offset from the stub's first parameter's location on the stack to the parameter that describes the conformance.</span></span> <span data-ttu-id="b5b1b-148">No se utiliza en modo **– os** .</span><span class="sxs-lookup"><span data-stu-id="b5b1b-148">This is not used in **–Os** mode.</span></span> <span data-ttu-id="b5b1b-149">Hay otras excepciones a la interpretación del campo de desplazamiento. dichas excepciones se describen en la descripción de esos tipos.</span><span class="sxs-lookup"><span data-stu-id="b5b1b-149">There are other exceptions to the interpretation of the offset field; such exceptions are described in the description of those types.</span></span>

<span data-ttu-id="b5b1b-150">Cuando se usa offset<2> con \_ la devolución de llamada FC, contiene un índice en la tabla de rutina de evaluación de expresiones generada por el compilador.</span><span class="sxs-lookup"><span data-stu-id="b5b1b-150">When offset<2> is used with FC\_CALLBACK, it contains an index in the expression evaluation routine table generated by the compiler.</span></span> <span data-ttu-id="b5b1b-151">El mensaje de código auxiliar se pasa a la rutina de evaluación, que luego calcula el valor de conformidad y lo asigna al campo MaxCount del mensaje de código auxiliar.</span><span class="sxs-lookup"><span data-stu-id="b5b1b-151">The stub message is passed to the evaluation routine, which then computes the conformance value and assigns it to the MaxCount field of the stub message.</span></span>

<span data-ttu-id="b5b1b-152">Se \_ han agregado las marcas sólidas<2> campo para Windows 2000 para admitir [**/Robust**](/windows/desktop/Midl/-robust), como la característica de denegación de ataques.</span><span class="sxs-lookup"><span data-stu-id="b5b1b-152">The robust\_flags<2> field has been added for Windows 2000 to support [**/robust**](/windows/desktop/Midl/-robust), such as the denial-of-attacks feature.</span></span> <span data-ttu-id="b5b1b-153">Las marcas siguientes se definen en el primer byte:</span><span class="sxs-lookup"><span data-stu-id="b5b1b-153">The following flags are defined on the first byte:</span></span>

``` syntax
typedef  struct  _NDR_CORRELATION_FLAGS
  {
  unsigned char   Early     : 1;
  unsigned char   Split     : 1;
  unsigned char   IsIidIs   : 1;
  unsigned char   DontCheck : 1;
  unsigned char   Unused    : 4;
  } NDR_CORRELATION_FLAGS;
```

<span data-ttu-id="b5b1b-154">La marca temprana indica la correlación temprana y tardía.</span><span class="sxs-lookup"><span data-stu-id="b5b1b-154">The Early flag indicates early versus late correlation.</span></span> <span data-ttu-id="b5b1b-155">Una correlación temprana es cuando el argumento de expresión precede al argumento descrito; por ejemplo, un argumento de tamaño está delante de un argumento de puntero de tamaño.</span><span class="sxs-lookup"><span data-stu-id="b5b1b-155">An early correlation is when the expression argument precedes the described argument, for example a size argument is before a sized pointer argument.</span></span> <span data-ttu-id="b5b1b-156">Una correlación tardía es cuando el argumento de expresión aparece después del argumento relacionado.</span><span class="sxs-lookup"><span data-stu-id="b5b1b-156">A late correlation is when the expression argument comes after the related argument.</span></span> <span data-ttu-id="b5b1b-157">El motor realiza la validación de los valores de la correlación temprana de inmediato, mientras que los valores de la correlación tardía se almacenan para la comprobación después de que se haya anulado la serialización.</span><span class="sxs-lookup"><span data-stu-id="b5b1b-157">The engine performs validation of early correlation values right away, the late correlation values are stored for checking after unmarshaling is done.</span></span>

<span data-ttu-id="b5b1b-158">La marca de división indica una división asincrónica entre los \[ \] argumentos in y \[ out \] .</span><span class="sxs-lookup"><span data-stu-id="b5b1b-158">The Split flag indicates an async split among \[in\] and \[out\] arguments.</span></span> <span data-ttu-id="b5b1b-159">Por ejemplo, un argumento de tamaño puede estar \[ en, \] mientras que el puntero de tamaño puede estar \[ fuera \] .</span><span class="sxs-lookup"><span data-stu-id="b5b1b-159">For example, a size argument may be \[in\] while the sized pointer may be \[out\].</span></span> <span data-ttu-id="b5b1b-160">En el contexto asincrónico DCOM, estos argumentos se producen en pilas diferentes, por lo que el motor debe ser consciente de ello.</span><span class="sxs-lookup"><span data-stu-id="b5b1b-160">In the DCOM async context, these arguments happen to be on different stacks, so the engine must be aware of this.</span></span>

<span data-ttu-id="b5b1b-161">La marca IsIidIs indica que una correlación **\_ es ()** .</span><span class="sxs-lookup"><span data-stu-id="b5b1b-161">The IsIidIs flag indicates an **iid\_is()** correlation.</span></span> <span data-ttu-id="b5b1b-162">La rutina NdrComputeConformance se engaña para obtener un puntero a IID como un valor de expresión, pero la rutina de validación no puede comparar estos valores (son punteros) y, por tanto, la marca indica que se deben comparar los IID reales.</span><span class="sxs-lookup"><span data-stu-id="b5b1b-162">The NdrComputeConformance routine is tricked to obtain a pointer to IID as an expression value, but the validation routine cannot compare such values (they would be pointers) and so the flag indicates that actual IIDs need to be compared.</span></span>

### <a name="variance-description-and-other-array-attributes"></a><span data-ttu-id="b5b1b-163">Descripción de la varianza y otros atributos de la matriz</span><span class="sxs-lookup"><span data-stu-id="b5b1b-163">Variance Description and Other Array Attributes</span></span>

<span data-ttu-id="b5b1b-164">El formato del campo de descripción de la varianza es idéntico al campo Descripción del cumplimiento.</span><span class="sxs-lookup"><span data-stu-id="b5b1b-164">The variance description field format is identical to the conformance description field.</span></span> <span data-ttu-id="b5b1b-165">La diferencia es que el motor NDR usa un campo de mensaje de código auxiliar diferente como una variable temporal.</span><span class="sxs-lookup"><span data-stu-id="b5b1b-165">The difference is that a different stub message field is used by the NDR engine as a temporary variable.</span></span> <span data-ttu-id="b5b1b-166">En el caso de la descripción de la varianza, es la longitud que se evalúa y el campo correspondiente se denomina ActualLength.</span><span class="sxs-lookup"><span data-stu-id="b5b1b-166">In the case of variance description, it is the length that is evaluated and the corresponding field is called ActualLength.</span></span>

<span data-ttu-id="b5b1b-167">Con varianza, el desplazamiento inicial suele ser cero y el motor se optimiza en consecuencia.</span><span class="sxs-lookup"><span data-stu-id="b5b1b-167">With variance, the starting offset is typically zero and the engine is tuned accordingly.</span></span> <span data-ttu-id="b5b1b-168">Si el **primer atributo \_ es ()** se aplica a una matriz variable conforme, se fuerza una devolución de llamada a una rutina de evaluación de expresión.</span><span class="sxs-lookup"><span data-stu-id="b5b1b-168">If the **first\_is()** attribute is applied to a conformant varying array, a callback to an expression evaluation routine is forced.</span></span>

 

 