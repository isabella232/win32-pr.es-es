---
title: Ejemplo de SimpleRibbon
description: En este ejemplo de código se muestra cómo implementar una sencilla aplicación de cinta de Windows.
ms.assetid: 9196ae63-ca9e-43ae-8b4c-a30f1ef700f0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5055d47db2d947778699d55bbae96649b9b45ef
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492496"
---
# <a name="simpleribbon-sample"></a><span data-ttu-id="5e648-103">Ejemplo de SimpleRibbon</span><span class="sxs-lookup"><span data-stu-id="5e648-103">SimpleRibbon Sample</span></span>

<span data-ttu-id="5e648-104">En este ejemplo de código se muestra cómo implementar una sencilla aplicación de cinta de Windows.</span><span class="sxs-lookup"><span data-stu-id="5e648-104">This code sample demonstrates how to implement a simple Windows Ribbon application.</span></span>

-   [<span data-ttu-id="5e648-105">Uso</span><span class="sxs-lookup"><span data-stu-id="5e648-105">Usage</span></span>](#usage)
    -   [<span data-ttu-id="5e648-106">Compilar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="5e648-106">Building the Sample</span></span>](#building-the-sample)
    -   [<span data-ttu-id="5e648-107">Ejecutar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="5e648-107">Running the Sample</span></span>](#running-the-sample)
-   [<span data-ttu-id="5e648-108">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="5e648-108">Support</span></span>](#support)
-   [<span data-ttu-id="5e648-109">Requisitos mínimos</span><span class="sxs-lookup"><span data-stu-id="5e648-109">Minimum Requirements</span></span>](#minimum-requirements)

## <a name="usage"></a><span data-ttu-id="5e648-110">Uso</span><span class="sxs-lookup"><span data-stu-id="5e648-110">Usage</span></span>

<span data-ttu-id="5e648-111">El ejemplo SimpleRibbon se puede descargar como un proyecto de Microsoft Visual Studio independiente desde el [centro de descarga de Microsoft](https://www.microsoft.com/DOWNLOADS/en/default.aspx) o instalarse como parte del kit de desarrollo de [software (SDK) de Windows](https://msdn.microsoft.com/windows/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="5e648-111">The SimpleRibbon Sample can be downloaded as a standalone Microsoft Visual Studio project from the [Microsoft Download Center](https://www.microsoft.com/DOWNLOADS/en/default.aspx) or installed as part of the [Windows Software Development Kit (SDK)](https://msdn.microsoft.com/windows/bb980924.aspx).</span></span>

-   <span data-ttu-id="5e648-112">Centro de descarga de Microsoft: [ejemplos de cinta de Windows](https://www.microsoft.com/downloads/details.aspx?familyid=141e13e8-b10b-4356-aaa5-609b2981574a&displaylang=en)</span><span class="sxs-lookup"><span data-stu-id="5e648-112">Microsoft Download Center: [Windows Ribbon Samples](https://www.microsoft.com/downloads/details.aspx?familyid=141e13e8-b10b-4356-aaa5-609b2981574a&displaylang=en)</span></span>
-   <span data-ttu-id="5e648-113">Kit de desarrollo de software (SDK) de Windows (ruta de instalación estándar):% ProgramFiles% \\ Microsoft SDK \\ número de versión de Windows \\ \[ ejemplos de código \] \\ \\ WinUI \\ WindowsRibbon \\ SimpleRibbon</span><span class="sxs-lookup"><span data-stu-id="5e648-113">Windows Software Development Kit (SDK) (standard installation path): %ProgramFiles%\\Microsoft SDKs\\Windows\\\[version number\]\\Samples\\winui\\WindowsRibbon\\SimpleRibbon</span></span>

### <a name="building-the-sample"></a><span data-ttu-id="5e648-114">Generar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="5e648-114">Building the Sample</span></span>

<span data-ttu-id="5e648-115">Descargue el ejemplo en el disco duro.</span><span class="sxs-lookup"><span data-stu-id="5e648-115">Download the sample to your hard disk.</span></span>

<span data-ttu-id="5e648-116">Instale el Windows SDK para Windows 7 y abra la ventana de comandos del entorno de compilación.</span><span class="sxs-lookup"><span data-stu-id="5e648-116">Install the Windows SDK for Windows 7 and open its build environment command window.</span></span> <span data-ttu-id="5e648-117">En el menú Inicio, elija Todos los programas, Microsoft Windows SDK y haga clic en Shell CMD.</span><span class="sxs-lookup"><span data-stu-id="5e648-117">On the Start menu, point to All Programs, Microsoft Windows SDK, and then click CMD Shell.</span></span>

<span data-ttu-id="5e648-118">Para generar el ejemplo en la ventana de comados del entorno de compilación, vaya al directorio de origen del ejemplo.</span><span class="sxs-lookup"><span data-stu-id="5e648-118">To build the sample from the build environment command window, go to the source directory of the sample.</span></span> <span data-ttu-id="5e648-119">En el símbolo del sistema, escriba MSBUILD.</span><span class="sxs-lookup"><span data-stu-id="5e648-119">At the command prompt, type MSBUILD.</span></span>

<span data-ttu-id="5e648-120">Para compilar el ejemplo en Microsoft Visual Studio, cargue la solución de ejemplo o el archivo del proyecto y presione CTRL+MAYÚS+B.</span><span class="sxs-lookup"><span data-stu-id="5e648-120">To build the sample in Microsoft Visual Studio, load the sample solution or project file and then press CTRL+SHIFT+B.</span></span>

### <a name="running-the-sample"></a><span data-ttu-id="5e648-121">Ejecutar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="5e648-121">Running the Sample</span></span>

<span data-ttu-id="5e648-122">Para ejecutar el ejemplo desde la ventana de comandos del entorno de compilación, ejecute los archivos. exe de la \\ carpeta bin Debug o bin \\ Release incluida en la carpeta de origen de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="5e648-122">To run the sample from the build environment command window, execute the .exe files in the Bin\\Debug or Bin\\Release folder contained in the sample source folder.</span></span>

<span data-ttu-id="5e648-123">Para ejecutar el ejemplo compilado con depuración en Visual Studio, presione F5.</span><span class="sxs-lookup"><span data-stu-id="5e648-123">To run the compiled sample with debugging in Visual Studio, press F5.</span></span>

## <a name="support"></a><span data-ttu-id="5e648-124">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="5e648-124">Support</span></span>

<span data-ttu-id="5e648-125">El [Foro de desarrollo](https://social.msdn.microsoft.com/Forums/windowsdesktop/home?forum=windowsribbondevelopment) de la cinta de opciones de Windows está disponible para discutir temas y formular preguntas relacionadas con el desarrollo de aplicaciones de la cinta de opciones de Windows.</span><span class="sxs-lookup"><span data-stu-id="5e648-125">The [Windows Ribbon Development Forum](https://social.msdn.microsoft.com/Forums/windowsdesktop/home?forum=windowsribbondevelopment) is available to discuss topics and ask questions related to developing Windows Ribbon applications.</span></span>

## <a name="minimum-requirements"></a><span data-ttu-id="5e648-126">Requisitos mínimos</span><span class="sxs-lookup"><span data-stu-id="5e648-126">Minimum Requirements</span></span>



| <span data-ttu-id="5e648-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="5e648-127">Requirement</span></span> | <span data-ttu-id="5e648-128">Value</span><span class="sxs-lookup"><span data-stu-id="5e648-128">Value</span></span> |
|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5e648-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5e648-129">Minimum supported client</span></span> | <span data-ttu-id="5e648-130">Windows 7</span><span class="sxs-lookup"><span data-stu-id="5e648-130">Windows 7</span></span><br/> <span data-ttu-id="5e648-131">Windows Vista con Service Pack 2 (SP2) y la [actualización de la plataforma para Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx)</span><span class="sxs-lookup"><span data-stu-id="5e648-131">Windows Vista with Service Pack 2 (SP2) and [Platform Update for Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx)</span></span><br/>         |
| <span data-ttu-id="5e648-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5e648-132">Minimum supported server</span></span> | <span data-ttu-id="5e648-133">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="5e648-133">Windows Server 2008 R2</span></span><br/> <span data-ttu-id="5e648-134">Windows Server 2008 con SP2 y [actualización de la plataforma para Windows server 2008](https://msdn.microsoft.com/library/dd378748.aspx)</span><span class="sxs-lookup"><span data-stu-id="5e648-134">Windows Server 2008 with SP2 and [Platform Update for Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx)</span></span><br/> |
| <span data-ttu-id="5e648-135">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="5e648-135">Windows SDK</span></span>              | <span data-ttu-id="5e648-136">7.0</span><span class="sxs-lookup"><span data-stu-id="5e648-136">7.0</span></span>                                                                                                                                                                      |
| <span data-ttu-id="5e648-137">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="5e648-137">Visual Studio</span></span>            | <span data-ttu-id="5e648-138">2008</span><span class="sxs-lookup"><span data-stu-id="5e648-138">2008</span></span>                                                                                                                                                                     |
| <span data-ttu-id="5e648-139">Archivos de encabezado y IDL</span><span class="sxs-lookup"><span data-stu-id="5e648-139">Header and IDL files</span></span>     | <span data-ttu-id="5e648-140">uiribbon. h, uiribbon. idl</span><span class="sxs-lookup"><span data-stu-id="5e648-140">uiribbon.h, uiribbon.idl</span></span>                                                                                                                                                 |



 

> [!Note]  
> <span data-ttu-id="5e648-141">La [actualización de la plataforma para Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) y la [actualización de la plataforma para Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) son conjuntos de bibliotecas en tiempo de ejecución que permiten a los desarrolladores tener como destino aplicaciones de cinta de Windows para Windows Vista y Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="5e648-141">The [Platform Update for Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) and [Platform Update for Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) are sets of run-time libraries that enable developers to target Windows Ribbon applications to both Windows Vista and Windows Server 2008.</span></span> <span data-ttu-id="5e648-142">Las actualizaciones de la plataforma estarán disponibles para todos los clientes de Windows Vista y Windows Server 2008 a través de Windows Update.</span><span class="sxs-lookup"><span data-stu-id="5e648-142">The platform updates will be available to all Windows Vista and Windows Server 2008 customers through Windows Update.</span></span> <span data-ttu-id="5e648-143">Las aplicaciones de terceros que requieren la [actualización de la plataforma para Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) o la [actualización de la plataforma para Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) pueden detectar Windows Update detectar si está instalado el requerido actualizado; en caso contrario, Windows Update lo descargará e instalará en segundo plano.</span><span class="sxs-lookup"><span data-stu-id="5e648-143">Third-party applications that require [Platform Update for Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) or [Platform Update for Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) can have Windows Update detect whether the required updated is installed; if it is not, Windows Update will download and install it in the background.</span></span>

 

 

 





