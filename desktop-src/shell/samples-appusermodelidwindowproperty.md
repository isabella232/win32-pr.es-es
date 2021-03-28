---
description: Muestra cómo controlar el comportamiento de agrupación de la barra de tareas de las ventanas de una aplicación a través de la propiedad System.AppUserModel.ID.
title: Ejemplo de propiedad de ventana de identificador de modelo del usuario de la aplicación
ms.topic: article
ms.date: 05/31/2018
ms.assetid: D4B22B3F-C849-4b5f-BDA0-FB42D7E0E4C9
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 42544992248143c95ae905db39fe854b27751862
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985831"
---
# <a name="application-user-model-id-appid-window-property-sample"></a><span data-ttu-id="111d4-103">Ejemplo de propiedad de ventana ID. de modelo de usuario (AppID)</span><span class="sxs-lookup"><span data-stu-id="111d4-103">Application User Model ID (AppID) Window Property Sample</span></span>

<span data-ttu-id="111d4-104">Muestra cómo controlar el comportamiento de agrupación de la barra de tareas de las ventanas de una aplicación a través de la propiedad [System.AppUserModel.ID](../properties/props-system-appusermodel-id.md) .</span><span class="sxs-lookup"><span data-stu-id="111d4-104">Demonstrates how to control the taskbar grouping behavior of an application's windows through the [System.AppUserModel.ID](../properties/props-system-appusermodel-id.md) property.</span></span>

<span data-ttu-id="111d4-105">En este tema se incluyen las siguientes secciones.</span><span class="sxs-lookup"><span data-stu-id="111d4-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="111d4-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="111d4-106">Description</span></span>](#description)
-   [<span data-ttu-id="111d4-107">Requisitos</span><span class="sxs-lookup"><span data-stu-id="111d4-107">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="111d4-108">Descargar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="111d4-108">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="111d4-109">Compilar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="111d4-109">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="111d4-110">Ejecutar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="111d4-110">Running the Sample</span></span>](#running-the-sample)
-   [<span data-ttu-id="111d4-111">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="111d4-111">Related topics</span></span>](#related-topics)

## <a name="description"></a><span data-ttu-id="111d4-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="111d4-112">Description</span></span>

<span data-ttu-id="111d4-113">Este ejemplo muestra cómo establecer la propiedad [System.AppUserModel.ID](../properties/props-system-appusermodel-id.md) mediante el uso de la implementación de [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) de la ventana, que se obtiene a través de [**SHGetPropertyStoreForWindow**](/windows/win32/api/shellapi/nf-shellapi-shgetpropertystoreforwindow).</span><span class="sxs-lookup"><span data-stu-id="111d4-113">This sample shows how to set the [System.AppUserModel.ID](../properties/props-system-appusermodel-id.md) property through the use of the window's [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) implementation, which is obtained through [**SHGetPropertyStoreForWindow**](/windows/win32/api/shellapi/nf-shellapi-shgetpropertystoreforwindow).</span></span>

## <a name="requirements"></a><span data-ttu-id="111d4-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="111d4-114">Requirements</span></span>



| <span data-ttu-id="111d4-115">Producto</span><span class="sxs-lookup"><span data-stu-id="111d4-115">Product</span></span>                                | <span data-ttu-id="111d4-116">Versión mínima del producto</span><span class="sxs-lookup"><span data-stu-id="111d4-116">Minimum Product Version</span></span> |
|----------------------------------------|-------------------------|
| <span data-ttu-id="111d4-117">Windows</span><span class="sxs-lookup"><span data-stu-id="111d4-117">Windows</span></span>                                | <span data-ttu-id="111d4-118">Windows 7</span><span class="sxs-lookup"><span data-stu-id="111d4-118">Windows 7</span></span>               |
| <span data-ttu-id="111d4-119">Kit de desarrollo de software de Windows (SDK)</span><span class="sxs-lookup"><span data-stu-id="111d4-119">Windows Software Development Kit (SDK)</span></span> | <span data-ttu-id="111d4-120">7.0</span><span class="sxs-lookup"><span data-stu-id="111d4-120">7.0</span></span>                     |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="111d4-121">Descargar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="111d4-121">Downloading the Sample</span></span>

| <span data-ttu-id="111d4-122">Ubicación</span><span class="sxs-lookup"><span data-stu-id="111d4-122">Location</span></span>      | <span data-ttu-id="111d4-123">URL de ruta de acceso</span><span class="sxs-lookup"><span data-stu-id="111d4-123">Path URL</span></span>                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="111d4-124">GitHub</span><span class="sxs-lookup"><span data-stu-id="111d4-124">GitHub</span></span>  | [<span data-ttu-id="111d4-125">Ejemplo de AppUserModelIDWindowProperty</span><span class="sxs-lookup"><span data-stu-id="111d4-125">AppUserModelIDWindowProperty sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/AppUserModelIDWindowProperty) |


## <a name="building-the-sample"></a><span data-ttu-id="111d4-126">Generar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="111d4-126">Building the Sample</span></span>

<span data-ttu-id="111d4-127">Para compilar el ejemplo desde el símbolo del sistema:</span><span class="sxs-lookup"><span data-stu-id="111d4-127">To build the sample from the command prompt:</span></span>

1.  <span data-ttu-id="111d4-128">Abra la ventana del símbolo del sistema y navegue hasta el directorio del proyecto **AppUserModelIDWindowProperty** .</span><span class="sxs-lookup"><span data-stu-id="111d4-128">Open the command prompt window and navigate to the **AppUserModelIDWindowProperty** project directory.</span></span>
2.  <span data-ttu-id="111d4-129">Escriba `msbuild AppUserModelIDWindowProperty.sln`.</span><span class="sxs-lookup"><span data-stu-id="111d4-129">Enter `msbuild AppUserModelIDWindowProperty.sln`.</span></span>

<span data-ttu-id="111d4-130">Para compilar el ejemplo mediante Microsoft Visual Studio (preferido):</span><span class="sxs-lookup"><span data-stu-id="111d4-130">To build the sample using Microsoft Visual Studio (preferred):</span></span>

1.  <span data-ttu-id="111d4-131">Abra el explorador de Windows y navegue hasta el directorio del proyecto **AppUserModelIDWindowProperty** .</span><span class="sxs-lookup"><span data-stu-id="111d4-131">Open Windows Explorer and navigate to the **AppUserModelIDWindowProperty** project directory.</span></span>
2.  <span data-ttu-id="111d4-132">Haga doble clic en el icono del archivo AppUserModelIDWindowProperty. sln para abrir el proyecto en Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="111d4-132">Double-click the icon for the AppUserModelIDWindowProperty.sln file to open the project in Visual Studio.</span></span>
3.  <span data-ttu-id="111d4-133">En el menú **compilar** , seleccione **compilar solución**.</span><span class="sxs-lookup"><span data-stu-id="111d4-133">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="111d4-134">Ejecutar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="111d4-134">Running the Sample</span></span>

1.  <span data-ttu-id="111d4-135">Navegue hasta el directorio que contiene el nuevo ejecutable, mediante el símbolo del sistema o el explorador de Windows.</span><span class="sxs-lookup"><span data-stu-id="111d4-135">Navigate to the directory that contains the new executable, using the command prompt or Windows Explorer.</span></span>
2.  <span data-ttu-id="111d4-136">En la línea de comandos, escriba `AppUserModelIDWindowProperty.exe` .</span><span class="sxs-lookup"><span data-stu-id="111d4-136">At the command line, enter `AppUserModelIDWindowProperty.exe`.</span></span> <span data-ttu-id="111d4-137">Como alternativa, en el explorador de Windows, haga doble clic en el icono de AppUserModelIDWindowProperty.exe.</span><span class="sxs-lookup"><span data-stu-id="111d4-137">Alternatively, from Windows Explorer double-click the icon for AppUserModelIDWindowProperty.exe.</span></span>
3.  <span data-ttu-id="111d4-138">Para demostrar el efecto que tienen los identificadores de modelo de usuario de la aplicación (AppUserModelIDs) en la agrupación de la barra de tareas, inicie al menos tres instancias de la aplicación al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="111d4-138">To demonstrate the effect Application User Model IDs (AppUserModelIDs) have on taskbar grouping, launch at least three instances of the application at the same time.</span></span>
4.  <span data-ttu-id="111d4-139">Use el menú para establecer un AppUserModelID diferente en cada una de las tres ventanas.</span><span class="sxs-lookup"><span data-stu-id="111d4-139">Use the menu to set a different AppUserModelID on each of the three windows.</span></span> <span data-ttu-id="111d4-140">Tenga en cuenta que cada uno de los distintos resultados de AppUserModelID es un botón de la barra de tareas independiente y que Windows puede cambiar su identidad en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="111d4-140">Notice that each separate AppUserModelID results in a separate taskbar button and that windows can change their identity at runtime.</span></span>
5.  <span data-ttu-id="111d4-141">Establezca al menos dos ventanas en el segundo AppUserModelID.</span><span class="sxs-lookup"><span data-stu-id="111d4-141">Set at least two windows to the second AppUserModelID.</span></span> <span data-ttu-id="111d4-142">Tenga en cuenta que ambos se mueven al mismo grupo de la barra de tareas.</span><span class="sxs-lookup"><span data-stu-id="111d4-142">Notice that they both move into the same taskbar group.</span></span>
6.  <span data-ttu-id="111d4-143">Abra la **barra de tareas y la ventana Propiedades del menú Inicio** haciendo clic con el botón secundario en la barra de tareas y seleccionando **propiedades** en el menú contextual.</span><span class="sxs-lookup"><span data-stu-id="111d4-143">Open the **Taskbar and Start Menu Properties** window by right-clicking the taskbar and selecting **Properties** in the context menu.</span></span> <span data-ttu-id="111d4-144">Cambiar los **botones de la barra de tareas:** desplegable entre **combinar cuando la barra de tareas está llena** y **nunca combinar** valores.</span><span class="sxs-lookup"><span data-stu-id="111d4-144">Change the **Taskbar buttons:** drop-down between the **Combine when taskbar is full** and **Never combine** values.</span></span> <span data-ttu-id="111d4-145">Observe que cada ventana puede obtener un botón independiente, pero que los botones están agrupados por AppUserModelID.</span><span class="sxs-lookup"><span data-stu-id="111d4-145">Notice that each window can get a separate button, but that the buttons are grouped by AppUserModelID.</span></span>

## <a name="related-topics"></a><span data-ttu-id="111d4-146">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="111d4-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="111d4-147">Identificadores de modelo de usuario de la aplicación (AppUserModelIDs)</span><span class="sxs-lookup"><span data-stu-id="111d4-147">Application User Model IDs (AppUserModelIDs)</span></span>](appids.md)
</dt> </dl>

 

 
