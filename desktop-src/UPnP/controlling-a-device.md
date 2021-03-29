---
title: Controlar un dispositivo
description: Una vez que haya detectado dispositivos, puede controlarlos.
ms.assetid: 6d0efb80-d6f5-4b36-a184-19f06afeb2a7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ff91339c67b67de5d3e90eda0ce64ebcc68b9e2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903794"
---
# <a name="controlling-a-device"></a><span data-ttu-id="20836-103">Controlar un dispositivo</span><span class="sxs-lookup"><span data-stu-id="20836-103">Controlling a Device</span></span>

<span data-ttu-id="20836-104">Una vez que haya detectado dispositivos, puede controlarlos.</span><span class="sxs-lookup"><span data-stu-id="20836-104">Once you have discovered devices, you can control them.</span></span>

<span data-ttu-id="20836-105">**Para ver las propiedades del dispositivo**</span><span class="sxs-lookup"><span data-stu-id="20836-105">**To view device properties**</span></span>

1.  <span data-ttu-id="20836-106">Seleccione un dispositivo en la lista **dispositivos encontrados** .</span><span class="sxs-lookup"><span data-stu-id="20836-106">Select a device from the **Devices Found** list.</span></span>
2.  <span data-ttu-id="20836-107">Haga clic en **propiedades del dispositivo**.</span><span class="sxs-lookup"><span data-stu-id="20836-107">Click **Device Properties**.</span></span> <span data-ttu-id="20836-108">La ventana **propiedades del dispositivo** aparece con la información solicitada.</span><span class="sxs-lookup"><span data-stu-id="20836-108">The **Device Properties** window appears with the requested information.</span></span>

> [!Note]  
> <span data-ttu-id="20836-109">La funcionalidad de presentación de la **vista** no está disponible en el código de ejemplo de C++.</span><span class="sxs-lookup"><span data-stu-id="20836-109">The **View Presentation** functionality is not available in the C++ sample code.</span></span>

 

<span data-ttu-id="20836-110">**Para ver la página de presentación de un dispositivo**</span><span class="sxs-lookup"><span data-stu-id="20836-110">**To view a device's presentation page**</span></span>

1.  <span data-ttu-id="20836-111">Seleccione un dispositivo en la lista **dispositivos encontrados** .</span><span class="sxs-lookup"><span data-stu-id="20836-111">Select a device from the **Devices Found** list.</span></span>
2.  <span data-ttu-id="20836-112">Haga clic en **ver presentación**.</span><span class="sxs-lookup"><span data-stu-id="20836-112">Click **View Presentation**.</span></span> <span data-ttu-id="20836-113">Aparece una ventana de Internet Explorer con la página de presentación solicitada.</span><span class="sxs-lookup"><span data-stu-id="20836-113">An Internet Explorer window appears with the requested presentation page.</span></span>

> [!Note]  
> <span data-ttu-id="20836-114">La funcionalidad de **ver Descripción de servicio** no está disponible en el código de ejemplo de C++.</span><span class="sxs-lookup"><span data-stu-id="20836-114">The **View Service Desc.** functionality is not available in the C++ sample code.</span></span>

 

<span data-ttu-id="20836-115">**Para ver una descripción del servicio**</span><span class="sxs-lookup"><span data-stu-id="20836-115">**To view a service description**</span></span>

1.  <span data-ttu-id="20836-116">Puede escribir la dirección URL de la descripción del servicio en la descripción del **servicio. Campo de dirección URL** .</span><span class="sxs-lookup"><span data-stu-id="20836-116">You can enter the URL to the service description in the **Service Desc. URL** field.</span></span>

    ![URL de descripción de servicio](images/ucp-url.png)

2.  <span data-ttu-id="20836-118">Haga clic en **ver Descripción del servicio.** Se muestra la ventana **visor de descripción de servicio** .</span><span class="sxs-lookup"><span data-stu-id="20836-118">Click **View Service Desc.** The **Service Description Viewer** window is displayed.</span></span> <span data-ttu-id="20836-119">A continuación, puede examinar la descripción del servicio mediante la vista de árbol.</span><span class="sxs-lookup"><span data-stu-id="20836-119">You can then browse the service description using the tree view.</span></span> <span data-ttu-id="20836-120">Esta funcionalidad no está disponible en el código de ejemplo de C++.</span><span class="sxs-lookup"><span data-stu-id="20836-120">This functionality is not available in the C++ sample code.</span></span>

    ![ventana del visor de descripción de servicio](images/ucp-serv.png)

    <span data-ttu-id="20836-122">Hay cinco comandos que puede usar en la ventana del visor de descripción de servicio.</span><span class="sxs-lookup"><span data-stu-id="20836-122">There are five commands you can use in the Service Description Viewer window.</span></span>



| <span data-ttu-id="20836-123">Botón</span><span class="sxs-lookup"><span data-stu-id="20836-123">Button</span></span>                 | <span data-ttu-id="20836-124">Acción realizada</span><span class="sxs-lookup"><span data-stu-id="20836-124">Action Performed</span></span>                                                                                                                                                                      |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="20836-125">Go</span><span class="sxs-lookup"><span data-stu-id="20836-125">Go</span></span>                     | <span data-ttu-id="20836-126">Carga el archivo que se muestra en la **Descripción del servicio. Campo de dirección URL** .</span><span class="sxs-lookup"><span data-stu-id="20836-126">Loads the file shown in the **Service Desc. URL** field.</span></span>                                                                                                                              |
| <span data-ttu-id="20836-127">Establecer acción</span><span class="sxs-lookup"><span data-stu-id="20836-127">Set Action</span></span>             | <span data-ttu-id="20836-128">Seleccione un nombre de acción en el árbol de Descripción del servicio y haga clic en **establecer acción**.</span><span class="sxs-lookup"><span data-stu-id="20836-128">Select an action name in the service description tree and click **Set Action**.</span></span> <span data-ttu-id="20836-129">El nombre de la acción se escribe en el campo **invocar acción** de la ventana principal del **UCP** .</span><span class="sxs-lookup"><span data-stu-id="20836-129">The action name is entered into the **Invoke Action** field of the main **Generic UCP** window.</span></span>       |
| <span data-ttu-id="20836-130">Establecer variable</span><span class="sxs-lookup"><span data-stu-id="20836-130">Set Variable</span></span>           | <span data-ttu-id="20836-131">Seleccione un nombre de variable en el árbol de Descripción del servicio y haga clic en **establecer variable**.</span><span class="sxs-lookup"><span data-stu-id="20836-131">Select a variable name in the service description tree and click **Set Variable**.</span></span> <span data-ttu-id="20836-132">El nombre de la variable se escribe en el campo **variable de consulta** de la ventana principal del **UCP** .</span><span class="sxs-lookup"><span data-stu-id="20836-132">The variable name is entered into the **Query Variable** field of the main **Generic UCP** window.</span></span> |
| <span data-ttu-id="20836-133">Rellenar lista de variables</span><span class="sxs-lookup"><span data-stu-id="20836-133">Populate Variable List</span></span> | <span data-ttu-id="20836-134">Carga todos los nombres de variable del servicio en la lista de **variables de consulta** de la ventana principal del **UCP** .</span><span class="sxs-lookup"><span data-stu-id="20836-134">Loads all the service's variable names into the **Query Variable** list of the main **Generic UCP** window.</span></span>                                                                           |
| <span data-ttu-id="20836-135">Rellenar lista de acciones</span><span class="sxs-lookup"><span data-stu-id="20836-135">Populate Action List</span></span>   | <span data-ttu-id="20836-136">Carga todos los nombres de acción del servicio en la lista de **acciones de invocación** de la ventana principal del **UCP** .</span><span class="sxs-lookup"><span data-stu-id="20836-136">Loads all the service's action names into the **Invoke Action** list of the main **Generic UCP** window.</span></span>                                                                              |



 

<span data-ttu-id="20836-137">**Para controlar un dispositivo**</span><span class="sxs-lookup"><span data-stu-id="20836-137">**To control a device**</span></span>

1.  <span data-ttu-id="20836-138">En la lista **dispositivos encontrados** , seleccione el dispositivo que desea controlar.</span><span class="sxs-lookup"><span data-stu-id="20836-138">From the **Devices Found** list, select the device you want to control.</span></span>
2.  <span data-ttu-id="20836-139">En la lista **elegir servicio** , seleccione el servicio que desea invocar o la variable de estado que desea consultar.</span><span class="sxs-lookup"><span data-stu-id="20836-139">From the **Choose Service** list, select the service you want to invoke or state variable you want to query.</span></span>

    ![ventana controlar dispositivos](images/ucp-contr.png)

    > [!Note]  
    > <span data-ttu-id="20836-141">El contenido de la **lista de servicios** se basa en el dispositivo seleccionado en la lista **dispositivos encontrados** .</span><span class="sxs-lookup"><span data-stu-id="20836-141">The contents of the **Service List** is based on the device selected in the **Devices Found** list.</span></span>

     

3.  <span data-ttu-id="20836-142">Si desea averiguar el valor de una variable de estado para el servicio seleccionado, escriba el nombre de la variable en el campo **variable de consulta** para servicio.</span><span class="sxs-lookup"><span data-stu-id="20836-142">If you want to find out the value of a state variable for the selected service, enter the variable name in the **Query Variable** field for service.</span></span> <span data-ttu-id="20836-143">Haga clic en **Consulta**.</span><span class="sxs-lookup"><span data-stu-id="20836-143">Click **Query**.</span></span> <span data-ttu-id="20836-144">Los resultados se muestran en el campo **valor de estado de consulta/argumentos de acción de salida** .</span><span class="sxs-lookup"><span data-stu-id="20836-144">The results are shown in the **Query State Value/Action Out Arguments** field.</span></span>
4.  <span data-ttu-id="20836-145">Si desea invocar una acción para un servicio, escriba el nombre de la acción en el campo **invocar acción** y los argumentos en el campo argumentos de la **acción** .</span><span class="sxs-lookup"><span data-stu-id="20836-145">If you want to invoke an action for a service, enter the action name in the **Invoke Action** field, and any arguments in the **Action Arguments** field.</span></span> <span data-ttu-id="20836-146">Haga clic en **invocar**.</span><span class="sxs-lookup"><span data-stu-id="20836-146">Click **Invoke**.</span></span> <span data-ttu-id="20836-147">Los resultados se muestran en el campo **valor de estado de consulta/argumentos de acción out** , si los hay.</span><span class="sxs-lookup"><span data-stu-id="20836-147">The results are shown in the **Query State Value/Action Out Arguments** field, if any.</span></span>

    <span data-ttu-id="20836-148">El valor devuelto, si existe, está incluido en el primer argumento out.</span><span class="sxs-lookup"><span data-stu-id="20836-148">The return value, if any, is contained in the first out argument.</span></span>

    > [!Note]  
    > <span data-ttu-id="20836-149">Si hay varios argumentos para una acción, sepárelos con espacios.</span><span class="sxs-lookup"><span data-stu-id="20836-149">If there are multiple arguments for an action, separate them with spaces.</span></span>

     

5.  <span data-ttu-id="20836-150">Ver información de eventos en el campo **eventos** del servicio seleccionado.</span><span class="sxs-lookup"><span data-stu-id="20836-150">View eventing information in the **Events** field for the selected service.</span></span>

 

 




