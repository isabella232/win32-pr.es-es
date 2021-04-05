---
description: Con Windows Vista, el árbol de elementos de adquisición de imágenes de Windows (WIA) ha cambiado significativamente.
ms.assetid: dda87bcc-2315-4f0d-87a0-d5a33d5d929a
title: Acerca del árbol de elementos IWiaItem2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4d3e7d39319c7b1c94f88612c5d571f17f2a027
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909874"
---
# <a name="about-the-iwiaitem2-item-tree"></a><span data-ttu-id="bf81f-103">Acerca del árbol de elementos IWiaItem2</span><span class="sxs-lookup"><span data-stu-id="bf81f-103">About the IWiaItem2 Item Tree</span></span>

<span data-ttu-id="bf81f-104">Con Windows Vista, el árbol de elementos de adquisición de imágenes de Windows (WIA) ha cambiado significativamente.</span><span class="sxs-lookup"><span data-stu-id="bf81f-104">With Windows Vista, the Windows Image Acquisition (WIA) item tree has changed significantly.</span></span> <span data-ttu-id="bf81f-105">Los elementos [**IWiaItem2**](-wia-iwiaitem2.md) se usan para representar los atributos del dispositivo y los datos del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="bf81f-105">[**IWiaItem2**](-wia-iwiaitem2.md) items are used to represent device attributes and device data.</span></span> <span data-ttu-id="bf81f-106">Las aplicaciones de imágenes ven un dispositivo de adquisición de imágenes de Windows (WIA) 2,0 como un árbol jerárquico de elementos, con el elemento raíz que representa el propio dispositivo y los elementos secundarios que representan elementos como orígenes de datos programables, imágenes o carpetas que contienen imágenes.</span><span class="sxs-lookup"><span data-stu-id="bf81f-106">Imaging applications see a Windows Image Acquisition (WIA) 2.0 device as a hierarchical tree of items, with the root item representing the device itself and the child items representing things like programmable data sources, images, or folders that contain images.</span></span>

-   [<span data-ttu-id="bf81f-107">Elementos de aplicación</span><span class="sxs-lookup"><span data-stu-id="bf81f-107">Application Items</span></span>](#application-items)
-   [<span data-ttu-id="bf81f-108">Marcas de elemento</span><span class="sxs-lookup"><span data-stu-id="bf81f-108">Item Flags</span></span>](#item-flags)
-   [<span data-ttu-id="bf81f-109">Categorías de elementos</span><span class="sxs-lookup"><span data-stu-id="bf81f-109">Item Categories</span></span>](#item-categories)
-   [<span data-ttu-id="bf81f-110">Elemento raíz</span><span class="sxs-lookup"><span data-stu-id="bf81f-110">Root Item</span></span>](#root-item)
-   [<span data-ttu-id="bf81f-111">Elemento de datos</span><span class="sxs-lookup"><span data-stu-id="bf81f-111">Data Item</span></span>](#data-item)
-   [<span data-ttu-id="bf81f-112">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="bf81f-112">Related topics</span></span>](#related-topics)

## <a name="application-items"></a><span data-ttu-id="bf81f-113">Elementos de aplicación</span><span class="sxs-lookup"><span data-stu-id="bf81f-113">Application Items</span></span>

<span data-ttu-id="bf81f-114">El árbol de elementos de WIA 2,0 que puede ver una aplicación es independiente del árbol creado y mantenido por un minicontrolador de WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="bf81f-114">The WIA 2.0 item tree that an application can see is separate from the tree created and maintained by a WIA 2.0 minidriver.</span></span> <span data-ttu-id="bf81f-115">Cuando un minicontrolador crea un árbol, el servicio WIA 2,0 usa este árbol de elementos de WIA 2,0 como guía para crear una copia del árbol que las aplicaciones de imágenes pueden ver.</span><span class="sxs-lookup"><span data-stu-id="bf81f-115">When a minidriver creates a tree, the WIA 2.0 service uses this WIA 2.0 item tree as a guide to create a copy of the tree that can be viewed by imaging applications.</span></span> <span data-ttu-id="bf81f-116">Los elementos del árbol copiado se denominan elementos de la *aplicación* .</span><span class="sxs-lookup"><span data-stu-id="bf81f-116">Items in the copied tree are called *application* items.</span></span> <span data-ttu-id="bf81f-117">Los elementos del árbol creados por un minicontrolador se denominan elementos de *controlador* .</span><span class="sxs-lookup"><span data-stu-id="bf81f-117">Items in the tree created by a minidriver are called *driver* items.</span></span>

<span data-ttu-id="bf81f-118">Un elemento WIA puede representar un origen de datos programable para el alimentador de documentos de un escáner o los datos almacenados en ese dispositivo.</span><span class="sxs-lookup"><span data-stu-id="bf81f-118">A WIA item can represent a programmable data source for a scanner's document feeder or the data stored on that device.</span></span> <span data-ttu-id="bf81f-119">Un dispositivo WIA debe dividirse en elementos individuales que describan los diferentes datos generados por ese dispositivo.</span><span class="sxs-lookup"><span data-stu-id="bf81f-119">A WIA device should be divided into individual items that describe different data produced by that device.</span></span>

<span data-ttu-id="bf81f-120">Por ejemplo, un escáner WIA que admite el análisis de escáneres y el examen del alimentador de documentos podría dividirse en dos elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="bf81f-120">For example, a WIA scanner that supports both flatbed scanning and document feeder scanning might be divided into two child items.</span></span> <span data-ttu-id="bf81f-121">Una representa la funcionalidad de digitalización plana y la otra representa la funcionalidad de exploración del alimentador de documentos.</span><span class="sxs-lookup"><span data-stu-id="bf81f-121">One represents the flatbed scanning functionality and the other represents the document feeder scanning functionality.</span></span>

<span data-ttu-id="bf81f-122">Se pueden colocar varias imágenes en un escáner plano y examinar al mismo tiempo en una carpeta.</span><span class="sxs-lookup"><span data-stu-id="bf81f-122">Multiple images laid out on a flatbed scanner and scanned at the same time can be placed in one folder.</span></span> <span data-ttu-id="bf81f-123">Con el filtro de segmentación ([**IWiaSegmentationFilter**](-wia-iwiasegmentationfilter.md)), cada imagen o subregión se puede crear como un elemento secundario de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="bf81f-123">Using the segmentation filter ([**IWiaSegmentationFilter**](-wia-iwiasegmentationfilter.md)), each image or subregion can then be created as a child item of the folder.</span></span>

<span data-ttu-id="bf81f-124">El árbol WIA de un dispositivo de cámara que almacena fotos ("película") puede dividirse en elementos que representan carpetas, subcarpetas y fotos.</span><span class="sxs-lookup"><span data-stu-id="bf81f-124">The WIA tree for a camera device that stores photos ("Film") can be divided into items that represent folders, subfolders, and photos.</span></span>

## <a name="item-flags"></a><span data-ttu-id="bf81f-125">Marcas de elemento</span><span class="sxs-lookup"><span data-stu-id="bf81f-125">Item Flags</span></span>

<span data-ttu-id="bf81f-126">Las marcas de elementos WIA ayudan a clasificar el contenido o el comportamiento compatible de un elemento WIA determinado.</span><span class="sxs-lookup"><span data-stu-id="bf81f-126">WIA item flags help classify the content or supported behavior of a particular WIA item.</span></span> <span data-ttu-id="bf81f-127">Las marcas de elementos WIA se dividen en dos grupos.</span><span class="sxs-lookup"><span data-stu-id="bf81f-127">WIA item flags fall into two groups.</span></span>

1.  <span data-ttu-id="bf81f-128">Las marcas de estado del elemento notifican el estado actual del elemento WIA, por ejemplo, [**WiaItemTypeDisconnected**](-wia-wia-item-type-flags.md), **WiaItemTypeDeleted**, etc.</span><span class="sxs-lookup"><span data-stu-id="bf81f-128">Item status flags report the current state of the WIA item, for example, [**WiaItemTypeDisconnected**](-wia-wia-item-type-flags.md), **WiaItemTypeDeleted**, and so forth.</span></span>
2.  <span data-ttu-id="bf81f-129">Los indicadores de uso y representación de datos de elementos notifican los datos que el elemento WIA representa o pueden generar si se transfieren.</span><span class="sxs-lookup"><span data-stu-id="bf81f-129">Item data representation/usage flags report the data that the WIA item represents or can produce if transferred.</span></span> <span data-ttu-id="bf81f-130">Por ejemplo, [**WiaItemTypeImage**](-wia-wia-item-type-flags.md) es una marca de representación de datos que indica a la aplicación que los datos asociados al elemento WIA actual son datos de imagen y deben tener propiedades de datos de imagen.</span><span class="sxs-lookup"><span data-stu-id="bf81f-130">For example, [**WiaItemTypeImage**](-wia-wia-item-type-flags.md) is a data representation flag that tells the application the data associated with the current WIA item is image data and should have image data properties.</span></span> <span data-ttu-id="bf81f-131">**WIA \_ \_ \_ Marcas de elemento IPA** es una marca de uso de elementos que indica a la aplicación que el elemento WIA es configurable y sigue un conjunto de reglas de configuración predefinidas basadas en la [**\_ \_ \_ categoría de elemento IPA de WIA**](-wia-wiaitempropcommonitem.md) , y que la configuración puede cambiar el resultado de cada transferencia de datos.</span><span class="sxs-lookup"><span data-stu-id="bf81f-131">**WIA\_IPA\_ITEM\_FLAGS** is an item usage flag that tells the application that the WIA item is configurable and follows a set of predefined configuration rules based on the [**WIA\_IPA\_ITEM\_CATEGORY**](-wia-wiaitempropcommonitem.md) and that the configuration can possibly change the result for each data transfer.</span></span> <span data-ttu-id="bf81f-132">(Para obtener más información sobre las definiciones de categoría [, vea categorías de elementos item Categories](#item-categories) ).</span><span class="sxs-lookup"><span data-stu-id="bf81f-132">(For more information about category definitions, see [Item Categories](#item-categories) item categories.)</span></span>

<span data-ttu-id="bf81f-133">En el gráfico siguiente se muestra un ejemplo de un árbol de elementos WIA y las distintas marcas que pueden estar asociadas a cada elemento.</span><span class="sxs-lookup"><span data-stu-id="bf81f-133">The following graphic shows an example of a WIA item tree and the various flags that might be associated with each item.</span></span>

![ejemplos de marcas de elemento para los elementos de un árbol](images/scannertree1.jpg)

## <a name="item-categories"></a><span data-ttu-id="bf81f-135">Categorías de elementos</span><span class="sxs-lookup"><span data-stu-id="bf81f-135">Item Categories</span></span>

<span data-ttu-id="bf81f-136">Los elementos de WIA se agrupan en categorías mediante los valores de propiedad de [**\_ \_ \_ categoría de elemento IPA de WIA**](-wia-wiaitempropcommonitem.md) .</span><span class="sxs-lookup"><span data-stu-id="bf81f-136">WIA items are grouped into categories using the [**WIA\_IPA\_ITEM\_CATEGORY**](-wia-wiaitempropcommonitem.md) property values.</span></span> <span data-ttu-id="bf81f-137">Estas categorías definen cómo se trata o se utiliza un elemento WIA.</span><span class="sxs-lookup"><span data-stu-id="bf81f-137">These categories define how a WIA item is to be treated or used.</span></span> <span data-ttu-id="bf81f-138">Por ejemplo, si el elemento representa un archivo terminado ( \_ el archivo de categoría de WIA \_ finalizada \_ ), una aplicación WIA debe asumir que los datos son estáticos y se encuentran en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="bf81f-138">For example, if the item represents a finished file (WIA\_CATEGORY\_FINISHED\_FILE), a WIA application should assume that the data is static and located on the device.</span></span> <span data-ttu-id="bf81f-139">Si el elemento representa un alimentador ( \_ alimentador de categoría WIA \_ ), la aplicación debe esperar que contenga las propiedades necesarias del alimentador de documentos y que funcione como un alimentador de documentos.</span><span class="sxs-lookup"><span data-stu-id="bf81f-139">If the item represents a feeder (WIA\_CATEGORY\_FEEDER), the application should expect it to contain the required document feeder properties and operate like a document feeder.</span></span>

<span data-ttu-id="bf81f-140">Las categorías definidas por WIA son:</span><span class="sxs-lookup"><span data-stu-id="bf81f-140">The categories defined by WIA are:</span></span>

-   <span data-ttu-id="bf81f-141">Categoría de WIA \_ \_ auto</span><span class="sxs-lookup"><span data-stu-id="bf81f-141">WIA\_CATEGORY\_AUTO</span></span>
-   <span data-ttu-id="bf81f-142">\_alimentador de categoría WIA \_</span><span class="sxs-lookup"><span data-stu-id="bf81f-142">WIA\_CATEGORY\_FEEDER</span></span>
-   <span data-ttu-id="bf81f-143">\_película de categoría WIA \_</span><span class="sxs-lookup"><span data-stu-id="bf81f-143">WIA\_CATEGORY\_FILM</span></span>
-   <span data-ttu-id="bf81f-144">archivo de categoría de WIA \_ \_ finalizada \_</span><span class="sxs-lookup"><span data-stu-id="bf81f-144">WIA\_CATEGORY\_FINISHED\_FILE</span></span>
-   <span data-ttu-id="bf81f-145">plano de la \_ categoría WIA \_</span><span class="sxs-lookup"><span data-stu-id="bf81f-145">WIA\_CATEGORY\_FLATBED</span></span>

<span data-ttu-id="bf81f-146">Por ejemplo, el elemento plano de un escáner puede tener [**las \_ \_ \_ marcas de elemento del IPA de WIA**](-wia-wiaitempropcommonitem.md) establecidas en [**WiaItemTypeImage**](-wia-wia-item-type-flags.md), **WiaItemTypeTransfer** y **WiaItemTypeProgrammableDataSource**, y la propiedad **\_ \_ \_ categoría de elemento IPA de WIA** establecida en la categoría de WIA \_ \_ plano.</span><span class="sxs-lookup"><span data-stu-id="bf81f-146">For example, a scanner's flatbed item may have the [**WIA\_IPA\_ITEM\_FLAGS**](-wia-wiaitempropcommonitem.md) set to [**WiaItemTypeImage**](-wia-wia-item-type-flags.md), **WiaItemTypeTransfer**, and **WiaItemTypeProgrammableDataSource**, and the **WIA\_IPA\_ITEM\_CATEGORY** property set to WIA\_CATEGORY\_FLATBED.</span></span>

<span data-ttu-id="bf81f-147">En la tabla siguiente se muestra la agrupación de categorías WIA con marcas de elementos y elementos WIA.</span><span class="sxs-lookup"><span data-stu-id="bf81f-147">The following table shows WIA category grouping with item flags and WIA items.</span></span> <span data-ttu-id="bf81f-148">En esta tabla no se incluye una lista completa de las marcas de elementos de WIA definidas por WIA.</span><span class="sxs-lookup"><span data-stu-id="bf81f-148">This table does not include a full list of the WIA item flags defined by WIA.</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bf81f-149">Categoría WIA</span><span class="sxs-lookup"><span data-stu-id="bf81f-149">WIA Category</span></span></th>
<th><span data-ttu-id="bf81f-150">Marcas de elemento WIA válidas</span><span class="sxs-lookup"><span data-stu-id="bf81f-150">Valid WIA Item Flags</span></span></th>
<th><span data-ttu-id="bf81f-151">Conjunto de propiedades de WIA</span><span class="sxs-lookup"><span data-stu-id="bf81f-151">WIA Property Set</span></span></th>
<th><span data-ttu-id="bf81f-152">Elementos WIA</span><span class="sxs-lookup"><span data-stu-id="bf81f-152">WIA Items</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="bf81f-153">WIA_CATEGORY_AUTO</span><span class="sxs-lookup"><span data-stu-id="bf81f-153">WIA_CATEGORY_AUTO</span></span></td>
<td><ul>
<li><span data-ttu-id="bf81f-154"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeProgrammableDataSource</strong></a></span><span class="sxs-lookup"><span data-stu-id="bf81f-154"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeProgrammableDataSource</strong></a></span></span></li>
<li><span data-ttu-id="bf81f-155"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeImage</strong></a></span><span class="sxs-lookup"><span data-stu-id="bf81f-155"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeImage</strong></a></span></span></li>
<li><span data-ttu-id="bf81f-156"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeTransfer</strong></a></span><span class="sxs-lookup"><span data-stu-id="bf81f-156"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeTransfer</strong></a></span></span></li>
<li><span data-ttu-id="bf81f-157"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeFile</strong></a></span><span class="sxs-lookup"><span data-stu-id="bf81f-157"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeFile</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="bf81f-158">El conjunto de propiedades incluye propiedades del escáner configuradas automáticamente.</span><span class="sxs-lookup"><span data-stu-id="bf81f-158">Property set includes auto-configured scanner properties.</span></span></td>
<td><span data-ttu-id="bf81f-159">Elemento automático WIA que representa la configuración de exploración automática del escáner.</span><span class="sxs-lookup"><span data-stu-id="bf81f-159">WIA auto item that represents the scanner's auto-configured scanning settings.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bf81f-160">WIA_CATEGORY_FEEDER</span><span class="sxs-lookup"><span data-stu-id="bf81f-160">WIA_CATEGORY_FEEDER</span></span></td>
<td><ul>
<li><span data-ttu-id="bf81f-161"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeProgrammableDataSource</strong></a></span><span class="sxs-lookup"><span data-stu-id="bf81f-161"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeProgrammableDataSource</strong></a></span></span></li>
<li><span data-ttu-id="bf81f-162"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeImage</strong></a></span><span class="sxs-lookup"><span data-stu-id="bf81f-162"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeImage</strong></a></span></span></li>
<li><span data-ttu-id="bf81f-163"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeDocument</strong></a></span><span class="sxs-lookup"><span data-stu-id="bf81f-163"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeDocument</strong></a></span></span></li>
<li><span data-ttu-id="bf81f-164"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeTransfer</strong></a></span><span class="sxs-lookup"><span data-stu-id="bf81f-164"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeTransfer</strong></a></span></span></li>
<li><span data-ttu-id="bf81f-165"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeFolder</strong></a></span><span class="sxs-lookup"><span data-stu-id="bf81f-165"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeFolder</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="bf81f-166">El conjunto de propiedades incluye propiedades de control de escáner del alimentador (normalmente conjunto de propiedades específicas del documento y imagen).</span><span class="sxs-lookup"><span data-stu-id="bf81f-166">Property set includes feeder scanner control properties (usually image and document specific property set).</span></span></td>
<td><span data-ttu-id="bf81f-167">Elementos del alimentador WIA, incluidos los elementos secundarios que representan las páginas frontal y posterior de un documento.</span><span class="sxs-lookup"><span data-stu-id="bf81f-167">WIA Feeder items, including child items that represent the front and back pages of a document.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bf81f-168">WIA_CATEGORY_FILM</span><span class="sxs-lookup"><span data-stu-id="bf81f-168">WIA_CATEGORY_FILM</span></span></td>
<td><ul>
<li><span data-ttu-id="bf81f-169"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeProgrammableDataSource</strong></a></span><span class="sxs-lookup"><span data-stu-id="bf81f-169"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeProgrammableDataSource</strong></a></span></span></li>
<li><span data-ttu-id="bf81f-170"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeImage</strong></a></span><span class="sxs-lookup"><span data-stu-id="bf81f-170"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeImage</strong></a></span></span></li>
<li><span data-ttu-id="bf81f-171"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeTransfer</strong></a></span><span class="sxs-lookup"><span data-stu-id="bf81f-171"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeTransfer</strong></a></span></span></li>
<li><span data-ttu-id="bf81f-172"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeFolder</strong></a></span><span class="sxs-lookup"><span data-stu-id="bf81f-172"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeFolder</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="bf81f-173">El conjunto de propiedades incluye propiedades de control de escáner de película (normalmente, conjunto de propiedades específicas de imagen y documento).</span><span class="sxs-lookup"><span data-stu-id="bf81f-173">Property set includes film scanner control properties (usually image and document specific property set).</span></span></td>
<td><span data-ttu-id="bf81f-174">Elementos de película WIA, incluidos los elementos secundarios que representan los fotogramas de digitalización individuales.</span><span class="sxs-lookup"><span data-stu-id="bf81f-174">WIA Film items, including child items that represent the individual scanning frames.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bf81f-175">WIA_CATEGORY_FINISHED_FILE</span><span class="sxs-lookup"><span data-stu-id="bf81f-175">WIA_CATEGORY_FINISHED_FILE</span></span></td>
<td><ul>
<li><span data-ttu-id="bf81f-176"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeFolder</strong></a></span><span class="sxs-lookup"><span data-stu-id="bf81f-176"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeFolder</strong></a></span></span></li>
<li><span data-ttu-id="bf81f-177"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeImage</strong></a></span><span class="sxs-lookup"><span data-stu-id="bf81f-177"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeImage</strong></a></span></span></li>
<li><span data-ttu-id="bf81f-178"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeAudio</strong></a></span><span class="sxs-lookup"><span data-stu-id="bf81f-178"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeAudio</strong></a></span></span></li>
<li><span data-ttu-id="bf81f-179"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeVideo</strong></a></span><span class="sxs-lookup"><span data-stu-id="bf81f-179"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeVideo</strong></a></span></span></li>
<li><span data-ttu-id="bf81f-180"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeDocument</strong></a></span><span class="sxs-lookup"><span data-stu-id="bf81f-180"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeDocument</strong></a></span></span></li>
<li><span data-ttu-id="bf81f-181"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeTransfer</strong></a></span><span class="sxs-lookup"><span data-stu-id="bf81f-181"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeTransfer</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="bf81f-182">La propiedad establecida en este elemento depende del tipo de elemento indicado.</span><span class="sxs-lookup"><span data-stu-id="bf81f-182">The property set on this item depends on the item type reported.</span></span> <span data-ttu-id="bf81f-183">Por ejemplo, <a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeImage</strong></a> debe incluir algunas propiedades de elementos de imagen, como bits por píxel y así sucesivamente.</span><span class="sxs-lookup"><span data-stu-id="bf81f-183">For example, <a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeImage</strong></a> should include some image item properties, like bits per pixel and so forth.</span></span></td>
<td><span data-ttu-id="bf81f-184">Elementos de almacenamiento WIA, incluidos los elementos secundarios que representan el contenido del archivo finalizado (archivos de datos como JPEG, HTML, TXT, etc.).</span><span class="sxs-lookup"><span data-stu-id="bf81f-184">WIA storage items, including child items that represent finished file content (data files like JPEG, HTML, TXT, and so forth).</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bf81f-185">WIA_CATEGORY_FLATBED</span><span class="sxs-lookup"><span data-stu-id="bf81f-185">WIA_CATEGORY_FLATBED</span></span></td>
<td><ul>
<li><span data-ttu-id="bf81f-186"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeProgrammableDataSource</strong></a></span><span class="sxs-lookup"><span data-stu-id="bf81f-186"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeProgrammableDataSource</strong></a></span></span></li>
<li><span data-ttu-id="bf81f-187"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeImage</strong></a></span><span class="sxs-lookup"><span data-stu-id="bf81f-187"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeImage</strong></a></span></span></li>
<li><span data-ttu-id="bf81f-188"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeDocument</strong></a></span><span class="sxs-lookup"><span data-stu-id="bf81f-188"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeDocument</strong></a></span></span></li>
<li><span data-ttu-id="bf81f-189"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeTransfer</strong></a></span><span class="sxs-lookup"><span data-stu-id="bf81f-189"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeTransfer</strong></a></span></span></li>
<li><span data-ttu-id="bf81f-190"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeFolder</strong></a>: puede estar presente si el escáner admite el análisis de varios elementos.</span><span class="sxs-lookup"><span data-stu-id="bf81f-190"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeFolder</strong></a>—may be present if the scanner supports multi-item scanning.</span></span></li>
<li><span data-ttu-id="bf81f-191"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeGenerated</strong></a>: puede estar presente si la aplicación genera un elemento WIA durante una sesión de examen de varios elementos.</span><span class="sxs-lookup"><span data-stu-id="bf81f-191"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeGenerated</strong></a>—may be present if the application generates a WIA item during a multi-item scanning session.</span></span></li>
</ul></td>
<td><span data-ttu-id="bf81f-192">El conjunto de propiedades incluye las propiedades de control de escáner plano (normalmente, la imagen y el conjunto de propiedades específicas del documento).</span><span class="sxs-lookup"><span data-stu-id="bf81f-192">The property set includes flatbed scanner control properties (usually image and document specific property set).</span></span></td>
<td><span data-ttu-id="bf81f-193">Elementos de escáner WIA, incluidos los elementos secundarios que representan las regiones que se están analizando en la placa de escáner.</span><span class="sxs-lookup"><span data-stu-id="bf81f-193">WIA flatbed items, including child items that represent regions being scanned on the scanner's flatbed platen.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="bf81f-194">En el gráfico siguiente se muestra un ejemplo de un árbol de elementos WIA y las distintas categorías que pueden estar asociadas a cada elemento.</span><span class="sxs-lookup"><span data-stu-id="bf81f-194">The following graphic shows an example of a WIA item tree and the various categories that might be associated with each item.</span></span>

![ejemplos de categorías de elementos para los elementos de un árbol](images/scannertree2.jpg)

## <a name="root-item"></a><span data-ttu-id="bf81f-196">Elemento raíz</span><span class="sxs-lookup"><span data-stu-id="bf81f-196">Root Item</span></span>

<span data-ttu-id="bf81f-197">Un elemento raíz de WIA es un elemento de carpeta marcado con marcas [**WiaItemTypeRoot**](-wia-wia-item-type-flags.md) y **WiaItemTypeDevice** que representa el propio dispositivo.</span><span class="sxs-lookup"><span data-stu-id="bf81f-197">A WIA root item is a folder item marked with [**WiaItemTypeRoot**](-wia-wia-item-type-flags.md) and **WiaItemTypeDevice** flags that represents the device itself.</span></span> <span data-ttu-id="bf81f-198">Contiene atributos de dispositivo como el fabricante, el nombre del dispositivo y los atributos del controlador, como la versión del controlador y el identificador de clase (CLSID) de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="bf81f-198">It contains device attributes like manufacturer, device name, and driver attributes like driver version and user interface class identifier (CLSID).</span></span> <span data-ttu-id="bf81f-199">Las aplicaciones de creación de imágenes obtienen la raíz del árbol de elementos WIA mediante una llamada al método [**IWiaDevMgr2:: CreateDevice**](-wia-iwiadevmgr2-createdevice.md) .</span><span class="sxs-lookup"><span data-stu-id="bf81f-199">Imaging applications get the root to the WIA item tree by calling [**IWiaDevMgr2::CreateDevice**](-wia-iwiadevmgr2-createdevice.md) method.</span></span> <span data-ttu-id="bf81f-200">La aplicación utiliza el elemento raíz para obtener acceso a los elementos de WIA secundarios individuales enumerando el árbol (vea [**IEnumWiaItem2**](-wia-ienumwiaitem2.md)).</span><span class="sxs-lookup"><span data-stu-id="bf81f-200">The application uses the root item to gain access to the individual child WIA items by enumerating the tree (see [**IEnumWiaItem2**](-wia-ienumwiaitem2.md)).</span></span>

## <a name="data-item"></a><span data-ttu-id="bf81f-201">Data Item</span><span class="sxs-lookup"><span data-stu-id="bf81f-201">Data Item</span></span>

<span data-ttu-id="bf81f-202">Cualquier elemento que se pueda usar para transferir datos se considera un elemento de datos.</span><span class="sxs-lookup"><span data-stu-id="bf81f-202">Any item that can be use to transfer data is considered a data item.</span></span> <span data-ttu-id="bf81f-203">Esto incluye los elementos marcados con la marca [**WiaItemTypeProgrammableDataSource**](-wia-wia-item-type-flags.md) .</span><span class="sxs-lookup"><span data-stu-id="bf81f-203">This includes items marked with the [**WiaItemTypeProgrammableDataSource**](-wia-wia-item-type-flags.md) flag.</span></span>

<span data-ttu-id="bf81f-204">Los elementos de carpeta y los elementos que no son de carpeta pueden exponer la capacidad de transferir datos marcando con la marca [**WiaItemTypeTransfer**](-wia-wia-item-type-flags.md) .</span><span class="sxs-lookup"><span data-stu-id="bf81f-204">Folder items and nonfolder items can expose the ability to transfer data by being marked with the [**WiaItemTypeTransfer**](-wia-wia-item-type-flags.md) flag.</span></span> <span data-ttu-id="bf81f-205">Cualquier elemento con esta marca establecida tiene que proporcionar las siguientes propiedades de elemento WIA:</span><span class="sxs-lookup"><span data-stu-id="bf81f-205">Any item with this flag set has to provide the following WIA item properties:</span></span>

-   [<span data-ttu-id="bf81f-206">**\_derechos de \_ acceso del IPA de WIA \_**</span><span class="sxs-lookup"><span data-stu-id="bf81f-206">**WIA\_IPA\_ACCESS\_RIGHTS**</span></span>](-wia-wiaitempropcommonitem.md)
-   [<span data-ttu-id="bf81f-207">**\_tamaño del \_ elemento \_ IPA de WIA**</span><span class="sxs-lookup"><span data-stu-id="bf81f-207">**WIA\_IPA\_ITEM\_SIZE**</span></span>](-wia-wiaitempropcommonitem.md)
-   [<span data-ttu-id="bf81f-208">**\_tamaño de \_ búfer de IPA de WIA \_**</span><span class="sxs-lookup"><span data-stu-id="bf81f-208">**WIA\_IPA\_BUFFER\_SIZE**</span></span>](-wia-wiaitempropcommonitem.md)
-   [<span data-ttu-id="bf81f-209">**\_formato de IPA de WIA \_**</span><span class="sxs-lookup"><span data-stu-id="bf81f-209">**WIA\_IPA\_FORMAT**</span></span>](-wia-wiaitempropcommonitem.md)
-   [<span data-ttu-id="bf81f-210">**\_ \_ formato preferido del IPA de WIA \_**</span><span class="sxs-lookup"><span data-stu-id="bf81f-210">**WIA\_IPA\_PREFERRED\_FORMAT**</span></span>](-wia-wiaitempropcommonitem.md)
-   [<span data-ttu-id="bf81f-211">**\_TYMED del IPA de WIA \_**</span><span class="sxs-lookup"><span data-stu-id="bf81f-211">**WIA\_IPA\_TYMED**</span></span>](-wia-wiaitempropcommonitem.md)
-   [<span data-ttu-id="bf81f-212">**\_extensión de \_ nombre de archivo de WIA IPA \_**</span><span class="sxs-lookup"><span data-stu-id="bf81f-212">**WIA\_IPA\_FILENAME\_EXTENSION**</span></span>](-wia-wiaitempropcommonitem.md)

<span data-ttu-id="bf81f-213">Los elementos de origen de datos programables marcados con la marca [**WiaItemTypeTransfer**](-wia-wia-item-type-flags.md) también deben proporcionar el conjunto de propiedades requerido del elemento de datos.</span><span class="sxs-lookup"><span data-stu-id="bf81f-213">Programmable data source items marked with the [**WiaItemTypeTransfer**](-wia-wia-item-type-flags.md) flag must also supply the data item required property set.</span></span>

<span data-ttu-id="bf81f-214">Los elementos de datos WIA pueden tener propiedades adicionales en función de la configuración de la marca del elemento.</span><span class="sxs-lookup"><span data-stu-id="bf81f-214">WIA data items may have additional properties depending on the item's flag settings.</span></span> <span data-ttu-id="bf81f-215">Por ejemplo, los elementos de WIA marcados con la marca [**WiaItemTypeImage**](-wia-wia-item-type-flags.md) deben tener propiedades de información específica de la imagen, como la [**\_ \_ profundidad de IPA de WIA**](-wia-wiaitempropcommonitem.md) y el **\_ \_ número \_ de \_ líneas del IPA de WIA**.</span><span class="sxs-lookup"><span data-stu-id="bf81f-215">For example, WIA items marked with the [**WiaItemTypeImage**](-wia-wia-item-type-flags.md) flag should have image specific information properties, like [**WIA\_IPA\_DEPTH**](-wia-wiaitempropcommonitem.md) and **WIA\_IPA\_NUMBER\_OF\_LINES**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bf81f-216">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="bf81f-216">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="bf81f-217">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="bf81f-217">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="bf81f-218">**IWiaItem2**</span><span class="sxs-lookup"><span data-stu-id="bf81f-218">**IWiaItem2**</span></span>](-wia-iwiaitem2.md)
</dt> <dt>

[<span data-ttu-id="bf81f-219">**IEnumWiaItem2**</span><span class="sxs-lookup"><span data-stu-id="bf81f-219">**IEnumWiaItem2**</span></span>](-wia-ienumwiaitem2.md)
</dt> <dt>

[<span data-ttu-id="bf81f-220">**IWiaDevMgr2**</span><span class="sxs-lookup"><span data-stu-id="bf81f-220">**IWiaDevMgr2**</span></span>](-wia-iwiadevmgr2.md)
</dt> </dl>

 

 



