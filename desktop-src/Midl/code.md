---
title: atributo Code
description: El atributo \ Code \ ACF hace que se genere código auxiliar de cliente para las funciones remotas.
ms.assetid: 735a8c25-29d4-4073-a2db-88bc8615ccc1
keywords:
- código MIDL del atributo Code
topic_type:
- apiref
api_name:
- code
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa041859c0bffca2771695b7055105b8ae846221
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104358270"
---
# <a name="code-attribute"></a><span data-ttu-id="85cce-104">atributo Code</span><span class="sxs-lookup"><span data-stu-id="85cce-104">code attribute</span></span>

<span data-ttu-id="85cce-105">El atributo ACF de **\[ código \]** hace que se genere código auxiliar de cliente para las funciones remotas.</span><span class="sxs-lookup"><span data-stu-id="85cce-105">The **\[code\]** ACF attribute causes client stub code to be generated for remote functions.</span></span>

``` syntax
[
    code [ , ACF-interface-attributes ] 
] 
interface interface-name
{
  [ include filename-list ; ]
  [ typedef [type-attribute-list] typenam; ]
  [ [code [ , ACF-function-attributes ]] function-name (
            [ ACF-parameter-attributes ] parameter-name,
        ...);
  ]
    ...
}
```

## <a name="parameters"></a><span data-ttu-id="85cce-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="85cce-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="85cce-107">*ACF-interfaz-atributos*</span><span class="sxs-lookup"><span data-stu-id="85cce-107">*ACF-interface-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="85cce-108">Especifica una lista de uno o más atributos que se aplican a la interfaz en conjunto.</span><span class="sxs-lookup"><span data-stu-id="85cce-108">Specifies a list of one or more attributes that apply to the interface as a whole.</span></span> <span data-ttu-id="85cce-109">Entre los atributos válidos se incluyen el [**\[ \_ controlador \] auto**](auto-handle.md) o el [**\[ \_ identificador \] implícito**](implicit-handle.md) y **\[ code \]**, [**\[ \] nocode**](nocode.md)u [**\[ Optimize \]**](optimize.md).</span><span class="sxs-lookup"><span data-stu-id="85cce-109">Valid attributes include either [**\[auto\_handle\]**](auto-handle.md) or [**\[implicit\_handle\]**](implicit-handle.md) and either **\[code\]**, [**\[nocode\]**](nocode.md), or [**\[optimize\]**](optimize.md).</span></span> <span data-ttu-id="85cce-110">Cuando dos o más atributos de interfaz están presentes, deben separarse con comas.</span><span class="sxs-lookup"><span data-stu-id="85cce-110">When two or more interface attributes are present, they must be separated by commas.</span></span>

</dd> <dt>

<span data-ttu-id="85cce-111">*nombre de interfaz*</span><span class="sxs-lookup"><span data-stu-id="85cce-111">*interface-name*</span></span> 
</dt> <dd>

<span data-ttu-id="85cce-112">Especifica el nombre de la interfaz.</span><span class="sxs-lookup"><span data-stu-id="85cce-112">Specifies the name of the interface.</span></span>

</dd> <dt>

<span data-ttu-id="85cce-113">*nombre de archivo-lista*</span><span class="sxs-lookup"><span data-stu-id="85cce-113">*filename-list*</span></span> 
</dt> <dd>

<span data-ttu-id="85cce-114">Especifica una lista de uno o más nombres de archivo de encabezado C, separados por comas.</span><span class="sxs-lookup"><span data-stu-id="85cce-114">Specifies a list of one or more C-header file names, separated by commas.</span></span> <span data-ttu-id="85cce-115">Debe proporcionar el nombre de archivo completo, incluida la extensión.</span><span class="sxs-lookup"><span data-stu-id="85cce-115">You must supply the full file name, including the extension.</span></span>

</dd> <dt>

<span data-ttu-id="85cce-116">*lista de atributos de tipo*</span><span class="sxs-lookup"><span data-stu-id="85cce-116">*type-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="85cce-117">Especifica una lista de uno o varios atributos, separados por comas, que se aplican al tipo especificado.</span><span class="sxs-lookup"><span data-stu-id="85cce-117">Specifies a list of one or more attributes, separated by commas, that apply to the specified type.</span></span> <span data-ttu-id="85cce-118">Entre los atributos de tipo válidos se incluyen [**\[ \] asignar**](allocate.md) y [**\[ representar \_ como \]**](represent-as.md).</span><span class="sxs-lookup"><span data-stu-id="85cce-118">Valid type attributes include [**\[allocate\]**](allocate.md) and [**\[represent\_as\]**](represent-as.md).</span></span>

</dd> <dt>

<span data-ttu-id="85cce-119">*nombreDeTipo*</span><span class="sxs-lookup"><span data-stu-id="85cce-119">*typename*</span></span> 
</dt> <dd>

<span data-ttu-id="85cce-120">Especifica un tipo definido en el archivo IDL.</span><span class="sxs-lookup"><span data-stu-id="85cce-120">Specifies a type defined in the IDL file.</span></span> <span data-ttu-id="85cce-121">Los atributos de tipo de ACF solo se pueden aplicar a los tipos definidos anteriormente en el archivo IDL.</span><span class="sxs-lookup"><span data-stu-id="85cce-121">Type attributes in the ACF can be applied only to types previously defined in the IDL file.</span></span>

</dd> <dt>

<span data-ttu-id="85cce-122">*ACF: atributos de función*</span><span class="sxs-lookup"><span data-stu-id="85cce-122">*ACF-function-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="85cce-123">Especifica cero o más atributos que se aplican a la función en su totalidad, como el [**\[ \_ estado \] de COMM**](comm-status.md).</span><span class="sxs-lookup"><span data-stu-id="85cce-123">Specifies zero or more attributes that apply to the function as a whole, such as [**\[comm\_status\]**](comm-status.md).</span></span> <span data-ttu-id="85cce-124">Los atributos de función se incluyen entre corchetes.</span><span class="sxs-lookup"><span data-stu-id="85cce-124">Function attributes are enclosed in square brackets.</span></span> <span data-ttu-id="85cce-125">Separe varios atributos de función con comas.</span><span class="sxs-lookup"><span data-stu-id="85cce-125">Separate multiple function attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="85cce-126">*nombre-de-la-función*</span><span class="sxs-lookup"><span data-stu-id="85cce-126">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="85cce-127">Especifica el nombre de la función tal y como se define en el archivo IDL.</span><span class="sxs-lookup"><span data-stu-id="85cce-127">Specifies the name of the function as defined in the IDL file.</span></span>

</dd> <dt>

<span data-ttu-id="85cce-128">*ACF-Parameter-Attributes*</span><span class="sxs-lookup"><span data-stu-id="85cce-128">*ACF-parameter-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="85cce-129">Especifica los atributos ACF que se aplican a un parámetro.</span><span class="sxs-lookup"><span data-stu-id="85cce-129">Specifies ACF attributes that apply to a parameter.</span></span> <span data-ttu-id="85cce-130">Tenga en cuenta que se pueden aplicar cero, uno o varios atributos al parámetro.</span><span class="sxs-lookup"><span data-stu-id="85cce-130">Note that zero, one, or more attributes can be applied to the parameter.</span></span> <span data-ttu-id="85cce-131">Separe varios atributos de parámetro con comas.</span><span class="sxs-lookup"><span data-stu-id="85cce-131">Separate multiple parameter attributes with commas.</span></span> <span data-ttu-id="85cce-132">Los atributos del parámetro ACF se incluyen entre corchetes.</span><span class="sxs-lookup"><span data-stu-id="85cce-132">ACF parameter attributes are enclosed in square brackets.</span></span>

</dd> <dt>

<span data-ttu-id="85cce-133">*nombre de parámetro*</span><span class="sxs-lookup"><span data-stu-id="85cce-133">*parameter-name*</span></span> 
</dt> <dd>

<span data-ttu-id="85cce-134">Especifica un parámetro de la función tal y como se define en el archivo IDL.</span><span class="sxs-lookup"><span data-stu-id="85cce-134">Specifies a parameter of the function as defined in the IDL file.</span></span> <span data-ttu-id="85cce-135">Cada parámetro de la función se debe especificar en la misma secuencia y con el mismo nombre que el definido en el archivo IDL.</span><span class="sxs-lookup"><span data-stu-id="85cce-135">Each parameter for the function must be specified in the same sequence and with the same name as defined in the IDL file.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="85cce-136">Observaciones</span><span class="sxs-lookup"><span data-stu-id="85cce-136">Remarks</span></span>

<span data-ttu-id="85cce-137">El atributo **\[ code \]** puede aparecer en el encabezado ACF o aplicarse a una función individual.</span><span class="sxs-lookup"><span data-stu-id="85cce-137">The **\[code\]** attribute can appear in the ACF header or be applied to an individual function.</span></span>

<span data-ttu-id="85cce-138">Cuando el atributo **\[ code \]** aparece en el encabezado ACF, se genera código auxiliar de cliente para todas las funciones remotas que no tienen el atributo de función [**\[ nocode \]**](nocode.md) .</span><span class="sxs-lookup"><span data-stu-id="85cce-138">When the **\[code\]** attribute appears in the ACF header, client stub code is generated for all remote functions that do not have the [**\[nocode\]**](nocode.md) function attribute.</span></span> <span data-ttu-id="85cce-139">Puede invalidar el atributo **\[ code \]** en el encabezado de una función individual especificando el atributo **\[ nocode \]** como un atributo de función.</span><span class="sxs-lookup"><span data-stu-id="85cce-139">You can override the **\[code\]** attribute in the header for an individual function by specifying the **\[nocode\]** attribute as a function attribute.</span></span>

<span data-ttu-id="85cce-140">Cuando el atributo **\[ code \]** aparece en la lista de atributos de la función remota, se genera código auxiliar de cliente para la función.</span><span class="sxs-lookup"><span data-stu-id="85cce-140">When the **\[code\]** attribute appears in the remote function's attribute list, client stub code is generated for the function.</span></span> <span data-ttu-id="85cce-141">El código auxiliar de cliente no se genera cuando:</span><span class="sxs-lookup"><span data-stu-id="85cce-141">Client stub code is not generated when:</span></span>

-   <span data-ttu-id="85cce-142">El encabezado ACF incluye el atributo [**\[ nocode \]**](nocode.md) .</span><span class="sxs-lookup"><span data-stu-id="85cce-142">The ACF header includes the [**\[nocode\]**](nocode.md) attribute.</span></span>
-   <span data-ttu-id="85cce-143">El atributo [**\[ nocode \]**](nocode.md) se aplica a la función.</span><span class="sxs-lookup"><span data-stu-id="85cce-143">The [**\[nocode\]**](nocode.md) attribute is applied to the function.</span></span>
-   <span data-ttu-id="85cce-144">El atributo [**\[ local \]**](local.md) se aplica a la función en el archivo de interfaz.</span><span class="sxs-lookup"><span data-stu-id="85cce-144">The [**\[local\]**](local.md) attribute applies to the function in the interface file.</span></span>

<span data-ttu-id="85cce-145">**\[ Code \]** o [**\[ nocode \]**](nocode.md) pueden aparecer en la lista de atributos de interfaz o función, pero el que elija solo puede aparecer una vez en la lista.</span><span class="sxs-lookup"><span data-stu-id="85cce-145">Either **\[code\]** or [**\[nocode\]**](nocode.md) can appear in the interface or function attribute list, but the one you choose can appear only once in the list.</span></span>

## <a name="see-also"></a><span data-ttu-id="85cce-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="85cce-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85cce-147">Archivo de configuración de la aplicación (ACF)</span><span class="sxs-lookup"><span data-stu-id="85cce-147">Application Configuration File (ACF)</span></span>](application-configuration-file-acf-.md)
</dt> <dt>

[<span data-ttu-id="85cce-148">**allocate**</span><span class="sxs-lookup"><span data-stu-id="85cce-148">**allocate**</span></span>](allocate.md)
</dt> <dt>

[<span data-ttu-id="85cce-149">**\_identificador automático**</span><span class="sxs-lookup"><span data-stu-id="85cce-149">**auto\_handle**</span></span>](auto-handle.md)
</dt> <dt>

[<span data-ttu-id="85cce-150">**Estado de COMM \_**</span><span class="sxs-lookup"><span data-stu-id="85cce-150">**comm\_status**</span></span>](comm-status.md)
</dt> <dt>

[<span data-ttu-id="85cce-151">**\_identificador implícito**</span><span class="sxs-lookup"><span data-stu-id="85cce-151">**implicit\_handle**</span></span>](implicit-handle.md)
</dt> <dt>

[<span data-ttu-id="85cce-152">**localizar**</span><span class="sxs-lookup"><span data-stu-id="85cce-152">**local**</span></span>](local.md)
</dt> <dt>

[<span data-ttu-id="85cce-153">**nocode**</span><span class="sxs-lookup"><span data-stu-id="85cce-153">**nocode**</span></span>](nocode.md)
</dt> <dt>

[<span data-ttu-id="85cce-154">**optimiz**</span><span class="sxs-lookup"><span data-stu-id="85cce-154">**optimize**</span></span>](optimize.md)
</dt> <dt>

[<span data-ttu-id="85cce-155">**representar \_ como**</span><span class="sxs-lookup"><span data-stu-id="85cce-155">**represent\_as**</span></span>](represent-as.md)
</dt> </dl>

 

 




