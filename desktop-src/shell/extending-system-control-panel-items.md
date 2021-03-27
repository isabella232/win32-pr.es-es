---
description: Algunos de los elementos del sistema que se encuentran en el panel de control son extensibles. Para instalar una extensión del panel de control, registre la extensión de shell como se indica a continuación, donde nombre es el nombre predefinido del elemento del sistema (vea la tabla siguiente).
title: Extender elementos del panel de control del sistema
ms.topic: article
ms.date: 05/31/2018
ms.assetid: b8b18b71-c95f-4c71-8df4-fe9342ce0165
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 9b0f6628d7bc75378915c1d9f3e20327478742df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997301"
---
# <a name="extending-system-control-panel-items"></a><span data-ttu-id="fea10-104">Extender elementos del panel de control del sistema</span><span class="sxs-lookup"><span data-stu-id="fea10-104">Extending System Control Panel Items</span></span>

<span data-ttu-id="fea10-105">Algunos de los elementos del sistema que se encuentran en el panel de control son extensibles.</span><span class="sxs-lookup"><span data-stu-id="fea10-105">Some of the system items found in the Control Panel are extensible.</span></span> <span data-ttu-id="fea10-106">Para instalar una extensión del panel de control, registre la extensión de shell como se indica a continuación, donde *nombre* es el nombre predefinido del elemento del sistema (vea la tabla siguiente).</span><span class="sxs-lookup"><span data-stu-id="fea10-106">To install a Control Panel extension, register your Shell extension as follows, where *name* is the predefined name of the system item (see table below).</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Controls Folder
                  name
                     shellex
                        PropertySheetHandlers
```

<span data-ttu-id="fea10-107">Esto es similar a la manera en que registraría una extensión para un objeto de Shell predefinido.</span><span class="sxs-lookup"><span data-stu-id="fea10-107">This is similar to the way you would register an extension for a predefined Shell object.</span></span> <span data-ttu-id="fea10-108">Dado que las únicas extensiones de Shell que admiten los elementos del panel de control son hojas de propiedades, el registro debe estar bajo la subclave **shellex** \\ **PropertySheetHandlers** .</span><span class="sxs-lookup"><span data-stu-id="fea10-108">Because the only Shell extensions supported by Control Panel items are property sheets, the registration must be under the **shellex**\\**PropertySheetHandlers** subkey.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="fea10-109">Elemento del panel de control</span><span class="sxs-lookup"><span data-stu-id="fea10-109">Control Panel item</span></span></th>
<th><span data-ttu-id="fea10-110"><em>name</em></span><span class="sxs-lookup"><span data-stu-id="fea10-110"><em>name</em></span></span></th>
<th><span data-ttu-id="fea10-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fea10-111">Remarks</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="fea10-112">Pantalla</span><span class="sxs-lookup"><span data-stu-id="fea10-112">Display</span></span></td>
<td><span data-ttu-id="fea10-113">Desk (Escritorio)</span><span class="sxs-lookup"><span data-stu-id="fea10-113">Desk</span></span></td>
<td><span data-ttu-id="fea10-114">También admite el reemplazo de la página del <strong>escritorio</strong> .</span><span class="sxs-lookup"><span data-stu-id="fea10-114">Also supports replacement of the <strong>Desktop</strong> page.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="fea10-115">Ya no se admite en Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="fea10-115">This is no longer supported under Windows Vista.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fea10-116">Configuración de pantalla avanzada</span><span class="sxs-lookup"><span data-stu-id="fea10-116">Display Settings Advanced</span></span></td>
<td><span data-ttu-id="fea10-117">Dispositivo</span><span class="sxs-lookup"><span data-stu-id="fea10-117">Device</span></span></td>
<td><span data-ttu-id="fea10-118">Propiedades avanzadas no específicas del hardware.</span><span class="sxs-lookup"><span data-stu-id="fea10-118">Nonhardware-specific advanced properties.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="fea10-119">Ya no se admite en Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="fea10-119">This is no longer supported under Windows Vista.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fea10-120">Configuración de pantalla avanzada</span><span class="sxs-lookup"><span data-stu-id="fea10-120">Display Settings Advanced</span></span></td>
<td><span data-ttu-id="fea10-121">Pantalla</span><span class="sxs-lookup"><span data-stu-id="fea10-121">Display</span></span></td>
<td><span data-ttu-id="fea10-122">Propiedades avanzadas específicas del hardware.</span><span class="sxs-lookup"><span data-stu-id="fea10-122">Hardware-specific advanced properties.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="fea10-123">Ya no se admite en Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="fea10-123">This is no longer supported under Windows Vista.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fea10-124">Opciones de Internet</span><span class="sxs-lookup"><span data-stu-id="fea10-124">Internet Options</span></span></td>
<td><span data-ttu-id="fea10-125">Internet</span><span class="sxs-lookup"><span data-stu-id="fea10-125">Internet</span></span></td>
<td><span data-ttu-id="fea10-126">El número máximo de páginas de extensión es 18.</span><span class="sxs-lookup"><span data-stu-id="fea10-126">The maximum number of extension pages is 18.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fea10-127">Teclado</span><span class="sxs-lookup"><span data-stu-id="fea10-127">Keyboard</span></span></td>
<td><span data-ttu-id="fea10-128">Teclado</span><span class="sxs-lookup"><span data-stu-id="fea10-128">Keyboard</span></span></td>
<td><span data-ttu-id="fea10-129">El número máximo de páginas de extensión es 30.</span><span class="sxs-lookup"><span data-stu-id="fea10-129">The maximum number of extension pages is 30.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fea10-130">Mouse</span><span class="sxs-lookup"><span data-stu-id="fea10-130">Mouse</span></span></td>
<td><span data-ttu-id="fea10-131">Mouse</span><span class="sxs-lookup"><span data-stu-id="fea10-131">Mouse</span></span></td>
<td><span data-ttu-id="fea10-132">También admite la sustitución de páginas estándar.</span><span class="sxs-lookup"><span data-stu-id="fea10-132">Also supports replacement of standard pages.</span></span> <span data-ttu-id="fea10-133">El número máximo de páginas de extensión es 8.</span><span class="sxs-lookup"><span data-stu-id="fea10-133">The maximum number of extension pages is 8.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fea10-134">Opciones de energía</span><span class="sxs-lookup"><span data-stu-id="fea10-134">Power Options</span></span></td>
<td><span data-ttu-id="fea10-135">Power</span><span class="sxs-lookup"><span data-stu-id="fea10-135">Power</span></span></td>
<td><span data-ttu-id="fea10-136">El número máximo de páginas, incluidas las páginas estándar, es 18.</span><span class="sxs-lookup"><span data-stu-id="fea10-136">The maximum number of pages, including standard pages, is 18.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fea10-137">Sistema</span><span class="sxs-lookup"><span data-stu-id="fea10-137">System</span></span></td>
<td><span data-ttu-id="fea10-138">Sistema</span><span class="sxs-lookup"><span data-stu-id="fea10-138">System</span></span></td>
<td><span data-ttu-id="fea10-139">El número máximo de páginas de extensión es 8.</span><span class="sxs-lookup"><span data-stu-id="fea10-139">The maximum number of extension pages is 8.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="fea10-140">Ya no se admite en Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="fea10-140">This is no longer supported under Windows Vista.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="fea10-141">El elemento **Agregar o quitar programas** del panel de control de Windows XP no es una hoja de propiedades y, por tanto, no se puede ampliar con los métodos descritos aquí.</span><span class="sxs-lookup"><span data-stu-id="fea10-141">The **Add or Remove Programs** item in the Windows XP Control Panel is not a property sheet and therefore cannot be extended by the methods discussed here.</span></span> <span data-ttu-id="fea10-142">En su lugar, su contenido se obtiene de los publicadores de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="fea10-142">Instead, its content is obtained from application publishers.</span></span> <span data-ttu-id="fea10-143">Para obtener más información sobre cómo agregar contenido para **Agregar o quitar programas**, consulte [**IAppPublisher**](/windows/desktop/api/Shappmgr/nn-shappmgr-iapppublisher), [**IEnumPublishedApps**](/windows/desktop/api/Shappmgr/nn-shappmgr-ienumpublishedapps)y [**IPublishedApp**](/windows/desktop/api/Shappmgr/nn-shappmgr-ipublishedapp).</span><span class="sxs-lookup"><span data-stu-id="fea10-143">For more information on adding content to **Add or Remove Programs**, see [**IAppPublisher**](/windows/desktop/api/Shappmgr/nn-shappmgr-iapppublisher), [**IEnumPublishedApps**](/windows/desktop/api/Shappmgr/nn-shappmgr-ienumpublishedapps), and [**IPublishedApp**](/windows/desktop/api/Shappmgr/nn-shappmgr-ipublishedapp).</span></span>

## <a name="related-topics"></a><span data-ttu-id="fea10-144">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="fea10-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fea10-145">Elementos del panel de control</span><span class="sxs-lookup"><span data-stu-id="fea10-145">Control Panel Items</span></span>](control-panel-applications.md)
</dt> <dt>

[<span data-ttu-id="fea10-146">Directrices de la experiencia de usuario</span><span class="sxs-lookup"><span data-stu-id="fea10-146">User Experience Guidelines</span></span>](user-experience-guidelines.md)
</dt> <dt>

[<span data-ttu-id="fea10-147">Registrar elementos del panel de control</span><span class="sxs-lookup"><span data-stu-id="fea10-147">Registering Control Panel Items</span></span>](registering-control-panel-items.md)
</dt> <dt>

[<span data-ttu-id="fea10-148">Usar CPLApplet</span><span class="sxs-lookup"><span data-stu-id="fea10-148">Using CPLApplet</span></span>](using-cplapplet.md)
</dt> <dt>

[<span data-ttu-id="fea10-149">Procesamiento de mensajes del panel de control</span><span class="sxs-lookup"><span data-stu-id="fea10-149">Control Panel Message Processing</span></span>](message-processing.md)
</dt> <dt>

[<span data-ttu-id="fea10-150">Ejecutar elementos del panel de control</span><span class="sxs-lookup"><span data-stu-id="fea10-150">Executing Control Panel Items</span></span>](executing-control-panel-items.md)
</dt> <dt>

[<span data-ttu-id="fea10-151">Asignar categorías del panel de control</span><span class="sxs-lookup"><span data-stu-id="fea10-151">Assigning Control Panel Categories</span></span>](assigning-control-panel-categories.md)
</dt> <dt>

[<span data-ttu-id="fea10-152">Crear vínculos de tarea que se pueden buscar para un elemento del panel de control</span><span class="sxs-lookup"><span data-stu-id="fea10-152">Creating Searchable Task Links for a Control Panel Item</span></span>](creating-searchable-task-links.md)
</dt> <dt>

[<span data-ttu-id="fea10-153">Acceder al panel de control en modo seguro en Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fea10-153">Accessing the Control Panel in Safe Mode under Windows Vista</span></span>](accessing-the-cp-in-safe-mode-under-vista.md)
</dt> </dl>

 

 




