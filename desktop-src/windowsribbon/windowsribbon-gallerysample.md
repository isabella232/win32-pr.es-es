---
title: Ejemplo de galería
description: En este ejemplo de código se muestra el marcado y el código necesarios para usar los distintos tipos de controles de galería incluidos en el marco de Windows cinta de opciones.
ms.assetid: 1a462f4e-e75a-40cf-9c52-0bad0a645d57
ms.topic: article
ms.date: 07/13/2021
ms.openlocfilehash: ef776a8a1a8eadf9ee41cf9964066cc612a9f9a1
ms.sourcegitcommit: 63c93e0ad0b48d60b11008767196718feb475cb0
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/13/2021
ms.locfileid: "113691754"
---
# <a name="gallery-sample"></a><span data-ttu-id="02a20-103">Ejemplo de galería</span><span class="sxs-lookup"><span data-stu-id="02a20-103">Gallery Sample</span></span>

<span data-ttu-id="02a20-104">En este ejemplo de código se muestra el marcado y el código necesarios para usar los distintos tipos de controles de galería incluidos en el marco de Windows cinta de opciones.</span><span class="sxs-lookup"><span data-stu-id="02a20-104">This code sample demonstrates the markup and code required to use the different types of Gallery controls included in the Windows Ribbon framework.</span></span> <span data-ttu-id="02a20-105">El ejemplo incluye código que se puede usar para rellenar dinámicamente elementos en las galerías y controlar eventos de vista previa de la Galería especiales que admiten la interfaz de usuario orientada a resultados.</span><span class="sxs-lookup"><span data-stu-id="02a20-105">The sample includes code that can be used to dynamically populate items into the Galleries, and handle special Gallery previewing events that support results-oriented UI.</span></span>

- [<span data-ttu-id="02a20-106">Uso</span><span class="sxs-lookup"><span data-stu-id="02a20-106">Usage</span></span>](#usage)
  - [<span data-ttu-id="02a20-107">Compilar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="02a20-107">Building the Sample</span></span>](#building-the-sample)
  - [<span data-ttu-id="02a20-108">Ejecución del ejemplo</span><span class="sxs-lookup"><span data-stu-id="02a20-108">Running the Sample</span></span>](#running-the-sample)
- [<span data-ttu-id="02a20-109">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="02a20-109">Support</span></span>](#support)
- [<span data-ttu-id="02a20-110">Requisitos mínimos</span><span class="sxs-lookup"><span data-stu-id="02a20-110">Minimum Requirements</span></span>](#minimum-requirements)
- [<span data-ttu-id="02a20-111">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="02a20-111">Related topics</span></span>](#related-topics)

## <a name="usage"></a><span data-ttu-id="02a20-112">Uso</span><span class="sxs-lookup"><span data-stu-id="02a20-112">Usage</span></span>

<span data-ttu-id="02a20-113">Los ejemplos Windows marco de la cinta de opciones se pueden descargar como proyectos de Microsoft Visual Studio independientes desde el Centro de descarga de [Microsoft](https://www.microsoft.com/download/details.aspx?id=9620) o instalarse como parte del Kit de desarrollo de [software (SDK)](https://developer.microsoft.com/windows/downloads/sdk-archive/)de Windows .</span><span class="sxs-lookup"><span data-stu-id="02a20-113">The Windows Ribbon framework samples can be downloaded as standalone Microsoft Visual Studio projects from the [Microsoft Download Center](https://www.microsoft.com/download/details.aspx?id=9620) or installed as part of the [Windows Software Development Kit (SDK)](https://developer.microsoft.com/windows/downloads/sdk-archive/).</span></span>

- <span data-ttu-id="02a20-114">Windows Kit de desarrollo de software (SDK) (ruta de instalación estándar): %ProgramFiles% SDK de Microsoft Windows número de versión \\ \\ Ejemplos \\ \[ \] \\ \\ winui \\ WindowsRibbon \\ Gallery</span><span class="sxs-lookup"><span data-stu-id="02a20-114">Windows Software Development Kit (SDK) (standard installation path): %ProgramFiles%\\Microsoft SDKs\\Windows\\\[version number\]\\Samples\\winui\\WindowsRibbon\\Gallery</span></span>

### <a name="building-the-sample"></a><span data-ttu-id="02a20-115">Generar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="02a20-115">Building the Sample</span></span>

<span data-ttu-id="02a20-116">Descargue el ejemplo.</span><span class="sxs-lookup"><span data-stu-id="02a20-116">Download the sample.</span></span>

<span data-ttu-id="02a20-117">Instale el SDK Windows para Windows 7 y abra su ventana de comandos del entorno de compilación.</span><span class="sxs-lookup"><span data-stu-id="02a20-117">Install the Windows SDK for Windows 7 and open its build environment command window.</span></span> <span data-ttu-id="02a20-118">En el menú Inicio, elija Todos los programas, Microsoft Windows SDK y haga clic en Shell CMD.</span><span class="sxs-lookup"><span data-stu-id="02a20-118">On the Start menu, point to All Programs, Microsoft Windows SDK, and then click CMD Shell.</span></span>

<span data-ttu-id="02a20-119">Para generar el ejemplo en la ventana de comados del entorno de compilación, vaya al directorio de origen del ejemplo.</span><span class="sxs-lookup"><span data-stu-id="02a20-119">To build the sample from the build environment command window, go to the source directory of the sample.</span></span> <span data-ttu-id="02a20-120">En el símbolo del sistema, escriba MSBUILD.</span><span class="sxs-lookup"><span data-stu-id="02a20-120">At the command prompt, type MSBUILD.</span></span>

<span data-ttu-id="02a20-121">Para compilar el ejemplo en Microsoft Visual Studio, cargue la solución de ejemplo o el archivo del proyecto y presione CTRL+MAYÚS+B.</span><span class="sxs-lookup"><span data-stu-id="02a20-121">To build the sample in Microsoft Visual Studio, load the sample solution or project file and then press CTRL+SHIFT+B.</span></span>

### <a name="running-the-sample"></a><span data-ttu-id="02a20-122">Ejecutar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="02a20-122">Running the Sample</span></span>

<span data-ttu-id="02a20-123">Para ejecutar el ejemplo desde la ventana de comandos del entorno de compilación, ejecute los archivos .exe en la carpeta Bin Debug o Bin Release contenida en la carpeta \\ \\ de origen de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="02a20-123">To run the sample from the build environment command window, execute the .exe files in the Bin\\Debug or Bin\\Release folder contained in the sample source folder.</span></span>

<span data-ttu-id="02a20-124">Para ejecutar el ejemplo compilado con depuración en Visual Studio, presione F5.</span><span class="sxs-lookup"><span data-stu-id="02a20-124">To run the compiled sample with debugging in Visual Studio, press F5.</span></span>

## <a name="support"></a><span data-ttu-id="02a20-125">Compatibilidad</span><span class="sxs-lookup"><span data-stu-id="02a20-125">Support</span></span>

<span data-ttu-id="02a20-126">El [foro Windows desarrollo de la cinta](https://social.msdn.microsoft.com/Forums/windowsdesktop/home?forum=windowsribbondevelopment) de opciones está disponible para analizar temas y hacer preguntas relacionadas con el desarrollo de Windows de cinta de opciones.</span><span class="sxs-lookup"><span data-stu-id="02a20-126">The [Windows Ribbon Development Forum](https://social.msdn.microsoft.com/Forums/windowsdesktop/home?forum=windowsribbondevelopment) is available to discuss topics and ask questions related to developing Windows Ribbon applications.</span></span>

## <a name="minimum-requirements"></a><span data-ttu-id="02a20-127">Requisitos mínimos</span><span class="sxs-lookup"><span data-stu-id="02a20-127">Minimum Requirements</span></span>



| <span data-ttu-id="02a20-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="02a20-128">Requirement</span></span> | <span data-ttu-id="02a20-129">Valor</span><span class="sxs-lookup"><span data-stu-id="02a20-129">Value</span></span> |
|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="02a20-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="02a20-130">Minimum supported client</span></span> | <span data-ttu-id="02a20-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="02a20-131">Windows 7</span></span><br/> <span data-ttu-id="02a20-132">Windows Vista con Service Pack 2 (SP2) y [actualización de plataforma para Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx)</span><span class="sxs-lookup"><span data-stu-id="02a20-132">Windows Vista with Service Pack 2 (SP2) and [Platform Update for Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx)</span></span><br/>         |
| <span data-ttu-id="02a20-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="02a20-133">Minimum supported server</span></span> | <span data-ttu-id="02a20-134">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="02a20-134">Windows Server 2008 R2</span></span><br/> <span data-ttu-id="02a20-135">Windows Server 2008 con SP2 y actualización de plataforma [para Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx)</span><span class="sxs-lookup"><span data-stu-id="02a20-135">Windows Server 2008 with SP2 and [Platform Update for Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx)</span></span><br/> |
| <span data-ttu-id="02a20-136">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="02a20-136">Windows SDK</span></span>              | <span data-ttu-id="02a20-137">7.0</span><span class="sxs-lookup"><span data-stu-id="02a20-137">7.0</span></span>                                                                                                                                                                      |
| <span data-ttu-id="02a20-138">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="02a20-138">Visual Studio</span></span>            | <span data-ttu-id="02a20-139">2008</span><span class="sxs-lookup"><span data-stu-id="02a20-139">2008</span></span>                                                                                                                                                                     |
| <span data-ttu-id="02a20-140">Archivos de encabezado e IDL</span><span class="sxs-lookup"><span data-stu-id="02a20-140">Header and IDL files</span></span>     | <span data-ttu-id="02a20-141">uiribbon.h, uiribbon.idl</span><span class="sxs-lookup"><span data-stu-id="02a20-141">uiribbon.h, uiribbon.idl</span></span>                                                                                                                                                 |



 

> [!Note]  
> <span data-ttu-id="02a20-142">La actualización de plataforma para [Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) y la actualización de plataforma para Windows [Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) son conjuntos de bibliotecas en tiempo de ejecución que permiten a los desarrolladores dirigir aplicaciones de la cinta de opciones de Windows a Windows Vista y Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="02a20-142">The [Platform Update for Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) and [Platform Update for Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) are sets of run-time libraries that enable developers to target Windows Ribbon applications to both Windows Vista and Windows Server 2008.</span></span> <span data-ttu-id="02a20-143">Las actualizaciones de la plataforma estarán disponibles para todos los Windows Vista y Windows Server 2008 a través de Windows Update.</span><span class="sxs-lookup"><span data-stu-id="02a20-143">The platform updates will be available to all Windows Vista and Windows Server 2008 customers through Windows Update.</span></span> <span data-ttu-id="02a20-144">Las aplicaciones de terceros que requieren Actualización de plataforma para [Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) o Actualización de plataforma para Windows [Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) pueden hacer que Windows Update detecte si está instalada la actualización necesaria; Si no es así, Windows Update la descargará e instalará en segundo plano.</span><span class="sxs-lookup"><span data-stu-id="02a20-144">Third-party applications that require [Platform Update for Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) or [Platform Update for Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) can have Windows Update detect whether the required updated is installed; if it is not, Windows Update will download and install it in the background.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="02a20-145">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="02a20-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="02a20-146">Trabajar con galerías</span><span class="sxs-lookup"><span data-stu-id="02a20-146">Working with Galleries</span></span>](ribbon-controls-galleries.md)
</dt> <dt>

[<span data-ttu-id="02a20-147">Cuadro combinado</span><span class="sxs-lookup"><span data-stu-id="02a20-147">Combo Box</span></span>](windowsribbon-controls-combobox.md)
</dt> <dt>

[<span data-ttu-id="02a20-148">Galería desplegable</span><span class="sxs-lookup"><span data-stu-id="02a20-148">Drop-Down Gallery</span></span>](windowsribbon-controls-dropdowngallery.md)
</dt> <dt>

[<span data-ttu-id="02a20-149">Galería en la cinta de opciones</span><span class="sxs-lookup"><span data-stu-id="02a20-149">In-Ribbon Gallery</span></span>](windowsribbon-controls-inribbongallery.md)
</dt> <dt>

[<span data-ttu-id="02a20-150">Galería de botones de división</span><span class="sxs-lookup"><span data-stu-id="02a20-150">Split Button Gallery</span></span>](windowsribbon-controls-splitbuttongallery.md)
</dt> <dt>

[<span data-ttu-id="02a20-151">Propiedades de la colección</span><span class="sxs-lookup"><span data-stu-id="02a20-151">Collection Properties</span></span>](windowsribbon-reference-properties-collection.md)
</dt> </dl>

 

 





