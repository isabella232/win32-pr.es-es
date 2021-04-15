---
title: transmit_as (atributo)
description: El atributo \ Transmit \_ as indica al compilador que asocie el tipo de identificador, que es un tipo presentado que las aplicaciones cliente y de servidor manipulan, con un tipo de transmisión de tipos transmitidos.
ms.assetid: 3dd1a242-03ec-49b4-ac96-87ef186e41d2
keywords:
- transmit_as el atributo MIDL
topic_type:
- apiref
api_name:
- transmit_as
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ec0cba27e994f7d77d441aef7bb783cad71cbad
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "105665782"
---
# <a name="transmit_as-attribute"></a><span data-ttu-id="e252a-104">transmitir \_ como atributo</span><span class="sxs-lookup"><span data-stu-id="e252a-104">transmit\_as attribute</span></span>

<span data-ttu-id="e252a-105">El atributo **\[ Transmit \_ as \]** indica al compilador que asocie \*\*type-id \*\* \* \*, que es un tipo presentado que las aplicaciones cliente y de servidor manipulan, con un tipo **de transmisión de** tipos transmitido.</span><span class="sxs-lookup"><span data-stu-id="e252a-105">The **\[transmit\_as\]** attribute instructs the compiler to associate \**type-id\*\*\*,* which is a presented type that client and server applications manipulate, with a transmitted type **xmit-type.**</span></span>

``` syntax
typedef [transmit_as(xmit-type) [[ , type-attribute-list ]] ] type-specifier declarator-list; 

void __RPC_USER type-id_to_xmit (
  type-id __RPC_FAR *,
  xmit-type __RPC_FAR * __RPC_FAR *);
void __RPC_USER type-id_from_xmit (
  xmit-type __RPC_FAR *,
  type-id __RPC_FAR *);
void __RPC_USER type-id_free_inst (
  type-id __RPC_FAR *);
void __RPC_USER type-id_free_xmit (
  xmit-type__RPC_FAR *);
```

## <a name="parameters"></a><span data-ttu-id="e252a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e252a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e252a-107">*tipo de transmisión*</span><span class="sxs-lookup"><span data-stu-id="e252a-107">*xmit-type*</span></span> 
</dt> <dd>

<span data-ttu-id="e252a-108">Especifica el tipo de datos que se transmite entre el cliente y el servidor.</span><span class="sxs-lookup"><span data-stu-id="e252a-108">Specifies the data type that is transmitted between client and server.</span></span>

</dd> <dt>

<span data-ttu-id="e252a-109">*lista de atributos de tipo*</span><span class="sxs-lookup"><span data-stu-id="e252a-109">*type-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="e252a-110">Especifica uno o más atributos que se aplican al tipo.</span><span class="sxs-lookup"><span data-stu-id="e252a-110">Specifies one or more attributes that apply to the type.</span></span> <span data-ttu-id="e252a-111">Entre los atributos de tipo válidos se incluyen **\[** el [**identificador**](handle.md) **\]** , **\[** el [**\_ tipo de conmutador**](switch-type.md) **\]** ; el atributo de puntero **\[** [**ref**](ref.md) **\]** , **\[** [**Unique**](unique.md) **\]** o **\[** [**ptr**](ptr.md) **\]** y la cadena de atributos de uso **\[** [](string.md) **\]** y **\[** [**omitir**](ignore.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="e252a-111">Valid type attributes include **\[**[**handle**](handle.md)**\]**, **\[**[**switch\_type**](switch-type.md)**\]**; the pointer attribute **\[**[**ref**](ref.md)**\]**, **\[**[**unique**](unique.md)**\]**, or **\[**[**ptr**](ptr.md)**\]**; and the usage attributes **\[**[**string**](string.md)**\]** and **\[**[**ignore**](ignore.md)**\]**.</span></span> <span data-ttu-id="e252a-112">Separe varios atributos con comas.</span><span class="sxs-lookup"><span data-stu-id="e252a-112">Separate multiple attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="e252a-113">*Type-Specifier*</span><span class="sxs-lookup"><span data-stu-id="e252a-113">*type-specifier*</span></span> 
</dt> <dd>

<span data-ttu-id="e252a-114">Especifica un [tipo base](midl-base-types.md), un [**struct**](struct.md), una [**Unión**](union.md), un tipo de [**enumeración**](enum.md) o un identificador de tipo.</span><span class="sxs-lookup"><span data-stu-id="e252a-114">Specifies a [base type](midl-base-types.md), [**struct**](struct.md), [**union**](union.md), [**enum**](enum.md) type, or type identifier.</span></span> <span data-ttu-id="e252a-115">Una especificación de almacenamiento opcional puede preceder *a Type-Specifier*.</span><span class="sxs-lookup"><span data-stu-id="e252a-115">An optional storage specification can precede *type-specifier*.</span></span>

</dd> <dt>

<span data-ttu-id="e252a-116">*lista de declaradores*</span><span class="sxs-lookup"><span data-stu-id="e252a-116">*declarator-list*</span></span> 
</dt> <dd>

<span data-ttu-id="e252a-117">Especifica los declaradores estándar de C, como identificadores, declaradores de puntero y declaradores de matriz.</span><span class="sxs-lookup"><span data-stu-id="e252a-117">Specifies standard C declarators, such as identifiers, pointer declarators, and array declarators.</span></span> <span data-ttu-id="e252a-118">Para obtener más información, vea [matrices y Sized-Pointer atributos](array-and-sized-pointer-attributes.md), [**matrices**](arrays-1.md)y [matrices y punteros](/windows/desktop/Rpc/arrays-and-pointers).</span><span class="sxs-lookup"><span data-stu-id="e252a-118">For more information, see [Array and Sized-Pointer Attributes](array-and-sized-pointer-attributes.md), [**arrays**](arrays-1.md), and [Arrays and Pointers](/windows/desktop/Rpc/arrays-and-pointers).</span></span> <span data-ttu-id="e252a-119">La *lista de declaradores* consta de uno o varios declaradores separados por comas.</span><span class="sxs-lookup"><span data-stu-id="e252a-119">The *declarator-list* consists of one or more declarators separated by commas.</span></span> <span data-ttu-id="e252a-120">El declarador de parámetro del declarador de la función, como el nombre del parámetro, es opcional.</span><span class="sxs-lookup"><span data-stu-id="e252a-120">The parameter declarator in the function declarator, such as the parameter name, is optional.</span></span>

</dd> <dt>

<span data-ttu-id="e252a-121">*identificador de tipo*</span><span class="sxs-lookup"><span data-stu-id="e252a-121">*type-id*</span></span> 
</dt> <dd>

<span data-ttu-id="e252a-122">Especifica el nombre del tipo de datos que se presenta a las aplicaciones de cliente y de servidor.</span><span class="sxs-lookup"><span data-stu-id="e252a-122">Specifies the name of the data type that is presented to the client and server applications.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e252a-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e252a-123">Remarks</span></span>

<span data-ttu-id="e252a-124">Para usar el atributo **\[ Transmit \_ as \]** , el usuario debe proporcionar rutinas que conviertan datos entre los tipos presentados y transmitidos; estas rutinas también deben liberar la memoria que se usa para contener los datos convertidos.</span><span class="sxs-lookup"><span data-stu-id="e252a-124">To use the **\[transmit\_as\]** attribute, the user must supply routines that convert data between the presented and the transmitted types; these routines must also free memory used to hold the converted data.</span></span> <span data-ttu-id="e252a-125">El atributo **\[ Transmit \_ as \]** indica al código auxiliar que llame a las rutinas de conversión proporcionadas por el usuario.</span><span class="sxs-lookup"><span data-stu-id="e252a-125">The **\[transmit\_as\]** attribute instructs the stubs to call the user-supplied conversion routines.</span></span>

<span data-ttu-id="e252a-126">El tipo *de transmisión de* tipos transmitidos debe resolverse en un tipo base de MIDL, un tipo predefinido o un identificador de tipo.</span><span class="sxs-lookup"><span data-stu-id="e252a-126">The transmitted type *xmit-type* must resolve to a MIDL base type, predefined type, or a type identifier.</span></span> <span data-ttu-id="e252a-127">Para obtener más información, vea [tipos base de MIDL](midl-base-types.md).</span><span class="sxs-lookup"><span data-stu-id="e252a-127">For more information, see [MIDL Base Types](midl-base-types.md).</span></span>

<span data-ttu-id="e252a-128">El usuario debe proporcionar las rutinas siguientes.</span><span class="sxs-lookup"><span data-stu-id="e252a-128">The user must supply the following routines.</span></span>



| <span data-ttu-id="e252a-129">Nombre de rutina</span><span class="sxs-lookup"><span data-stu-id="e252a-129">Routine name</span></span>              | <span data-ttu-id="e252a-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="e252a-130">Description</span></span>                                                                                                                                                                                                       |
|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e252a-131">*Type-ID \* \* \* \_ para la \_ transmisión*\*</span><span class="sxs-lookup"><span data-stu-id="e252a-131">*type-id\*\*\*\_to\_xmit*\*</span></span>   | <span data-ttu-id="e252a-132">Convierte los datos del tipo presentado al tipo transmitido.</span><span class="sxs-lookup"><span data-stu-id="e252a-132">Converts data from the presented type to the transmitted type.</span></span> <span data-ttu-id="e252a-133">Esta rutina asigna memoria para el tipo transmitido y para los datos a los que hacen referencia los punteros en el tipo transmitido.</span><span class="sxs-lookup"><span data-stu-id="e252a-133">This routine allocates memory for the transmitted type and for any data referenced by pointers in the transmitted type.</span></span>                            |
| <span data-ttu-id="e252a-134">*ID. de tipo \* \* \* \_ de \_ transmisión*\*</span><span class="sxs-lookup"><span data-stu-id="e252a-134">*type-id\*\*\*\_from\_xmit*\*</span></span> | <span data-ttu-id="e252a-135">Convierte los datos del tipo transmitido al tipo presentado.</span><span class="sxs-lookup"><span data-stu-id="e252a-135">Converts data from the transmitted type to the presented type.</span></span> <span data-ttu-id="e252a-136">Esta rutina es responsable de la asignación de memoria para los datos a los que hacen referencia los punteros en el tipo presentado.</span><span class="sxs-lookup"><span data-stu-id="e252a-136">This routine is responsible for allocating memory for data referenced by pointers in the presented type.</span></span> <span data-ttu-id="e252a-137">RPC asigna memoria para el propio tipo.</span><span class="sxs-lookup"><span data-stu-id="e252a-137">RPC allocates memory for the type itself.</span></span> |
| <span data-ttu-id="e252a-138">*ID. de tipo \* \* \_ \* \_ inst.*\*</span><span class="sxs-lookup"><span data-stu-id="e252a-138">*type-id\*\*\*\_free\_inst*\*</span></span> | <span data-ttu-id="e252a-139">Libera la memoria asignada para los datos a los que hacen referencia los punteros en el tipo presentado.</span><span class="sxs-lookup"><span data-stu-id="e252a-139">Frees memory allocated for data referenced by pointers in the presented type.</span></span> <span data-ttu-id="e252a-140">RPC libera memoria para el propio tipo.</span><span class="sxs-lookup"><span data-stu-id="e252a-140">RPC frees memory for the type itself.</span></span>                                                                                               |
| <span data-ttu-id="e252a-141">*tipo-ID \* \* \* \_ \_ transmisión gratuita*\*</span><span class="sxs-lookup"><span data-stu-id="e252a-141">*type-id\*\*\*\_free\_xmit*\*</span></span> | <span data-ttu-id="e252a-142">Libera el almacenamiento utilizado por el llamador para el tipo transmitido y para los datos a los que hacen referencia los punteros en el tipo transmitido.</span><span class="sxs-lookup"><span data-stu-id="e252a-142">Frees storage used by the caller for the transmitted type and for data referenced by pointers in the transmitted type.</span></span>                                                                                            |



 

 

<span data-ttu-id="e252a-143">El código auxiliar del cliente llama al *ID. de tipo \* \* \* \_ para la \_ transmisión*\* para asignar espacio para el tipo transmitido y para traducir los datos en objetos de tipo *tipo de transmisión.*</span><span class="sxs-lookup"><span data-stu-id="e252a-143">The client stub calls *type-id\*\*\*\_to\_xmit*\* to allocate space for the transmitted type and to translate the data into objects of type *xmit-type.*</span></span> <span data-ttu-id="e252a-144">El código auxiliar del servidor asigna espacio para el tipo de datos original y llama al *identificador de tipo \* \* \* \_ desde \_ transmisión*\* para traducir los datos de su tipo transmitido al tipo presentado.</span><span class="sxs-lookup"><span data-stu-id="e252a-144">The server stub allocates space for the original data type and calls *type-id\*\*\*\_from\_xmit*\* to translate the data from its transmitted type to the presented type.</span></span>

<span data-ttu-id="e252a-145">Al volver del código de la aplicación, el código auxiliar del servidor llama a *type-id \* \* \* \_ Free \_ inst*\* para desasignar el almacenamiento para el ID. de *tipo* en el lado del servidor.</span><span class="sxs-lookup"><span data-stu-id="e252a-145">Upon return from the application code, the server stub calls *type-id\*\*\*\_free\_inst*\* to deallocate the storage for *type-id* on the server side.</span></span> <span data-ttu-id="e252a-146">El código auxiliar del cliente llama al *identificador de tipo \* \* \* \_ \_ transmisión gratuita*\* para desasignar el almacenamiento del *tipo de transmisión* en el lado cliente.</span><span class="sxs-lookup"><span data-stu-id="e252a-146">The client stub calls *type-id\*\*\*\_free\_xmit*\* to deallocate the *xmit-type* storage on the client side.</span></span>

<span data-ttu-id="e252a-147">Los tipos siguientes no pueden tener un atributo de **\[ transmisión \_ como \]** :</span><span class="sxs-lookup"><span data-stu-id="e252a-147">The following types cannot have a **\[transmit\_as\]** attribute:</span></span>

-   <span data-ttu-id="e252a-148">Identificadores de contexto (tipos con el atributo de tipo de **\[** [**\_ identificador de contexto**](context-handle.md) **\]** y los tipos que se usan como parámetros con el atributo de **\[ \_ identificador \] de contexto** )</span><span class="sxs-lookup"><span data-stu-id="e252a-148">Context handles (types with the **\[**[**context\_handle**](context-handle.md)**\]** type attribute and types that are used as parameters with the **\[context\_handle\]** attribute)</span></span>
-   <span data-ttu-id="e252a-149">Tipos que se canalizan o derivan de canalizaciones</span><span class="sxs-lookup"><span data-stu-id="e252a-149">Types that are pipes or derived from pipes</span></span>
-   <span data-ttu-id="e252a-150">Tipos de datos que se usan como tipo base de una definición de canalización</span><span class="sxs-lookup"><span data-stu-id="e252a-150">Data types that are used as the base type of a pipe definition</span></span>
-   <span data-ttu-id="e252a-151">Parámetros que son punteros o se resuelven en punteros</span><span class="sxs-lookup"><span data-stu-id="e252a-151">Parameters that are pointers or resolve to pointers</span></span>
-   <span data-ttu-id="e252a-152">Parámetros que son compatibles, variables o matrices de apertura</span><span class="sxs-lookup"><span data-stu-id="e252a-152">Parameters that are conformant, varying, or open arrays</span></span>
-   <span data-ttu-id="e252a-153">Estructuras que contienen matrices compatibles</span><span class="sxs-lookup"><span data-stu-id="e252a-153">Structures that contain conformant arrays</span></span>
-   <span data-ttu-id="e252a-154">Identificador de tipo predefinido [**\_ t**](handle-t.md), [**void**](void.md)</span><span class="sxs-lookup"><span data-stu-id="e252a-154">The predefined type [**handle\_t**](handle-t.md), [**void**](void.md)</span></span>

<span data-ttu-id="e252a-155">Los tipos que se transmiten deben cumplir las restricciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="e252a-155">Types that are transmitted must conform to the following restrictions:</span></span>

-   <span data-ttu-id="e252a-156">No deben ser punteros ni contener punteros.</span><span class="sxs-lookup"><span data-stu-id="e252a-156">They must not be pointers or contain pointers.</span></span>
-   <span data-ttu-id="e252a-157">No deben ser canalizaciones ni contener canalizaciones.</span><span class="sxs-lookup"><span data-stu-id="e252a-157">They must not be pipes or contain pipes.</span></span>

## <a name="examples"></a><span data-ttu-id="e252a-158">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="e252a-158">Examples</span></span>

``` syntax
typedef struct _TREE_NODE_TYPE 
{ 
    unsigned short data; 
    struct _TREE_NODE_TYPE * left; 
    struct _TREE_NODE_TYPE * right; 
} TREE_NODE_TYPE; 
 
typedef [transmit_as(TREE_XMIT_TYPE)] TREE_NODE_TYPE * TREE_TYPE; 
 
void __RPC_USER TREE_TYPE_to_xmit( 
    TREE_TYPE __RPC_FAR * , 
    TREE_XMIT_TYPE __RPC_FAR * __RPC_FAR *); 
 
void __RPC_USER TREE_TYPE_from_xmit ( 
    TREE_XMIT_TYPE __RPC_FAR *, 
    TREE_TYPE __RPC_FAR *); 
 
void __RPC_USER TREE_TYPE_free_inst( 
    TREE_TYPE __RPC_FAR *); 
 
void __RPC_USER TREE_TYPE_free_xmit( 
    TREE_XMIT_TYPE __RPC_FAR *);
```

## <a name="see-also"></a><span data-ttu-id="e252a-159">Vea también</span><span class="sxs-lookup"><span data-stu-id="e252a-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e252a-160">**matrices**</span><span class="sxs-lookup"><span data-stu-id="e252a-160">**arrays**</span></span>](arrays-1.md)
</dt> <dt>

[<span data-ttu-id="e252a-161">Tipos base de MIDL</span><span class="sxs-lookup"><span data-stu-id="e252a-161">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="e252a-162">**identificador de contexto \_**</span><span class="sxs-lookup"><span data-stu-id="e252a-162">**context\_handle**</span></span>](context-handle.md)
</dt> <dt>

[<span data-ttu-id="e252a-163">**enumeración**</span><span class="sxs-lookup"><span data-stu-id="e252a-163">**enum**</span></span>](enum.md)
</dt> <dt>

[<span data-ttu-id="e252a-164">**asa**</span><span class="sxs-lookup"><span data-stu-id="e252a-164">**handle**</span></span>](handle.md)
</dt> <dt>

[<span data-ttu-id="e252a-165">**identificador \_ t**</span><span class="sxs-lookup"><span data-stu-id="e252a-165">**handle\_t**</span></span>](handle-t.md)
</dt> <dt>

[<span data-ttu-id="e252a-166">Archivo de definición de interfaz (IDL)</span><span class="sxs-lookup"><span data-stu-id="e252a-166">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="e252a-167">**omitir**</span><span class="sxs-lookup"><span data-stu-id="e252a-167">**ignore**</span></span>](ignore.md)
</dt> <dt>

[<span data-ttu-id="e252a-168">**ptr**</span><span class="sxs-lookup"><span data-stu-id="e252a-168">**ptr**</span></span>](ptr.md)
</dt> <dt>

[<span data-ttu-id="e252a-169">**ref**</span><span class="sxs-lookup"><span data-stu-id="e252a-169">**ref**</span></span>](ref.md)
</dt> <dt>

[<span data-ttu-id="e252a-170">**string**</span><span class="sxs-lookup"><span data-stu-id="e252a-170">**string**</span></span>](string.md)
</dt> <dt>

[<span data-ttu-id="e252a-171">**Destructor**</span><span class="sxs-lookup"><span data-stu-id="e252a-171">**struct**</span></span>](struct.md)
</dt> <dt>

[<span data-ttu-id="e252a-172">**tipo de conmutador \_**</span><span class="sxs-lookup"><span data-stu-id="e252a-172">**switch\_type**</span></span>](switch-type.md)
</dt> <dt>

[<span data-ttu-id="e252a-173">**typedef**</span><span class="sxs-lookup"><span data-stu-id="e252a-173">**typedef**</span></span>](typedef.md)
</dt> <dt>

[<span data-ttu-id="e252a-174">**Unión**</span><span class="sxs-lookup"><span data-stu-id="e252a-174">**union**</span></span>](union.md)
</dt> <dt>

[<span data-ttu-id="e252a-175">**espeficarse**</span><span class="sxs-lookup"><span data-stu-id="e252a-175">**unique**</span></span>](unique.md)
</dt> <dt>

[<span data-ttu-id="e252a-176">**void**</span><span class="sxs-lookup"><span data-stu-id="e252a-176">**void**</span></span>](void.md)
</dt> </dl>

 

 