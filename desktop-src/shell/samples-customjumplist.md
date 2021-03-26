---
description: Muestra cómo crear una Jump List personalizada para una aplicación, incluida la adición de una categoría y tareas personalizadas.
title: Ejemplo de lista de accesos directos personalizada
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 60DEDB01-8F8F-4c25-8FCC-8EAC461A99B7
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: c20592e508a24985e0f8283993482c7bd61af232
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278012"
---
# <a name="custom-jump-list-sample"></a><span data-ttu-id="b1065-103">Ejemplo de lista de accesos directos personalizada</span><span class="sxs-lookup"><span data-stu-id="b1065-103">Custom Jump List Sample</span></span>

<span data-ttu-id="b1065-104">Muestra cómo crear una Jump List personalizada para una aplicación, incluida la adición de una categoría y tareas personalizadas.</span><span class="sxs-lookup"><span data-stu-id="b1065-104">Demonstrates how to create a custom Jump List for an application, including adding a custom category and tasks.</span></span>

<span data-ttu-id="b1065-105">En este tema se incluyen las siguientes secciones.</span><span class="sxs-lookup"><span data-stu-id="b1065-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="b1065-106">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b1065-106">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="b1065-107">Descargar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="b1065-107">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="b1065-108">Compilar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="b1065-108">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="b1065-109">Ejecutar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="b1065-109">Running the Sample</span></span>](#running-the-sample)
-   [<span data-ttu-id="b1065-110">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b1065-110">Related topics</span></span>](#related-topics)

## <a name="requirements"></a><span data-ttu-id="b1065-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b1065-111">Requirements</span></span>



| <span data-ttu-id="b1065-112">Producto</span><span class="sxs-lookup"><span data-stu-id="b1065-112">Product</span></span>                                | <span data-ttu-id="b1065-113">Versión mínima del producto</span><span class="sxs-lookup"><span data-stu-id="b1065-113">Minimum Product Version</span></span> |
|----------------------------------------|-------------------------|
| <span data-ttu-id="b1065-114">Windows</span><span class="sxs-lookup"><span data-stu-id="b1065-114">Windows</span></span>                                | <span data-ttu-id="b1065-115">Windows 7</span><span class="sxs-lookup"><span data-stu-id="b1065-115">Windows 7</span></span>               |
| <span data-ttu-id="b1065-116">Kit de desarrollo de software de Windows (SDK)</span><span class="sxs-lookup"><span data-stu-id="b1065-116">Windows Software Development Kit (SDK)</span></span> | <span data-ttu-id="b1065-117">7.0</span><span class="sxs-lookup"><span data-stu-id="b1065-117">7.0</span></span>                     |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="b1065-118">Descargar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="b1065-118">Downloading the Sample</span></span>

| <span data-ttu-id="b1065-119">Ubicación</span><span class="sxs-lookup"><span data-stu-id="b1065-119">Location</span></span>      | <span data-ttu-id="b1065-120">URL de ruta de acceso</span><span class="sxs-lookup"><span data-stu-id="b1065-120">Path URL</span></span>                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1065-121">GitHub</span><span class="sxs-lookup"><span data-stu-id="b1065-121">GitHub</span></span>  | [<span data-ttu-id="b1065-122">Ejemplo de CustomJumpList</span><span class="sxs-lookup"><span data-stu-id="b1065-122">CustomJumpList sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/CustomJumpList) |

## <a name="building-the-sample"></a><span data-ttu-id="b1065-123">Generar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="b1065-123">Building the Sample</span></span>

<span data-ttu-id="b1065-124">Para compilar el ejemplo desde el símbolo del sistema:</span><span class="sxs-lookup"><span data-stu-id="b1065-124">To build the sample from the command prompt:</span></span>

1.  <span data-ttu-id="b1065-125">Abra la ventana del símbolo del sistema y navegue hasta el directorio del proyecto **CustomJumpList** .</span><span class="sxs-lookup"><span data-stu-id="b1065-125">Open the command prompt window and navigate to the **CustomJumpList** project directory.</span></span>
2.  <span data-ttu-id="b1065-126">Escriba `msbuild CustomJumpListSample.sln`.</span><span class="sxs-lookup"><span data-stu-id="b1065-126">Enter `msbuild CustomJumpListSample.sln`.</span></span>

<span data-ttu-id="b1065-127">Para compilar el ejemplo mediante Microsoft Visual Studio (preferido):</span><span class="sxs-lookup"><span data-stu-id="b1065-127">To build the sample using Microsoft Visual Studio (preferred):</span></span>

1.  <span data-ttu-id="b1065-128">Abra el explorador de Windows y navegue hasta el directorio del proyecto **CustomJumpList** .</span><span class="sxs-lookup"><span data-stu-id="b1065-128">Open Windows Explorer and navigate to the **CustomJumpList** project directory.</span></span>
2.  <span data-ttu-id="b1065-129">Haga doble clic en el icono del archivo CustomJumpListSample. sln para abrir el proyecto en Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="b1065-129">Double-click the icon for the CustomJumpListSample.sln file to open the project in Visual Studio.</span></span>
3.  <span data-ttu-id="b1065-130">En el menú **compilar** , seleccione **compilar solución**.</span><span class="sxs-lookup"><span data-stu-id="b1065-130">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="b1065-131">Ejecutar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="b1065-131">Running the Sample</span></span>

1.  <span data-ttu-id="b1065-132">Navegue hasta el directorio que contiene el nuevo ejecutable, mediante el símbolo del sistema o el explorador de Windows.</span><span class="sxs-lookup"><span data-stu-id="b1065-132">Navigate to the directory that contains the new executable, using the command prompt or Windows Explorer.</span></span>
2.  <span data-ttu-id="b1065-133">En la línea de comandos, escriba `CustomJumpListSample.exe` .</span><span class="sxs-lookup"><span data-stu-id="b1065-133">At the command line, enter `CustomJumpListSample.exe`.</span></span> <span data-ttu-id="b1065-134">Como alternativa, en el explorador de Windows, haga doble clic en el icono de CustomJumpListSample.exe.</span><span class="sxs-lookup"><span data-stu-id="b1065-134">Alternatively, from Windows Explorer double-click the icon for CustomJumpListSample.exe.</span></span>
3.  <span data-ttu-id="b1065-135">Este ejemplo debe ejecutarse como administrador la primera vez que se ejecuta para que pueda instalar los registros de tipo de archivo necesarios.</span><span class="sxs-lookup"><span data-stu-id="b1065-135">This sample must be run as an administrator the first time it is run so that it can install the necessary file type registrations.</span></span> <span data-ttu-id="b1065-136">Una vez que se han registrado los tipos de archivo, el ejemplo se puede ejecutar como un usuario estándar.</span><span class="sxs-lookup"><span data-stu-id="b1065-136">After the file types have been registered, the sample can run as a standard user.</span></span>
4.  <span data-ttu-id="b1065-137">Seleccione opciones en el menú de la aplicación de ejemplo para ver cómo afectan a la Jump List de la aplicación en la barra de tareas.</span><span class="sxs-lookup"><span data-stu-id="b1065-137">Select options from the menu in the sample application to see how they affect the application's Jump List in the taskbar.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b1065-138">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b1065-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b1065-139">Identificadores de modelo de usuario de la aplicación (AppUserModelIDs)</span><span class="sxs-lookup"><span data-stu-id="b1065-139">Application User Model IDs (AppUserModelIDs)</span></span>](appids.md)
</dt> </dl>

 

 



