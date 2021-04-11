---
title: Crear un proyecto de ejemplo
description: Crear un proyecto de ejemplo
ms.assetid: 9cbbd1a7-88e7-4947-8dca-e06e364102f7
keywords:
- Windows Media Player tiendas en línea, crear proyectos de ejemplo
- tiendas en línea, crear proyectos de ejemplo
- tipo 2 tiendas en línea, crear proyectos de ejemplo
- Windows Media Player tiendas en línea, proyectos de ejemplo
- tiendas en línea, proyectos de ejemplo
- tipo 2 tiendas en línea, proyectos de ejemplo
- Windows Media Player tiendas en línea, Asistente para proyectos
- tiendas en línea, Asistente para proyectos
- tipo 2 tiendas en línea, Asistente para proyectos
- complementos, Asistente para proyectos
- Complementos de Windows Media Player, Asistente para proyectos
- crear proyectos de ejemplo
- ejemplos, tipo 2 tiendas en línea
- Asistente para proyectos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4756cc7ae8d27c2a790a7ac96af638eea72d861
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/21/2020
ms.locfileid: "104149116"
---
# <a name="creating-a-sample-project"></a><span data-ttu-id="51ac4-117">Crear un proyecto de ejemplo</span><span class="sxs-lookup"><span data-stu-id="51ac4-117">Creating a Sample Project</span></span>

<span data-ttu-id="51ac4-118">Para crear un nuevo proyecto mediante el Asistente para proyectos, siga estos pasos:</span><span class="sxs-lookup"><span data-stu-id="51ac4-118">To create a new project using the project wizard, follow these steps:</span></span>

1.  <span data-ttu-id="51ac4-119">Abra Microsoft Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="51ac4-119">Open Microsoft Visual Studio.</span></span>
2.  <span data-ttu-id="51ac4-120">Desde el menú **Archivo**, pulse **Nuevo** y, después, haga clic en **Proyecto**.</span><span class="sxs-lookup"><span data-stu-id="51ac4-120">From the **File** menu, point to **New**, and then click **Project**.</span></span>
3.  <span data-ttu-id="51ac4-121">En el cuadro de lista **tipos de proyecto** , elija **proyectos de Visual C++**.</span><span class="sxs-lookup"><span data-stu-id="51ac4-121">In the **Project Types** list box, choose **Visual C++ Projects**.</span></span>
4.  <span data-ttu-id="51ac4-122">En el cuadro de lista **plantillas** , elija **Windows Media Player Asistente para tiendas en línea**.</span><span class="sxs-lookup"><span data-stu-id="51ac4-122">In the **Templates** list box, choose **Windows Media Player Online Stores Wizard**.</span></span>
5.  <span data-ttu-id="51ac4-123">Escriba un nombre y una ubicación para el proyecto.</span><span class="sxs-lookup"><span data-stu-id="51ac4-123">Type a name and location for your project.</span></span>
6.  <span data-ttu-id="51ac4-124">Haga clic en **Aceptar** para iniciar el Asistente para proyectos.</span><span class="sxs-lookup"><span data-stu-id="51ac4-124">Click **OK** to start the project wizard.</span></span>
7.  <span data-ttu-id="51ac4-125">Seleccione **tipo 2 (integración básica)** y haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="51ac4-125">Select **Type 2 (Basic integration)**, and click **Next**.</span></span>
8.  <span data-ttu-id="51ac4-126">Escriba el nombre descriptivo y el ID. de distribuidor de contenido para el servicio.</span><span class="sxs-lookup"><span data-stu-id="51ac4-126">Type the friendly name and content distributor ID for your service.</span></span> <span data-ttu-id="51ac4-127">Escriba la dirección URL de la página web que quita el servicio del equipo del usuario.</span><span class="sxs-lookup"><span data-stu-id="51ac4-127">Type the URL for the webpage that removes the service from the user's computer.</span></span>
    > [!Note]  
    > <span data-ttu-id="51ac4-128">El valor que se proporciona para el identificador del distribuidor de contenido no debe contener espacios.</span><span class="sxs-lookup"><span data-stu-id="51ac4-128">The value you provide for the content distributor ID must not contain spaces.</span></span> <span data-ttu-id="51ac4-129">El asistente quita los espacios de la cadena proporcionada.</span><span class="sxs-lookup"><span data-stu-id="51ac4-129">The wizard removes any spaces from the string you provide.</span></span>

     

9.  <span data-ttu-id="51ac4-130">Haga clic en **Finish** (Finalizar) para crear el proyecto.</span><span class="sxs-lookup"><span data-stu-id="51ac4-130">Click **Finish** to create the project.</span></span>

<span data-ttu-id="51ac4-131">El asistente genera automáticamente un nuevo proyecto de C++ que crea un complemento de la tienda en línea de tipo 2 que implementa las interfaces **IWMPSubscriptionService** y **IWMPSubscriptionService2** .</span><span class="sxs-lookup"><span data-stu-id="51ac4-131">The wizard automatically generates a new C++ project that creates a type 2 online store plug-in that implements the **IWMPSubscriptionService** and **IWMPSubscriptionService2** interfaces.</span></span> <span data-ttu-id="51ac4-132">Cada vez que se ejecuta el asistente, se crea el mismo proyecto, pero el componente que se crea al compilar el proyecto tiene un identificador de clase único.</span><span class="sxs-lookup"><span data-stu-id="51ac4-132">Each time you run the wizard it creates the same project, but the component that is created when you compile the project has a unique class ID.</span></span> <span data-ttu-id="51ac4-133">El nombre del proyecto, el nombre descriptivo y el identificador del distribuidor de contenido también pueden ser diferentes en función de los valores proporcionados al ejecutar el asistente.</span><span class="sxs-lookup"><span data-stu-id="51ac4-133">The project name, the friendly name, and content distributor ID may also be different depending on the values you provided when you ran the wizard.</span></span> <span data-ttu-id="51ac4-134">El proyecto de ejemplo registra el componente mediante el uso de un nombre de clave que coincida con el valor proporcionado para el nombre descriptivo.</span><span class="sxs-lookup"><span data-stu-id="51ac4-134">The sample project registers the component by using a key name that matches the value you supplied for the friendly name.</span></span>

<span data-ttu-id="51ac4-135">En el ejemplo se utiliza el código de Active Template Library (ATL) para proporcionar implementaciones COM.</span><span class="sxs-lookup"><span data-stu-id="51ac4-135">The sample uses Active Template Library (ATL) code to provide COM implementations.</span></span>

<span data-ttu-id="51ac4-136">El asistente crea los siguientes archivos:</span><span class="sxs-lookup"><span data-stu-id="51ac4-136">The wizard creates the following files for you:</span></span>

-   <span data-ttu-id="51ac4-137">*Projectname* dll. cpp.</span><span class="sxs-lookup"><span data-stu-id="51ac4-137">*ProjectName* dll.cpp.</span></span> <span data-ttu-id="51ac4-138">Implementa las exportaciones de la biblioteca de vínculos dinámicos (DLL), como la función de punto de entrada DLL principal.</span><span class="sxs-lookup"><span data-stu-id="51ac4-138">Implements the Dynamic Link Library (DLL) exports such as the main DLL entry point function.</span></span> <span data-ttu-id="51ac4-139">También contiene la declaración de módulo y el mapa de objetos ATL.</span><span class="sxs-lookup"><span data-stu-id="51ac4-139">Also contains the ATL object map and module declaration.</span></span>
-   <span data-ttu-id="51ac4-140">*Projectname*. cpp.</span><span class="sxs-lookup"><span data-stu-id="51ac4-140">*ProjectName*.cpp.</span></span> <span data-ttu-id="51ac4-141">Contiene implementaciones predeterminadas para los métodos de las interfaces IWMPSubscriptionService y IWMPSubscriptionService2.</span><span class="sxs-lookup"><span data-stu-id="51ac4-141">Contains default implementations for the methods of the IWMPSubscriptionService and IWMPSubscriptionService2 interfaces.</span></span> <span data-ttu-id="51ac4-142">También contiene código para definir los cuadros de diálogo que se abre en el ejemplo cuando Windows Media Player llama a los métodos.</span><span class="sxs-lookup"><span data-stu-id="51ac4-142">Also contains code to define the dialog boxes that the sample opens when methods are called by Windows Media Player.</span></span>
-   <span data-ttu-id="51ac4-143">*Projectname*. def. Declara las exportaciones de DLL.</span><span class="sxs-lookup"><span data-stu-id="51ac4-143">*ProjectName*.def. Declares the DLL exports.</span></span>
-   <span data-ttu-id="51ac4-144">StdAfx. cpp.</span><span class="sxs-lookup"><span data-stu-id="51ac4-144">StdAfx.cpp.</span></span> <span data-ttu-id="51ac4-145">Incluye encabezados estándar.</span><span class="sxs-lookup"><span data-stu-id="51ac4-145">Includes standard headers.</span></span>
-   <span data-ttu-id="51ac4-146">WMP. h.</span><span class="sxs-lookup"><span data-stu-id="51ac4-146">wmp.h.</span></span> <span data-ttu-id="51ac4-147">El archivo de encabezado de Media Player de Windows.</span><span class="sxs-lookup"><span data-stu-id="51ac4-147">The Windows Media Player header file.</span></span>
-   <span data-ttu-id="51ac4-148">wmpplug. h.</span><span class="sxs-lookup"><span data-stu-id="51ac4-148">wmpplug.h.</span></span> <span data-ttu-id="51ac4-149">El archivo de encabezado del complemento de Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="51ac4-149">The Windows Media Player plug-in header file.</span></span>
-   <span data-ttu-id="51ac4-150">subscriptionservices. h.</span><span class="sxs-lookup"><span data-stu-id="51ac4-150">subscriptionservices.h.</span></span> <span data-ttu-id="51ac4-151">El archivo de encabezado de Windows Media Player online Stores.</span><span class="sxs-lookup"><span data-stu-id="51ac4-151">The Windows Media Player online stores header file.</span></span>
-   <span data-ttu-id="51ac4-152">Resource. h.</span><span class="sxs-lookup"><span data-stu-id="51ac4-152">resource.h.</span></span> <span data-ttu-id="51ac4-153">Contiene definiciones de recursos.</span><span class="sxs-lookup"><span data-stu-id="51ac4-153">Contains resource definitions.</span></span>
-   <span data-ttu-id="51ac4-154">**Projectname**. h.</span><span class="sxs-lookup"><span data-stu-id="51ac4-154">**ProjectName**.h.</span></span> <span data-ttu-id="51ac4-155">Contiene definiciones de clase para el objeto de tienda en línea y los cuadros de diálogo.</span><span class="sxs-lookup"><span data-stu-id="51ac4-155">Contains class definitions for the online store object and the dialog boxes.</span></span> <span data-ttu-id="51ac4-156">Define el identificador de clase del objeto y la constante de identificador del distribuidor de contenido.</span><span class="sxs-lookup"><span data-stu-id="51ac4-156">Defines the object's class ID and the content distributor ID constant.</span></span>
-   <span data-ttu-id="51ac4-157">StdAfx. h.</span><span class="sxs-lookup"><span data-stu-id="51ac4-157">StdAfx.h.</span></span> <span data-ttu-id="51ac4-158">Contiene inclusiones del sistema estándar.</span><span class="sxs-lookup"><span data-stu-id="51ac4-158">Contains standard system includes.</span></span>
-   <span data-ttu-id="51ac4-159">*NombreDeProyecto*. rc.</span><span class="sxs-lookup"><span data-stu-id="51ac4-159">*ProjectName*.rc.</span></span> <span data-ttu-id="51ac4-160">Archivo de script de recursos.</span><span class="sxs-lookup"><span data-stu-id="51ac4-160">The resource script file.</span></span> <span data-ttu-id="51ac4-161">Contiene definiciones de los recursos y controles del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="51ac4-161">This contains definitions for the dialog box resources and controls.</span></span> <span data-ttu-id="51ac4-162">Aquí también es donde se almacena la tabla de cadenas.</span><span class="sxs-lookup"><span data-stu-id="51ac4-162">This is also where the string table is stored.</span></span> <span data-ttu-id="51ac4-163">La tabla de cadenas contiene las constantes de cadena de nombre de proyecto y nombre descriptivo.</span><span class="sxs-lookup"><span data-stu-id="51ac4-163">The string table contains your project name and friendly name string constants.</span></span> <span data-ttu-id="51ac4-164">Normalmente se trabaja con este archivo en el editor de recursos de Visual Studio, no como texto sin formato.</span><span class="sxs-lookup"><span data-stu-id="51ac4-164">Usually you work with this file in the Visual Studio resource editor, not as plain text.</span></span>
-   <span data-ttu-id="51ac4-165">*Projectname*. RGS.</span><span class="sxs-lookup"><span data-stu-id="51ac4-165">*ProjectName*.rgs.</span></span> <span data-ttu-id="51ac4-166">Archivo de script del registro.</span><span class="sxs-lookup"><span data-stu-id="51ac4-166">The registry script file.</span></span> <span data-ttu-id="51ac4-167">Este archivo contiene la información que se usa para agregar la clase de componente al registro para que Windows Media Player pueda encontrarla.</span><span class="sxs-lookup"><span data-stu-id="51ac4-167">This file contains the information used to add your component class to the registry so Windows Media Player can locate it.</span></span> <span data-ttu-id="51ac4-168">Puede cambiar el nombre de la clave del servicio en este archivo.</span><span class="sxs-lookup"><span data-stu-id="51ac4-168">You can change the key name for your service in this file.</span></span>

> [!Note]  
> <span data-ttu-id="51ac4-169">Debe establecer la dirección base del archivo DLL en 0x0F100000 para evitar conflictos con Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="51ac4-169">You should set the base address for your DLL to 0x0F100000 to avoid conflicts with Windows Media Player.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="51ac4-170">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="51ac4-170">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="51ac4-171">**Compilar el complemento para una tienda en línea de tipo 2**</span><span class="sxs-lookup"><span data-stu-id="51ac4-171">**Building the Plug-in for a Type 2 Online Store**</span></span>](building-the-plug-in-for-a-type-2-online-store.md)
</dt> <dt>

[<span data-ttu-id="51ac4-172">**Interfaz IWMPSubscriptionService**</span><span class="sxs-lookup"><span data-stu-id="51ac4-172">**IWMPSubscriptionService Interface**</span></span>](/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservice)
</dt> <dt>

[<span data-ttu-id="51ac4-173">**Interfaz IWMPSubscriptionService2**</span><span class="sxs-lookup"><span data-stu-id="51ac4-173">**IWMPSubscriptionService2 Interface**</span></span>](/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservice2)
</dt> </dl>

 

 




