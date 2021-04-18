---
title: error_status_t atributo)
description: La \_ \_ palabra clave de estado de error t designa un tipo para un objeto que contiene información sobre el estado de la comunicación o el estado de error.
ms.assetid: 7eff0d20-c058-4f16-a3db-0b4c82303135
keywords:
- error_status_t el atributo MIDL
topic_type:
- apiref
api_name:
- error_status_t
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0d017b4eaf460b5d5b7ecb8a0bd79201ac8bdee
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104357999"
---
# <a name="error_status_t-attribute"></a><span data-ttu-id="0718e-104">atributo de estado de error \_ \_ t</span><span class="sxs-lookup"><span data-stu-id="0718e-104">error\_status\_t attribute</span></span>

<span data-ttu-id="0718e-105">La palabra clave de **Estado de error \_ \_ t** designa un tipo para un objeto que contiene información sobre el estado de la comunicación o el estado de error.</span><span class="sxs-lookup"><span data-stu-id="0718e-105">The **error\_status\_t** keyword designates a type for an object that contains communication-status or fault-status information.</span></span>

``` syntax
[ [ , ACF-function-attributes ] ] error_status_t function-name(
        [ [ ACF-parameter-attributes ] ] parameter-name
        , ...);

[ [ ACF-function-attributes ] ] function-name(
    [ [ ACF-parameter-attributes ] ] error_status_t parameter-name
    , ...);
```

## <a name="parameters"></a><span data-ttu-id="0718e-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0718e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0718e-107">*ACF: atributos de función*</span><span class="sxs-lookup"><span data-stu-id="0718e-107">*ACF-function-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="0718e-108">Especifica cero o más atributos de función ACF, como el **\[** [**\_ Estado de COMM**](comm-status.md) **\]** , el **\[** [**\_ Estado de error**](fault-status.md) **\]** o **\[** [**nocode**](nocode.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="0718e-108">Specifies zero or more ACF function attributes, such as **\[**[**comm\_status**](comm-status.md)**\]**, **\[**[**fault\_status**](fault-status.md)**\]**, or **\[**[**nocode**](nocode.md)**\]**.</span></span> <span data-ttu-id="0718e-109">Los atributos de función se incluyen entre corchetes.</span><span class="sxs-lookup"><span data-stu-id="0718e-109">Function attributes are enclosed in square brackets.</span></span> <span data-ttu-id="0718e-110">Cero o más atributos se pueden aplicar a una función.</span><span class="sxs-lookup"><span data-stu-id="0718e-110">Zero or more attributes can be applied to a function.</span></span> <span data-ttu-id="0718e-111">Separe varios atributos de función con comas.</span><span class="sxs-lookup"><span data-stu-id="0718e-111">Separate multiple function attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="0718e-112">*nombre-de-la-función*</span><span class="sxs-lookup"><span data-stu-id="0718e-112">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="0718e-113">Especifica el nombre de la función tal y como se define en el archivo IDL.</span><span class="sxs-lookup"><span data-stu-id="0718e-113">Specifies the name of the function as defined in the IDL file.</span></span>

</dd> <dt>

<span data-ttu-id="0718e-114">*ACF-Parameter-Attributes*</span><span class="sxs-lookup"><span data-stu-id="0718e-114">*ACF-parameter-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="0718e-115">Especifica los atributos que se aplican a un parámetro.</span><span class="sxs-lookup"><span data-stu-id="0718e-115">Specifies attributes that apply to a parameter.</span></span> <span data-ttu-id="0718e-116">Tenga en cuenta que se pueden aplicar cero, uno o varios atributos al parámetro.</span><span class="sxs-lookup"><span data-stu-id="0718e-116">Note that zero, one, or more attributes can be applied to the parameter.</span></span> <span data-ttu-id="0718e-117">Separe varios atributos de parámetro con comas.</span><span class="sxs-lookup"><span data-stu-id="0718e-117">Separate multiple parameter attributes with commas.</span></span> <span data-ttu-id="0718e-118">Los atributos de parámetro se incluyen entre corchetes.</span><span class="sxs-lookup"><span data-stu-id="0718e-118">Parameter attributes are enclosed in square brackets.</span></span> <span data-ttu-id="0718e-119">Los atributos de parámetros IDL, como los atributos direccionales, no se permiten en ACF.</span><span class="sxs-lookup"><span data-stu-id="0718e-119">IDL parameter attributes, such as directional attributes, are not allowed in the ACF.</span></span>

</dd> <dt>

<span data-ttu-id="0718e-120">*nombre de parámetro*</span><span class="sxs-lookup"><span data-stu-id="0718e-120">*parameter-name*</span></span> 
</dt> <dd>

<span data-ttu-id="0718e-121">Especifica el parámetro para la función tal y como se define en el archivo IDL.</span><span class="sxs-lookup"><span data-stu-id="0718e-121">Specifies the parameter for the function as defined in the IDL file.</span></span> <span data-ttu-id="0718e-122">Cada parámetro de la función se debe especificar en la misma secuencia, con el mismo nombre que el definido en el archivo IDL.</span><span class="sxs-lookup"><span data-stu-id="0718e-122">Each parameter for the function must be specified in the same sequence, using the same name as defined in the IDL file.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0718e-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0718e-123">Remarks</span></span>

<span data-ttu-id="0718e-124">El tipo de **Estado de error \_ \_ t** se usa como parte de la arquitectura de control de excepciones en IDL.</span><span class="sxs-lookup"><span data-stu-id="0718e-124">The **error\_status\_t** type is used as a part of the exception handling architecture in IDL.</span></span> <span data-ttu-id="0718e-125">Este tipo se asigna a una [**longitud**](long.md) [**sin signo**](unsigned.md) .</span><span class="sxs-lookup"><span data-stu-id="0718e-125">This type maps to an [**unsigned**](unsigned.md) [**long**](long.md).</span></span> <span data-ttu-id="0718e-126">Las aplicaciones que detectan situaciones de error tienen un **\[** [](out-idl.md) **\]** parámetro de salida o un tipo de valor devuelto de un procedimiento especificado como **Estado de error \_ \_ t**, y califican el **Estado de error \_ \_ t** con los **\[** atributos de estado de la [**comunicación \_**](comm-status.md) **\]** o **\[** [**\_ Estado**](fault-status.md) **\]** de error de ACF.</span><span class="sxs-lookup"><span data-stu-id="0718e-126">Applications that catch error situations have an **\[**[**out**](out-idl.md)**\]** parameter or a return type of a procedure specified as **error\_status\_t**, and qualify the **error\_status\_t** with the **\[**[**comm\_status**](comm-status.md)**\]** or **\[**[**fault\_status**](fault-status.md)**\]** attributes in the ACF.</span></span> <span data-ttu-id="0718e-127">Si el parámetro o el tipo de valor devuelto no se calificó con los atributos de estado de **\[ comunicación \_ \]** o **\[ \_ estado \] de error** , el parámetro funciona como si fuera una longitud sin signo.</span><span class="sxs-lookup"><span data-stu-id="0718e-127">If the parameter or return type was not qualified with the **\[comm\_status\]** or **\[fault\_status\]** attributes, then the parameter operates as though it were an unsigned long.</span></span>

<span data-ttu-id="0718e-128">A partir de la versión 2,0, el compilador MIDL genera código auxiliar que contiene la arquitectura de control de errores adecuada.</span><span class="sxs-lookup"><span data-stu-id="0718e-128">Beginning with version 2.0, the MIDL compiler generates stubs that contain the proper error handling architecture.</span></span> <span data-ttu-id="0718e-129">Sin embargo, las versiones anteriores del compilador de MIDL administraban un parámetro o tipo de valor devuelto de **Estado de error \_ \_ t** como si se aplicaran los atributos de estado de **\[** [**comunicación \_**](comm-status.md) **\]** y **\[** [**\_ Estado**](fault-status.md) de error **\]** , aunque no fueran.</span><span class="sxs-lookup"><span data-stu-id="0718e-129">However, earlier versions of the MIDL compiler handled a parameter or return type of **error\_status\_t** as though the **\[**[**comm\_status**](comm-status.md)**\]** and **\[**[**fault\_status**](fault-status.md)**\]** attributes were applied, even if they were not.</span></span> <span data-ttu-id="0718e-130">Con MIDL 2,0 o posterior, debe aplicar explícitamente los atributos de estado de **\[ comunicación \_ \]** y **\[ \_ estado \] de error** al parámetro o al procedimiento de ACF.</span><span class="sxs-lookup"><span data-stu-id="0718e-130">With MIDL 2.0 or later, you must explicitly apply the **\[comm\_status\]** and **\[fault\_status\]** attributes to the parameter or procedure in the ACF.</span></span>

<span data-ttu-id="0718e-131">El tipo de **Estado de error \_ \_ t** es uno de los tipos predefinidos del lenguaje de definición de interfaz.</span><span class="sxs-lookup"><span data-stu-id="0718e-131">The **error\_status\_t** type is one of the predefined types of the interface definition language.</span></span> <span data-ttu-id="0718e-132">Los tipos predefinidos pueden aparecer como especificadores de tipo en las declaraciones [**typedef**](typedef.md) , en las declaraciones generales y en los declaradores de función (como los especificadores de tipo de valor de función o tipo de parámetro).</span><span class="sxs-lookup"><span data-stu-id="0718e-132">Predefined types can appear as type specifiers in [**typedef**](typedef.md) declarations, in general declarations, and in function declarators (either as the function-return-type or as parameter-type specifiers).</span></span>

## <a name="see-also"></a><span data-ttu-id="0718e-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="0718e-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0718e-134">**Estado de COMM \_**</span><span class="sxs-lookup"><span data-stu-id="0718e-134">**comm\_status**</span></span>](comm-status.md)
</dt> <dt>

[<span data-ttu-id="0718e-135">**Estado de error \_**</span><span class="sxs-lookup"><span data-stu-id="0718e-135">**fault\_status**</span></span>](fault-status.md)
</dt> <dt>

[<span data-ttu-id="0718e-136">Archivo de definición de interfaz (IDL)</span><span class="sxs-lookup"><span data-stu-id="0718e-136">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="0718e-137">**tal**</span><span class="sxs-lookup"><span data-stu-id="0718e-137">**long**</span></span>](long.md)
</dt> <dt>

[<span data-ttu-id="0718e-138">**enuncia**</span><span class="sxs-lookup"><span data-stu-id="0718e-138">**out**</span></span>](out-idl.md)
</dt> <dt>

[<span data-ttu-id="0718e-139">**typedef**</span><span class="sxs-lookup"><span data-stu-id="0718e-139">**typedef**</span></span>](typedef.md)
</dt> <dt>

[<span data-ttu-id="0718e-140">**sin signo**</span><span class="sxs-lookup"><span data-stu-id="0718e-140">**unsigned**</span></span>](unsigned.md)
</dt> </dl>

 

 




