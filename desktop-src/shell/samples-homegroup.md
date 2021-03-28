---
description: Muestra cómo determinar el estado de pertenencia a un grupo en el hogar, enumerar los elementos de nivel superior en la carpeta del shell del grupo hogar e iniciar el Asistente para compartir el grupo en el hogar.
title: Ejemplo de HomeGroup
ms.topic: article
ms.date: 05/31/2018
ms.assetid: FDEFF261-BF86-4fbb-8567-892F79F23D92
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: c22ea84431f464ef8fcae6bfad0d90a45ba310d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104082814"
---
# <a name="homegroup-sample"></a><span data-ttu-id="99b05-103">Ejemplo de HomeGroup</span><span class="sxs-lookup"><span data-stu-id="99b05-103">HomeGroup Sample</span></span>

<span data-ttu-id="99b05-104">Muestra cómo determinar el estado de pertenencia a un grupo en el hogar, enumerar los elementos de nivel superior en la carpeta del shell del **Grupo hogar** e iniciar el **Asistente para compartir el grupo** en el hogar.</span><span class="sxs-lookup"><span data-stu-id="99b05-104">Demonstrates how to determine HomeGroup membership status, enumerate top-level items in the **HomeGroup** Shell folder, and launch the **HomeGroup Sharing Wizard**.</span></span>

<span data-ttu-id="99b05-105">En este tema se incluyen las siguientes secciones.</span><span class="sxs-lookup"><span data-stu-id="99b05-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="99b05-106">Requisitos</span><span class="sxs-lookup"><span data-stu-id="99b05-106">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="99b05-107">Descargar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="99b05-107">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="99b05-108">Compilar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="99b05-108">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="99b05-109">Ejecutar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="99b05-109">Running the Sample</span></span>](#running-the-sample)
-   [<span data-ttu-id="99b05-110">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="99b05-110">Related topics</span></span>](#related-topics)

## <a name="requirements"></a><span data-ttu-id="99b05-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="99b05-111">Requirements</span></span>



| <span data-ttu-id="99b05-112">Producto</span><span class="sxs-lookup"><span data-stu-id="99b05-112">Product</span></span>                                | <span data-ttu-id="99b05-113">Versión mínima del producto</span><span class="sxs-lookup"><span data-stu-id="99b05-113">Minimum Product Version</span></span> |
|----------------------------------------|-------------------------|
| <span data-ttu-id="99b05-114">Windows</span><span class="sxs-lookup"><span data-stu-id="99b05-114">Windows</span></span>                                | <span data-ttu-id="99b05-115">Windows 7</span><span class="sxs-lookup"><span data-stu-id="99b05-115">Windows 7</span></span>               |
| <span data-ttu-id="99b05-116">Kit de desarrollo de software de Windows (SDK)</span><span class="sxs-lookup"><span data-stu-id="99b05-116">Windows Software Development Kit (SDK)</span></span> | <span data-ttu-id="99b05-117">7.0</span><span class="sxs-lookup"><span data-stu-id="99b05-117">7.0</span></span>                     |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="99b05-118">Descargar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="99b05-118">Downloading the Sample</span></span>

| <span data-ttu-id="99b05-119">Ubicación</span><span class="sxs-lookup"><span data-stu-id="99b05-119">Location</span></span>      | <span data-ttu-id="99b05-120">URL de ruta de acceso</span><span class="sxs-lookup"><span data-stu-id="99b05-120">Path URL</span></span>                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="99b05-121">GitHub</span><span class="sxs-lookup"><span data-stu-id="99b05-121">GitHub</span></span>  | [<span data-ttu-id="99b05-122">Ejemplo de grupo hogar</span><span class="sxs-lookup"><span data-stu-id="99b05-122">HomeGroup sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/HomeGroup) |

## <a name="building-the-sample"></a><span data-ttu-id="99b05-123">Generar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="99b05-123">Building the Sample</span></span>

<span data-ttu-id="99b05-124">Para compilar el ejemplo desde el símbolo del sistema:</span><span class="sxs-lookup"><span data-stu-id="99b05-124">To build the sample from the command prompt:</span></span>

1.  <span data-ttu-id="99b05-125">Abra la ventana del símbolo del sistema y navegue hasta el directorio del proyecto **Grupo hogar** .</span><span class="sxs-lookup"><span data-stu-id="99b05-125">Open the command prompt window and navigate to the **HomeGroup** project directory.</span></span>
2.  <span data-ttu-id="99b05-126">Escriba `msbuild HomeGroup.sln`.</span><span class="sxs-lookup"><span data-stu-id="99b05-126">Enter `msbuild HomeGroup.sln`.</span></span>

<span data-ttu-id="99b05-127">Para compilar el ejemplo mediante Microsoft Visual Studio (preferido):</span><span class="sxs-lookup"><span data-stu-id="99b05-127">To build the sample using Microsoft Visual Studio (preferred):</span></span>

1.  <span data-ttu-id="99b05-128">Abra el explorador de Windows y navegue hasta el directorio del proyecto **Grupo hogar** .</span><span class="sxs-lookup"><span data-stu-id="99b05-128">Open Windows Explorer and navigate to the **HomeGroup** project directory.</span></span>
2.  <span data-ttu-id="99b05-129">Haga doble clic en el icono del archivo webhogar. sln para abrir el proyecto en Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="99b05-129">Double-click the icon for the HomeGroup.sln file to open the project in Visual Studio.</span></span>
3.  <span data-ttu-id="99b05-130">En el menú **compilar** , seleccione **compilar solución**.</span><span class="sxs-lookup"><span data-stu-id="99b05-130">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="99b05-131">Ejecutar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="99b05-131">Running the Sample</span></span>

1.  <span data-ttu-id="99b05-132">Navegue hasta el directorio que contiene el nuevo ejecutable, mediante el símbolo del sistema o el explorador de Windows.</span><span class="sxs-lookup"><span data-stu-id="99b05-132">Navigate to the directory that contains the new executable, using the command prompt or Windows Explorer.</span></span>
2.  <span data-ttu-id="99b05-133">En la línea de comandos, escriba `HomeGroup.exe` .</span><span class="sxs-lookup"><span data-stu-id="99b05-133">At the command line, enter `HomeGroup.exe`.</span></span> <span data-ttu-id="99b05-134">Como alternativa, en el explorador de Windows, haga doble clic en el icono de HomeGroup.exe.</span><span class="sxs-lookup"><span data-stu-id="99b05-134">Alternatively, from Windows Explorer double-click the icon for HomeGroup.exe.</span></span>

## <a name="related-topics"></a><span data-ttu-id="99b05-135">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="99b05-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="99b05-136">**IHomeGroup**</span><span class="sxs-lookup"><span data-stu-id="99b05-136">**IHomeGroup**</span></span>](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ihomegroup)
</dt> <dt>

[<span data-ttu-id="99b05-137">**KNOWNFOLDERID**</span><span class="sxs-lookup"><span data-stu-id="99b05-137">**KNOWNFOLDERID**</span></span>](knownfolderid.md)
</dt> </dl>

 

 



