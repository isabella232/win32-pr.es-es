---
description: Muestra cómo escribir un controlador utilizado para mostrar una vista previa del archivo en el panel de vista previa del explorador de Windows o en otros hosts del controlador de vista previa.
title: Ejemplo de controlador de vista previa de recetas
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 2C926922-48C0-46f5-8928-67007C6FF957
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 05208010c90c7185a777bb75f5de1e67bdb5bc14
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985783"
---
# <a name="recipe-preview-handler-sample"></a><span data-ttu-id="d63bf-103">Ejemplo de controlador de vista previa de recetas</span><span class="sxs-lookup"><span data-stu-id="d63bf-103">Recipe Preview Handler Sample</span></span>

<span data-ttu-id="d63bf-104">Muestra cómo escribir un controlador utilizado para mostrar una vista previa del archivo en el panel de vista previa del explorador de Windows o en otros hosts del controlador de vista previa.</span><span class="sxs-lookup"><span data-stu-id="d63bf-104">Demonstrates how to write a handler used to display a file preview inside the Windows Explorer preview pane or other preview handler hosts.</span></span>

<span data-ttu-id="d63bf-105">Este tema contiene las siguientes secciones:</span><span class="sxs-lookup"><span data-stu-id="d63bf-105">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="d63bf-106">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d63bf-106">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="d63bf-107">Descargar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="d63bf-107">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="d63bf-108">Compilar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="d63bf-108">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="d63bf-109">Ejecutar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="d63bf-109">Running the Sample</span></span>](#running-the-sample)
-   [<span data-ttu-id="d63bf-110">Anular el registro del archivo DLL del controlador de vista previa de ejemplo</span><span class="sxs-lookup"><span data-stu-id="d63bf-110">Unregistering the Sample Preview Handler DLL</span></span>](#unregistering-the-sample-preview-handler-dll)
-   [<span data-ttu-id="d63bf-111">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d63bf-111">Related topics</span></span>](#related-topics)

## <a name="requirements"></a><span data-ttu-id="d63bf-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d63bf-112">Requirements</span></span>



| <span data-ttu-id="d63bf-113">Producto</span><span class="sxs-lookup"><span data-stu-id="d63bf-113">Product</span></span>                                | <span data-ttu-id="d63bf-114">Versión mínima del producto</span><span class="sxs-lookup"><span data-stu-id="d63bf-114">Minimum Product Version</span></span> |
|----------------------------------------|-------------------------|
| <span data-ttu-id="d63bf-115">Windows</span><span class="sxs-lookup"><span data-stu-id="d63bf-115">Windows</span></span>                                | <span data-ttu-id="d63bf-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d63bf-116">Windows Vista</span></span>           |
| <span data-ttu-id="d63bf-117">Kit de desarrollo de software de Windows (SDK)</span><span class="sxs-lookup"><span data-stu-id="d63bf-117">Windows Software Development Kit (SDK)</span></span> | <span data-ttu-id="d63bf-118">7.0</span><span class="sxs-lookup"><span data-stu-id="d63bf-118">7.0</span></span>                     |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="d63bf-119">Descargar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="d63bf-119">Downloading the Sample</span></span>

| <span data-ttu-id="d63bf-120">Ubicación</span><span class="sxs-lookup"><span data-stu-id="d63bf-120">Location</span></span>      | <span data-ttu-id="d63bf-121">URL de ruta de acceso</span><span class="sxs-lookup"><span data-stu-id="d63bf-121">Path URL</span></span>                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d63bf-122">GitHub</span><span class="sxs-lookup"><span data-stu-id="d63bf-122">GitHub</span></span>  | [<span data-ttu-id="d63bf-123">Ejemplo de RecipePreviewHandler</span><span class="sxs-lookup"><span data-stu-id="d63bf-123">RecipePreviewHandler sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/RecipePreviewHandler) |

## <a name="building-the-sample"></a><span data-ttu-id="d63bf-124">Generar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="d63bf-124">Building the Sample</span></span>

<span data-ttu-id="d63bf-125">Para compilar el ejemplo desde el símbolo del sistema:</span><span class="sxs-lookup"><span data-stu-id="d63bf-125">To build the sample from the command prompt:</span></span>

1.  <span data-ttu-id="d63bf-126">Abra la ventana del símbolo del sistema y navegue hasta el directorio del proyecto **RecipePreviewHandler** .</span><span class="sxs-lookup"><span data-stu-id="d63bf-126">Open the command prompt window and navigate to the **RecipePreviewHandler** project directory.</span></span> <span data-ttu-id="d63bf-127">Por ejemplo, `C:\Program Files\MicrosoftSDKs\Windows\v7.0\Samples\WinUI\Shell\AppShellIntegration\RecipePreviewHandler`.</span><span class="sxs-lookup"><span data-stu-id="d63bf-127">For example, `C:\Program Files\MicrosoftSDKs\Windows\v7.0\Samples\WinUI\Shell\AppShellIntegration\RecipePreviewHandler`.</span></span>
2.  <span data-ttu-id="d63bf-128">Escriba `msbuild PreviewHandlerSDKSample.sln`.</span><span class="sxs-lookup"><span data-stu-id="d63bf-128">Enter `msbuild PreviewHandlerSDKSample.sln`.</span></span>

<span data-ttu-id="d63bf-129">Para compilar el ejemplo mediante Microsoft Visual Studio (preferido):</span><span class="sxs-lookup"><span data-stu-id="d63bf-129">To build the sample using Microsoft Visual Studio (preferred):</span></span>

1.  <span data-ttu-id="d63bf-130">Abra el explorador de Windows y navegue hasta el directorio del proyecto **RecipePreviewHandler** .</span><span class="sxs-lookup"><span data-stu-id="d63bf-130">Open Windows Explorer and navigate to the **RecipePreviewHandler** project directory.</span></span>
2.  <span data-ttu-id="d63bf-131">Haga doble clic en el icono del archivo PreviewHandlerSDKSample. sln para abrir el proyecto en Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="d63bf-131">Double-click the icon for the PreviewHandlerSDKSample.sln file to open the project in Visual Studio.</span></span>
    > [!Note]  
    > <span data-ttu-id="d63bf-132">La extensión de nombre de archivo. sln no se muestra en configuración de carpeta predeterminada.</span><span class="sxs-lookup"><span data-stu-id="d63bf-132">The .sln file name extension is not shown under default folder settings.</span></span> <span data-ttu-id="d63bf-133">En esa situación, puede identificarse por su icono único o por la descripción de tipo "Microsoft Visual Studio solución".</span><span class="sxs-lookup"><span data-stu-id="d63bf-133">In that situation, it can be identified by its unique icon or by its type description "Microsoft Visual Studio Solution".</span></span>

     

3.  <span data-ttu-id="d63bf-134">En el menú **compilar** , seleccione **compilar solución**.</span><span class="sxs-lookup"><span data-stu-id="d63bf-134">From the **Build** menu, select **Build Solution**.</span></span>

> [!Note]  
> <span data-ttu-id="d63bf-135">Si el sistema de destino es 64 bits (x64), este controlador de vista previa de ejemplo debe compilarse como una aplicación de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="d63bf-135">If the target system is 64-bit (x64), this sample preview handler must be built as a 64-bit application.</span></span>

 

## <a name="running-the-sample"></a><span data-ttu-id="d63bf-136">Ejecutar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="d63bf-136">Running the Sample</span></span>

1.  <span data-ttu-id="d63bf-137">Abra la ventana del símbolo del sistema y navegue hasta el directorio de proyecto de **RecipePreviewHandler** compilado.</span><span class="sxs-lookup"><span data-stu-id="d63bf-137">Open the command prompt window and navigate to the built **RecipePreviewHandler** project directory.</span></span> <span data-ttu-id="d63bf-138">Por ejemplo, `C:\Program Files\MicrosoftSDKs\Windows\v7.0\Samples\WinUI\Shell\AppShellIntegration\RecipePreviewHandler\RecipePreviewHandler`.</span><span class="sxs-lookup"><span data-stu-id="d63bf-138">For example, `C:\Program Files\MicrosoftSDKs\Windows\v7.0\Samples\WinUI\Shell\AppShellIntegration\RecipePreviewHandler\RecipePreviewHandler`.</span></span> <span data-ttu-id="d63bf-139">Escriba `regsvr32.exe PreviewHandlerSDKSample.dll` para registrar el controlador.</span><span class="sxs-lookup"><span data-stu-id="d63bf-139">Enter `regsvr32.exe PreviewHandlerSDKSample.dll` to register the handler.</span></span>
2.  <span data-ttu-id="d63bf-140">Abra el explorador de Windows y muestre el panel de vista previa si aún no se muestra.</span><span class="sxs-lookup"><span data-stu-id="d63bf-140">Open Windows Explorer and show the preview pane if it is not already displayed.</span></span>
    -   <span data-ttu-id="d63bf-141">**Windows 7**: haga clic en el botón panel de vista previa.</span><span class="sxs-lookup"><span data-stu-id="d63bf-141">**Windows 7**: Click the preview pane button.</span></span>
    -   <span data-ttu-id="d63bf-142">**Windows Vista**: haga clic en el menú **organizar** , vaya al submenú **diseño** y seleccione **Panel de vista previa**.</span><span class="sxs-lookup"><span data-stu-id="d63bf-142">**Windows Vista**: Click the **Organize** menu, go to the **Layout** submenu and select **Preview Pane**.</span></span>
3.  <span data-ttu-id="d63bf-143">Use el explorador de Windows para navegar al directorio del proyecto **RecipePreviewHandler** .</span><span class="sxs-lookup"><span data-stu-id="d63bf-143">Use Windows Explorer to navigate to the **RecipePreviewHandler** project directory.</span></span>
4.  <span data-ttu-id="d63bf-144">Seleccione el archivo example. Recipe.</span><span class="sxs-lookup"><span data-stu-id="d63bf-144">Select the example .recipe file.</span></span>

<span data-ttu-id="d63bf-145">Para hacer que la salida de 32 bits (x86) y 64 bits (x64) funcione en una versión de 64 bits de Windows, establezca el valor de **AppID** en el host de suplentes WOW64 `{534A1E02-D58F-44f0-B58B-36CBED287C7C}` , como se muestra en el código siguiente.</span><span class="sxs-lookup"><span data-stu-id="d63bf-145">To make both the 32-bit (x86) and 64-bit (x64) output work on a 64-bit version of Windows, set the **AppId** value to the WOW64 surrogate host `{534A1E02-D58F-44f0-B58B-36CBED287C7C}`, as shown in the following code.</span></span>


```
{HKEY_CURRENT_USER,   
 L"Software\\Classes\\CLSID\\" SZ_CLSID_RecipePreviewHandler,
 L"AppID",
 L"{534A1E02-D58F-44f0-B58B-36CBED287C7C}"}
```



## <a name="unregistering-the-sample-preview-handler-dll"></a><span data-ttu-id="d63bf-146">Anular el registro del archivo DLL del controlador de vista previa de ejemplo</span><span class="sxs-lookup"><span data-stu-id="d63bf-146">Unregistering the Sample Preview Handler DLL</span></span>

-   <span data-ttu-id="d63bf-147">Abra la ventana del símbolo del sistema y escriba `regsvr32.exe /u PreviewHandlerSDKSample.dll` para anular el registro del controlador.</span><span class="sxs-lookup"><span data-stu-id="d63bf-147">Open the command prompt window and enter `regsvr32.exe /u PreviewHandlerSDKSample.dll` to unregister the handler.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d63bf-148">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d63bf-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d63bf-149">**IPreviewHandler**</span><span class="sxs-lookup"><span data-stu-id="d63bf-149">**IPreviewHandler**</span></span>](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipreviewhandler)
</dt> <dt>

[<span data-ttu-id="d63bf-150">**IPreviewHandlerFrame**</span><span class="sxs-lookup"><span data-stu-id="d63bf-150">**IPreviewHandlerFrame**</span></span>](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipreviewhandlerframe)
</dt> <dt>

[<span data-ttu-id="d63bf-151">Identificadores de modelo de usuario de la aplicación (AppUserModelIDs)</span><span class="sxs-lookup"><span data-stu-id="d63bf-151">Application User Model IDs (AppUserModelIDs)</span></span>](appids.md)
</dt> </dl>

 

 
