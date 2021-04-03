---
title: comm_status atributo)
description: El atributo \ COMM \_ status \ ACF hace que se devuelva un código de error cuando se produce un error de comunicación durante la ejecución de una función.
ms.assetid: 3ea9ce62-8bd4-40fe-b838-bfebd52b5a15
keywords:
- comm_status el atributo MIDL
topic_type:
- apiref
api_name:
- comm_status
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd4952d03a80dbbffb135043d024b0c0eb18966f
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "103784313"
---
# <a name="comm_status-attribute"></a><span data-ttu-id="48064-104">atributo de estado de COMM \_</span><span class="sxs-lookup"><span data-stu-id="48064-104">comm\_status attribute</span></span>

<span data-ttu-id="48064-105">El atributo ACF de **\[ \_ estado \] de COMM** hace que se devuelva un código de error cuando se produce un error de comunicación durante la ejecución de una función.</span><span class="sxs-lookup"><span data-stu-id="48064-105">The **\[comm\_status\]** ACF attribute causes an error code to be returned when a communication error occurs during the execution of a function.</span></span>

``` syntax
[comm_status [ , ACF-function-attributes ] ] 
    error_status_t function-name(
        [ [ ACF-parameter-attributes ] ] parameter-name
        , ...);

[ [ ACF-function-attributes ] ] function-name(
    [comm_status [ , ACF-parameter-attributes ] ] error_status_t name
    , ...);
```

## <a name="parameters"></a><span data-ttu-id="48064-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="48064-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="48064-107">*ACF: atributos de función*</span><span class="sxs-lookup"><span data-stu-id="48064-107">*ACF-function-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="48064-108">Especifica cero o más atributos de función ACF, como el **\[ \_ estado \] de COMM** y **\[** [**nocode**](nocode.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="48064-108">Specifies zero or more ACF function attributes, such as **\[comm\_status\]** and **\[**[**nocode**](nocode.md)**\]**.</span></span> <span data-ttu-id="48064-109">Los atributos de función se incluyen entre corchetes.</span><span class="sxs-lookup"><span data-stu-id="48064-109">Function attributes are enclosed in square brackets.</span></span> <span data-ttu-id="48064-110">Cero o más atributos se pueden aplicar a una función.</span><span class="sxs-lookup"><span data-stu-id="48064-110">Zero or more attributes can be applied to a function.</span></span> <span data-ttu-id="48064-111">Separe varios atributos de función con comas.</span><span class="sxs-lookup"><span data-stu-id="48064-111">Separate multiple function attributes with commas.</span></span> <span data-ttu-id="48064-112">Tenga en cuenta que si el **\[ \_ estado \] de COMM** aparece como un atributo de función, tampoco puede aparecer como atributo de parámetro.</span><span class="sxs-lookup"><span data-stu-id="48064-112">Note that if **\[comm\_status\]** appears as a function attribute, it cannot also appear as a parameter attribute.</span></span>

</dd> <dt>

<span data-ttu-id="48064-113">*nombre-de-la-función*</span><span class="sxs-lookup"><span data-stu-id="48064-113">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="48064-114">Especifica el nombre de la función tal y como se define en el archivo IDL.</span><span class="sxs-lookup"><span data-stu-id="48064-114">Specifies the name of the function as defined in the IDL file.</span></span>

</dd> <dt>

<span data-ttu-id="48064-115">*ACF-Parameter-Attributes*</span><span class="sxs-lookup"><span data-stu-id="48064-115">*ACF-parameter-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="48064-116">Especifica los atributos que se aplican a un parámetro.</span><span class="sxs-lookup"><span data-stu-id="48064-116">Specifies attributes that apply to a parameter.</span></span> <span data-ttu-id="48064-117">Tenga en cuenta que se pueden aplicar cero, uno o varios atributos al parámetro.</span><span class="sxs-lookup"><span data-stu-id="48064-117">Note that zero, one, or more attributes can be applied to the parameter.</span></span> <span data-ttu-id="48064-118">Separe varios atributos de parámetro con comas.</span><span class="sxs-lookup"><span data-stu-id="48064-118">Separate multiple parameter attributes with commas.</span></span> <span data-ttu-id="48064-119">Los atributos de parámetro se incluyen entre corchetes.</span><span class="sxs-lookup"><span data-stu-id="48064-119">Parameter attributes are enclosed in square brackets.</span></span> <span data-ttu-id="48064-120">Los atributos de parámetros IDL, como los atributos direccionales, no se permiten en ACF.</span><span class="sxs-lookup"><span data-stu-id="48064-120">IDL parameter attributes, such as directional attributes, are not allowed in the ACF.</span></span> <span data-ttu-id="48064-121">Tenga en cuenta que si el **\[ \_ estado \] de COMM** aparece como un atributo de parámetro, tampoco puede aparecer como un atributo de función.</span><span class="sxs-lookup"><span data-stu-id="48064-121">Note that if **\[comm\_status\]** appears as a parameter attribute, it cannot also appear as a function attribute.</span></span>

</dd> <dt>

<span data-ttu-id="48064-122">*nombre de parámetro*</span><span class="sxs-lookup"><span data-stu-id="48064-122">*parameter-name*</span></span> 
</dt> <dd>

<span data-ttu-id="48064-123">Especifica el parámetro para la función tal y como se define en el archivo IDL.</span><span class="sxs-lookup"><span data-stu-id="48064-123">Specifies the parameter for the function as defined in the IDL file.</span></span> <span data-ttu-id="48064-124">Cada parámetro de la función se debe especificar en la misma secuencia, con el mismo nombre que el definido en el archivo IDL.</span><span class="sxs-lookup"><span data-stu-id="48064-124">Each parameter for the function must be specified in the same sequence, using the same name as defined in the IDL file.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="48064-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="48064-125">Remarks</span></span>

<span data-ttu-id="48064-126">El atributo de **\[ \_ estado \] de COMM** se puede usar como un atributo de función o como un atributo de parámetro, pero solo puede aparecer una vez por función.</span><span class="sxs-lookup"><span data-stu-id="48064-126">The **\[comm\_status\]** attribute can be used as either a function attribute or as a parameter attribute, but it can appear only once per function.</span></span> <span data-ttu-id="48064-127">Se puede aplicar a la función o a un parámetro de cada función.</span><span class="sxs-lookup"><span data-stu-id="48064-127">It can be applied either to the function or to one parameter in each function.</span></span>

<span data-ttu-id="48064-128">El atributo de **\[ \_ estado \] de COMM** solo se puede aplicar a funciones que devuelven el tipo de estado de [**error \_ \_ t**](error-status-t.md).</span><span class="sxs-lookup"><span data-stu-id="48064-128">The **\[comm\_status\]** attribute can be applied only to functions that return the type [**error\_status\_t**](error-status-t.md).</span></span> <span data-ttu-id="48064-129">Cuando se produce un error de comunicación durante la ejecución de la función, se devuelve un código de error.</span><span class="sxs-lookup"><span data-stu-id="48064-129">When a communication error occurs during the execution of the function, an error code is returned.</span></span>

<span data-ttu-id="48064-130">Cuando se usa el **\[ \_ estado \] de COMM** como atributo de parámetro, el parámetro debe definirse en el archivo IDL y debe ser un **\[** parámetro [**out**](out-idl.md) **\]** de tipo [**error \_ \_ t**](error-status-t.md).</span><span class="sxs-lookup"><span data-stu-id="48064-130">When **\[comm\_status\]** is used as a parameter attribute, the parameter must be defined in the IDL file and must be an **\[**[**out**](out-idl.md)**\]** parameter of type [**error\_status\_t**](error-status-t.md).</span></span> <span data-ttu-id="48064-131">Cuando se produce un error de comunicación durante la ejecución de la función, el parámetro se establece en el código de error.</span><span class="sxs-lookup"><span data-stu-id="48064-131">When a communication error occurs during the execution of the function, the parameter is set to the error code.</span></span> <span data-ttu-id="48064-132">Cuando la llamada remota se completa correctamente, el procedimiento establece el valor.</span><span class="sxs-lookup"><span data-stu-id="48064-132">When the remote call is completed successfully, the procedure sets the value.</span></span>

<span data-ttu-id="48064-133">Es posible que los atributos **\[ \_ estado \] de comunicación** y **\[** [**\_ Estado de error**](fault-status.md) **\]** aparezcan en una sola función, ya sea como atributos de función o atributos de parámetro.</span><span class="sxs-lookup"><span data-stu-id="48064-133">It is possible for both the **\[comm\_status\]** and **\[**[**fault\_status**](fault-status.md)**\]** attributes to appear in a single function, either as function attributes or parameter attributes.</span></span> <span data-ttu-id="48064-134">Si ambos atributos son atributos de función o si se aplican al mismo parámetro y no se produce ningún error, la función o el parámetro tiene el valor de **Estado de error \_ \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="48064-134">If both attributes are function attributes or if they apply to the same parameter and no error occurs, the function or parameter has the value **error\_status\_ok**.</span></span> <span data-ttu-id="48064-135">De lo contrario, contiene el valor de estado de **\[ comunicación \_ \]** adecuado o el valor de **\[ \_ estado \] de error** .</span><span class="sxs-lookup"><span data-stu-id="48064-135">Otherwise, it contains the appropriate **\[comm\_status\]** or **\[fault\_status\]** value.</span></span> <span data-ttu-id="48064-136">Dado que los valores devueltos para el **\[ \_ estado \] de COMM** son distintos de los valores devueltos para el **\[ \_ estado \] de error**, los valores devueltos se interpretan fácilmente.</span><span class="sxs-lookup"><span data-stu-id="48064-136">Because values returned for **\[comm\_status\]** are different from the values returned for **\[fault\_status\]**, the returned values are readily interpreted.</span></span>

## <a name="see-also"></a><span data-ttu-id="48064-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="48064-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48064-138">Archivo de configuración de la aplicación (ACF)</span><span class="sxs-lookup"><span data-stu-id="48064-138">Application Configuration File (ACF)</span></span>](application-configuration-file-acf-.md)
</dt> <dt>

[<span data-ttu-id="48064-139">**Estado de error \_ \_ t**</span><span class="sxs-lookup"><span data-stu-id="48064-139">**error\_status\_t**</span></span>](error-status-t.md)
</dt> <dt>

[<span data-ttu-id="48064-140">**Estado de error \_**</span><span class="sxs-lookup"><span data-stu-id="48064-140">**fault\_status**</span></span>](fault-status.md)
</dt> <dt>

[<span data-ttu-id="48064-141">**nocode**</span><span class="sxs-lookup"><span data-stu-id="48064-141">**nocode**</span></span>](nocode.md)
</dt> <dt>

[<span data-ttu-id="48064-142">**enuncia**</span><span class="sxs-lookup"><span data-stu-id="48064-142">**out**</span></span>](out-idl.md)
</dt> </dl>

 

 




