---
title: Descriptores de parámetros
description: Como se mencionó anteriormente, los descriptores de parámetros de estilo 8211, OI y \ 8211; existen.
ms.assetid: c2dad284-abe5-4b38-b3a6-3c7373fc5b84
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22f6f8b19eb6632c4111547925151865b03b9adc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103793209"
---
# <a name="parameter-descriptors"></a><span data-ttu-id="598c3-103">Descriptores de parámetros</span><span class="sxs-lookup"><span data-stu-id="598c3-103">Parameter Descriptors</span></span>

<span data-ttu-id="598c3-104">Como se mencionó anteriormente, los descriptores de parámetros de estilo [**-OI**](/windows/desktop/Midl/-oi) y **-** transformated Style existen.</span><span class="sxs-lookup"><span data-stu-id="598c3-104">As mentioned previously, [**–Oi**](/windows/desktop/Midl/-oi) and **–Oif** style parameter descriptors exist.</span></span>

## <a name="the-oi-parameter-descriptors"></a><span data-ttu-id="598c3-105">Descriptores de parámetros – OI</span><span class="sxs-lookup"><span data-stu-id="598c3-105">The –Oi Parameter Descriptors</span></span>

<span data-ttu-id="598c3-106">Los códigos auxiliares totalmente interpretados requieren información adicional para cada uno de los parámetros de una llamada RPC.</span><span class="sxs-lookup"><span data-stu-id="598c3-106">Fully interpreted stubs require additional information for each of the parameters in an RPC call.</span></span> <span data-ttu-id="598c3-107">Las descripciones de los parámetros de un procedimiento siguen inmediatamente después de la descripción del procedimiento.</span><span class="sxs-lookup"><span data-stu-id="598c3-107">The parameter descriptions of a procedure follow immediately after the description of the procedure.</span></span>

[<span data-ttu-id="598c3-108">**Simple: OI**</span><span class="sxs-lookup"><span data-stu-id="598c3-108">**Simple –Oi**</span></span>](/windows/desktop/Midl/-oi)

<span data-ttu-id="598c3-109">**Descriptores de parámetros**</span><span class="sxs-lookup"><span data-stu-id="598c3-109">**Parameter Descriptors**</span></span>

<span data-ttu-id="598c3-110">El formato de la descripción de un \[  \] parámetro de tipo simple in o Return es:</span><span class="sxs-lookup"><span data-stu-id="598c3-110">The format for the description of an \[**in**\] or return simple type parameter is:</span></span>

``` syntax
FC_IN_PARAM_BASETYPE 
simple_type<1>
```

<span data-ttu-id="598c3-111">-o bien-</span><span class="sxs-lookup"><span data-stu-id="598c3-111">–or–</span></span>

``` syntax
FC_RETURN_PARAM_BASETYPE 
simple_type<1>
```

<span data-ttu-id="598c3-112">Donde el \_ tipo simple<1> es el token de FC que indica el tipo simple.</span><span class="sxs-lookup"><span data-stu-id="598c3-112">Where simple\_type<1> is the FC token indicating the simple type.</span></span> <span data-ttu-id="598c3-113">Los códigos son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="598c3-113">The codes are as follows:</span></span>

``` syntax
4e  FC_IN_PARAM_BASETYPE 
53  FC_RETURN_PARAM_BASETYPE
```

<span data-ttu-id="598c3-114">**Otro: OI**</span><span class="sxs-lookup"><span data-stu-id="598c3-114">**Other –Oi**</span></span>

<span data-ttu-id="598c3-115">**Descriptores de parámetros**</span><span class="sxs-lookup"><span data-stu-id="598c3-115">**Parameter Descriptors**</span></span>

<span data-ttu-id="598c3-116">El formato de la descripción de todos los demás tipos de parámetro es:</span><span class="sxs-lookup"><span data-stu-id="598c3-116">The format for the description for all other parameter types is:</span></span>

``` syntax
param_direction<1> 
stack_size<1> 
type_offset<2>
```

<span data-ttu-id="598c3-117">Donde la dirección del parámetro \_<1> campo para cada una de estas descripciones debe ser uno de los que se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="598c3-117">Where the param\_direction<1> field for each of these descriptions must be one of those shown in the following table.</span></span>



| <span data-ttu-id="598c3-118">Hex</span><span class="sxs-lookup"><span data-stu-id="598c3-118">Hex</span></span> | <span data-ttu-id="598c3-119">Marca</span><span class="sxs-lookup"><span data-stu-id="598c3-119">Flag</span></span>                          | <span data-ttu-id="598c3-120">Significado</span><span class="sxs-lookup"><span data-stu-id="598c3-120">Meaning</span></span>                                                     |
|-----|-------------------------------|-------------------------------------------------------------|
| <span data-ttu-id="598c3-121">4d</span><span class="sxs-lookup"><span data-stu-id="598c3-121">4d</span></span>  | <span data-ttu-id="598c3-122">FC \_ en \_ param</span><span class="sxs-lookup"><span data-stu-id="598c3-122">FC\_IN\_PARAM</span></span>                 | <span data-ttu-id="598c3-123">Parámetro in.</span><span class="sxs-lookup"><span data-stu-id="598c3-123">An in parameter.</span></span>                                            |
| <span data-ttu-id="598c3-124">50</span><span class="sxs-lookup"><span data-stu-id="598c3-124">50</span></span>  | <span data-ttu-id="598c3-125">\_parámetro FC in \_ out \_</span><span class="sxs-lookup"><span data-stu-id="598c3-125">FC\_IN\_OUT\_PARAM</span></span>            | <span data-ttu-id="598c3-126">Parámetro in/out.</span><span class="sxs-lookup"><span data-stu-id="598c3-126">An in/out parameter.</span></span>                                        |
| <span data-ttu-id="598c3-127">51</span><span class="sxs-lookup"><span data-stu-id="598c3-127">51</span></span>  | <span data-ttu-id="598c3-128">\_parámetro de salida FC \_</span><span class="sxs-lookup"><span data-stu-id="598c3-128">FC\_OUT\_PARAM</span></span>                | <span data-ttu-id="598c3-129">Parámetro Out.</span><span class="sxs-lookup"><span data-stu-id="598c3-129">An out parameter.</span></span>                                           |
| <span data-ttu-id="598c3-130">52</span><span class="sxs-lookup"><span data-stu-id="598c3-130">52</span></span>  | <span data-ttu-id="598c3-131">\_parámetro de devolución de FC \_</span><span class="sxs-lookup"><span data-stu-id="598c3-131">FC\_RETURN\_PARAM</span></span>             | <span data-ttu-id="598c3-132">Valor devuelto de un procedimiento.</span><span class="sxs-lookup"><span data-stu-id="598c3-132">A procedure return value.</span></span>                                   |
| <span data-ttu-id="598c3-133">4F</span><span class="sxs-lookup"><span data-stu-id="598c3-133">4f</span></span>  | <span data-ttu-id="598c3-134">FC \_ en \_ parámetro \_ no \_ disponible \_ inst.</span><span class="sxs-lookup"><span data-stu-id="598c3-134">FC\_IN\_PARAM\_NO\_FREE\_INST</span></span> | <span data-ttu-id="598c3-135">En transmisión/REP como un parámetro para el que no se realiza ninguna liberación.</span><span class="sxs-lookup"><span data-stu-id="598c3-135">An in xmit/rep as a parameter for which no freeing is made.</span></span> |



 

<span data-ttu-id="598c3-136">El \_ tamaño de la pila<1> es el tamaño del parámetro en la pila, expresado como el número de enteros que el parámetro ocupa en la pila.</span><span class="sxs-lookup"><span data-stu-id="598c3-136">The stack\_size<1> is the size of the parameter on the stack, expressed as the number of integers the parameter occupies on the stack.</span></span>

> [!Note]  
> <span data-ttu-id="598c3-137">El modo [**– OI**](/windows/desktop/Midl/-oi) no se admite en las plataformas de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="598c3-137">The [**–Oi**](/windows/desktop/Midl/-oi) mode is not supported on 64-bit platforms.</span></span>

 

<span data-ttu-id="598c3-138">El \_ desplazamiento de tipo<2> campo es el desplazamiento en la tabla de cadenas de formato de tipo, que indica el descriptor de tipos para el argumento.</span><span class="sxs-lookup"><span data-stu-id="598c3-138">The type\_offset<2> field is the offset in the type format string table, indicating the type descriptor for the argument.</span></span>

## <a name="the-oif-parameter-descriptors"></a><span data-ttu-id="598c3-139">Descriptores de parámetros – interfaces</span><span class="sxs-lookup"><span data-stu-id="598c3-139">The –Oif Parameter Descriptors</span></span>

<span data-ttu-id="598c3-140">Hay dos formatos posibles para una descripción de parámetro, uno para los tipos base, otro para todos los demás tipos.</span><span class="sxs-lookup"><span data-stu-id="598c3-140">There are two possible formats for a parameter description, one for base types, another for all other types.</span></span>

<span data-ttu-id="598c3-141">Tipos base:</span><span class="sxs-lookup"><span data-stu-id="598c3-141">Base types:</span></span>

``` syntax
PARAM_ATTRIBUTES<2> 
stack_offset<2> 
type_format_char<1> 
unused<1>
```

<span data-ttu-id="598c3-142">Otros:</span><span class="sxs-lookup"><span data-stu-id="598c3-142">Other:</span></span>

``` syntax
PARAM_ATTRIBUTES<2> 
stack_offset<2> 
type_offset<2>
```

<span data-ttu-id="598c3-143">En \_ el desplazamiento de la pila<2> indica el desplazamiento en la pila de argumentos virtuales, en bytes.</span><span class="sxs-lookup"><span data-stu-id="598c3-143">In both stack\_offset<2> indicates the offset on the virtual argument stack, in bytes.</span></span> <span data-ttu-id="598c3-144">En el caso de los tipos base, el tipo de argumento lo proporciona directamente el carácter de formato correspondiente al tipo.</span><span class="sxs-lookup"><span data-stu-id="598c3-144">For base types, the argument type is given directly by the format character corresponding to the type.</span></span> <span data-ttu-id="598c3-145">Para otros tipos, el \_ campo desplazamiento de tipo<2> proporciona el desplazamiento en la tabla de cadenas de formato de tipo donde se encuentra el descriptor de tipos para el argumento.</span><span class="sxs-lookup"><span data-stu-id="598c3-145">For other types, the type\_offset<2> field gives the offset in the type format string table where the type descriptor for the argument is located.</span></span>

<span data-ttu-id="598c3-146">El campo atributo de parámetro se define de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="598c3-146">The parameter attribute field is defined as follows:</span></span>

``` syntax
typedef struct
  {
  unsigned short  MustSize            : 1;    // 0x0001
  unsigned short  MustFree            : 1;    // 0x0002
  unsigned short  IsPipe              : 1;    // 0x0004
  unsigned short  IsIn                : 1;    // 0x0008
  unsigned short  IsOut               : 1;    // 0x0010
  unsigned short  IsReturn            : 1;    // 0x0020
  unsigned short  IsBasetype          : 1;    // 0x0040
  unsigned short  IsByValue           : 1;    // 0x0080
  unsigned short  IsSimpleRef         : 1;    // 0x0100
  unsigned short  IsDontCallFreeInst  : 1;    // 0x0200
  unsigned short  SaveForAsyncFinish  : 1;    // 0x0400
  unsigned short  Unused              : 2;
  unsigned short  ServerAllocSize     : 3;    // 0xe000
  } PARAM_ATTRIBUTES, *PPARAM_ATTRIBUTES;
```

-   <span data-ttu-id="598c3-147">El bit **MustSize** solo se establece si se debe ajustar el tamaño del parámetro.</span><span class="sxs-lookup"><span data-stu-id="598c3-147">The **MustSize** bit is set only if the parameter must be sized.</span></span>
-   <span data-ttu-id="598c3-148">El bit **MustFree** se establece si el servidor debe llamar a la rutina NdrFree del parámetro \* .</span><span class="sxs-lookup"><span data-stu-id="598c3-148">The **MustFree** bit is set if the server must call the parameter's NdrFree\* routine.</span></span>
-   <span data-ttu-id="598c3-149">El bit **IsSimpleRef** se establece para un parámetro que es un puntero de referencia a cualquier otro puntero y que no tiene atributos de asignación.</span><span class="sxs-lookup"><span data-stu-id="598c3-149">The **IsSimpleRef** bit is set for a parameter that is a reference pointer to anything other than another pointer, and which has no allocate attributes.</span></span> <span data-ttu-id="598c3-150">Para este tipo, el desplazamiento de tipo de la descripción del parámetro \_<> campo, excepto un puntero de referencia a un tipo base, proporciona el desplazamiento al tipo del campo de referencia; el puntero de referencia simplemente se omite.</span><span class="sxs-lookup"><span data-stu-id="598c3-150">For such a type, the parameter description's type\_offset<> field, except for a reference pointer to a base type, provides the offset to the referent's type; the reference pointer is simply skipped.</span></span>
-   <span data-ttu-id="598c3-151">El bit **IsDontCallFreeInst** se establece para ciertos representan \_ como parámetros cuyas rutinas de instancia gratuitas no deben llamarse.</span><span class="sxs-lookup"><span data-stu-id="598c3-151">The **IsDontCallFreeInst** bit is set for certain represent\_as parameters whose free instance routines should not be called.</span></span>
-   <span data-ttu-id="598c3-152">Los bits **ServerAllocSize** son distintos de cero si el parámetro está \[ **fuera** \] , \[ **en** \] , o \[ **en,** un puntero \] a puntero o puntero a enum16, y se inicializará en la pila del intérprete del servidor, en lugar de usar una llamada a **I \_ RpcAllocate**.</span><span class="sxs-lookup"><span data-stu-id="598c3-152">The **ServerAllocSize** bits are nonzero if the parameter is \[**out**\], \[**in**\], or \[**in,out**\] pointer to pointer, or pointer to enum16, and will be initialized on the server interpreter's stack, rather than using a call to **I\_RpcAllocate**.</span></span> <span data-ttu-id="598c3-153">Si es distinto de cero, este valor se multiplica por 8 para obtener el número de bytes para el parámetro.</span><span class="sxs-lookup"><span data-stu-id="598c3-153">If nonzero, this value is multiplied by 8 to get the number of bytes for the parameter.</span></span> <span data-ttu-id="598c3-154">Tenga en cuenta que esto significa que siempre se asignan al menos 8 bytes para un puntero.</span><span class="sxs-lookup"><span data-stu-id="598c3-154">Note that doing so means at least 8 bytes are always allocated for a pointer.</span></span>
-   <span data-ttu-id="598c3-155">El bit **IsBasetype** se establece para los tipos simples que se van a serializar mediante el bucle del intérprete principal [**– saliente**](/windows/desktop/Midl/-oi) .</span><span class="sxs-lookup"><span data-stu-id="598c3-155">The **IsBasetype** bit is set for simple types that are being marshaled by the main [**–Oif**](/windows/desktop/Midl/-oi) interpreter loop.</span></span> <span data-ttu-id="598c3-156">En concreto, un tipo simple con un atributo de intervalo en él no se marca como un tipo base para forzar el cálculo de referencias de rutina de intervalo mediante el envío mediante un \_ token de intervalo FC.</span><span class="sxs-lookup"><span data-stu-id="598c3-156">In particular, a simple type with a range attribute on it is not flagged as a base type in order to force the range routine marshaling through dispatching using an FC\_RANGE token.</span></span>
-   <span data-ttu-id="598c3-157">El bit **IsByValue** se establece para los tipos compuestos que se envían por valor, pero no se establece para los tipos simples, independientemente de si el argumento es un puntero.</span><span class="sxs-lookup"><span data-stu-id="598c3-157">The **IsByValue** bit is set for compound types being sent by value, but is not set for simple types, regardless of whether the argument is a pointer.</span></span> <span data-ttu-id="598c3-158">Los tipos compuestos para los que se establece son estructuras, uniones, [**transmitir \_ como**](/windows/desktop/Midl/transmit-as), [**representar \_ como**](/windows/desktop/Midl/represent-as), [**\_ serialización de cable**](/windows/desktop/Midl/wire-marshal) y SafeArray.</span><span class="sxs-lookup"><span data-stu-id="598c3-158">The compound types for which it is set are structures, unions, [**transmit\_as**](/windows/desktop/Midl/transmit-as), [**represent\_as**](/windows/desktop/Midl/represent-as), [**wire\_marshal**](/windows/desktop/Midl/wire-marshal) and SAFEARRAY.</span></span> <span data-ttu-id="598c3-159">En general, el bit se incorporó a la ventaja del bucle del intérprete principal en el intérprete [**– Oicf**](/windows/desktop/Midl/-oi) , para asegurarse de que los argumentos no simples (conocidos como argumentos de tipo compuesto) se desreferencian correctamente.</span><span class="sxs-lookup"><span data-stu-id="598c3-159">In general, the bit was introduced for the benefit of the main interpreter loop in the [**–Oicf**](/windows/desktop/Midl/-oi) interpreter, to ensure the nonsimple arguments (referred to as compound type arguments) are properly dereferenced.</span></span> <span data-ttu-id="598c3-160">Este bit nunca se usaba en versiones anteriores del intérprete.</span><span class="sxs-lookup"><span data-stu-id="598c3-160">This bit was never used in previous versions of the interpreter.</span></span>

 

 