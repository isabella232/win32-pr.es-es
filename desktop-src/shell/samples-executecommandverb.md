---
description: Muestra cómo implementar un verbo de Shell mediante el método ExecuteCommand.
title: Ejemplo de verbo Execute Command
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 0418318A-3E62-4690-AFB3-9B4A391C537E
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 2deeb63fc6648d07b3d870888d6d2eabc6fb0490
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279515"
---
# <a name="execute-command-verb-sample"></a><span data-ttu-id="0f660-103">Ejemplo de verbo Execute Command</span><span class="sxs-lookup"><span data-stu-id="0f660-103">Execute Command Verb Sample</span></span>

<span data-ttu-id="0f660-104">Muestra cómo implementar un verbo de Shell mediante el método ExecuteCommand.</span><span class="sxs-lookup"><span data-stu-id="0f660-104">Demonstrates how to implement a Shell verb using the ExecuteCommand method.</span></span>

<span data-ttu-id="0f660-105">En este tema se incluyen las siguientes secciones.</span><span class="sxs-lookup"><span data-stu-id="0f660-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="0f660-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="0f660-106">Description</span></span>](#description)
-   [<span data-ttu-id="0f660-107">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0f660-107">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="0f660-108">Descargar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="0f660-108">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="0f660-109">Compilar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="0f660-109">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="0f660-110">Ejecutar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="0f660-110">Running the Sample</span></span>](#running-the-sample)

## <a name="description"></a><span data-ttu-id="0f660-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="0f660-111">Description</span></span>

<span data-ttu-id="0f660-112">Este método es preferible para implementaciones de verbo porque proporciona la máxima flexibilidad, es simple y admite la activación fuera de proceso.</span><span class="sxs-lookup"><span data-stu-id="0f660-112">This method is preferred for verb implementations because it provides the most flexibility, is simple, and supports out-of-process activation.</span></span> <span data-ttu-id="0f660-113">En este ejemplo se implementa un objeto de modelo de objetos componentes (COM) de servidor local independiente, pero se espera que la implementación del verbo se integre en las aplicaciones existentes.</span><span class="sxs-lookup"><span data-stu-id="0f660-113">This sample implements a standalone, local server Component Object Model (COM) object, but it is expected that the verb implementation will be integrated into existing applications.</span></span> <span data-ttu-id="0f660-114">Para ello, el objeto de aplicación principal debe registrar un generador de clases para sí mismo.</span><span class="sxs-lookup"><span data-stu-id="0f660-114">To do so, your main application object must register a class factory for itself.</span></span> <span data-ttu-id="0f660-115">Ese objeto implementa [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) para los verbos de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="0f660-115">That object implements [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) for your application's verbs.</span></span> <span data-ttu-id="0f660-116">Tenga en cuenta que COM inicia la aplicación si aún no se está ejecutando pero se conecta a una instancia en ejecución de la aplicación si hay alguna.</span><span class="sxs-lookup"><span data-stu-id="0f660-116">Note that COM launches your application if it is not already running but connects to a running instance of your application if one is present.</span></span>

## <a name="requirements"></a><span data-ttu-id="0f660-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0f660-117">Requirements</span></span>



| <span data-ttu-id="0f660-118">Producto</span><span class="sxs-lookup"><span data-stu-id="0f660-118">Product</span></span>                                | <span data-ttu-id="0f660-119">Versión mínima del producto</span><span class="sxs-lookup"><span data-stu-id="0f660-119">Minimum Product Version</span></span> |
|----------------------------------------|-------------------------|
| <span data-ttu-id="0f660-120">Windows</span><span class="sxs-lookup"><span data-stu-id="0f660-120">Windows</span></span>                                | <span data-ttu-id="0f660-121">Windows 7</span><span class="sxs-lookup"><span data-stu-id="0f660-121">Windows 7</span></span>               |
| <span data-ttu-id="0f660-122">Kit de desarrollo de software de Windows (SDK)</span><span class="sxs-lookup"><span data-stu-id="0f660-122">Windows Software Development Kit (SDK)</span></span> | <span data-ttu-id="0f660-123">7.0</span><span class="sxs-lookup"><span data-stu-id="0f660-123">7.0</span></span>                     |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="0f660-124">Descargar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="0f660-124">Downloading the Sample</span></span>

| <span data-ttu-id="0f660-125">Ubicación</span><span class="sxs-lookup"><span data-stu-id="0f660-125">Location</span></span>      | <span data-ttu-id="0f660-126">URL de ruta de acceso</span><span class="sxs-lookup"><span data-stu-id="0f660-126">Path URL</span></span>                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0f660-127">GitHub</span><span class="sxs-lookup"><span data-stu-id="0f660-127">GitHub</span></span>  | [<span data-ttu-id="0f660-128">Ejemplo de ExecuteCommandVerb</span><span class="sxs-lookup"><span data-stu-id="0f660-128">ExecuteCommandVerb sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/ExecuteCommandVerb) |

## <a name="building-the-sample"></a><span data-ttu-id="0f660-129">Generar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="0f660-129">Building the Sample</span></span>

<span data-ttu-id="0f660-130">Para compilar el ejemplo desde el símbolo del sistema:</span><span class="sxs-lookup"><span data-stu-id="0f660-130">To build the sample from the command prompt:</span></span>

1.  <span data-ttu-id="0f660-131">Abra la ventana del símbolo del sistema y navegue hasta el directorio del proyecto **ExecuteCommandVerb** .</span><span class="sxs-lookup"><span data-stu-id="0f660-131">Open the command prompt window and navigate to the **ExecuteCommandVerb** project directory.</span></span>
2.  <span data-ttu-id="0f660-132">Escriba `msbuild ExecuteCommand.sln`.</span><span class="sxs-lookup"><span data-stu-id="0f660-132">Enter `msbuild ExecuteCommand.sln`.</span></span>

<span data-ttu-id="0f660-133">Para compilar el ejemplo mediante Microsoft Visual Studio (preferido):</span><span class="sxs-lookup"><span data-stu-id="0f660-133">To build the sample using Microsoft Visual Studio (preferred):</span></span>

1.  <span data-ttu-id="0f660-134">Abra el explorador de Windows y navegue hasta el directorio del proyecto **ExecuteCommandVerb** .</span><span class="sxs-lookup"><span data-stu-id="0f660-134">Open Windows Explorer and navigate to the **ExecuteCommandVerb** project directory.</span></span>
2.  <span data-ttu-id="0f660-135">Haga doble clic en el icono del archivo ExecuteCommand. sln para abrir el proyecto en Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="0f660-135">Double-click the icon for the ExecuteCommand.sln file to open the project in Visual Studio.</span></span>
3.  <span data-ttu-id="0f660-136">En el menú **compilar** , seleccione **compilar solución**.</span><span class="sxs-lookup"><span data-stu-id="0f660-136">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="0f660-137">Ejecutar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="0f660-137">Running the Sample</span></span>

1.  <span data-ttu-id="0f660-138">Navegue hasta el directorio que contiene el nuevo ejecutable, mediante el símbolo del sistema o el explorador de Windows.</span><span class="sxs-lookup"><span data-stu-id="0f660-138">Navigate to the directory that contains the new executable, using the command prompt or Windows Explorer.</span></span>
2.  <span data-ttu-id="0f660-139">En la línea de comandos, escriba `ExecuteCommand.exe` .</span><span class="sxs-lookup"><span data-stu-id="0f660-139">At the command line, enter `ExecuteCommand.exe`.</span></span> <span data-ttu-id="0f660-140">Como alternativa, en el explorador de Windows, haga doble clic en el icono de ExecuteCommand.exe.</span><span class="sxs-lookup"><span data-stu-id="0f660-140">Alternatively, from Windows Explorer double-click the icon for ExecuteCommand.exe.</span></span>
3.  <span data-ttu-id="0f660-141">Siga las instrucciones del cuadro de diálogo que aparece</span><span class="sxs-lookup"><span data-stu-id="0f660-141">Follow the instructions in the displayed dialog</span></span>

 

 
