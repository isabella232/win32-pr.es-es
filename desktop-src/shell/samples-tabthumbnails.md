---
description: Muestra cómo una aplicación puede exponer varios destinos de conmutador (como para las pestañas) en un taskband y cómo proporcionar sus miniaturas.
title: Ejemplo de TabThumbnails
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 3F48EAA2-98A3-4530-9FC6-A395987157B7
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 323604d104be3432a5fc251901c4308bfc989f90
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104986034"
---
# <a name="tabthumbnails-sample"></a><span data-ttu-id="d0000-103">Ejemplo de TabThumbnails</span><span class="sxs-lookup"><span data-stu-id="d0000-103">TabThumbnails Sample</span></span>

<span data-ttu-id="d0000-104">Muestra cómo una aplicación puede exponer varios destinos de conmutador (como para las pestañas) en un taskband y cómo proporcionar sus miniaturas.</span><span class="sxs-lookup"><span data-stu-id="d0000-104">Demonstrates how an application can expose multiple switch targets (as for tabs) on a taskband and how to provide their thumbnails.</span></span>

<span data-ttu-id="d0000-105">En este tema se incluyen las siguientes secciones.</span><span class="sxs-lookup"><span data-stu-id="d0000-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="d0000-106">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d0000-106">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="d0000-107">Descargar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="d0000-107">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="d0000-108">Compilar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="d0000-108">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="d0000-109">Ejecutar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="d0000-109">Running the Sample</span></span>](#running-the-sample)

## <a name="requirements"></a><span data-ttu-id="d0000-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d0000-110">Requirements</span></span>



| <span data-ttu-id="d0000-111">Producto</span><span class="sxs-lookup"><span data-stu-id="d0000-111">Product</span></span>                                | <span data-ttu-id="d0000-112">Versión mínima del producto</span><span class="sxs-lookup"><span data-stu-id="d0000-112">Minimum Product Version</span></span> |
|----------------------------------------|-------------------------|
| <span data-ttu-id="d0000-113">Windows</span><span class="sxs-lookup"><span data-stu-id="d0000-113">Windows</span></span>                                | <span data-ttu-id="d0000-114">Windows 7</span><span class="sxs-lookup"><span data-stu-id="d0000-114">Windows 7</span></span>               |
| <span data-ttu-id="d0000-115">Kit de desarrollo de software de Windows (SDK)</span><span class="sxs-lookup"><span data-stu-id="d0000-115">Windows Software Development Kit (SDK)</span></span> | <span data-ttu-id="d0000-116">7.0</span><span class="sxs-lookup"><span data-stu-id="d0000-116">7.0</span></span>                     |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="d0000-117">Descargar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="d0000-117">Downloading the Sample</span></span>

| <span data-ttu-id="d0000-118">Ubicación</span><span class="sxs-lookup"><span data-stu-id="d0000-118">Location</span></span>      | <span data-ttu-id="d0000-119">URL de ruta de acceso</span><span class="sxs-lookup"><span data-stu-id="d0000-119">Path URL</span></span>                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d0000-120">GitHub</span><span class="sxs-lookup"><span data-stu-id="d0000-120">GitHub</span></span>  | [<span data-ttu-id="d0000-121">Ejemplo de TabThumbnails</span><span class="sxs-lookup"><span data-stu-id="d0000-121">TabThumbnails sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/TabThumbnails) |

## <a name="building-the-sample"></a><span data-ttu-id="d0000-122">Generar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="d0000-122">Building the Sample</span></span>

<span data-ttu-id="d0000-123">Para compilar el ejemplo desde el símbolo del sistema:</span><span class="sxs-lookup"><span data-stu-id="d0000-123">To build the sample from the command prompt:</span></span>

1.  <span data-ttu-id="d0000-124">Abra la ventana del símbolo del sistema y navegue hasta el directorio del proyecto **TabThumbnails** .</span><span class="sxs-lookup"><span data-stu-id="d0000-124">Open the command prompt window and navigate to the **TabThumbnails** project directory.</span></span>
2.  <span data-ttu-id="d0000-125">Escriba `msbuild TabThumbnails.sln`.</span><span class="sxs-lookup"><span data-stu-id="d0000-125">Enter `msbuild TabThumbnails.sln`.</span></span>

<span data-ttu-id="d0000-126">Para compilar el ejemplo mediante Microsoft Visual Studio (preferido):</span><span class="sxs-lookup"><span data-stu-id="d0000-126">To build the sample using Microsoft Visual Studio (preferred):</span></span>

1.  <span data-ttu-id="d0000-127">Abra el explorador de Windows y navegue hasta el directorio del proyecto **TabThumbnails** .</span><span class="sxs-lookup"><span data-stu-id="d0000-127">Open Windows Explorer and navigate to the **TabThumbnails** project directory.</span></span>
2.  <span data-ttu-id="d0000-128">Haga doble clic en el icono del archivo TabThumbnails. sln para abrir el proyecto en Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="d0000-128">Double-click the icon for the TabThumbnails.sln file to open the project in Visual Studio.</span></span>
3.  <span data-ttu-id="d0000-129">En el menú **compilar** , seleccione **compilar solución**.</span><span class="sxs-lookup"><span data-stu-id="d0000-129">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="d0000-130">Ejecutar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="d0000-130">Running the Sample</span></span>

1.  <span data-ttu-id="d0000-131">Navegue hasta el directorio que contiene el nuevo ejecutable, mediante el símbolo del sistema o el explorador de Windows.</span><span class="sxs-lookup"><span data-stu-id="d0000-131">Navigate to the directory that contains the new executable, using the command prompt or Windows Explorer.</span></span>
2.  <span data-ttu-id="d0000-132">En la línea de comandos, escriba `TabThumbnails.exe` .</span><span class="sxs-lookup"><span data-stu-id="d0000-132">At the command line, enter `TabThumbnails.exe`.</span></span> <span data-ttu-id="d0000-133">Como alternativa, en el explorador de Windows, haga doble clic en el icono de TabThumbnails.exe.</span><span class="sxs-lookup"><span data-stu-id="d0000-133">Alternatively, from Windows Explorer double-click the icon for TabThumbnails.exe.</span></span>

 

 



