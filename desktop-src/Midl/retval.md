---
title: retval (atributo)
description: El atributo/retval \ designa el parámetro que recibe el valor devuelto del miembro.
ms.assetid: 3a5f1469-7828-4c38-b58f-195a47b2a66f
keywords:
- atributo de retval MIDL
topic_type:
- apiref
api_name:
- retval
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04b53aa2b8ab66737bd4d97710fe942ee73bf0b8
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103904523"
---
# <a name="retval-attribute"></a><span data-ttu-id="a157c-104">retval (atributo)</span><span class="sxs-lookup"><span data-stu-id="a157c-104">retval attribute</span></span>

<span data-ttu-id="a157c-105">El atributo **\[ retval \]** designa el parámetro que recibe el valor devuelto del miembro.</span><span class="sxs-lookup"><span data-stu-id="a157c-105">The **\[retval\]** attribute designates the parameter that receives the return value of the member.</span></span>

``` syntax
return-type function-name(
    [out, retval [, optional-attributes]] data-type * param-name,
    ...);
```

## <a name="parameters"></a><span data-ttu-id="a157c-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a157c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a157c-107">*tipo de valor devuelto*</span><span class="sxs-lookup"><span data-stu-id="a157c-107">*return-type*</span></span> 
</dt> <dd>

<span data-ttu-id="a157c-108">El tipo de datos del valor devuelto del procedimiento remoto.</span><span class="sxs-lookup"><span data-stu-id="a157c-108">The data type of the return value of the remote procedure.</span></span>

</dd> <dt>

<span data-ttu-id="a157c-109">*nombre-de-la-función*</span><span class="sxs-lookup"><span data-stu-id="a157c-109">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="a157c-110">Nombre que se usa para invocar el procedimiento remoto.</span><span class="sxs-lookup"><span data-stu-id="a157c-110">The name used to invoke the remote procedure.</span></span>

</dd> <dt>

<span data-ttu-id="a157c-111">*opcional: atributos*</span><span class="sxs-lookup"><span data-stu-id="a157c-111">*optional-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="a157c-112">Cero o más atributos de MIDL.</span><span class="sxs-lookup"><span data-stu-id="a157c-112">Zero or more MIDL attributes.</span></span>

</dd> <dt>

<span data-ttu-id="a157c-113">*tipo de datos*</span><span class="sxs-lookup"><span data-stu-id="a157c-113">*data-type*</span></span> 
</dt> <dd>

<span data-ttu-id="a157c-114">Tipo de los datos que se pasan a través del parámetro.</span><span class="sxs-lookup"><span data-stu-id="a157c-114">The type of the data passed through the parameter.</span></span>

</dd> <dt>

<span data-ttu-id="a157c-115">*param: nombre*</span><span class="sxs-lookup"><span data-stu-id="a157c-115">*param-name*</span></span> 
</dt> <dd>

<span data-ttu-id="a157c-116">Nombre del identificador del parámetro.</span><span class="sxs-lookup"><span data-stu-id="a157c-116">The identifier name of the parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a157c-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a157c-117">Remarks</span></span>

<span data-ttu-id="a157c-118">Puede usar el atributo **\[ retval \]** en los parámetros de los miembros de interfaz que describen métodos u obtienen propiedades.</span><span class="sxs-lookup"><span data-stu-id="a157c-118">You can use the **\[retval\]** attribute on parameters of interface members that describe methods or get properties.</span></span> <span data-ttu-id="a157c-119">(El atributo es obligatorio en el último parámetro de un método que tenga **\[** [**propget**](propget.md) **\]** atributo). El parámetro debe tener el **\[** atributo [**out**](out-idl.md) **\]** y debe ser un tipo de puntero.</span><span class="sxs-lookup"><span data-stu-id="a157c-119">(The attribute is required on the last parameter of a method that has the **\[**[**propget**](propget.md)**\]** attribute.) The parameter must have the **\[**[**out**](out-idl.md)**\]** attribute and must be a pointer type.</span></span>

<span data-ttu-id="a157c-120">No se puede aplicar el **\[** atributo [**opcional**](optional.md) **\]** a un parámetro **\[ \] retval** .</span><span class="sxs-lookup"><span data-stu-id="a157c-120">You cannot apply the **\[**[**optional**](optional.md)**\]** attribute to a **\[retval\]** parameter.</span></span>

<span data-ttu-id="a157c-121">El compilador MIDL acepta el siguiente orden de parámetros (de izquierda a derecha):</span><span class="sxs-lookup"><span data-stu-id="a157c-121">The MIDL compiler accepts the following parameter ordering (from left-to-right):</span></span>

1.  <span data-ttu-id="a157c-122">Parámetros obligatorios (parámetros que no tienen los **\[** atributos [**DefaultValue**](defaultvalue.md) **\]** u **\[** [**opcional**](optional.md) **\]** ).</span><span class="sxs-lookup"><span data-stu-id="a157c-122">Required parameters (parameters that do not have the **\[**[**defaultvalue**](defaultvalue.md)**\]** or **\[**[**optional**](optional.md)**\]** attributes).</span></span>
2.  <span data-ttu-id="a157c-123">Parámetros opcionales con o sin el **\[** atributo [**DefaultValue**](defaultvalue.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="a157c-123">Optional parameters with or without the **\[**[**defaultvalue**](defaultvalue.md)**\]** attribute.</span></span>
3.  <span data-ttu-id="a157c-124">Parámetros con el **\[** atributo [**opcional**](optional.md) **\]** y sin el **\[** atributo [**DefaultValue**](defaultvalue.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="a157c-124">Parameters with the **\[**[**optional**](optional.md)**\]** attribute and without the **\[**[**defaultvalue**](defaultvalue.md)**\]** attribute.</span></span>
4.  <span data-ttu-id="a157c-125">**\[** parámetro [**LCID**](lcid.md) **\]** , si existe.</span><span class="sxs-lookup"><span data-stu-id="a157c-125">**\[**[**lcid**](lcid.md)**\]** parameter, if any.</span></span>
5.  <span data-ttu-id="a157c-126">parámetro **\[ retval \]** .</span><span class="sxs-lookup"><span data-stu-id="a157c-126">**\[retval\]** parameter.</span></span>

<span data-ttu-id="a157c-127">Los parámetros con el atributo **\[ retval \]** no se muestran en exploradores orientados al usuario.</span><span class="sxs-lookup"><span data-stu-id="a157c-127">Parameters with the **\[retval\]** attribute are not displayed in user-oriented browsers.</span></span>

### <a name="flags"></a><span data-ttu-id="a157c-128">Marcas</span><span class="sxs-lookup"><span data-stu-id="a157c-128">Flags</span></span>

<span data-ttu-id="a157c-129">IDLFLAG \_ FRETVAL</span><span class="sxs-lookup"><span data-stu-id="a157c-129">IDLFLAG\_FRETVAL</span></span>

## <a name="examples"></a><span data-ttu-id="a157c-130">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="a157c-130">Examples</span></span>

``` syntax
HRESULT MyMethod([out, retval] InMyFace** ReturnVal);
HRESULT MyOtherMethod([out, retval] VARIANT_BOOL* ReturnVal);
```

## <a name="see-also"></a><span data-ttu-id="a157c-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="a157c-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a157c-132">**DefaultValue**</span><span class="sxs-lookup"><span data-stu-id="a157c-132">**defaultvalue**</span></span>](defaultvalue.md)
</dt> <dt>

[<span data-ttu-id="a157c-133">Generar una biblioteca de tipos con MIDL</span><span class="sxs-lookup"><span data-stu-id="a157c-133">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="a157c-134">**LCID**</span><span class="sxs-lookup"><span data-stu-id="a157c-134">**lcid**</span></span>](lcid.md)
</dt> <dt>

[<span data-ttu-id="a157c-135">Ejemplo de archivo ODL</span><span class="sxs-lookup"><span data-stu-id="a157c-135">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="a157c-136">Sintaxis del archivo ODL</span><span class="sxs-lookup"><span data-stu-id="a157c-136">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="a157c-137">**opta**</span><span class="sxs-lookup"><span data-stu-id="a157c-137">**optional**</span></span>](optional.md)
</dt> <dt>

[<span data-ttu-id="a157c-138">**enuncia**</span><span class="sxs-lookup"><span data-stu-id="a157c-138">**out**</span></span>](out-idl.md)
</dt> <dt>

[<span data-ttu-id="a157c-139">**propget**</span><span class="sxs-lookup"><span data-stu-id="a157c-139">**propget**</span></span>](propget.md)
</dt> <dt>

[<span data-ttu-id="a157c-140">**TYPEFLAGS**</span><span class="sxs-lookup"><span data-stu-id="a157c-140">**TYPEFLAGS**</span></span>](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> </dl>

 

 