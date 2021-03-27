---
description: Muestra cómo agregar elementos a la lista de saltos automática de una aplicación, incluido el cambio entre la presentación de las categorías frecuentes y recientes.
title: Ejemplo de lista de accesos directos automática
ms.topic: article
ms.date: 05/31/2018
ms.assetid: C33152FE-1322-42f8-A656-3D5FAF4B612D
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: ce0b6520163fcb07bb990b7a5a9fe742d976a899
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104497926"
---
# <a name="automatic-jump-list-sample"></a><span data-ttu-id="0a74b-103">Ejemplo de lista de accesos directos automática</span><span class="sxs-lookup"><span data-stu-id="0a74b-103">Automatic Jump List Sample</span></span>

<span data-ttu-id="0a74b-104">Muestra cómo agregar elementos a la lista de saltos automática de una aplicación, incluido el cambio entre la presentación de las categorías frecuentes y recientes.</span><span class="sxs-lookup"><span data-stu-id="0a74b-104">Demonstrates how to add items to the automatic Jump List for an application, including switching between the display of the Frequent and Recent categories.</span></span>

<span data-ttu-id="0a74b-105">En este tema se incluyen las siguientes secciones.</span><span class="sxs-lookup"><span data-stu-id="0a74b-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="0a74b-106">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0a74b-106">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="0a74b-107">Descargar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="0a74b-107">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="0a74b-108">Compilar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="0a74b-108">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="0a74b-109">Ejecutar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="0a74b-109">Running the Sample</span></span>](#running-the-sample)
-   [<span data-ttu-id="0a74b-110">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="0a74b-110">Related topics</span></span>](#related-topics)

## <a name="requirements"></a><span data-ttu-id="0a74b-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0a74b-111">Requirements</span></span>



| <span data-ttu-id="0a74b-112">Producto</span><span class="sxs-lookup"><span data-stu-id="0a74b-112">Product</span></span>                                | <span data-ttu-id="0a74b-113">Versión mínima del producto</span><span class="sxs-lookup"><span data-stu-id="0a74b-113">Minimum Product Version</span></span> |
|----------------------------------------|-------------------------|
| <span data-ttu-id="0a74b-114">Windows</span><span class="sxs-lookup"><span data-stu-id="0a74b-114">Windows</span></span>                                | <span data-ttu-id="0a74b-115">Windows 7</span><span class="sxs-lookup"><span data-stu-id="0a74b-115">Windows 7</span></span>               |
| <span data-ttu-id="0a74b-116">Kit de desarrollo de software de Windows (SDK)</span><span class="sxs-lookup"><span data-stu-id="0a74b-116">Windows Software Development Kit (SDK)</span></span> | <span data-ttu-id="0a74b-117">7.0</span><span class="sxs-lookup"><span data-stu-id="0a74b-117">7.0</span></span>                     |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="0a74b-118">Descargar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="0a74b-118">Downloading the Sample</span></span>

| <span data-ttu-id="0a74b-119">Ubicación</span><span class="sxs-lookup"><span data-stu-id="0a74b-119">Location</span></span>      | <span data-ttu-id="0a74b-120">URL de ruta de acceso</span><span class="sxs-lookup"><span data-stu-id="0a74b-120">Path URL</span></span>                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0a74b-121">GitHub</span><span class="sxs-lookup"><span data-stu-id="0a74b-121">GitHub</span></span>  | [<span data-ttu-id="0a74b-122">Ejemplo de AutomaticJumpList</span><span class="sxs-lookup"><span data-stu-id="0a74b-122">AutomaticJumpList sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/AutomaticJumpList) |

## <a name="building-the-sample"></a><span data-ttu-id="0a74b-123">Generar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="0a74b-123">Building the Sample</span></span>

<span data-ttu-id="0a74b-124">Para compilar el ejemplo desde el símbolo del sistema:</span><span class="sxs-lookup"><span data-stu-id="0a74b-124">To build the sample from the command prompt:</span></span>

1.  <span data-ttu-id="0a74b-125">Abra la ventana del símbolo del sistema y navegue hasta el directorio del proyecto **AutomaticJumpList** .</span><span class="sxs-lookup"><span data-stu-id="0a74b-125">Open the command prompt window and navigate to the **AutomaticJumpList** project directory.</span></span>
2.  <span data-ttu-id="0a74b-126">Escriba `msbuild AutomaticJumpListSample.sln`.</span><span class="sxs-lookup"><span data-stu-id="0a74b-126">Enter `msbuild AutomaticJumpListSample.sln`.</span></span>

<span data-ttu-id="0a74b-127">Para compilar el ejemplo mediante Microsoft Visual Studio (preferido):</span><span class="sxs-lookup"><span data-stu-id="0a74b-127">To build the sample using Microsoft Visual Studio (preferred):</span></span>

1.  <span data-ttu-id="0a74b-128">Abra el explorador de Windows y navegue hasta el directorio del proyecto **AutomaticJumpList** .</span><span class="sxs-lookup"><span data-stu-id="0a74b-128">Open Windows Explorer and navigate to the **AutomaticJumpList** project directory.</span></span>
2.  <span data-ttu-id="0a74b-129">Haga doble clic en el icono del archivo AutomaticJumpListSample. sln para abrir el proyecto en Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="0a74b-129">Double-click the icon for the AutomaticJumpListSample.sln file to open the project in Visual Studio.</span></span>
3.  <span data-ttu-id="0a74b-130">En el menú **compilar** , seleccione **compilar solución**.</span><span class="sxs-lookup"><span data-stu-id="0a74b-130">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="0a74b-131">Ejecutar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="0a74b-131">Running the Sample</span></span>

1.  <span data-ttu-id="0a74b-132">Navegue hasta el directorio que contiene el nuevo ejecutable, mediante el símbolo del sistema o el explorador de Windows.</span><span class="sxs-lookup"><span data-stu-id="0a74b-132">Navigate to the directory that contains the new executable, using the command prompt or Windows Explorer.</span></span>
2.  <span data-ttu-id="0a74b-133">En la línea de comandos, escriba `AutomaticJumpListSample.exe` .</span><span class="sxs-lookup"><span data-stu-id="0a74b-133">At the command line, enter `AutomaticJumpListSample.exe`.</span></span> <span data-ttu-id="0a74b-134">Como alternativa, en el explorador de Windows, haga doble clic en el icono de AutomaticJumpListSample.exe.</span><span class="sxs-lookup"><span data-stu-id="0a74b-134">Alternatively, from Windows Explorer double-click the icon for AutomaticJumpListSample.exe.</span></span>
3.  <span data-ttu-id="0a74b-135">Este ejemplo debe ejecutarse como administrador la primera vez que se ejecuta para que pueda instalar los registros de tipo de archivo necesarios.</span><span class="sxs-lookup"><span data-stu-id="0a74b-135">This sample must be run as an administrator the first time it is run so that it can install the necessary file type registrations.</span></span> <span data-ttu-id="0a74b-136">Una vez que se han registrado los tipos de archivo, el ejemplo se puede ejecutar como un usuario estándar.</span><span class="sxs-lookup"><span data-stu-id="0a74b-136">After the file types have been registered, the sample can run as a standard user.</span></span>
4.  <span data-ttu-id="0a74b-137">Seleccione opciones en el menú de la aplicación de ejemplo, incluida la selección de documentos. txt o. doc a través del cuadro de diálogo **abrir** para ver cómo afectan a la Jump List de la aplicación en la barra de tareas.</span><span class="sxs-lookup"><span data-stu-id="0a74b-137">Select options from the menu in the sample application, including the selection of .txt or .doc documents through the **Open** dialog to see how they affect the application's Jump List in the taskbar.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0a74b-138">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="0a74b-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0a74b-139">Identificadores de modelo de usuario de la aplicación (AppUserModelIDs)</span><span class="sxs-lookup"><span data-stu-id="0a74b-139">Application User Model IDs (AppUserModelIDs)</span></span>](appids.md)
</dt> </dl>

 

 



