---
title: interface (atributo)
description: La palabra clave interface especifica el nombre de la interfaz. El nombre de la interfaz debe proporcionarse en el archivo IDL y en el ACF.
ms.assetid: 239b782e-57de-493c-b2f4-310d1859a9ae
keywords:
- atributo de interfaz MIDL
topic_type:
- apiref
api_name:
- interface
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 852c29b2ba7b43e9d8b15863e60db8ad2fbde33f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103904536"
---
# <a name="interface-attribute"></a><span data-ttu-id="14eac-105">interface (atributo)</span><span class="sxs-lookup"><span data-stu-id="14eac-105">interface attribute</span></span>

<span data-ttu-id="14eac-106">La palabra clave **interface** especifica el nombre de la interfaz.</span><span class="sxs-lookup"><span data-stu-id="14eac-106">The **interface** keyword specifies the name of the interface.</span></span> <span data-ttu-id="14eac-107">El nombre de la interfaz debe proporcionarse en el archivo IDL y en el ACF.</span><span class="sxs-lookup"><span data-stu-id="14eac-107">The interface name must be provided in both the IDL file and the ACF.</span></span>

``` syntax
[ 
    interface-attribute-list 
] 
interface interface-name [ : base-interface ]
{
}

typedef interface interface-name declarator-list
```

## <a name="parameters"></a><span data-ttu-id="14eac-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="14eac-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="14eac-109">*interfaz-atributo-lista*</span><span class="sxs-lookup"><span data-stu-id="14eac-109">*interface-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="14eac-110">Especifica los atributos que se aplican a la interfaz en conjunto.</span><span class="sxs-lookup"><span data-stu-id="14eac-110">Specifies attributes that apply to the interface as a whole.</span></span> <span data-ttu-id="14eac-111">Los atributos de interfaz válidos para un archivo IDL incluyen el **\[** [**punto de conexión**](endpoint.md) **\]** , **\[** [**local**](local.md) **\]** , **\[** [**objeto**](object.md) **\]** , **\[** [**\_ valor predeterminado del puntero**](pointer-default.md), **\]** **\[** [**UUID**](uuid.md) **\]** y **\[** [**versión**](version.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="14eac-111">Valid interface attributes for an IDL file include **\[**[**endpoint**](endpoint.md)**\]**, **\[**[**local**](local.md)**\]**, **\[**[**object**](object.md)**\]**, **\[**[**pointer\_default**](pointer-default.md)**\]**, **\[**[**uuid**](uuid.md)**\]**, and **\[**[**version**](version.md)**\]**.</span></span> <span data-ttu-id="14eac-112">Los atributos de interfaz válidos para un ACF incluyen **\[** [**codificación**](encode.md) **\]** , **\[** [**descodificación**](decode.md) **\]** , **\[** [**\_ identificador automático**](auto-handle.md) **\]** o **\[** [**\_ identificador implícito**](implicit-handle.md) **\]** , y **\[** [**código**](code.md) **\]** o **\[** [**nocode**](nocode.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="14eac-112">Valid interface attributes for an ACF include **\[**[**encode**](encode.md)**\]**, **\[**[**decode**](decode.md)**\]**, either **\[**[**auto\_handle**](auto-handle.md)**\]** or **\[**[**implicit\_handle**](implicit-handle.md)**\]**, and either **\[**[**code**](code.md)**\]** or **\[**[**nocode**](nocode.md)**\]**.</span></span>

</dd> <dt>

<span data-ttu-id="14eac-113">*nombre de interfaz*</span><span class="sxs-lookup"><span data-stu-id="14eac-113">*interface-name*</span></span> 
</dt> <dd>

<span data-ttu-id="14eac-114">Especifica el nombre de la interfaz.</span><span class="sxs-lookup"><span data-stu-id="14eac-114">Specifies the name of the interface.</span></span> <span data-ttu-id="14eac-115">El nombre de la interfaz debe ser un nombre único y debe comenzar por un carácter alfabético o de subrayado.</span><span class="sxs-lookup"><span data-stu-id="14eac-115">The interface name must be a unique name and must start with an alphabetic or underscore character.</span></span>

</dd> <dt>

<span data-ttu-id="14eac-116">*interfaz base*</span><span class="sxs-lookup"><span data-stu-id="14eac-116">*base-interface*</span></span> 
</dt> <dd>

<span data-ttu-id="14eac-117">Especifica el nombre de una interfaz de la que esta interfaz derivada hereda las funciones miembro, los códigos de estado y los atributos de interfaz.</span><span class="sxs-lookup"><span data-stu-id="14eac-117">Specifies the name of an interface from which this derived interface inherits member functions, status codes, and interface attributes.</span></span> <span data-ttu-id="14eac-118">La interfaz derivada no hereda las definiciones de tipo.</span><span class="sxs-lookup"><span data-stu-id="14eac-118">The derived interface does not inherit type definitions.</span></span> <span data-ttu-id="14eac-119">Para ello, use la palabra clave [**Import**](import.md) para importar el archivo IDL de la interfaz base.</span><span class="sxs-lookup"><span data-stu-id="14eac-119">To do this, use the [**import**](import.md) keyword to import the IDL file of the base interface.</span></span>

</dd> <dt>

<span data-ttu-id="14eac-120">*lista de declaradores*</span><span class="sxs-lookup"><span data-stu-id="14eac-120">*declarator-list*</span></span> 
</dt> <dd>

<span data-ttu-id="14eac-121">Especifica los declaradores estándar de C, como identificadores, declaradores de puntero y declaradores de matriz.</span><span class="sxs-lookup"><span data-stu-id="14eac-121">Specifies standard C declarators, such as identifiers, pointer declarators, and array declarators.</span></span> <span data-ttu-id="14eac-122">Para obtener más información, vea matrices [y Sized-Pointer atributos](array-and-sized-pointer-attributes.md) [**, matrices**](arrays-1.md)y [matrices y punteros](/windows/desktop/Rpc/arrays-and-pointers).</span><span class="sxs-lookup"><span data-stu-id="14eac-122">For more information, see [Array and Sized-Pointer Attributes](array-and-sized-pointer-attributes.md), [**arrays**](arrays-1.md)., and [Arrays and Pointers](/windows/desktop/Rpc/arrays-and-pointers).</span></span> <span data-ttu-id="14eac-123">La *lista de declaradores* consta de uno o varios declaradores, separados por comas.</span><span class="sxs-lookup"><span data-stu-id="14eac-123">The *declarator-list* consists of one or more declarators, separated by commas.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="14eac-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="14eac-124">Remarks</span></span>

<span data-ttu-id="14eac-125">Los nombres de interfaz en el archivo IDL y ACF deben ser los mismos, excepto cuando se usa el modificador de compilador MIDL [**/ACF**](-acf.md).</span><span class="sxs-lookup"><span data-stu-id="14eac-125">The interface names in the IDL file and ACF must be the same, except when you use the MIDL compiler switch [**/acf**](-acf.md).</span></span>

<span data-ttu-id="14eac-126">El nombre de la interfaz forma la primera parte del nombre de las estructuras de datos de identificador de interfaz que son parámetros de las funciones en tiempo de ejecución de RPC.</span><span class="sxs-lookup"><span data-stu-id="14eac-126">The interface name forms the first part of the name of interface-handle data structures that are parameters to the RPC run-time functions.</span></span> <span data-ttu-id="14eac-127">Para obtener más información, vea [**RPC \_ If \_ Handle**](/windows/desktop/Rpc/rpc-if-handle).</span><span class="sxs-lookup"><span data-stu-id="14eac-127">For more information, see [**RPC\_IF\_HANDLE**](/windows/desktop/Rpc/rpc-if-handle).</span></span>

<span data-ttu-id="14eac-128">Si el encabezado de la interfaz incluye el **\[** [](object.md) **\]** atributo de objeto para indicar una interfaz com, también debe incluir el **\[** atributo [**UUID**](uuid.md) **\]** y debe especificar la interfaz com base de la que se deriva.</span><span class="sxs-lookup"><span data-stu-id="14eac-128">If the interface header includes the **\[**[**object**](object.md)**\]** attribute to indicate a COM interface, it must also include the **\[**[**uuid**](uuid.md)**\]** attribute and must specify the base COM interface from which it is derived.</span></span> <span data-ttu-id="14eac-129">Para obtener más información sobre las interfaces COM, vea **\[** [**Object**](object.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="14eac-129">For more information about COM interfaces, see **\[**[**object**](object.md)**\]**.</span></span>

<span data-ttu-id="14eac-130">También puede utilizar la palabra clave **interface** con la palabra clave [**typedef**](typedef.md) para definir un tipo de datos de interfaz.</span><span class="sxs-lookup"><span data-stu-id="14eac-130">You can also use the **interface** keyword with the [**typedef**](typedef.md) keyword to define an interface data type.</span></span>

## <a name="examples"></a><span data-ttu-id="14eac-131">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="14eac-131">Examples</span></span>

``` syntax
/* use of interface keyword in IDL file for an RPC interface */ 
[ 
    uuid (00000000-0000-0000-0000-000000000000), 
    version (1.0) 
] 
interface remote_if_2 
{  
    // Interface definition statements.
} 
 
/* use of interface keyword in ACF for an RPC interface */ 
[
    implicit_handle( handle_t xa_bhandle ) 
] 
interface remote_if_2 
{ 
    // Attribute configuration statements.
} 
 
/* use of interface keyword in IDL file for a COM interface */ 
[ 
    object, uuid (00000000-0000-0000-0000-000000000000) 
] 
interface IDerivedInterface : IBaseInterface 
{  
    import "base.idl" 
    Save(); 
} 
 
/* use of interface keyword to define an interface pointer type */ 
typedef interface IStorage *LPSTORAGE;
```

## <a name="see-also"></a><span data-ttu-id="14eac-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="14eac-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14eac-133">Archivo de configuración de la aplicación (ACF)</span><span class="sxs-lookup"><span data-stu-id="14eac-133">Application Configuration File (ACF)</span></span>](application-configuration-file-acf-.md)
</dt> <dt>

[<span data-ttu-id="14eac-134">**finales**</span><span class="sxs-lookup"><span data-stu-id="14eac-134">**endpoint**</span></span>](endpoint.md)
</dt> <dt>

[<span data-ttu-id="14eac-135">Archivo de definición de interfaz (IDL)</span><span class="sxs-lookup"><span data-stu-id="14eac-135">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="14eac-136">**localizar**</span><span class="sxs-lookup"><span data-stu-id="14eac-136">**local**</span></span>](local.md)
</dt> <dt>

[<span data-ttu-id="14eac-137">**objeto**</span><span class="sxs-lookup"><span data-stu-id="14eac-137">**object**</span></span>](object.md)
</dt> <dt>

[<span data-ttu-id="14eac-138">**puntero \_ predeterminado**</span><span class="sxs-lookup"><span data-stu-id="14eac-138">**pointer\_default**</span></span>](pointer-default.md)
</dt> <dt>

[<span data-ttu-id="14eac-139">**identificador de RPC \_ If \_**</span><span class="sxs-lookup"><span data-stu-id="14eac-139">**RPC\_IF\_HANDLE**</span></span>](/windows/desktop/Rpc/rpc-if-handle)
</dt> <dt>

[<span data-ttu-id="14eac-140">**typedef**</span><span class="sxs-lookup"><span data-stu-id="14eac-140">**typedef**</span></span>](typedef.md)
</dt> <dt>

[<span data-ttu-id="14eac-141">**uuid**</span><span class="sxs-lookup"><span data-stu-id="14eac-141">**uuid**</span></span>](uuid.md)
</dt> <dt>

[<span data-ttu-id="14eac-142">**Versión**</span><span class="sxs-lookup"><span data-stu-id="14eac-142">**version**</span></span>](version.md)
</dt> </dl>

 

 