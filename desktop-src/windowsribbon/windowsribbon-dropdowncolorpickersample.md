---
title: Ejemplo de DropDownColorPicker
description: En este ejemplo de código se muestra el marcado y el código necesarios para usar un control DropDownColorPicker de la cinta de opciones de Windows.
ms.assetid: cc8e18a6-9ed5-47ca-a807-f50838821f14
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0000db12fbc3b3f7ace679e4e8b1f4756d59f6e5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150371"
---
# <a name="dropdowncolorpicker-sample"></a><span data-ttu-id="630ec-103">Ejemplo de DropDownColorPicker</span><span class="sxs-lookup"><span data-stu-id="630ec-103">DropDownColorPicker Sample</span></span>

<span data-ttu-id="630ec-104">En este ejemplo de código se muestra el marcado y el código necesarios para usar un control DropDownColorPicker de la cinta de opciones de Windows.</span><span class="sxs-lookup"><span data-stu-id="630ec-104">This code sample demonstrates the markup and code required to use a Windows Ribbon DropDownColorPicker control.</span></span>

-   [<span data-ttu-id="630ec-105">Uso</span><span class="sxs-lookup"><span data-stu-id="630ec-105">Usage</span></span>](#usage)
    -   [<span data-ttu-id="630ec-106">Compilar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="630ec-106">Building the Sample</span></span>](#building-the-sample)
    -   [<span data-ttu-id="630ec-107">Ejecutar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="630ec-107">Running the Sample</span></span>](#running-the-sample)
-   [<span data-ttu-id="630ec-108">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="630ec-108">Support</span></span>](#support)
-   [<span data-ttu-id="630ec-109">Requisitos mínimos</span><span class="sxs-lookup"><span data-stu-id="630ec-109">Minimum Requirements</span></span>](#minimum-requirements)
-   [<span data-ttu-id="630ec-110">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="630ec-110">Related topics</span></span>](#related-topics)

## <a name="usage"></a><span data-ttu-id="630ec-111">Uso</span><span class="sxs-lookup"><span data-stu-id="630ec-111">Usage</span></span>

<span data-ttu-id="630ec-112">El ejemplo DropDownColorPicker se puede descargar como un proyecto de Microsoft Visual Studio independiente desde el [centro de descarga de Microsoft](https://www.microsoft.com/DOWNLOADS/en/default.aspx) o instalarse como parte del kit de desarrollo de [software (SDK) de Windows](https://msdn.microsoft.com/windows/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="630ec-112">The DropDownColorPicker Sample can be downloaded as a standalone Microsoft Visual Studio project from the [Microsoft Download Center](https://www.microsoft.com/DOWNLOADS/en/default.aspx) or installed as part of the [Windows Software Development Kit (SDK)](https://msdn.microsoft.com/windows/bb980924.aspx).</span></span>

-   <span data-ttu-id="630ec-113">Centro de descarga de Microsoft: [ejemplos de cinta de Windows](https://www.microsoft.com/downloads/details.aspx?familyid=141e13e8-b10b-4356-aaa5-609b2981574a&displaylang=en)</span><span class="sxs-lookup"><span data-stu-id="630ec-113">Microsoft Download Center: [Windows Ribbon Samples](https://www.microsoft.com/downloads/details.aspx?familyid=141e13e8-b10b-4356-aaa5-609b2981574a&displaylang=en)</span></span>
-   <span data-ttu-id="630ec-114">Kit de desarrollo de software (SDK) de Windows (ruta de instalación estándar):% ProgramFiles% \\ Microsoft SDK \\ número de versión de Windows \\ \[ ejemplos de código \] \\ \\ WinUI \\ WindowsRibbon \\ DropDownColorPicker</span><span class="sxs-lookup"><span data-stu-id="630ec-114">Windows Software Development Kit (SDK) (standard installation path): %ProgramFiles%\\Microsoft SDKs\\Windows\\\[version number\]\\Samples\\winui\\WindowsRibbon\\DropDownColorPicker</span></span>

### <a name="building-the-sample"></a><span data-ttu-id="630ec-115">Generar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="630ec-115">Building the Sample</span></span>

<span data-ttu-id="630ec-116">Descargue el ejemplo en el disco duro.</span><span class="sxs-lookup"><span data-stu-id="630ec-116">Download the sample to your hard disk.</span></span>

<span data-ttu-id="630ec-117">Instale el Windows SDK para Windows 7 y abra la ventana de comandos del entorno de compilación.</span><span class="sxs-lookup"><span data-stu-id="630ec-117">Install the Windows SDK for Windows 7 and open its build environment command window.</span></span> <span data-ttu-id="630ec-118">En el menú Inicio, elija Todos los programas, Microsoft Windows SDK y haga clic en Shell CMD.</span><span class="sxs-lookup"><span data-stu-id="630ec-118">On the Start menu, point to All Programs, Microsoft Windows SDK, and then click CMD Shell.</span></span>

<span data-ttu-id="630ec-119">Para generar el ejemplo en la ventana de comados del entorno de compilación, vaya al directorio de origen del ejemplo.</span><span class="sxs-lookup"><span data-stu-id="630ec-119">To build the sample from the build environment command window, go to the source directory of the sample.</span></span> <span data-ttu-id="630ec-120">En el símbolo del sistema, escriba MSBUILD.</span><span class="sxs-lookup"><span data-stu-id="630ec-120">At the command prompt, type MSBUILD.</span></span>

<span data-ttu-id="630ec-121">Para compilar el ejemplo en Microsoft Visual Studio, cargue la solución de ejemplo o el archivo del proyecto y presione CTRL+MAYÚS+B.</span><span class="sxs-lookup"><span data-stu-id="630ec-121">To build the sample in Microsoft Visual Studio, load the sample solution or project file and then press CTRL+SHIFT+B.</span></span>

### <a name="running-the-sample"></a><span data-ttu-id="630ec-122">Ejecutar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="630ec-122">Running the Sample</span></span>

<span data-ttu-id="630ec-123">Para ejecutar el ejemplo desde la ventana de comandos del entorno de compilación, ejecute los archivos. exe de la \\ carpeta bin Debug o bin \\ Release incluida en la carpeta de origen de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="630ec-123">To run the sample from the build environment command window, execute the .exe files in the Bin\\Debug or Bin\\Release folder contained in the sample source folder.</span></span>

<span data-ttu-id="630ec-124">Para ejecutar el ejemplo compilado con depuración en Visual Studio, presione F5.</span><span class="sxs-lookup"><span data-stu-id="630ec-124">To run the compiled sample with debugging in Visual Studio, press F5.</span></span>

## <a name="support"></a><span data-ttu-id="630ec-125">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="630ec-125">Support</span></span>

<span data-ttu-id="630ec-126">El [Foro de desarrollo](https://social.msdn.microsoft.com/Forums/windowsdesktop/home?forum=windowsribbondevelopment) de la cinta de opciones de Windows está disponible para discutir temas y formular preguntas relacionadas con el desarrollo de aplicaciones de la cinta de opciones de Windows.</span><span class="sxs-lookup"><span data-stu-id="630ec-126">The [Windows Ribbon Development Forum](https://social.msdn.microsoft.com/Forums/windowsdesktop/home?forum=windowsribbondevelopment) is available to discuss topics and ask questions related to developing Windows Ribbon applications.</span></span>

## <a name="minimum-requirements"></a><span data-ttu-id="630ec-127">Requisitos mínimos</span><span class="sxs-lookup"><span data-stu-id="630ec-127">Minimum Requirements</span></span>



| <span data-ttu-id="630ec-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="630ec-128">Requirement</span></span> | <span data-ttu-id="630ec-129">Value</span><span class="sxs-lookup"><span data-stu-id="630ec-129">Value</span></span> |
|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="630ec-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="630ec-130">Minimum supported client</span></span> | <span data-ttu-id="630ec-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="630ec-131">Windows 7</span></span><br/> <span data-ttu-id="630ec-132">Windows Vista con Service Pack 2 (SP2) y la [actualización de la plataforma para Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx)</span><span class="sxs-lookup"><span data-stu-id="630ec-132">Windows Vista with Service Pack 2 (SP2) and [Platform Update for Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx)</span></span><br/>         |
| <span data-ttu-id="630ec-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="630ec-133">Minimum supported server</span></span> | <span data-ttu-id="630ec-134">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="630ec-134">Windows Server 2008 R2</span></span><br/> <span data-ttu-id="630ec-135">Windows Server 2008 con SP2 y [actualización de la plataforma para Windows server 2008](https://msdn.microsoft.com/library/dd378748.aspx)</span><span class="sxs-lookup"><span data-stu-id="630ec-135">Windows Server 2008 with SP2 and [Platform Update for Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx)</span></span><br/> |
| <span data-ttu-id="630ec-136">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="630ec-136">Windows SDK</span></span>              | <span data-ttu-id="630ec-137">7.0</span><span class="sxs-lookup"><span data-stu-id="630ec-137">7.0</span></span>                                                                                                                                                                      |
| <span data-ttu-id="630ec-138">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="630ec-138">Visual Studio</span></span>            | <span data-ttu-id="630ec-139">2008</span><span class="sxs-lookup"><span data-stu-id="630ec-139">2008</span></span>                                                                                                                                                                     |
| <span data-ttu-id="630ec-140">Archivos de encabezado y IDL</span><span class="sxs-lookup"><span data-stu-id="630ec-140">Header and IDL files</span></span>     | <span data-ttu-id="630ec-141">uiribbon. h, uiribbon. idl</span><span class="sxs-lookup"><span data-stu-id="630ec-141">uiribbon.h, uiribbon.idl</span></span>                                                                                                                                                 |



 

> [!Note]  
> <span data-ttu-id="630ec-142">La [actualización de la plataforma para Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) y la [actualización de la plataforma para Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) son conjuntos de bibliotecas en tiempo de ejecución que permiten a los desarrolladores tener como destino aplicaciones de cinta de Windows para Windows Vista y Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="630ec-142">The [Platform Update for Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) and [Platform Update for Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) are sets of run-time libraries that enable developers to target Windows Ribbon applications to both Windows Vista and Windows Server 2008.</span></span> <span data-ttu-id="630ec-143">Las actualizaciones de la plataforma estarán disponibles para todos los clientes de Windows Vista y Windows Server 2008 a través de Windows Update.</span><span class="sxs-lookup"><span data-stu-id="630ec-143">The platform updates will be available to all Windows Vista and Windows Server 2008 customers through Windows Update.</span></span> <span data-ttu-id="630ec-144">Las aplicaciones de terceros que requieren la [actualización de la plataforma para Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) o la [actualización de la plataforma para Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) pueden detectar Windows Update detectar si está instalado el requerido actualizado; en caso contrario, Windows Update lo descargará e instalará en segundo plano.</span><span class="sxs-lookup"><span data-stu-id="630ec-144">Third-party applications that require [Platform Update for Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) or [Platform Update for Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) can have Windows Update detect whether the required updated is installed; if it is not, Windows Update will download and install it in the background.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="630ec-145">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="630ec-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="630ec-146">Selector de colores desplegables</span><span class="sxs-lookup"><span data-stu-id="630ec-146">Drop-Down Color Picker</span></span>](windowsribbon-controls-dropdowncolorpicker.md)
</dt> <dt>

[<span data-ttu-id="630ec-147">Propiedades del selector de colores</span><span class="sxs-lookup"><span data-stu-id="630ec-147">Color Picker Properties</span></span>](windowsribbon-reference-properties-colorpicker.md)
</dt> </dl>

 

 





