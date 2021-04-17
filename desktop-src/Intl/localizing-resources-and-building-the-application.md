---
description: En este tema se describe cómo compilar una aplicación de MUI típica.
ms.assetid: 386e9601-ce21-4ef0-b225-0c4249d1942d
title: Localizar recursos y compilar la aplicación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74262499b20836ee4860f1c0fc1a1bf80e19d58d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687096"
---
# <a name="localizing-resources-and-building-the-application"></a><span data-ttu-id="aa7f5-103">Localizar recursos y compilar la aplicación</span><span class="sxs-lookup"><span data-stu-id="aa7f5-103">Localizing Resources and Building the Application</span></span>

<span data-ttu-id="aa7f5-104">En este tema se describe cómo compilar una aplicación de MUI típica.</span><span class="sxs-lookup"><span data-stu-id="aa7f5-104">This topic describes how to build a typical MUI application.</span></span> <span data-ttu-id="aa7f5-105">Se supone que usa Microsoft Visual Studio para la codificación y Microsoft Visual Studio o la línea de comandos de Visual Studio para la compilación.</span><span class="sxs-lookup"><span data-stu-id="aa7f5-105">It is assumed that you are using Microsoft Visual Studio for coding and either Microsoft Visual Studio or the Visual Studio command line for building.</span></span> <span data-ttu-id="aa7f5-106">Se supone que usa un archivo de solución. sln para la aplicación y que admite un archivo resource. h para reflejar el archivo de recursos de idioma base.</span><span class="sxs-lookup"><span data-stu-id="aa7f5-106">You are assumed to use an .sln solution file for your application and support a Resource.h file to reflect the base language resource file.</span></span>

> [!Note]  
> <span data-ttu-id="aa7f5-107">Si usa la línea de comandos de Visual Studio para la compilación, usará el comando **VCBUILD** para compilar el archivo de solución.</span><span class="sxs-lookup"><span data-stu-id="aa7f5-107">If using the Visual Studio command line for the build, you will use the **vcbuild** command to build the solution file.</span></span>

 

<span data-ttu-id="aa7f5-108">Los archivos de aplicación se compilan por separado para cada idioma.</span><span class="sxs-lookup"><span data-stu-id="aa7f5-108">Application files are built separately for each language.</span></span> <span data-ttu-id="aa7f5-109">Cada compilación crea idénticos archivos. exe, independientes del lenguaje y específicos del lenguaje.</span><span class="sxs-lookup"><span data-stu-id="aa7f5-109">Each build creates identical language-neutral .exe and language-specific .exe.mui files.</span></span> <span data-ttu-id="aa7f5-110">Además, se copian varios archivos en las carpetas de versión correspondientes.</span><span class="sxs-lookup"><span data-stu-id="aa7f5-110">In addition, various other files are copied to the appropriate release folders.</span></span>

<span data-ttu-id="aa7f5-111">La compilación de la aplicación depende del tipo de recursos y del tipo de localización que esté usando.</span><span class="sxs-lookup"><span data-stu-id="aa7f5-111">The application build depends on the type of resources and the type of localization that you are using.</span></span> <span data-ttu-id="aa7f5-112">Para la localización anterior a la compilación, tiene una copia del archivo de idioma base localizado para cada idioma admitido.</span><span class="sxs-lookup"><span data-stu-id="aa7f5-112">For pre-build localization, you have one copy of the base language file localized for each supported language.</span></span> <span data-ttu-id="aa7f5-113">En la localización posterior a la compilación, puede copiar el archivo. mui resultante de la compilación del módulo ejecutable y de recursos, y proporcionar las copias a los localizadores.</span><span class="sxs-lookup"><span data-stu-id="aa7f5-113">For post-build localization, you can copy the .mui file resulting from the build of the executable and resource module, and provide the copies to the localizers.</span></span>

> [!Note]  
> <span data-ttu-id="aa7f5-114">En el procedimiento siguiente se presupone que los recursos de Win32 PE tienen un proyecto de Visual Studio creado para cada lenguaje.</span><span class="sxs-lookup"><span data-stu-id="aa7f5-114">The following procedure assumes Win32 PE resources with one Visual Studio project built for each language.</span></span> <span data-ttu-id="aa7f5-115">Los recursos de idioma base se proporcionan en un archivo. RC y se cargan mediante un módulo DLL.</span><span class="sxs-lookup"><span data-stu-id="aa7f5-115">The base language resources are provided in an .rc file and loaded using a DLL module.</span></span> <span data-ttu-id="aa7f5-116">Puede repetir el procedimiento según sea necesario para compilar para todos los idiomas admitidos.</span><span class="sxs-lookup"><span data-stu-id="aa7f5-116">You can repeat the procedure as needed to build for all languages supported.</span></span>

 

<span data-ttu-id="aa7f5-117">**Para compilar la aplicación**</span><span class="sxs-lookup"><span data-stu-id="aa7f5-117">**To build the application**</span></span>

1.  <span data-ttu-id="aa7f5-118">Configure un proyecto de Visual Studio para el idioma base.</span><span class="sxs-lookup"><span data-stu-id="aa7f5-118">Set up a Visual Studio project for the base language.</span></span>
2.  <span data-ttu-id="aa7f5-119">Si está interesado en usar un archivo de configuración de recursos con las herramientas de recursos, configure uno como se describe en [preparación de un archivo de configuración de recursos](preparing-a-resource-configuration-file.md).</span><span class="sxs-lookup"><span data-stu-id="aa7f5-119">If interested in using a resource configuration file with the resource tools, set one up as described in [Preparing a Resource Configuration File](preparing-a-resource-configuration-file.md).</span></span>
3.  <span data-ttu-id="aa7f5-120">Establezca los parámetros requeridos por la utilidad del compilador RC en las páginas de propiedades del proyecto, en **propiedades de configuración → recursos → línea de comandos → opciones adicionales**.</span><span class="sxs-lookup"><span data-stu-id="aa7f5-120">Set parameters required by the RC Compiler utility in the property pages for the project under **Configuration Properties → Resources → Command Line → Additional options**.</span></span>
4.  <span data-ttu-id="aa7f5-121">Ejecute el compilador RC.</span><span class="sxs-lookup"><span data-stu-id="aa7f5-121">Run RC Compiler.</span></span> <span data-ttu-id="aa7f5-122">La utilidad compila y divide los recursos no localizables y localizables en dos archivos de objeto diferentes, utilizando los datos de configuración de recursos.</span><span class="sxs-lookup"><span data-stu-id="aa7f5-122">The utility compiles and splits the non-localizable and localizable resources into two different object files, using resource configuration data.</span></span> <span data-ttu-id="aa7f5-123">En este paso, los recursos independientes del lenguaje están vinculados a un archivo LN.</span><span class="sxs-lookup"><span data-stu-id="aa7f5-123">In this step the language-neutral resources are linked into an LN file.</span></span> <span data-ttu-id="aa7f5-124">Para obtener más información, consulte la descripción de la utilidad en [Resource Utilities](resource-utilities.md).</span><span class="sxs-lookup"><span data-stu-id="aa7f5-124">For more information, see the utility description in [Resource Utilities](resource-utilities.md).</span></span>
5.  <span data-ttu-id="aa7f5-125">Para vincular los recursos específicos del idioma a un archivo. mui específico del idioma, establezca un evento posterior a la compilación para el proyecto en las páginas de propiedades de **propiedades de configuración → eventos de compilación → evento posterior a la compilación → línea de comandos**.</span><span class="sxs-lookup"><span data-stu-id="aa7f5-125">To link the language-specific resources into a language-specific .mui file, set a post-build event for the project in the property pages under **Configuration Properties → Build Events → Post-Build Event → Command Line**.</span></span>
6.  <span data-ttu-id="aa7f5-126">Establezca un evento posterior a la compilación para aplicar el valor de la suma de comprobación del archivo LN al archivo. mui correspondiente al idioma.</span><span class="sxs-lookup"><span data-stu-id="aa7f5-126">Set a post-build event to apply the checksum value from the LN file to the .mui file for the language.</span></span> <span data-ttu-id="aa7f5-127">Puede usar la utilidad MUIRCT para este paso.</span><span class="sxs-lookup"><span data-stu-id="aa7f5-127">You can use the MUIRCT utility for this step.</span></span> <span data-ttu-id="aa7f5-128">Para obtener más información, consulte la descripción de la utilidad en [Resource Utilities](resource-utilities.md).</span><span class="sxs-lookup"><span data-stu-id="aa7f5-128">For more information, see the utility description in [Resource Utilities](resource-utilities.md).</span></span>
7.  <span data-ttu-id="aa7f5-129">Use la línea de comandos del evento posterior a la compilación para agregar comandos para copiar los archivos en la estructura de carpetas de versión adecuada.</span><span class="sxs-lookup"><span data-stu-id="aa7f5-129">Use the post-build event command line to add commands to copy the files into the appropriate release folder structure.</span></span>

## <a name="related-topics"></a><span data-ttu-id="aa7f5-130">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="aa7f5-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aa7f5-131">Uso de la interfaz de usuario multilingüe</span><span class="sxs-lookup"><span data-stu-id="aa7f5-131">Using Multilingual User Interface</span></span>](using-multilingual-user-interface.md)
</dt> <dt>

[<span data-ttu-id="aa7f5-132">Preparación de un archivo de configuración de recursos</span><span class="sxs-lookup"><span data-stu-id="aa7f5-132">Preparing a Resource Configuration File</span></span>](preparing-a-resource-configuration-file.md)
</dt> <dt>

[<span data-ttu-id="aa7f5-133">Utilidades de recursos</span><span class="sxs-lookup"><span data-stu-id="aa7f5-133">Resource Utilities</span></span>](resource-utilities.md)
</dt> </dl>

 

 



