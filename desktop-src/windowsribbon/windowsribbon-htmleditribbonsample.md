---
title: Ejemplo de HTMLEditRibbon
description: En este ejemplo de código se muestra el marcado y el código necesarios para migrar una aplicación Microsoft Foundation Classes (MFC) existente para usar la cinta de opciones de Windows.
ms.assetid: 1505aaea-76d2-47bc-bdc9-12e761da93f9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f98d4d76508b812d86a4dab38f8dcec96dadc52
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079085"
---
# <a name="htmleditribbon-sample"></a><span data-ttu-id="e6f39-103">Ejemplo de HTMLEditRibbon</span><span class="sxs-lookup"><span data-stu-id="e6f39-103">HTMLEditRibbon Sample</span></span>

<span data-ttu-id="e6f39-104">En este ejemplo de código se muestra el marcado y el código necesarios para migrar una aplicación Microsoft Foundation Classes (MFC) existente para usar la cinta de opciones de Windows.</span><span class="sxs-lookup"><span data-stu-id="e6f39-104">This code sample shows markup and code required to migrate an existing Microsoft Foundation Classes (MFC) application to use the Windows Ribbon.</span></span> <span data-ttu-id="e6f39-105">Se creó tomando la aplicación de ejemplo HTMLEdit de MFC existente y modificando su código y sus recursos para usar la cinta de opciones de Windows.</span><span class="sxs-lookup"><span data-stu-id="e6f39-105">It was created by taking the existing MFC HTMLEdit sample application and modifying its code and resources to use the Windows Ribbon.</span></span>

-   [<span data-ttu-id="e6f39-106">Comentarios:</span><span class="sxs-lookup"><span data-stu-id="e6f39-106">Remarks</span></span>](#remarks)
-   [<span data-ttu-id="e6f39-107">Uso</span><span class="sxs-lookup"><span data-stu-id="e6f39-107">Usage</span></span>](#usage)
    -   [<span data-ttu-id="e6f39-108">Compilar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="e6f39-108">Building the Sample</span></span>](#building-the-sample)
    -   [<span data-ttu-id="e6f39-109">Ejecutar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="e6f39-109">Running the Sample</span></span>](#running-the-sample)
-   [<span data-ttu-id="e6f39-110">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="e6f39-110">Support</span></span>](#support)
-   [<span data-ttu-id="e6f39-111">Requisitos mínimos</span><span class="sxs-lookup"><span data-stu-id="e6f39-111">Minimum Requirements</span></span>](#minimum-requirements)

## <a name="remarks"></a><span data-ttu-id="e6f39-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e6f39-112">Remarks</span></span>

<span data-ttu-id="e6f39-113">Para obtener el ejemplo de MFC, vea [ejemplo de HTMLEdit: incluye el control de edición MSHTML de Internet Explorer](https://msdn.microsoft.com/library/ea8hhwb6(VS.80).aspx).</span><span class="sxs-lookup"><span data-stu-id="e6f39-113">For the MFC sample, see [HTMLEdit Sample: Wraps the Internet Explorer MSHTML Editing Control](https://msdn.microsoft.com/library/ea8hhwb6(VS.80).aspx).</span></span>

## <a name="usage"></a><span data-ttu-id="e6f39-114">Uso</span><span class="sxs-lookup"><span data-stu-id="e6f39-114">Usage</span></span>

<span data-ttu-id="e6f39-115">El ejemplo HTMLEditRibbon se puede descargar como un proyecto de Microsoft Visual Studio independiente desde el [centro de descarga de Microsoft](https://www.microsoft.com/DOWNLOADS/en/default.aspx) o instalarse como parte del kit de desarrollo de [software (SDK) de Windows](https://msdn.microsoft.com/windows/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="e6f39-115">The HTMLEditRibbon Sample can be downloaded as a standalone Microsoft Visual Studio project from the [Microsoft Download Center](https://www.microsoft.com/DOWNLOADS/en/default.aspx) or installed as part of the [Windows Software Development Kit (SDK)](https://msdn.microsoft.com/windows/bb980924.aspx).</span></span>

-   <span data-ttu-id="e6f39-116">Centro de descarga de Microsoft: [ejemplos de cinta de Windows](https://www.microsoft.com/downloads/details.aspx?familyid=141e13e8-b10b-4356-aaa5-609b2981574a&displaylang=en)</span><span class="sxs-lookup"><span data-stu-id="e6f39-116">Microsoft Download Center: [Windows Ribbon Samples](https://www.microsoft.com/downloads/details.aspx?familyid=141e13e8-b10b-4356-aaa5-609b2981574a&displaylang=en)</span></span>
-   <span data-ttu-id="e6f39-117">Kit de desarrollo de software (SDK) de Windows (ruta de instalación estándar):% ProgramFiles% \\ Microsoft SDK \\ número de versión de Windows \\ \[ ejemplos de código \] \\ \\ WinUI \\ WindowsRibbon \\ HTMLEditRibbon</span><span class="sxs-lookup"><span data-stu-id="e6f39-117">Windows Software Development Kit (SDK) (standard installation path): %ProgramFiles%\\Microsoft SDKs\\Windows\\\[version number\]\\Samples\\winui\\WindowsRibbon\\HTMLEditRibbon</span></span>

### <a name="building-the-sample"></a><span data-ttu-id="e6f39-118">Generar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="e6f39-118">Building the Sample</span></span>

<span data-ttu-id="e6f39-119">Descargue el ejemplo en el disco duro.</span><span class="sxs-lookup"><span data-stu-id="e6f39-119">Download the sample to your hard disk.</span></span>

<span data-ttu-id="e6f39-120">Instale el Windows SDK para Windows 7 y abra la ventana de comandos del entorno de compilación.</span><span class="sxs-lookup"><span data-stu-id="e6f39-120">Install the Windows SDK for Windows 7 and open its build environment command window.</span></span> <span data-ttu-id="e6f39-121">En el menú Inicio, elija Todos los programas, Microsoft Windows SDK y haga clic en Shell CMD.</span><span class="sxs-lookup"><span data-stu-id="e6f39-121">On the Start menu, point to All Programs, Microsoft Windows SDK, and then click CMD Shell.</span></span>

<span data-ttu-id="e6f39-122">Para generar el ejemplo en la ventana de comados del entorno de compilación, vaya al directorio de origen del ejemplo.</span><span class="sxs-lookup"><span data-stu-id="e6f39-122">To build the sample from the build environment command window, go to the source directory of the sample.</span></span> <span data-ttu-id="e6f39-123">En el símbolo del sistema, escriba MSBUILD.</span><span class="sxs-lookup"><span data-stu-id="e6f39-123">At the command prompt, type MSBUILD.</span></span>

<span data-ttu-id="e6f39-124">Para compilar el ejemplo en Microsoft Visual Studio, cargue la solución de ejemplo o el archivo del proyecto y presione CTRL+MAYÚS+B.</span><span class="sxs-lookup"><span data-stu-id="e6f39-124">To build the sample in Microsoft Visual Studio, load the sample solution or project file and then press CTRL+SHIFT+B.</span></span>

### <a name="running-the-sample"></a><span data-ttu-id="e6f39-125">Ejecutar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="e6f39-125">Running the Sample</span></span>

<span data-ttu-id="e6f39-126">Para ejecutar el ejemplo desde la ventana de comandos del entorno de compilación, ejecute los archivos. exe de la \\ carpeta bin Debug o bin \\ Release incluida en la carpeta de origen de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="e6f39-126">To run the sample from the build environment command window, execute the .exe files in the Bin\\Debug or Bin\\Release folder contained in the sample source folder.</span></span>

<span data-ttu-id="e6f39-127">Para ejecutar el ejemplo compilado con depuración en Visual Studio, presione F5.</span><span class="sxs-lookup"><span data-stu-id="e6f39-127">To run the compiled sample with debugging in Visual Studio, press F5.</span></span>

## <a name="support"></a><span data-ttu-id="e6f39-128">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="e6f39-128">Support</span></span>

<span data-ttu-id="e6f39-129">El [Foro de desarrollo](https://social.msdn.microsoft.com/Forums/windowsdesktop/home?forum=windowsribbondevelopment) de la cinta de opciones de Windows está disponible para discutir temas y formular preguntas relacionadas con el desarrollo de aplicaciones de la cinta de opciones de Windows.</span><span class="sxs-lookup"><span data-stu-id="e6f39-129">The [Windows Ribbon Development Forum](https://social.msdn.microsoft.com/Forums/windowsdesktop/home?forum=windowsribbondevelopment) is available to discuss topics and ask questions related to developing Windows Ribbon applications.</span></span>

## <a name="minimum-requirements"></a><span data-ttu-id="e6f39-130">Requisitos mínimos</span><span class="sxs-lookup"><span data-stu-id="e6f39-130">Minimum Requirements</span></span>



| <span data-ttu-id="e6f39-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="e6f39-131">Requirement</span></span> | <span data-ttu-id="e6f39-132">Value</span><span class="sxs-lookup"><span data-stu-id="e6f39-132">Value</span></span> |
|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e6f39-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e6f39-133">Minimum supported client</span></span> | <span data-ttu-id="e6f39-134">Windows 7</span><span class="sxs-lookup"><span data-stu-id="e6f39-134">Windows 7</span></span><br/> <span data-ttu-id="e6f39-135">Windows Vista con Service Pack 2 (SP2) y la [actualización de la plataforma para Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx)</span><span class="sxs-lookup"><span data-stu-id="e6f39-135">Windows Vista with Service Pack 2 (SP2) and [Platform Update for Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx)</span></span><br/>         |
| <span data-ttu-id="e6f39-136">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e6f39-136">Minimum supported server</span></span> | <span data-ttu-id="e6f39-137">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e6f39-137">Windows Server 2008 R2</span></span><br/> <span data-ttu-id="e6f39-138">Windows Server 2008 con SP2 y [actualización de la plataforma para Windows server 2008](https://msdn.microsoft.com/library/dd378748.aspx)</span><span class="sxs-lookup"><span data-stu-id="e6f39-138">Windows Server 2008 with SP2 and [Platform Update for Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx)</span></span><br/> |
| <span data-ttu-id="e6f39-139">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="e6f39-139">Windows SDK</span></span>              | <span data-ttu-id="e6f39-140">7.0</span><span class="sxs-lookup"><span data-stu-id="e6f39-140">7.0</span></span>                                                                                                                                                                      |
| <span data-ttu-id="e6f39-141">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="e6f39-141">Visual Studio</span></span>            | <span data-ttu-id="e6f39-142">2008</span><span class="sxs-lookup"><span data-stu-id="e6f39-142">2008</span></span>                                                                                                                                                                     |
| <span data-ttu-id="e6f39-143">Archivos de encabezado y IDL</span><span class="sxs-lookup"><span data-stu-id="e6f39-143">Header and IDL files</span></span>     | <span data-ttu-id="e6f39-144">uiribbon. h, uiribbon. idl</span><span class="sxs-lookup"><span data-stu-id="e6f39-144">uiribbon.h, uiribbon.idl</span></span>                                                                                                                                                 |



 

> [!Note]  
> <span data-ttu-id="e6f39-145">La [actualización de la plataforma para Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) y la [actualización de la plataforma para Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) son conjuntos de bibliotecas en tiempo de ejecución que permiten a los desarrolladores tener como destino aplicaciones de cinta de Windows para Windows Vista y Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="e6f39-145">The [Platform Update for Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) and [Platform Update for Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) are sets of run-time libraries that enable developers to target Windows Ribbon applications to both Windows Vista and Windows Server 2008.</span></span> <span data-ttu-id="e6f39-146">Las actualizaciones de la plataforma estarán disponibles para todos los clientes de Windows Vista y Windows Server 2008 a través de Windows Update.</span><span class="sxs-lookup"><span data-stu-id="e6f39-146">The platform updates will be available to all Windows Vista and Windows Server 2008 customers through Windows Update.</span></span> <span data-ttu-id="e6f39-147">Las aplicaciones de terceros que requieren la [actualización de la plataforma para Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) o la [actualización de la plataforma para Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) pueden detectar Windows Update detectar si está instalado el requerido actualizado; en caso contrario, Windows Update lo descargará e instalará en segundo plano.</span><span class="sxs-lookup"><span data-stu-id="e6f39-147">Third-party applications that require [Platform Update for Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) or [Platform Update for Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) can have Windows Update detect whether the required updated is installed; if it is not, Windows Update will download and install it in the background.</span></span>

 

 

 





