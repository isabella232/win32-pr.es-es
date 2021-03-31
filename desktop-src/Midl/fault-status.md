---
title: fault_status atributo)
description: El atributo \ \_ ACF status \ ACF especifica que un código de error de tipo error \_ \_ t indica un error en el procedimiento remoto, en lugar de otros tipos de problemas, como errores de comunicación.
ms.assetid: 9da7bd3d-cef0-4ad4-b2a4-3f8aa156e8e0
keywords:
- fault_status el atributo MIDL
topic_type:
- apiref
api_name:
- fault_status
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 134d9772e167fe63e133d569b9985a7735668d3c
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "103783611"
---
# <a name="fault_status-attribute"></a><span data-ttu-id="58d74-104">atributo de estado de error \_</span><span class="sxs-lookup"><span data-stu-id="58d74-104">fault\_status attribute</span></span>

<span data-ttu-id="58d74-105">El atributo ACF de **\[ \_ estado \]** de error especifica que un código de error de tipo [**error \_ \_ t**](error-status-t.md) indica un error en el procedimiento remoto, en lugar de otros tipos de problemas, como errores de comunicación.</span><span class="sxs-lookup"><span data-stu-id="58d74-105">The **\[fault\_status\]** ACF attribute specifies that an error code of type [**error\_status\_t**](error-status-t.md) indicates a failure of the remote procedure, rather than other types of problems such as communication errors.</span></span>

``` syntax
[fault_status [ , ACF-function-attributes ] ] function-name(
    [ [ ACF-parameter-attributes ] ] parameter-name
    , ... );

[ [ ACF-function-attributes ] ] function-name(
    [fault_status [ , ACF-parameter-attributes ] ] parameter-name
    , ... );
```

## <a name="parameters"></a><span data-ttu-id="58d74-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="58d74-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="58d74-107">*ACF: atributos de función*</span><span class="sxs-lookup"><span data-stu-id="58d74-107">*ACF-function-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="58d74-108">Especifica cero o más atributos de función ACF como el **\[ \_ estado \] de error** y **\[** [**nocode**](nocode.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="58d74-108">Specifies zero or more ACF function attributes such as **\[fault\_status\]** and **\[**[**nocode**](nocode.md)**\]**.</span></span> <span data-ttu-id="58d74-109">Los atributos de función se incluyen entre corchetes.</span><span class="sxs-lookup"><span data-stu-id="58d74-109">Function attributes are enclosed in square brackets.</span></span> <span data-ttu-id="58d74-110">Tenga en cuenta que cero o más atributos se pueden aplicar a una función.</span><span class="sxs-lookup"><span data-stu-id="58d74-110">Note that zero or more attributes can be applied to a function.</span></span> <span data-ttu-id="58d74-111">Separe varios atributos de función con comas.</span><span class="sxs-lookup"><span data-stu-id="58d74-111">Separate multiple function attributes with commas.</span></span> <span data-ttu-id="58d74-112">Tenga en cuenta también que si el **\[ \_ estado \] de error** aparece como un atributo de función, tampoco puede aparecer como atributo de parámetro.</span><span class="sxs-lookup"><span data-stu-id="58d74-112">Also note that if **\[fault\_status\]** appears as a function attribute, it cannot also appear as a parameter attribute.</span></span>

</dd> <dt>

<span data-ttu-id="58d74-113">*nombre-de-la-función*</span><span class="sxs-lookup"><span data-stu-id="58d74-113">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="58d74-114">Especifica el nombre de la función tal y como se define en el archivo IDL.</span><span class="sxs-lookup"><span data-stu-id="58d74-114">Specifies the name of the function as defined in the IDL file.</span></span>

</dd> <dt>

<span data-ttu-id="58d74-115">*ACF-Parameter-Attributes*</span><span class="sxs-lookup"><span data-stu-id="58d74-115">*ACF-parameter-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="58d74-116">Especifica los atributos que se aplican a un parámetro.</span><span class="sxs-lookup"><span data-stu-id="58d74-116">Specifies attributes that apply to a parameter.</span></span> <span data-ttu-id="58d74-117">Tenga en cuenta que se pueden aplicar cero o más atributos al parámetro.</span><span class="sxs-lookup"><span data-stu-id="58d74-117">Note that zero or more attributes can be applied to the parameter.</span></span> <span data-ttu-id="58d74-118">Los atributos de parámetro se incluyen entre corchetes.</span><span class="sxs-lookup"><span data-stu-id="58d74-118">Parameter attributes are enclosed in square brackets.</span></span> <span data-ttu-id="58d74-119">Separe varios atributos de parámetro con comas.</span><span class="sxs-lookup"><span data-stu-id="58d74-119">Separate multiple parameter attributes with commas.</span></span> <span data-ttu-id="58d74-120">Los atributos de parámetros IDL, como los atributos direccionales, no se permiten en ACF.</span><span class="sxs-lookup"><span data-stu-id="58d74-120">IDL parameter attributes, such as directional attributes, are not allowed in the ACF.</span></span> <span data-ttu-id="58d74-121">Tenga en cuenta que si el **\[ \_ estado \] de error** aparece como un atributo de parámetro, tampoco puede aparecer como un atributo de función.</span><span class="sxs-lookup"><span data-stu-id="58d74-121">Note that if **\[fault\_status\]** appears as a parameter attribute, it cannot also appear as a function attribute.</span></span>

</dd> <dt>

<span data-ttu-id="58d74-122">*nombre de parámetro*</span><span class="sxs-lookup"><span data-stu-id="58d74-122">*parameter-name*</span></span> 
</dt> <dd>

<span data-ttu-id="58d74-123">Especifica el parámetro para la función tal y como se define en el archivo IDL.</span><span class="sxs-lookup"><span data-stu-id="58d74-123">Specifies the parameter for the function as defined in the IDL file.</span></span> <span data-ttu-id="58d74-124">Cada parámetro de la función se debe especificar en la misma secuencia, con el mismo nombre que el definido en el archivo IDL.</span><span class="sxs-lookup"><span data-stu-id="58d74-124">Each parameter for the function must be specified in the same sequence, using the same name as defined in the IDL file.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="58d74-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="58d74-125">Remarks</span></span>

<span data-ttu-id="58d74-126">El atributo de **\[ \_ estado \] de error** se puede usar como un atributo de función o como un atributo de parámetro, pero solo puede aparecer una vez por función.</span><span class="sxs-lookup"><span data-stu-id="58d74-126">The **\[fault\_status\]** attribute can be used as either a function attribute or as a parameter attribute, but it can appear only once per function.</span></span> <span data-ttu-id="58d74-127">Se puede aplicar a la propia función o a un parámetro de cada función.</span><span class="sxs-lookup"><span data-stu-id="58d74-127">It can be applied either to the function itself or to one parameter in each function.</span></span>

<span data-ttu-id="58d74-128">El atributo de **\[ \_ estado \]** de error solo se puede aplicar a funciones que devuelven el tipo de [**Estado de error \_ \_ t**](error-status-t.md).</span><span class="sxs-lookup"><span data-stu-id="58d74-128">The **\[fault\_status\]** attribute can be applied only to functions that return the type [**error\_status\_t**](error-status-t.md).</span></span> <span data-ttu-id="58d74-129">Cuando se produce un error en el procedimiento remoto de forma que hace que se devuelva una PDU de error, se devuelve un código de error.</span><span class="sxs-lookup"><span data-stu-id="58d74-129">When the remote procedure fails in a way that causes a fault PDU to be returned, an error code is returned.</span></span>

<span data-ttu-id="58d74-130">Cuando el **\[ \_ estado \] de error** se usa como atributo de parámetro, el parámetro debe ser un **\[** [](out-idl.md) **\]** parámetro de salida de tipo [**error de \_ estado \_ t**](error-status-t.md).</span><span class="sxs-lookup"><span data-stu-id="58d74-130">When **\[fault\_status\]** is used as a parameter attribute, the parameter must be an **\[**[**out**](out-idl.md)**\]** parameter of type [**error\_status\_t**](error-status-t.md).</span></span> <span data-ttu-id="58d74-131">Si se produce un error de servidor, el parámetro se establece en el código de error.</span><span class="sxs-lookup"><span data-stu-id="58d74-131">If a server error occurs, the parameter is set to the error code.</span></span> <span data-ttu-id="58d74-132">Cuando la llamada remota se completa correctamente, el procedimiento establece el valor.</span><span class="sxs-lookup"><span data-stu-id="58d74-132">When the remote call is successfully completed, the procedure sets the value.</span></span>

<span data-ttu-id="58d74-133">No es necesario especificar el parámetro asociado al atributo de **\[ \_ estado \] de error** en el archivo IDL.</span><span class="sxs-lookup"><span data-stu-id="58d74-133">The parameter associated with the **\[fault\_status\]** attribute does not have to be specified in the IDL file.</span></span> <span data-ttu-id="58d74-134">Cuando no se especifica el parámetro, se genera un nuevo parámetro [**out**](out-idl.md) de tipo [**error \_ status \_ t**](error-status-t.md) después del último parámetro definido en el archivo de DCE IDL.</span><span class="sxs-lookup"><span data-stu-id="58d74-134">When the parameter is not specified, a new [**out**](out-idl.md) parameter of type [**error\_status\_t**](error-status-t.md) is generated following the last parameter defined in the DCE IDL file.</span></span>

<span data-ttu-id="58d74-135">Es posible que los atributos **\[ \_ estado \] de error** y **\[** [**\_ Estado de comunicación**](comm-status.md) **\]** aparezcan en una sola función, ya sea como atributos de función o atributos de parámetro.</span><span class="sxs-lookup"><span data-stu-id="58d74-135">It is possible for both the **\[fault\_status\]** and **\[**[**comm\_status**](comm-status.md)**\]** attributes to appear in a single function, either as function attributes or parameter attributes.</span></span> <span data-ttu-id="58d74-136">Si ambos atributos son atributos de función, o si se aplican al mismo parámetro y no se produce ningún error, la función o el parámetro tiene el valor de **Estado de error \_ \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="58d74-136">If both attributes are function attributes, or if they apply to the same parameter and no error occurs, the function or parameter has the value **error\_status\_ok**.</span></span> <span data-ttu-id="58d74-137">De lo contrario, contiene el valor de código de estado adecuado.</span><span class="sxs-lookup"><span data-stu-id="58d74-137">Otherwise, it contains the appropriate status code value.</span></span> <span data-ttu-id="58d74-138">Dado que los valores devueltos para el **\[ \_ estado \] de error** son diferentes de los valores devueltos para el **\[ \_ estado \] de COMM**, los valores devueltos se interpretan fácilmente.</span><span class="sxs-lookup"><span data-stu-id="58d74-138">Because values returned for **\[fault\_status\]** are different from the values returned for **\[comm\_status\]**, the returned values are readily interpreted.</span></span>

## <a name="see-also"></a><span data-ttu-id="58d74-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="58d74-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58d74-140">Archivo de configuración de la aplicación (ACF)</span><span class="sxs-lookup"><span data-stu-id="58d74-140">Application Configuration File (ACF)</span></span>](application-configuration-file-acf-.md)
</dt> <dt>

[<span data-ttu-id="58d74-141">**Estado de COMM \_**</span><span class="sxs-lookup"><span data-stu-id="58d74-141">**comm\_status**</span></span>](comm-status.md)
</dt> <dt>

[<span data-ttu-id="58d74-142">**Estado de error \_ \_ t**</span><span class="sxs-lookup"><span data-stu-id="58d74-142">**error\_status\_t**</span></span>](error-status-t.md)
</dt> <dt>

[<span data-ttu-id="58d74-143">**nocode**</span><span class="sxs-lookup"><span data-stu-id="58d74-143">**nocode**</span></span>](nocode.md)
</dt> <dt>

[<span data-ttu-id="58d74-144">**enuncia**</span><span class="sxs-lookup"><span data-stu-id="58d74-144">**out**</span></span>](out-idl.md)
</dt> </dl>

 

 




