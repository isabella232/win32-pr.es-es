---
title: represent_as atributo)
description: El atributo \ representated \_ as \ ACF asocia un tipo local con nombre en el lenguaje de destino repr-Type con un tipo de transferencia denominado-Type que se transfiere entre el cliente y el servidor.
ms.assetid: ae44d220-e8f3-47a3-8f5e-a2668ac75411
keywords:
- represent_as el atributo MIDL
topic_type:
- apiref
api_name:
- represent_as
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a17d0b8915e75bb3065b394ef76900bd8efb5e0c
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104076482"
---
# <a name="represent_as-attribute"></a><span data-ttu-id="be61c-104">representar \_ como atributo</span><span class="sxs-lookup"><span data-stu-id="be61c-104">represent\_as attribute</span></span>

<span data-ttu-id="be61c-105">El atributo **\[ representa \_ como \]** ACF asocia un tipo local con nombre en el lenguaje de destino *repr-Type* con un tipo *de transferencia denominado-Type* que se transfiere entre el cliente y el servidor.</span><span class="sxs-lookup"><span data-stu-id="be61c-105">The **\[represent\_as\]** ACF attribute associates a named local type in the target language *repr-type* with a transfer type *named-type* that is transferred between client and server.</span></span>

``` syntax
typedef [represent_as(repr-type) [[ , type-attribute-list ]] ] named-type; 
void __RPC_USER named-type_from_local (
  repr-type __RPC_FAR * ,
  named-type __RPC_FAR * __RPC_FAR * );
void __RPC_USER named-type_to_local (
  named-type __RPC_FAR * ,
  repr-type __RPC_FAR * ); void __RPC_USER named-type _free_inst ( named-type __RPC_FAR * ); void __RPC_USER named-type _free_local ( repr-type __RPC_FAR * );
```

## <a name="parameters"></a><span data-ttu-id="be61c-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="be61c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="be61c-107">*tipo con nombre*</span><span class="sxs-lookup"><span data-stu-id="be61c-107">*named-type*</span></span> 
</dt> <dd>

<span data-ttu-id="be61c-108">Especifica el tipo de datos de transferencia con nombre que se transfiere entre el cliente y el servidor.</span><span class="sxs-lookup"><span data-stu-id="be61c-108">Specifies the named transfer data type that is transferred between client and server.</span></span>

</dd> <dt>

<span data-ttu-id="be61c-109">*lista de atributos de tipo*</span><span class="sxs-lookup"><span data-stu-id="be61c-109">*type-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="be61c-110">Especifica uno o más atributos que se aplican al tipo.</span><span class="sxs-lookup"><span data-stu-id="be61c-110">Specifies one or more attributes that apply to the type.</span></span> <span data-ttu-id="be61c-111">Separe varios atributos con comas.</span><span class="sxs-lookup"><span data-stu-id="be61c-111">Separate multiple attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="be61c-112">*tipo de repr*</span><span class="sxs-lookup"><span data-stu-id="be61c-112">*repr-type*</span></span> 
</dt> <dd>

<span data-ttu-id="be61c-113">Especifica el tipo local representado en el lenguaje de destino que se presenta a las aplicaciones de cliente y de servidor.</span><span class="sxs-lookup"><span data-stu-id="be61c-113">Specifies the represented local type in the target language that is presented to the client and server applications.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="be61c-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="be61c-114">Remarks</span></span>

<span data-ttu-id="be61c-115">Al usar **\[ representar \_ como \]**, debe proporcionar rutinas que conviertan entre los tipos de transferencia local y y que la memoria libre usada para contener los datos convertidos.</span><span class="sxs-lookup"><span data-stu-id="be61c-115">When using **\[represent\_as\]**, you must supply routines that convert between the local and the transfer types and that free memory used to hold the converted data.</span></span> <span data-ttu-id="be61c-116">El atributo **\[ representa \_ como \]** indica al código auxiliar que llame a las rutinas de conversión proporcionadas por el usuario.</span><span class="sxs-lookup"><span data-stu-id="be61c-116">The **\[represent\_as\]** attribute instructs the stubs to call the user-supplied conversion routines.</span></span>

<span data-ttu-id="be61c-117">El tipo transferido *denominado-Type* debe resolverse en un tipo base de MIDL, un tipo predefinido o en un identificador de tipo.</span><span class="sxs-lookup"><span data-stu-id="be61c-117">The transferred type *named-type* must resolve to a MIDL base type, predefined type, or to a type identifier.</span></span> <span data-ttu-id="be61c-118">Para obtener más información, vea [tipos base de MIDL](midl-base-types.md).</span><span class="sxs-lookup"><span data-stu-id="be61c-118">For more information, see [MIDL Base Types](midl-base-types.md).</span></span>

<span data-ttu-id="be61c-119">Debe proporcionar las siguientes rutinas:</span><span class="sxs-lookup"><span data-stu-id="be61c-119">You must supply the following routines:</span></span>



| <span data-ttu-id="be61c-120">Nombre de rutina</span><span class="sxs-lookup"><span data-stu-id="be61c-120">Routine name</span></span>                   | <span data-ttu-id="be61c-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="be61c-121">Description</span></span>                                                                                                                                                                                                |
|--------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="be61c-122">*tipo con nombre \_ \* \* \* \_ de \_ local*\*</span><span class="sxs-lookup"><span data-stu-id="be61c-122">*named\_type\*\*\*\_from\_local*\*</span></span> | <span data-ttu-id="be61c-123">Convierte los datos del tipo local al tipo de red.</span><span class="sxs-lookup"><span data-stu-id="be61c-123">Converts data from the local type to the network type.</span></span> <span data-ttu-id="be61c-124">La rutina asigna memoria para el tipo de datos de red, incluida la memoria para los datos a los que hacen referencia los punteros en el tipo de datos de red.</span><span class="sxs-lookup"><span data-stu-id="be61c-124">The routine allocates memory for the network data type, including memory for any data referenced by pointers in the network data type.</span></span>              |
| <span data-ttu-id="be61c-125">*tipo con nombre \_ \* \* \* \_ a \_ local*\*</span><span class="sxs-lookup"><span data-stu-id="be61c-125">*named\_type\*\*\*\_to\_local*\*</span></span>   | <span data-ttu-id="be61c-126">Convierte los datos del tipo de red al tipo local.</span><span class="sxs-lookup"><span data-stu-id="be61c-126">Converts data from the network type to the local type.</span></span> <span data-ttu-id="be61c-127">La rutina es responsable de la asignación de memoria para los datos a los que hacen referencia los punteros en el tipo local.</span><span class="sxs-lookup"><span data-stu-id="be61c-127">The routine is responsible for allocating memory for data referenced by pointers in the local type.</span></span> <span data-ttu-id="be61c-128">RPC asigna memoria para el propio tipo local.</span><span class="sxs-lookup"><span data-stu-id="be61c-128">RPC allocates memory for the local type itself.</span></span> |
| <span data-ttu-id="be61c-129">*tipo con nombre \_ \* \* \_ \* \_ local gratis*\*</span><span class="sxs-lookup"><span data-stu-id="be61c-129">*named\_type\*\*\*\_free\_local*\*</span></span> | <span data-ttu-id="be61c-130">Libera la memoria asignada para los datos a los que hacen referencia los punteros en el tipo local.</span><span class="sxs-lookup"><span data-stu-id="be61c-130">Frees memory allocated for data referenced by pointers in the local type.</span></span> <span data-ttu-id="be61c-131">RPC libera memoria para el propio tipo.</span><span class="sxs-lookup"><span data-stu-id="be61c-131">RPC frees memory for the type itself</span></span>                                                                                             |
| <span data-ttu-id="be61c-132">*tipo con nombre \_ \* \* \_ \* \_ inst. inst.*\*</span><span class="sxs-lookup"><span data-stu-id="be61c-132">*named\_type\*\*\*\_free\_inst*\*</span></span>  | <span data-ttu-id="be61c-133">Libera la memoria asignada para los datos a los que hacen referencia los punteros en el tipo de red y para el propio tipo de red.</span><span class="sxs-lookup"><span data-stu-id="be61c-133">Frees memory allocated for the data referenced by pointers in the network type and for the network type itself.</span></span>                                                                                            |



 

<span data-ttu-id="be61c-134">El código auxiliar del cliente llama a *denominado-Type \* \* \* \_ desde \_ local*\* para asignar espacio para el tipo transmitido y para traducir los datos del tipo local al tipo de red.</span><span class="sxs-lookup"><span data-stu-id="be61c-134">The client stub calls *named-type\*\*\*\_from\_local*\* to allocate space for the transmitted type and to translate the data from the local type to the network type.</span></span> <span data-ttu-id="be61c-135">El código auxiliar del servidor asigna espacio para el tipo de datos original y llama al tipo *con nombre \* \* \* \_ a \_ local*\* para traducir los datos del tipo de red al tipo local.</span><span class="sxs-lookup"><span data-stu-id="be61c-135">The server stub allocates space for the original data type and calls *named-type\*\*\*\_to\_local*\* to translate the data from the network type to the local type.</span></span>

<span data-ttu-id="be61c-136">Al volver del código de la aplicación, el código auxiliar del cliente y del servidor llama a la *función con nombre-tipo \* \* \* \_ Free \_ inst*\* para desasignar el almacenamiento para el tipo de red.</span><span class="sxs-lookup"><span data-stu-id="be61c-136">Upon return from the application code, the client and server stubs call *named-type\*\*\*\_free\_inst*\* to deallocate the storage for network type.</span></span> <span data-ttu-id="be61c-137">El código auxiliar del cliente llama al *tipo denominado \* \* \* \_ \_ local gratis*\* para desasignar el almacenamiento devuelto por la rutina.</span><span class="sxs-lookup"><span data-stu-id="be61c-137">The client stub calls *named-type\*\*\*\_free\_local*\* to deallocate storage returned by the routine.</span></span>

<span data-ttu-id="be61c-138">Los tipos siguientes no pueden tener un atributo **\[ representated \_ as \]** :</span><span class="sxs-lookup"><span data-stu-id="be61c-138">The following types cannot have a **\[represent\_as\]** attribute:</span></span>

-   <span data-ttu-id="be61c-139">Matrices conformes, variadas o conformes</span><span class="sxs-lookup"><span data-stu-id="be61c-139">Conformant, varying, or conformant-varying arrays</span></span>
-   <span data-ttu-id="be61c-140">Estructuras en las que el último miembro es una matriz compatible (una estructura compatible)</span><span class="sxs-lookup"><span data-stu-id="be61c-140">Structures in which the last member is a conformant array (a conformant structure)</span></span>
-   <span data-ttu-id="be61c-141">Punteros o tipos que contienen un puntero</span><span class="sxs-lookup"><span data-stu-id="be61c-141">Pointers or types that contain a pointer</span></span>
-   <span data-ttu-id="be61c-142">Canalizaciones o tipos que contienen canalizaciones</span><span class="sxs-lookup"><span data-stu-id="be61c-142">Pipes or types that contain pipes</span></span>
-   <span data-ttu-id="be61c-143">Tipos que se usan como tipo base para una canalización</span><span class="sxs-lookup"><span data-stu-id="be61c-143">Types that are used as the base type for a pipe</span></span>
-   <span data-ttu-id="be61c-144">Identificador de tipos predefinidos [**\_ t**](handle-t.md), [**void**](void.md)</span><span class="sxs-lookup"><span data-stu-id="be61c-144">Predefined types [**handle\_t**](handle-t.md), [**void**](void.md)</span></span>
-   <span data-ttu-id="be61c-145">Tipos que tienen el atributo [**\[ Handle \]**](handle.md)</span><span class="sxs-lookup"><span data-stu-id="be61c-145">Types that have the [**\[handle\]**](handle.md) attribute</span></span>

## <a name="examples"></a><span data-ttu-id="be61c-146">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="be61c-146">Examples</span></span>

``` syntax
//these data types defined in .IDL or elsewhere
typedef struct  _lbox 
{ 
    long         data; 
    struct _lbox *next; 
} lbox; 
typedef [ref] lbox *PBOX_LOC; 
typedef long LONG4[4]; 
 
//in .ACF file :
interface iface
{
    typedef  [ represent_as(PBOX_LOC) ]  LONG4; 
}
```

## <a name="see-also"></a><span data-ttu-id="be61c-147">Vea también</span><span class="sxs-lookup"><span data-stu-id="be61c-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be61c-148">Archivo de configuración de la aplicación (ACF)</span><span class="sxs-lookup"><span data-stu-id="be61c-148">Application Configuration File (ACF)</span></span>](application-configuration-file-acf-.md)
</dt> <dt>

[<span data-ttu-id="be61c-149">**matrices**</span><span class="sxs-lookup"><span data-stu-id="be61c-149">**arrays**</span></span>](arrays-1.md)
</dt> <dt>

[<span data-ttu-id="be61c-150">Tipos base de MIDL</span><span class="sxs-lookup"><span data-stu-id="be61c-150">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="be61c-151">**identificador \_ t**</span><span class="sxs-lookup"><span data-stu-id="be61c-151">**handle\_t**</span></span>](handle-t.md)
</dt> <dt>

[<span data-ttu-id="be61c-152">**typedef**</span><span class="sxs-lookup"><span data-stu-id="be61c-152">**typedef**</span></span>](typedef.md)
</dt> <dt>

[<span data-ttu-id="be61c-153">**void**</span><span class="sxs-lookup"><span data-stu-id="be61c-153">**void**</span></span>](void.md)
</dt> </dl>

 

 




