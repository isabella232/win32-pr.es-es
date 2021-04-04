---
title: posible atributo
description: La palabra clave \ maybe \ indica que la llamada a procedimiento remoto no tiene que ejecutarse cada vez que se llama a y el cliente no espera una respuesta. Tenga en cuenta que el protocolo \ tal vez no garantiza la entrega o la finalización de la llamada.
ms.assetid: 163b9fd5-7dce-493e-95bc-63807f42a498
keywords:
- posible atributo MIDL
topic_type:
- apiref
api_name:
- maybe
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 68704e19d421150444933d74f6b78fc5bada46f6
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104076578"
---
# <a name="maybe-attribute"></a><span data-ttu-id="91939-105">posible atributo</span><span class="sxs-lookup"><span data-stu-id="91939-105">maybe attribute</span></span>

<span data-ttu-id="91939-106">La palabra clave **\[ puede \]** indicar que la llamada a procedimiento remoto no tiene que ejecutarse cada vez que se llama a y el cliente no espera una respuesta.</span><span class="sxs-lookup"><span data-stu-id="91939-106">The keyword **\[maybe\]** indicates that the remote procedure call does not need to execute every time it is called and the client does not expect a response.</span></span> <span data-ttu-id="91939-107">Tenga en cuenta que el protocolo **\[ maybe \]** no garantiza la entrega ni la finalización de la llamada.</span><span class="sxs-lookup"><span data-stu-id="91939-107">Note that the **\[maybe\]** protocol ensures neither delivery nor completion of the call.</span></span>

``` syntax
[
    interface-attribute-list
] 
interface interface-name 
{
    [maybe [, attribute-list]] returntype function-name(params)
}
```

## <a name="parameters"></a><span data-ttu-id="91939-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="91939-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="91939-109">*interfaz-atributo-lista*</span><span class="sxs-lookup"><span data-stu-id="91939-109">*interface-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="91939-110">Especifica una lista de cero o más atributos IDL que se aplican a la interfaz en conjunto.</span><span class="sxs-lookup"><span data-stu-id="91939-110">Specifies a list of zero or more IDL attributes that apply to the interface as a whole.</span></span> <span data-ttu-id="91939-111">Cuando dos o más atributos de interfaz están presentes, deben separarse con comas.</span><span class="sxs-lookup"><span data-stu-id="91939-111">When two or more interface attributes are present, they must be separated by commas.</span></span>

</dd> <dt>

<span data-ttu-id="91939-112">*nombre de interfaz*</span><span class="sxs-lookup"><span data-stu-id="91939-112">*interface-name*</span></span> 
</dt> <dd>

<span data-ttu-id="91939-113">Especifica el nombre de la interfaz.</span><span class="sxs-lookup"><span data-stu-id="91939-113">Specifies the name of the interface.</span></span>

</dd> <dt>

<span data-ttu-id="91939-114">*lista de atributos*</span><span class="sxs-lookup"><span data-stu-id="91939-114">*attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="91939-115">Especifica los atributos adicionales que se van a aplicar a la función.</span><span class="sxs-lookup"><span data-stu-id="91939-115">Specifies additional attributes to be applied to the function.</span></span> <span data-ttu-id="91939-116">Separe varios atributos con comas.</span><span class="sxs-lookup"><span data-stu-id="91939-116">Separate multiple attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="91939-117">*ReturnType*</span><span class="sxs-lookup"><span data-stu-id="91939-117">*returntype*</span></span> 
</dt> <dd>

<span data-ttu-id="91939-118">Especifica el tipo de valor devuelto de la función.</span><span class="sxs-lookup"><span data-stu-id="91939-118">Specifies the return type of the function.</span></span>

</dd> <dt>

<span data-ttu-id="91939-119">*nombre-de-la-función*</span><span class="sxs-lookup"><span data-stu-id="91939-119">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="91939-120">Especifica el nombre de la función a la que se aplicará el atributo **\[ maybe \]** .</span><span class="sxs-lookup"><span data-stu-id="91939-120">Specifies the name of the function to which the **\[maybe\]** attribute will be applied.</span></span>

</dd> <dt>

<span data-ttu-id="91939-121">*params*</span><span class="sxs-lookup"><span data-stu-id="91939-121">*params*</span></span> 
</dt> <dd>

<span data-ttu-id="91939-122">Lista de parámetros de función.</span><span class="sxs-lookup"><span data-stu-id="91939-122">Function parameter list.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="91939-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="91939-123">Remarks</span></span>

<span data-ttu-id="91939-124">Una llamada con el atributo **\[ maybe \]** no puede contener parámetros de salida y es implícitamente una **\[** llamada [**idempotente**](idempotent.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="91939-124">A call with the **\[maybe\]** attribute cannot contain output parameters and is implicitly an **\[**[**idempotent**](idempotent.md)**\]** call.</span></span>

## <a name="see-also"></a><span data-ttu-id="91939-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="91939-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91939-126">**amplia**</span><span class="sxs-lookup"><span data-stu-id="91939-126">**broadcast**</span></span>](broadcast.md)
</dt> <dt>

[<span data-ttu-id="91939-127">**idempotent**</span><span class="sxs-lookup"><span data-stu-id="91939-127">**idempotent**</span></span>](idempotent.md)
</dt> <dt>

[<span data-ttu-id="91939-128">Archivo de definición de interfaz (IDL)</span><span class="sxs-lookup"><span data-stu-id="91939-128">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> </dl>

 

 




