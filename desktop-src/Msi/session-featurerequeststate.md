---
description: La propiedad FeatureRequestState es una propiedad de lectura y escritura del objeto de sesión.
ms.assetid: ba19603b-ac81-4a8b-81ca-ad5f28974599
title: Propiedad Session. FeatureRequestState
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.FeatureRequestState
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 1531157ab094d817d34650f8eae2ac6dc23c681c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679522"
---
# <a name="sessionfeaturerequeststate-property"></a><span data-ttu-id="3096e-103">Propiedad Session. FeatureRequestState</span><span class="sxs-lookup"><span data-stu-id="3096e-103">Session.FeatureRequestState property</span></span>

<span data-ttu-id="3096e-104">La propiedad **FeatureRequestState** es una propiedad de lectura y escritura del objeto de [**sesión**](session-object.md) .</span><span class="sxs-lookup"><span data-stu-id="3096e-104">The **FeatureRequestState** property is a read-write property of the [**Session**](session-object.md) object.</span></span> <span data-ttu-id="3096e-105">Se puede usar para obtener el estado de acción actual de una característica o para solicitar un cambio en la acción de una característica y sus subcaracterísticas.</span><span class="sxs-lookup"><span data-stu-id="3096e-105">It can be used to obtain the current action state of a feature or to request a change in the action of a feature and its subfeatures.</span></span> <span data-ttu-id="3096e-106">La característica debe denominarse en la tabla de [características](feature-table.md) .</span><span class="sxs-lookup"><span data-stu-id="3096e-106">The feature must be named in the [Feature](feature-table.md) table.</span></span> <span data-ttu-id="3096e-107">Si se solicita un cambio en el estado de acción de una característica, también se puede cambiar el estado de la acción de todos los componentes de la característica cambiada.</span><span class="sxs-lookup"><span data-stu-id="3096e-107">If a change to the action state of a feature is requested, the action state of all components of the changed feature may be changed as well.</span></span> <span data-ttu-id="3096e-108">El estado de la acción de los componentes compartidos por más de una característica cambiará según corresponda según el nuevo estado de acción de la característica (vea la sección comentarios).</span><span class="sxs-lookup"><span data-stu-id="3096e-108">The action state of components shared by more than one feature will be changed as appropriate based on the new feature action state (see Remarks).</span></span> <span data-ttu-id="3096e-109">La propiedad **FeatureRequestState** también se puede usar para configurar todas las características a la vez mediante la especificación de la palabra clave All en lugar de un nombre de característica específico.</span><span class="sxs-lookup"><span data-stu-id="3096e-109">The **FeatureRequestState** property can also be used to configure all features at once by specifying the keyword ALL instead of a specific feature name.</span></span>

<span data-ttu-id="3096e-110">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="3096e-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="3096e-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3096e-111">Syntax</span></span>


```JScript
propVal = Session.FeatureRequestState
Session.FeatureRequestState = propVal 
```



## <a name="property-value"></a><span data-ttu-id="3096e-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="3096e-112">Property value</span></span>

<span data-ttu-id="3096e-113">Cadena requerida que especifica el nombre de la característica que se va a configurar.</span><span class="sxs-lookup"><span data-stu-id="3096e-113">Required string that specifies the name of the feature to be configured.</span></span> <span data-ttu-id="3096e-114">Para establecer todas las características en un estado de solicitud deseado, use la palabra reservada sin distinción de mayúsculas y minúsculas: todos.</span><span class="sxs-lookup"><span data-stu-id="3096e-114">To set all features to a desired request state, use the reserved case-insensitive word: ALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="3096e-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3096e-115">Remarks</span></span>

<span data-ttu-id="3096e-116">Se debe llamar al método [**SetInstallLevel**](session-setinstalllevel.md) antes de llamar a **FeatureRequestState**.</span><span class="sxs-lookup"><span data-stu-id="3096e-116">The [**SetInstallLevel**](session-setinstalllevel.md) method must be called before calling **FeatureRequestState**.</span></span>

<span data-ttu-id="3096e-117">Si se solicita el estado actual de la característica, la propiedad **FeatureRequestState** devuelve uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="3096e-117">If the current state of the feature is being requested, the **FeatureRequestState** property returns one of the following values.</span></span>



| <span data-ttu-id="3096e-118">Nombre del estado de selección</span><span class="sxs-lookup"><span data-stu-id="3096e-118">Selection state name</span></span>         | <span data-ttu-id="3096e-119">Significado</span><span class="sxs-lookup"><span data-stu-id="3096e-119">Meaning</span></span>                                                               |
|------------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="3096e-120">msiInstallStateUnknown =-1</span><span class="sxs-lookup"><span data-stu-id="3096e-120">msiInstallStateUnknown = -1</span></span>  | <span data-ttu-id="3096e-121">No se realiza ninguna acción para la característica.</span><span class="sxs-lookup"><span data-stu-id="3096e-121">No action is taken for the feature.</span></span> <span data-ttu-id="3096e-122">Es equivalente a NULL.</span><span class="sxs-lookup"><span data-stu-id="3096e-122">This is equivalent to null.</span></span>       |
| <span data-ttu-id="3096e-123">msiInstallStateAdvertised = 1</span><span class="sxs-lookup"><span data-stu-id="3096e-123">msiInstallStateAdvertised =1</span></span> | <span data-ttu-id="3096e-124">La característica se va a anunciar.</span><span class="sxs-lookup"><span data-stu-id="3096e-124">Feature is to be advertised.</span></span>                                          |
| <span data-ttu-id="3096e-125">msiInstallStateAbsent = 2</span><span class="sxs-lookup"><span data-stu-id="3096e-125">msiInstallStateAbsent = 2</span></span>    | <span data-ttu-id="3096e-126">La característica se va a quitar.</span><span class="sxs-lookup"><span data-stu-id="3096e-126">Feature is to be removed.</span></span>                                             |
| <span data-ttu-id="3096e-127">msiInstallStateLocal = 3</span><span class="sxs-lookup"><span data-stu-id="3096e-127">msiInstallStateLocal = 3</span></span>     | <span data-ttu-id="3096e-128">La característica se instalará como de ejecución local.</span><span class="sxs-lookup"><span data-stu-id="3096e-128">Feature is to be installed as run-local.</span></span>                              |
| <span data-ttu-id="3096e-129">msiInstallStateSource = 4</span><span class="sxs-lookup"><span data-stu-id="3096e-129">msiInstallStateSource = 4</span></span>    | <span data-ttu-id="3096e-130">La característica se instalará como ejecutar desde el origen.</span><span class="sxs-lookup"><span data-stu-id="3096e-130">Feature is to be installed as run-from-source.</span></span>                        |
| <span data-ttu-id="3096e-131">msiInstallStateDefault = 5</span><span class="sxs-lookup"><span data-stu-id="3096e-131">msiInstallStateDefault = 5</span></span>   | <span data-ttu-id="3096e-132">La característica se debe volver a instalar con el estado de acción actual de la característica.</span><span class="sxs-lookup"><span data-stu-id="3096e-132">Feature is to be reinstalled with the feature's current action state.</span></span> |



 

<span data-ttu-id="3096e-133">Por ejemplo, lo siguiente obtiene el estado actual de "función" de una acción personalizada de VBScript.</span><span class="sxs-lookup"><span data-stu-id="3096e-133">For example, the following obtains the current state of "MyFeature" from a VBScript custom action.</span></span>


```VB
Dim iRequestState
iRequestState = Session.FeatureRequestState("MyFeature")
```



<span data-ttu-id="3096e-134">Si se está configurando el estado de la característica, la propiedad **FeatureRequestState** debe establecerse en uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="3096e-134">If the state of the feature is being configured, the **FeatureRequestState** property should be set to one of the following values.</span></span>



| <span data-ttu-id="3096e-135">Nombre del estado de selección</span><span class="sxs-lookup"><span data-stu-id="3096e-135">Selection state name</span></span>          | <span data-ttu-id="3096e-136">Significado</span><span class="sxs-lookup"><span data-stu-id="3096e-136">Meaning</span></span>                                 |
|-------------------------------|-----------------------------------------|
| <span data-ttu-id="3096e-137">msiInstallStateAdvertised = 1</span><span class="sxs-lookup"><span data-stu-id="3096e-137">msiInstallStateAdvertised = 1</span></span> | <span data-ttu-id="3096e-138">Anuncie la característica.</span><span class="sxs-lookup"><span data-stu-id="3096e-138">Advertise the feature.</span></span>                  |
| <span data-ttu-id="3096e-139">msiInstallStateAbsent = 2</span><span class="sxs-lookup"><span data-stu-id="3096e-139">msiInstallStateAbsent = 2</span></span>     | <span data-ttu-id="3096e-140">Quite la característica.</span><span class="sxs-lookup"><span data-stu-id="3096e-140">Remove the feature.</span></span>                     |
| <span data-ttu-id="3096e-141">msiInstallStateLocal = 3</span><span class="sxs-lookup"><span data-stu-id="3096e-141">msiInstallStateLocal = 3</span></span>      | <span data-ttu-id="3096e-142">Instale la característica como Run-local.</span><span class="sxs-lookup"><span data-stu-id="3096e-142">Install the feature as run-local.</span></span>       |
| <span data-ttu-id="3096e-143">msiInstallStateSource = 4</span><span class="sxs-lookup"><span data-stu-id="3096e-143">msiInstallStateSource = 4</span></span>     | <span data-ttu-id="3096e-144">Instale la característica como ejecutar desde el origen.</span><span class="sxs-lookup"><span data-stu-id="3096e-144">Install the feature as run-from-source.</span></span> |



 

<span data-ttu-id="3096e-145">Por ejemplo, las siguientes solicitudes de una acción personalizada de VBScript que "mi característica" se instalarán para ejecutarse localmente en el equipo.</span><span class="sxs-lookup"><span data-stu-id="3096e-145">For example, the following requests from a VBScript custom action that "MyFeature" be installed to run locally on the computer.</span></span>


```VB
Session.FeatureRequestState("MyFeature")=3
```



<span data-ttu-id="3096e-146">Cuando se llama a **FeatureRequestState** , el instalador intenta establecer el estado de la acción de cada componente asociado a la característica especificada en el estado especificado, lo mejor posible.</span><span class="sxs-lookup"><span data-stu-id="3096e-146">When **FeatureRequestState** is called, the installer attempts to set the action state of each component tied to the specified feature to the specified state, as best as possible.</span></span> <span data-ttu-id="3096e-147">Sin embargo, hay situaciones comunes en las que la solicitud no se puede respetar por completo.</span><span class="sxs-lookup"><span data-stu-id="3096e-147">However, there are common situations when the request cannot be fully honored.</span></span> <span data-ttu-id="3096e-148">Por ejemplo, si una característica está asociada a dos componentes, el componente A y el componente B, a través de la tabla [FeatureComponents](featurecomponents-table.md) y el componente a tiene el atributo **msidbComponentAttributesLocalOnly** y el componente b tiene el atributo **msidbComponentAttributesSourceOnly** .</span><span class="sxs-lookup"><span data-stu-id="3096e-148">For example, if a feature is tied to two components, Component A and Component B, through the [FeatureComponents](featurecomponents-table.md) table and Component A has the **msidbComponentAttributesLocalOnly** attribute and component B has the **msidbComponentAttributesSourceOnly** attribute.</span></span> <span data-ttu-id="3096e-149">En este caso, si se llama a **FeatureRequestState** con un estado solicitado de MsiInstallStateLocal o msiInstallStateSource, no se puede respetar la solicitud para ambos componentes.</span><span class="sxs-lookup"><span data-stu-id="3096e-149">In this case, if **FeatureRequestState** is called with a requested state of either msiInstallStateLocal or msiInstallStateSource, the request cannot be honored for both components.</span></span> <span data-ttu-id="3096e-150">En este caso, ambos componentes se pueden activar con el componente a establecido en msiInstallStateLocal y el componente B establecido en msiInstallStateSource.</span><span class="sxs-lookup"><span data-stu-id="3096e-150">In this case, both components can be turned on with Component A set to msiInstallStateLocal and Component B set to msiInstallStateSource.</span></span>

<span data-ttu-id="3096e-151">Si hay más de una característica vinculada a un único componente, el estado de acción final de ese componente se determina de la siguiente manera: si al menos una de las características llama a para que el componente se instale localmente, se instala msiInstallStateLocal.</span><span class="sxs-lookup"><span data-stu-id="3096e-151">If more than one feature is linked to a single component, the final action state of that component is determined as follows: If at least one feature calls for the component to be installed locally, it is installed msiInstallStateLocal.</span></span> <span data-ttu-id="3096e-152">Si al menos una de las características llama a para que el componente se ejecute desde el medio de origen, se instala msiInstallStateSource.</span><span class="sxs-lookup"><span data-stu-id="3096e-152">If at least one feature calls for the component to be run from the source media, it is installed msiInstallStateSource.</span></span> <span data-ttu-id="3096e-153">Si al menos una de las características llama a para quitar el componente, el estado de la acción es msiInstallStateAbsent.</span><span class="sxs-lookup"><span data-stu-id="3096e-153">If at least one feature calls for the removal of the component, the action state is msiInstallStateAbsent.</span></span> <span data-ttu-id="3096e-154">Para obtener más información sobre cómo se seleccionan las características para la instalación, vea la tabla de [características](feature-table.md) .</span><span class="sxs-lookup"><span data-stu-id="3096e-154">For more information on how features are selected for installation, see the [Feature](feature-table.md) table.</span></span>

<span data-ttu-id="3096e-155">Si se produce un error en la propiedad, puede obtener información de error extendida mediante el método [**LastErrorRecord**](installer-lasterrorrecord.md) .</span><span class="sxs-lookup"><span data-stu-id="3096e-155">If the property fails, you can obtain extended error information by using the [**LastErrorRecord**](installer-lasterrorrecord.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="3096e-156">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3096e-156">Requirements</span></span>



| <span data-ttu-id="3096e-157">Requisito</span><span class="sxs-lookup"><span data-stu-id="3096e-157">Requirement</span></span> | <span data-ttu-id="3096e-158">Value</span><span class="sxs-lookup"><span data-stu-id="3096e-158">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3096e-159">Versión</span><span class="sxs-lookup"><span data-stu-id="3096e-159">Version</span></span><br/> | <span data-ttu-id="3096e-160">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="3096e-160">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="3096e-161">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="3096e-161">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="3096e-162">Windows Installer en Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="3096e-162">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="3096e-163">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3096e-163">DLL</span></span><br/>     | <dl> <span data-ttu-id="3096e-164"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3096e-164"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="3096e-165">IID</span><span class="sxs-lookup"><span data-stu-id="3096e-165">IID</span></span><br/>     | <span data-ttu-id="3096e-166">El IID \_ ISession se define como 000C109E-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="3096e-166">IID\_ISession is defined as 000C109E-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                             |



## <a name="see-also"></a><span data-ttu-id="3096e-167">Vea también</span><span class="sxs-lookup"><span data-stu-id="3096e-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3096e-168">**De sesión**</span><span class="sxs-lookup"><span data-stu-id="3096e-168">**Session**</span></span>](session-object.md)
</dt> <dt>

[<span data-ttu-id="3096e-169">Característica</span><span class="sxs-lookup"><span data-stu-id="3096e-169">Feature</span></span>](feature-table.md)
</dt> </dl>

 

 




