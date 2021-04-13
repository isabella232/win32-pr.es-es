---
title: nocode (atributo)
description: El atributo \ nocode \ se usa en encabezados ACF o con funciones individuales para evitar la generación de código auxiliar de cliente.
ms.assetid: d3b6e4c8-103c-4ea2-8748-11d844fdda97
keywords:
- atributo nocode MIDL
topic_type:
- apiref
api_name:
- nocode
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64f5138dc1794e9b2714e5f64762c1af17b47fb2
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104357997"
---
# <a name="nocode-attribute"></a><span data-ttu-id="91da8-104">nocode (atributo)</span><span class="sxs-lookup"><span data-stu-id="91da8-104">nocode attribute</span></span>

<span data-ttu-id="91da8-105">El atributo **\[ nocode \]** se usa en encabezados ACF o en funciones individuales para evitar la generación de código auxiliar de cliente.</span><span class="sxs-lookup"><span data-stu-id="91da8-105">The **\[nocode\]** attribute is used in ACF headers or with individual functions to prevent the generation of client stub code.</span></span>

``` syntax
[ 
    nocode 
    [ , ACF-interface-attributes ] 
] 
interface interface-name
{
  [ include filename-list ; ]
  [ typedef [type-attribute-list] typename; ] 
  [ [ nocode [ , ACF-function-attributes ] ] function-name (
        [ ACF-parameter-attributes ] parameter-name ;
        ...);
  ]
    ...
}
```

## <a name="parameters"></a><span data-ttu-id="91da8-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="91da8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="91da8-107">*ACF-interfaz-atributos*</span><span class="sxs-lookup"><span data-stu-id="91da8-107">*ACF-interface-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="91da8-108">Especifica una lista de uno o más atributos que se aplican a la interfaz en conjunto.</span><span class="sxs-lookup"><span data-stu-id="91da8-108">Specifies a list of one or more attributes that apply to the interface as a whole.</span></span> <span data-ttu-id="91da8-109">Entre los atributos válidos se incluyen el **\[** [**\_ controlador auto**](auto-handle.md) **\]** o el **\[** [**\_ identificador implícito**](implicit-handle.md) **\]** y **\[** [**code**](code.md) **\]** o **\[ \] nocode**.</span><span class="sxs-lookup"><span data-stu-id="91da8-109">Valid attributes include either **\[**[**auto\_handle**](auto-handle.md)**\]** or **\[**[**implicit\_handle**](implicit-handle.md)**\]** and either **\[**[**code**](code.md)**\]** or **\[nocode\]**.</span></span> <span data-ttu-id="91da8-110">Cuando dos o más atributos de interfaz están presentes, deben separarse con comas.</span><span class="sxs-lookup"><span data-stu-id="91da8-110">When two or more interface attributes are present, they must be separated by commas.</span></span>

</dd> <dt>

<span data-ttu-id="91da8-111">*nombre de interfaz*</span><span class="sxs-lookup"><span data-stu-id="91da8-111">*interface-name*</span></span> 
</dt> <dd>

<span data-ttu-id="91da8-112">Especifica el nombre de la interfaz.</span><span class="sxs-lookup"><span data-stu-id="91da8-112">Specifies the name of the interface.</span></span> <span data-ttu-id="91da8-113">En el modo de compatibilidad con DCE, el nombre de la interfaz debe coincidir con el nombre de la interfaz especificada en el archivo IDL.</span><span class="sxs-lookup"><span data-stu-id="91da8-113">In DCE-compatibility mode, the interface name must match the name of the interface specified in the IDL file.</span></span> <span data-ttu-id="91da8-114">Cuando se usa el modificador de compilador de MIDL [**/ACF**](-acf.md), el nombre de la interfaz en ACF y el nombre de la interfaz en el archivo IDL pueden ser diferentes.</span><span class="sxs-lookup"><span data-stu-id="91da8-114">When you use the MIDL compiler switch [**/acf**](-acf.md), the interface name in the ACF and the interface name in the IDL file can be different.</span></span>

</dd> <dt>

<span data-ttu-id="91da8-115">*nombre de archivo-lista*</span><span class="sxs-lookup"><span data-stu-id="91da8-115">*filename-list*</span></span> 
</dt> <dd>

<span data-ttu-id="91da8-116">Especifica una lista de uno o más nombres de archivo de encabezado de lenguaje C, separados por comas.</span><span class="sxs-lookup"><span data-stu-id="91da8-116">Specifies a list of one or more C-language header file names, separated by commas.</span></span> <span data-ttu-id="91da8-117">Se debe proporcionar el nombre de archivo completo, incluida la extensión.</span><span class="sxs-lookup"><span data-stu-id="91da8-117">The full file name, including the extension, must be supplied.</span></span>

</dd> <dt>

<span data-ttu-id="91da8-118">*lista de atributos de tipo*</span><span class="sxs-lookup"><span data-stu-id="91da8-118">*type-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="91da8-119">Especifica una lista de uno o varios atributos, separados por comas, que se aplican al tipo especificado.</span><span class="sxs-lookup"><span data-stu-id="91da8-119">Specifies a list of one or more attributes, separated by commas, that apply to the specified type.</span></span> <span data-ttu-id="91da8-120">Entre los atributos de tipo válidos se incluyen **\[** [**asignar**](allocate.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="91da8-120">Valid type attributes include **\[**[**allocate**](allocate.md)**\]**.</span></span>

</dd> <dt>

<span data-ttu-id="91da8-121">*nombreDeTipo*</span><span class="sxs-lookup"><span data-stu-id="91da8-121">*typename*</span></span> 
</dt> <dd>

<span data-ttu-id="91da8-122">Especifica un tipo definido en el archivo IDL.</span><span class="sxs-lookup"><span data-stu-id="91da8-122">Specifies a type defined in the IDL file.</span></span> <span data-ttu-id="91da8-123">Los atributos de tipo de ACF solo se pueden aplicar a los tipos definidos anteriormente en el archivo IDL.</span><span class="sxs-lookup"><span data-stu-id="91da8-123">Type attributes in the ACF can only be applied to types previously defined in the IDL file.</span></span>

</dd> <dt>

<span data-ttu-id="91da8-124">*ACF: atributos de función*</span><span class="sxs-lookup"><span data-stu-id="91da8-124">*ACF-function-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="91da8-125">Especifica los atributos que se aplican a la función en su totalidad, como el **\[** [**\_ Estado de COMM**](comm-status.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="91da8-125">Specifies attributes that apply to the function as a whole, such as **\[**[**comm\_status**](comm-status.md)**\]**.</span></span> <span data-ttu-id="91da8-126">Los atributos de función se incluyen entre corchetes.</span><span class="sxs-lookup"><span data-stu-id="91da8-126">Function attributes are enclosed in square brackets.</span></span> <span data-ttu-id="91da8-127">Separe varios atributos de función con comas.</span><span class="sxs-lookup"><span data-stu-id="91da8-127">Separate multiple function attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="91da8-128">*nombre-de-la-función*</span><span class="sxs-lookup"><span data-stu-id="91da8-128">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="91da8-129">Especifica el nombre de la función tal y como se define en el archivo IDL.</span><span class="sxs-lookup"><span data-stu-id="91da8-129">Specifies the name of the function as defined in the IDL file.</span></span>

</dd> <dt>

<span data-ttu-id="91da8-130">*ACF-Parameter-Attributes*</span><span class="sxs-lookup"><span data-stu-id="91da8-130">*ACF-parameter-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="91da8-131">Especifica los atributos ACF que se aplican a un parámetro.</span><span class="sxs-lookup"><span data-stu-id="91da8-131">Specifies ACF attributes that apply to a parameter.</span></span> <span data-ttu-id="91da8-132">Tenga en cuenta que se pueden aplicar cero o más atributos al parámetro.</span><span class="sxs-lookup"><span data-stu-id="91da8-132">Note that zero or more attributes can be applied to the parameter.</span></span> <span data-ttu-id="91da8-133">Separe varios atributos de parámetro con comas.</span><span class="sxs-lookup"><span data-stu-id="91da8-133">Separate multiple parameter attributes with commas.</span></span> <span data-ttu-id="91da8-134">Los atributos del parámetro ACF se incluyen entre corchetes.</span><span class="sxs-lookup"><span data-stu-id="91da8-134">ACF parameter attributes are enclosed in square brackets.</span></span>

</dd> <dt>

<span data-ttu-id="91da8-135">*nombre de parámetro*</span><span class="sxs-lookup"><span data-stu-id="91da8-135">*parameter-name*</span></span> 
</dt> <dd>

<span data-ttu-id="91da8-136">Especifica un parámetro de la función tal y como se define en el archivo IDL.</span><span class="sxs-lookup"><span data-stu-id="91da8-136">Specifies a parameter of the function as defined in the IDL file.</span></span> <span data-ttu-id="91da8-137">Cada parámetro de la función se debe especificar en la misma secuencia y usar el mismo nombre que el definido en el archivo IDL.</span><span class="sxs-lookup"><span data-stu-id="91da8-137">Each parameter for the function must be specified in the same sequence and using the same name as defined in the IDL file.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="91da8-138">Observaciones</span><span class="sxs-lookup"><span data-stu-id="91da8-138">Remarks</span></span>

<span data-ttu-id="91da8-139">El atributo **\[ nocode \]** puede aparecer en el encabezado ACF, o bien se puede aplicar a una función individual.</span><span class="sxs-lookup"><span data-stu-id="91da8-139">The **\[nocode\]** attribute can appear in the ACF header, or it can be applied to an individual function.</span></span>

<span data-ttu-id="91da8-140">Cuando el atributo **\[ \] nocode** aparece en el encabezado ACF, no se genera código auxiliar de cliente para ninguna función remota a menos que tenga el atributo de función de **\[** [**código**](code.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="91da8-140">When the **\[nocode\]** attribute appears in the ACF header, client stub code is not generated for any remote function unless it has the **\[**[**code**](code.md)**\]** function attribute.</span></span> <span data-ttu-id="91da8-141">Puede invalidar el atributo **\[ nocode \]** en el encabezado de una función individual especificando el atributo **\[ code \]** como un atributo de función.</span><span class="sxs-lookup"><span data-stu-id="91da8-141">You can override the **\[nocode\]** attribute in the header for an individual function by specifying the **\[code\]** attribute as a function attribute.</span></span>

<span data-ttu-id="91da8-142">Cuando el atributo **\[ nocode \]** aparece en la lista de atributos de la función, no se genera ningún código auxiliar de cliente para la función.</span><span class="sxs-lookup"><span data-stu-id="91da8-142">When the **\[nocode\]** attribute appears in the function's attribute list, no client stub code is generated for the function.</span></span>

<span data-ttu-id="91da8-143">El código auxiliar de cliente no se genera cuando:</span><span class="sxs-lookup"><span data-stu-id="91da8-143">Client stub code is not generated when:</span></span>

-   <span data-ttu-id="91da8-144">El encabezado ACF incluye el atributo **\[ nocode \]** .</span><span class="sxs-lookup"><span data-stu-id="91da8-144">The ACF header includes the **\[nocode\]** attribute.</span></span>
-   <span data-ttu-id="91da8-145">El atributo **\[ nocode \]** se aplica a la función.</span><span class="sxs-lookup"><span data-stu-id="91da8-145">The **\[nocode\]** attribute is applied to the function.</span></span>
-   <span data-ttu-id="91da8-146">El **\[** atributo [**local**](local.md) **\]** se aplica a la función en el archivo de interfaz.</span><span class="sxs-lookup"><span data-stu-id="91da8-146">The **\[**[**local**](local.md)**\]** attribute applies to the function in the interface file.</span></span>

<span data-ttu-id="91da8-147">**\[** [](code.md) **\]** Puede aparecer código o **\[ nocode \]** en la lista de atributos de una función y el que elija puede aparecer exactamente una vez.</span><span class="sxs-lookup"><span data-stu-id="91da8-147">Either **\[**[**code**](code.md)**\]** or **\[nocode\]** can appear in a function's attribute list, and the one you choose can appear exactly once.</span></span>

<span data-ttu-id="91da8-148">El atributo **\[ nocode \]** se omite cuando se generan códigos auxiliares de servidor.</span><span class="sxs-lookup"><span data-stu-id="91da8-148">The **\[nocode\]** attribute is ignored when server stubs are generated.</span></span> <span data-ttu-id="91da8-149">No se puede aplicar al generar códigos auxiliares de servidor en modo de compatibilidad de DCE.</span><span class="sxs-lookup"><span data-stu-id="91da8-149">You cannot apply it when generating server stubs in DCE-compatibility mode.</span></span>

## <a name="see-also"></a><span data-ttu-id="91da8-150">Vea también</span><span class="sxs-lookup"><span data-stu-id="91da8-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91da8-151">Archivo de configuración de la aplicación (ACF)</span><span class="sxs-lookup"><span data-stu-id="91da8-151">Application Configuration File (ACF)</span></span>](application-configuration-file-acf-.md)
</dt> <dt>

[<span data-ttu-id="91da8-152">**/acf**</span><span class="sxs-lookup"><span data-stu-id="91da8-152">**/acf**</span></span>](-acf.md)
</dt> <dt>

[<span data-ttu-id="91da8-153">**allocate**</span><span class="sxs-lookup"><span data-stu-id="91da8-153">**allocate**</span></span>](allocate.md)
</dt> <dt>

[<span data-ttu-id="91da8-154">**\_identificador automático**</span><span class="sxs-lookup"><span data-stu-id="91da8-154">**auto\_handle**</span></span>](auto-handle.md)
</dt> <dt>

[<span data-ttu-id="91da8-155">**codifica**</span><span class="sxs-lookup"><span data-stu-id="91da8-155">**code**</span></span>](code.md)
</dt> <dt>

[<span data-ttu-id="91da8-156">**Estado de COMM \_**</span><span class="sxs-lookup"><span data-stu-id="91da8-156">**comm\_status**</span></span>](comm-status.md)
</dt> <dt>

[<span data-ttu-id="91da8-157">**\_identificador implícito**</span><span class="sxs-lookup"><span data-stu-id="91da8-157">**implicit\_handle**</span></span>](implicit-handle.md)
</dt> </dl>

 

 




