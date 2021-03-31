---
title: Ejemplo de la galería
description: En este ejemplo de código se muestra el marcado y el código necesarios para usar los distintos tipos de controles de Galería incluidos en el marco de cinta de Windows.
ms.assetid: 1a462f4e-e75a-40cf-9c52-0bad0a645d57
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5aacc52081fbcd2b6b58fd4c2439894705880d30
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150024"
---
# <a name="gallery-sample"></a><span data-ttu-id="40fb3-103">Ejemplo de la galería</span><span class="sxs-lookup"><span data-stu-id="40fb3-103">Gallery Sample</span></span>

<span data-ttu-id="40fb3-104">En este ejemplo de código se muestra el marcado y el código necesarios para usar los distintos tipos de controles de Galería incluidos en el marco de cinta de Windows.</span><span class="sxs-lookup"><span data-stu-id="40fb3-104">This code sample demonstrates the markup and code required to use the different types of Gallery controls included in the Windows Ribbon framework.</span></span> <span data-ttu-id="40fb3-105">En el ejemplo se incluye código que se puede usar para rellenar los elementos de forma dinámica en las galerías y controlar eventos especiales de vista previa de la galería que admiten la interfaz de usuario orientada a los resultados.</span><span class="sxs-lookup"><span data-stu-id="40fb3-105">The sample includes code that can be used to dynamically populate items into the Galleries, and handle special Gallery previewing events that support results-oriented UI.</span></span>

-   [<span data-ttu-id="40fb3-106">Uso</span><span class="sxs-lookup"><span data-stu-id="40fb3-106">Usage</span></span>](#usage)
    -   [<span data-ttu-id="40fb3-107">Compilar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="40fb3-107">Building the Sample</span></span>](#building-the-sample)
    -   [<span data-ttu-id="40fb3-108">Ejecutar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="40fb3-108">Running the Sample</span></span>](#running-the-sample)
-   [<span data-ttu-id="40fb3-109">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="40fb3-109">Support</span></span>](#support)
-   [<span data-ttu-id="40fb3-110">Requisitos mínimos</span><span class="sxs-lookup"><span data-stu-id="40fb3-110">Minimum Requirements</span></span>](#minimum-requirements)
-   [<span data-ttu-id="40fb3-111">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="40fb3-111">Related topics</span></span>](#related-topics)

## <a name="usage"></a><span data-ttu-id="40fb3-112">Uso</span><span class="sxs-lookup"><span data-stu-id="40fb3-112">Usage</span></span>

<span data-ttu-id="40fb3-113">El ejemplo de la galería de se puede descargar como un proyecto de Microsoft Visual Studio independiente desde el [centro de descarga de Microsoft](https://www.microsoft.com/DOWNLOADS/en/default.aspx) o instalarse como parte del kit de desarrollo de [software (SDK) de Windows](https://msdn.microsoft.com/windows/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="40fb3-113">The Gallery Sample can be downloaded as a standalone Microsoft Visual Studio project from the [Microsoft Download Center](https://www.microsoft.com/DOWNLOADS/en/default.aspx) or installed as part of the [Windows Software Development Kit (SDK)](https://msdn.microsoft.com/windows/bb980924.aspx).</span></span>

-   <span data-ttu-id="40fb3-114">Centro de descarga de Microsoft: [ejemplos de cinta de Windows](https://www.microsoft.com/downloads/details.aspx?familyid=141e13e8-b10b-4356-aaa5-609b2981574a&displaylang=en)</span><span class="sxs-lookup"><span data-stu-id="40fb3-114">Microsoft Download Center: [Windows Ribbon Samples](https://www.microsoft.com/downloads/details.aspx?familyid=141e13e8-b10b-4356-aaa5-609b2981574a&displaylang=en)</span></span>
-   <span data-ttu-id="40fb3-115">Kit de desarrollo de software (SDK) de Windows (ruta de instalación estándar):% ProgramFiles% \\ Microsoft SDKs \\ Windows \\ \[ número de versión de \] \\ ejemplo \\ WinUI \\ WindowsRibbon \\ Gallery</span><span class="sxs-lookup"><span data-stu-id="40fb3-115">Windows Software Development Kit (SDK) (standard installation path): %ProgramFiles%\\Microsoft SDKs\\Windows\\\[version number\]\\Samples\\winui\\WindowsRibbon\\Gallery</span></span>

### <a name="building-the-sample"></a><span data-ttu-id="40fb3-116">Generar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="40fb3-116">Building the Sample</span></span>

<span data-ttu-id="40fb3-117">Descargue el ejemplo en el disco duro.</span><span class="sxs-lookup"><span data-stu-id="40fb3-117">Download the sample to your hard disk.</span></span>

<span data-ttu-id="40fb3-118">Instale el Windows SDK para Windows 7 y abra la ventana de comandos del entorno de compilación.</span><span class="sxs-lookup"><span data-stu-id="40fb3-118">Install the Windows SDK for Windows 7 and open its build environment command window.</span></span> <span data-ttu-id="40fb3-119">En el menú Inicio, elija Todos los programas, Microsoft Windows SDK y haga clic en Shell CMD.</span><span class="sxs-lookup"><span data-stu-id="40fb3-119">On the Start menu, point to All Programs, Microsoft Windows SDK, and then click CMD Shell.</span></span>

<span data-ttu-id="40fb3-120">Para generar el ejemplo en la ventana de comados del entorno de compilación, vaya al directorio de origen del ejemplo.</span><span class="sxs-lookup"><span data-stu-id="40fb3-120">To build the sample from the build environment command window, go to the source directory of the sample.</span></span> <span data-ttu-id="40fb3-121">En el símbolo del sistema, escriba MSBUILD.</span><span class="sxs-lookup"><span data-stu-id="40fb3-121">At the command prompt, type MSBUILD.</span></span>

<span data-ttu-id="40fb3-122">Para compilar el ejemplo en Microsoft Visual Studio, cargue la solución de ejemplo o el archivo del proyecto y presione CTRL+MAYÚS+B.</span><span class="sxs-lookup"><span data-stu-id="40fb3-122">To build the sample in Microsoft Visual Studio, load the sample solution or project file and then press CTRL+SHIFT+B.</span></span>

### <a name="running-the-sample"></a><span data-ttu-id="40fb3-123">Ejecutar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="40fb3-123">Running the Sample</span></span>

<span data-ttu-id="40fb3-124">Para ejecutar el ejemplo desde la ventana de comandos del entorno de compilación, ejecute los archivos. exe de la \\ carpeta bin Debug o bin \\ Release incluida en la carpeta de origen de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="40fb3-124">To run the sample from the build environment command window, execute the .exe files in the Bin\\Debug or Bin\\Release folder contained in the sample source folder.</span></span>

<span data-ttu-id="40fb3-125">Para ejecutar el ejemplo compilado con depuración en Visual Studio, presione F5.</span><span class="sxs-lookup"><span data-stu-id="40fb3-125">To run the compiled sample with debugging in Visual Studio, press F5.</span></span>

## <a name="support"></a><span data-ttu-id="40fb3-126">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="40fb3-126">Support</span></span>

<span data-ttu-id="40fb3-127">El [Foro de desarrollo](https://social.msdn.microsoft.com/Forums/windowsdesktop/home?forum=windowsribbondevelopment) de la cinta de opciones de Windows está disponible para discutir temas y formular preguntas relacionadas con el desarrollo de aplicaciones de la cinta de opciones de Windows.</span><span class="sxs-lookup"><span data-stu-id="40fb3-127">The [Windows Ribbon Development Forum](https://social.msdn.microsoft.com/Forums/windowsdesktop/home?forum=windowsribbondevelopment) is available to discuss topics and ask questions related to developing Windows Ribbon applications.</span></span>

## <a name="minimum-requirements"></a><span data-ttu-id="40fb3-128">Requisitos mínimos</span><span class="sxs-lookup"><span data-stu-id="40fb3-128">Minimum Requirements</span></span>



| <span data-ttu-id="40fb3-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="40fb3-129">Requirement</span></span> | <span data-ttu-id="40fb3-130">Value</span><span class="sxs-lookup"><span data-stu-id="40fb3-130">Value</span></span> |
|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="40fb3-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="40fb3-131">Minimum supported client</span></span> | <span data-ttu-id="40fb3-132">Windows 7</span><span class="sxs-lookup"><span data-stu-id="40fb3-132">Windows 7</span></span><br/> <span data-ttu-id="40fb3-133">Windows Vista con Service Pack 2 (SP2) y la [actualización de la plataforma para Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx)</span><span class="sxs-lookup"><span data-stu-id="40fb3-133">Windows Vista with Service Pack 2 (SP2) and [Platform Update for Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx)</span></span><br/>         |
| <span data-ttu-id="40fb3-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="40fb3-134">Minimum supported server</span></span> | <span data-ttu-id="40fb3-135">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="40fb3-135">Windows Server 2008 R2</span></span><br/> <span data-ttu-id="40fb3-136">Windows Server 2008 con SP2 y [actualización de la plataforma para Windows server 2008](https://msdn.microsoft.com/library/dd378748.aspx)</span><span class="sxs-lookup"><span data-stu-id="40fb3-136">Windows Server 2008 with SP2 and [Platform Update for Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx)</span></span><br/> |
| <span data-ttu-id="40fb3-137">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="40fb3-137">Windows SDK</span></span>              | <span data-ttu-id="40fb3-138">7.0</span><span class="sxs-lookup"><span data-stu-id="40fb3-138">7.0</span></span>                                                                                                                                                                      |
| <span data-ttu-id="40fb3-139">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="40fb3-139">Visual Studio</span></span>            | <span data-ttu-id="40fb3-140">2008</span><span class="sxs-lookup"><span data-stu-id="40fb3-140">2008</span></span>                                                                                                                                                                     |
| <span data-ttu-id="40fb3-141">Archivos de encabezado y IDL</span><span class="sxs-lookup"><span data-stu-id="40fb3-141">Header and IDL files</span></span>     | <span data-ttu-id="40fb3-142">uiribbon. h, uiribbon. idl</span><span class="sxs-lookup"><span data-stu-id="40fb3-142">uiribbon.h, uiribbon.idl</span></span>                                                                                                                                                 |



 

> [!Note]  
> <span data-ttu-id="40fb3-143">La [actualización de la plataforma para Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) y la [actualización de la plataforma para Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) son conjuntos de bibliotecas en tiempo de ejecución que permiten a los desarrolladores tener como destino aplicaciones de cinta de Windows para Windows Vista y Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="40fb3-143">The [Platform Update for Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) and [Platform Update for Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) are sets of run-time libraries that enable developers to target Windows Ribbon applications to both Windows Vista and Windows Server 2008.</span></span> <span data-ttu-id="40fb3-144">Las actualizaciones de la plataforma estarán disponibles para todos los clientes de Windows Vista y Windows Server 2008 a través de Windows Update.</span><span class="sxs-lookup"><span data-stu-id="40fb3-144">The platform updates will be available to all Windows Vista and Windows Server 2008 customers through Windows Update.</span></span> <span data-ttu-id="40fb3-145">Las aplicaciones de terceros que requieren la [actualización de la plataforma para Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) o la [actualización de la plataforma para Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) pueden detectar Windows Update detectar si está instalado el requerido actualizado; en caso contrario, Windows Update lo descargará e instalará en segundo plano.</span><span class="sxs-lookup"><span data-stu-id="40fb3-145">Third-party applications that require [Platform Update for Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) or [Platform Update for Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) can have Windows Update detect whether the required updated is installed; if it is not, Windows Update will download and install it in the background.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="40fb3-146">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="40fb3-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="40fb3-147">Trabajar con galerías</span><span class="sxs-lookup"><span data-stu-id="40fb3-147">Working with Galleries</span></span>](ribbon-controls-galleries.md)
</dt> <dt>

[<span data-ttu-id="40fb3-148">Cuadro combinado</span><span class="sxs-lookup"><span data-stu-id="40fb3-148">Combo Box</span></span>](windowsribbon-controls-combobox.md)
</dt> <dt>

[<span data-ttu-id="40fb3-149">Galería desplegable</span><span class="sxs-lookup"><span data-stu-id="40fb3-149">Drop-Down Gallery</span></span>](windowsribbon-controls-dropdowngallery.md)
</dt> <dt>

[<span data-ttu-id="40fb3-150">En la galería de la cinta de opciones</span><span class="sxs-lookup"><span data-stu-id="40fb3-150">In-Ribbon Gallery</span></span>](windowsribbon-controls-inribbongallery.md)
</dt> <dt>

[<span data-ttu-id="40fb3-151">Galería de botones de expansión</span><span class="sxs-lookup"><span data-stu-id="40fb3-151">Split Button Gallery</span></span>](windowsribbon-controls-splitbuttongallery.md)
</dt> <dt>

[<span data-ttu-id="40fb3-152">Propiedades de la colección</span><span class="sxs-lookup"><span data-stu-id="40fb3-152">Collection Properties</span></span>](windowsribbon-reference-properties-collection.md)
</dt> </dl>

 

 





