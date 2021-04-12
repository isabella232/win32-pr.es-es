---
title: Asas
description: Hasta dos partes de la descripción de la cadena de formato de una dirección de procedimiento que controla.
ms.assetid: 11c6742c-b2f5-4201-8b1c-7e31ae52e0da
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d1c1ce68b74440fc9339fb9cf9170bfdd1fdfcd
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359284"
---
# <a name="handles"></a><span data-ttu-id="f57d6-103">Asas</span><span class="sxs-lookup"><span data-stu-id="f57d6-103">Handles</span></span>

<span data-ttu-id="f57d6-104">Hasta dos partes de la descripción de la cadena de formato de una dirección de procedimiento que controla.</span><span class="sxs-lookup"><span data-stu-id="f57d6-104">As many as two parts in the format string description of a procedure address handles.</span></span> <span data-ttu-id="f57d6-105">La primera parte es el \_ tipo de identificador<1> campo de la descripción de un procedimiento, que se usa para indicar identificadores implícitos.</span><span class="sxs-lookup"><span data-stu-id="f57d6-105">The first part is the handle\_type<1> field of a procedure's description, used to indicate implicit handles.</span></span> <span data-ttu-id="f57d6-106">Esta parte siempre está presente.</span><span class="sxs-lookup"><span data-stu-id="f57d6-106">This part is always present.</span></span> <span data-ttu-id="f57d6-107">La segunda parte es una descripción de parámetro de cualquier identificador explícito en el procedimiento.</span><span class="sxs-lookup"><span data-stu-id="f57d6-107">The second part is a parameter description of any explicit handle in the procedure.</span></span> <span data-ttu-id="f57d6-108">Ambos se explican en las secciones siguientes, junto con una explicación de la compatibilidad del compilador de MIDL adicional de la estructura de descriptores de código auxiliar para los problemas de identificador de enlace.</span><span class="sxs-lookup"><span data-stu-id="f57d6-108">Both are explained in the following sections, along with a discussion of the additional MIDL compiler support of the Stub Descriptor structure for binding handle issues.</span></span>

## <a name="implicit-handles"></a><span data-ttu-id="f57d6-109">Identificadores implícitos</span><span class="sxs-lookup"><span data-stu-id="f57d6-109">Implicit Handles</span></span>

<span data-ttu-id="f57d6-110">Si un procedimiento usa un identificador implícito para el enlace, el \_ tipo de identificador<1> campo de la descripción del procedimiento contiene uno de los tres valores distintos de cero válidos.</span><span class="sxs-lookup"><span data-stu-id="f57d6-110">If a procedure uses an implicit handle for binding, the handle\_type<1> field of the procedure's description contains one of three valid nonzero values.</span></span> <span data-ttu-id="f57d6-111">La compatibilidad del compilador de MIDL con los identificadores implícitos se encuentra en el \_ \_ campo información de identificador implícita de la estructura del descriptor de código auxiliar:</span><span class="sxs-lookup"><span data-stu-id="f57d6-111">MIDL compiler support for implicit handles is found in the IMPLICIT\_HANDLE\_INFO field of the Stub Descriptor structure:</span></span>

``` syntax
typedef  (__RPC_FAR * GENERIC_BINDING_ROUTINE)();

typedef struct 
  {
  GENERIC_BINDING_ROUTINE  pfnBind;
  GENERIC_BINDING_ROUTINE  pfnUnbind;
  } GENERIC_BINDING_ROUTINE_PAIR;
  
typedef struct __GENERIC_BINDING_INFO 
  {
  void __RPC_FAR*          pObj;
  unsigned char            Size;
  GENERIC_BINDING_ROUTINE  pfnBind;
  GENERIC_BINDING_ROUTINE    pfnUnbind;
  } GENERIC_BINDING_INFO,  *PGENERIC_BINDING_INFO;

union 
  {
  handle_t*                pAutoHandle;
  handle_t*                pPrimitiveHandle;
  PGENERIC_BINDING_INFO    pGenericBindingInfo;
  } IMPLICIT_HANDLE_INFO;
```

<span data-ttu-id="f57d6-112">Si el procedimiento usa un identificador automático, el miembro **pAutoHandle** contiene la dirección de la variable de identificador automático definido por stub.</span><span class="sxs-lookup"><span data-stu-id="f57d6-112">If the procedure uses an auto handle, the **pAutoHandle** member contains the address of the stub defined–auto handle variable.</span></span>

<span data-ttu-id="f57d6-113">Si el procedimiento usa un identificador primitivo implícito, el miembro **pPrimitiveHandle** contiene la dirección de la variable de identificador primitivo definida por el código auxiliar.</span><span class="sxs-lookup"><span data-stu-id="f57d6-113">If the procedure uses an implicit primitive handle, the **pPrimitiveHandle** member contains the address of the stub defined–primitive handle variable.</span></span>

<span data-ttu-id="f57d6-114">Por último, si el procedimiento usa un identificador genérico implícito, el miembro **pGenericBindingInfo** contiene la dirección del puntero a la estructura **de \_ \_ información de enlace genérica** correspondiente.</span><span class="sxs-lookup"><span data-stu-id="f57d6-114">Finally, if the procedure uses an implicit generic handle, the **pGenericBindingInfo** member holds the address of the pointer to the corresponding **GENERIC\_BINDING\_INFO** structure.</span></span> <span data-ttu-id="f57d6-115">La descripción del **\_ código auxiliar \_ de MIDL** de la estructura de datos contiene un puntero a una colección de estructuras de **\_ \_ pares de enlace genéricos** .</span><span class="sxs-lookup"><span data-stu-id="f57d6-115">The data structure **MIDL\_STUB\_DESC** contains a pointer to a collection of **GENERIC\_BINDING\_PAIR** structures.</span></span> <span data-ttu-id="f57d6-116">La entrada en la posición cero de esta colección está reservada para las rutinas de **enlace** y **desenlace** correspondientes al identificador de enlace genérico al que hace referencia **pGenericBindingInfo** en la **\_ \_ información de identificador implícita**.</span><span class="sxs-lookup"><span data-stu-id="f57d6-116">The entry in the zero position of this collection is reserved for the **bind** and **unbind** routines corresponding to the generic binding handle referenced by **pGenericBindingInfo** in **IMPLICIT\_HANDLE\_INFO**.</span></span> <span data-ttu-id="f57d6-117">El tipo de identificador de enlace implícito se indica en la cadena de formato.</span><span class="sxs-lookup"><span data-stu-id="f57d6-117">The type of implicit binding handle is indicated in the format string.</span></span>

## <a name="explicit-handles"></a><span data-ttu-id="f57d6-118">Identificadores explícitos</span><span class="sxs-lookup"><span data-stu-id="f57d6-118">Explicit Handles</span></span>

<span data-ttu-id="f57d6-119">Hay tres posibles tipos de identificador explícito: context, Generic y Primitive.</span><span class="sxs-lookup"><span data-stu-id="f57d6-119">There are three possible explicit handle types: context, generic, and primitive.</span></span> <span data-ttu-id="f57d6-120">En el caso de un identificador explícito (o un \[  \] identificador de contexto de solo salida, que se administra de la misma manera), la información del controlador de enlace aparece como uno de los parámetros del procedimiento.</span><span class="sxs-lookup"><span data-stu-id="f57d6-120">In the case of an explicit handle (or an \[**out**\] only context handle, which is handled in the same way), the binding handle information appears as one of the procedure's parameters.</span></span> <span data-ttu-id="f57d6-121">Las tres descripciones posibles son las siguientes.</span><span class="sxs-lookup"><span data-stu-id="f57d6-121">The three possible descriptions are as follows.</span></span>

<span data-ttu-id="f57d6-122">Primitivo</span><span class="sxs-lookup"><span data-stu-id="f57d6-122">Primitive</span></span>

``` syntax
FC_BIND_PRIMITIVE, flag<1>, offset<2>.
```

<span data-ttu-id="f57d6-123">La marca<1> indica si un puntero pasa el identificador.</span><span class="sxs-lookup"><span data-stu-id="f57d6-123">The flag<1> indicates whether the handle is passed by a pointer.</span></span>

<span data-ttu-id="f57d6-124">El desplazamiento<2> proporciona el desplazamiento desde el principio de la pila hasta el identificador primitivo.</span><span class="sxs-lookup"><span data-stu-id="f57d6-124">The offset<2> provides the offset from the beginning of the stack to the primitive handle.</span></span>

> [!Note]  
> <span data-ttu-id="f57d6-125">Una descripción de identificador primitivo en la cadena de formato de tipo se reduce a un único \_ pase por alto de FC.</span><span class="sxs-lookup"><span data-stu-id="f57d6-125">A primitive handle description in the type format string is reduced to a single FC\_IGNORE.</span></span>

 

<span data-ttu-id="f57d6-126">Genérico</span><span class="sxs-lookup"><span data-stu-id="f57d6-126">Generic</span></span>

``` syntax
FC_BIND_GENERIC, flag_and_size<1>, offset<2>, binding_routine_pair_index<1>, FC_PAD
```

<span data-ttu-id="f57d6-127">La marca \_ y el \_ tamaño<1> tiene la marca superior y el tamaño de la parte inferior.</span><span class="sxs-lookup"><span data-stu-id="f57d6-127">The flag\_and \_size<1> has the upper flag nibble and the lower size nibble.</span></span> <span data-ttu-id="f57d6-128">La marca indica si el identificador se pasa mediante un puntero.</span><span class="sxs-lookup"><span data-stu-id="f57d6-128">The flag indicates whether the handle is passed by a pointer.</span></span> <span data-ttu-id="f57d6-129">El campo tamaño proporciona el tamaño del tipo de identificador genérico definido por el usuario.</span><span class="sxs-lookup"><span data-stu-id="f57d6-129">The size field provides the size of the user defined–generic handle type.</span></span> <span data-ttu-id="f57d6-130">Este tamaño está limitado a 1, 2 o 4 bytes en sistemas de 32 bits y 1, 2, 4 u 8 bytes en sistemas de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="f57d6-130">This size is limited to be 1, 2 or 4 bytes on 32-bit systems and 1, 2, 4 or 8 bytes on 64-bit systems.</span></span>

<span data-ttu-id="f57d6-131">El campo desplazamiento<2> proporciona el desplazamiento desde el principio de la pila del puntero a los datos del tamaño especificado.</span><span class="sxs-lookup"><span data-stu-id="f57d6-131">The offset<2> field provides the offset from the beginning of the stack of the pointer to the data of the size given.</span></span>

<span data-ttu-id="f57d6-132">El \_ \_ \_ campo de índice de rutina de enlace<1> proporciona el índice en el campo AGenericBindingRoutinePairs del descriptor de código auxiliar para los punteros de función de rutina de **enlace** y **desenlace** para el identificador genérico.</span><span class="sxs-lookup"><span data-stu-id="f57d6-132">The binding\_routine\_pair\_index<1> field gives the index into the aGenericBindingRoutinePairs field of the Stub Descriptor to the **bind** and **unbind** routine function pointers for the generic handle.</span></span>

> [!Note]  
> <span data-ttu-id="f57d6-133">Una descripción de identificador genérico en el formato de tipo es la descripción del tipo de datos relacionado.</span><span class="sxs-lookup"><span data-stu-id="f57d6-133">A generic handle description in the type format is the description of the related data type only.</span></span>

 

<span data-ttu-id="f57d6-134">Context</span><span class="sxs-lookup"><span data-stu-id="f57d6-134">Context</span></span>

``` syntax
FC_BIND_CONTEXT flags<1> offset<2> context_rundown_routine_index<1> param_num<1>
```

<span data-ttu-id="f57d6-135">Las marcas<1> indican cómo se pasa el identificador y qué tipo es.</span><span class="sxs-lookup"><span data-stu-id="f57d6-135">The flags<1> indicate how the handle is passed and what type it is.</span></span> <span data-ttu-id="f57d6-136">En la tabla siguiente se muestran marcas válidas.</span><span class="sxs-lookup"><span data-stu-id="f57d6-136">Valid flags are shown in the following table.</span></span>



| <span data-ttu-id="f57d6-137">Hex</span><span class="sxs-lookup"><span data-stu-id="f57d6-137">Hex</span></span> | <span data-ttu-id="f57d6-138">Marca</span><span class="sxs-lookup"><span data-stu-id="f57d6-138">Flag</span></span>                                   |
|-----|----------------------------------------|
| <span data-ttu-id="f57d6-139">80</span><span class="sxs-lookup"><span data-stu-id="f57d6-139">80</span></span>  | <span data-ttu-id="f57d6-140">el \_ parámetro de identificador \_ es \_ mediante \_ ptr</span><span class="sxs-lookup"><span data-stu-id="f57d6-140">HANDLE\_PARAM\_IS\_VIA\_PTR</span></span>            |
| <span data-ttu-id="f57d6-141">40</span><span class="sxs-lookup"><span data-stu-id="f57d6-141">40</span></span>  | <span data-ttu-id="f57d6-142">el \_ parámetro \_ de identificador está \_ en</span><span class="sxs-lookup"><span data-stu-id="f57d6-142">HANDLE\_PARAM\_IS\_IN</span></span>                  |
| <span data-ttu-id="f57d6-143">20</span><span class="sxs-lookup"><span data-stu-id="f57d6-143">20</span></span>  | <span data-ttu-id="f57d6-144">el \_ parámetro de identificador \_ está \_ fuera</span><span class="sxs-lookup"><span data-stu-id="f57d6-144">HANDLE\_PARAM\_IS\_OUT</span></span>                 |
| <span data-ttu-id="f57d6-145">21</span><span class="sxs-lookup"><span data-stu-id="f57d6-145">21</span></span>  | <span data-ttu-id="f57d6-146">el \_ parámetro de identificador \_ es \_ devuelto</span><span class="sxs-lookup"><span data-stu-id="f57d6-146">HANDLE\_PARAM\_IS\_RETURN</span></span>              |
| <span data-ttu-id="f57d6-147">08</span><span class="sxs-lookup"><span data-stu-id="f57d6-147">08</span></span>  | <span data-ttu-id="f57d6-148">identificador de contexto de NDR \_ STRICT \_ \_</span><span class="sxs-lookup"><span data-stu-id="f57d6-148">NDR\_STRICT\_CONTEXT\_HANDLE</span></span>           |
| <span data-ttu-id="f57d6-149">04</span><span class="sxs-lookup"><span data-stu-id="f57d6-149">04</span></span>  | <span data-ttu-id="f57d6-150">\_identificador de contexto NDR \_ \_ sin \_ serialización</span><span class="sxs-lookup"><span data-stu-id="f57d6-150">NDR\_CONTEXT\_HANDLE\_NO\_SERIALIZE</span></span>    |
| <span data-ttu-id="f57d6-151">02</span><span class="sxs-lookup"><span data-stu-id="f57d6-151">02</span></span>  | <span data-ttu-id="f57d6-152">\_ \_ serializar identificador de contexto de NDR \_</span><span class="sxs-lookup"><span data-stu-id="f57d6-152">NDR\_CONTEXT\_HANDLE\_SERIALIZE</span></span>        |
| <span data-ttu-id="f57d6-153">01</span><span class="sxs-lookup"><span data-stu-id="f57d6-153">01</span></span>  | <span data-ttu-id="f57d6-154">el \_ identificador de contexto de NDR \_ \_ no puede \_ ser \_ nulo</span><span class="sxs-lookup"><span data-stu-id="f57d6-154">NDR\_CONTEXT\_HANDLE\_CANNOT\_BE\_NULL</span></span> |



 

<span data-ttu-id="f57d6-155">Las primeras cuatro marcas siempre están presentes, las cuatro últimas se agregaron en Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="f57d6-155">The first four flags have always been present, the last four were added in Windows 2000.</span></span>

<span data-ttu-id="f57d6-156">El campo desplazamiento<2> proporciona el desplazamiento desde el inicio de la pila hasta el identificador de contexto.</span><span class="sxs-lookup"><span data-stu-id="f57d6-156">The offset<2> field provides the offset from the start of the stack to the context handle.</span></span>

<span data-ttu-id="f57d6-157">El \_ Índice de \_ rutina de informe detallado de contexto \_<1> proporciona un índice en el campo **apfnNdrRundownRoutines** del descriptor de código auxiliar de la rutina de detención utilizada para este identificador de contexto.</span><span class="sxs-lookup"><span data-stu-id="f57d6-157">The context\_rundown\_routine\_index<1> provides an index into the **apfnNdrRundownRoutines** field of the Stub Descriptor to the rundown routine used for this context handle.</span></span> <span data-ttu-id="f57d6-158">El compilador siempre genera un índice.</span><span class="sxs-lookup"><span data-stu-id="f57d6-158">The compiler always generates an index.</span></span> <span data-ttu-id="f57d6-159">En el caso de las rutinas que no tienen una rutina de informe detallado, se trata de un índice de una posición de tabla que contiene null.</span><span class="sxs-lookup"><span data-stu-id="f57d6-159">For routines that do not have a rundown routine, this is an index to a table position that holds null.</span></span>

<span data-ttu-id="f57d6-160">En el caso de los códigos auxiliares integrados **: Oi2**, el parámetro \_ num<1> proporciona el recuento ordinal, empezando por cero y especificando el identificador de contexto que se encuentra en el procedimiento especificado.</span><span class="sxs-lookup"><span data-stu-id="f57d6-160">For stubs built in **–Oi2**, the param\_num<1> provides the ordinal count, starting at zero, specifying which context handle it is in the given procedure.</span></span>

<span data-ttu-id="f57d6-161">En el caso de las versiones anteriores del intérprete, param \_ num<1> proporciona el número de parámetro del identificador de contexto, empezando por cero, en el procedimiento.</span><span class="sxs-lookup"><span data-stu-id="f57d6-161">For previous versions of the interpreter, the param\_num<1> provides the context handle's parameter number, starting at zero, in its procedure.</span></span>

> [!Note]  
> <span data-ttu-id="f57d6-162">Una descripción de identificador de contexto en la cadena de formato de tipo no tendrá el desplazamiento<2> en la descripción.</span><span class="sxs-lookup"><span data-stu-id="f57d6-162">A context handle description in the type format string will not have the offset<2> in the description.</span></span>

 

## <a name="the-new-oif-header"></a><span data-ttu-id="f57d6-163">Nuevo encabezado – interfaces</span><span class="sxs-lookup"><span data-stu-id="f57d6-163">The New –Oif Header</span></span>

<span data-ttu-id="f57d6-164">Como se mencionó anteriormente, el encabezado [**–**](/windows/desktop/Midl/-oi) activations se expande en el encabezado **– OI** .</span><span class="sxs-lookup"><span data-stu-id="f57d6-164">As mentioned previously, the [**–Oif**](/windows/desktop/Midl/-oi) header expands on the **–Oi** header.</span></span> <span data-ttu-id="f57d6-165">Para mayor comodidad, aquí se muestran todos los campos:</span><span class="sxs-lookup"><span data-stu-id="f57d6-165">For convenience, all fields are shown here:</span></span>

<span data-ttu-id="f57d6-166">(El encabezado anterior)</span><span class="sxs-lookup"><span data-stu-id="f57d6-166">(The old header)</span></span>

``` syntax
handle_type<1> 
Oi_flags<1>
[rpc_flags<4>]
proc_num<2>  
stack_size<2>
[explicit_handle_description<>]
```

<span data-ttu-id="f57d6-167">(Extensiones de [**-interfaces**](/windows/desktop/Midl/-oi) )</span><span class="sxs-lookup"><span data-stu-id="f57d6-167">(The [**–Oif**](/windows/desktop/Midl/-oi) extensions)</span></span>

``` syntax
constant_client_buffer_size<2>
constant_server_buffer_size<2>
INTERPRETER_OPT_FLAGS<1>
number_of_params<1>
```

<span data-ttu-id="f57d6-168">El \_ \_ \_ tamaño de búfer de cliente constante<2> proporciona el tamaño del búfer de serialización que podría haber sido calculado previamente por el compilador.</span><span class="sxs-lookup"><span data-stu-id="f57d6-168">The constant\_client\_buffer\_size<2> provides the size of the marshaling buffer that could have been pre-computed by the compiler.</span></span> <span data-ttu-id="f57d6-169">Esto puede ser solo un tamaño parcial, ya que la marca ClientMustSize desencadena el tamaño.</span><span class="sxs-lookup"><span data-stu-id="f57d6-169">This may be only a partial size, as the ClientMustSize flag triggers the sizing.</span></span>

<span data-ttu-id="f57d6-170">El \_ \_ \_ tamaño de búfer de servidor constante<2> proporciona el tamaño del búfer de serialización calculado por el compilador.</span><span class="sxs-lookup"><span data-stu-id="f57d6-170">The constant\_server\_buffer\_size<2> provides the size of the marshaling buffer as precomputed by the compiler.</span></span> <span data-ttu-id="f57d6-171">Esto puede ser solo un tamaño parcial, ya que la marca ServerMustSize desencadena el tamaño.</span><span class="sxs-lookup"><span data-stu-id="f57d6-171">This may be only a partial size, as the ServerMustSize flag triggers the sizing.</span></span>

<span data-ttu-id="f57d6-172">Las \_ marcas opt del intérprete \_ se definen en Ndrtypes. h:</span><span class="sxs-lookup"><span data-stu-id="f57d6-172">The INTERPRETER\_OPT\_FLAGS are defined in Ndrtypes.h:</span></span>

``` syntax
typedef struct
  {
  unsigned char   ServerMustSize      : 1;    // 0x01
  unsigned char   ClientMustSize      : 1;    // 0x02
  unsigned char   HasReturn           : 1;    // 0x04
  unsigned char   HasPipes            : 1;    // 0x08
  unsigned char   Unused              : 1;
  unsigned char   HasAsyncUuid        : 1;    // 0x20
  unsigned char   HasExtensions       : 1;    // 0x40
  unsigned char   HasAsyncHandle      : 1;    // 0x80
  } INTERPRETER_OPT_FLAGS, *PINTERPRETER_OPT_FLAGS;
```

-   <span data-ttu-id="f57d6-173">El bit ServerMustSize se establece si el servidor necesita realizar un paso de tamaño del búfer.</span><span class="sxs-lookup"><span data-stu-id="f57d6-173">The ServerMustSize bit is set if the server needs to perform a buffer sizing pass.</span></span>
-   <span data-ttu-id="f57d6-174">El bit ClientMustSize se establece si el cliente necesita realizar un paso de tamaño del búfer.</span><span class="sxs-lookup"><span data-stu-id="f57d6-174">The ClientMustSize bit is set if the client needs to perform a buffer sizing pass.</span></span>
-   <span data-ttu-id="f57d6-175">El bit HasReturn se establece si el procedimiento tiene un valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="f57d6-175">The HasReturn bit is set if the procedure has a return value.</span></span>
-   <span data-ttu-id="f57d6-176">El bit HasPipes se establece si el paquete de canalización debe usarse para admitir un argumento de canalización.</span><span class="sxs-lookup"><span data-stu-id="f57d6-176">The HasPipes bit is set if the pipe package needs to be used to support a pipe argument.</span></span>
-   <span data-ttu-id="f57d6-177">El bit HasAsyncUuid se establece si el procedimiento es un procedimiento DCOM asincrónico.</span><span class="sxs-lookup"><span data-stu-id="f57d6-177">The HasAsyncUuid bit is set if the procedure is an asynchronous DCOM procedure.</span></span>
-   <span data-ttu-id="f57d6-178">El bit HasExtensions indica que se usan las extensiones de Windows 2000 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="f57d6-178">The HasExtensions bit indicates that Windows 2000 and later extensions are used.</span></span>
-   <span data-ttu-id="f57d6-179">El bit HasAsyncHandle indica un procedimiento RPC asincrónico.</span><span class="sxs-lookup"><span data-stu-id="f57d6-179">The HasAsyncHandle bit indicates an asynchronous RPC procedure.</span></span>

<span data-ttu-id="f57d6-180">El bit HasAsyncHandle se ha usado inicialmente para una implementación DCOM diferente de compatibilidad asincrónica y, por tanto, no se pudo usar para la compatibilidad asincrónica de estilo actual en DCOM.</span><span class="sxs-lookup"><span data-stu-id="f57d6-180">The HasAsyncHandle bit has been initially used for a different DCOM implementation of async support, and hence could not be used for the current style async support in DCOM.</span></span> <span data-ttu-id="f57d6-181">El bit HasAsyncUuid indica actualmente esto.</span><span class="sxs-lookup"><span data-stu-id="f57d6-181">The HasAsyncUuid bit currently indicates this.</span></span>

 

 