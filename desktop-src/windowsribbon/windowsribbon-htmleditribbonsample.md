---
title: Ejemplo HTMLEditRibbon
description: En este ejemplo de código se muestra el marcado y el código necesarios para migrar una aplicación Microsoft Foundation Classes existente (MFC) para usar la cinta Windows opciones.
ms.assetid: 1505aaea-76d2-47bc-bdc9-12e761da93f9
ms.topic: article
ms.date: 07/13/2021
ms.openlocfilehash: cfe75d13a69e0122766e51a00bcb1b15d52eab4e
ms.sourcegitcommit: 63c93e0ad0b48d60b11008767196718feb475cb0
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/13/2021
ms.locfileid: "113691714"
---
# <a name="htmleditribbon-sample"></a><span data-ttu-id="b7e31-103">Ejemplo HTMLEditRibbon</span><span class="sxs-lookup"><span data-stu-id="b7e31-103">HTMLEditRibbon Sample</span></span>

<span data-ttu-id="b7e31-104">En este ejemplo de código se muestra el marcado y el código necesarios para migrar una aplicación Microsoft Foundation Classes existente (MFC) para usar la cinta Windows opciones.</span><span class="sxs-lookup"><span data-stu-id="b7e31-104">This code sample shows markup and code required to migrate an existing Microsoft Foundation Classes (MFC) application to use the Windows Ribbon.</span></span> <span data-ttu-id="b7e31-105">Se creó tomando la aplicación de ejemplo HTMLEdit de MFC existente y modificando su código y recursos para usar la Windows cinta de opciones.</span><span class="sxs-lookup"><span data-stu-id="b7e31-105">It was created by taking the existing MFC HTMLEdit sample application and modifying its code and resources to use the Windows Ribbon.</span></span>

- [<span data-ttu-id="b7e31-106">Comentarios:</span><span class="sxs-lookup"><span data-stu-id="b7e31-106">Remarks</span></span>](#remarks)
- [<span data-ttu-id="b7e31-107">Uso</span><span class="sxs-lookup"><span data-stu-id="b7e31-107">Usage</span></span>](#usage)
  - [<span data-ttu-id="b7e31-108">Compilar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="b7e31-108">Building the Sample</span></span>](#building-the-sample)
  - [<span data-ttu-id="b7e31-109">Ejecución del ejemplo</span><span class="sxs-lookup"><span data-stu-id="b7e31-109">Running the Sample</span></span>](#running-the-sample)
- [<span data-ttu-id="b7e31-110">Soporte técnico</span><span class="sxs-lookup"><span data-stu-id="b7e31-110">Support</span></span>](#support)
- [<span data-ttu-id="b7e31-111">Requisitos mínimos</span><span class="sxs-lookup"><span data-stu-id="b7e31-111">Minimum Requirements</span></span>](#minimum-requirements)

## <a name="remarks"></a><span data-ttu-id="b7e31-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b7e31-112">Remarks</span></span>

<span data-ttu-id="b7e31-113">Para obtener el ejemplo mfc, vea [HTMLEdit Sample: Wraps the Internet Explorer Control de edición MSHTML](https://msdn.microsoft.com/library/ea8hhwb6(VS.80).aspx).</span><span class="sxs-lookup"><span data-stu-id="b7e31-113">For the MFC sample, see [HTMLEdit Sample: Wraps the Internet Explorer MSHTML Editing Control](https://msdn.microsoft.com/library/ea8hhwb6(VS.80).aspx).</span></span>

## <a name="usage"></a><span data-ttu-id="b7e31-114">Uso</span><span class="sxs-lookup"><span data-stu-id="b7e31-114">Usage</span></span>

<span data-ttu-id="b7e31-115">Los ejemplos Windows marco de la cinta de opciones se pueden descargar como proyectos de Microsoft Visual Studio independientes desde el Centro de descarga de [Microsoft](https://www.microsoft.com/download/details.aspx?id=9620) o instalarse como parte del Kit de desarrollo de [software (SDK)](https://developer.microsoft.com/windows/downloads/sdk-archive/)de Windows .</span><span class="sxs-lookup"><span data-stu-id="b7e31-115">The Windows Ribbon framework samples can be downloaded as standalone Microsoft Visual Studio projects from the [Microsoft Download Center](https://www.microsoft.com/download/details.aspx?id=9620) or installed as part of the [Windows Software Development Kit (SDK)](https://developer.microsoft.com/windows/downloads/sdk-archive/).</span></span>

- <span data-ttu-id="b7e31-116">Windows Kit de desarrollo de software (SDK) (ruta de instalación estándar): %ProgramFiles% SDK de Microsoft Windows número de versión \\ \\ Ejemplos \\ \[ \] \\ \\ winui \\ WindowsRibbon \\ HTMLEditRibbon</span><span class="sxs-lookup"><span data-stu-id="b7e31-116">Windows Software Development Kit (SDK) (standard installation path): %ProgramFiles%\\Microsoft SDKs\\Windows\\\[version number\]\\Samples\\winui\\WindowsRibbon\\HTMLEditRibbon</span></span>

### <a name="building-the-sample"></a><span data-ttu-id="b7e31-117">Generar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="b7e31-117">Building the Sample</span></span>

<span data-ttu-id="b7e31-118">Descargue el ejemplo.</span><span class="sxs-lookup"><span data-stu-id="b7e31-118">Download the sample.</span></span>

<span data-ttu-id="b7e31-119">Instale el SDK Windows para Windows 7 y abra su ventana de comandos del entorno de compilación.</span><span class="sxs-lookup"><span data-stu-id="b7e31-119">Install the Windows SDK for Windows 7 and open its build environment command window.</span></span> <span data-ttu-id="b7e31-120">En el menú Inicio, elija Todos los programas, Microsoft Windows SDK y haga clic en Shell CMD.</span><span class="sxs-lookup"><span data-stu-id="b7e31-120">On the Start menu, point to All Programs, Microsoft Windows SDK, and then click CMD Shell.</span></span>

<span data-ttu-id="b7e31-121">Para generar el ejemplo en la ventana de comados del entorno de compilación, vaya al directorio de origen del ejemplo.</span><span class="sxs-lookup"><span data-stu-id="b7e31-121">To build the sample from the build environment command window, go to the source directory of the sample.</span></span> <span data-ttu-id="b7e31-122">En el símbolo del sistema, escriba MSBUILD.</span><span class="sxs-lookup"><span data-stu-id="b7e31-122">At the command prompt, type MSBUILD.</span></span>

<span data-ttu-id="b7e31-123">Para compilar el ejemplo en Microsoft Visual Studio, cargue la solución de ejemplo o el archivo del proyecto y presione CTRL+MAYÚS+B.</span><span class="sxs-lookup"><span data-stu-id="b7e31-123">To build the sample in Microsoft Visual Studio, load the sample solution or project file and then press CTRL+SHIFT+B.</span></span>

### <a name="running-the-sample"></a><span data-ttu-id="b7e31-124">Ejecutar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="b7e31-124">Running the Sample</span></span>

<span data-ttu-id="b7e31-125">Para ejecutar el ejemplo desde la ventana de comandos del entorno de compilación, ejecute los archivos .exe en la carpeta Bin Debug o Bin Release contenida en la carpeta \\ \\ de origen de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="b7e31-125">To run the sample from the build environment command window, execute the .exe files in the Bin\\Debug or Bin\\Release folder contained in the sample source folder.</span></span>

<span data-ttu-id="b7e31-126">Para ejecutar el ejemplo compilado con depuración en Visual Studio, presione F5.</span><span class="sxs-lookup"><span data-stu-id="b7e31-126">To run the compiled sample with debugging in Visual Studio, press F5.</span></span>

## <a name="support"></a><span data-ttu-id="b7e31-127">Compatibilidad</span><span class="sxs-lookup"><span data-stu-id="b7e31-127">Support</span></span>

<span data-ttu-id="b7e31-128">El [foro Windows desarrollo de la cinta](https://social.msdn.microsoft.com/Forums/windowsdesktop/home?forum=windowsribbondevelopment) de opciones está disponible para analizar temas y hacer preguntas relacionadas con el desarrollo de Windows de cinta de opciones.</span><span class="sxs-lookup"><span data-stu-id="b7e31-128">The [Windows Ribbon Development Forum](https://social.msdn.microsoft.com/Forums/windowsdesktop/home?forum=windowsribbondevelopment) is available to discuss topics and ask questions related to developing Windows Ribbon applications.</span></span>

## <a name="minimum-requirements"></a><span data-ttu-id="b7e31-129">Requisitos mínimos</span><span class="sxs-lookup"><span data-stu-id="b7e31-129">Minimum Requirements</span></span>



| <span data-ttu-id="b7e31-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="b7e31-130">Requirement</span></span> | <span data-ttu-id="b7e31-131">Valor</span><span class="sxs-lookup"><span data-stu-id="b7e31-131">Value</span></span> |
|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b7e31-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b7e31-132">Minimum supported client</span></span> | <span data-ttu-id="b7e31-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="b7e31-133">Windows 7</span></span><br/> <span data-ttu-id="b7e31-134">Windows Vista con Service Pack 2 (SP2) y [actualización de plataforma para Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx)</span><span class="sxs-lookup"><span data-stu-id="b7e31-134">Windows Vista with Service Pack 2 (SP2) and [Platform Update for Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx)</span></span><br/>         |
| <span data-ttu-id="b7e31-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b7e31-135">Minimum supported server</span></span> | <span data-ttu-id="b7e31-136">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b7e31-136">Windows Server 2008 R2</span></span><br/> <span data-ttu-id="b7e31-137">Windows Server 2008 con SP2 y actualización de plataforma [para Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx)</span><span class="sxs-lookup"><span data-stu-id="b7e31-137">Windows Server 2008 with SP2 and [Platform Update for Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx)</span></span><br/> |
| <span data-ttu-id="b7e31-138">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="b7e31-138">Windows SDK</span></span>              | <span data-ttu-id="b7e31-139">7.0</span><span class="sxs-lookup"><span data-stu-id="b7e31-139">7.0</span></span>                                                                                                                                                                      |
| <span data-ttu-id="b7e31-140">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="b7e31-140">Visual Studio</span></span>            | <span data-ttu-id="b7e31-141">2008</span><span class="sxs-lookup"><span data-stu-id="b7e31-141">2008</span></span>                                                                                                                                                                     |
| <span data-ttu-id="b7e31-142">Archivos de encabezado e IDL</span><span class="sxs-lookup"><span data-stu-id="b7e31-142">Header and IDL files</span></span>     | <span data-ttu-id="b7e31-143">uiribbon.h, uiribbon.idl</span><span class="sxs-lookup"><span data-stu-id="b7e31-143">uiribbon.h, uiribbon.idl</span></span>                                                                                                                                                 |



 

> [!Note]  
> <span data-ttu-id="b7e31-144">La actualización de plataforma para [Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) y la actualización de plataforma para Windows [Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) son conjuntos de bibliotecas en tiempo de ejecución que permiten a los desarrolladores dirigir aplicaciones de la cinta de opciones de Windows a Windows Vista y Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="b7e31-144">The [Platform Update for Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) and [Platform Update for Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) are sets of run-time libraries that enable developers to target Windows Ribbon applications to both Windows Vista and Windows Server 2008.</span></span> <span data-ttu-id="b7e31-145">Las actualizaciones de la plataforma estarán disponibles para todos los Windows Vista y Windows Server 2008 a través de Windows Update.</span><span class="sxs-lookup"><span data-stu-id="b7e31-145">The platform updates will be available to all Windows Vista and Windows Server 2008 customers through Windows Update.</span></span> <span data-ttu-id="b7e31-146">Las aplicaciones de terceros que requieren Actualización de plataforma para [Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) o Actualización de plataforma para Windows [Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) pueden hacer que Windows Update detecte si está instalada la actualización necesaria; Si no es así, Windows Update la descargará e instalará en segundo plano.</span><span class="sxs-lookup"><span data-stu-id="b7e31-146">Third-party applications that require [Platform Update for Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) or [Platform Update for Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) can have Windows Update detect whether the required updated is installed; if it is not, Windows Update will download and install it in the background.</span></span>

 

 

 





