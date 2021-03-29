---
description: El Windows SDK incluye ejemplos de código y herramientas útiles para ayudarle a entender y usar el sensor de Windows y la plataforma de ubicación y las API relacionadas.
ms.assetid: e31174f6-1c2b-4d97-b6b6-e54825ff47f5
title: Acerca de los ejemplos y las herramientas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6126ec5e07829cfd17c2b07313bb104140c6fee6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912237"
---
# <a name="about-the-samples-and-tools"></a><span data-ttu-id="8bd85-103">Acerca de los ejemplos y las herramientas</span><span class="sxs-lookup"><span data-stu-id="8bd85-103">About the Samples and Tools</span></span>

<span data-ttu-id="8bd85-104">El Windows SDK incluye ejemplos de código y herramientas útiles para ayudarle a entender y usar el sensor de Windows y la plataforma de ubicación y las API relacionadas.</span><span class="sxs-lookup"><span data-stu-id="8bd85-104">The Windows SDK includes useful code samples and tools to help you understand and use the Windows Sensor and Location platform and related APIs.</span></span>

## <a name="samples"></a><span data-ttu-id="8bd85-105">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="8bd85-105">Samples</span></span>

<span data-ttu-id="8bd85-106">El Windows SDK incluye los siguientes ejemplos de API de sensor.</span><span class="sxs-lookup"><span data-stu-id="8bd85-106">The Windows SDK includes the following Sensor API samples.</span></span> <span data-ttu-id="8bd85-107">Puede encontrar los ejemplos de API de sensor en la carpeta denominada \\ Samples \\ WinUI \\ Sensors, donde ha instalado el Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="8bd85-107">You can find the Sensor API samples in the folder named \\Samples\\winui\\Sensors, where you installed the Windows SDK.</span></span> <span data-ttu-id="8bd85-108">Por ejemplo, si instaló el Windows SDK en la unidad C, encontraría los ejemplos en la siguiente carpeta: C: archivos de \\ programa \\ Microsoft SDK \\ Windows \\ v 7.0 \\ Samples \\ WinUI \\ Sensors.</span><span class="sxs-lookup"><span data-stu-id="8bd85-108">For example, if you installed the Windows SDK on drive C, you would find the samples in the following folder: C:\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples\\winui\\Sensors.</span></span>



| <span data-ttu-id="8bd85-109">Nombre del ejemplo</span><span class="sxs-lookup"><span data-stu-id="8bd85-109">Sample name</span></span>       | <span data-ttu-id="8bd85-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="8bd85-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8bd85-111">AmbientLightAware</span><span class="sxs-lookup"><span data-stu-id="8bd85-111">AmbientLightAware</span></span> | <span data-ttu-id="8bd85-112">En este ejemplo de MFC se muestra cómo usar la API de sensor mediante la lectura de datos de sensores de luz ambiente en el equipo y el cambio de tamaño de texto en función de las condiciones de iluminación.</span><span class="sxs-lookup"><span data-stu-id="8bd85-112">This MFC sample shows how to use the Sensor API by reading data from ambient light sensors on the computer and changing text size according to the lighting conditions.</span></span> <span data-ttu-id="8bd85-113">Puede ver el código que muestra cómo administrar eventos y cómo solicitar permisos de usuario.</span><span class="sxs-lookup"><span data-stu-id="8bd85-113">You can see code that shows how to manage events and how to request user permissions.</span></span> <span data-ttu-id="8bd85-114">También puede ver un ejemplo de cómo administrar la interfaz de usuario en función de las condiciones de iluminación variables.</span><span class="sxs-lookup"><span data-stu-id="8bd85-114">You can also see an example of how to manage the user interface based on varying lighting conditions.</span></span> <span data-ttu-id="8bd85-115">Para obtener más información, consulte [creación de Light-Aware interfaces de usuario](creating-light-aware-user-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="8bd85-115">For more information, see [Creating Light-Aware User Interfaces](creating-light-aware-user-interfaces.md).</span></span><br/> <span data-ttu-id="8bd85-116">Debe tener instalado Visual Studio 2008 para compilar este ejemplo.</span><span class="sxs-lookup"><span data-stu-id="8bd85-116">You must have Visual Studio 2008 installed to build this sample.</span></span><br/> |



 

<span data-ttu-id="8bd85-117">Para obtener más información, vea el archivo denominado ReadMe.txt que se incluye con el ejemplo.</span><span class="sxs-lookup"><span data-stu-id="8bd85-117">For more information, see the file named ReadMe.txt that is included with the sample.</span></span>

<span data-ttu-id="8bd85-118">También puede descargar el ejemplo AmbientLightAware de la galería de código.</span><span class="sxs-lookup"><span data-stu-id="8bd85-118">You can also download the AmbientLightAware sample from Code Gallery.</span></span> <span data-ttu-id="8bd85-119">Para obtener más información, consulte la página de descarga compatible con la [luz ambiente](/samples/browse/?redirectedfrom=MSDN-samples) .</span><span class="sxs-lookup"><span data-stu-id="8bd85-119">For more information, see the [Ambient Light Aware](/samples/browse/?redirectedfrom=MSDN-samples) download page.</span></span>

## <a name="tools"></a><span data-ttu-id="8bd85-120">Herramientas</span><span class="sxs-lookup"><span data-stu-id="8bd85-120">Tools</span></span>

<span data-ttu-id="8bd85-121">El Windows SDK incluye un sensor de luz virtual que puede usar para simular un dispositivo de sensor de luz basado en hardware.</span><span class="sxs-lookup"><span data-stu-id="8bd85-121">The Windows SDK includes a virtual light sensor that you can use to simulate a hardware-based light sensor device.</span></span> <span data-ttu-id="8bd85-122">Puede usar esta herramienta para proporcionar datos al ejemplo AmbientLightAware para ver cómo funciona el código del ejemplo.</span><span class="sxs-lookup"><span data-stu-id="8bd85-122">You can use this tool to provide data to the AmbientLightAware sample to see how the code in the sample works.</span></span>

<span data-ttu-id="8bd85-123">En la tabla siguiente se describen los archivos que se deben usar para ejecutar el sensor de luz virtual.</span><span class="sxs-lookup"><span data-stu-id="8bd85-123">The following table describes the files you must use to run the virtual light sensor.</span></span> <span data-ttu-id="8bd85-124">Puede encontrar estos archivos en la carpeta denominada bin, donde ha instalado el Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="8bd85-124">You can find these files in the folder named Bin, where you installed the Windows SDK.</span></span> <span data-ttu-id="8bd85-125">Por ejemplo, si instaló el Windows SDK en la unidad C en un equipo de 32 bits, encontraría los archivos del sensor de luz virtual en la carpeta siguiente: C: \\ archivos de programa \\ Microsoft SDK \\ Windows \\ v 7.0 \\ bin.</span><span class="sxs-lookup"><span data-stu-id="8bd85-125">For example, if you installed the Windows SDK on drive C on a 32-bit computer, you would find the virtual light sensor files in the following folder: C:\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Bin.</span></span> <span data-ttu-id="8bd85-126">En equipos de 64 bits, debe usar la versión de 64 bits de la herramienta.</span><span class="sxs-lookup"><span data-stu-id="8bd85-126">On 64-bit computers, you must use the 64-bit version of the tool.</span></span> <span data-ttu-id="8bd85-127">En el Windows SDK, las herramientas de 64 bits se encuentran en la subcarpeta denominada x64.</span><span class="sxs-lookup"><span data-stu-id="8bd85-127">In the Windows SDK, 64-bit tools are located in the subfolder named x64.</span></span>



| <span data-ttu-id="8bd85-128">Nombre de archivo</span><span class="sxs-lookup"><span data-stu-id="8bd85-128">File name</span></span>                    | <span data-ttu-id="8bd85-129">Descripción</span><span class="sxs-lookup"><span data-stu-id="8bd85-129">Description</span></span>                                                                                                                    |
|------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8bd85-130">VirtualLightSensor.exe</span><span class="sxs-lookup"><span data-stu-id="8bd85-130">VirtualLightSensor.exe</span></span>       | <span data-ttu-id="8bd85-131">Este programa proporciona un control deslizante que le permite cambiar el nivel de los datos claros que el sensor virtual informa.</span><span class="sxs-lookup"><span data-stu-id="8bd85-131">This program provides a slider control that enables you to change the level of the light data that the virtual sensor reports.</span></span> |
| <span data-ttu-id="8bd85-132">VirtualLightSensorDriver.dll</span><span class="sxs-lookup"><span data-stu-id="8bd85-132">VirtualLightSensorDriver.dll</span></span> | <span data-ttu-id="8bd85-133">Controlador de sensor lógico que simula un sensor ligero.</span><span class="sxs-lookup"><span data-stu-id="8bd85-133">The logical sensor driver that simulates a light sensor.</span></span>                                                                       |
| <span data-ttu-id="8bd85-134">VirtualLightSensorDriver. inf</span><span class="sxs-lookup"><span data-stu-id="8bd85-134">VirtualLightSensorDriver.inf</span></span> | <span data-ttu-id="8bd85-135">El archivo INF para el controlador del sensor de luz virtual.</span><span class="sxs-lookup"><span data-stu-id="8bd85-135">The INF file for the virtual light sensor driver.</span></span>                                                                              |



 

### <a name="installing-the-virtual-light-sensor"></a><span data-ttu-id="8bd85-136">Instalación del sensor de luz virtual</span><span class="sxs-lookup"><span data-stu-id="8bd85-136">Installing the Virtual Light Sensor</span></span>

<span data-ttu-id="8bd85-137">Antes de usar la aplicación de sensor de luz virtual, debe instalar el controlador de sensor lógico.</span><span class="sxs-lookup"><span data-stu-id="8bd85-137">Before you use the virtual light sensor application, you must install the logical sensor driver.</span></span> <span data-ttu-id="8bd85-138">Siga estos pasos:</span><span class="sxs-lookup"><span data-stu-id="8bd85-138">Follow these steps:</span></span>

1.  <span data-ttu-id="8bd85-139">Abra una ventana de comandos como administrador.</span><span class="sxs-lookup"><span data-stu-id="8bd85-139">Open a command window as an administrator.</span></span>
2.  <span data-ttu-id="8bd85-140">Cambie a la carpeta Windows SDK bin.</span><span class="sxs-lookup"><span data-stu-id="8bd85-140">Change to the Windows SDK Bin folder.</span></span>
3.  <span data-ttu-id="8bd85-141">Escriba **pnputil-a VirtualLightSensorDriver. inf**.</span><span class="sxs-lookup"><span data-stu-id="8bd85-141">Type **pnputil -a VirtualLightSensorDriver.inf**.</span></span>
4.  <span data-ttu-id="8bd85-142">Cuando se le solicite, haga clic en **instalar este software de controlador de todos modos**.</span><span class="sxs-lookup"><span data-stu-id="8bd85-142">When prompted, click **Install this driver software anyway**.</span></span>
5.  <span data-ttu-id="8bd85-143">Espere a que la ventana de comandos informe de que el controlador se ha instalado correctamente.</span><span class="sxs-lookup"><span data-stu-id="8bd85-143">Wait for the command window to report that the driver was successfully installed.</span></span>

### <a name="running-the-virtual-light-sensor"></a><span data-ttu-id="8bd85-144">Ejecutar el sensor de luz virtual</span><span class="sxs-lookup"><span data-stu-id="8bd85-144">Running the Virtual Light Sensor</span></span>

<span data-ttu-id="8bd85-145">Para ejecutar el sensor de luz virtual, simplemente haga doble clic en el archivo. exe.</span><span class="sxs-lookup"><span data-stu-id="8bd85-145">To run the virtual light sensor, simply double-click the .exe file.</span></span> <span data-ttu-id="8bd85-146">Cuando se le solicite, asegúrese de habilitar el sensor.</span><span class="sxs-lookup"><span data-stu-id="8bd85-146">Be sure to enable the sensor, when prompted.</span></span>

<span data-ttu-id="8bd85-147">Al ejecutar el programa, es posible que observe que hay un retraso antes de que el sensor esté disponible.</span><span class="sxs-lookup"><span data-stu-id="8bd85-147">When you run the program, you may notice that there is a delay before the sensor becomes available.</span></span> <span data-ttu-id="8bd85-148">La interfaz de usuario del sensor virtual de luz mostrará el mensaje "en espera" en la barra de título mientras el administrador del sensor lógico crea un nodo de dispositivo para el sensor lógico.</span><span class="sxs-lookup"><span data-stu-id="8bd85-148">The virtual light sensor user interface will display the message "Waiting" in the title bar while the logical sensor manager creates a device node for the logical sensor.</span></span> <span data-ttu-id="8bd85-149">Después de que el mensaje en espera salga, puede usar el control deslizante para establecer el nivel de salida de lux para el sensor de luz virtual.</span><span class="sxs-lookup"><span data-stu-id="8bd85-149">After the waiting message goes away, you can use the slider to set the lux output level for the virtual light sensor.</span></span>

<span data-ttu-id="8bd85-150">En la imagen siguiente se muestra la interfaz de usuario del sensor de luz virtual en estado listo.</span><span class="sxs-lookup"><span data-stu-id="8bd85-150">The following image shows the virtual light sensor user interface in its ready state.</span></span>

![interfaz de usuario del sensor virtual Light](images/virtuallightsensor.png)

## <a name="related-topics"></a><span data-ttu-id="8bd85-152">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8bd85-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8bd85-153">Acerca de los sensores lógicos</span><span class="sxs-lookup"><span data-stu-id="8bd85-153">About Logical Sensors</span></span>](about-logical-sensors.md)
</dt> <dt>

[<span data-ttu-id="8bd85-154">**\_luz de categoría de sensor \_**</span><span class="sxs-lookup"><span data-stu-id="8bd85-154">**SENSOR\_CATEGORY\_LIGHT**</span></span>](sensor-category-light.md)
</dt> </dl>

 

