---
description: En el ejemplo de código PropertyEdit se muestra cómo convertir el nombre de la propiedad canónica en una PROPERTYKEY, establecer el valor del almacén de propiedades en el del elemento y volver a escribir los datos en la secuencia de archivos.
ms.assetid: 5918b4f6-6b6f-4229-8f29-1c41f80b3b02
title: PropertyEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa248b9e86f8ab93cccba3d5d6b169d7e8699dbb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907749"
---
# <a name="propertyedit"></a><span data-ttu-id="30e7b-103">PropertyEdit</span><span class="sxs-lookup"><span data-stu-id="30e7b-103">PropertyEdit</span></span>

<span data-ttu-id="30e7b-104">En el ejemplo de código PropertyEdit se muestra cómo convertir el nombre de la propiedad canónica en una PROPERTYKEY, establecer el valor del almacén de propiedades en el del elemento y volver a escribir los datos en la secuencia de archivos.</span><span class="sxs-lookup"><span data-stu-id="30e7b-104">The PropertyEdit code sample demonstrates how to convert the canonical property name to a PROPERTYKEY, set the value of the property store to that of the item, and write the data back to the file stream.</span></span>

<span data-ttu-id="30e7b-105">En este tema se incluyen las siguientes secciones.</span><span class="sxs-lookup"><span data-stu-id="30e7b-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="30e7b-106">Requisitos</span><span class="sxs-lookup"><span data-stu-id="30e7b-106">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="30e7b-107">Descargar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="30e7b-107">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="30e7b-108">Compilar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="30e7b-108">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="30e7b-109">Ejecutar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="30e7b-109">Running the Sample</span></span>](#running-the-sample)
-   [<span data-ttu-id="30e7b-110">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="30e7b-110">Related topics</span></span>](#related-topics)

## <a name="requirements"></a><span data-ttu-id="30e7b-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="30e7b-111">Requirements</span></span>



| <span data-ttu-id="30e7b-112">Producto</span><span class="sxs-lookup"><span data-stu-id="30e7b-112">Product</span></span>     | <span data-ttu-id="30e7b-113">Versión mínima del producto</span><span class="sxs-lookup"><span data-stu-id="30e7b-113">Minimum Product Version</span></span> |
|-------------|-------------------------|
| <span data-ttu-id="30e7b-114">Windows</span><span class="sxs-lookup"><span data-stu-id="30e7b-114">Windows</span></span>     | <span data-ttu-id="30e7b-115">Windows 7</span><span class="sxs-lookup"><span data-stu-id="30e7b-115">Windows 7</span></span>               |
| <span data-ttu-id="30e7b-116">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="30e7b-116">Windows SDK</span></span> | <span data-ttu-id="30e7b-117">7.0</span><span class="sxs-lookup"><span data-stu-id="30e7b-117">7.0</span></span>                     |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="30e7b-118">Descargar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="30e7b-118">Downloading the Sample</span></span>

<span data-ttu-id="30e7b-119">Este ejemplo está disponible en las siguientes ubicaciones.</span><span class="sxs-lookup"><span data-stu-id="30e7b-119">This sample is available in the following locations.</span></span>



| <span data-ttu-id="30e7b-120">Location</span><span class="sxs-lookup"><span data-stu-id="30e7b-120">Location</span></span>      | <span data-ttu-id="30e7b-121">URL de ruta de acceso</span><span class="sxs-lookup"><span data-stu-id="30e7b-121">Path URL</span></span>                                                                  |
|---------------|---------------------------------------------------------------------------|
| <span data-ttu-id="30e7b-122">GitHub</span><span class="sxs-lookup"><span data-stu-id="30e7b-122">GitHub</span></span>  | [<span data-ttu-id="30e7b-123">Ejemplo de PropertyEdit</span><span class="sxs-lookup"><span data-stu-id="30e7b-123">PropertyEdit sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appplatform/PropertyEdit)    |



 

 

> [!Note]  
> <span data-ttu-id="30e7b-124">En todas las versiones de Windows, incluido Windows 7, se recomienda descargar los ejemplos directamente desde GitHub para obtener la versión más actualizada.</span><span class="sxs-lookup"><span data-stu-id="30e7b-124">For all versions of Windows, including Windows 7, it is recommended to download the samples directly from GitHub for the most up to date version.</span></span>

 

## <a name="building-the-sample"></a><span data-ttu-id="30e7b-125">Generar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="30e7b-125">Building the Sample</span></span>

<span data-ttu-id="30e7b-126">Para compilar el ejemplo desde el símbolo del sistema:</span><span class="sxs-lookup"><span data-stu-id="30e7b-126">To build the sample from the Command Prompt:</span></span>

1.  <span data-ttu-id="30e7b-127">Abra la ventana del símbolo del sistema y navegue hasta el directorio del proyecto **PropertyEdit** .</span><span class="sxs-lookup"><span data-stu-id="30e7b-127">Open the Command Prompt window and navigate to the **PropertyEdit** project directory.</span></span> 
2.  <span data-ttu-id="30e7b-128">Escriba `msbuild PropertyEdit.sln`.</span><span class="sxs-lookup"><span data-stu-id="30e7b-128">Enter `msbuild PropertyEdit.sln`.</span></span>

<span data-ttu-id="30e7b-129">Para compilar el ejemplo mediante Microsoft Visual Studio (preferido):</span><span class="sxs-lookup"><span data-stu-id="30e7b-129">To build the sample using Microsoft Visual Studio (preferred):</span></span>

1.  <span data-ttu-id="30e7b-130">Abra el explorador de Windows y navegue hasta el directorio del proyecto **PropertyEdit** .</span><span class="sxs-lookup"><span data-stu-id="30e7b-130">Open Windows Explorer and navigate to the **PropertyEdit** project directory.</span></span>
2.  <span data-ttu-id="30e7b-131">Haga doble clic en el icono del archivo PropertyEdit. sln para abrir el proyecto en Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="30e7b-131">Double-click the icon for the PropertyEdit.sln file to open the project in Visual Studio.</span></span>
    > [!Note]  
    > <span data-ttu-id="30e7b-132">La extensión de nombre de archivo. sln no se muestra en configuración de carpeta predeterminada.</span><span class="sxs-lookup"><span data-stu-id="30e7b-132">The .sln file name extension is not shown under default folder settings.</span></span> <span data-ttu-id="30e7b-133">En esa situación, puede identificarse por su icono único o por su descripción de tipo, "Microsoft Visual Studio solución".</span><span class="sxs-lookup"><span data-stu-id="30e7b-133">In that situation, it can be identified by its unique icon or by its type description, "Microsoft Visual Studio Solution".</span></span>

     

3.  <span data-ttu-id="30e7b-134">En el menú **compilar** , seleccione **compilar solución**.</span><span class="sxs-lookup"><span data-stu-id="30e7b-134">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="30e7b-135">Ejecutar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="30e7b-135">Running the Sample</span></span>

1.  <span data-ttu-id="30e7b-136">Desplácese hasta el directorio que contiene el nuevo ejecutable, mediante la ventana del símbolo del sistema o el explorador de Windows.</span><span class="sxs-lookup"><span data-stu-id="30e7b-136">Navigate to the directory that contains the new executable, using the Command Prompt window or Windows Explorer.</span></span>
2.  <span data-ttu-id="30e7b-137">En el símbolo del sistema, escriba `PropertyEdit.exe` o, en el explorador de Windows, haga doble clic en el icono de PropertyEdit.exe.</span><span class="sxs-lookup"><span data-stu-id="30e7b-137">At the command prompt, enter `PropertyEdit.exe`, or from Windows Explorer, double-click the icon for PropertyEdit.exe.</span></span>

## <a name="related-topics"></a><span data-ttu-id="30e7b-138">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="30e7b-138">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="30e7b-139">**Vista**</span><span class="sxs-lookup"><span data-stu-id="30e7b-139">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="30e7b-140">Ejemplos de código de búsqueda</span><span class="sxs-lookup"><span data-stu-id="30e7b-140">Search Code Samples</span></span>](-search-samples-ovw.md)
</dt> <dt>

<span data-ttu-id="30e7b-141">**Otros recursos**</span><span class="sxs-lookup"><span data-stu-id="30e7b-141">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="30e7b-142">**IPropertyStore**</span><span class="sxs-lookup"><span data-stu-id="30e7b-142">**IPropertyStore**</span></span>](/windows/win32/api/propsys/nn-propsys-ipropertystore)
</dt> <dt>

[<span data-ttu-id="30e7b-143">Acerca de las propiedades y los controladores de propiedades</span><span class="sxs-lookup"><span data-stu-id="30e7b-143">About Properties and Property Handlers</span></span>](../properties/building-property-handlers-properties.md)
</dt> <dt>

<span data-ttu-id="30e7b-144">[Esquema de descripción de propiedad](/previous-versions//cc144127(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="30e7b-144">[Property Description Schema](/previous-versions//cc144127(v=vs.85))</span></span>
</dt> </dl>

 

 
