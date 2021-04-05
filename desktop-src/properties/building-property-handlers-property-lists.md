---
description: Después de evaluar la estrategia de propiedades, debe determinar qué propiedades se deben mostrar en la interfaz de usuario del explorador de Windows y dónde.
ms.assetid: b7af0491-2ece-42b5-8eea-32643854632f
title: Usar listas de propiedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8644e0d51141751ac55d50966cd6163a3359435d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001576"
---
# <a name="using-property-lists"></a><span data-ttu-id="3eb2d-103">Usar listas de propiedades</span><span class="sxs-lookup"><span data-stu-id="3eb2d-103">Using Property Lists</span></span>

<span data-ttu-id="3eb2d-104">Después de evaluar la estrategia de propiedades, debe determinar qué propiedades se deben mostrar en la interfaz de usuario del explorador de Windows y dónde.</span><span class="sxs-lookup"><span data-stu-id="3eb2d-104">After you assess your property strategy, you must determine what properties to show in the Windows Explorer UI, and where.</span></span> <span data-ttu-id="3eb2d-105">Hay varias ubicaciones en las que las propiedades se muestran en modo de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="3eb2d-105">There are various locations where properties are displayed in a read-only manner.</span></span> <span data-ttu-id="3eb2d-106">Por otro lado, la edición de propiedades solo está habilitada en el cuadro de diálogo **propiedades** .</span><span class="sxs-lookup"><span data-stu-id="3eb2d-106">Property editing, on the other hand, is enabled only in the **Properties** dialog box.</span></span> <span data-ttu-id="3eb2d-107">Ese cuadro de diálogo se puede invocar a través del vínculo **Editar propiedades** en el **Panel de vista previa** o en el menú contextual de un elemento.</span><span class="sxs-lookup"><span data-stu-id="3eb2d-107">That dialog box can be invoked through either the **Edit Properties** link in the **Preview Pane** or the shortcut menu of an item.</span></span>

<span data-ttu-id="3eb2d-108">Las listas de propiedades son cadenas delimitadas por punto y coma que tienen el formato siguiente.</span><span class="sxs-lookup"><span data-stu-id="3eb2d-108">The property lists are semi-colon delimited strings that have the following form.</span></span>


```
Prop:[flags]PropertyCanonicalName;[flags]PropertyCanonicalName;
```



<span data-ttu-id="3eb2d-109">La única marca disponible actualmente se muestra en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="3eb2d-109">The only flag currently available is shown in the following table.</span></span>



| <span data-ttu-id="3eb2d-110">Marca</span><span class="sxs-lookup"><span data-stu-id="3eb2d-110">Flag</span></span> | <span data-ttu-id="3eb2d-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="3eb2d-111">Description</span></span>                                                                                                                                                                                   |
|------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \*   | <span data-ttu-id="3eb2d-112">No muestre la propiedad en el **Panel de vista previa** como se indica en el valor de la clave del registro **PreviewDetails** .</span><span class="sxs-lookup"><span data-stu-id="3eb2d-112">Do not show the property in the **Preview Pane** as instructed in the **PreviewDetails** registry key value.</span></span> <span data-ttu-id="3eb2d-113">Vea el ejemplo que sigue a la siguiente tabla si no se establece el valor de esa propiedad.</span><span class="sxs-lookup"><span data-stu-id="3eb2d-113">See the example that follows the next table if that property's value is not set.</span></span> |



 

<span data-ttu-id="3eb2d-114">Después de definir una lista de propiedades, puede almacenar esa cadena en el registro a través del sistema de [asociaciones de archivo de Shell](../shell/fa-file-types.md) estándar en **HKEY \_ classes \_ root.**</span><span class="sxs-lookup"><span data-stu-id="3eb2d-114">After you define a property list, you can store that string in the registry through the standard [Shell file association](../shell/fa-file-types.md) system under **HKEY\_CLASSES\_ROOT.**</span></span> <span data-ttu-id="3eb2d-115">En la tabla siguiente se resumen los valores de las listas de propiedades que se pueden asignar en la clave del registro para una extensión de nombre de archivo determinada.</span><span class="sxs-lookup"><span data-stu-id="3eb2d-115">The following table summarizes the values for the property lists that can be assigned under the registry key for a particular file name extension.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3eb2d-116">Value</span><span class="sxs-lookup"><span data-stu-id="3eb2d-116">Value</span></span></th>
<th><span data-ttu-id="3eb2d-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="3eb2d-117">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3eb2d-118">FullDetails</span><span class="sxs-lookup"><span data-stu-id="3eb2d-118">FullDetails</span></span></td>
<td><span data-ttu-id="3eb2d-119">Las propiedades se muestran en la pestaña <strong>detalles</strong> del cuadro de diálogo <strong>propiedades</strong> .</span><span class="sxs-lookup"><span data-stu-id="3eb2d-119">Properties are displayed on the <strong>Details</strong> tab of the <strong>Properties</strong> dialog box.</span></span> <span data-ttu-id="3eb2d-120">Esta es la lista completa de propiedades que admite el tipo de archivo.</span><span class="sxs-lookup"><span data-stu-id="3eb2d-120">This is the complete list of properties that the file type supports.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3eb2d-121">PreviewDetails</span><span class="sxs-lookup"><span data-stu-id="3eb2d-121">PreviewDetails</span></span></td>
<td><span data-ttu-id="3eb2d-122">Las propiedades se muestran en el <strong>Panel de vista previa</strong>.</span><span class="sxs-lookup"><span data-stu-id="3eb2d-122">Properties are displayed in the <strong>Preview Pane</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3eb2d-123">PreviewTitle</span><span class="sxs-lookup"><span data-stu-id="3eb2d-123">PreviewTitle</span></span></td>
<td><span data-ttu-id="3eb2d-124">Las propiedades se muestran en el área de título del <strong>Panel de vista previa</strong> junto a la miniatura del elemento.</span><span class="sxs-lookup"><span data-stu-id="3eb2d-124">Properties are displayed in the title area of the <strong>Preview Pane</strong> next to the thumbnail for the item.</span></span> <span data-ttu-id="3eb2d-125">El número máximo de entradas es 3.</span><span class="sxs-lookup"><span data-stu-id="3eb2d-125">The maximum number of entries is 3.</span></span> <span data-ttu-id="3eb2d-126">Si la lista de propiedades contiene más del número máximo permitido, se omite el resto de las entradas.</span><span class="sxs-lookup"><span data-stu-id="3eb2d-126">If the property list contains more than the maximum allowable number, the rest of the entries are ignored.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3eb2d-127">TileInfo</span><span class="sxs-lookup"><span data-stu-id="3eb2d-127">TileInfo</span></span></td>
<td><span data-ttu-id="3eb2d-128">Las propiedades se muestran cuando la vista de lista está en modo de vista en <strong>mosaico</strong> .</span><span class="sxs-lookup"><span data-stu-id="3eb2d-128">Properties are displayed when the list view is in <strong>Tiles</strong> view mode.</span></span> <span data-ttu-id="3eb2d-129">El número máximo de entradas es 3.</span><span class="sxs-lookup"><span data-stu-id="3eb2d-129">The maximum number of entries is 3.</span></span> <span data-ttu-id="3eb2d-130">Si la lista de propiedades contiene más del número máximo permitido, se omite el resto de las entradas.</span><span class="sxs-lookup"><span data-stu-id="3eb2d-130">If the property list contains more than the maximum allowable number, the rest of the entries are ignored.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="3eb2d-131">Este valor estaba presente en Windows XP.</span><span class="sxs-lookup"><span data-stu-id="3eb2d-131">This value was present in Windows XP.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3eb2d-132">ExtendedTileInfo</span><span class="sxs-lookup"><span data-stu-id="3eb2d-132">ExtendedTileInfo</span></span></td>
<td><span data-ttu-id="3eb2d-133">Las propiedades se muestran para un elemento cuando la vista de lista está en modo de vista de <strong>mosaico extendido</strong> .</span><span class="sxs-lookup"><span data-stu-id="3eb2d-133">Properties are displayed for an item when the list view is in <strong>Extended Tile</strong> view mode.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3eb2d-134">InfoTip</span><span class="sxs-lookup"><span data-stu-id="3eb2d-134">InfoTip</span></span></td>
<td><span data-ttu-id="3eb2d-135">Las propiedades se muestran en un recuadro informativo cuando un usuario mantiene el mouse sobre un elemento.</span><span class="sxs-lookup"><span data-stu-id="3eb2d-135">Properties are displayed in an infotip when a user hovers over an item.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="3eb2d-136">Este valor estaba presente en Windows XP.</span><span class="sxs-lookup"><span data-stu-id="3eb2d-136">This value was present in Windows XP.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3eb2d-137">QuickTip</span><span class="sxs-lookup"><span data-stu-id="3eb2d-137">QuickTip</span></span></td>
<td><span data-ttu-id="3eb2d-138">Las propiedades se muestran cuando es difícil recuperar propiedades directamente de un elemento, como cuando se debe tener acceso al elemento a través de una conexión de red lenta.</span><span class="sxs-lookup"><span data-stu-id="3eb2d-138">Properties are displayed when it is difficult to retrieve properties directly from an item, such as when the item must be accessed over a slow network connection.</span></span> <span data-ttu-id="3eb2d-139">Se recomienda que las propiedades mencionadas aquí, como tipo o tamaño, no requieran abrir el flujo de archivo para determinar su valor.</span><span class="sxs-lookup"><span data-stu-id="3eb2d-139">It is recommended that the properties named here, such as Type or Size, do not require opening the file stream to determine their value.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="3eb2d-140">Este valor estaba presente en Windows XP.</span><span class="sxs-lookup"><span data-stu-id="3eb2d-140">This value was present in Windows XP.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="3eb2d-141">En el ejemplo siguiente se define el valor de PreviewDetails para un tipo de archivo. Recipe mediante un ProgID de **RecipeKey**.</span><span class="sxs-lookup"><span data-stu-id="3eb2d-141">The example below defines the PreviewDetails value for a .recipe file type, using a ProgID of **RecipeKey**.</span></span>

```
HKEY_CLASSES_ROOT
   .recipe
      (Default) = Recipe File
   RecipeFile
      PreviewDetails = prop:*System.Title;*System.Author
```

<span data-ttu-id="3eb2d-142">Como se explica en el tema [Asociación de archivos de Shell](../shell/fa-file-types.md) , las asociaciones de archivo se pueden describir para el formato más específico del más general.</span><span class="sxs-lookup"><span data-stu-id="3eb2d-142">As explained in the [Shell file association](../shell/fa-file-types.md) topic, file associations can be described for the most specific to the most general form.</span></span> <span data-ttu-id="3eb2d-143">La forma más específica es la extensión de nombre de archivo única y la forma más genérica es una clave que se aplica a todos los archivos y carpetas de archivos.</span><span class="sxs-lookup"><span data-stu-id="3eb2d-143">The most specific form is the single file name extension and the most generic form is a key that applies to all files and file folders.</span></span> <span data-ttu-id="3eb2d-144">Entre esos dos extremos, también puede definir un [ProgID](../shell/fa-progids.md) que agrupe un conjunto de extensiones de nombre de archivo (por ejemplo, los tipos. jpg y. JPEG agrupados como **jpegfile**).</span><span class="sxs-lookup"><span data-stu-id="3eb2d-144">Between those two extremes, you can also define a [PROGID](../shell/fa-progids.md) that groups a set of file name extensions together (for instance, .jpg and .jpeg types grouped as **jpegfile**).</span></span> <span data-ttu-id="3eb2d-145">Al definir las listas de propiedades, debe definirlas para los ProgID o, en algunos casos, las extensiones de nombre de archivo específicas.</span><span class="sxs-lookup"><span data-stu-id="3eb2d-145">When you define property lists, you should define them for ProgIDs or, in some cases, specific file name extensions.</span></span> <span data-ttu-id="3eb2d-146">Evite depender de entradas amplias, como la clave **AllFileSystemObjects** .</span><span class="sxs-lookup"><span data-stu-id="3eb2d-146">Avoid relying on broad entries such as the **AllFileSystemObjects** key.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3eb2d-147">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="3eb2d-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3eb2d-148">Descripción de los controladores de propiedades</span><span class="sxs-lookup"><span data-stu-id="3eb2d-148">Understanding Property Handlers</span></span>](./building-property-handlers-properties.md)
</dt> <dt>

[<span data-ttu-id="3eb2d-149">Usar nombres de tipo</span><span class="sxs-lookup"><span data-stu-id="3eb2d-149">Using Kind Names</span></span>](./building-property-handlers-user-friendly-kind-names.md)
</dt> <dt>

[<span data-ttu-id="3eb2d-150">Inicializar controladores de propiedades</span><span class="sxs-lookup"><span data-stu-id="3eb2d-150">Initializing Property Handlers</span></span>](./building-property-handlers-property-handlers.md)
</dt> <dt>

[<span data-ttu-id="3eb2d-151">Registrar y distribuir controladores de propiedades</span><span class="sxs-lookup"><span data-stu-id="3eb2d-151">Registering and Distributing Property Handlers</span></span>](./prophand-reg-dist.md)
</dt> <dt>

[<span data-ttu-id="3eb2d-152">Prácticas recomendadas y preguntas más frecuentes sobre controladores de propiedades</span><span class="sxs-lookup"><span data-stu-id="3eb2d-152">Property Handler Best Practices and FAQ</span></span>](./prophand-bestprac-faq.md)
</dt> </dl>

 

 
