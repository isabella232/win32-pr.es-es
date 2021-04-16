---
title: vararg (atributo)
description: El atributo \ vararg \ especifica que la función toma un número variable de parámetros. Para ello, el último parámetro debe ser una matriz segura de tipo VARIANT que contenga todos los parámetros restantes.
ms.assetid: df0995d3-5266-4a13-90aa-d78bfa753e0e
keywords:
- atributo vararg MIDL
topic_type:
- apiref
api_name:
- vararg
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c3880a3713daaff13fe827beb989dd377440af4
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "105651364"
---
# <a name="vararg-attribute"></a><span data-ttu-id="23214-105">vararg (atributo)</span><span class="sxs-lookup"><span data-stu-id="23214-105">vararg attribute</span></span>

<span data-ttu-id="23214-106">El atributo **\[ vararg \]** especifica que la función toma un número variable de parámetros.</span><span class="sxs-lookup"><span data-stu-id="23214-106">The **\[vararg\]** attribute specifies that the function takes a variable number of parameters.</span></span> <span data-ttu-id="23214-107">Para ello, el último parámetro debe ser una matriz segura de tipo **Variant** que contenga todos los parámetros restantes.</span><span class="sxs-lookup"><span data-stu-id="23214-107">To accomplish this, the last parameter must be a safe array of **VARIANT** type that contains all the remaining parameters.</span></span>

``` syntax
[vararg [, optional-attributes]] return-type function-name(
  [optional-param-attributes] param-list, 
  SAFEARRAY(VARIANT) last-param-name);
```

## <a name="parameters"></a><span data-ttu-id="23214-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="23214-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="23214-109">*opcional: atributos*</span><span class="sxs-lookup"><span data-stu-id="23214-109">*optional-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="23214-110">Especifica cero o más atributos que se van a aplicar a la función.</span><span class="sxs-lookup"><span data-stu-id="23214-110">Specifies zero or more attributes to be applied to the function.</span></span> <span data-ttu-id="23214-111">Separe varios atributos con comas.</span><span class="sxs-lookup"><span data-stu-id="23214-111">Separate multiple attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="23214-112">*tipo de valor devuelto*</span><span class="sxs-lookup"><span data-stu-id="23214-112">*return-type*</span></span> 
</dt> <dd>

<span data-ttu-id="23214-113">El tipo de los datos devueltos por el procedimiento remoto al finalizar.</span><span class="sxs-lookup"><span data-stu-id="23214-113">The type of the data returned by the remote procedure upon completion.</span></span>

</dd> <dt>

<span data-ttu-id="23214-114">*nombre-de-la-función*</span><span class="sxs-lookup"><span data-stu-id="23214-114">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="23214-115">Nombre del procedimiento remoto.</span><span class="sxs-lookup"><span data-stu-id="23214-115">The name of the remote procedure.</span></span>

</dd> <dt>

<span data-ttu-id="23214-116">*Optional-param-Attributes*</span><span class="sxs-lookup"><span data-stu-id="23214-116">*optional-param-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="23214-117">Especifica cero o más atributos que se van a aplicar al parámetro de función inmediatamente después de la lista de atributos.</span><span class="sxs-lookup"><span data-stu-id="23214-117">Specifies zero or more attributes to be applied to the function parameter immediately following the attribute listing.</span></span>

</dd> <dt>

<span data-ttu-id="23214-118">*lista de parámetros*</span><span class="sxs-lookup"><span data-stu-id="23214-118">*param-list*</span></span> 
</dt> <dd>

<span data-ttu-id="23214-119">Especifica todos los parámetros, guarda el parámetro final, varying.</span><span class="sxs-lookup"><span data-stu-id="23214-119">Specifies all the parameters, save the final, varying, parameter.</span></span>

</dd> <dt>

<span data-ttu-id="23214-120">*nombre del último parámetro*</span><span class="sxs-lookup"><span data-stu-id="23214-120">*last-param-name*</span></span> 
</dt> <dd>

<span data-ttu-id="23214-121">Nombre del parámetro varying.</span><span class="sxs-lookup"><span data-stu-id="23214-121">The name of the varying parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="23214-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="23214-122">Remarks</span></span>

<span data-ttu-id="23214-123">No se pueden aplicar los **\[** [](optional.md) **\]** atributos opcionales o **\[** [**DefaultValue**](defaultvalue.md) **\]** a los parámetros de una función que tenga el atributo **\[ vararg \]** .</span><span class="sxs-lookup"><span data-stu-id="23214-123">You cannot apply the **\[**[**optional**](optional.md)**\]** or **\[**[**defaultvalue**](defaultvalue.md)**\]** attributes to any parameters in a function that has the **\[vararg\]** attribute.</span></span>

## <a name="examples"></a><span data-ttu-id="23214-124">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="23214-124">Examples</span></span>

``` syntax
[vararg] VARIANT_BOOL Button([in]SAFEARRAY(VARIANT) psa);
```

## <a name="see-also"></a><span data-ttu-id="23214-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="23214-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23214-126">**DefaultValue**</span><span class="sxs-lookup"><span data-stu-id="23214-126">**defaultvalue**</span></span>](defaultvalue.md)
</dt> <dt>

[<span data-ttu-id="23214-127">Generar una biblioteca de tipos con MIDL</span><span class="sxs-lookup"><span data-stu-id="23214-127">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="23214-128">Ejemplo de archivo ODL</span><span class="sxs-lookup"><span data-stu-id="23214-128">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="23214-129">Sintaxis del archivo ODL</span><span class="sxs-lookup"><span data-stu-id="23214-129">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="23214-130">**opta**</span><span class="sxs-lookup"><span data-stu-id="23214-130">**optional**</span></span>](optional.md)
</dt> </dl>

 

 