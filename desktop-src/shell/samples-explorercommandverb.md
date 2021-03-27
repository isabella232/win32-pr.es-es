---
description: Muestra cómo implementar un verbo de Shell mediante los métodos ExplorerCommand y ExplorerCommandState.
title: Ejemplo de verbo Explorer Command
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 2310A6AA-EAF9-4d7a-A784-04931BDC2089
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: a35662c3df0e0fcddae049ccfaac2d9e3e265ee3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912922"
---
# <a name="explorer-command-verb-sample"></a><span data-ttu-id="000be-103">Ejemplo de verbo Explorer Command</span><span class="sxs-lookup"><span data-stu-id="000be-103">Explorer Command Verb Sample</span></span>

<span data-ttu-id="000be-104">Muestra cómo implementar un verbo de Shell mediante los métodos ExplorerCommand y ExplorerCommandState.</span><span class="sxs-lookup"><span data-stu-id="000be-104">Demonstrates how to implement a Shell verb using the ExplorerCommand and ExplorerCommandState methods.</span></span>

<span data-ttu-id="000be-105">En este tema se incluyen las siguientes secciones.</span><span class="sxs-lookup"><span data-stu-id="000be-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="000be-106">Requisitos</span><span class="sxs-lookup"><span data-stu-id="000be-106">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="000be-107">Descargar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="000be-107">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="000be-108">Compilar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="000be-108">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="000be-109">Ejecutar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="000be-109">Running the Sample</span></span>](#running-the-sample)

## <a name="requirements"></a><span data-ttu-id="000be-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="000be-110">Requirements</span></span>



| <span data-ttu-id="000be-111">Producto</span><span class="sxs-lookup"><span data-stu-id="000be-111">Product</span></span>                                | <span data-ttu-id="000be-112">Versión mínima del producto</span><span class="sxs-lookup"><span data-stu-id="000be-112">Minimum Product Version</span></span> |
|----------------------------------------|-------------------------|
| <span data-ttu-id="000be-113">Windows</span><span class="sxs-lookup"><span data-stu-id="000be-113">Windows</span></span>                                | <span data-ttu-id="000be-114">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="000be-114">Windows Vista</span></span>           |
| <span data-ttu-id="000be-115">Kit de desarrollo de software de Windows (SDK)</span><span class="sxs-lookup"><span data-stu-id="000be-115">Windows Software Development Kit (SDK)</span></span> | <span data-ttu-id="000be-116">7.0</span><span class="sxs-lookup"><span data-stu-id="000be-116">7.0</span></span>                     |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="000be-117">Descargar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="000be-117">Downloading the Sample</span></span>

| <span data-ttu-id="000be-118">Ubicación</span><span class="sxs-lookup"><span data-stu-id="000be-118">Location</span></span>      | <span data-ttu-id="000be-119">URL de ruta de acceso</span><span class="sxs-lookup"><span data-stu-id="000be-119">Path URL</span></span>                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="000be-120">GitHub</span><span class="sxs-lookup"><span data-stu-id="000be-120">GitHub</span></span>  | [<span data-ttu-id="000be-121">Ejemplo de ExplorerCommandVerb</span><span class="sxs-lookup"><span data-stu-id="000be-121">ExplorerCommandVerb sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/ExplorerCommandVerb) |

## <a name="building-the-sample"></a><span data-ttu-id="000be-122">Generar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="000be-122">Building the Sample</span></span>

<span data-ttu-id="000be-123">Para compilar el ejemplo desde el símbolo del sistema:</span><span class="sxs-lookup"><span data-stu-id="000be-123">To build the sample from the command prompt:</span></span>

1.  <span data-ttu-id="000be-124">Abra la ventana del símbolo del sistema y navegue hasta el directorio del proyecto **ExplorerCommandVerb** .</span><span class="sxs-lookup"><span data-stu-id="000be-124">Open the command prompt window and navigate to the **ExplorerCommandVerb** project directory.</span></span>
2.  <span data-ttu-id="000be-125">Escriba `msbuild ExplorerCommandVerb.sln`.</span><span class="sxs-lookup"><span data-stu-id="000be-125">Enter `msbuild ExplorerCommandVerb.sln`.</span></span>

<span data-ttu-id="000be-126">Para compilar el ejemplo mediante Microsoft Visual Studio (preferido):</span><span class="sxs-lookup"><span data-stu-id="000be-126">To build the sample using Microsoft Visual Studio (preferred):</span></span>

1.  <span data-ttu-id="000be-127">Abra el explorador de Windows y navegue hasta el directorio del proyecto **ExplorerCommandVerb** .</span><span class="sxs-lookup"><span data-stu-id="000be-127">Open Windows Explorer and navigate to the **ExplorerCommandVerb** project directory.</span></span>
2.  <span data-ttu-id="000be-128">Haga doble clic en el icono del archivo ExplorerCommandVerb. sln para abrir el proyecto en Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="000be-128">Double-click the icon for the ExplorerCommandVerb.sln file to open the project in Visual Studio.</span></span>
3.  <span data-ttu-id="000be-129">En el menú **compilar** , seleccione **compilar solución**.</span><span class="sxs-lookup"><span data-stu-id="000be-129">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="000be-130">Ejecutar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="000be-130">Running the Sample</span></span>

1.  <span data-ttu-id="000be-131">Navegue hasta el directorio que contiene el ExplorerCommandVerb.dll, mediante el símbolo del sistema o el explorador de Windows.</span><span class="sxs-lookup"><span data-stu-id="000be-131">Navigate to the directory that contains the ExplorerCommandVerb.dll, using the command prompt or Windows Explorer.</span></span> <span data-ttu-id="000be-132">Asegúrese de usar el archivo DLL de 64 bits en Windows de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="000be-132">Make sure you use the 64-bit DLL file on 64-bit Windows.</span></span>
2.  <span data-ttu-id="000be-133">En la línea de comandos, escriba `regsvr32.exe ExplorerCommandVerb.dll` .</span><span class="sxs-lookup"><span data-stu-id="000be-133">At the command line, enter `regsvr32.exe ExplorerCommandVerb.dll`.</span></span>
3.  <span data-ttu-id="000be-134">Al hacer clic con el botón secundario en un archivo. txt, se mostrarán dos nuevos verbos en el menú contextual.</span><span class="sxs-lookup"><span data-stu-id="000be-134">Two new verbs will be shown on the context menu when you right-click a .txt file.</span></span>

 

 



