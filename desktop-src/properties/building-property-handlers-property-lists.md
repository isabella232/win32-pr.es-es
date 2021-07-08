---
description: Después de evaluar la estrategia de propiedades, debe determinar qué propiedades mostrar en la interfaz de usuario Windows Explorer y dónde.
ms.assetid: b7af0491-2ece-42b5-8eea-32643854632f
title: Usar listas de propiedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ade6cba2807e87306aa9cacb3649499d9e5ffe1
ms.sourcegitcommit: ecd0ba4732f5264aab9baa2839c11f7fea36318f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/07/2021
ms.locfileid: "113481920"
---
# <a name="using-property-lists"></a><span data-ttu-id="b62a5-103">Usar listas de propiedades</span><span class="sxs-lookup"><span data-stu-id="b62a5-103">Using Property Lists</span></span>

<span data-ttu-id="b62a5-104">Después de evaluar la estrategia de propiedades, debe determinar qué propiedades mostrar en la interfaz de usuario Windows Explorer y dónde.</span><span class="sxs-lookup"><span data-stu-id="b62a5-104">After you assess your property strategy, you must determine what properties to show in the Windows Explorer UI, and where.</span></span> <span data-ttu-id="b62a5-105">Hay varias ubicaciones en las que las propiedades se muestran de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="b62a5-105">There are various locations where properties are displayed in a read-only manner.</span></span> <span data-ttu-id="b62a5-106">Por otro lado, la edición de propiedades solo está habilitada en el **cuadro de diálogo** Propiedades.</span><span class="sxs-lookup"><span data-stu-id="b62a5-106">Property editing, on the other hand, is enabled only in the **Properties** dialog box.</span></span> <span data-ttu-id="b62a5-107">Ese cuadro de diálogo se puede invocar mediante el vínculo **Editar** propiedades en el **panel** vista previa o el menú contextual de un elemento.</span><span class="sxs-lookup"><span data-stu-id="b62a5-107">That dialog box can be invoked through either the **Edit Properties** link in the **Preview Pane** or the shortcut menu of an item.</span></span>

<span data-ttu-id="b62a5-108">Las listas de propiedades son cadenas delimitadas por punto y coma que tienen el formato siguiente.</span><span class="sxs-lookup"><span data-stu-id="b62a5-108">The property lists are semi-colon delimited strings that have the following form.</span></span>


```
Prop:[flags]PropertyCanonicalName;[flags]PropertyCanonicalName;
```



<span data-ttu-id="b62a5-109">La única marca disponible actualmente se muestra en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="b62a5-109">The only flag currently available is shown in the following table.</span></span>



| <span data-ttu-id="b62a5-110">Marca</span><span class="sxs-lookup"><span data-stu-id="b62a5-110">Flag</span></span> | <span data-ttu-id="b62a5-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="b62a5-111">Description</span></span>                                                                                                                                                                                   |
|------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \*   | <span data-ttu-id="b62a5-112">No muestre la propiedad en el panel **vista** previa como se indica en el valor de clave del Registro **PreviewDetails.**</span><span class="sxs-lookup"><span data-stu-id="b62a5-112">Do not show the property in the **Preview Pane** as instructed in the **PreviewDetails** registry key value.</span></span> <span data-ttu-id="b62a5-113">Vea el ejemplo que sigue a la tabla siguiente si no se establece el valor de esa propiedad.</span><span class="sxs-lookup"><span data-stu-id="b62a5-113">See the example that follows the next table if that property's value is not set.</span></span> |



 

<span data-ttu-id="b62a5-114">Después de definir una lista de propiedades, puede almacenar esa cadena en el Registro a través del sistema de asociación de archivos de [Shell](../shell/fa-file-types.md) estándar en **HKEY \_ CLASSES \_ ROOT.**</span><span class="sxs-lookup"><span data-stu-id="b62a5-114">After you define a property list, you can store that string in the registry through the standard [Shell file association](../shell/fa-file-types.md) system under **HKEY\_CLASSES\_ROOT.**</span></span> <span data-ttu-id="b62a5-115">En la tabla siguiente se resumen los valores de las listas de propiedades que se pueden asignar en la clave del Registro para una extensión de nombre de archivo determinada.</span><span class="sxs-lookup"><span data-stu-id="b62a5-115">The following table summarizes the values for the property lists that can be assigned under the registry key for a particular file name extension.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b62a5-116">Value</span><span class="sxs-lookup"><span data-stu-id="b62a5-116">Value</span></span></th>
<th><span data-ttu-id="b62a5-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="b62a5-117">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b62a5-118">FullDetails</span><span class="sxs-lookup"><span data-stu-id="b62a5-118">FullDetails</span></span></td>
<td><span data-ttu-id="b62a5-119">Las propiedades se muestran en la <strong>pestaña Detalles</strong> del cuadro <strong>de diálogo</strong> Propiedades .</span><span class="sxs-lookup"><span data-stu-id="b62a5-119">Properties are displayed on the <strong>Details</strong> tab of the <strong>Properties</strong> dialog box.</span></span> <span data-ttu-id="b62a5-120">Esta es la lista completa de propiedades que admite el tipo de archivo.</span><span class="sxs-lookup"><span data-stu-id="b62a5-120">This is the complete list of properties that the file type supports.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b62a5-121">PreviewDetails</span><span class="sxs-lookup"><span data-stu-id="b62a5-121">PreviewDetails</span></span></td>
<td><span data-ttu-id="b62a5-122">Las propiedades se muestran en el panel <strong>vista previa</strong>.</span><span class="sxs-lookup"><span data-stu-id="b62a5-122">Properties are displayed in the <strong>Preview Pane</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b62a5-123">PreviewTitle</span><span class="sxs-lookup"><span data-stu-id="b62a5-123">PreviewTitle</span></span></td>
<td><span data-ttu-id="b62a5-124">Las propiedades se muestran en el área de título del panel <strong>vista previa</strong> junto a la miniatura del elemento.</span><span class="sxs-lookup"><span data-stu-id="b62a5-124">Properties are displayed in the title area of the <strong>Preview Pane</strong> next to the thumbnail for the item.</span></span> <span data-ttu-id="b62a5-125">El número máximo de entradas es 3.</span><span class="sxs-lookup"><span data-stu-id="b62a5-125">The maximum number of entries is 3.</span></span> <span data-ttu-id="b62a5-126">Si la lista de propiedades contiene más del número máximo permitido, se omiten el resto de las entradas.</span><span class="sxs-lookup"><span data-stu-id="b62a5-126">If the property list contains more than the maximum allowable number, the rest of the entries are ignored.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b62a5-127">TileInfo</span><span class="sxs-lookup"><span data-stu-id="b62a5-127">TileInfo</span></span></td>
<td><span data-ttu-id="b62a5-128">Las propiedades se muestran cuando la vista de lista está en <strong>modo de vista</strong> Iconos.</span><span class="sxs-lookup"><span data-stu-id="b62a5-128">Properties are displayed when the list view is in <strong>Tiles</strong> view mode.</span></span> <span data-ttu-id="b62a5-129">El número máximo de entradas es 3.</span><span class="sxs-lookup"><span data-stu-id="b62a5-129">The maximum number of entries is 3.</span></span> <span data-ttu-id="b62a5-130">Si la lista de propiedades contiene más del número máximo permitido, se omiten el resto de las entradas.</span><span class="sxs-lookup"><span data-stu-id="b62a5-130">If the property list contains more than the maximum allowable number, the rest of the entries are ignored.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="b62a5-131">Este valor estaba presente en Windows XP.</span><span class="sxs-lookup"><span data-stu-id="b62a5-131">This value was present in Windows XP.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b62a5-132">ExtendedTileInfo</span><span class="sxs-lookup"><span data-stu-id="b62a5-132">ExtendedTileInfo</span></span></td>
<td><span data-ttu-id="b62a5-133">Las propiedades se muestran para un elemento cuando la vista de lista está en modo <strong>de vista icono</strong> extendido.</span><span class="sxs-lookup"><span data-stu-id="b62a5-133">Properties are displayed for an item when the list view is in <strong>Extended Tile</strong> view mode.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b62a5-134">InfoTip</span><span class="sxs-lookup"><span data-stu-id="b62a5-134">InfoTip</span></span></td>
<td><span data-ttu-id="b62a5-135">Las propiedades se muestran en una información general cuando un usuario mantiene el puntero sobre un elemento.</span><span class="sxs-lookup"><span data-stu-id="b62a5-135">Properties are displayed in an infotip when a user hovers over an item.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="b62a5-136">Este valor estaba presente en Windows XP.</span><span class="sxs-lookup"><span data-stu-id="b62a5-136">This value was present in Windows XP.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b62a5-137">Información rápida</span><span class="sxs-lookup"><span data-stu-id="b62a5-137">QuickTip</span></span></td>
<td><span data-ttu-id="b62a5-138">Las propiedades se muestran cuando es difícil recuperar propiedades directamente desde un elemento, por ejemplo, cuando se debe tener acceso al elemento a través de una conexión de red lenta.</span><span class="sxs-lookup"><span data-stu-id="b62a5-138">Properties are displayed when it is difficult to retrieve properties directly from an item, such as when the item must be accessed over a slow network connection.</span></span> <span data-ttu-id="b62a5-139">Se recomienda que las propiedades denominadas aquí, como Tipo o Tamaño, no requieran abrir la secuencia de archivos para determinar su valor.</span><span class="sxs-lookup"><span data-stu-id="b62a5-139">It is recommended that the properties named here, such as Type or Size, do not require opening the file stream to determine their value.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="b62a5-140">Este valor estaba presente en Windows XP.</span><span class="sxs-lookup"><span data-stu-id="b62a5-140">This value was present in Windows XP.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="b62a5-141">En el ejemplo siguiente se define el valor PreviewDetails para un tipo de archivo .recipe, mediante un ProgID de **RecipeKey**.</span><span class="sxs-lookup"><span data-stu-id="b62a5-141">The example below defines the PreviewDetails value for a .recipe file type, using a ProgID of **RecipeKey**.</span></span>

```
HKEY_CLASSES_ROOT
   .recipe
      (Default) = Recipe File
   RecipeFile
      PreviewDetails = prop:*System.Title;*System.Author
```

<span data-ttu-id="b62a5-142">Como se explica en el tema [Asociación de archivos de Shell,](../shell/fa-file-types.md) las asociaciones de archivos se pueden describir para el formato más específico de la forma más general.</span><span class="sxs-lookup"><span data-stu-id="b62a5-142">As explained in the [Shell file association](../shell/fa-file-types.md) topic, file associations can be described for the most specific to the most general form.</span></span> <span data-ttu-id="b62a5-143">El formulario más específico es la extensión de nombre de archivo único y el formulario más genérico es una clave que se aplica a todos los archivos y carpetas de archivos.</span><span class="sxs-lookup"><span data-stu-id="b62a5-143">The most specific form is the single file name extension and the most generic form is a key that applies to all files and file folders.</span></span> <span data-ttu-id="b62a5-144">Entre esos dos extremos, también puede definir un [PROGID](../shell/fa-progids.md) que agrupa un conjunto de extensiones de nombre de archivo (por ejemplo, los tipos .jpg y .jpeg agrupados como **jpegfile).**</span><span class="sxs-lookup"><span data-stu-id="b62a5-144">Between those two extremes, you can also define a [PROGID](../shell/fa-progids.md) that groups a set of file name extensions together (for instance, .jpg and .jpeg types grouped as **jpegfile**).</span></span> <span data-ttu-id="b62a5-145">Al definir listas de propiedades, debe definirlas para ProgID o, en algunos casos, extensiones de nombre de archivo específicas.</span><span class="sxs-lookup"><span data-stu-id="b62a5-145">When you define property lists, you should define them for ProgIDs or, in some cases, specific file name extensions.</span></span> <span data-ttu-id="b62a5-146">Evite confiar en entradas amplias, como la **clave AllFileSystemObjects.**</span><span class="sxs-lookup"><span data-stu-id="b62a5-146">Avoid relying on broad entries such as the **AllFileSystemObjects** key.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b62a5-147">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b62a5-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b62a5-148">Descripción de los controladores de propiedades</span><span class="sxs-lookup"><span data-stu-id="b62a5-148">Understanding Property Handlers</span></span>](./building-property-handlers-properties.md)
</dt> <dt>

[<span data-ttu-id="b62a5-149">Usar nombres de tipo</span><span class="sxs-lookup"><span data-stu-id="b62a5-149">Using Kind Names</span></span>](./building-property-handlers-user-friendly-kind-names.md)
</dt> <dt>

[<span data-ttu-id="b62a5-150">Inicialización de controladores de propiedades</span><span class="sxs-lookup"><span data-stu-id="b62a5-150">Initializing Property Handlers</span></span>](./building-property-handlers-property-handlers.md)
</dt> <dt>

[<span data-ttu-id="b62a5-151">Registro y distribución de controladores de propiedades</span><span class="sxs-lookup"><span data-stu-id="b62a5-151">Registering and Distributing Property Handlers</span></span>](./prophand-reg-dist.md)
</dt> <dt>

[<span data-ttu-id="b62a5-152">Procedimientos recomendados y preguntas más frecuentes sobre el controlador de propiedades</span><span class="sxs-lookup"><span data-stu-id="b62a5-152">Property Handler Best Practices and FAQ</span></span>](./prophand-bestprac-faq.yml)
</dt> </dl>

 

 
