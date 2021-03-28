---
description: Muestra cómo crear un verbo que opera en elementos de Shell y contenedores que reproducen elementos o agregan elementos a una cola.
title: Ejemplo de verbo del reproductor
ms.topic: article
ms.date: 05/31/2018
ms.assetid: ABD905DD-F216-495e-A052-E43D93DD3D6B
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: b8346d54bfb99c5f1870812775b31097d850025f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277226"
---
# <a name="player-verb-sample"></a><span data-ttu-id="cedb0-103">Ejemplo de verbo del reproductor</span><span class="sxs-lookup"><span data-stu-id="cedb0-103">Player Verb Sample</span></span>

<span data-ttu-id="cedb0-104">Muestra cómo crear un verbo que opera en elementos de Shell y contenedores que reproducen elementos o agregan elementos a una cola.</span><span class="sxs-lookup"><span data-stu-id="cedb0-104">Demonstrates how to create a verb that operates on Shell items and containers which plays items or adds items to a queue.</span></span> <span data-ttu-id="cedb0-105">Este ejemplo es especialmente útil para las aplicaciones multimedia.</span><span class="sxs-lookup"><span data-stu-id="cedb0-105">This sample is particularly useful for media applications.</span></span>

<span data-ttu-id="cedb0-106">En este tema se incluyen las siguientes secciones.</span><span class="sxs-lookup"><span data-stu-id="cedb0-106">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="cedb0-107">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cedb0-107">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="cedb0-108">Descargar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="cedb0-108">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="cedb0-109">Compilar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="cedb0-109">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="cedb0-110">Ejecutar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="cedb0-110">Running the Sample</span></span>](#running-the-sample)

## <a name="requirements"></a><span data-ttu-id="cedb0-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cedb0-111">Requirements</span></span>



| <span data-ttu-id="cedb0-112">Producto</span><span class="sxs-lookup"><span data-stu-id="cedb0-112">Product</span></span>                                | <span data-ttu-id="cedb0-113">Versión mínima del producto</span><span class="sxs-lookup"><span data-stu-id="cedb0-113">Minimum Product Version</span></span> |
|----------------------------------------|-------------------------|
| <span data-ttu-id="cedb0-114">Windows</span><span class="sxs-lookup"><span data-stu-id="cedb0-114">Windows</span></span>                                | <span data-ttu-id="cedb0-115">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cedb0-115">Windows Vista</span></span>           |
| <span data-ttu-id="cedb0-116">Kit de desarrollo de software de Windows (SDK)</span><span class="sxs-lookup"><span data-stu-id="cedb0-116">Windows Software Development Kit (SDK)</span></span> | <span data-ttu-id="cedb0-117">7.0</span><span class="sxs-lookup"><span data-stu-id="cedb0-117">7.0</span></span>                     |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="cedb0-118">Descargar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="cedb0-118">Downloading the Sample</span></span>

| <span data-ttu-id="cedb0-119">Ubicación</span><span class="sxs-lookup"><span data-stu-id="cedb0-119">Location</span></span>      | <span data-ttu-id="cedb0-120">URL de ruta de acceso</span><span class="sxs-lookup"><span data-stu-id="cedb0-120">Path URL</span></span>                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cedb0-121">GitHub</span><span class="sxs-lookup"><span data-stu-id="cedb0-121">GitHub</span></span>  | [<span data-ttu-id="cedb0-122">Ejemplo de PlayerVerb</span><span class="sxs-lookup"><span data-stu-id="cedb0-122">PlayerVerb sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/PlayerVerbSample) |

## <a name="building-the-sample"></a><span data-ttu-id="cedb0-123">Generar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="cedb0-123">Building the Sample</span></span>

<span data-ttu-id="cedb0-124">Para compilar el ejemplo desde el símbolo del sistema:</span><span class="sxs-lookup"><span data-stu-id="cedb0-124">To build the sample from the command prompt:</span></span>

1.  <span data-ttu-id="cedb0-125">Abra la ventana del símbolo del sistema y navegue hasta el directorio del proyecto **PlayerVerbSample** .</span><span class="sxs-lookup"><span data-stu-id="cedb0-125">Open the command prompt window and navigate to the **PlayerVerbSample** project directory.</span></span>
2.  <span data-ttu-id="cedb0-126">Escriba `msbuild PlayerVerbSample.sln`.</span><span class="sxs-lookup"><span data-stu-id="cedb0-126">Enter `msbuild PlayerVerbSample.sln`.</span></span>

<span data-ttu-id="cedb0-127">Para compilar el ejemplo mediante Microsoft Visual Studio (preferido):</span><span class="sxs-lookup"><span data-stu-id="cedb0-127">To build the sample using Microsoft Visual Studio (preferred):</span></span>

1.  <span data-ttu-id="cedb0-128">Abra el explorador de Windows y navegue hasta el directorio del proyecto **PlayerVerbSample** .</span><span class="sxs-lookup"><span data-stu-id="cedb0-128">Open Windows Explorer and navigate to the **PlayerVerbSample** project directory.</span></span>
2.  <span data-ttu-id="cedb0-129">Haga doble clic en el icono del archivo PlayerVerbSample. sln para abrir el proyecto en Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="cedb0-129">Double-click the icon for the PlayerVerbSample.sln file to open the project in Visual Studio.</span></span>
3.  <span data-ttu-id="cedb0-130">En el menú **compilar** , seleccione **compilar solución**.</span><span class="sxs-lookup"><span data-stu-id="cedb0-130">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="cedb0-131">Ejecutar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="cedb0-131">Running the Sample</span></span>

1.  <span data-ttu-id="cedb0-132">Navegue hasta el directorio que contiene el nuevo ejecutable, mediante el símbolo del sistema o el explorador de Windows.</span><span class="sxs-lookup"><span data-stu-id="cedb0-132">Navigate to the directory that contains the new executable, using the command prompt or Windows Explorer.</span></span>
2.  <span data-ttu-id="cedb0-133">En la línea de comandos, escriba `PlayerVerbSample.exe` .</span><span class="sxs-lookup"><span data-stu-id="cedb0-133">At the command line, enter `PlayerVerbSample.exe`.</span></span> <span data-ttu-id="cedb0-134">Como alternativa, en el explorador de Windows, haga doble clic en el icono de PlayerVerbSample.exe.</span><span class="sxs-lookup"><span data-stu-id="cedb0-134">Alternatively, from Windows Explorer double-click the icon for PlayerVerbSample.exe.</span></span>
3.  <span data-ttu-id="cedb0-135">Seleccione `Register Verbs` en el cuadro de diálogo de **ejemplo del verbo de reproductor** .</span><span class="sxs-lookup"><span data-stu-id="cedb0-135">Select `Register Verbs` in the **Player Verb Sample** dialog.</span></span>
4.  <span data-ttu-id="cedb0-136">Haga clic con el botón secundario en elementos de imagen (archivo, carpeta o pila) en el explorador de Windows para agregarlos a una cola o reproducirlos en la aplicación de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="cedb0-136">Right-click picture items (file, folder, or stack) in Windows Explorer to add them to a queue or play them in the sample application.</span></span> <span data-ttu-id="cedb0-137">Usar elementos de música al cambiar el ejemplo para trabajar con música.</span><span class="sxs-lookup"><span data-stu-id="cedb0-137">Use music items when you change the sample to work with music.</span></span>

 

 



