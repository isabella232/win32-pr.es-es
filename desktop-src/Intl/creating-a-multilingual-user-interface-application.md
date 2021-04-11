---
description: En este tutorial se muestra cómo tomar una aplicación Monolingual y hacer que esté lista para el mundo. Esta aplicación está en forma de una solución completa que se compila en Microsoft Visual Studio.
ms.assetid: 6d71aa90-8444-4f30-a2f8-f1a2aab015b0
title: Agregar compatibilidad con la interfaz de usuario multilingüe a una aplicación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 192d9053513a7fe915990c80deb32ffdb9114910
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912562"
---
# <a name="adding-multilingual-user-interface-support-to-an-application"></a><span data-ttu-id="67bfa-104">Agregar compatibilidad con la interfaz de usuario multilingüe a una aplicación</span><span class="sxs-lookup"><span data-stu-id="67bfa-104">Adding Multilingual User Interface Support to an Application</span></span>

<span data-ttu-id="67bfa-105">En este tutorial se muestra cómo tomar una aplicación Monolingual y hacer que esté lista para el mundo.</span><span class="sxs-lookup"><span data-stu-id="67bfa-105">This tutorial demonstrates how to take a monolingual application and make it world-ready.</span></span> <span data-ttu-id="67bfa-106">Esta aplicación está en forma de una solución completa que se compila en Microsoft Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="67bfa-106">This application is in the form of a complete solution that is built within Microsoft Visual Studio.</span></span>

-   [<span data-ttu-id="67bfa-107">Información general</span><span class="sxs-lookup"><span data-stu-id="67bfa-107">Overview</span></span>](#splitting-the-various-language-resource-modules-an-overview)
    -   [<span data-ttu-id="67bfa-108">La idea detrás de Hello MUI</span><span class="sxs-lookup"><span data-stu-id="67bfa-108">The Idea Behind Hello MUI</span></span>](#the-idea-behind-hello-mui)
-   [<span data-ttu-id="67bfa-109">Configuración de la solución Hello MUI</span><span class="sxs-lookup"><span data-stu-id="67bfa-109">Setting up the Hello MUI Solution</span></span>](#setting-up-the-hello-mui-solution)
    -   [<span data-ttu-id="67bfa-110">Requisitos de la plataforma</span><span class="sxs-lookup"><span data-stu-id="67bfa-110">Platform Requirements</span></span>](#platform-requirements)
    -   [<span data-ttu-id="67bfa-111">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="67bfa-111">Prerequisites</span></span>](#prerequisites)
-   [<span data-ttu-id="67bfa-112">Paso 0: creación del MUI de Hello codificado de forma rígida</span><span class="sxs-lookup"><span data-stu-id="67bfa-112">Step 0: Creating the Hard-coded Hello MUI</span></span>](#step-0-creating-the-hard-coded-hello-mui)
-   [<span data-ttu-id="67bfa-113">Paso 1: implementar el módulo de recursos básico</span><span class="sxs-lookup"><span data-stu-id="67bfa-113">Step 1: Implementing the Basic Resource Module</span></span>](#step-1-implementing-the-basic-resource-module)
-   [<span data-ttu-id="67bfa-114">Paso 2: compilar el módulo de recursos básico</span><span class="sxs-lookup"><span data-stu-id="67bfa-114">Step 2: Building the Basic Resource Module</span></span>](#step-2-building-the-basic-resource-module)
    -   [<span data-ttu-id="67bfa-115">División de los distintos módulos de recursos de idioma: información general</span><span class="sxs-lookup"><span data-stu-id="67bfa-115">Splitting the Various Language Resource Modules: An Overview</span></span>](#splitting-the-various-language-resource-modules-an-overview)
    -   [<span data-ttu-id="67bfa-116">División de los distintos módulos de recursos de idioma: crear los archivos</span><span class="sxs-lookup"><span data-stu-id="67bfa-116">Splitting the Various Language Resource Modules: Creating the Files</span></span>](#splitting-the-various-language-resource-modules-creating-the-files)
-   [<span data-ttu-id="67bfa-117">Paso 3: creación de un Resource-Savvy "Hello MUI"</span><span class="sxs-lookup"><span data-stu-id="67bfa-117">Step 3: Creating a Resource-Savvy "Hello MUI"</span></span>](#step-3-creating-a-resource-savvy-hello-mui)
-   [<span data-ttu-id="67bfa-118">Paso 4: globalización de "Hello MUI"</span><span class="sxs-lookup"><span data-stu-id="67bfa-118">Step 4: Globalizing "Hello MUI"</span></span>](#step-4-globalizing-hello-mui)
-   [<span data-ttu-id="67bfa-119">Paso 5: personalización de "Hello MUI"</span><span class="sxs-lookup"><span data-stu-id="67bfa-119">Step 5: Customizing "Hello MUI"</span></span>](#step-5-customizing-hello-mui)
-   [<span data-ttu-id="67bfa-120">Consideraciones adicionales para MUI</span><span class="sxs-lookup"><span data-stu-id="67bfa-120">Additional Considerations for MUI</span></span>](#additional-considerations-for-mui)
    -   [<span data-ttu-id="67bfa-121">Compatibilidad con aplicaciones de consola</span><span class="sxs-lookup"><span data-stu-id="67bfa-121">Support for Console Applications</span></span>](#support-for-console-applications)
    -   [<span data-ttu-id="67bfa-122">Determinación de los idiomas que se admiten en tiempo de ejecución</span><span class="sxs-lookup"><span data-stu-id="67bfa-122">Determination of Languages to Support at Run-Time</span></span>](#determination-of-languages-to-support-at-run-time)
    -   [<span data-ttu-id="67bfa-123">Compatibilidad con scripts complejos en versiones anteriores a Windows Vista</span><span class="sxs-lookup"><span data-stu-id="67bfa-123">Complex Script Support in Versions Prior to Windows Vista</span></span>](#complex-script-support-in-versions-prior-to-windows-vista)
-   [<span data-ttu-id="67bfa-124">Resumen</span><span class="sxs-lookup"><span data-stu-id="67bfa-124">Summary</span></span>](#summary)

## <a name="overview"></a><span data-ttu-id="67bfa-125">Información general</span><span class="sxs-lookup"><span data-stu-id="67bfa-125">Overview</span></span>

<span data-ttu-id="67bfa-126">A partir de Windows Vista, el propio sistema operativo Windows se creó desde el principio para ser una plataforma multilingüe, con compatibilidad adicional que le permite crear aplicaciones multilingües que usan el modelo de recursos de Windows MUI.</span><span class="sxs-lookup"><span data-stu-id="67bfa-126">Beginning with Windows Vista, the Windows operating system itself was built from the ground up to be a multilingual platform, with additional support that enables you to create multilingual applications that use the Windows MUI resource model.</span></span>

<span data-ttu-id="67bfa-127">En este tutorial se muestra esta nueva compatibilidad con aplicaciones multilingües, cubriendo los aspectos siguientes:</span><span class="sxs-lookup"><span data-stu-id="67bfa-127">This tutorial illustrates this new support for multilingual applications by covering the following aspects:</span></span>

-   <span data-ttu-id="67bfa-128">Usa la compatibilidad con la plataforma MUI mejorada para habilitar fácilmente aplicaciones multilingües.</span><span class="sxs-lookup"><span data-stu-id="67bfa-128">Uses the improved MUI platform support to easily enable multilingual applications.</span></span>
-   <span data-ttu-id="67bfa-129">Extiende las aplicaciones multilingües para que se ejecuten en versiones de Windows anteriores a Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="67bfa-129">Extends multilingual applications to run on versions of Windows prior to Windows Vista.</span></span>
-   <span data-ttu-id="67bfa-130">Toca las consideraciones adicionales implicadas en el desarrollo de aplicaciones multilingües especializadas, como aplicaciones de consola.</span><span class="sxs-lookup"><span data-stu-id="67bfa-130">Touches on the additional considerations involved in developing specialized multilingual applications such as console applications.</span></span>

<span data-ttu-id="67bfa-131">Estos vínculos ayudan a proporcionar un actualizador rápido sobre los conceptos sobre internacionalización y MUI:</span><span class="sxs-lookup"><span data-stu-id="67bfa-131">These links help provide a quick refresher on the concepts on internationalization and MUI:</span></span>

-   <span data-ttu-id="67bfa-132">[Información general rápida de internacionalización](understanding-internationalization.md).</span><span class="sxs-lookup"><span data-stu-id="67bfa-132">[Quick overview of internationalization](understanding-internationalization.md).</span></span>
-   <span data-ttu-id="67bfa-133">[Conceptos de MUI](understanding-mui.md).</span><span class="sxs-lookup"><span data-stu-id="67bfa-133">[MUI Concepts](understanding-mui.md).</span></span>
-   <span data-ttu-id="67bfa-134">[Usar MUI para desarrollar aplicaciones Win32](using-multilingual-user-interface.md).</span><span class="sxs-lookup"><span data-stu-id="67bfa-134">[Using MUI to develop Win32 applications](using-multilingual-user-interface.md).</span></span>

### <a name="the-idea-behind-hello-mui"></a><span data-ttu-id="67bfa-135">La idea detrás de Hello MUI</span><span class="sxs-lookup"><span data-stu-id="67bfa-135">The Idea Behind Hello MUI</span></span>

<span data-ttu-id="67bfa-136">Probablemente esté familiarizado con la aplicación Hola mundo clásica, que muestra los conceptos básicos de la programación.</span><span class="sxs-lookup"><span data-stu-id="67bfa-136">You are probably familiar with the classic Hello World application, which illustrates basic programming concepts.</span></span> <span data-ttu-id="67bfa-137">Este tutorial tiene un enfoque similar para ilustrar cómo usar el modelo de recursos de MUI para actualizar una aplicación de Monolingual para crear una versión multilingüe denominada Hola MUI.</span><span class="sxs-lookup"><span data-stu-id="67bfa-137">This tutorial takes a similar approach to illustrate how to use the MUI resource model to update a monolingual application to create a multilingual version called Hello MUI.</span></span>

> [!Note]  
> <span data-ttu-id="67bfa-138">Las tareas de este tutorial se describen en pasos detallados debido a la precisión con la que se deben realizar estas actividades y la necesidad de explicar los detalles a los desarrolladores que tienen poca experiencia con estas tareas.</span><span class="sxs-lookup"><span data-stu-id="67bfa-138">The tasks in this tutorial are described in detailed steps because of the precision with which these activities must be performed, and the need to explain the details to developers who have little experience with these tasks.</span></span>

 

## <a name="setting-up-the-hello-mui-solution"></a><span data-ttu-id="67bfa-139">Configuración de la solución Hello MUI</span><span class="sxs-lookup"><span data-stu-id="67bfa-139">Setting up the Hello MUI Solution</span></span>

<span data-ttu-id="67bfa-140">En estos pasos se describe cómo preparar la creación de la solución Hello MUI.</span><span class="sxs-lookup"><span data-stu-id="67bfa-140">These steps outline how to prepare to create the Hello MUI solution.</span></span>

### <a name="platform-requirements"></a><span data-ttu-id="67bfa-141">Requisitos de la plataforma</span><span class="sxs-lookup"><span data-stu-id="67bfa-141">Platform Requirements</span></span>

<span data-ttu-id="67bfa-142">Debe compilar los ejemplos de código de este tutorial con el kit de desarrollo de software (SDK) de Windows para Windows 7 y Visual Studio 2008.</span><span class="sxs-lookup"><span data-stu-id="67bfa-142">You must compile the code samples in this tutorial using the Windows Software Development Kit (SDK) for Windows 7 and Visual Studio 2008.</span></span> <span data-ttu-id="67bfa-143">El SDK de Windows 7 se instalará en Windows XP, Windows Vista y Windows 7, y la solución de ejemplo se puede crear en cualquiera de estas versiones de sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="67bfa-143">The Windows 7 SDK will install on Windows XP, Windows Vista and Windows 7, and the sample solution can be built on any of these operating system versions.</span></span>

<span data-ttu-id="67bfa-144">Todos los ejemplos de código de este tutorial están diseñados para ejecutarse en las versiones x86 y x64 de Windows XP, Windows Vista y Windows 7.</span><span class="sxs-lookup"><span data-stu-id="67bfa-144">All code samples in this tutorial are designed to be executed on x86 and x64 versions of Windows XP, Windows Vista and Windows 7.</span></span> <span data-ttu-id="67bfa-145">Las partes específicas que no funcionarán en Windows XP se indican donde corresponda.</span><span class="sxs-lookup"><span data-stu-id="67bfa-145">Specific parts that will not work on Windows XP are called out where appropriate.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="67bfa-146">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="67bfa-146">Prerequisites</span></span>

1.  <span data-ttu-id="67bfa-147">Instale Visual Studio 2008.</span><span class="sxs-lookup"><span data-stu-id="67bfa-147">Install Visual Studio 2008.</span></span>

    <span data-ttu-id="67bfa-148">Para obtener más información, vea el [Centro para desarrolladores de Visual Studio](https://msdn.microsoft.com/vstudio/default.aspx).</span><span class="sxs-lookup"><span data-stu-id="67bfa-148">For more information, see the [Visual Studio Developer Center](https://msdn.microsoft.com/vstudio/default.aspx).</span></span>

2.  <span data-ttu-id="67bfa-149">Instale el Windows SDK para Windows 7.</span><span class="sxs-lookup"><span data-stu-id="67bfa-149">Install the Windows SDK for Windows 7.</span></span>

    <span data-ttu-id="67bfa-150">Puede instalarlo desde la página Windows SDK del centro para [desarrolladores de Windows](https://msdn.microsoft.com/windowsserver/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="67bfa-150">You can install it from the Windows SDK page of the [Windows Developer Center](https://msdn.microsoft.com/windowsserver/bb980924.aspx).</span></span> <span data-ttu-id="67bfa-151">El SDK incluye utilidades para desarrollar aplicaciones para versiones del sistema operativo a partir de Windows XP a través del más reciente.</span><span class="sxs-lookup"><span data-stu-id="67bfa-151">The SDK includes utilities to develop applications for OS versions starting from Windows XP through the most recent.</span></span>

    > [!Note]  
    > <span data-ttu-id="67bfa-152">Si no va a instalar el paquete en la ubicación predeterminada, o si no está instalando en la unidad del sistema, que normalmente es la unidad C, tome nota de la ruta de instalación.</span><span class="sxs-lookup"><span data-stu-id="67bfa-152">If you are not installing the package to the default location, or if you are not installing on the system drive, which is usually the C drive, make note of the install path.</span></span>

     

3.  <span data-ttu-id="67bfa-153">Configure los parámetros de línea de comandos de Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="67bfa-153">Configure the Visual Studio command line parameters.</span></span>

    1.  <span data-ttu-id="67bfa-154">Abra una ventana de comandos de Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="67bfa-154">Open a Visual Studio command window.</span></span>
    2.  <span data-ttu-id="67bfa-155">Escriba **set path**.</span><span class="sxs-lookup"><span data-stu-id="67bfa-155">Type **set path**.</span></span>
    3.  <span data-ttu-id="67bfa-156">Confirme que la variable PATH incluye la ruta de acceso de la carpeta bin del SDK de Windows 7:... Microsoft SDK \\ Windows \\ v 7.0 \\ bin</span><span class="sxs-lookup"><span data-stu-id="67bfa-156">Confirm that the path variable includes the path of the bin folder of the Windows 7 SDK: ...Microsoft SDKs\\Windows\\v7.0\\bin</span></span>

4.  <span data-ttu-id="67bfa-157">Instale el paquete del complemento Microsoft NLS Downlevel API.</span><span class="sxs-lookup"><span data-stu-id="67bfa-157">Install the Microsoft NLS downlevel APIs add-on package.</span></span>
    > [!Note]  
    > <span data-ttu-id="67bfa-158">En el contexto de este tutorial, este paquete solo es necesario si va a personalizar la aplicación para que se ejecute en versiones de Windows anteriores a Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="67bfa-158">In the context of this tutorial, this package is necessary only if you will be customizing the application to run on Windows versions prior to Windows Vista.</span></span> <span data-ttu-id="67bfa-159">Vea [STEP 5: customizating Hello mui](#step-5-customizing-hello-mui).</span><span class="sxs-lookup"><span data-stu-id="67bfa-159">See [Step 5: Customizing Hello MUI](#step-5-customizing-hello-mui).</span></span>

     

    1.  <span data-ttu-id="67bfa-160">Descargue e instale el paquete desde su [sitio de descarga](https://www.microsoft.com/downloads/details.aspx?FamilyID=eb72cda0-834e-4c35-9419-ff14bc349c9d&amp;DisplayLang=en).</span><span class="sxs-lookup"><span data-stu-id="67bfa-160">Download and install the package from its [download site](https://www.microsoft.com/downloads/details.aspx?FamilyID=eb72cda0-834e-4c35-9419-ff14bc349c9d&amp;DisplayLang=en).</span></span>
    2.  <span data-ttu-id="67bfa-161">Al igual que con el Windows SDK, si no va a instalar el paquete en la ubicación predeterminada, o si no está instalando en la unidad del sistema, que normalmente es la unidad C, anote la ruta de instalación.</span><span class="sxs-lookup"><span data-stu-id="67bfa-161">As with the Windows SDK, if you are not installing the package to the default location, or if you are not installing on the system drive, which is usually the C drive, make note of the install path.</span></span>
    3.  <span data-ttu-id="67bfa-162">Si la plataforma de desarrollo es Windows XP o Windows Server 2003, confirme que Nlsdl.dll esté instalado y registrado correctamente.</span><span class="sxs-lookup"><span data-stu-id="67bfa-162">If your development platform is Windows XP or Windows Server 2003, confirm that Nlsdl.dll is installed and registered correctly.</span></span>

        1.  <span data-ttu-id="67bfa-163">Vaya a la carpeta "Redist" en la ubicación de la ruta de instalación.</span><span class="sxs-lookup"><span data-stu-id="67bfa-163">Browse to the "redist" folder under the install path location.</span></span>
        2.  <span data-ttu-id="67bfa-164">Ejecute el nlsdl redistribuible adecuado \* . exe, como nlsdl.x86.exe.</span><span class="sxs-lookup"><span data-stu-id="67bfa-164">Run the appropriate redistributable Nlsdl.\*.exe, such as nlsdl.x86.exe.</span></span> <span data-ttu-id="67bfa-165">En este paso se instalan y registran Nlsdl.dll.</span><span class="sxs-lookup"><span data-stu-id="67bfa-165">This step installs and registers Nlsdl.dll.</span></span>

    > [!Note]  
    > <span data-ttu-id="67bfa-166">Si desarrolla una aplicación que usa MUI y que se debe ejecutar en versiones de Windows anteriores a Windows Vista, Nlsdl.dll debe estar presente en la plataforma de Windows de destino.</span><span class="sxs-lookup"><span data-stu-id="67bfa-166">If you develop an application that uses MUI and that must run on Windows versions prior to Windows Vista, Nlsdl.dll must be present on the destination Windows platform.</span></span> <span data-ttu-id="67bfa-167">En la mayoría de los casos, esto significa que la aplicación debe llevar e instalar el instalador redistribuible de nlsdl (y no simplemente copiar Nlsdl.dll).</span><span class="sxs-lookup"><span data-stu-id="67bfa-167">In most cases, this means that the application needs to carry and install the redistributable Nlsdl installer (and not merely copy Nlsdl.dll itself).</span></span>

     

## <a name="step-0-creating-the-hard-coded-hello-mui"></a><span data-ttu-id="67bfa-168">Paso 0: creación del MUI de Hello codificado de forma rígida</span><span class="sxs-lookup"><span data-stu-id="67bfa-168">Step 0: Creating the Hard-coded Hello MUI</span></span>

<span data-ttu-id="67bfa-169">Este tutorial comienza con la versión Monolingual de la aplicación Hello MUI.</span><span class="sxs-lookup"><span data-stu-id="67bfa-169">This tutorial begins with the monolingual version of the Hello MUI application.</span></span> <span data-ttu-id="67bfa-170">La aplicación asume el uso del lenguaje de programación C++, las cadenas de caracteres anchos y la función [**MessageBoxW**](/windows/win32/api/winuser/nf-winuser-messagebox) para la salida.</span><span class="sxs-lookup"><span data-stu-id="67bfa-170">The application assumes the use of the C++ programming language, wide character strings, and the [**MessageBoxW**](/windows/win32/api/winuser/nf-winuser-messagebox) function for output.</span></span>

<span data-ttu-id="67bfa-171">Empiece por crear la aplicación GuiStep \_ 0 inicial, así como la solución HelloMUI, que contiene todas las aplicaciones de este tutorial.</span><span class="sxs-lookup"><span data-stu-id="67bfa-171">Begin by creating the initial GuiStep\_0 application, as well as the HelloMUI solution, which contain all of the applications in this tutorial.</span></span>

1.  <span data-ttu-id="67bfa-172">En Visual Studio 2008, cree un nuevo proyecto.</span><span class="sxs-lookup"><span data-stu-id="67bfa-172">In Visual Studio 2008, create a new project.</span></span> <span data-ttu-id="67bfa-173">Use los valores y valores siguientes:</span><span class="sxs-lookup"><span data-stu-id="67bfa-173">Use the following settings and values:</span></span>

    1.  <span data-ttu-id="67bfa-174">Tipo de proyecto: en Visual C++ Seleccione Win32 y, después, en plantillas instaladas de Visual Studio, seleccione proyecto Win32.</span><span class="sxs-lookup"><span data-stu-id="67bfa-174">Project type: Under Visual C++ select Win32, and then under Visual Studio installed templates select Win32 Project.</span></span>
    2.  <span data-ttu-id="67bfa-175">Nombre: GuiStep \_ 0.</span><span class="sxs-lookup"><span data-stu-id="67bfa-175">Name: GuiStep\_0.</span></span>
    3.  <span data-ttu-id="67bfa-176">Ubicación: *ProjectRootDirectory* (los pasos posteriores hacen referencia a este directorio).</span><span class="sxs-lookup"><span data-stu-id="67bfa-176">Location: *ProjectRootDirectory* (Later steps reference this directory).</span></span>
    4.  <span data-ttu-id="67bfa-177">Nombre de la solución: HelloMUI.</span><span class="sxs-lookup"><span data-stu-id="67bfa-177">Solution Name: HelloMUI.</span></span>
    5.  <span data-ttu-id="67bfa-178">Seleccione Crear directorio para la solución.</span><span class="sxs-lookup"><span data-stu-id="67bfa-178">Select Create directory for solution.</span></span>
    6.  <span data-ttu-id="67bfa-179">En el Asistente para aplicaciones Win32, seleccione el tipo de aplicación predeterminado: aplicación Windows.</span><span class="sxs-lookup"><span data-stu-id="67bfa-179">In the Win32 Application Wizard, select the default Application type: Windows application.</span></span>

2.  <span data-ttu-id="67bfa-180">Configure el modelo de subprocesos del proyecto:</span><span class="sxs-lookup"><span data-stu-id="67bfa-180">Configure the project threading model:</span></span>

    1.  <span data-ttu-id="67bfa-181">En el Explorador de soluciones, haga clic con el botón secundario en el proyecto GuiStep \_ 0 y, a continuación, seleccione Propiedades.</span><span class="sxs-lookup"><span data-stu-id="67bfa-181">In the Solution Explorer, right-click the project GuiStep\_0, and then select Properties.</span></span>
    2.  <span data-ttu-id="67bfa-182">En el cuadro de diálogo páginas de propiedades del proyecto:</span><span class="sxs-lookup"><span data-stu-id="67bfa-182">In the project Property Pages dialog box:</span></span>

        1.  <span data-ttu-id="67bfa-183">En la lista desplegable superior izquierda, establezca configuración en todas las configuraciones.</span><span class="sxs-lookup"><span data-stu-id="67bfa-183">In the top left drop-down, set Configuration to All Configurations.</span></span>
        2.  <span data-ttu-id="67bfa-184">En propiedades de configuración, expanda C/C++, seleccione generación de código y establezca biblioteca en tiempo de ejecución: depuración multiproceso (/MTd).</span><span class="sxs-lookup"><span data-stu-id="67bfa-184">Under Configuration Properties expand C/C++, select Code Generation, and set Runtime Library: Multi-threaded Debug (/MTd).</span></span>

3.  <span data-ttu-id="67bfa-185">Reemplace el contenido de GuiStep \_ 0. cpp por el código siguiente:</span><span class="sxs-lookup"><span data-stu-id="67bfa-185">Replace the contents of GuiStep\_0.cpp with the following code:</span></span>
    ```C++
    // GuiStep_0.cpp : Defines the entry point for the application.
    //

    #include "stdafx.h"
    #include "GuiStep_0.h"

    int WINAPI WinMain(HINSTANCE hInstance, HINSTANCE hPrevInstance, LPSTR lpCmdLine, int nCmdShow)
    {
        UNREFERENCED_PARAMETER(hInstance);
        UNREFERENCED_PARAMETER(hPrevInstance);
        UNREFERENCED_PARAMETER(lpCmdLine);
        UNREFERENCED_PARAMETER(nCmdShow);

        MessageBoxW(NULL,L"Hello MUI",L"HelloMUI!",MB_OK | MB_ICONINFORMATION);
        return 0;
    }
    ```

    

4.  <span data-ttu-id="67bfa-186">Compile y ejecute la aplicación.</span><span class="sxs-lookup"><span data-stu-id="67bfa-186">Build and run the application.</span></span>

<span data-ttu-id="67bfa-187">El código fuente sencillo anterior hace que la opción de diseño simplista de la codificación o la inserción se realice de forma rígida, todo el resultado que verá el usuario (en este caso, el texto "Hello MUI").</span><span class="sxs-lookup"><span data-stu-id="67bfa-187">The straightforward source code above makes the simplistic design choice of hard-coding, or embedding, all the output the user will see—in this case the text "Hello MUI".</span></span> <span data-ttu-id="67bfa-188">Esta opción limita la utilidad de la aplicación para los usuarios que no reconocen la palabra "Hola" en inglés.</span><span class="sxs-lookup"><span data-stu-id="67bfa-188">This choice limits the utility of the application for users who don't recognize the English word "Hello."</span></span> <span data-ttu-id="67bfa-189">Dado que MUI es un acrónimo en inglés basado en la tecnología, en este tutorial se supone que la cadena sigue siendo "MUI" para todos los idiomas.</span><span class="sxs-lookup"><span data-stu-id="67bfa-189">Because MUI is a technology-based English acronym, it is assumed for this tutorial that the string remains "MUI" for all languages.</span></span>

## <a name="step-1-implementing-the-basic-resource-module"></a><span data-ttu-id="67bfa-190">Paso 1: implementar el módulo de recursos básico</span><span class="sxs-lookup"><span data-stu-id="67bfa-190">Step 1: Implementing the Basic Resource Module</span></span>

<span data-ttu-id="67bfa-191">Microsoft Win32 ha expuesto la capacidad de los desarrolladores de aplicaciones para separar los datos de recursos de la interfaz de usuario del código fuente de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="67bfa-191">Microsoft Win32 has long exposed the capability for application developers to separate their UI resource data from application source code.</span></span> <span data-ttu-id="67bfa-192">Esta separación tiene el formato del modelo de recursos de Win32, en el que las cadenas, mapas de bits, iconos, mensajes y otros elementos que se muestran normalmente a un usuario se empaquetan en una sección distinta del archivo ejecutable, separadas del código ejecutable.</span><span class="sxs-lookup"><span data-stu-id="67bfa-192">This separation comes in the form of the Win32 resource model, in which strings, bitmaps, icons, messages and other items normally displayed to a user are packaged into a distinct section of the executable, separated from executable code.</span></span>

<span data-ttu-id="67bfa-193">Para ilustrar esta separación entre el código ejecutable y el empaquetado de datos de recursos, en este paso, el tutorial coloca la cadena "Hello" codificada previamente (el recurso "en-US") en la sección de recursos de un módulo DLL del \_ proyecto HelloModule en \_ EE. UU.</span><span class="sxs-lookup"><span data-stu-id="67bfa-193">To illustrate this separation between executable code and resource data packaging, in this step the tutorial places the previously hard-coded "Hello" string (the "en-US" resource) into the resource section of a DLL module in the HelloModule\_en\_us project.</span></span>

<span data-ttu-id="67bfa-194">Este archivo DLL de Win32 también puede contener la funcionalidad ejecutable de tipo de biblioteca (como cualquier otro archivo DLL).</span><span class="sxs-lookup"><span data-stu-id="67bfa-194">This Win32 DLL could also contain library type executable functionality (as any other DLL might).</span></span> <span data-ttu-id="67bfa-195">Pero para ayudar a centrarse en los aspectos relacionados con los recursos de Win32, dejamos en DllMain. cpp el código DLL en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="67bfa-195">But to help focus on the Win32 resource-related aspects, we leave the run-time DLL code stubbed out in dllmain.cpp.</span></span> <span data-ttu-id="67bfa-196">Las secciones siguientes de este tutorial hacen uso de los datos de recursos de HelloModule que se crean aquí y también presentan el código de tiempo de ejecución adecuado.</span><span class="sxs-lookup"><span data-stu-id="67bfa-196">Subsequent sections of this tutorial make use of the HelloModule resource data being built here and also present appropriate runtime code.</span></span>

<span data-ttu-id="67bfa-197">Para construir un módulo de recursos de Win32, empiece por crear un archivo DLL con una función DllMain de stub:</span><span class="sxs-lookup"><span data-stu-id="67bfa-197">To construct a Win32 resource module, start by creating a DLL with a stubbed out dllmain:</span></span>

1.  <span data-ttu-id="67bfa-198">Agregue un nuevo proyecto a la solución HelloMUI:</span><span class="sxs-lookup"><span data-stu-id="67bfa-198">Add a new project to the HelloMUI solution:</span></span>

    1.  <span data-ttu-id="67bfa-199">En el menú Archivo, seleccione Agregar y, a continuación, nuevo proyecto.</span><span class="sxs-lookup"><span data-stu-id="67bfa-199">From the File menu, select Add, and then New Project.</span></span>
    2.  <span data-ttu-id="67bfa-200">Tipo de proyecto: proyecto Win32.</span><span class="sxs-lookup"><span data-stu-id="67bfa-200">Project type: Win32 Project.</span></span>
    3.  <span data-ttu-id="67bfa-201">Nombre: HelloModule \_ en \_ EE. UU.</span><span class="sxs-lookup"><span data-stu-id="67bfa-201">Name: HelloModule\_en\_us.</span></span>
    4.  <span data-ttu-id="67bfa-202">Ubicación: *ProjectRootDirectory* \\ HelloMUI.</span><span class="sxs-lookup"><span data-stu-id="67bfa-202">Location: *ProjectRootDirectory*\\HelloMUI.</span></span>
    5.  <span data-ttu-id="67bfa-203">En el Asistente para aplicaciones Win32, seleccione tipo de aplicación: DLL.</span><span class="sxs-lookup"><span data-stu-id="67bfa-203">In the Win32 Application Wizard, select Application type: DLL.</span></span>

2.  <span data-ttu-id="67bfa-204">Configure el modelo de subprocesos de este proyecto:</span><span class="sxs-lookup"><span data-stu-id="67bfa-204">Configure this project's threading model:</span></span>

    1.  <span data-ttu-id="67bfa-205">En el Explorador de soluciones, haga clic con el botón derecho en el proyecto HelloModule \_ en \_ US y seleccione Propiedades.</span><span class="sxs-lookup"><span data-stu-id="67bfa-205">In the Solution Explorer, right-click the project HelloModule\_en\_us and select Properties.</span></span>
    2.  <span data-ttu-id="67bfa-206">En el cuadro de diálogo páginas de propiedades del proyecto:</span><span class="sxs-lookup"><span data-stu-id="67bfa-206">In the project's Property Pages dialog box:</span></span>

        1.  <span data-ttu-id="67bfa-207">En la lista desplegable superior izquierda, establezca configuración en todas las configuraciones.</span><span class="sxs-lookup"><span data-stu-id="67bfa-207">In the top left drop-down, set Configuration to All Configurations.</span></span>
        2.  <span data-ttu-id="67bfa-208">En propiedades de configuración, expanda C/C++, seleccione generación de código y establezca biblioteca en tiempo de ejecución: depuración multiproceso (/MTd).</span><span class="sxs-lookup"><span data-stu-id="67bfa-208">Under Configuration Properties expand C/C++, select Code Generation, and set Runtime Library: Multi-threaded Debug (/MTd).</span></span>

3.  <span data-ttu-id="67bfa-209">Examine DllMain. cpp.</span><span class="sxs-lookup"><span data-stu-id="67bfa-209">Examine dllmain.cpp.</span></span> <span data-ttu-id="67bfa-210">(Puede que desee agregar el no REFERENCIAdo \_ Las macros de parámetros al código generado, como tenemos aquí, para permitir que se compile en el nivel de ADVERTENCIA 4).</span><span class="sxs-lookup"><span data-stu-id="67bfa-210">(You may want to add the UNREFERENCED\_PARAMETER macros to the generated code, as we have here, to enable it to compile at warning level 4.)</span></span>
    ```C++
    // dllmain.cpp : Defines the entry point for the DLL application.
    #include "stdafx.h"

    BOOL APIENTRY DllMain( HMODULE hModule,
                           DWORD  ul_reason_for_call,
                           LPVOID lpReserved
                         )
    {
        UNREFERENCED_PARAMETER(hModule);
        UNREFERENCED_PARAMETER(lpReserved);

        switch (ul_reason_for_call)
        {
        case DLL_PROCESS_ATTACH:
        case DLL_THREAD_ATTACH:
        case DLL_THREAD_DETACH:
        case DLL_PROCESS_DETACH:
            break;
        }
        return TRUE;
    }
    ```

    

4.  <span data-ttu-id="67bfa-211">Agregue un archivo de definición de recursos HelloModule. rc al proyecto:</span><span class="sxs-lookup"><span data-stu-id="67bfa-211">Add a resource-definition file HelloModule.rc to the project:</span></span>

    1.  <span data-ttu-id="67bfa-212">En el proyecto HelloModule \_ en \_ EE. UU., haga clic con el botón derecho en la carpeta archivos de recursos, seleccione Agregar y, a continuación, seleccione nuevo elemento.</span><span class="sxs-lookup"><span data-stu-id="67bfa-212">Under the project HelloModule\_en\_us, right-click the Resource Files folder, and select Add, and then select New Item.</span></span>
    2.  <span data-ttu-id="67bfa-213">En el cuadro de diálogo Agregar nuevo elemento, elija lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="67bfa-213">In the Add New Item dialog box, choose the following:</span></span>

        1.  <span data-ttu-id="67bfa-214">Categorías: en Visual C++ Seleccione recurso y, en "plantillas instaladas de Visual Studio", seleccione Archivo de recursos (. RC).</span><span class="sxs-lookup"><span data-stu-id="67bfa-214">Categories: Under Visual C++ select Resource, and then under "Visual Studio installed templates" select Resource File (.rc).</span></span>
        2.  <span data-ttu-id="67bfa-215">Nombre: HelloModule.</span><span class="sxs-lookup"><span data-stu-id="67bfa-215">Name: HelloModule.</span></span>
        3.  <span data-ttu-id="67bfa-216">Ubicación: acepte el valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="67bfa-216">Location: accept the default.</span></span>
        4.  <span data-ttu-id="67bfa-217">Haga clic en Agregar.</span><span class="sxs-lookup"><span data-stu-id="67bfa-217">Click Add.</span></span>

    3.  <span data-ttu-id="67bfa-218">Especifique que el nuevo archivo HelloModule. RC se va a guardar como Unicode:</span><span class="sxs-lookup"><span data-stu-id="67bfa-218">Specify that the new HelloModule.rc file is to be saved as Unicode:</span></span>

        1.  <span data-ttu-id="67bfa-219">En el Explorador de soluciones, haga clic con el botón secundario en HelloModule. RC y seleccione Ver código.</span><span class="sxs-lookup"><span data-stu-id="67bfa-219">In the Solution Explorer, right-click HelloModule.rc, and select View Code.</span></span>
        2.  <span data-ttu-id="67bfa-220">Si ve un mensaje que le indica que el archivo ya está abierto y pregunta si desea cerrarlo, haga clic en sí.</span><span class="sxs-lookup"><span data-stu-id="67bfa-220">If you see a message that tells you that the file is already open, and asks whether you want to close it, click Yes.</span></span>
        3.  <span data-ttu-id="67bfa-221">Con el archivo mostrado como texto, cree el archivo de selección de menú y, a continuación, opciones avanzadas para guardar.</span><span class="sxs-lookup"><span data-stu-id="67bfa-221">With the file displayed as text, make the menu selection File and then Advanced Save Options.</span></span>
        4.  <span data-ttu-id="67bfa-222">En codificación, especifique Unicode-CodePage 1200.</span><span class="sxs-lookup"><span data-stu-id="67bfa-222">Under Encoding, specify Unicode - Codepage 1200.</span></span>
        5.  <span data-ttu-id="67bfa-223">Haga clic en Aceptar.</span><span class="sxs-lookup"><span data-stu-id="67bfa-223">Click OK.</span></span>
        6.  <span data-ttu-id="67bfa-224">Guarde y cierre HelloModule. rc.</span><span class="sxs-lookup"><span data-stu-id="67bfa-224">Save and close HelloModule.rc.</span></span>

    4.  <span data-ttu-id="67bfa-225">Agregue una tabla de cadenas que contenga la cadena "Hello":</span><span class="sxs-lookup"><span data-stu-id="67bfa-225">Add a string table containing the "Hello" string:</span></span>

        1.  <span data-ttu-id="67bfa-226">En el Vista de recursos, haga clic con el botón secundario en HelloModule. RC y seleccione Agregar recurso.</span><span class="sxs-lookup"><span data-stu-id="67bfa-226">In the Resource View, right-click HelloModule.rc and select Add Resource.</span></span>
        2.  <span data-ttu-id="67bfa-227">Seleccione Tabla de cadenas.</span><span class="sxs-lookup"><span data-stu-id="67bfa-227">Select String Table.</span></span>
        3.  <span data-ttu-id="67bfa-228">Haga clic en Nuevo.</span><span class="sxs-lookup"><span data-stu-id="67bfa-228">Click New.</span></span>
        4.  <span data-ttu-id="67bfa-229">Agregue una cadena a la tabla de cadenas:</span><span class="sxs-lookup"><span data-stu-id="67bfa-229">Add a string to the String Table:</span></span>

            1.  <span data-ttu-id="67bfa-230">ID: HELLO \_ mui \_ Str Str \_ 0.</span><span class="sxs-lookup"><span data-stu-id="67bfa-230">ID: HELLO\_MUI\_STR\_0.</span></span>
            2.  <span data-ttu-id="67bfa-231">Valor: 0.</span><span class="sxs-lookup"><span data-stu-id="67bfa-231">Value: 0.</span></span>
            3.  <span data-ttu-id="67bfa-232">Título: Hola.</span><span class="sxs-lookup"><span data-stu-id="67bfa-232">Caption: Hello.</span></span>

        <span data-ttu-id="67bfa-233">Si ve HelloModule. RC como texto ahora, verá varias partes del código fuente específico del recurso.</span><span class="sxs-lookup"><span data-stu-id="67bfa-233">If you view HelloModule.rc as text now, you will see various pieces of resource-specific source code.</span></span> <span data-ttu-id="67bfa-234">El mayor interés es la sección que describe la cadena "Hello":</span><span class="sxs-lookup"><span data-stu-id="67bfa-234">The one of greatest interest is the section that describes the "Hello" string:</span></span>

        ```C++
        /////////////////////////////////////////////////////////////////////////////
        //
        // String Table
        //

        STRINGTABLE 
        BEGIN
            HELLO_MUI_STR_0         "Hello"
        END
        ```

        

        <span data-ttu-id="67bfa-235">Esta cadena "Hello" es el recurso que debe localizarse (es decir, traducirse) en cada idioma que la aplicación espera que admita.</span><span class="sxs-lookup"><span data-stu-id="67bfa-235">This "Hello" string is the resource that needs to be localized (that is, translated) into every language that the application hopes to support.</span></span> <span data-ttu-id="67bfa-236">Por ejemplo, el HelloModule \_ TA \_ en el proyecto (que creará en el paso siguiente) contendrá su propia versión localizada de HelloModule. RC para "TA-in":</span><span class="sxs-lookup"><span data-stu-id="67bfa-236">For example, the HelloModule\_ta\_in project (which you will create in the next step) will contain its own localized version of HelloModule.rc for "ta-IN":</span></span>

        ```C++
        /////////////////////////////////////////////////////////////////////////////
        //
        // String Table
        //

        STRINGTABLE 
        BEGIN
            HELLO_MUI_STR_0         "வணக்கம்"
        END
        ```

        

    5.  <span data-ttu-id="67bfa-237">Compile el \_ proyecto HelloModule en \_ US para asegurarse de que no hay errores.</span><span class="sxs-lookup"><span data-stu-id="67bfa-237">Build the HelloModule\_en\_us project to be sure there are no errors.</span></span>

5.  <span data-ttu-id="67bfa-238">Cree seis proyectos más en la solución HelloMUI (o como muchos de los deseados) para crear seis dll de recursos más para otros idiomas.</span><span class="sxs-lookup"><span data-stu-id="67bfa-238">Create six more projects in the HelloMUI solution (or as many of them as you wish) to create six more resource DLLs for additional languages.</span></span> <span data-ttu-id="67bfa-239">Use los valores de esta tabla:</span><span class="sxs-lookup"><span data-stu-id="67bfa-239">Use the values in this table:</span></span>

    | <span data-ttu-id="67bfa-240">Nombre de proyecto</span><span class="sxs-lookup"><span data-stu-id="67bfa-240">Project name</span></span>        | <span data-ttu-id="67bfa-241">Nombre del archivo. RC</span><span class="sxs-lookup"><span data-stu-id="67bfa-241">Name of .rc file</span></span> | <span data-ttu-id="67bfa-242">Identificador de cadena</span><span class="sxs-lookup"><span data-stu-id="67bfa-242">String ID</span></span>          | <span data-ttu-id="67bfa-243">Valor de cadena</span><span class="sxs-lookup"><span data-stu-id="67bfa-243">String value</span></span> | <span data-ttu-id="67bfa-244">Título de cadena</span><span class="sxs-lookup"><span data-stu-id="67bfa-244">String caption</span></span> |
    |---------------------|------------------|--------------------|--------------|----------------|
    | <span data-ttu-id="67bfa-245">HelloModule \_ de \_</span><span class="sxs-lookup"><span data-stu-id="67bfa-245">HelloModule\_de\_de</span></span> | <span data-ttu-id="67bfa-246">HelloModule</span><span class="sxs-lookup"><span data-stu-id="67bfa-246">HelloModule</span></span>      | <span data-ttu-id="67bfa-247">HELLO \_ mui \_ Str Str \_ 0</span><span class="sxs-lookup"><span data-stu-id="67bfa-247">HELLO\_MUI\_STR\_0</span></span> | <span data-ttu-id="67bfa-248">0</span><span class="sxs-lookup"><span data-stu-id="67bfa-248">0</span></span>            | <span data-ttu-id="67bfa-249">Hallo</span><span class="sxs-lookup"><span data-stu-id="67bfa-249">Hallo</span></span>          |
    | <span data-ttu-id="67bfa-250">HelloModule \_ es \_ es</span><span class="sxs-lookup"><span data-stu-id="67bfa-250">HelloModule\_es\_es</span></span> | <span data-ttu-id="67bfa-251">HelloModule</span><span class="sxs-lookup"><span data-stu-id="67bfa-251">HelloModule</span></span>      | <span data-ttu-id="67bfa-252">HELLO \_ mui \_ Str Str \_ 0</span><span class="sxs-lookup"><span data-stu-id="67bfa-252">HELLO\_MUI\_STR\_0</span></span> | <span data-ttu-id="67bfa-253">0</span><span class="sxs-lookup"><span data-stu-id="67bfa-253">0</span></span>            | <span data-ttu-id="67bfa-254">Hola</span><span class="sxs-lookup"><span data-stu-id="67bfa-254">Hola</span></span>           |
    | <span data-ttu-id="67bfa-255">HelloModule \_ fr \_ fr</span><span class="sxs-lookup"><span data-stu-id="67bfa-255">HelloModule\_fr\_fr</span></span> | <span data-ttu-id="67bfa-256">HelloModule</span><span class="sxs-lookup"><span data-stu-id="67bfa-256">HelloModule</span></span>      | <span data-ttu-id="67bfa-257">HELLO \_ mui \_ Str Str \_ 0</span><span class="sxs-lookup"><span data-stu-id="67bfa-257">HELLO\_MUI\_STR\_0</span></span> | <span data-ttu-id="67bfa-258">0</span><span class="sxs-lookup"><span data-stu-id="67bfa-258">0</span></span>            | <span data-ttu-id="67bfa-259">Bonjour</span><span class="sxs-lookup"><span data-stu-id="67bfa-259">Bonjour</span></span>        |
    | <span data-ttu-id="67bfa-260">HelloModule \_ HI \_ en</span><span class="sxs-lookup"><span data-stu-id="67bfa-260">HelloModule\_hi\_in</span></span> | <span data-ttu-id="67bfa-261">HelloModule</span><span class="sxs-lookup"><span data-stu-id="67bfa-261">HelloModule</span></span>      | <span data-ttu-id="67bfa-262">HELLO \_ mui \_ Str Str \_ 0</span><span class="sxs-lookup"><span data-stu-id="67bfa-262">HELLO\_MUI\_STR\_0</span></span> | <span data-ttu-id="67bfa-263">0</span><span class="sxs-lookup"><span data-stu-id="67bfa-263">0</span></span>            | <span data-ttu-id="67bfa-264">नमस्</span><span class="sxs-lookup"><span data-stu-id="67bfa-264">नमस्</span></span>           |
    | <span data-ttu-id="67bfa-265">HelloModule \_ RU \_ RU</span><span class="sxs-lookup"><span data-stu-id="67bfa-265">HelloModule\_ru\_ru</span></span> | <span data-ttu-id="67bfa-266">HelloModule</span><span class="sxs-lookup"><span data-stu-id="67bfa-266">HelloModule</span></span>      | <span data-ttu-id="67bfa-267">HELLO \_ mui \_ Str Str \_ 0</span><span class="sxs-lookup"><span data-stu-id="67bfa-267">HELLO\_MUI\_STR\_0</span></span> | <span data-ttu-id="67bfa-268">0</span><span class="sxs-lookup"><span data-stu-id="67bfa-268">0</span></span>            | <span data-ttu-id="67bfa-269">Здравствуйте</span><span class="sxs-lookup"><span data-stu-id="67bfa-269">Здравствуйте</span></span>   |
    | <span data-ttu-id="67bfa-270">HelloModule \_ TA \_</span><span class="sxs-lookup"><span data-stu-id="67bfa-270">HelloModule\_ta\_in</span></span> | <span data-ttu-id="67bfa-271">HelloModule</span><span class="sxs-lookup"><span data-stu-id="67bfa-271">HelloModule</span></span>      | <span data-ttu-id="67bfa-272">HELLO \_ mui \_ Str Str \_ 0</span><span class="sxs-lookup"><span data-stu-id="67bfa-272">HELLO\_MUI\_STR\_0</span></span> | <span data-ttu-id="67bfa-273">0</span><span class="sxs-lookup"><span data-stu-id="67bfa-273">0</span></span>            | <span data-ttu-id="67bfa-274">வணக்கம்</span><span class="sxs-lookup"><span data-stu-id="67bfa-274">வணக்கம்</span></span>        |

    

     

<span data-ttu-id="67bfa-275">Para obtener más información sobre la sintaxis y la estructura del archivo. rc, consulte [acerca de los archivos de recursos](../menurc/about-resource-files.md).</span><span class="sxs-lookup"><span data-stu-id="67bfa-275">For more about .rc file structure and syntax, see [About Resource Files](../menurc/about-resource-files.md).</span></span>

## <a name="step-2-building-the-basic-resource-module"></a><span data-ttu-id="67bfa-276">Paso 2: compilar el módulo de recursos básico</span><span class="sxs-lookup"><span data-stu-id="67bfa-276">Step 2: Building the Basic Resource Module</span></span>

<span data-ttu-id="67bfa-277">Con los modelos de recursos anteriores, la creación de uno de los siete proyectos HelloModule daría como resultado siete dll independientes.</span><span class="sxs-lookup"><span data-stu-id="67bfa-277">Using previous resource models, building any one of the seven HelloModule projects would result in seven separate DLLs.</span></span> <span data-ttu-id="67bfa-278">Cada archivo DLL contiene una sección de recursos con una sola cadena localizada en el idioma adecuado.</span><span class="sxs-lookup"><span data-stu-id="67bfa-278">Each DLL would contain a resource section with a single string localized into the appropriate language.</span></span> <span data-ttu-id="67bfa-279">Aunque es adecuado para el modelo de recursos históricos de Win32, este diseño no aprovecha MUI.</span><span class="sxs-lookup"><span data-stu-id="67bfa-279">Although appropriate for the historic Win32 resource model, this design does not take advantage of MUI.</span></span>

<span data-ttu-id="67bfa-280">En el SDK de Windows Vista y versiones posteriores, MUI proporciona la capacidad de dividir los ejecutables en módulos de contenido localizable y código fuente.</span><span class="sxs-lookup"><span data-stu-id="67bfa-280">In the Windows Vista SDK and later, MUI provides the ability to split executables into source code and localizable content modules.</span></span> <span data-ttu-id="67bfa-281">Con la personalización adicional que se trata más adelante en el paso 5, las aplicaciones pueden estar habilitadas para que la compatibilidad con varios idiomas se ejecute en versiones anteriores a Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="67bfa-281">With the additional customization that is covered later in Step 5, applications can be enabled for multi-lingual support to run on versions prior to Windows Vista.</span></span>

<span data-ttu-id="67bfa-282">Los mecanismos principales disponibles para dividir los recursos del código ejecutable, a partir de Windows Vista, son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="67bfa-282">The primary mechanisms available to split resources from executable code, starting with Windows Vista, are:</span></span>

-   <span data-ttu-id="67bfa-283">Usar rc.exe (el compilador de RC) con modificadores específicos, o</span><span class="sxs-lookup"><span data-stu-id="67bfa-283">Using rc.exe (the RC Compiler) with specific switches, or</span></span>
-   <span data-ttu-id="67bfa-284">Usar una herramienta de división de estilo posterior a la compilación denominada muirct.exe.</span><span class="sxs-lookup"><span data-stu-id="67bfa-284">Using a post-build style splitting tool named muirct.exe.</span></span>

<span data-ttu-id="67bfa-285">Consulte [utilidades de recursos](resource-utilities.md) para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="67bfa-285">See [Resource Utilities](resource-utilities.md) for more information.</span></span>

<span data-ttu-id="67bfa-286">Por simplicidad, en este tutorial se usa muirct.exe para dividir el archivo ejecutable "Hello MUI".</span><span class="sxs-lookup"><span data-stu-id="67bfa-286">For the sake of simplicity, this tutorial uses muirct.exe to split the "Hello MUI" executable.</span></span>

### <a name="splitting-the-various-language-resource-modules-an-overview"></a><span data-ttu-id="67bfa-287">División de los distintos módulos de recursos de idioma: información general</span><span class="sxs-lookup"><span data-stu-id="67bfa-287">Splitting the Various Language Resource Modules: An Overview</span></span>

<span data-ttu-id="67bfa-288">Un proceso de varias partes implica dividir los archivos dll en un HelloModule.dll ejecutable, además de un HelloModule.dll. MUI para cada uno de los siete idiomas admitidos en este tutorial.</span><span class="sxs-lookup"><span data-stu-id="67bfa-288">A multi-part process is involved in splitting the DLLs into one executable HelloModule.dll, plus a HelloModule.dll.mui for each of the seven supported languages within this tutorial.</span></span> <span data-ttu-id="67bfa-289">En esta información general se describen los pasos necesarios; en la sección siguiente se muestra un archivo de comandos que realiza esos pasos.</span><span class="sxs-lookup"><span data-stu-id="67bfa-289">This overview describes the required steps; the next section presents a command file that performs those steps.</span></span>

<span data-ttu-id="67bfa-290">En primer lugar, divida el módulo de HelloModule.dll solo en inglés con el comando:</span><span class="sxs-lookup"><span data-stu-id="67bfa-290">First, split the English-only HelloModule.dll module by using the command:</span></span>


```C++
mkdir .\en-US
muirct.exe -q DoReverseMuiLoc.rcconfig -v 2 -x 0x0409 -g 0x0407 .\HelloModule_en_us.dll .\HelloModule.dll .\en-US\HelloModule.dll.mui
```



<span data-ttu-id="67bfa-291">La línea de comandos anterior usa el archivo de configuración DoReverseMuiLoc. rcconfig.</span><span class="sxs-lookup"><span data-stu-id="67bfa-291">The command line above uses the configuration file DoReverseMuiLoc.rcconfig.</span></span> <span data-ttu-id="67bfa-292">Normalmente, muirct.exe usa este tipo de archivo de configuración para dividir los recursos entre el archivo DLL del lenguaje neutro (LN) y los archivos. mui dependientes del lenguaje.</span><span class="sxs-lookup"><span data-stu-id="67bfa-292">This type of configuration file is typically used by muirct.exe to split resources between the language-neutral (LN) DLL and the language-dependent .mui files.</span></span> <span data-ttu-id="67bfa-293">En este caso, el archivo XML DoReverseMuiLoc. rcconfig (que se muestra en la sección siguiente) indica muchos tipos de recursos, pero todos se encuentran en la categoría de archivos "localizedResources" o. mui y no hay ningún recurso en la categoría de idioma neutro.</span><span class="sxs-lookup"><span data-stu-id="67bfa-293">In this case, the DoReverseMuiLoc.rcconfig xml file (listed in the next section) indicates many resource types, but they all fall into the "localizedResources" or .mui file category, and there are no resources in the language-neutral category.</span></span> <span data-ttu-id="67bfa-294">Para obtener más información sobre cómo preparar un archivo de configuración de recursos, vea [preparar un archivo de configuración de recursos](preparing-a-resource-configuration-file.md).</span><span class="sxs-lookup"><span data-stu-id="67bfa-294">For more information about how to prepare a resource configuration file, see [Preparing a Resource Configuration File](preparing-a-resource-configuration-file.md).</span></span>

<span data-ttu-id="67bfa-295">Además de crear un archivo HelloModule.dll. mui que contiene la cadena en inglés "Hello", muirct.exe también inserta un recurso de MUI en el módulo de HelloModule.dll durante la división.</span><span class="sxs-lookup"><span data-stu-id="67bfa-295">In addition to creating a HelloModule.dll.mui file which contains the English string "Hello", muirct.exe also embeds a MUI resource into the HelloModule.dll module during the splitting.</span></span> <span data-ttu-id="67bfa-296">Con el fin de cargar correctamente en tiempo de ejecución los recursos adecuados desde los módulos de HelloModule.dll. mui específicos del idioma, cada archivo. mui debe tener sus sumas de comprobación fijas para que coincidan con las sumas de comprobación en el módulo LN del lenguaje de línea de base.</span><span class="sxs-lookup"><span data-stu-id="67bfa-296">In order to properly load at run-time the appropriate resources from the language-specific HelloModule.dll.mui modules, each .mui file must have its checksums fixed-up to match the checksums in the baseline language-neutral LN module.</span></span> <span data-ttu-id="67bfa-297">Esto se realiza mediante un comando como:</span><span class="sxs-lookup"><span data-stu-id="67bfa-297">This is done by a command such as:</span></span>


```C++
muirct.exe -c HelloModule.dll -e en-US\HelloModule.dll.mui
```



<span data-ttu-id="67bfa-298">Del mismo modo, muirct.exe se invoca para crear un archivo HelloModule.dll. MUI para cada uno de los demás idiomas.</span><span class="sxs-lookup"><span data-stu-id="67bfa-298">Similarly, muirct.exe is invoked to create a HelloModule.dll.mui file for each of the other languages.</span></span> <span data-ttu-id="67bfa-299">Sin embargo, en esos casos se descarta el archivo DLL independiente del lenguaje, ya que solo se necesitará el primero que se cree.</span><span class="sxs-lookup"><span data-stu-id="67bfa-299">However, in those cases the language-neutral DLL is discarded, as only the first one created will be needed.</span></span> <span data-ttu-id="67bfa-300">Los comandos que procesan los recursos español y francés tienen el siguiente aspecto:</span><span class="sxs-lookup"><span data-stu-id="67bfa-300">The commands that process the Spanish and French resources look like this:</span></span>


```C++
mkdir .\es-ES
muirct.exe -q DoReverseMuiLoc.rcconfig -v 2 -x 0x0C0A -g 0x0407 .\HelloModule_es_es.dll .\HelloModule_discard.dll .\es-ES\HelloModule.dll.mui
muirct.exe -c HelloModule.dll -e es-ES\HelloModule.dll.mui

mkdir .\fr-FR
muirct.exe -q DoReverseMuiLoc.rcconfig -v 2 -x 0x040C -g 0x0407 .\HelloModule_fr_fr.dll .\HelloModule_discard.dll .\fr-FR\HelloModule.dll.mui
muirct.exe -c HelloModule.dll -e fr-FR\HelloModule.dll.mui
```



<span data-ttu-id="67bfa-301">Uno de los aspectos más importantes que se deben tener en cuenta en el muirct.exe las líneas de comandos anteriores es que la marca-x se usa para especificar un identificador de idioma de destino.</span><span class="sxs-lookup"><span data-stu-id="67bfa-301">One of the most important things to notice in the muirct.exe command lines above is that the -x flag is used to specify a target language ID.</span></span> <span data-ttu-id="67bfa-302">El valor proporcionado para muirct.exe es diferente para cada módulo de HelloModule.dll específico del idioma.</span><span class="sxs-lookup"><span data-stu-id="67bfa-302">The value provided to muirct.exe is different for each language-specific HelloModule.dll module.</span></span> <span data-ttu-id="67bfa-303">Este valor de idioma es central y lo usa muirct.exe para marcar correctamente el archivo. mui durante la división.</span><span class="sxs-lookup"><span data-stu-id="67bfa-303">This language value is central and is used by muirct.exe to appropriately mark the .mui file during splitting.</span></span> <span data-ttu-id="67bfa-304">Un valor incorrecto produce errores de carga de recursos para ese archivo. mui determinado en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="67bfa-304">An incorrect value produces resource loading failures for that particular .mui file at run-time.</span></span> <span data-ttu-id="67bfa-305">Consulte [constantes y cadenas de identificador de idioma](language-identifier-constants-and-strings.md) para obtener más detalles sobre cómo asignar el nombre del idioma a LCID.</span><span class="sxs-lookup"><span data-stu-id="67bfa-305">See [Language Identifier Constants and Strings](language-identifier-constants-and-strings.md) for more details on mapping language name to LCID.</span></span>

<span data-ttu-id="67bfa-306">Cada archivo Split. mui termina de colocarse en un directorio que se corresponde con su nombre de idioma, inmediatamente debajo del directorio en el que residirá el HelloModule.dll independiente del lenguaje.</span><span class="sxs-lookup"><span data-stu-id="67bfa-306">Each split .mui file ends up being placed into a directory corresponding to its language name, immediately underneath the directory in which the language-neutral HelloModule.dll will reside.</span></span> <span data-ttu-id="67bfa-307">Para obtener más información sobre la ubicación de los archivos. MUI, vea [implementación de aplicaciones](application-deployment.md).</span><span class="sxs-lookup"><span data-stu-id="67bfa-307">For more about .mui file placement, see [Application Deployment](application-deployment.md).</span></span>

### <a name="splitting-the-various-language-resource-modules-creating-the-files"></a><span data-ttu-id="67bfa-308">División de los distintos módulos de recursos de idioma: crear los archivos</span><span class="sxs-lookup"><span data-stu-id="67bfa-308">Splitting the Various Language Resource Modules: Creating the Files</span></span>

<span data-ttu-id="67bfa-309">En este tutorial se crea un archivo de comandos que contiene los comandos para dividir los distintos archivos dll y se invoca manualmente.</span><span class="sxs-lookup"><span data-stu-id="67bfa-309">For this tutorial you create a command file containing the commands to split the various DLLs, and you invoke it manually.</span></span> <span data-ttu-id="67bfa-310">Tenga en cuenta que, en el trabajo de desarrollo real, puede reducir la posibilidad de que se produzcan errores de compilación al incluir estos comandos como eventos anteriores o posteriores a la compilación en la solución HelloMUI, pero eso está fuera del ámbito de este tutorial.</span><span class="sxs-lookup"><span data-stu-id="67bfa-310">Note that in actual development work, you could reduce the potential for build errors by including these commands as pre-build or post-build events in the HelloMUI solution, but that is beyond the scope of this tutorial.</span></span>

<span data-ttu-id="67bfa-311">Cree los archivos para la compilación de depuración:</span><span class="sxs-lookup"><span data-stu-id="67bfa-311">Create the files for the debug build:</span></span>

1.  <span data-ttu-id="67bfa-312">Cree un archivo de comandos DoReverseMuiLoc. cmd que contenga los siguientes comandos:</span><span class="sxs-lookup"><span data-stu-id="67bfa-312">Create a command file DoReverseMuiLoc.cmd containing the following commands:</span></span>
    ```C++
    mkdir .\en-US
    muirct.exe -q DoReverseMuiLoc.rcconfig -v 2 -x 0x0409 -g 0x0407 .\HelloModule_en_us.dll .\HelloModule.dll .\en-US\HelloModule.dll.mui
    muirct.exe -c HelloModule.dll -e en-US\HelloModule.dll.mui

    mkdir .\de-DE
    muirct.exe -q DoReverseMuiLoc.rcconfig -v 2 -x 0x0407 -g 0x0407 .\HelloModule_de_de.dll .\HelloModule_discard.dll .\de-DE\HelloModule.dll.mui
    muirct.exe -c HelloModule.dll -e de-DE\HelloModule.dll.mui

    mkdir .\es-ES
    muirct.exe -q DoReverseMuiLoc.rcconfig -v 2 -x 0x0C0A -g 0x0407 .\HelloModule_es_es.dll .\HelloModule_discard.dll .\es-ES\HelloModule.dll.mui
    muirct.exe -c HelloModule.dll -e es-ES\HelloModule.dll.mui

    mkdir .\fr-FR
    muirct.exe -q DoReverseMuiLoc.rcconfig -v 2 -x 0x040C -g 0x0407 .\HelloModule_fr_fr.dll .\HelloModule_discard.dll .\fr-FR\HelloModule.dll.mui
    muirct.exe -c HelloModule.dll -e fr-FR\HelloModule.dll.mui

    mkdir .\hi-IN
    muirct.exe -q DoReverseMuiLoc.rcconfig -v 2 -x 0x0439 -g 0x0407 .\HelloModule_hi_in.dll .\HelloModule_discard.dll .\hi-IN\HelloModule.dll.mui
    muirct.exe -c HelloModule.dll -e hi-IN\HelloModule.dll.mui

    mkdir .\ru-RU
    muirct.exe -q DoReverseMuiLoc.rcconfig -v 2 -x 0x0419 -g 0x0407 .\HelloModule_ru_ru.dll .\HelloModule_discard.dll .\ru-RU\HelloModule.dll.mui
    muirct.exe -c HelloModule.dll -e ru-RU\HelloModule.dll.mui

    mkdir .\ta-IN
    muirct.exe -q DoReverseMuiLoc.rcconfig -v 2 -x 0x0449 -g 0x0407 .\HelloModule_ta_in.dll .\HelloModule_discard.dll .\ta-IN\HelloModule.dll.mui
    muirct.exe -c HelloModule.dll -e ta-IN\HelloModule.dll.mui
    pause
    ```

    

2.  <span data-ttu-id="67bfa-313">Cree un archivo XML DoReverseMuiLoc. rcconfig que contenga las líneas siguientes:</span><span class="sxs-lookup"><span data-stu-id="67bfa-313">Create an xml file DoReverseMuiLoc.rcconfig containing the following lines:</span></span>
    ```C++
    <?xml version="1.0" encoding="utf-8"?>
        <localization>
            <resources>
                <win32Resources fileType="Application">
                    <neutralResources>
                    </neutralResources>
                    <localizedResources>
                        <resourceType typeNameId="#1"/>
                        <resourceType typeNameId="#10"/>
                        <resourceType typeNameId="#1024"/>
                        <resourceType typeNameId="#11"/>
                        <resourceType typeNameId="#12"/>
                        <resourceType typeNameId="#13"/>
                        <resourceType typeNameId="#14"/>
                        <resourceType typeNameId="#15"/>
                        <resourceType typeNameId="#16"/>
                        <resourceType typeNameId="#17"/>
                        <resourceType typeNameId="#18"/>
                        <resourceType typeNameId="#19"/>
                        <resourceType typeNameId="#2"/>
                        <resourceType typeNameId="#20"/>
                        <resourceType typeNameId="#2110"/>
                        <resourceType typeNameId="#23"/>
                        <resourceType typeNameId="#240"/>
                        <resourceType typeNameId="#3"/>
                        <resourceType typeNameId="#4"/>
                        <resourceType typeNameId="#5"/>
                        <resourceType typeNameId="#6"/>
                        <resourceType typeNameId="#7"/>
                        <resourceType typeNameId="#8"/>
                        <resourceType typeNameId="#9"/>
                        <resourceType typeNameId="HTML"/>
                        <resourceType typeNameId="MOFDATA"/>
                    </localizedResources>
                </win32Resources>
            </resources>
        </localization>
    ```

    

3.  <span data-ttu-id="67bfa-314">Copie DoReverseMuiLoc. cmd y DoReverseMuiLoc. rcconfig en *ProjectRootDirectory* \\ HelloMUI \\ Debug.</span><span class="sxs-lookup"><span data-stu-id="67bfa-314">Copy DoReverseMuiLoc.cmd and DoReverseMuiLoc.rcconfig to *ProjectRootDirectory*\\HelloMUI\\Debug.</span></span>
4.  <span data-ttu-id="67bfa-315">Abra el símbolo del sistema de Visual Studio 2008 y navegue hasta el directorio de depuración.</span><span class="sxs-lookup"><span data-stu-id="67bfa-315">Open the Visual Studio 2008 command prompt and navigate to the Debug directory.</span></span>
5.  <span data-ttu-id="67bfa-316">Ejecute DoReverseMuiLoc. cmd.</span><span class="sxs-lookup"><span data-stu-id="67bfa-316">Run DoReverseMuiLoc.cmd.</span></span>

<span data-ttu-id="67bfa-317">Al crear una compilación de versión, copie los mismos archivos DoReverseMuiLoc. cmd y DoReverseMuiLoc. rcconfig en el directorio de versión y ejecute el archivo de comandos allí.</span><span class="sxs-lookup"><span data-stu-id="67bfa-317">When you create a release build, you copy the same DoReverseMuiLoc.cmd and DoReverseMuiLoc.rcconfig files to the Release directory and run the command file there.</span></span>

## <a name="step-3-creating-a-resource-savvy-hello-mui"></a><span data-ttu-id="67bfa-318">Paso 3: creación de un Resource-Savvy "Hello MUI"</span><span class="sxs-lookup"><span data-stu-id="67bfa-318">Step 3: Creating a Resource-Savvy "Hello MUI"</span></span>

<span data-ttu-id="67bfa-319">Al basarse en el \_ ejemplo de GuiStep0.exe codificado de forma rígida anterior, podría ampliar el alcance de la aplicación a varios usuarios de lenguajes si opta por incorporar el modelo de recursos de Win32.</span><span class="sxs-lookup"><span data-stu-id="67bfa-319">Building on the initial hard-coded GuiStep\_0.exe example from above, you could extend the reach of the application to multiple language users by choosing to incorporate the Win32 resource model.</span></span> <span data-ttu-id="67bfa-320">El nuevo código en tiempo de ejecución presentado en este paso incluye la lógica de carga de módulos ([**LoadLibraryEx**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibraryexa)) y de recuperación de cadenas ([**LoadString**](/windows/win32/api/winuser/nf-winuser-loadstringa)).</span><span class="sxs-lookup"><span data-stu-id="67bfa-320">The new run-time code presented in this step includes the module loading ([**LoadLibraryEx**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibraryexa)) and string retrieval ([**LoadString**](/windows/win32/api/winuser/nf-winuser-loadstringa)) logic.</span></span>

1.  <span data-ttu-id="67bfa-321">Agregue un nuevo proyecto a la solución HelloMUI (mediante el archivo de selección de menú, agregue y nuevo proyecto) con los valores y valores siguientes:</span><span class="sxs-lookup"><span data-stu-id="67bfa-321">Add a new project to the HelloMUI solution (using the menu selection File, Add, and New Project) with the following settings and values:</span></span>

    1.  <span data-ttu-id="67bfa-322">Tipo de proyecto: proyecto Win32.</span><span class="sxs-lookup"><span data-stu-id="67bfa-322">Project type: Win32 Project.</span></span>
    2.  <span data-ttu-id="67bfa-323">Nombre: GuiStep \_ 1.</span><span class="sxs-lookup"><span data-stu-id="67bfa-323">Name: GuiStep\_1.</span></span>
    3.  <span data-ttu-id="67bfa-324">Ubicación: acepte el valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="67bfa-324">Location: accept the default.</span></span>
    4.  <span data-ttu-id="67bfa-325">En el Asistente para aplicaciones Win32, seleccione el tipo de aplicación predeterminado: aplicación Windows.</span><span class="sxs-lookup"><span data-stu-id="67bfa-325">In the Win32 Application Wizard, select the default Application type: Windows application.</span></span>

2.  <span data-ttu-id="67bfa-326">Establezca este proyecto para que se ejecute desde dentro de Visual Studio y configure su modelo de subprocesos:</span><span class="sxs-lookup"><span data-stu-id="67bfa-326">Set this project to run from within Visual Studio, and configure its threading model:</span></span>

    1.  <span data-ttu-id="67bfa-327">En el Explorador de soluciones, haga clic con el botón derecho en el proyecto GuiStep \_ 1 y seleccione establecer como proyecto de inicio.</span><span class="sxs-lookup"><span data-stu-id="67bfa-327">In the Solution Explorer, right-click the project GuiStep\_1 and select Set as StartUp Project.</span></span>
    2.  <span data-ttu-id="67bfa-328">Vuelva a hacer clic con el botón secundario y seleccione Propiedades.</span><span class="sxs-lookup"><span data-stu-id="67bfa-328">Right-click it again and select Properties.</span></span>
    3.  <span data-ttu-id="67bfa-329">En el cuadro de diálogo páginas de propiedades del proyecto:</span><span class="sxs-lookup"><span data-stu-id="67bfa-329">In the project's Property Pages dialog box:</span></span>

        1.  <span data-ttu-id="67bfa-330">En la lista desplegable superior izquierda, establezca configuración en todas las configuraciones.</span><span class="sxs-lookup"><span data-stu-id="67bfa-330">In the top left drop-down, set Configuration to All Configurations.</span></span>
        2.  <span data-ttu-id="67bfa-331">En propiedades de configuración, expanda C/C++, seleccione generación de código y establezca biblioteca en tiempo de ejecución: depuración multiproceso (/MTd).</span><span class="sxs-lookup"><span data-stu-id="67bfa-331">Under Configuration Properties expand C/C++, select Code Generation, and set Runtime Library: Multi-threaded Debug (/MTd).</span></span>

3.  <span data-ttu-id="67bfa-332">Reemplace el contenido de GuiStep \_ 1. cpp por el código siguiente:</span><span class="sxs-lookup"><span data-stu-id="67bfa-332">Replace the contents of GuiStep\_1.cpp with the following code:</span></span>
    ```C++
    // GuiStep_1.cpp : Defines the entry point for the application.
    //

    #include "stdafx.h"
    #include "GuiStep_1.h"
    #include "..\HelloModule_en_us\resource.h"

    #define SUFFICIENTLY_LARGE_STRING_BUFFER (MAX_PATH*2)
    #define SUFFICIENTLY_LARGE_ERROR_BUFFER (1024*2)
    #define HELLO_MODULE_CONTRIVED_FILE_PATH  (L"HelloModule.dll")

    int WINAPI WinMain(HINSTANCE hInstance, HINSTANCE hPrevInstance, LPSTR lpCmdLine, int nCmdShow)
    {
        UNREFERENCED_PARAMETER(hInstance);
        UNREFERENCED_PARAMETER(hPrevInstance);
        UNREFERENCED_PARAMETER(lpCmdLine);
        UNREFERENCED_PARAMETER(nCmdShow);

        // The following code presents a hypothetical, yet common use pattern of MUI technology
        WCHAR displayBuffer[SUFFICIENTLY_LARGE_ERROR_BUFFER];

        // 1. Basic application obtains access to the proper resource container 
        // for standard Win32 resource loading this is normally a PE module - use LoadLibraryEx
        // LoadLibraryEx is the preferred alternative for resource modules as used below because it
        // provides increased security and performance over that of LoadLibrary
        HMODULE resContainer = LoadLibraryExW(HELLO_MODULE_CONTRIVED_FILE_PATH,NULL,LOAD_LIBRARY_AS_IMAGE_RESOURCE | LOAD_LIBRARY_AS_DATAFILE);
        if(!resContainer)
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to load the resource container module, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            return 1; // exit
        }

        // 2. Application parses the resource container to find the appropriate item
        WCHAR szHello[SUFFICIENTLY_LARGE_STRING_BUFFER];
        if(LoadStringW(resContainer,HELLO_MUI_STR_0,szHello,SUFFICIENTLY_LARGE_STRING_BUFFER) == 0)
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to load the resource string, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            FreeLibrary(resContainer);
            return 1; // exit
        }

        // 3. Application presents the discovered resource to the user via UI
        swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"%s MUI",szHello);
        MessageBoxW(NULL,displayBuffer,L"HelloMUI",MB_OK | MB_ICONINFORMATION);

        // 4. Application cleans up memory associated with the resource container after this item is no longer needed.
        if(!FreeLibrary(resContainer))
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to unload the resource container, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            return 1; // exit
        }

        return 0;
    }
    ```

    

4.  <span data-ttu-id="67bfa-333">Compile y ejecute la aplicación.</span><span class="sxs-lookup"><span data-stu-id="67bfa-333">Build and run the application.</span></span> <span data-ttu-id="67bfa-334">El resultado se mostrará en el idioma establecido actualmente como el idioma de visualización del equipo (siempre que sea uno de los siete idiomas que hemos creado).</span><span class="sxs-lookup"><span data-stu-id="67bfa-334">The output will be displayed in the language currently set as the display language of the computer (provided it is one of the seven languages we have built).</span></span>

## <a name="step-4-globalizing-hello-mui"></a><span data-ttu-id="67bfa-335">Paso 4: globalización de "Hello MUI"</span><span class="sxs-lookup"><span data-stu-id="67bfa-335">Step 4: Globalizing "Hello MUI"</span></span>

<span data-ttu-id="67bfa-336">Aunque el ejemplo anterior es capaz de mostrar su salida en distintos idiomas, es breve en varias áreas.</span><span class="sxs-lookup"><span data-stu-id="67bfa-336">Although the previous example is able to display its output in different languages, it falls short in a number of areas.</span></span> <span data-ttu-id="67bfa-337">Quizás lo más notable es que la aplicación solo está disponible en un pequeño subconjunto de idiomas en comparación con el propio sistema operativo Windows.</span><span class="sxs-lookup"><span data-stu-id="67bfa-337">Perhaps the most noticeable is that the application is only available in a small subset of languages when compared to the Windows operating system itself.</span></span> <span data-ttu-id="67bfa-338">Si, por ejemplo, la \_ aplicación GuiStep 1 del paso anterior se instalaba en una compilación en japonés de Windows, es probable que se produzcan errores de ubicación de recursos.</span><span class="sxs-lookup"><span data-stu-id="67bfa-338">If, for example, the GuiStep\_1 application from the previous step were installed on a Japanese build of Windows, resource location failures would be likely.</span></span>

<span data-ttu-id="67bfa-339">Para solucionar esta situación, tiene dos opciones principales:</span><span class="sxs-lookup"><span data-stu-id="67bfa-339">To address this situation, you have two primary options:</span></span>

-   <span data-ttu-id="67bfa-340">Asegúrese de que se incluyen los recursos de un idioma de reserva Ultimate predeterminados.</span><span class="sxs-lookup"><span data-stu-id="67bfa-340">Ensure that resources in a predetermined ultimate fallback language are included.</span></span>
-   <span data-ttu-id="67bfa-341">Proporcionar una manera para que el usuario final Configure sus preferencias de idioma entre el subconjunto de idiomas admitidos específicamente por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="67bfa-341">Provide a way for the end user to configure their language preferences from among the subset of languages specifically supported by the application.</span></span>

<span data-ttu-id="67bfa-342">De estas opciones, el que proporciona un lenguaje de reserva final es muy aconsejable y se implementa en este tutorial pasando la marca-g a muirct.exe, como se ha mencionado anteriormente.</span><span class="sxs-lookup"><span data-stu-id="67bfa-342">Of these options, the one providing an ultimate fallback language is highly advisable and is implemented in this tutorial by passing the -g flag to muirct.exe, as seen above.</span></span> <span data-ttu-id="67bfa-343">Esta marca indica muirct.exe para convertir un idioma específico (de-DE/0x0407) en el idioma de reserva final asociado con el módulo DLL independiente del lenguaje (HelloModule.dll).</span><span class="sxs-lookup"><span data-stu-id="67bfa-343">This flag tells muirct.exe to make a specific language (de-DE / 0x0407) the ultimate fallback language associated with the language-neutral dll module (HelloModule.dll).</span></span> <span data-ttu-id="67bfa-344">En tiempo de ejecución, este parámetro se utiliza como último recurso para generar el texto que se va a mostrar al usuario.</span><span class="sxs-lookup"><span data-stu-id="67bfa-344">At run-time this parameter is used as a last resort to generate text to display to the user.</span></span> <span data-ttu-id="67bfa-345">En caso de que no se encuentre un idioma de reserva final y no haya ningún recurso adecuado disponible en el binario independiente del lenguaje, se producirá un error al cargar el recurso.</span><span class="sxs-lookup"><span data-stu-id="67bfa-345">In the event that an ultimate fallback language is not found and no appropriate resource is available in the language-neutral binary, loading of the resource fails.</span></span> <span data-ttu-id="67bfa-346">Por lo tanto, debe determinar cuidadosamente los escenarios en los que puede encontrarse la aplicación y planear el lenguaje de reserva final en consecuencia.</span><span class="sxs-lookup"><span data-stu-id="67bfa-346">Therefore you should carefully determine the scenarios that your application might encounter and plan the ultimate fallback language accordingly.</span></span>

<span data-ttu-id="67bfa-347">La otra opción de permitir las preferencias de idioma configurables y cargar recursos basados en esta jerarquía definida por el usuario puede aumentar considerablemente la satisfacción del cliente.</span><span class="sxs-lookup"><span data-stu-id="67bfa-347">The other option of allowing for configurable language preferences and loading resources based on this user-defined hierarchy can greatly increase customer satisfaction.</span></span> <span data-ttu-id="67bfa-348">Desafortunadamente, también complica la funcionalidad necesaria dentro de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="67bfa-348">Unfortunately, it also complicates the functionality needed within the application.</span></span>

<span data-ttu-id="67bfa-349">Este paso del tutorial usa un mecanismo de archivo de texto simplificado para habilitar la configuración de idioma del usuario personalizado.</span><span class="sxs-lookup"><span data-stu-id="67bfa-349">This step of the tutorial uses a simplified text file mechanism to enable custom user language configuration.</span></span> <span data-ttu-id="67bfa-350">La aplicación analiza el archivo de texto en tiempo de ejecución, y la lista de idiomas analizados y validados se usa para establecer una lista de reserva personalizada.</span><span class="sxs-lookup"><span data-stu-id="67bfa-350">The text file is parsed at run-time by the application, and the parsed and validated language list is used in establishing a custom fallback list.</span></span> <span data-ttu-id="67bfa-351">Una vez establecida la lista de reserva personalizada, las API de Windows cargarán los recursos según la prioridad de idioma establecida en esta lista.</span><span class="sxs-lookup"><span data-stu-id="67bfa-351">After the custom fallback list is established, the Windows APIs will load resources according to the language precedence set forth in this list.</span></span> <span data-ttu-id="67bfa-352">El resto del código es similar al que se encontró en el paso anterior.</span><span class="sxs-lookup"><span data-stu-id="67bfa-352">The remainder of the code is similar to that found in the preceding step.</span></span>

1.  <span data-ttu-id="67bfa-353">Agregue un nuevo proyecto a la solución HelloMUI (mediante el archivo de selección de menú, agregue y nuevo proyecto) con los valores y valores siguientes:</span><span class="sxs-lookup"><span data-stu-id="67bfa-353">Add a new project to the HelloMUI solution (using the menu selection File, Add, and New Project) with the following settings and values:</span></span>

    1.  <span data-ttu-id="67bfa-354">Tipo de proyecto: proyecto Win32.</span><span class="sxs-lookup"><span data-stu-id="67bfa-354">Project type: Win32 Project.</span></span>
    2.  <span data-ttu-id="67bfa-355">Nombre: GuiStep \_ 2.</span><span class="sxs-lookup"><span data-stu-id="67bfa-355">Name: GuiStep\_2.</span></span>
    3.  <span data-ttu-id="67bfa-356">Ubicación: acepte el valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="67bfa-356">Location: accept the default.</span></span>
    4.  <span data-ttu-id="67bfa-357">En el Asistente para aplicaciones Win32, seleccione el tipo de aplicación predeterminado: aplicación Windows.</span><span class="sxs-lookup"><span data-stu-id="67bfa-357">In the Win32 Application Wizard, select the default Application type: Windows application.</span></span>

2.  <span data-ttu-id="67bfa-358">Establezca este proyecto para que se ejecute desde dentro de Visual Studio y configure su modelo de subprocesos:</span><span class="sxs-lookup"><span data-stu-id="67bfa-358">Set this project to run from within Visual Studio, and configure its threading model:</span></span>

    1.  <span data-ttu-id="67bfa-359">En el Explorador de soluciones, haga clic con el botón derecho en el proyecto GuiStep \_ 2 y seleccione establecer como proyecto de inicio.</span><span class="sxs-lookup"><span data-stu-id="67bfa-359">In the Solution Explorer, right-click the project GuiStep\_2 and select Set as StartUp Project.</span></span>
    2.  <span data-ttu-id="67bfa-360">Vuelva a hacer clic con el botón secundario y seleccione Propiedades.</span><span class="sxs-lookup"><span data-stu-id="67bfa-360">Right-click it again and select Properties.</span></span>
    3.  <span data-ttu-id="67bfa-361">En el cuadro de diálogo páginas de propiedades del proyecto:</span><span class="sxs-lookup"><span data-stu-id="67bfa-361">In the project's Property Pages dialog box:</span></span>

        1.  <span data-ttu-id="67bfa-362">En la lista desplegable superior izquierda, establezca configuración en todas las configuraciones.</span><span class="sxs-lookup"><span data-stu-id="67bfa-362">In the top left drop-down, set Configuration to All Configurations.</span></span>
        2.  <span data-ttu-id="67bfa-363">En propiedades de configuración, expanda C/C++, seleccione generación de código y establezca biblioteca en tiempo de ejecución: depuración multiproceso (/MTd).</span><span class="sxs-lookup"><span data-stu-id="67bfa-363">Under Configuration Properties expand C/C++, select Code Generation, and set Runtime Library: Multi-threaded Debug (/MTd).</span></span>

3.  <span data-ttu-id="67bfa-364">Reemplace el contenido de GuiStep \_ 2. cpp por el código siguiente:</span><span class="sxs-lookup"><span data-stu-id="67bfa-364">Replace the contents of GuiStep\_2.cpp with the following code:</span></span>
    ```C++
    // GuiStep_2.cpp : Defines the entry point for the application.
    //

    #include "stdafx.h"
    #include "GuiStep_2.h"
    #include <strsafe.h>
    #include "..\HelloModule_en_us\resource.h"

    #define SUFFICIENTLY_LARGE_STRING_BUFFER (MAX_PATH*2)
    #define USER_CONFIGURATION_STRING_BUFFER (((LOCALE_NAME_MAX_LENGTH+1)*5)+1)
    #define SUFFICIENTLY_LARGE_ERROR_BUFFER (1024*2)
    #define HELLO_MODULE_CONTRIVED_FILE_PATH  (L"HelloModule.dll")

    BOOL GetMyUserDefinedLanguages(WCHAR * langStr, DWORD langStrSize);
    BOOL ConvertMyLangStrToMultiLangStr(WCHAR * langStr, WCHAR * langMultiStr, DWORD langMultiStrSize);

    int WINAPI WinMain(HINSTANCE hInstance, HINSTANCE hPrevInstance, LPSTR lpCmdLine, int nCmdShow)
    {
        UNREFERENCED_PARAMETER(hInstance);
        UNREFERENCED_PARAMETER(hPrevInstance);
        UNREFERENCED_PARAMETER(lpCmdLine);
        UNREFERENCED_PARAMETER(nCmdShow);

        // The following code presents a hypothetical, yet common use pattern of MUI technology
        WCHAR displayBuffer[SUFFICIENTLY_LARGE_ERROR_BUFFER];

        // 1. Application starts by applying any user defined language preferences
        // (language setting is potentially optional for an application that wishes to strictly use OS system language fallback)
        // 1a. Application looks in pre-defined location for user preferences (registry, file, web, etc.)
        WCHAR userLanguagesString[USER_CONFIGURATION_STRING_BUFFER*2];
        if(!GetMyUserDefinedLanguages(userLanguagesString,USER_CONFIGURATION_STRING_BUFFER*2))
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to find the user defined language configuration, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            return 1; // exit
        }
        // 1b. Application converts the user defined 'readable' languages to the proper multi-string 'less readable' language name format
        WCHAR userLanguagesMultiString[USER_CONFIGURATION_STRING_BUFFER];
        if(!ConvertMyLangStrToMultiLangStr(userLanguagesString,userLanguagesMultiString,USER_CONFIGURATION_STRING_BUFFER))
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to convert the user defined language configuration to multi-string, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            return 1; // exit
        }
        // 1c. Application now sets the appropriate fallback list
        DWORD langCount = 0;
        // next commented out line of code could be used on Windows 7 and later
        // using SetProcessPreferredUILanguages is recomended for new applications (esp. multi-threaded applications)
    //    if(!SetProcessPreferredUILanguages(MUI_LANGUAGE_NAME,userLanguagesMultiString,&langCount) || langCount == 0)
        // the following line of code is supported on Windows Vista and later
        if(!SetThreadPreferredUILanguages(MUI_LANGUAGE_NAME,userLanguagesMultiString,&langCount) || langCount == 0)
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to set the user defined languages, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            return 1; // exit
        }
        // NOTES on step #1:
        // an application developer that makes the assumption the fallback list provided by the
        // system / OS is entirely sufficient may or may not be making a good assumption based 
        // mostly on:
        // A. your choice of languages installed with your application
        // B. the languages on the OS at application install time
        // C. the OS users propensity to install/uninstall language packs
        // D. the OS users propensity to change laguage settings

        // 2. Application obtains access to the proper resource container 
        // for standard Win32 resource loading this is normally a PE module - use LoadLibraryEx
        // LoadLibraryEx is the preferred alternative for resource modules as used below because it
        // provides increased security and performance over that of LoadLibrary
        HMODULE resContainer = LoadLibraryExW(HELLO_MODULE_CONTRIVED_FILE_PATH,NULL,LOAD_LIBRARY_AS_IMAGE_RESOURCE | LOAD_LIBRARY_AS_DATAFILE);
        if(!resContainer)
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to load the resource container module, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            return 1; // exit
        }

        // 3. Application parses the resource container to find the appropriate item
        WCHAR szHello[SUFFICIENTLY_LARGE_STRING_BUFFER];
        if(LoadStringW(resContainer,HELLO_MUI_STR_0,szHello,SUFFICIENTLY_LARGE_STRING_BUFFER) == 0)
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to load the resource string, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            FreeLibrary(resContainer);
            return 1; // exit
        }

        // 4. Application presents the discovered resource to the user via UI
        swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"%s MUI",szHello);
        MessageBoxW(NULL,displayBuffer,L"HelloMUI",MB_OK | MB_ICONINFORMATION);

        // 5. Application cleans up memory associated with the resource container after this item is no longer needed.
        if(!FreeLibrary(resContainer))
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to unload the resource container, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            return 1; // exit
        }

        return 0;
    }

    BOOL GetMyUserDefinedLanguages(WCHAR * langStr, DWORD langStrSize)
    {
        BOOL rtnVal = FALSE;
        // very simple implementation - assumes that first 'langStrSize' characters of the 
        // L".\\langs.txt" file comprises a string of one or more languages
        HANDLE langConfigFileHandle = CreateFileW(L".\\langs.txt", GENERIC_READ, 0, 
            NULL, OPEN_EXISTING, FILE_ATTRIBUTE_NORMAL, NULL);
        if(langConfigFileHandle != INVALID_HANDLE_VALUE)
        {
            // clear out the input variables
            DWORD bytesActuallyRead = 0;
            if(ReadFile(langConfigFileHandle,langStr,langStrSize*sizeof(WCHAR),&bytesActuallyRead,NULL) && bytesActuallyRead > 0)
            {
                rtnVal = TRUE;
                DWORD nullIndex = (bytesActuallyRead/sizeof(WCHAR) < langStrSize) ? bytesActuallyRead/sizeof(WCHAR) : langStrSize;
                langStr[nullIndex] = L'\0';
            }
            CloseHandle(langConfigFileHandle);
        }
        return rtnVal;
    }
    BOOL ConvertMyLangStrToMultiLangStr(WCHAR * langStr, WCHAR * langMultiStr, DWORD langMultiStrSize)
    {
        BOOL rtnVal = FALSE;
        size_t strLen = 0;
        rtnVal = SUCCEEDED(StringCchLengthW(langStr,USER_CONFIGURATION_STRING_BUFFER*2,&strLen));
        if(rtnVal && strLen > 0 && langMultiStr && langMultiStrSize > 0)
        {
            WCHAR * langMultiStrPtr = langMultiStr;
            WCHAR * last = langStr + (langStr[0] == 0xFEFF ? 1 : 0);
            WCHAR * context = last;
            WCHAR * next = wcstok_s(last,L",; :",&context);
            while(next && rtnVal)
            {
                // make sure you validate the user input
                if(SUCCEEDED(StringCchLengthW(last,LOCALE_NAME_MAX_LENGTH,&strLen)) && 
                    IsValidLocaleName(next))
                {
                    langMultiStrPtr[0] = L'\0';
                    rtnVal &= SUCCEEDED(StringCchCatW(langMultiStrPtr,(langMultiStrSize - (langMultiStrPtr - langMultiStr)),next));
                    langMultiStrPtr += strLen + 1;
                }
                next = wcstok_s(NULL,L",; :",&context);
                if(next)
                    last = next;
            }
            if(rtnVal && (langMultiStrSize - (langMultiStrPtr - langMultiStr))) // make sure there is a double null term for the multi-string
            {
                langMultiStrPtr[0] = L'\0';
            }
            else // fail and guard anyone whom might use the multi-string
            {
                langMultiStr[0] = L'\0';
                langMultiStr[1] = L'\0';
            }
        }
        return rtnVal;
    }
    ```

    

4.  <span data-ttu-id="67bfa-365">Cree un archivo de texto Unicode langs.txt que contenga la línea siguiente:</span><span class="sxs-lookup"><span data-stu-id="67bfa-365">Create a Unicode text file langs.txt containing the following line:</span></span>

    ``` syntax
    hi-IN ta-IN ru-RU fr-FR es-ES en-US
    ```

    > [!Note]  
    > <span data-ttu-id="67bfa-366">Asegúrese de guardar el archivo como Unicode.</span><span class="sxs-lookup"><span data-stu-id="67bfa-366">Be sure to save the file as Unicode.</span></span>

     

    <span data-ttu-id="67bfa-367">Copie langs.txt en el directorio desde el que se ejecutará el programa:</span><span class="sxs-lookup"><span data-stu-id="67bfa-367">Copy langs.txt to the directory from which the program will run:</span></span>

    -   <span data-ttu-id="67bfa-368">Si se ejecuta desde dentro de Visual Studio, cópielo en *ProjectRootDirectory* \\ HelloMUI \\ GuiStep \_ 2.</span><span class="sxs-lookup"><span data-stu-id="67bfa-368">If running from within Visual Studio, copy it to *ProjectRootDirectory*\\HelloMUI\\GuiStep\_2.</span></span>
    -   <span data-ttu-id="67bfa-369">Si se ejecuta desde el explorador de Windows, cópielo en el mismo directorio que GuiStep \_2.exe.</span><span class="sxs-lookup"><span data-stu-id="67bfa-369">If running from Windows Explorer, copy it to the same directory as GuiStep\_2.exe.</span></span>

5.  <span data-ttu-id="67bfa-370">Compile y ejecute el proyecto.</span><span class="sxs-lookup"><span data-stu-id="67bfa-370">Build and run the project.</span></span> <span data-ttu-id="67bfa-371">Intente editar langs.txt para que aparezcan distintos idiomas al principio de la lista.</span><span class="sxs-lookup"><span data-stu-id="67bfa-371">Try editing langs.txt so that different languages appear at the front of the list.</span></span>

## <a name="step-5-customizing-hello-mui"></a><span data-ttu-id="67bfa-372">Paso 5: personalización de "Hello MUI"</span><span class="sxs-lookup"><span data-stu-id="67bfa-372">Step 5: Customizing "Hello MUI"</span></span>

<span data-ttu-id="67bfa-373">Una serie de las características en tiempo de ejecución que se mencionan hasta ahora en este tutorial solo están disponibles en Windows Vista y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="67bfa-373">A number of the run-time features mentioned so far within this tutorial are available only on Windows Vista and later.</span></span> <span data-ttu-id="67bfa-374">Es posible que desee volver a usar el esfuerzo invertido en la localización y la división de recursos haciendo que la aplicación funcione en versiones anteriores del sistema operativo Windows, como Windows XP.</span><span class="sxs-lookup"><span data-stu-id="67bfa-374">You may wish to re-use the effort invested in localizing and splitting resources by making the application work on downlevel Windows operating system versions, such as Windows XP.</span></span> <span data-ttu-id="67bfa-375">Este proceso implica ajustar el ejemplo anterior en dos áreas clave:</span><span class="sxs-lookup"><span data-stu-id="67bfa-375">This process involves adjusting the previous example in two key areas:</span></span>

-   <span data-ttu-id="67bfa-376">Las funciones de carga de recursos anteriores a Windows Vista (como [**LoadString**](/windows/win32/api/winuser/nf-winuser-loadstringa), [**LoadIcon**](/windows/win32/api/winuser/nf-winuser-loadicona), [**loadBitmap**](/windows/win32/api/winuser/nf-winuser-loadbitmapa), [**FormatMessage**](/windows/win32/api/winbase/nf-winbase-formatmessage)y otras) no reconocen MUI.</span><span class="sxs-lookup"><span data-stu-id="67bfa-376">The pre-Windows Vista resource loading functions (such as [**LoadString**](/windows/win32/api/winuser/nf-winuser-loadstringa), [**LoadIcon**](/windows/win32/api/winuser/nf-winuser-loadicona), [**LoadBitmap**](/windows/win32/api/winuser/nf-winuser-loadbitmapa), [**FormatMessage**](/windows/win32/api/winbase/nf-winbase-formatmessage), and others) are non-MUI aware.</span></span> <span data-ttu-id="67bfa-377">Las aplicaciones que se distribuyen con recursos divididos (archivos LN y. MUI) deben cargar los módulos de recursos mediante una de estas dos funciones:</span><span class="sxs-lookup"><span data-stu-id="67bfa-377">Applications that ship with split resources (LN and .mui files) must load resource modules using one of these two functions:</span></span>

    -   <span data-ttu-id="67bfa-378">Si la aplicación solo se va a ejecutar en Windows Vista y versiones posteriores, debe cargar los módulos de recursos con [**LoadLibraryEx**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibraryexa).</span><span class="sxs-lookup"><span data-stu-id="67bfa-378">If the application is to be run only on Windows Vista and later, it should load resource modules with [**LoadLibraryEx**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibraryexa).</span></span>
    -   <span data-ttu-id="67bfa-379">Si la aplicación se va a ejecutar en versiones anteriores a Windows Vista, así como en Windows Vista o posterior, debe usar [**LoadMUILibrary**](/windows/desktop/api/Muiload/nf-muiload-loadmuilibrarya), que es una función de nivel inferior específica que se proporciona en el SDK de Windows 7.</span><span class="sxs-lookup"><span data-stu-id="67bfa-379">If the application is to be run on versions prior to Windows Vista, as well as Windows Vista or later, it must use [**LoadMUILibrary**](/windows/desktop/api/Muiload/nf-muiload-loadmuilibrarya), which is a specific downlevel function provided in the Windows 7 SDK.</span></span>

-   <span data-ttu-id="67bfa-380">La compatibilidad con la administración de idiomas y el orden de reserva de idioma que se ofrece en las versiones anteriores a Windows Vista del sistema operativo Windows difiere significativamente de la de Windows Vista y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="67bfa-380">The language management and language fallback order support offered in pre-Windows Vista versions of the Windows operating system differs significantly from that in Windows Vista and later.</span></span> <span data-ttu-id="67bfa-381">Por este motivo, las aplicaciones que permiten la reserva de idiomas configurados por el usuario deben ajustar sus prácticas de administración de idioma:</span><span class="sxs-lookup"><span data-stu-id="67bfa-381">For this reason, applications that allow user-configured language fallback must adjust their language management practices:</span></span>

    -   <span data-ttu-id="67bfa-382">Si la aplicación solo se va a ejecutar en Windows Vista y versiones posteriores, basta con establecer la lista de idiomas con [**SetThreadPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-setthreadpreferreduilanguages) .</span><span class="sxs-lookup"><span data-stu-id="67bfa-382">If the application is to be run only on Windows Vista and later, setting the language list using [**SetThreadPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-setthreadpreferreduilanguages) is sufficient.</span></span>
    -   <span data-ttu-id="67bfa-383">Si la aplicación se va a ejecutar en todas las versiones de Windows, se debe construir código que se ejecutará en plataformas de nivel inferior para recorrer en iteración la lista de idiomas configurados por el usuario y sondear el módulo de recursos deseado.</span><span class="sxs-lookup"><span data-stu-id="67bfa-383">If the application is to be run on all Windows versions, code must be constructed that will run on downlevel platforms to iterate through the user configured language list and probe for the desired resource module.</span></span> <span data-ttu-id="67bfa-384">Esto se puede observar en las secciones 1C y 2 del código que se proporciona más adelante en este paso.</span><span class="sxs-lookup"><span data-stu-id="67bfa-384">This can be seen in sections 1c and 2 of the code provided later in this step.</span></span>

<span data-ttu-id="67bfa-385">Cree un proyecto que pueda usar los módulos de recursos localizados en cualquier versión de Windows:</span><span class="sxs-lookup"><span data-stu-id="67bfa-385">Create a project that can use the localized resource modules on any version of Windows:</span></span>

1.  <span data-ttu-id="67bfa-386">Agregue un nuevo proyecto a la solución HelloMUI (mediante el archivo de selección de menú, agregue y nuevo proyecto) con los valores y valores siguientes:</span><span class="sxs-lookup"><span data-stu-id="67bfa-386">Add a new project to the HelloMUI solution (using the menu selection File, Add, and New Project) with the following settings and values:</span></span>

    1.  <span data-ttu-id="67bfa-387">Tipo de proyecto: proyecto Win32.</span><span class="sxs-lookup"><span data-stu-id="67bfa-387">Project type: Win32 Project.</span></span>
    2.  <span data-ttu-id="67bfa-388">Nombre: GuiStep \_ 3.</span><span class="sxs-lookup"><span data-stu-id="67bfa-388">Name: GuiStep\_3.</span></span>
    3.  <span data-ttu-id="67bfa-389">Ubicación: acepte el valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="67bfa-389">Location: accept the default.</span></span>
    4.  <span data-ttu-id="67bfa-390">En el Asistente para aplicaciones Win32, seleccione el tipo de aplicación predeterminado: aplicación Windows.</span><span class="sxs-lookup"><span data-stu-id="67bfa-390">In the Win32 Application Wizard, select the default Application type: Windows application.</span></span>

2.  <span data-ttu-id="67bfa-391">Establezca este proyecto para que se ejecute desde Visual Studio y configure su modelo de subprocesos.</span><span class="sxs-lookup"><span data-stu-id="67bfa-391">Set this project to run from within Visual Studio, and configure its threading model.</span></span> <span data-ttu-id="67bfa-392">Además, configúrelo para agregar los encabezados y las bibliotecas necesarios.</span><span class="sxs-lookup"><span data-stu-id="67bfa-392">Also, configure it to add the necessary headers and libraries.</span></span>

    > [!Note]  
    > <span data-ttu-id="67bfa-393">Las rutas de acceso que se usan en este tutorial suponen que el SDK de Windows 7 y el paquete de las API de Microsoft NLS Downlevel se instalaron en sus directorios predeterminados.</span><span class="sxs-lookup"><span data-stu-id="67bfa-393">The paths used in this tutorial assume that the Windows 7 SDK and the Microsoft NLS downlevel APIs package were installed to their default directories.</span></span> <span data-ttu-id="67bfa-394">Si no es así, modifique las rutas de acceso de forma adecuada.</span><span class="sxs-lookup"><span data-stu-id="67bfa-394">If that is not the case, modify the paths appropriately.</span></span>

     

    1.  <span data-ttu-id="67bfa-395">En el Explorador de soluciones, haga clic con el botón derecho en el proyecto GuiStep \_ 3 y seleccione establecer como proyecto de inicio.</span><span class="sxs-lookup"><span data-stu-id="67bfa-395">In the Solution Explorer, right-click the project GuiStep\_3 and select Set as StartUp Project.</span></span>
    2.  <span data-ttu-id="67bfa-396">Vuelva a hacer clic con el botón secundario y seleccione Propiedades.</span><span class="sxs-lookup"><span data-stu-id="67bfa-396">Right-click it again and select Properties.</span></span>
    3.  <span data-ttu-id="67bfa-397">En el cuadro de diálogo páginas de propiedades del proyecto:</span><span class="sxs-lookup"><span data-stu-id="67bfa-397">In the project's Property Pages dialog box:</span></span>

        1.  <span data-ttu-id="67bfa-398">En la lista desplegable superior izquierda, establezca configuración en todas las configuraciones.</span><span class="sxs-lookup"><span data-stu-id="67bfa-398">In the top left drop-down, set Configuration to All Configurations.</span></span>
        2.  <span data-ttu-id="67bfa-399">En propiedades de configuración, expanda C/C++, seleccione generación de código y establezca biblioteca en tiempo de ejecución: depuración multiproceso (/MTd).</span><span class="sxs-lookup"><span data-stu-id="67bfa-399">Under Configuration Properties expand C/C++, select Code Generation, and set Runtime Library: Multi-threaded Debug (/MTd).</span></span>
        3.  <span data-ttu-id="67bfa-400">Seleccione general y agregar a directorios de inclusión adicionales:</span><span class="sxs-lookup"><span data-stu-id="67bfa-400">Select General and add to Additional Include Directories:</span></span>

            -   <span data-ttu-id="67bfa-401">"C: las \\ API de Microsoft NLS Downlevel \\ incluyen".</span><span class="sxs-lookup"><span data-stu-id="67bfa-401">"C:\\Microsoft NLS Downlevel APIs\\Include".</span></span>

        4.  <span data-ttu-id="67bfa-402">Seleccione idioma y establezca tratar WCHAR \_ t como tipo integrado: no (/ZC: WCHAR \_ t-).</span><span class="sxs-lookup"><span data-stu-id="67bfa-402">Select Language and set Treat wchar\_t as Built-in Type: No (/Zc:wchar\_t-).</span></span>
        5.  <span data-ttu-id="67bfa-403">Seleccione avanzadas y establezca Convención de llamada: \_ Stdcall (/gz).</span><span class="sxs-lookup"><span data-stu-id="67bfa-403">Select Advanced and set Calling Convention: \_stdcall (/Gz).</span></span>
        6.  <span data-ttu-id="67bfa-404">En propiedades de configuración, expanda enlazador, seleccione entrada y agregue a dependencias adicionales:</span><span class="sxs-lookup"><span data-stu-id="67bfa-404">Under Configuration Properties expand Linker, select Input, and add to Additional Dependencies:</span></span>

            -   <span data-ttu-id="67bfa-405">"C: \\ archivos de programa \\ Microsoft SDK \\ Windows \\ v 7.0 \\ lib \\ MUILoad. lib".</span><span class="sxs-lookup"><span data-stu-id="67bfa-405">"C:\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Lib\\MUILoad.lib".</span></span>
            -   <span data-ttu-id="67bfa-406">"C: \\ Microsoft NLS Downlevel API \\ lib \\ x86 \\ nlsdl. lib".</span><span class="sxs-lookup"><span data-stu-id="67bfa-406">"C:\\Microsoft NLS Downlevel APIs\\Lib\\x86\\Nlsdl.lib".</span></span>

3.  <span data-ttu-id="67bfa-407">Reemplace el contenido de GuiStep \_ 3. cpp por el código siguiente:</span><span class="sxs-lookup"><span data-stu-id="67bfa-407">Replace the contents of GuiStep\_3.cpp with the following code:</span></span>
    ```C++
    // GuiStep_3.cpp : Defines the entry point for the application.
    //

    #include "stdafx.h"
    #include "GuiStep_3.h"
    #include <strsafe.h>
    #include <Nlsdl.h>
    #include <MUILoad.h>
    #include "..\HelloModule_en_us\resource.h"

    #define SUFFICIENTLY_LARGE_STRING_BUFFER (MAX_PATH*2)
    #define USER_CONFIGURATION_STRING_BUFFER (((LOCALE_NAME_MAX_LENGTH+1)*5)+1)
    #define SUFFICIENTLY_LARGE_ERROR_BUFFER (1024*2)
    #define HELLO_MODULE_CONTRIVED_FILE_PATH  (L"HelloModule.dll")

    BOOL GetMyUserDefinedLanguages(WCHAR * langStr, DWORD langStrSize);
    BOOL ConvertMyLangStrToMultiLangStr(WCHAR * langStr, WCHAR * langMultiStr, DWORD langMultiStrSize);

    int WINAPI WinMain(HINSTANCE hInstance, HINSTANCE hPrevInstance, LPSTR lpCmdLine, int nCmdShow)
    {
        UNREFERENCED_PARAMETER(hInstance);
        UNREFERENCED_PARAMETER(hPrevInstance);
        UNREFERENCED_PARAMETER(lpCmdLine);
        UNREFERENCED_PARAMETER(nCmdShow);

        // The following code presents a hypothetical, yet common use pattern of MUI technology
        WCHAR displayBuffer[SUFFICIENTLY_LARGE_ERROR_BUFFER];

        // 1. Application starts by applying any user defined language preferences
        // (language setting is potentially optional for an application that wishes to strictly use OS system language fallback)
        // 1a. Application looks in pre-defined location for user preferences (registry, file, web, etc.)
        WCHAR userLanguagesString[USER_CONFIGURATION_STRING_BUFFER*2];
        if(!GetMyUserDefinedLanguages(userLanguagesString,USER_CONFIGURATION_STRING_BUFFER*2))
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to find the user defined language configuration, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            return 1; // exit
        }
        // 1b. Application converts the user defined 'readable' languages to the proper multi-string 'less readable' language name format
        WCHAR userLanguagesMultiString[USER_CONFIGURATION_STRING_BUFFER];
        if(!ConvertMyLangStrToMultiLangStr(userLanguagesString,userLanguagesMultiString,USER_CONFIGURATION_STRING_BUFFER))
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to convert the user defined language configuration to multi-string, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            return 1; // exit
        }
        // 1c. Application now attempts to set the fallback list - this is much different for a down-level 
        // shipping application when compared to a Windows Vista or Windows 7 only shipping application    
        BOOL setSuccess = FALSE;
        DWORD setLangCount = 0;
        HMODULE hDLL = GetModuleHandleW(L"kernel32.dll");
        if( hDLL )
        {
            typedef BOOL (* SET_PREFERRED_UI_LANGUAGES_PROTOTYPE ) ( DWORD, PCWSTR, PULONG );
            SET_PREFERRED_UI_LANGUAGES_PROTOTYPE fp_SetPreferredUILanguages = (SET_PREFERRED_UI_LANGUAGES_PROTOTYPE)NULL;
            fp_SetPreferredUILanguages = (SET_PREFERRED_UI_LANGUAGES_PROTOTYPE) GetProcAddress(hDLL,"SetProcessPreferredUILanguages");
            if( fp_SetPreferredUILanguages )
            {
                // call SetProcessPreferredUILanguages if it is available in Kernel32.dll's export table - Windows 7 and later
                setSuccess = fp_SetPreferredUILanguages(MUI_LANGUAGE_NAME,userLanguagesMultiString,&setLangCount);
            }
            else
            {
                fp_SetPreferredUILanguages = (SET_PREFERRED_UI_LANGUAGES_PROTOTYPE) GetProcAddress(hDLL,"SetThreadPreferredUILanguages");
                // call SetThreadPreferredUILanguages if it is available in Kernel32.dll's export table - Windows Vista and later
                if(fp_SetPreferredUILanguages)
                    setSuccess = fp_SetPreferredUILanguages(MUI_LANGUAGE_NAME,userLanguagesMultiString,&setLangCount);
            }
        }

        // 2. Application obtains access to the proper resource container 
        // for standard Win32 resource loading this is normally a PE module
        // LoadMUILibrary is the preferred alternative for loading of resource modules
        // when the application is potentially run on OS versions prior to Windows Vista
        // LoadMUILibrary is available via Windows SDK releases in Windows Vista and later
        // When available, it is advised to get the most up-to-date Windows SDK (e.g., Windows 7)
        HMODULE resContainer = NULL;
        if(setSuccess) // Windows Vista and later OS scenario
        {
            resContainer = LoadMUILibraryW(HELLO_MODULE_CONTRIVED_FILE_PATH,MUI_LANGUAGE_NAME,0);
        }
        else // this block should only be hit on Windows XP and earlier OS platforms as setSuccess will be TRUE on Windows Vista and later
        {
            // need to provide your own fallback mechanism such as the implementation below
            // in essence the application will iterate through the user configured language list
            WCHAR * next = userLanguagesMultiString;
            while(!resContainer && *next != L'\0')
            {
                // convert the language name to an appropriate LCID
                // DownlevelLocaleNameToLCID is available via standalone download package 
                // and is contained in Nlsdl.h / Nlsdl.lib
                LCID nextLcid = DownlevelLocaleNameToLCID(next,DOWNLEVEL_LOCALE_NAME);
                // then have LoadMUILibrary attempt to probe for the right .mui module
                resContainer = LoadMUILibraryW(HELLO_MODULE_CONTRIVED_FILE_PATH,MUI_LANGUAGE_NAME,(LANGID)nextLcid);
                // increment to the next language name in our list
                size_t nextStrLen = 0;
                if(SUCCEEDED(StringCchLengthW(next,LOCALE_NAME_MAX_LENGTH,&nextStrLen)))
                    next += (nextStrLen + 1);
                else
                    break; // string is invalid - need to exit
            }
            // if the user configured list did not locate a module then try the languages associated with the system
            if(!resContainer)
                resContainer = LoadMUILibraryW(HELLO_MODULE_CONTRIVED_FILE_PATH,MUI_LANGUAGE_NAME,0);
        }
        if(!resContainer)
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to load the resource container module, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            return 1; // exit
        }

        // 3. Application parses the resource container to find the appropriate item
        WCHAR szHello[SUFFICIENTLY_LARGE_STRING_BUFFER];
        if(LoadStringW(resContainer,HELLO_MUI_STR_0,szHello,SUFFICIENTLY_LARGE_STRING_BUFFER) == 0)
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to load the resource string, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            FreeLibrary(resContainer);
            return 1; // exit
        }

        // 4. Application presents the discovered resource to the user via UI
        swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"%s MUI",szHello);
        MessageBoxW(NULL,displayBuffer,L"HelloMUI",MB_OK | MB_ICONINFORMATION);

        // 5. Application cleans up memory associated with the resource container after this item is no longer needed.
        if(!FreeMUILibrary(resContainer))
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to unload the resource container, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            return 1; // exit
        }

        return 0;
    }

    BOOL GetMyUserDefinedLanguages(WCHAR * langStr, DWORD langStrSize)
    {
        BOOL rtnVal = FALSE;
        // very simple implementation - assumes that first 'langStrSize' characters of the 
        // L".\\langs.txt" file comprises a string of one or more languages
        HANDLE langConfigFileHandle = CreateFileW(L".\\langs.txt", GENERIC_READ, 0, 
            NULL, OPEN_EXISTING, FILE_ATTRIBUTE_NORMAL, NULL);
        if(langConfigFileHandle != INVALID_HANDLE_VALUE)
        {
            // clear out the input variables
            DWORD bytesActuallyRead = 0;
            if(ReadFile(langConfigFileHandle,langStr,langStrSize*sizeof(WCHAR),&bytesActuallyRead,NULL) && bytesActuallyRead > 0)
            {
                rtnVal = TRUE;
                DWORD nullIndex = (bytesActuallyRead/sizeof(WCHAR) < langStrSize) ? bytesActuallyRead/sizeof(WCHAR) : langStrSize;
                langStr[nullIndex] = L'\0';
            }
            CloseHandle(langConfigFileHandle);
        }
        return rtnVal;
    }
    BOOL ConvertMyLangStrToMultiLangStr(WCHAR * langStr, WCHAR * langMultiStr, DWORD langMultiStrSize)
    {
        BOOL rtnVal = FALSE;
        size_t strLen = 0;
        rtnVal = SUCCEEDED(StringCchLengthW(langStr,USER_CONFIGURATION_STRING_BUFFER*2,&strLen));
        if(rtnVal && strLen > 0 && langMultiStr && langMultiStrSize > 0)
        {
            WCHAR * langMultiStrPtr = langMultiStr;
            WCHAR * last = langStr + (langStr[0] == 0xFEFF ? 1 : 0);
            WCHAR * context = last;
            WCHAR * next = wcstok_s(last,L",; :",&context);
            while(next && rtnVal)
            {
                // make sure you validate the user input
                if(SUCCEEDED(StringCchLengthW(last,LOCALE_NAME_MAX_LENGTH,&strLen)) 
                    && DownlevelLocaleNameToLCID(next,0) != 0)
                {
                    langMultiStrPtr[0] = L'\0';
                    rtnVal &= SUCCEEDED(StringCchCatW(langMultiStrPtr,(langMultiStrSize - (langMultiStrPtr - langMultiStr)),next));
                    langMultiStrPtr += strLen + 1;
                }
                next = wcstok_s(NULL,L",; :",&context);
                if(next)
                    last = next;
            }
            if(rtnVal && (langMultiStrSize - (langMultiStrPtr - langMultiStr))) // make sure there is a double null term for the multi-string 
            {
                langMultiStrPtr[0] = L'\0';
            }
            else // fail and guard anyone whom might use the multi-string
            {
                langMultiStr[0] = L'\0';
                langMultiStr[1] = L'\0';
            }
        }
        return rtnVal;
    }
    ```

    

4.  <span data-ttu-id="67bfa-408">Cree o copie langs.txt en el directorio adecuado, tal y como se describe anteriormente en el [paso 4: globalizar "Hello mui"](#step-4-globalizing-hello-mui).</span><span class="sxs-lookup"><span data-stu-id="67bfa-408">Create or copy langs.txt to the appropriate directory, as previously described in [Step 4: Globalizing "Hello MUI"](#step-4-globalizing-hello-mui).</span></span>
5.  <span data-ttu-id="67bfa-409">Compile y ejecute el proyecto.</span><span class="sxs-lookup"><span data-stu-id="67bfa-409">Build and run the project.</span></span>

> [!Note]  
> <span data-ttu-id="67bfa-410">Si la aplicación se debe ejecutar en versiones de Windows anteriores a Windows Vista, asegúrese de leer los documentos que se incluían con el paquete de las [API de Microsoft NLS de nivel inferior](https://www.microsoft.com/downloads/details.aspx?FamilyID=eb72cda0-834e-4c35-9419-ff14bc349c9d&amp;DisplayLang=en) sobre cómo redistribuir Nlsdl.dll.</span><span class="sxs-lookup"><span data-stu-id="67bfa-410">If the application should run on Windows versions prior to Windows Vista, be sure to read the documents that came with the [Microsoft NLS downlevel APIs](https://www.microsoft.com/downloads/details.aspx?FamilyID=eb72cda0-834e-4c35-9419-ff14bc349c9d&amp;DisplayLang=en) package on how to redistribute Nlsdl.dll.</span></span>

 

## <a name="additional-considerations-for-mui"></a><span data-ttu-id="67bfa-411">Consideraciones adicionales para MUI</span><span class="sxs-lookup"><span data-stu-id="67bfa-411">Additional Considerations for MUI</span></span>

### <a name="support-for-console-applications"></a><span data-ttu-id="67bfa-412">Compatibilidad con aplicaciones de consola</span><span class="sxs-lookup"><span data-stu-id="67bfa-412">Support for Console Applications</span></span>

<span data-ttu-id="67bfa-413">Las técnicas que se describen en este tutorial también se pueden usar en aplicaciones de consola.</span><span class="sxs-lookup"><span data-stu-id="67bfa-413">The techniques covered in this tutorial can also be used in console applications.</span></span> <span data-ttu-id="67bfa-414">Sin embargo, a diferencia de la mayoría de los controles estándar de la interfaz gráfica de usuario, la ventana comandos de Windows no puede mostrar caracteres para todos los idiomas.</span><span class="sxs-lookup"><span data-stu-id="67bfa-414">However, unlike most standard GUI controls, the Windows command window cannot display characters for all languages.</span></span> <span data-ttu-id="67bfa-415">Por este motivo, las aplicaciones de consola multilingüe requieren atención especial.</span><span class="sxs-lookup"><span data-stu-id="67bfa-415">For this reason, multilingual console applications require special attention.</span></span>

<span data-ttu-id="67bfa-416">La llamada a las API [**SetThreadUILanguage**](/windows/desktop/api/Winnls/nf-winnls-setthreaduilanguage) o [**SetThreadPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-setthreadpreferreduilanguages) con marcas de filtrado específicas hace que las funciones de carga de recursos quiten los sondeos de recursos de idioma para los idiomas específicos que normalmente no se muestran en una ventana de comandos.</span><span class="sxs-lookup"><span data-stu-id="67bfa-416">Calling the APIs [**SetThreadUILanguage**](/windows/desktop/api/Winnls/nf-winnls-setthreaduilanguage) or [**SetThreadPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-setthreadpreferreduilanguages) with specific filtering flags causes the resource loading functions to remove language resource probes for specific languages that are not normally displayed within a command window.</span></span> <span data-ttu-id="67bfa-417">Cuando se establecen estas marcas, los algoritmos de configuración de lenguaje solo permiten que los idiomas que se mostrarán correctamente en la ventana de comandos estén en la lista de reserva.</span><span class="sxs-lookup"><span data-stu-id="67bfa-417">When these flags are set, the language-setting algorithms allow only those languages that will display properly in the command window to be on the fallback list.</span></span>

<span data-ttu-id="67bfa-418">Para obtener más información sobre el uso de estas API para compilar una aplicación de consola multilingüe, vea las secciones comentarios de [**SetThreadUILanguage**](/windows/desktop/api/Winnls/nf-winnls-setthreaduilanguage) y [**SetThreadPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-setthreadpreferreduilanguages).</span><span class="sxs-lookup"><span data-stu-id="67bfa-418">For more information on using these APIs to build a multilingual console application, see the remarks sections of [**SetThreadUILanguage**](/windows/desktop/api/Winnls/nf-winnls-setthreaduilanguage) and [**SetThreadPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-setthreadpreferreduilanguages).</span></span>

### <a name="determination-of-languages-to-support-at-run-time"></a><span data-ttu-id="67bfa-419">Determinación de los idiomas que se admiten en Run-Time</span><span class="sxs-lookup"><span data-stu-id="67bfa-419">Determination of Languages to Support at Run-Time</span></span>

<span data-ttu-id="67bfa-420">Puede adoptar una de las siguientes sugerencias de diseño para determinar qué idiomas debe admitir la aplicación en tiempo de ejecución:</span><span class="sxs-lookup"><span data-stu-id="67bfa-420">You can adopt one of the following design suggestions to determine which languages your application should support at run-time:</span></span>

-   <span data-ttu-id="67bfa-421">**Durante la instalación, permita que el usuario final Seleccione el idioma preferido en la lista de idiomas admitidos.**</span><span class="sxs-lookup"><span data-stu-id="67bfa-421">**During installation, enable the end user to select the preferred language from a list of supported languages**</span></span>

-   <span data-ttu-id="67bfa-422">**Leer una lista de idiomas de un archivo de configuración**</span><span class="sxs-lookup"><span data-stu-id="67bfa-422">**Read a language list from a configuration file**</span></span>

    <span data-ttu-id="67bfa-423">Algunos de los proyectos de este tutorial contienen una función que se usa para analizar un archivo de configuración de langs.txt, que contiene una lista de idiomas.</span><span class="sxs-lookup"><span data-stu-id="67bfa-423">Some of the projects in this tutorial contain a function used to parse a langs.txt configuration file, which contains a language list.</span></span>

    <span data-ttu-id="67bfa-424">Dado que esta función toma una entrada externa, valide los idiomas que se proporcionan como entrada.</span><span class="sxs-lookup"><span data-stu-id="67bfa-424">Because this function takes external input, validate the languages that are provided as input.</span></span> <span data-ttu-id="67bfa-425">Vea las funciones [**IsValidLocaleName**](/windows/desktop/api/Winnls/nf-winnls-isvalidlocalename) o [**DownLevelLocaleNameToLCID**](downlevellocalenametolcid.md) para obtener más información sobre cómo realizar esa validación.</span><span class="sxs-lookup"><span data-stu-id="67bfa-425">See the [**IsValidLocaleName**](/windows/desktop/api/Winnls/nf-winnls-isvalidlocalename) or [**DownLevelLocaleNameToLCID**](downlevellocalenametolcid.md) functions for more details on performing that validation.</span></span>

-   <span data-ttu-id="67bfa-426">**Consultar el sistema operativo para determinar qué idiomas están instalados**</span><span class="sxs-lookup"><span data-stu-id="67bfa-426">**Query the operating system to determine which languages are installed**</span></span>

    <span data-ttu-id="67bfa-427">Este enfoque ayuda a la aplicación a usar el mismo idioma que el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="67bfa-427">This approach helps the application use the same language as the operating system.</span></span> <span data-ttu-id="67bfa-428">Aunque esto no requiere la solicitud del usuario, si elige esta opción, tenga en cuenta que los idiomas del sistema operativo se pueden agregar o quitar en cualquier momento y pueden cambiar después de que el usuario instale la aplicación.</span><span class="sxs-lookup"><span data-stu-id="67bfa-428">Although this does not require user prompting, if you choose this option, be aware that operating system languages can be added or removed at any time and can change after the user installs the application.</span></span> <span data-ttu-id="67bfa-429">Además, tenga en cuenta que, en algunos casos, el sistema operativo se instala con compatibilidad de idioma limitado y la aplicación ofrece más valor si es compatible con los idiomas que el sistema operativo no admite.</span><span class="sxs-lookup"><span data-stu-id="67bfa-429">Also, be aware that in some cases, the operating system is installed with limited language support, and the application offers more value if it supports languages that the operating system does not support.</span></span>

    <span data-ttu-id="67bfa-430">Para obtener más información sobre cómo determinar los idiomas instalados actualmente en el sistema operativo, consulte la función [**EnumUILanguages**](/windows/desktop/api/Winnls/nf-winnls-enumuilanguagesa) .</span><span class="sxs-lookup"><span data-stu-id="67bfa-430">For more information on how to determine the currently installed languages in the operating system, see the [**EnumUILanguages**](/windows/desktop/api/Winnls/nf-winnls-enumuilanguagesa) function.</span></span>

### <a name="complex-script-support-in-versions-prior-to-windows-vista"></a><span data-ttu-id="67bfa-431">Compatibilidad con scripts complejos en versiones anteriores a Windows Vista</span><span class="sxs-lookup"><span data-stu-id="67bfa-431">Complex Script Support in Versions Prior to Windows Vista</span></span>

<span data-ttu-id="67bfa-432">Cuando una aplicación que admite determinados scripts complejos se ejecuta en una versión de Windows anterior a Windows Vista, es posible que el texto de ese script no se muestre correctamente en los componentes de la GUI.</span><span class="sxs-lookup"><span data-stu-id="67bfa-432">When an application that supports certain complex scripts runs on a version of Windows prior to Windows Vista, text in that script may not display properly in GUI components.</span></span> <span data-ttu-id="67bfa-433">Por ejemplo, en el proyecto de nivel inferior de este tutorial, es posible que no se muestren los scripts de alta y escritura en el cuadro de mensaje debido a problemas con el procesamiento de scripts complejos y la falta de fuentes relacionadas.</span><span class="sxs-lookup"><span data-stu-id="67bfa-433">For example, in the downlevel project within this tutorial, hi-IN and ta-IN scripts may not display in the message box due to issues with processing complex scripts and the lack of related fonts.</span></span> <span data-ttu-id="67bfa-434">Normalmente, los problemas de esta naturaleza aparecen como cuadros cuadrados en el componente GUI.</span><span class="sxs-lookup"><span data-stu-id="67bfa-434">Normally, problems of this nature present themselves as square boxes in the GUI component.</span></span>

<span data-ttu-id="67bfa-435">Puede encontrar más información sobre cómo habilitar el procesamiento complejo de scripts en [compatibilidad con scripts y fuentes en Windows](https://msdn.microsoft.com/goglobal/bb688099.aspx).</span><span class="sxs-lookup"><span data-stu-id="67bfa-435">More information about how to enable complex script processing can be found at [Script and Font Support in Windows](https://msdn.microsoft.com/goglobal/bb688099.aspx).</span></span>

## <a name="summary"></a><span data-ttu-id="67bfa-436">Resumen</span><span class="sxs-lookup"><span data-stu-id="67bfa-436">Summary</span></span>

<span data-ttu-id="67bfa-437">En este tutorial se ha globalizado una aplicación Monolingual y se han mostrado las siguientes prácticas recomendadas.</span><span class="sxs-lookup"><span data-stu-id="67bfa-437">This tutorial globalized a monolingual application and demonstrated the following best practices.</span></span>

-   <span data-ttu-id="67bfa-438">Diseñe la aplicación para aprovechar las ventajas del modelo de recursos de Win32.</span><span class="sxs-lookup"><span data-stu-id="67bfa-438">Design the application to take advantage of the Win32 resource model.</span></span>
-   <span data-ttu-id="67bfa-439">Use la división de los recursos de MUI en binarios satélite (archivos. MUI).</span><span class="sxs-lookup"><span data-stu-id="67bfa-439">Utilize MUI splitting of resources into satellite binaries (.mui files).</span></span>
-   <span data-ttu-id="67bfa-440">Asegúrese de que el proceso de localización actualiza los recursos de los archivos. MUI para que sean adecuados para el idioma de destino.</span><span class="sxs-lookup"><span data-stu-id="67bfa-440">Ensure that the localization process updates the resources in the .mui files to be appropriate for the target language.</span></span>
-   <span data-ttu-id="67bfa-441">Asegúrese de que el empaquetado y la implementación de la aplicación, los archivos. mui asociados y el contenido de configuración se realizan correctamente para permitir que las API de carga de recursos encuentren el contenido localizado.</span><span class="sxs-lookup"><span data-stu-id="67bfa-441">Ensure that packaging and deployment of the application, associated .mui files, and configuration content is done correctly to allow the resource loading APIs to find the localized content.</span></span>
-   <span data-ttu-id="67bfa-442">Proporcionar al usuario final un mecanismo para ajustar la configuración de idioma de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="67bfa-442">Provide the end user a mechanism to adjust the language configuration of the application.</span></span>
-   <span data-ttu-id="67bfa-443">Ajuste el código en tiempo de ejecución para aprovechar las ventajas de la configuración de idioma para que la aplicación responda mejor a las necesidades de los usuarios finales.</span><span class="sxs-lookup"><span data-stu-id="67bfa-443">Adjust the run-time code to take advantage of language configuration, to make the application more responsive to end user needs.</span></span>

 

 
