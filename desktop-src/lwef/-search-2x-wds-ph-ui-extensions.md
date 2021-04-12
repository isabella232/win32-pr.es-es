---
title: Agregar iconos y menús contextuales con extensiones de Shell
description: Puede mejorar la experiencia de los usuarios con la búsqueda de escritorio de Microsoft Windows (WDS) y el controlador de protocolo mediante la implementación de extensiones de Shell.
ms.assetid: 899f3fd1-1ae9-45fe-ae6d-26d4f07bf6e4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adbd6b0f4c647c47e11d14aea5e5af748a59ba53
ms.sourcegitcommit: b9a94cea8f83153214af4c09509e1cc61a1bb616
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/19/2020
ms.locfileid: "104270763"
---
# <a name="adding-icons-and-context-menus-with-shell-extensions"></a><span data-ttu-id="c790d-103">Agregar iconos y menús contextuales con extensiones de Shell</span><span class="sxs-lookup"><span data-stu-id="c790d-103">Adding Icons and Context Menus with Shell Extensions</span></span>

> [!NOTE]
> <span data-ttu-id="c790d-104">Windows Desktop Search 2. x es una tecnología obsoleta que estaba disponible originalmente como complemento para Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="c790d-104">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="c790d-105">En versiones posteriores, use la [búsqueda de Windows](../search/-search-3x-wds-overview.md) en su lugar.</span><span class="sxs-lookup"><span data-stu-id="c790d-105">On later releases, use [Windows Search](../search/-search-3x-wds-overview.md) instead.</span></span>

<span data-ttu-id="c790d-106">Puede mejorar la experiencia de los usuarios con la búsqueda de escritorio de Microsoft Windows (WDS) y el controlador de protocolo mediante la implementación de extensiones de Shell.</span><span class="sxs-lookup"><span data-stu-id="c790d-106">You can improve your users' experience with Microsoft Windows Desktop Search (WDS) and your protocol handler by implementing Shell extensions.</span></span> <span data-ttu-id="c790d-107">Sin extensión adicional, el controlador de protocolo que cree no incluirá las siguientes experiencias de usuario:</span><span class="sxs-lookup"><span data-stu-id="c790d-107">Without further extension, the protocol handler you create will not include the following user experiences:</span></span>

-   <span data-ttu-id="c790d-108">WDS no mostrará iconos específicos para los resultados.</span><span class="sxs-lookup"><span data-stu-id="c790d-108">WDS will not display specific icons for your results.</span></span>
-   <span data-ttu-id="c790d-109">Cuando los usuarios hacen doble clic en un elemento, la interfaz de usuario no responderá al evento.</span><span class="sxs-lookup"><span data-stu-id="c790d-109">When users double-click an item, the user interface will not respond to the event.</span></span>
-   <span data-ttu-id="c790d-110">Cuando los usuarios hacen clic con el botón secundario en un elemento, el menú contextual no será compatible con las operaciones del elemento.</span><span class="sxs-lookup"><span data-stu-id="c790d-110">When users right-click an item, the context menu will not support any operations for the item.</span></span>

<span data-ttu-id="c790d-111">Las implementaciones mínimas de **IPersist** y **IPersistFolder** son necesarias para **IShellFolder**, y se requiere una implementación mínima de **IShellFolder** para **IContextMenu** y **IExtractIcon**, las dos interfaces que proporcionan una experiencia de usuario más sencilla.</span><span class="sxs-lookup"><span data-stu-id="c790d-111">Minimal implementations of **IPersist** and **IPersistFolder** are required by **IShellFolder**, and a minimal implementation of **IShellFolder** is required for **IContextMenu** and **IExtractIcon**, the two interfaces that provide a more seamless user experience.</span></span>

 

## <a name="ipersist"></a><span data-ttu-id="c790d-112">IPersist</span><span class="sxs-lookup"><span data-stu-id="c790d-112">IPersist</span></span>

<span data-ttu-id="c790d-113">La interfaz **IPersist** define el único método **GetClassID**, que está diseñado para proporcionar el CLSID de un objeto que se puede almacenar de forma persistente en el sistema.</span><span class="sxs-lookup"><span data-stu-id="c790d-113">The **IPersist** interface defines the single method **GetClassID**, which is designed to supply the CLSID of an object that can be stored persistently in the system.</span></span>



| <span data-ttu-id="c790d-114">Método</span><span class="sxs-lookup"><span data-stu-id="c790d-114">Method</span></span>       | <span data-ttu-id="c790d-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="c790d-115">Description</span></span>                                 |
|--------------|---------------------------------------------|
| <span data-ttu-id="c790d-116">GetClassID ()</span><span class="sxs-lookup"><span data-stu-id="c790d-116">GetClassID()</span></span> | <span data-ttu-id="c790d-117">Devuelve el ClassID del controlador de protocolo.</span><span class="sxs-lookup"><span data-stu-id="c790d-117">Returns the ClassID of the protocol handler</span></span> |



 

> [!Note]
>
> <span data-ttu-id="c790d-118">Se debe implementar el mismo CLSID para **IPersist**, **IPersistFolder** y **IShellFolder**.</span><span class="sxs-lookup"><span data-stu-id="c790d-118">The same CLSID should be implemented for **IPersist**, **IPersistFolder** and **IShellFolder**.</span></span>

 

 

## <a name="ipersistfolder"></a><span data-ttu-id="c790d-119">IPersistFolder</span><span class="sxs-lookup"><span data-stu-id="c790d-119">IPersistFolder</span></span>

<span data-ttu-id="c790d-120">La interfaz **IPersistFolder** se usa para inicializar los objetos de la carpeta de Shell.</span><span class="sxs-lookup"><span data-stu-id="c790d-120">The **IPersistFolder** interface is used to initialize Shell folder objects.</span></span> <span data-ttu-id="c790d-121">La implementación de esta interfaz, que se deriva de **IPersist**, es cómo se indica a la carpeta dónde se encuentra en el espacio de nombres del shell.</span><span class="sxs-lookup"><span data-stu-id="c790d-121">Implementation of this interface, which is derived from **IPersist**, is how the folder is told where it is in the Shell namespace.</span></span>



| <span data-ttu-id="c790d-122">Método</span><span class="sxs-lookup"><span data-stu-id="c790d-122">Method</span></span>       | <span data-ttu-id="c790d-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="c790d-123">Description</span></span>                                                                                            |
|--------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c790d-124">Initialize ()</span><span class="sxs-lookup"><span data-stu-id="c790d-124">Initialize()</span></span> | <span data-ttu-id="c790d-125">Indica a un objeto de carpeta de Shell que se inicialice a sí mismo basándose en la información que se pasa y devuelve S \_ correctos.</span><span class="sxs-lookup"><span data-stu-id="c790d-125">Instructs a Shell folder object to initialize itself based on the information passed and returns S\_OK</span></span> |



 

> [!Note]
>
> <span data-ttu-id="c790d-126">Se debe implementar el mismo CLSID para **IPersist**, **IPersistFolder** y **IShellFolder**.</span><span class="sxs-lookup"><span data-stu-id="c790d-126">The same CLSID should be implemented for **IPersist**, **IPersistFolder** and **IShellFolder**.</span></span>

 

<span data-ttu-id="c790d-127">No utilice esta interfaz directamente.</span><span class="sxs-lookup"><span data-stu-id="c790d-127">You do not use this interface directly.</span></span> <span data-ttu-id="c790d-128">Lo usa la implementación del sistema de archivos de la interfaz IShellFolder:: BindToObject cuando Inicializa un objeto de carpeta de Shell.</span><span class="sxs-lookup"><span data-stu-id="c790d-128">It is used by the file system implementation of the IShellFolder::BindToObject interface when it initializes a Shell folder object.</span></span>

 

## <a name="ishellfolder"></a><span data-ttu-id="c790d-129">IShellFolder</span><span class="sxs-lookup"><span data-stu-id="c790d-129">IShellFolder</span></span>

<span data-ttu-id="c790d-130">La interfaz **IShellFolder** se usa para administrar carpetas y se requiere una implementación parcial para que las interfaces de icono y de contexto implementadas para un controlador de protocolo se comporten correctamente en la interfaz de usuario de los resultados de búsqueda de escritorio de Windows.</span><span class="sxs-lookup"><span data-stu-id="c790d-130">The **IShellFolder** interface is used to manage folders, and a partial implementation is required so that the icon and context interfaces implemented for a protocol handler will behave correctly in the Windows Desktop Search results user interface.</span></span> <span data-ttu-id="c790d-131">La mayor parte de la funcionalidad requerida se expone a través del método **GetUIObjectOf** .</span><span class="sxs-lookup"><span data-stu-id="c790d-131">Most of the functionality required is exposed through the **GetUIObjectOf** method.</span></span> <span data-ttu-id="c790d-132">Este método permite que un complemento consulte las interfaces **IExtractIcon** y **IContextMenu** .</span><span class="sxs-lookup"><span data-stu-id="c790d-132">This method enables an add-in to query for the **IExtractIcon** and **IContextMenu** interfaces.</span></span>

<span data-ttu-id="c790d-133">La interfaz **IShellFolder** utiliza PIDL en lugar de direcciones URL.</span><span class="sxs-lookup"><span data-stu-id="c790d-133">The **IShellFolder** interface uses PIDLs instead of URLs.</span></span> <span data-ttu-id="c790d-134">A diferencia de los requisitos de una extensión de espacio de nombres completa, los complementos pueden usar una estructura IDL simple que solo contenga la dirección URL.</span><span class="sxs-lookup"><span data-stu-id="c790d-134">In contrast to the requirements of a complete Namespace extension, add-ins can use a simple IDL structure that contains only the URL.</span></span>

<span data-ttu-id="c790d-135">Se deben implementar los siguientes métodos de **IShellFolder** .</span><span class="sxs-lookup"><span data-stu-id="c790d-135">The following methods of **IShellFolder** must be implemented.</span></span> <span data-ttu-id="c790d-136">Tenga en cuenta que cinco de estos métodos requieren una implementación mínima.</span><span class="sxs-lookup"><span data-stu-id="c790d-136">Note that five of these methods require minimal implementation.</span></span>



| <span data-ttu-id="c790d-137">Método</span><span class="sxs-lookup"><span data-stu-id="c790d-137">Method</span></span>             | <span data-ttu-id="c790d-138">Descripción</span><span class="sxs-lookup"><span data-stu-id="c790d-138">Description</span></span>                                                                                                                                                                                                 |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c790d-139">BindToObject()</span><span class="sxs-lookup"><span data-stu-id="c790d-139">BindToObject()</span></span>     | <span data-ttu-id="c790d-140">Devuelve E \_ NOTIMPL</span><span class="sxs-lookup"><span data-stu-id="c790d-140">Returns E\_NOTIMPL</span></span>                                                                                                                                                                                          |
| <span data-ttu-id="c790d-141">BindToStorage()</span><span class="sxs-lookup"><span data-stu-id="c790d-141">BindToStorage()</span></span>    | <span data-ttu-id="c790d-142">Devuelve E \_ NOTIMPL</span><span class="sxs-lookup"><span data-stu-id="c790d-142">Returns E\_NOTIMPL</span></span>                                                                                                                                                                                          |
| <span data-ttu-id="c790d-143">CreateViewObject()</span><span class="sxs-lookup"><span data-stu-id="c790d-143">CreateViewObject()</span></span> | <span data-ttu-id="c790d-144">Devuelve E \_ NOTIMPL</span><span class="sxs-lookup"><span data-stu-id="c790d-144">Returns E\_NOTIMPL</span></span>                                                                                                                                                                                          |
| <span data-ttu-id="c790d-145">SetNameOf()</span><span class="sxs-lookup"><span data-stu-id="c790d-145">SetNameOf()</span></span>        | <span data-ttu-id="c790d-146">Devuelve E \_ NOTIMPL</span><span class="sxs-lookup"><span data-stu-id="c790d-146">Returns E\_NOTIMPL</span></span>                                                                                                                                                                                          |
| <span data-ttu-id="c790d-147">ParseDisplayName()</span><span class="sxs-lookup"><span data-stu-id="c790d-147">ParseDisplayName()</span></span> | <span data-ttu-id="c790d-148">Convierte una dirección URL en la estructura PIDL</span><span class="sxs-lookup"><span data-stu-id="c790d-148">Converts a URL to the PIDL structure</span></span>                                                                                                                                                                        |
| <span data-ttu-id="c790d-149">CompareIDs()</span><span class="sxs-lookup"><span data-stu-id="c790d-149">CompareIDs()</span></span>       | <span data-ttu-id="c790d-150">Compara dos valores de PIDL</span><span class="sxs-lookup"><span data-stu-id="c790d-150">Compares two PIDL values</span></span>                                                                                                                                                                                    |
| <span data-ttu-id="c790d-151">GetDisplayNameOf()</span><span class="sxs-lookup"><span data-stu-id="c790d-151">GetDisplayNameOf()</span></span> | <span data-ttu-id="c790d-152">Devuelve la dirección URL de un PIDL</span><span class="sxs-lookup"><span data-stu-id="c790d-152">Returns the URL for a PIDL</span></span>                                                                                                                                                                                  |
| <span data-ttu-id="c790d-153">GetUIObjectOf()</span><span class="sxs-lookup"><span data-stu-id="c790d-153">GetUIObjectOf()</span></span>    | <span data-ttu-id="c790d-154">Este método es similar al método QueryInterface de OLE COM.</span><span class="sxs-lookup"><span data-stu-id="c790d-154">This method is similar to the OLE COM QueryInterface method.</span></span> <span data-ttu-id="c790d-155">Si se solicita un icono, el autor de la llamada solicita el IID \_ IExtractIcon; si se solicita un menú contextual, el autor de la llamada solicita el IID \_ IContextMenu.</span><span class="sxs-lookup"><span data-stu-id="c790d-155">If an icon is requested, the caller requests the IID\_IExtractIcon; if a context menu is requested, the caller requests the IID\_IContextMenu.</span></span> |



 

> [!Note]
>
> <span data-ttu-id="c790d-156">Se debe implementar el mismo CLSID para **IPersist**, **IPersistFolder** y **IShellFolder**.</span><span class="sxs-lookup"><span data-stu-id="c790d-156">The same CLSID should be implemented for **IPersist**, **IPersistFolder** and **IShellFolder**.</span></span>

 

<span data-ttu-id="c790d-157">**IShellFolder** no se utiliza para enumerar carpetas.</span><span class="sxs-lookup"><span data-stu-id="c790d-157">**IShellFolder** is not used to enumerate folders.</span></span> <span data-ttu-id="c790d-158">Esto significa que el nombre para mostrar de una carpeta será la dirección URL física.</span><span class="sxs-lookup"><span data-stu-id="c790d-158">This means that the display name of a folder will be the physical URL.</span></span> <span data-ttu-id="c790d-159">Esto puede cambiar en el futuro.</span><span class="sxs-lookup"><span data-stu-id="c790d-159">This may change in the future.</span></span>

 

## <a name="icontextmenu"></a><span data-ttu-id="c790d-160">IContextMenu</span><span class="sxs-lookup"><span data-stu-id="c790d-160">IContextMenu</span></span>

<span data-ttu-id="c790d-161">Cuando WDS muestra los resultados al usuario, puede hacer clic con el botón secundario en un elemento y ver un menú contextual definido por la interfaz **IContextMenu** .</span><span class="sxs-lookup"><span data-stu-id="c790d-161">When WDS displays results to the user, the user can right-click an item and see a context menu defined by your **IContextMenu** interface.</span></span>

<span data-ttu-id="c790d-162">La acción predeterminada en el menú contextual es la misma acción que se realiza cuando se hace doble clic en el elemento.</span><span class="sxs-lookup"><span data-stu-id="c790d-162">The default action on the context menu is the same action taken when the item is double-clicked.</span></span> <span data-ttu-id="c790d-163">Sin las interfaces de **IShellFolder** o **IContextMenu** correspondientes para el elemento, el comportamiento predeterminado para un evento de doble clic es pasar la dirección URL como un argumento a la función ShellExecute.</span><span class="sxs-lookup"><span data-stu-id="c790d-163">Without the corresponding **IShellFolder** or **IContextMenu** interfaces for the item, the default behavior for a double-click event is to pass the URL as an argument to the ShellExecute function.</span></span>

 

## <a name="iextracticon"></a><span data-ttu-id="c790d-164">IExtractIcon</span><span class="sxs-lookup"><span data-stu-id="c790d-164">IExtractIcon</span></span>

<span data-ttu-id="c790d-165">**IExtractIcon** recupera un icono para la interfaz de usuario de WDS basado en la dirección URL en el PIDL proporcionado por el controlador de protocolo.</span><span class="sxs-lookup"><span data-stu-id="c790d-165">**IExtractIcon** retrieves an icon for the WDS user interface based on the URL in the PIDL provided by your protocol handler.</span></span>

 

## <a name="code-sample"></a><span data-ttu-id="c790d-166">Ejemplo de código</span><span class="sxs-lookup"><span data-stu-id="c790d-166">Code Sample</span></span>

<span data-ttu-id="c790d-167">En el código de ejemplo de la [interfaz de usuario del controlador de protocolo personalizado](-search-2x-wds-ph-ui-samplecode.md) se muestra una implementación de **IShellFolder** y las interfaces auxiliares, e incluye compatibilidad para manipular el PIDL.</span><span class="sxs-lookup"><span data-stu-id="c790d-167">The [Custom Protocol Handler User Interface Sample Code](-search-2x-wds-ph-ui-samplecode.md) demonstrates an implementation of **IShellFolder** and supporting interfaces and includes support for manipulating the PIDLs.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c790d-168">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c790d-168">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="c790d-169">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="c790d-169">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="c790d-170">Código de ejemplo de la interfaz de usuario del controlador de protocolo personalizado</span><span class="sxs-lookup"><span data-stu-id="c790d-170">Custom Protocol Handler User Interface Sample Code</span></span>](-search-2x-wds-ph-ui-samplecode.md)
</dt> <dt>

[<span data-ttu-id="c790d-171">Instalar y registrar controladores de protocolo</span><span class="sxs-lookup"><span data-stu-id="c790d-171">Installing and Registering Protocol Handlers</span></span>](-search-2x-wds-ph-install-registration.md)
</dt> </dl>

 

 




