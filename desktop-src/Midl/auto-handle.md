---
title: auto_handle atributo)
description: El atributo \ auto \_ Handle \ ACF indica al código auxiliar que establezca automáticamente el enlace para una función que no tenga un parámetro de control de enlace explícito. Tenga en cuenta que este atributo está obsoleto y ya no se admite.
ms.assetid: a402b933-f69b-4dfe-b0c5-b034d65d4a84
keywords:
- auto_handle el atributo MIDL
topic_type:
- apiref
api_name:
- auto_handle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01e9a4c91fac8553867536f4f5a8c3094e0f0ff9
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104487118"
---
# <a name="auto_handle-attribute"></a><span data-ttu-id="08eb1-104">\_atributo de control automático</span><span class="sxs-lookup"><span data-stu-id="08eb1-104">auto\_handle attribute</span></span>

<span data-ttu-id="08eb1-105">El atributo ACF de **\[ \_ control \] automático** indica al código auxiliar que establezca automáticamente el enlace para una función que no tenga un parámetro de control de enlace explícito.</span><span class="sxs-lookup"><span data-stu-id="08eb1-105">The **\[auto\_handle\]** ACF attribute directs the stub to automatically establish the binding for a function that does not have an explicit binding-handle parameter.</span></span>

> [!Note]  
> <span data-ttu-id="08eb1-106">Este atributo está obsoleto y ya no se admite.</span><span class="sxs-lookup"><span data-stu-id="08eb1-106">This attribute is obsolete and no longer supported.</span></span> <span data-ttu-id="08eb1-107">Se recomienda el uso del modificador [**/Robust**](-robust.md) .</span><span class="sxs-lookup"><span data-stu-id="08eb1-107">Use of the [**/robust**](-robust.md) switch is recommended.</span></span>

 

``` syntax
[ 
    auto_handle [, interface-attribute-list] 
] 
interface interface-name
{
    interface-definition
}
```

## <a name="parameters"></a><span data-ttu-id="08eb1-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="08eb1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="08eb1-109">*interfaz-atributo-lista*</span><span class="sxs-lookup"><span data-stu-id="08eb1-109">*interface-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="08eb1-110">Especifica cero o más atributos que se aplican a la interfaz en conjunto, como [**código**](code.md) o [**nocode**](nocode.md).</span><span class="sxs-lookup"><span data-stu-id="08eb1-110">Specifies zero or more attributes that apply to the interface as a whole, such as [**code**](code.md) or [**nocode**](nocode.md).</span></span> <span data-ttu-id="08eb1-111">Separe los atributos de interfaz con comas.</span><span class="sxs-lookup"><span data-stu-id="08eb1-111">Separate interface attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="08eb1-112">*nombre de interfaz*</span><span class="sxs-lookup"><span data-stu-id="08eb1-112">*interface-name*</span></span> 
</dt> <dd>

<span data-ttu-id="08eb1-113">Especifica el nombre de la interfaz.</span><span class="sxs-lookup"><span data-stu-id="08eb1-113">Specifies the name of the interface.</span></span>

</dd> <dt>

<span data-ttu-id="08eb1-114">*definición de interfaz*</span><span class="sxs-lookup"><span data-stu-id="08eb1-114">*interface-definition*</span></span> 
</dt> <dd>

<span data-ttu-id="08eb1-115">Especifica las instrucciones IDL que forman la definición de la interfaz.</span><span class="sxs-lookup"><span data-stu-id="08eb1-115">Specifies IDL statements that form the definition of the interface.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="08eb1-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="08eb1-116">Remarks</span></span>

<span data-ttu-id="08eb1-117">El atributo de **\[ \_ identificador \] automático** aparece en el encabezado de la interfaz del ACF.</span><span class="sxs-lookup"><span data-stu-id="08eb1-117">The **\[auto\_handle\]** attribute appears in the interface header of the ACF.</span></span> <span data-ttu-id="08eb1-118">También aparece en el encabezado de interfaz del archivo IDL cuando se especifica el modificador de compilador MIDL [**/App \_ config**](-app-config.md).</span><span class="sxs-lookup"><span data-stu-id="08eb1-118">It also appears in the interface header of the IDL file when you specify the MIDL compiler switch [**/app\_config**](-app-config.md).</span></span>

<span data-ttu-id="08eb1-119">Cuando el cliente llama a una función que utiliza el enlace automático y no existe ningún enlace a un servidor, el código auxiliar establece automáticamente el enlace.</span><span class="sxs-lookup"><span data-stu-id="08eb1-119">When the client calls a function that uses automatic binding and no binding to a server exists, the stub automatically establishes the binding.</span></span> <span data-ttu-id="08eb1-120">El enlace se reutiliza para las llamadas posteriores a otras funciones de la interfaz que utilizan el enlace automático.</span><span class="sxs-lookup"><span data-stu-id="08eb1-120">The binding is reused for subsequent calls to other functions in the interface that use automatic binding.</span></span> <span data-ttu-id="08eb1-121">El programa de aplicación cliente no tiene que declarar ni realizar ningún procesamiento relacionado con el identificador de enlace.</span><span class="sxs-lookup"><span data-stu-id="08eb1-121">The client application program does not have to declare or perform any processing relating to the binding handle.</span></span>

<span data-ttu-id="08eb1-122">Cuando el ACF no está presente o no incluye el atributo de [**\[ \_ identificador \] implícito**](implicit-handle.md) , el compilador MIDL usa el **\[ \_ \] identificador automático** y emite un mensaje informativo.</span><span class="sxs-lookup"><span data-stu-id="08eb1-122">When the ACF is not present or does not include the [**\[implicit\_handle\]**](implicit-handle.md) attribute, the MIDL compiler uses **\[auto\_handle\]** and issues an informational message.</span></span> <span data-ttu-id="08eb1-123">El compilador MIDL también utiliza el **\[ \_ identificador \] automático**, si es necesario, para establecer el enlace inicial de un [**\[ \_ identificador \] de contexto**](context-handle.md).</span><span class="sxs-lookup"><span data-stu-id="08eb1-123">The MIDL compiler also uses **\[auto\_handle\]**, if needed, to establish the initial binding for a [**\[context\_handle\]**](context-handle.md).</span></span>

<span data-ttu-id="08eb1-124">El atributo de **\[ \_ identificador \] automático** solo puede producirse si no se produce el [**\[ \_ identificador \] implícito**](implicit-handle.md) o el atributo de [**\[ \_ identificador \] explícito**](explicit-handle.md) .</span><span class="sxs-lookup"><span data-stu-id="08eb1-124">The **\[auto\_handle\]** attribute can occur only if the [**\[implicit\_handle\]**](implicit-handle.md) or [**\[explicit\_handle\]**](explicit-handle.md) attribute does not occur.</span></span> <span data-ttu-id="08eb1-125">El atributo de **\[ \_ identificador \] automático** puede aparecer en el encabezado de la interfaz ACF o IDL como máximo una vez.</span><span class="sxs-lookup"><span data-stu-id="08eb1-125">The **\[auto\_handle\]** attribute can occur in the ACF or IDL interface header at most once.</span></span>

> [!Note]  
> <span data-ttu-id="08eb1-126">No puede usar el enlace automático (ya sea con el atributo de **\[ \_ control \] automático** o de forma predeterminada) si está procesando datos a través de canalizaciones.</span><span class="sxs-lookup"><span data-stu-id="08eb1-126">You cannot use automatic binding (either with the **\[auto\_handle\]** attribute, or by default) if you are processing data through pipes.</span></span>

 

## <a name="examples"></a><span data-ttu-id="08eb1-127">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="08eb1-127">Examples</span></span>

``` syntax
[
    auto_handle
] 
interface MyInterface 
{ 
    /* Interface definition goes here*/
} 
[
    auto_handle, 
    code
] 
interface MyInterface
{ 
    /* Interface definition goes here*/
}
```

## <a name="see-also"></a><span data-ttu-id="08eb1-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="08eb1-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08eb1-129">Archivo de configuración de la aplicación (ACF)</span><span class="sxs-lookup"><span data-stu-id="08eb1-129">Application Configuration File (ACF)</span></span>](application-configuration-file-acf-.md)
</dt> <dt>

[<span data-ttu-id="08eb1-130">**configuración de/APP \_**</span><span class="sxs-lookup"><span data-stu-id="08eb1-130">**/app\_config**</span></span>](-app-config.md)
</dt> <dt>

[<span data-ttu-id="08eb1-131">**codifica**</span><span class="sxs-lookup"><span data-stu-id="08eb1-131">**code**</span></span>](code.md)
</dt> <dt>

[<span data-ttu-id="08eb1-132">**\_identificador explícito**</span><span class="sxs-lookup"><span data-stu-id="08eb1-132">**explicit\_handle**</span></span>](explicit-handle.md)
</dt> <dt>

[<span data-ttu-id="08eb1-133">**identificador de contexto \_**</span><span class="sxs-lookup"><span data-stu-id="08eb1-133">**context\_handle**</span></span>](context-handle.md)
</dt> <dt>

[<span data-ttu-id="08eb1-134">**\_identificador implícito**</span><span class="sxs-lookup"><span data-stu-id="08eb1-134">**implicit\_handle**</span></span>](implicit-handle.md)
</dt> <dt>

[<span data-ttu-id="08eb1-135">**nocode**</span><span class="sxs-lookup"><span data-stu-id="08eb1-135">**nocode**</span></span>](nocode.md)
</dt> </dl>

 

 




