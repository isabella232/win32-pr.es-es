---
title: Ejemplo de FontControl
description: En este ejemplo de código se muestra el marcado y el código necesarios para implementar un FontControl dentro de una Windows ribbon.
ms.assetid: 8fb84bd1-5e63-447c-b7a0-b3d7cb8c3be7
ms.topic: article
ms.date: 07/13/2021
ms.openlocfilehash: 52a81a1a1950305437a7bbc68aab95876b3a6374
ms.sourcegitcommit: 63c93e0ad0b48d60b11008767196718feb475cb0
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/13/2021
ms.locfileid: "113691764"
---
# <a name="fontcontrol-sample"></a><span data-ttu-id="e0878-103">Ejemplo de FontControl</span><span class="sxs-lookup"><span data-stu-id="e0878-103">FontControl Sample</span></span>

<span data-ttu-id="e0878-104">En este ejemplo de código se muestra el marcado y el código necesarios para implementar un FontControl dentro de una Windows ribbon.</span><span class="sxs-lookup"><span data-stu-id="e0878-104">This code sample demonstrates the markup and code required to implement a FontControl within a Windows Ribbon application.</span></span>

- [<span data-ttu-id="e0878-105">Uso</span><span class="sxs-lookup"><span data-stu-id="e0878-105">Usage</span></span>](#usage)
  - [<span data-ttu-id="e0878-106">Compilar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="e0878-106">Building the Sample</span></span>](#building-the-sample)
  - [<span data-ttu-id="e0878-107">Ejecución del ejemplo</span><span class="sxs-lookup"><span data-stu-id="e0878-107">Running the Sample</span></span>](#running-the-sample)
- [<span data-ttu-id="e0878-108">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="e0878-108">Support</span></span>](#support)
- [<span data-ttu-id="e0878-109">Requisitos mínimos</span><span class="sxs-lookup"><span data-stu-id="e0878-109">Minimum Requirements</span></span>](#minimum-requirements)
- [<span data-ttu-id="e0878-110">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e0878-110">Related topics</span></span>](#related-topics)

## <a name="usage"></a><span data-ttu-id="e0878-111">Uso</span><span class="sxs-lookup"><span data-stu-id="e0878-111">Usage</span></span>

<span data-ttu-id="e0878-112">Los ejemplos Windows marco de la cinta de opciones se pueden descargar como proyectos de Microsoft Visual Studio independientes desde el Centro de descarga de [Microsoft](https://www.microsoft.com/download/details.aspx?id=9620) o instalarse como parte del Kit de desarrollo de [software (SDK)](https://developer.microsoft.com/windows/downloads/sdk-archive/)de Windows .</span><span class="sxs-lookup"><span data-stu-id="e0878-112">The Windows Ribbon framework samples can be downloaded as standalone Microsoft Visual Studio projects from the [Microsoft Download Center](https://www.microsoft.com/download/details.aspx?id=9620) or installed as part of the [Windows Software Development Kit (SDK)](https://developer.microsoft.com/windows/downloads/sdk-archive/).</span></span>

- <span data-ttu-id="e0878-113">Windows Kit de desarrollo de software (SDK) (ruta de instalación estándar): %ProgramFiles% SDK de Microsoft Windows número de versión \\ \\ Ejemplos \\ \[ \] \\ \\ winui \\ WindowsRibbon \\ FontControl</span><span class="sxs-lookup"><span data-stu-id="e0878-113">Windows Software Development Kit (SDK) (standard installation path): %ProgramFiles%\\Microsoft SDKs\\Windows\\\[version number\]\\Samples\\winui\\WindowsRibbon\\FontControl</span></span>

### <a name="building-the-sample"></a><span data-ttu-id="e0878-114">Generar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="e0878-114">Building the Sample</span></span>

<span data-ttu-id="e0878-115">Descargue el ejemplo.</span><span class="sxs-lookup"><span data-stu-id="e0878-115">Download the sample.</span></span>

<span data-ttu-id="e0878-116">Instale el SDK Windows para Windows 7 y abra su ventana de comandos del entorno de compilación.</span><span class="sxs-lookup"><span data-stu-id="e0878-116">Install the Windows SDK for Windows 7 and open its build environment command window.</span></span> <span data-ttu-id="e0878-117">En el menú Inicio, elija Todos los programas, Microsoft Windows SDK y haga clic en Shell CMD.</span><span class="sxs-lookup"><span data-stu-id="e0878-117">On the Start menu, point to All Programs, Microsoft Windows SDK, and then click CMD Shell.</span></span>

<span data-ttu-id="e0878-118">Para generar el ejemplo en la ventana de comados del entorno de compilación, vaya al directorio de origen del ejemplo.</span><span class="sxs-lookup"><span data-stu-id="e0878-118">To build the sample from the build environment command window, go to the source directory of the sample.</span></span> <span data-ttu-id="e0878-119">En el símbolo del sistema, escriba MSBUILD.</span><span class="sxs-lookup"><span data-stu-id="e0878-119">At the command prompt, type MSBUILD.</span></span>

<span data-ttu-id="e0878-120">Para compilar el ejemplo en Microsoft Visual Studio, cargue la solución de ejemplo o el archivo del proyecto y presione CTRL+MAYÚS+B.</span><span class="sxs-lookup"><span data-stu-id="e0878-120">To build the sample in Microsoft Visual Studio, load the sample solution or project file and then press CTRL+SHIFT+B.</span></span>

### <a name="running-the-sample"></a><span data-ttu-id="e0878-121">Ejecutar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="e0878-121">Running the Sample</span></span>

<span data-ttu-id="e0878-122">Para ejecutar el ejemplo desde la ventana de comandos del entorno de compilación, ejecute los archivos .exe en la carpeta Bin Debug o Bin Release contenida en la carpeta \\ \\ de origen de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="e0878-122">To run the sample from the build environment command window, execute the .exe files in the Bin\\Debug or Bin\\Release folder contained in the sample source folder.</span></span>

<span data-ttu-id="e0878-123">Para ejecutar el ejemplo compilado con depuración en Visual Studio, presione F5.</span><span class="sxs-lookup"><span data-stu-id="e0878-123">To run the compiled sample with debugging in Visual Studio, press F5.</span></span>

## <a name="support"></a><span data-ttu-id="e0878-124">Compatibilidad</span><span class="sxs-lookup"><span data-stu-id="e0878-124">Support</span></span>

<span data-ttu-id="e0878-125">El [foro Windows desarrollo de la cinta](https://social.msdn.microsoft.com/Forums/windowsdesktop/home?forum=windowsribbondevelopment) de opciones está disponible para analizar temas y hacer preguntas relacionadas con el desarrollo de Windows de cinta de opciones.</span><span class="sxs-lookup"><span data-stu-id="e0878-125">The [Windows Ribbon Development Forum](https://social.msdn.microsoft.com/Forums/windowsdesktop/home?forum=windowsribbondevelopment) is available to discuss topics and ask questions related to developing Windows Ribbon applications.</span></span>

## <a name="minimum-requirements"></a><span data-ttu-id="e0878-126">Requisitos mínimos</span><span class="sxs-lookup"><span data-stu-id="e0878-126">Minimum Requirements</span></span>



| <span data-ttu-id="e0878-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="e0878-127">Requirement</span></span> | <span data-ttu-id="e0878-128">Valor</span><span class="sxs-lookup"><span data-stu-id="e0878-128">Value</span></span> |
|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e0878-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e0878-129">Minimum supported client</span></span> | <span data-ttu-id="e0878-130">Windows 7</span><span class="sxs-lookup"><span data-stu-id="e0878-130">Windows 7</span></span><br/> <span data-ttu-id="e0878-131">Windows Vista con Service Pack 2 (SP2) y [actualización de plataforma para Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx)</span><span class="sxs-lookup"><span data-stu-id="e0878-131">Windows Vista with Service Pack 2 (SP2) and [Platform Update for Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx)</span></span><br/>         |
| <span data-ttu-id="e0878-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e0878-132">Minimum supported server</span></span> | <span data-ttu-id="e0878-133">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e0878-133">Windows Server 2008 R2</span></span><br/> <span data-ttu-id="e0878-134">Windows Server 2008 con SP2 y actualización de plataforma [para Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx)</span><span class="sxs-lookup"><span data-stu-id="e0878-134">Windows Server 2008 with SP2 and [Platform Update for Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx)</span></span><br/> |
| <span data-ttu-id="e0878-135">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="e0878-135">Windows SDK</span></span>              | <span data-ttu-id="e0878-136">7.0</span><span class="sxs-lookup"><span data-stu-id="e0878-136">7.0</span></span>                                                                                                                                                                      |
| <span data-ttu-id="e0878-137">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="e0878-137">Visual Studio</span></span>            | <span data-ttu-id="e0878-138">2008</span><span class="sxs-lookup"><span data-stu-id="e0878-138">2008</span></span>                                                                                                                                                                     |
| <span data-ttu-id="e0878-139">Archivos de encabezado e IDL</span><span class="sxs-lookup"><span data-stu-id="e0878-139">Header and IDL files</span></span>     | <span data-ttu-id="e0878-140">uiribbon.h, uiribbon.idl</span><span class="sxs-lookup"><span data-stu-id="e0878-140">uiribbon.h, uiribbon.idl</span></span>                                                                                                                                                 |



 

> [!Note]  
> <span data-ttu-id="e0878-141">La actualización de plataforma para [Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) y la actualización de plataforma para Windows [Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) son conjuntos de bibliotecas en tiempo de ejecución que permiten a los desarrolladores dirigir aplicaciones de la cinta de opciones de Windows a Windows Vista y Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="e0878-141">The [Platform Update for Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) and [Platform Update for Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) are sets of run-time libraries that enable developers to target Windows Ribbon applications to both Windows Vista and Windows Server 2008.</span></span> <span data-ttu-id="e0878-142">Las actualizaciones de la plataforma estarán disponibles para todos los Windows Vista y Windows Server 2008 a través de Windows Update.</span><span class="sxs-lookup"><span data-stu-id="e0878-142">The platform updates will be available to all Windows Vista and Windows Server 2008 customers through Windows Update.</span></span> <span data-ttu-id="e0878-143">Las aplicaciones de terceros que requieren Actualización de plataforma para [Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) o Actualización de plataforma para Windows [Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) pueden hacer que Windows Update detecte si está instalada la actualización necesaria; Si no es así, Windows Update la descargará e instalará en segundo plano.</span><span class="sxs-lookup"><span data-stu-id="e0878-143">Third-party applications that require [Platform Update for Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) or [Platform Update for Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) can have Windows Update detect whether the required updated is installed; if it is not, Windows Update will download and install it in the background.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="e0878-144">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e0878-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e0878-145">Control de fuentes</span><span class="sxs-lookup"><span data-stu-id="e0878-145">Font Control</span></span>](windowsribbon-controls-fontcontrol.md)
</dt> <dt>

[<span data-ttu-id="e0878-146">Propiedades del control de fuentes</span><span class="sxs-lookup"><span data-stu-id="e0878-146">Font Control Properties</span></span>](windowsribbon-reference-properties-fontcontrol.md)
</dt> </dl>

 

 





