---
description: Muestra cómo implementar un verbo de Shell mediante el método CreateProcess.
title: Ejemplo de verbo CreateProcess
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 2939BC36-35C0-4549-9971-742CBDA02547
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 8e52f251e12f0ca06bcb729407a7c8303836f9fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985826"
---
# <a name="createprocess-verb-sample"></a><span data-ttu-id="6fe8c-103">Ejemplo de verbo CreateProcess</span><span class="sxs-lookup"><span data-stu-id="6fe8c-103">CreateProcess Verb Sample</span></span>

<span data-ttu-id="6fe8c-104">Muestra cómo implementar un verbo de Shell mediante el método CreateProcess.</span><span class="sxs-lookup"><span data-stu-id="6fe8c-104">Demonstrates how to implement a Shell verb using the CreateProcess method.</span></span>

<span data-ttu-id="6fe8c-105">En este tema se incluyen las siguientes secciones.</span><span class="sxs-lookup"><span data-stu-id="6fe8c-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="6fe8c-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="6fe8c-106">Description</span></span>](#description)
-   [<span data-ttu-id="6fe8c-107">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6fe8c-107">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="6fe8c-108">Descargar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="6fe8c-108">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="6fe8c-109">Compilar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="6fe8c-109">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="6fe8c-110">Ejecutar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="6fe8c-110">Running the Sample</span></span>](#running-the-sample)

## <a name="description"></a><span data-ttu-id="6fe8c-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="6fe8c-111">Description</span></span>

<span data-ttu-id="6fe8c-112">Los verbos basados en CreateProcess dependen de la ejecución de un ejecutable y de su pasa un argumento de línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="6fe8c-112">CreateProcess-based verbs depend on running a executable and passing it a command-line argument.</span></span> <span data-ttu-id="6fe8c-113">Este método no es tan eficaz como los métodos DropTarget y ExecuteCommand, pero logra el comportamiento deseado fuera de proceso.</span><span class="sxs-lookup"><span data-stu-id="6fe8c-113">This method is not as powerful as the DropTarget and ExecuteCommand methods but it does achieve the desirable out-of-process behavior.</span></span>

## <a name="requirements"></a><span data-ttu-id="6fe8c-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6fe8c-114">Requirements</span></span>



| <span data-ttu-id="6fe8c-115">Producto</span><span class="sxs-lookup"><span data-stu-id="6fe8c-115">Product</span></span>                                | <span data-ttu-id="6fe8c-116">Versión mínima del producto</span><span class="sxs-lookup"><span data-stu-id="6fe8c-116">Minimum Product Version</span></span> |
|----------------------------------------|-------------------------|
| <span data-ttu-id="6fe8c-117">Windows</span><span class="sxs-lookup"><span data-stu-id="6fe8c-117">Windows</span></span>                                | <span data-ttu-id="6fe8c-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6fe8c-118">Windows Vista</span></span>           |
| <span data-ttu-id="6fe8c-119">Kit de desarrollo de software de Windows (SDK)</span><span class="sxs-lookup"><span data-stu-id="6fe8c-119">Windows Software Development Kit (SDK)</span></span> | <span data-ttu-id="6fe8c-120">7.0</span><span class="sxs-lookup"><span data-stu-id="6fe8c-120">7.0</span></span>                     |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="6fe8c-121">Descargar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="6fe8c-121">Downloading the Sample</span></span>

| <span data-ttu-id="6fe8c-122">Ubicación</span><span class="sxs-lookup"><span data-stu-id="6fe8c-122">Location</span></span>      | <span data-ttu-id="6fe8c-123">URL de ruta de acceso</span><span class="sxs-lookup"><span data-stu-id="6fe8c-123">Path URL</span></span>                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6fe8c-124">GitHub</span><span class="sxs-lookup"><span data-stu-id="6fe8c-124">GitHub</span></span>  | [<span data-ttu-id="6fe8c-125">Ejemplo de CreateProcessVerb</span><span class="sxs-lookup"><span data-stu-id="6fe8c-125">CreateProcessVerb sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/CreateProcessVerb) |

## <a name="building-the-sample"></a><span data-ttu-id="6fe8c-126">Generar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="6fe8c-126">Building the Sample</span></span>

<span data-ttu-id="6fe8c-127">Para compilar el ejemplo desde el símbolo del sistema:</span><span class="sxs-lookup"><span data-stu-id="6fe8c-127">To build the sample from the command prompt:</span></span>

1.  <span data-ttu-id="6fe8c-128">Abra la ventana del símbolo del sistema y navegue hasta el directorio del proyecto **CreateProcessVerb** .</span><span class="sxs-lookup"><span data-stu-id="6fe8c-128">Open the command prompt window and navigate to the **CreateProcessVerb** project directory.</span></span>
2.  <span data-ttu-id="6fe8c-129">Escriba `msbuild CreateProcessVerb.sln`.</span><span class="sxs-lookup"><span data-stu-id="6fe8c-129">Enter `msbuild CreateProcessVerb.sln`.</span></span>

<span data-ttu-id="6fe8c-130">Para compilar el ejemplo mediante Microsoft Visual Studio (preferido):</span><span class="sxs-lookup"><span data-stu-id="6fe8c-130">To build the sample using Microsoft Visual Studio (preferred):</span></span>

1.  <span data-ttu-id="6fe8c-131">Abra el explorador de Windows y navegue hasta el directorio del proyecto **CreateProcessVerb** .</span><span class="sxs-lookup"><span data-stu-id="6fe8c-131">Open Windows Explorer and navigate to the **CreateProcessVerb** project directory.</span></span>
2.  <span data-ttu-id="6fe8c-132">Haga doble clic en el icono del archivo CreateProcessVerb. sln para abrir el proyecto en Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="6fe8c-132">Double-click the icon for the CreateProcessVerb.sln file to open the project in Visual Studio.</span></span>
3.  <span data-ttu-id="6fe8c-133">En el menú **compilar** , seleccione **compilar solución**.</span><span class="sxs-lookup"><span data-stu-id="6fe8c-133">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="6fe8c-134">Ejecutar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="6fe8c-134">Running the Sample</span></span>

1.  <span data-ttu-id="6fe8c-135">Navegue hasta el directorio que contiene el nuevo ejecutable, mediante el símbolo del sistema o el explorador de Windows.</span><span class="sxs-lookup"><span data-stu-id="6fe8c-135">Navigate to the directory that contains the new executable, using the command prompt or Windows Explorer.</span></span>
2.  <span data-ttu-id="6fe8c-136">En la línea de comandos, escriba `CreateProcessVerb.exe` .</span><span class="sxs-lookup"><span data-stu-id="6fe8c-136">At the command line, enter `CreateProcessVerb.exe`.</span></span> <span data-ttu-id="6fe8c-137">Como alternativa, en el explorador de Windows, haga doble clic en el icono de CreateProcessVerb.exe.</span><span class="sxs-lookup"><span data-stu-id="6fe8c-137">Alternatively, from Windows Explorer double-click the icon for CreateProcessVerb.exe.</span></span>
3.  <span data-ttu-id="6fe8c-138">Siga las instrucciones del cuadro de diálogo que aparece</span><span class="sxs-lookup"><span data-stu-id="6fe8c-138">Follow the instructions in the displayed dialog</span></span>

 

 



