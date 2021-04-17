---
title: Elemento ServiceTask3
description: Tenga en cuenta que en esta sección se describe la funcionalidad diseñada para su uso en tiendas en línea. No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea. El elemento ServiceTask3 representa el tercer panel de tareas de la tienda en línea.
ms.assetid: 3d08f9ff-d75b-4967-90f8-23ab71d38883
keywords:
- Elemento ServiceTask3 Media Player Windows
topic_type:
- apiref
api_name:
- ServiceTask3 Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d78b9e70c7e6933693f4d29750e9e3c0b4e897a7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105650171"
---
# <a name="servicetask3-element"></a><span data-ttu-id="6a384-106">Elemento ServiceTask3</span><span class="sxs-lookup"><span data-stu-id="6a384-106">ServiceTask3 Element</span></span>

> [!Note]  
> <span data-ttu-id="6a384-107">En esta sección se describe la funcionalidad diseñada para su uso en tiendas en línea.</span><span class="sxs-lookup"><span data-stu-id="6a384-107">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="6a384-108">No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea.</span><span class="sxs-lookup"><span data-stu-id="6a384-108">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="6a384-109">El elemento **ServiceTask3** representa el tercer panel de tareas de la tienda en línea.</span><span class="sxs-lookup"><span data-stu-id="6a384-109">The **ServiceTask3** element represents the third online store task pane.</span></span>

``` syntax
<ServiceTask3
    URL = "URL"
/>
```

## <a name="attributes"></a><span data-ttu-id="6a384-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="6a384-110">Attributes</span></span>



| <span data-ttu-id="6a384-111">Término</span><span class="sxs-lookup"><span data-stu-id="6a384-111">Term</span></span>                                                                                                                             | <span data-ttu-id="6a384-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="6a384-112">Description</span></span>                                                        |
|----------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="6a384-113"><span id="URL__required_"></span><span id="url__required_"></span><span id="URL__REQUIRED_"></span>**URL** (obligatorio)</span><span class="sxs-lookup"><span data-stu-id="6a384-113"><span id="URL__required_"></span><span id="url__required_"></span><span id="URL__REQUIRED_"></span>**URL** (required)</span></span><br/> | <span data-ttu-id="6a384-114">Dirección URL de la página web que Windows Media Player muestra.</span><span class="sxs-lookup"><span data-stu-id="6a384-114">URL for the webpage that Windows Media Player displays.</span></span><br/> |



 

## <a name="parentchild-elements"></a><span data-ttu-id="6a384-115">Elementos primarios y secundarios</span><span class="sxs-lookup"><span data-stu-id="6a384-115">Parent/Child Elements</span></span>



| <span data-ttu-id="6a384-116">Hierarchy</span><span class="sxs-lookup"><span data-stu-id="6a384-116">Hierarchy</span></span>       | <span data-ttu-id="6a384-117">Elemento</span><span class="sxs-lookup"><span data-stu-id="6a384-117">Element</span></span>                       |
|-----------------|-------------------------------|
| <span data-ttu-id="6a384-118">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="6a384-118">Parent elements</span></span> | <span data-ttu-id="6a384-119">**ServiceInfo**</span><span class="sxs-lookup"><span data-stu-id="6a384-119">**ServiceInfo**</span></span>               |
| <span data-ttu-id="6a384-120">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="6a384-120">Child elements</span></span>  | <span data-ttu-id="6a384-121">**ButtonText**, **ButtonTip**</span><span class="sxs-lookup"><span data-stu-id="6a384-121">**ButtonText**, **ButtonTip**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="6a384-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6a384-122">Remarks</span></span>

<span data-ttu-id="6a384-123">**ServiceTask1** se considera el panel de tareas principal para participar en la actividad comercial.</span><span class="sxs-lookup"><span data-stu-id="6a384-123">**ServiceTask1** is considered the primary task pane for engaging in commercial activity.</span></span> <span data-ttu-id="6a384-124">Es el panel de tareas que se muestra cuando el usuario elige comprar música.</span><span class="sxs-lookup"><span data-stu-id="6a384-124">It is the task pane that displays when the user chooses to purchase music.</span></span> <span data-ttu-id="6a384-125">Use **ServiceTask3** para otra actividad de la tienda en línea.</span><span class="sxs-lookup"><span data-stu-id="6a384-125">Use **ServiceTask3** for other online store activity.</span></span>

> [!Note]  
> <span data-ttu-id="6a384-126">Windows Media Player 10 tiene tres paneles de tareas en los que una tienda en línea puede mostrar sus páginas Web.</span><span class="sxs-lookup"><span data-stu-id="6a384-126">Windows Media Player 10 has three task panes where an online store can display its webpages.</span></span> <span data-ttu-id="6a384-127">La tienda en línea puede elegir usar uno, dos o los tres paneles de tareas.</span><span class="sxs-lookup"><span data-stu-id="6a384-127">The online store can choose to use one, two, or all three of the task panes.</span></span> <span data-ttu-id="6a384-128">Windows Media Player 11 solo tiene un panel de tareas, que el usuario puede ver haciendo clic en la pestaña **tiendas en línea** . Windows Media Player 11 omite los elementos **ServiceTask2** y **ServiceTask3** .</span><span class="sxs-lookup"><span data-stu-id="6a384-128">Windows Media Player 11 has only one task pane, which the user can view by clicking on the **Online Stores** tab. Windows Media Player 11 ignores the **ServiceTask2** and **ServiceTask3** elements.</span></span>

 

<span data-ttu-id="6a384-129">Los paneles de tareas de tiendas en línea comparten una única instancia del explorador.</span><span class="sxs-lookup"><span data-stu-id="6a384-129">Online stores task panes share a single browser instance.</span></span> <span data-ttu-id="6a384-130">Esto significa que no debe escribir código de script en la página web que espera que continúe ejecutándose cuando el usuario cambia de la tarea de servicio actual.</span><span class="sxs-lookup"><span data-stu-id="6a384-130">This means that you should not write script code in your webpage that you expect to continue to run when the user switches away from the current service task.</span></span>

<span data-ttu-id="6a384-131">Cuando el usuario cambia los paneles de tareas, Windows Media Player almacena las cookies de la dirección URL y la sesión.</span><span class="sxs-lookup"><span data-stu-id="6a384-131">When the user switches task panes, Windows Media Player stores the URL and session cookies.</span></span> <span data-ttu-id="6a384-132">Cuando el usuario vuelve al panel de tareas, el reproductor restaura la dirección URL y las cookies.</span><span class="sxs-lookup"><span data-stu-id="6a384-132">When the user switches back to the task pane, the Player restores the URL and cookies.</span></span> <span data-ttu-id="6a384-133">Si el usuario elige usar una tienda en línea diferente, se borran los datos de la dirección URL y la sesión.</span><span class="sxs-lookup"><span data-stu-id="6a384-133">If the user chooses to use a different online store, the URL and session data are cleared.</span></span>

<span data-ttu-id="6a384-134">En la tabla siguiente se detallan los parámetros que se envían con la solicitud URL.</span><span class="sxs-lookup"><span data-stu-id="6a384-134">The following table details the parameters sent with the URL request.</span></span>



| <span data-ttu-id="6a384-135">Nombre</span><span class="sxs-lookup"><span data-stu-id="6a384-135">Name</span></span>         | <span data-ttu-id="6a384-136">Value</span><span class="sxs-lookup"><span data-stu-id="6a384-136">Value</span></span>                                                                                                                                                               |
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6a384-137">*Geoid*</span><span class="sxs-lookup"><span data-stu-id="6a384-137">*geoid*</span></span>      | <span data-ttu-id="6a384-138">IDENTIFICADOR de ubicación geográfica de Windows.</span><span class="sxs-lookup"><span data-stu-id="6a384-138">Windows geographical location ID.</span></span> <span data-ttu-id="6a384-139">El ID. de ubicación lo especifica el usuario en el área **Ubicación** de la configuración de configuración regional y de idioma del panel de control.</span><span class="sxs-lookup"><span data-stu-id="6a384-139">The location ID is specified by the user in the **Location** area of the Regional and Language Options settings in Control Panel.</span></span> |
| <span data-ttu-id="6a384-140">*locale*</span><span class="sxs-lookup"><span data-stu-id="6a384-140">*locale*</span></span>     | <span data-ttu-id="6a384-141">IDENTIFICADOR de configuración regional de Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="6a384-141">Windows Media Player locale ID.</span></span>                                                                                                                                     |
| <span data-ttu-id="6a384-142">*UserLocale*</span><span class="sxs-lookup"><span data-stu-id="6a384-142">*userlocale*</span></span> | <span data-ttu-id="6a384-143">IDENTIFICADOR de configuración regional de Windows.</span><span class="sxs-lookup"><span data-stu-id="6a384-143">Windows locale ID.</span></span> <span data-ttu-id="6a384-144">El usuario especifica la configuración regional en el área **estándares y formatos** de la configuración configuración regional y de idioma del panel de control.</span><span class="sxs-lookup"><span data-stu-id="6a384-144">The locale is specified by the user in the **Standards and Formats** area of the Regional and Language Options settings in Control Panel.</span></span>        |
| <span data-ttu-id="6a384-145">*version*</span><span class="sxs-lookup"><span data-stu-id="6a384-145">*version*</span></span>    | <span data-ttu-id="6a384-146">Windows Media Player número de versión con el formato siguiente: 10.0. x. xxxx o 11.0. x. xxxx.</span><span class="sxs-lookup"><span data-stu-id="6a384-146">Windows Media Player version number using the following format: 10.0.x.xxxx or 11.0.x.xxxx.</span></span>                                                                         |



 

## <a name="requirements"></a><span data-ttu-id="6a384-147">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6a384-147">Requirements</span></span>



| <span data-ttu-id="6a384-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="6a384-148">Requirement</span></span> | <span data-ttu-id="6a384-149">Value</span><span class="sxs-lookup"><span data-stu-id="6a384-149">Value</span></span> |
|--------------------|----------------------------------------------|
| <span data-ttu-id="6a384-150">Versión</span><span class="sxs-lookup"><span data-stu-id="6a384-150">Version</span></span><br/> | <span data-ttu-id="6a384-151">Windows Media Player 10 o posterior.</span><span class="sxs-lookup"><span data-stu-id="6a384-151">Windows Media Player 10 or later.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6a384-152">Vea también</span><span class="sxs-lookup"><span data-stu-id="6a384-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a384-153">**Ejemplo de documento ServiceInfo para una tienda en línea de tipo 1**</span><span class="sxs-lookup"><span data-stu-id="6a384-153">**Example ServiceInfo Document for a Type 1 Online Store**</span></span>](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[<span data-ttu-id="6a384-154">**Ejemplo de documento ServiceInfo para una tienda en línea de tipo 2**</span><span class="sxs-lookup"><span data-stu-id="6a384-154">**Example ServiceInfo Document for a Type 2 Online Store**</span></span>](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[<span data-ttu-id="6a384-155">**Documento ServiceInfo**</span><span class="sxs-lookup"><span data-stu-id="6a384-155">**ServiceInfo Document**</span></span>](serviceinfo-document.md)
</dt> </dl>

 

 





