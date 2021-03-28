---
description: Muestra cómo crear un verbo que opere en un elemento o contenedor de Shell seleccionado para crear una lista de reproducción.
title: Ejemplo de creador de listas de reproducción
ms.topic: article
ms.date: 05/31/2018
ms.assetid: B35B7A18-2163-4860-BC50-8918056C9F4A
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 5c5e4f6570faff459126a32ea4680d41a3b8302e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104986122"
---
# <a name="playlist-creator-sample"></a><span data-ttu-id="89969-103">Ejemplo de creador de listas de reproducción</span><span class="sxs-lookup"><span data-stu-id="89969-103">Playlist Creator Sample</span></span>

<span data-ttu-id="89969-104">Muestra cómo crear un verbo que opere en un elemento o contenedor de Shell seleccionado para crear una lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="89969-104">Demonstrates how to create a verb that operates on a selected Shell item or container to create a playlist.</span></span>

<span data-ttu-id="89969-105">En este tema se incluyen las siguientes secciones.</span><span class="sxs-lookup"><span data-stu-id="89969-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="89969-106">Requisitos</span><span class="sxs-lookup"><span data-stu-id="89969-106">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="89969-107">Descargar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="89969-107">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="89969-108">Compilar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="89969-108">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="89969-109">Ejecutar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="89969-109">Running the Sample</span></span>](#running-the-sample)

## <a name="requirements"></a><span data-ttu-id="89969-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="89969-110">Requirements</span></span>



| <span data-ttu-id="89969-111">Producto</span><span class="sxs-lookup"><span data-stu-id="89969-111">Product</span></span>                                | <span data-ttu-id="89969-112">Versión mínima del producto</span><span class="sxs-lookup"><span data-stu-id="89969-112">Minimum Product Version</span></span> |
|----------------------------------------|-------------------------|
| <span data-ttu-id="89969-113">Windows</span><span class="sxs-lookup"><span data-stu-id="89969-113">Windows</span></span>                                | <span data-ttu-id="89969-114">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="89969-114">Windows Vista</span></span>           |
| <span data-ttu-id="89969-115">Kit de desarrollo de software de Windows (SDK)</span><span class="sxs-lookup"><span data-stu-id="89969-115">Windows Software Development Kit (SDK)</span></span> | <span data-ttu-id="89969-116">7.0</span><span class="sxs-lookup"><span data-stu-id="89969-116">7.0</span></span>                     |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="89969-117">Descargar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="89969-117">Downloading the Sample</span></span>

| <span data-ttu-id="89969-118">Ubicación</span><span class="sxs-lookup"><span data-stu-id="89969-118">Location</span></span>      | <span data-ttu-id="89969-119">URL de ruta de acceso</span><span class="sxs-lookup"><span data-stu-id="89969-119">Path URL</span></span>                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="89969-120">GitHub</span><span class="sxs-lookup"><span data-stu-id="89969-120">GitHub</span></span>  | [<span data-ttu-id="89969-121">Ejemplo de PlaylistCreator</span><span class="sxs-lookup"><span data-stu-id="89969-121">PlaylistCreator sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/PlaylistCreator) |

## <a name="building-the-sample"></a><span data-ttu-id="89969-122">Generar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="89969-122">Building the Sample</span></span>

<span data-ttu-id="89969-123">Para compilar el ejemplo desde el símbolo del sistema:</span><span class="sxs-lookup"><span data-stu-id="89969-123">To build the sample from the command prompt:</span></span>

1.  <span data-ttu-id="89969-124">Abra la ventana del símbolo del sistema y navegue hasta el directorio del proyecto **PlaylistCreator** .</span><span class="sxs-lookup"><span data-stu-id="89969-124">Open the command prompt window and navigate to the **PlaylistCreator** project directory.</span></span>
2.  <span data-ttu-id="89969-125">Escriba `msbuild PlaylistCreator.sln`.</span><span class="sxs-lookup"><span data-stu-id="89969-125">Enter `msbuild PlaylistCreator.sln`.</span></span>

<span data-ttu-id="89969-126">Para compilar el ejemplo mediante Microsoft Visual Studio (preferido):</span><span class="sxs-lookup"><span data-stu-id="89969-126">To build the sample using Microsoft Visual Studio (preferred):</span></span>

> [!Note]  
> <span data-ttu-id="89969-127">Este ejemplo también se puede usar con la edición Visual C++ Express si no está disponible la versión completa de Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="89969-127">This sample can also be used with the Visual C++ Express Edition if the full Visual Studio is not available.</span></span>

 

1.  <span data-ttu-id="89969-128">Abra el explorador de Windows y navegue hasta el directorio del proyecto **PlaylistCreator** .</span><span class="sxs-lookup"><span data-stu-id="89969-128">Open Windows Explorer and navigate to the **PlaylistCreator** project directory.</span></span>
2.  <span data-ttu-id="89969-129">Haga doble clic en el icono del archivo PlaylistCreator. sln para abrir el proyecto en Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="89969-129">Double-click the icon for the PlaylistCreator.sln file to open the project in Visual Studio.</span></span>
3.  <span data-ttu-id="89969-130">En el menú **compilar** , seleccione **compilar solución**.</span><span class="sxs-lookup"><span data-stu-id="89969-130">From the **Build** menu, select **Build Solution**.</span></span>
    > [!Note]  
    > <span data-ttu-id="89969-131">Si está compilando 64 bits mediante Visual C++ Express Edition, debe usar el compilador cruzado x64 proporcionado con la Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="89969-131">If you are compiling 64-bit using the Visual C++ Express Edition, you must to use the x64 cross-compiler supplied with the Windows SDK.</span></span>

     

## <a name="running-the-sample"></a><span data-ttu-id="89969-132">Ejecutar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="89969-132">Running the Sample</span></span>

1.  <span data-ttu-id="89969-133">Navegue hasta el directorio que contiene el nuevo ejecutable, mediante el símbolo del sistema o el explorador de Windows.</span><span class="sxs-lookup"><span data-stu-id="89969-133">Navigate to the directory that contains the new executable, using the command prompt or Windows Explorer.</span></span>
2.  <span data-ttu-id="89969-134">En la línea de comandos, escriba `PlaylistCreator.exe` .</span><span class="sxs-lookup"><span data-stu-id="89969-134">At the command line, enter `PlaylistCreator.exe`.</span></span> <span data-ttu-id="89969-135">Como alternativa, en el explorador de Windows, haga doble clic en el icono de PlaylistCreator.exe.</span><span class="sxs-lookup"><span data-stu-id="89969-135">Alternatively, from Windows Explorer double-click the icon for PlaylistCreator.exe.</span></span>
3.  <span data-ttu-id="89969-136">Haga clic con el botón secundario en cualquier archivo de música o carpeta que contenga archivos de música en el explorador de Windows para crear una lista de reproducción para abrir el menú contextual.</span><span class="sxs-lookup"><span data-stu-id="89969-136">Right-click any music file or folder containing music files in Windows Explorer to create a playlist to bring up the context menu</span></span>
4.  <span data-ttu-id="89969-137">Puede crear una lista de reproducción. m3u o. wpl.</span><span class="sxs-lookup"><span data-stu-id="89969-137">You can create a .m3u or .wpl playlist.</span></span> <span data-ttu-id="89969-138">Las listas de reproducción se crean en la `%userprofile%\Music\Playlists` carpeta.</span><span class="sxs-lookup"><span data-stu-id="89969-138">Playlists are created in the `%userprofile%\Music\Playlists` folder.</span></span>
    > [!Note]  
    > <span data-ttu-id="89969-139">Los nuevos verbos en el menú contextual se pueden encontrar en la carpeta **música** , pilas de música, pilas de la **biblioteca de música** y colecciones de archivos de música.</span><span class="sxs-lookup"><span data-stu-id="89969-139">New verbs in the context menu can be found in the **Music** folder, music stacks, stacks in the **Music Library**, and collections of music files.</span></span>

     

 

 



