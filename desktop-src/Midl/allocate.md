---
title: asignar atributo
description: El atributo \ allocate \ ACF permite personalizar la asignación y desasignación de memoria para un tipo definido en el archivo IDL.
ms.assetid: 1956b11f-bafa-41c3-9025-5fcbb890d1a2
keywords:
- asignar el atributo MIDL
topic_type:
- apiref
api_name:
- allocate
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ff902e34e07ebd34edcb73797baa131eec8b222
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "103904037"
---
# <a name="allocate-attribute"></a><span data-ttu-id="d1a97-104">asignar atributo</span><span class="sxs-lookup"><span data-stu-id="d1a97-104">allocate attribute</span></span>

<span data-ttu-id="d1a97-105">El atributo **\[ allocate \]** ACF permite personalizar la asignación y desasignación de memoria para un tipo definido en el archivo IDL.</span><span class="sxs-lookup"><span data-stu-id="d1a97-105">The **\[allocate\]** ACF attribute lets you customize memory allocation and deallocation for a type defined in the IDL file.</span></span>

``` syntax
typedef [allocate (allocate-option-list) [, type-attribute-list] ] type-name;
```

## <a name="parameters"></a><span data-ttu-id="d1a97-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d1a97-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d1a97-107">*lista de opciones de asignación*</span><span class="sxs-lookup"><span data-stu-id="d1a97-107">*allocate-option-list*</span></span> 
</dt> <dd>

<span data-ttu-id="d1a97-108">Especifica una o más opciones de asignación de memoria.</span><span class="sxs-lookup"><span data-stu-id="d1a97-108">Specifies one or more memory-allocation options.</span></span> <span data-ttu-id="d1a97-109">Seleccione uno de **los \_ nodos** de un **solo \_ nodo** o de todos, o de uno de ellos **gratis** o **no \_ libre**, o de uno de los pares.</span><span class="sxs-lookup"><span data-stu-id="d1a97-109">Select one of either **single\_node** or **all\_nodes**, or one of either **free** or **dont\_free**, or one from each pair.</span></span> <span data-ttu-id="d1a97-110">Al especificar más de una opción, separe las opciones con comas.</span><span class="sxs-lookup"><span data-stu-id="d1a97-110">When you specify more than one option, separate the options with commas.</span></span>

</dd> <dt>

<span data-ttu-id="d1a97-111">*lista de atributos de tipo*</span><span class="sxs-lookup"><span data-stu-id="d1a97-111">*type-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="d1a97-112">Especifica otros atributos de tipo ACF opcionales.</span><span class="sxs-lookup"><span data-stu-id="d1a97-112">Specifies other optional ACF-type attributes.</span></span> <span data-ttu-id="d1a97-113">Al especificar más de un atributo de tipo, separe las opciones con comas.</span><span class="sxs-lookup"><span data-stu-id="d1a97-113">When you specify more than one type attribute, separate the options with commas.</span></span>

</dd> <dt>

<span data-ttu-id="d1a97-114">*nombre de tipo*</span><span class="sxs-lookup"><span data-stu-id="d1a97-114">*type-name*</span></span> 
</dt> <dd>

<span data-ttu-id="d1a97-115">Especifica un tipo definido en el archivo IDL.</span><span class="sxs-lookup"><span data-stu-id="d1a97-115">Specifies a type defined in the IDL file.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d1a97-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d1a97-116">Remarks</span></span>

<span data-ttu-id="d1a97-117">El atributo **\[ allocate \]** tiene las siguientes opciones válidas.</span><span class="sxs-lookup"><span data-stu-id="d1a97-117">The **\[allocate\]** attribute has the following valid options.</span></span>



| <span data-ttu-id="d1a97-118">Opción</span><span class="sxs-lookup"><span data-stu-id="d1a97-118">Option</span></span>           | <span data-ttu-id="d1a97-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="d1a97-119">Description</span></span>                                                           |
|------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="d1a97-120">**todos los \_ nodos**</span><span class="sxs-lookup"><span data-stu-id="d1a97-120">**all\_nodes**</span></span>   | <span data-ttu-id="d1a97-121">Realiza una llamada a para asignar y liberar memoria para todos los nodos.</span><span class="sxs-lookup"><span data-stu-id="d1a97-121">Makes one call to allocate and free memory for all nodes.</span></span>             |
| <span data-ttu-id="d1a97-122">**\_nodo único**</span><span class="sxs-lookup"><span data-stu-id="d1a97-122">**single\_node**</span></span> | <span data-ttu-id="d1a97-123">Realiza muchas llamadas individuales para asignar y liberar cada nodo de memoria.</span><span class="sxs-lookup"><span data-stu-id="d1a97-123">Makes many individual calls to allocate and free each node of memory.</span></span> |
| <span data-ttu-id="d1a97-124">**free**</span><span class="sxs-lookup"><span data-stu-id="d1a97-124">**free**</span></span>         | <span data-ttu-id="d1a97-125">Libera memoria al volver del código auxiliar del servidor.</span><span class="sxs-lookup"><span data-stu-id="d1a97-125">Frees memory on return from the server stub.</span></span>                          |
| <span data-ttu-id="d1a97-126">**no \_ gratis**</span><span class="sxs-lookup"><span data-stu-id="d1a97-126">**dont\_free**</span></span>   | <span data-ttu-id="d1a97-127">No libera memoria al volver del código auxiliar del servidor.</span><span class="sxs-lookup"><span data-stu-id="d1a97-127">Does not free memory on return from the server stub.</span></span>                  |



 

<span data-ttu-id="d1a97-128">De forma predeterminada, el código auxiliar puede asignar almacenamiento para los datos a los que hace referencia un puntero único o completo mediante una llamada a la [**\_ \_ asignación de usuarios de MIDL**](midl-user-allocate-1.md) y el [**usuario de MIDL \_ \_**](midl-user-free-1.md) de forma individual para cada puntero.</span><span class="sxs-lookup"><span data-stu-id="d1a97-128">By default, the stubs may allocate storage for data referenced by a unique or full pointer by calling [**midl\_user\_allocate**](midl-user-allocate-1.md) and [**midl\_user\_free**](midl-user-free-1.md) individually for each pointer.</span></span>

<span data-ttu-id="d1a97-129">Puede optimizar la velocidad de la aplicación especificando la opción **todos los \_ nodos**.</span><span class="sxs-lookup"><span data-stu-id="d1a97-129">You can optimize the speed of your application by specifying the option **all\_nodes**.</span></span> <span data-ttu-id="d1a97-130">Esta opción indica al código auxiliar que calcule el tamaño de toda la memoria a la que se hace referencia a través del puntero del tipo especificado y que realice una llamada única a la [**\_ \_ asignación de usuarios de MIDL**](midl-user-allocate-1.md).</span><span class="sxs-lookup"><span data-stu-id="d1a97-130">This option directs the stub to compute the size of all memory referenced through the pointer of the specified type and to make a single call to [**midl\_user\_allocate**](midl-user-allocate-1.md).</span></span> <span data-ttu-id="d1a97-131">El código auxiliar libera la memoria realizando una llamada a la versión [**\_ \_ gratuita del usuario de MIDL**](midl-user-free-1.md).</span><span class="sxs-lookup"><span data-stu-id="d1a97-131">The stub releases the memory by making one call to [**midl\_user\_free**](midl-user-free-1.md).</span></span>

<span data-ttu-id="d1a97-132">La opción **no \_ Free** indica al compilador de MIDL que genere un código auxiliar de servidor que no llame al [**usuario de MIDL \_ \_ Free**](midl-user-free-1.md) para el tipo especificado.</span><span class="sxs-lookup"><span data-stu-id="d1a97-132">The **dont\_free** option directs the MIDL compiler to generate a server stub that does not call [**midl\_user\_free**](midl-user-free-1.md) for the specified type.</span></span> <span data-ttu-id="d1a97-133">La opción **no \_ Free** permite que las estructuras de puntero sigan siendo accesibles para la aplicación de servidor después de que se haya completado la llamada a procedimiento remoto y se haya devuelto al cliente.</span><span class="sxs-lookup"><span data-stu-id="d1a97-133">The **dont\_free** option allows the pointer structures to remain accessible to the server application after the remote procedure call has completed and returned to the client.</span></span>

<span data-ttu-id="d1a97-134">El atributo **\[ allocate \]** producirá cualquier parámetro **\[ in, out \]** que sea un puntero a un tipo calificado con la opción **All \_ Nodes** para reasignar la memoria cuando no se calculan las referencias de los datos.</span><span class="sxs-lookup"><span data-stu-id="d1a97-134">The **\[allocate\]** attribute will cause any **\[in, out\]** parameter that is a pointer to a type qualified with the **all\_nodes** option to reallocate memory when the data is unmarshaled.</span></span> <span data-ttu-id="d1a97-135">Es responsabilidad de la aplicación liberar la memoria asignada previamente para este parámetro.</span><span class="sxs-lookup"><span data-stu-id="d1a97-135">It is the responsibility of the application to free the memory allocated previously for this parameter.</span></span> <span data-ttu-id="d1a97-136">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="d1a97-136">For example:</span></span>

``` syntax
typedef struct thistype 
{ 
    [string] char * PTHISTYPE;  
} * PTHISTYPE
HRESULT proc1 ( [in,out] PTHISTYPE * ppthistype);
```

<span data-ttu-id="d1a97-137">El código auxiliar reasignará el tipo de datos PTHISTYPE antes de la anulación de [**\[ \]**](out-idl.md) la serialización.</span><span class="sxs-lookup"><span data-stu-id="d1a97-137">The data type PTHISTYPE will be reallocated in the [**\[out\]**](out-idl.md) direction by the stub before unmarshaling.</span></span> <span data-ttu-id="d1a97-138">Por lo tanto, la aplicación debe liberar la memoria asignada previamente para los datos de este parámetro o se producirá una fuga de memoria.</span><span class="sxs-lookup"><span data-stu-id="d1a97-138">Therefore, the application must free the memory it previously allocated for this parameter's data, or a memory leak will occur.</span></span>

## <a name="examples"></a><span data-ttu-id="d1a97-139">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="d1a97-139">Examples</span></span>

``` syntax
/* ACF file */ 
typedef [allocate(all_nodes, dont_free)] PTYPE1; 
typedef [allocate(all_nodes)] PTYPE2; 
typedef [allocate(dont_free)] PTYPE3;
```

## <a name="see-also"></a><span data-ttu-id="d1a97-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="d1a97-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1a97-141">Archivo de configuración de la aplicación (ACF)</span><span class="sxs-lookup"><span data-stu-id="d1a97-141">Application Configuration File (ACF)</span></span>](application-configuration-file-acf-.md)
</dt> <dt>

[<span data-ttu-id="d1a97-142">**de**</span><span class="sxs-lookup"><span data-stu-id="d1a97-142">**in**</span></span>](in.md)
</dt> <dt>

[<span data-ttu-id="d1a97-143">**\_asignación de usuarios de MIDL \_**</span><span class="sxs-lookup"><span data-stu-id="d1a97-143">**midl\_user\_allocate**</span></span>](midl-user-allocate-1.md)
</dt> <dt>

[<span data-ttu-id="d1a97-144">**usuario de MIDL \_ \_ gratis**</span><span class="sxs-lookup"><span data-stu-id="d1a97-144">**midl\_user\_free**</span></span>](midl-user-free-1.md)
</dt> <dt>

[<span data-ttu-id="d1a97-145">**enuncia**</span><span class="sxs-lookup"><span data-stu-id="d1a97-145">**out**</span></span>](out-idl.md)
</dt> <dt>

[<span data-ttu-id="d1a97-146">**typedef**</span><span class="sxs-lookup"><span data-stu-id="d1a97-146">**typedef**</span></span>](typedef.md)
</dt> </dl>

 

 




