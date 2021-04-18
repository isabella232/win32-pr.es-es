---
title: Proveedor de servicios de ejemplo
description: Proveedor de servicios de ejemplo
ms.assetid: bbdeddb5-4ddf-4a61-828c-a9ba7af307ea
keywords:
- Administrador de dispositivos de Windows Media, ejemplos
- Administrador de dispositivos, ejemplos
- Windows Media Administrador de dispositivos, ejemplo de proveedor de servicios
- Administrador de dispositivos, ejemplo de proveedor de servicios
- proveedores de servicios, ejemplos
- ejemplos, proveedores de servicios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e8b7e781785944ac1ca390a62303f1149d710d1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105695329"
---
# <a name="sample-service-provider"></a><span data-ttu-id="d5a56-109">Proveedor de servicios de ejemplo</span><span class="sxs-lookup"><span data-stu-id="d5a56-109">Sample Service Provider</span></span>

<span data-ttu-id="d5a56-110">El SDK de Windows Media Administrador de dispositivos incluye un proveedor de servicios de ejemplo para su uso.</span><span class="sxs-lookup"><span data-stu-id="d5a56-110">The Windows Media Device Manager SDK includes a sample service provider for you to use.</span></span> <span data-ttu-id="d5a56-111">Este proveedor de servicios incluye una clase que informa de cada unidad de disco duro del equipo como si fuera un dispositivo conectado.</span><span class="sxs-lookup"><span data-stu-id="d5a56-111">This service provider includes a class that reports each hard drive on the computer as if it were an attached device.</span></span> <span data-ttu-id="d5a56-112">La única aplicación que utilizará este proveedor de servicios es la aplicación de ejemplo; El explorador de Windows no verá los dispositivos "devueltos por este proveedor de servicios".</span><span class="sxs-lookup"><span data-stu-id="d5a56-112">The only application that will use this service provider is the sample application; Windows Explorer will not see the "devices" reported by this service provider.</span></span> <span data-ttu-id="d5a56-113">El ejemplo de proveedor de servicios es un objeto COM compilado en ATL.</span><span class="sxs-lookup"><span data-stu-id="d5a56-113">The service provider sample is a COM object built on ATL.</span></span> <span data-ttu-id="d5a56-114">En los pasos siguientes se explica cómo usar el proveedor de servicios de ejemplo:</span><span class="sxs-lookup"><span data-stu-id="d5a56-114">The following steps explain how to use the sample service provider:</span></span>

> [!Note]  
> <span data-ttu-id="d5a56-115">El proveedor de servicios de ejemplo implementa muy pocas características, por lo que no debe usarse para probar aplicaciones de Windows Media Administrador de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="d5a56-115">The sample service provider implements very few features, and so it should not be used for testing Windows Media Device Manager applications.</span></span> <span data-ttu-id="d5a56-116">Para probar una aplicación, utilice un proveedor de servicios totalmente implementado.</span><span class="sxs-lookup"><span data-stu-id="d5a56-116">To test an application, use a fully-implemented service provider.</span></span>

 

-   <span data-ttu-id="d5a56-117">El ejemplo se ha enviado con un error de codificación que hará que el proveedor de servicios no funcione correctamente.</span><span class="sxs-lookup"><span data-stu-id="d5a56-117">The sample was shipped with a coding error that will cause the service provider to malfunction.</span></span> <span data-ttu-id="d5a56-118">Para corregir este error, abra el archivo MDSPEnumStorage. cpp instalado en la carpeta < *ruta de instalación del SDK*  > \\ WMFSDK95 \\ WMDM \\ mdsp \\ mshdsp, vaya a la línea 185 y cambie la línea siguiente:</span><span class="sxs-lookup"><span data-stu-id="d5a56-118">To correct this error, open the MDSPEnumStorage.cpp file installed in the folder < *SDK installation path* >\\WMFSDK95\\WMDM\\mdsp\\mshdsp, go to line 185, and change the following line:</span></span>

`wcsncpy(pStg->m_wcsName, m_wcsPath, dwLen);`

<span data-ttu-id="d5a56-119">Por esta otra:</span><span class="sxs-lookup"><span data-stu-id="d5a56-119">To this:</span></span>

`wcsncpy(pStg->m_wcsName, m_wcsPath, ARRAYSIZE(pStg->m_wcsName));`

1.  <span data-ttu-id="d5a56-120">Compile el archivo de MsHDSP.dll.</span><span class="sxs-lookup"><span data-stu-id="d5a56-120">Compile the MsHDSP.dll file.</span></span> <span data-ttu-id="d5a56-121">Puede hacerlo mediante NMAKE o Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="d5a56-121">You can do this using either NMAKE or Visual Studio.</span></span> <span data-ttu-id="d5a56-122">Vea [compilar el proveedor de servicios de ejemplo con NMAKE](compiling-the-sample-service-provider-using-nmake.md) o [compilar el proveedor de servicios de ejemplo con Visual Studio](compiling-the-sample-service-provider-using-visual-studio.md) para obtener información sobre cómo compilar la aplicación.</span><span class="sxs-lookup"><span data-stu-id="d5a56-122">See [Compiling the Sample Service Provider Using NMAKE](compiling-the-sample-service-provider-using-nmake.md) or [Compiling the Sample Service Provider Using Visual Studio](compiling-the-sample-service-provider-using-visual-studio.md) to learn how to compile the application.</span></span>
2.  <span data-ttu-id="d5a56-123">Registre MsHDSP.dll mediante regsvr32.</span><span class="sxs-lookup"><span data-stu-id="d5a56-123">Register MsHDSP.dll using regsvr32.</span></span> <span data-ttu-id="d5a56-124">En la línea siguiente, escrita en una ventana del símbolo del sistema en la misma carpeta que MsHDSP.dll, se registrará el proveedor de servicios de ejemplo:</span><span class="sxs-lookup"><span data-stu-id="d5a56-124">The following line, typed into a command-prompt window in the same folder as MsHDSP.dll, will register the sample service provider:</span></span>

    ```C++
    regsvr32 mshdsp.dll
    ```

    

    <span data-ttu-id="d5a56-125">Para detener la suplantación de un dispositivo, escriba la siguiente línea en el símbolo del sistema:</span><span class="sxs-lookup"><span data-stu-id="d5a56-125">To stop impersonating a device, enter the following line at the command prompt:</span></span>

    ```C++
    regsvr32 /u mshdsp.dll
    ```

    

3.  <span data-ttu-id="d5a56-126">Los dispositivos extraíbles suplantados por este archivo DLL solo pueden verse en la aplicación de ejemplo que se incluye con este SDK.</span><span class="sxs-lookup"><span data-stu-id="d5a56-126">The removable devices impersonated by this DLL can only be seen by the sample application shipped with this SDK.</span></span> <span data-ttu-id="d5a56-127">Compile la aplicación de ejemplo mediante uno de los métodos descritos en [aplicación de escritorio de ejemplo](sample-desktop-application.md).</span><span class="sxs-lookup"><span data-stu-id="d5a56-127">Compile the sample application using one of the methods described in [Sample Desktop Application](sample-desktop-application.md).</span></span>
4.  <span data-ttu-id="d5a56-128">Para depurar el proveedor de servicios con Visual Studio, abra el proveedor de servicios en Visual Studio y seleccione **iniciar** en el menú **depurar** .</span><span class="sxs-lookup"><span data-stu-id="d5a56-128">To debug the service provider with Visual Studio, open the service provider in Visual Studio and select **Start** on the **Debug** menu.</span></span> <span data-ttu-id="d5a56-129">En el cuadro de diálogo emergente, vaya a la aplicación de ejemplo que creó en el paso anterior y haga clic en **Aceptar**, y el proveedor de servicios comenzará a ejecutarse en modo de depuración.</span><span class="sxs-lookup"><span data-stu-id="d5a56-129">In the popup dialog box, browse to the sample application you built in the preceding step, and click **OK**, and the service provider will begin running in debug mode.</span></span>

    <span data-ttu-id="d5a56-130">Para ejecutar el proveedor de servicios sin depurar en Visual Studio, basta con registrar el msdhsp.dll y ejecutar la aplicación de escritorio de ejemplo que se incluye con el SDK.</span><span class="sxs-lookup"><span data-stu-id="d5a56-130">To run the service provider without debugging in Visual Studio, simply register the msdhsp.dll and run the sample desktop application that ships with the SDK.</span></span> <span data-ttu-id="d5a56-131">La aplicación de escritorio de ejemplo ejecuta el proveedor de servicios de ejemplo automáticamente.</span><span class="sxs-lookup"><span data-stu-id="d5a56-131">The sample desktop application runs the sample service provider automatically.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d5a56-132">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d5a56-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d5a56-133">**Ejemplos**</span><span class="sxs-lookup"><span data-stu-id="d5a56-133">**Samples**</span></span>](samples.md)
</dt> </dl>

 

 




