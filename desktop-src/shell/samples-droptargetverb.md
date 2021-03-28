---
description: Muestra cómo implementar un verbo de Shell mediante el método DropTarget.
title: Ejemplo de verbo DropTarget
ms.topic: article
ms.date: 05/31/2018
ms.assetid: BEAD20C9-B01A-48aa-A85A-B7171383FBDF
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 1f737c951c5bd588760dbb716859c04c0dc062fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985627"
---
# <a name="droptarget-verb-sample"></a><span data-ttu-id="2191d-103">Ejemplo de verbo DropTarget</span><span class="sxs-lookup"><span data-stu-id="2191d-103">DropTarget Verb Sample</span></span>

<span data-ttu-id="2191d-104">Muestra cómo implementar un verbo de Shell mediante el método DropTarget.</span><span class="sxs-lookup"><span data-stu-id="2191d-104">Demonstrates how to implement a Shell verb using the DropTarget method.</span></span>

<span data-ttu-id="2191d-105">En este tema se incluyen las siguientes secciones.</span><span class="sxs-lookup"><span data-stu-id="2191d-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="2191d-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="2191d-106">Description</span></span>](#description)
-   [<span data-ttu-id="2191d-107">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2191d-107">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="2191d-108">Descargar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="2191d-108">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="2191d-109">Compilar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="2191d-109">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="2191d-110">Ejecutar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="2191d-110">Running the Sample</span></span>](#running-the-sample)

## <a name="description"></a><span data-ttu-id="2191d-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="2191d-111">Description</span></span>

<span data-ttu-id="2191d-112">Este ejemplo muestra cómo implementar un verbo de Shell mediante el método DropTarget.</span><span class="sxs-lookup"><span data-stu-id="2191d-112">This sample shows how to implement a Shell verb using the DropTarget method.</span></span> <span data-ttu-id="2191d-113">Este método es preferible para implementaciones de verbo que deben funcionar en Windows XP.</span><span class="sxs-lookup"><span data-stu-id="2191d-113">This method is preferred for verb implementations that must work on Windows XP.</span></span> <span data-ttu-id="2191d-114">En este ejemplo se implementa un objeto de modelo de objetos componentes (COM) de servidor local independiente, pero se espera que la implementación del verbo se integre en las aplicaciones existentes.</span><span class="sxs-lookup"><span data-stu-id="2191d-114">This sample implements a standalone local server Component Object Model (COM) object but it is expected that the verb implementation will be integrated into existing applications.</span></span> <span data-ttu-id="2191d-115">Para ello, el objeto de aplicación principal registra un generador de clases para sí mismo.</span><span class="sxs-lookup"><span data-stu-id="2191d-115">To do so, your main application object registers a class factory for itself.</span></span> <span data-ttu-id="2191d-116">Ese objeto implementa [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) para los verbos de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="2191d-116">That object implements [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) for your application's verbs.</span></span> <span data-ttu-id="2191d-117">Tenga en cuenta que COM inicia la aplicación si aún no se está ejecutando pero se conecta a una instancia en ejecución de la aplicación si hay alguna.</span><span class="sxs-lookup"><span data-stu-id="2191d-117">Note that COM launches your application if it is not already running but connects to a running instance of your application if one is present.</span></span>

## <a name="requirements"></a><span data-ttu-id="2191d-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2191d-118">Requirements</span></span>



| <span data-ttu-id="2191d-119">Producto</span><span class="sxs-lookup"><span data-stu-id="2191d-119">Product</span></span>                                | <span data-ttu-id="2191d-120">Versión mínima del producto</span><span class="sxs-lookup"><span data-stu-id="2191d-120">Minimum Product Version</span></span> |
|----------------------------------------|-------------------------|
| <span data-ttu-id="2191d-121">Windows</span><span class="sxs-lookup"><span data-stu-id="2191d-121">Windows</span></span>                                | <span data-ttu-id="2191d-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2191d-122">Windows Vista</span></span>           |
| <span data-ttu-id="2191d-123">Kit de desarrollo de software de Windows (SDK)</span><span class="sxs-lookup"><span data-stu-id="2191d-123">Windows Software Development Kit (SDK)</span></span> | <span data-ttu-id="2191d-124">7.0</span><span class="sxs-lookup"><span data-stu-id="2191d-124">7.0</span></span>                     |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="2191d-125">Descargar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="2191d-125">Downloading the Sample</span></span>

| <span data-ttu-id="2191d-126">Ubicación</span><span class="sxs-lookup"><span data-stu-id="2191d-126">Location</span></span>      | <span data-ttu-id="2191d-127">URL de ruta de acceso</span><span class="sxs-lookup"><span data-stu-id="2191d-127">Path URL</span></span>                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2191d-128">GitHub</span><span class="sxs-lookup"><span data-stu-id="2191d-128">GitHub</span></span>  | [<span data-ttu-id="2191d-129">Ejemplo de DropTargetVerb</span><span class="sxs-lookup"><span data-stu-id="2191d-129">DropTargetVerb sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/DropTargetVerb) |

## <a name="building-the-sample"></a><span data-ttu-id="2191d-130">Generar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="2191d-130">Building the Sample</span></span>

<span data-ttu-id="2191d-131">Para compilar el ejemplo desde el símbolo del sistema:</span><span class="sxs-lookup"><span data-stu-id="2191d-131">To build the sample from the command prompt:</span></span>

1.  <span data-ttu-id="2191d-132">Abra la ventana del símbolo del sistema y navegue hasta el directorio del proyecto **DropTargetVerb** .</span><span class="sxs-lookup"><span data-stu-id="2191d-132">Open the command prompt window and navigate to the **DropTargetVerb** project directory.</span></span>
2.  <span data-ttu-id="2191d-133">Escriba `msbuild DropTargetVerb.sln`.</span><span class="sxs-lookup"><span data-stu-id="2191d-133">Enter `msbuild DropTargetVerb.sln`.</span></span>

<span data-ttu-id="2191d-134">Para compilar el ejemplo mediante Microsoft Visual Studio (preferido):</span><span class="sxs-lookup"><span data-stu-id="2191d-134">To build the sample using Microsoft Visual Studio (preferred):</span></span>

1.  <span data-ttu-id="2191d-135">Abra el explorador de Windows y navegue hasta el directorio del proyecto **DropTargetVerb** .</span><span class="sxs-lookup"><span data-stu-id="2191d-135">Open Windows Explorer and navigate to the **DropTargetVerb** project directory.</span></span>
2.  <span data-ttu-id="2191d-136">Haga doble clic en el icono del archivo DropTargetVerb. sln para abrir el proyecto en Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="2191d-136">Double-click the icon for the DropTargetVerb.sln file to open the project in Visual Studio.</span></span>
3.  <span data-ttu-id="2191d-137">En el menú **compilar** , seleccione **compilar solución**.</span><span class="sxs-lookup"><span data-stu-id="2191d-137">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="2191d-138">Ejecutar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="2191d-138">Running the Sample</span></span>

1.  <span data-ttu-id="2191d-139">Navegue hasta el directorio que contiene el nuevo ejecutable, mediante el símbolo del sistema o el explorador de Windows.</span><span class="sxs-lookup"><span data-stu-id="2191d-139">Navigate to the directory that contains the new executable, using the command prompt or Windows Explorer.</span></span>
2.  <span data-ttu-id="2191d-140">En la línea de comandos, escriba `DropTargetVerb.exe` .</span><span class="sxs-lookup"><span data-stu-id="2191d-140">At the command line, enter `DropTargetVerb.exe`.</span></span> <span data-ttu-id="2191d-141">Como alternativa, en el explorador de Windows, haga doble clic en el icono de DropTargetVerb.exe.</span><span class="sxs-lookup"><span data-stu-id="2191d-141">Alternatively, from Windows Explorer double-click the icon for DropTargetVerb.exe.</span></span>
3.  <span data-ttu-id="2191d-142">Siga las instrucciones del cuadro de diálogo que aparece</span><span class="sxs-lookup"><span data-stu-id="2191d-142">Follow the instructions in the displayed dialog</span></span>

 

 
