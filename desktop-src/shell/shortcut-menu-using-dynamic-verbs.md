---
description: Los controladores de menús contextuales también se denominan controladores de menú contextual o controladores de verbos. Un controlador de menú contextual es un tipo de controlador de tipo de archivo.
ms.assetid: 7FC65C6F-3798-404c-B359-2BC75D3F54E7
title: Personalización de un menú contextual mediante verbos dinámicos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9b24f035e84f0bde6dccde09f1ed94fefce421b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985751"
---
# <a name="customizing-a-shortcut-menu-using-dynamic-verbs"></a><span data-ttu-id="1229f-104">Personalización de un menú contextual mediante verbos dinámicos</span><span class="sxs-lookup"><span data-stu-id="1229f-104">Customizing a Shortcut Menu Using Dynamic Verbs</span></span>

<span data-ttu-id="1229f-105">Los controladores de menús contextuales también se denominan controladores de menú contextual o controladores de verbos.</span><span class="sxs-lookup"><span data-stu-id="1229f-105">Shortcut menu handlers are also known as context menu handlers or verb handlers.</span></span> <span data-ttu-id="1229f-106">Un controlador de menú contextual es un tipo de controlador de tipo de archivo.</span><span class="sxs-lookup"><span data-stu-id="1229f-106">A shortcut menu handler is a type of file type handler.</span></span>

<span data-ttu-id="1229f-107">Este tema se organiza de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="1229f-107">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="1229f-108">Acerca de los verbos estáticos y dinámicos</span><span class="sxs-lookup"><span data-stu-id="1229f-108">About Static and Dynamic Verbs</span></span>](#about-static-and-dynamic-verbs)
-   [<span data-ttu-id="1229f-109">Cómo funcionan los controladores de menú contextual con verbos dinámicos</span><span class="sxs-lookup"><span data-stu-id="1229f-109">How Shortcut Menu Handlers Work with Dynamic Verbs</span></span>](#how-shortcut-menu-handlers-work-with-dynamic-verbs)
-   [<span data-ttu-id="1229f-110">Evitar colisiones debido a nombres de verbo no completos</span><span class="sxs-lookup"><span data-stu-id="1229f-110">Avoiding Collisions Due to Unqualified Verb Names</span></span>](#avoiding-collisions-due-to-unqualified-verb-names)
-   [<span data-ttu-id="1229f-111">Registrar un controlador de menú contextual con un verbo dinámico</span><span class="sxs-lookup"><span data-stu-id="1229f-111">Registering a Shortcut Menu Handler with a Dynamic Verb</span></span>](#registering-a-shortcut-menu-handler-with-a-dynamic-verb)
-   [<span data-ttu-id="1229f-112">Implementar la interfaz IContextMenu</span><span class="sxs-lookup"><span data-stu-id="1229f-112">Implementing the IContextMenu Interface</span></span>](#implementing-the-icontextmenu-interface)
    -   [<span data-ttu-id="1229f-113">IContextMenu:: GetCommandString (método)</span><span class="sxs-lookup"><span data-stu-id="1229f-113">IContextMenu::GetCommandString Method</span></span>](#icontextmenugetcommandstring-method)
    -   [<span data-ttu-id="1229f-114">IContextMenu:: InvokeCommand (método)</span><span class="sxs-lookup"><span data-stu-id="1229f-114">IContextMenu::InvokeCommand Method</span></span>](#icontextmenuinvokecommand-method)
    -   [<span data-ttu-id="1229f-115">IContextMenu:: QueryContextMenu (método)</span><span class="sxs-lookup"><span data-stu-id="1229f-115">IContextMenu::QueryContextMenu Method</span></span>](#icontextmenuquerycontextmenu-method)
-   [<span data-ttu-id="1229f-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="1229f-116">Related topics</span></span>](#related-topics)

## <a name="about-static-and-dynamic-verbs"></a><span data-ttu-id="1229f-117">Acerca de los verbos estáticos y dinámicos</span><span class="sxs-lookup"><span data-stu-id="1229f-117">About Static and Dynamic Verbs</span></span>

<span data-ttu-id="1229f-118">Le recomendamos encarecidamente que implemente un menú contextual con uno de los métodos estáticos Verb.</span><span class="sxs-lookup"><span data-stu-id="1229f-118">We strongly encourage you to implement a shortcut menu using one of the static verb methods.</span></span> <span data-ttu-id="1229f-119">Se recomienda seguir las instrucciones proporcionadas en la sección "personalizar un menú contextual mediante verbos estáticos" de [creación de controladores de menú contextuales](context-menu-handlers.md).</span><span class="sxs-lookup"><span data-stu-id="1229f-119">We recommend that you follow the instructions provided in the "Customizing a Shortcut Menu using Static Verbs" section of [Creating Context Menu Handlers](context-menu-handlers.md).</span></span> <span data-ttu-id="1229f-120">Para obtener el comportamiento dinámico de los verbos estáticos en Windows 7 y versiones posteriores, vea el tema sobre cómo obtener el comportamiento dinámico para verbos estáticos en [creación de controladores de menú contextuales](context-menu-handlers.md).</span><span class="sxs-lookup"><span data-stu-id="1229f-120">To get dynamic behavior for static verbs in Windows 7 and later, see "Getting Dynamic Behavior for Static Verbs" in [Creating Context Menu Handlers](context-menu-handlers.md).</span></span> <span data-ttu-id="1229f-121">Para obtener información detallada sobre la implementación de verbos estáticos y los verbos dinámicos que se deben evitar, vea [elegir un verbo estático o dinámico para el menú contextual](shortcut-choose-method.md).</span><span class="sxs-lookup"><span data-stu-id="1229f-121">For details on static verb implementation, and which dynamic verbs to avoid, see [Choosing a Static or Dynamic Verb for your Shortcut Menu](shortcut-choose-method.md).</span></span>

<span data-ttu-id="1229f-122">Si debe extender el menú contextual de un tipo de archivo registrando un verbo dinámico para el tipo de archivo, siga las instrucciones que se proporcionan más adelante en este tema.</span><span class="sxs-lookup"><span data-stu-id="1229f-122">If you must extend the shortcut menu for a file type by registering a dynamic verb for the file type, then follow the instructions provided later in this topic.</span></span>

> [!Note]  
> <span data-ttu-id="1229f-123">Existen consideraciones especiales para Windows de 64 bits al registrar controladores que funcionan en el contexto de las aplicaciones de 32 bits: cuando los verbos de Shell se invocan en el contexto de una aplicación de 32 bits, el subsistema WOW64 redirige el acceso del sistema de archivos a algunas rutas de acceso.</span><span class="sxs-lookup"><span data-stu-id="1229f-123">There are special considerations for 64-bit Windows when registering handlers that work in the context of 32-bit applications: when Shell verbs are invoked in the context of a 32-bit application, the WOW64 subsystem redirects file system access to some paths.</span></span> <span data-ttu-id="1229f-124">Si el controlador. exe se almacena en una de esas rutas de acceso, no es accesible en este contexto.</span><span class="sxs-lookup"><span data-stu-id="1229f-124">If your .exe handler is stored in one of those paths, it is not accessible in this context.</span></span> <span data-ttu-id="1229f-125">Por lo tanto, como solución alternativa, almacene el archivo. exe en una ruta de acceso que no se redirija, o bien almacene una versión de código auxiliar del archivo. exe que inicia la versión real.</span><span class="sxs-lookup"><span data-stu-id="1229f-125">Therefore, as a work around, either store your .exe in a path that does not get redirected, or store a stub version of your .exe that launches the real version.</span></span>

 

## <a name="how-shortcut-menu-handlers-work-with-dynamic-verbs"></a><span data-ttu-id="1229f-126">Cómo funcionan los controladores de menú contextual con verbos dinámicos</span><span class="sxs-lookup"><span data-stu-id="1229f-126">How Shortcut Menu Handlers Work with Dynamic Verbs</span></span>

<span data-ttu-id="1229f-127">Además de [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown), los controladores de menú contextual exportan las siguientes interfaces adicionales para controlar la mensajería necesaria para implementar elementos de menú dibujados por el propietario:</span><span class="sxs-lookup"><span data-stu-id="1229f-127">In addition to [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown), shortcut menu handlers export the following additional interfaces to handle the messaging needed to implement owner-drawn menu items:</span></span>

-   <span data-ttu-id="1229f-128">[**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) (obligatorio)</span><span class="sxs-lookup"><span data-stu-id="1229f-128">[**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) (mandatory)</span></span>
-   <span data-ttu-id="1229f-129">[**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) (obligatorio)</span><span class="sxs-lookup"><span data-stu-id="1229f-129">[**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) (mandatory)</span></span>
-   <span data-ttu-id="1229f-130">[**IContextMenu2**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu2) (opcional)</span><span class="sxs-lookup"><span data-stu-id="1229f-130">[**IContextMenu2**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu2) (optional)</span></span>
-   <span data-ttu-id="1229f-131">[**IContextMenu3**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu3) (opcional)</span><span class="sxs-lookup"><span data-stu-id="1229f-131">[**IContextMenu3**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu3) (optional)</span></span>

<span data-ttu-id="1229f-132">Para obtener más información sobre los elementos de menú dibujados por el propietario, consulte la sección *creación de Owner-Drawn elementos de menú* en [uso de menús](../menurc/using-menus.md).</span><span class="sxs-lookup"><span data-stu-id="1229f-132">For more information on owner-drawn menu items, see the *Creating Owner-Drawn Menu Items* section in [Using Menus](../menurc/using-menus.md).</span></span>

<span data-ttu-id="1229f-133">Shell usa la interfaz [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) para inicializar el controlador.</span><span class="sxs-lookup"><span data-stu-id="1229f-133">Shell uses the [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) interface to initialize the handler.</span></span> <span data-ttu-id="1229f-134">Cuando el shell llama a [**IShellExtInit:: Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize), pasa un objeto de datos con el nombre del objeto y un puntero a una lista de identificadores de elemento (PIDL) de la carpeta que contiene el archivo.</span><span class="sxs-lookup"><span data-stu-id="1229f-134">When the Shell calls [**IShellExtInit::Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize), it passes in a data object with the object's name and a pointer to an item identifier list (PIDL) of the folder that contains the file.</span></span> <span data-ttu-id="1229f-135">El parámetro *hkeyProgID* es la ubicación del registro en la que se registra el identificador del menú contextual.</span><span class="sxs-lookup"><span data-stu-id="1229f-135">The *hkeyProgID* parameter is the registry location under which the shortcut menu handle is registered.</span></span> <span data-ttu-id="1229f-136">El método **IShellExtInit:: Initialize** debe extraer el nombre de archivo del objeto de datos y almacenar el nombre y el puntero de la carpeta en una lista de identificadores de elemento (PIDL) para su uso posterior.</span><span class="sxs-lookup"><span data-stu-id="1229f-136">The **IShellExtInit::Initialize** method must extract the file name from the data object and store the name and the folder's pointer to an item identifier list (PIDL) for later use.</span></span> <span data-ttu-id="1229f-137">Para obtener más información sobre la inicialización del controlador, vea [implementar IShellExtInit](handlers.md).</span><span class="sxs-lookup"><span data-stu-id="1229f-137">For more information on handler initialization, see [Implementing IShellExtInit](handlers.md).</span></span>

<span data-ttu-id="1229f-138">Cuando los verbos se presentan en un menú contextual, se detectan primero y, a continuación, se presentan al usuario y, por último, se invocan.</span><span class="sxs-lookup"><span data-stu-id="1229f-138">When verbs are presented in a shortcut menu, they are first discovered, then presented to the user, and finally invoked.</span></span> <span data-ttu-id="1229f-139">En la lista siguiente se describen estos tres pasos con más detalle:</span><span class="sxs-lookup"><span data-stu-id="1229f-139">The following list describes these three steps in more detail:</span></span>

1.  <span data-ttu-id="1229f-140">El shell llama a [**IContextMenu:: QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu), que devuelve un conjunto de verbos que pueden basarse en el estado de los elementos o del sistema.</span><span class="sxs-lookup"><span data-stu-id="1229f-140">The Shell calls [**IContextMenu::QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu), which returns a set of verbs that can be based on the state of the items or the system.</span></span>
2.  <span data-ttu-id="1229f-141">El sistema pasa un identificador **HMENU** que el método puede usar para agregar elementos al menú contextual.</span><span class="sxs-lookup"><span data-stu-id="1229f-141">The system passes in an **HMENU** handle that the method can use to add items to the shortcut menu.</span></span>
3.  <span data-ttu-id="1229f-142">Si el usuario hace clic en uno de los elementos del controlador, el shell llama a [**IContextMenu:: InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand).</span><span class="sxs-lookup"><span data-stu-id="1229f-142">If the user clicks one of the handler's items, the Shell calls [**IContextMenu::InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand).</span></span> <span data-ttu-id="1229f-143">Después, el controlador puede ejecutar el comando adecuado.</span><span class="sxs-lookup"><span data-stu-id="1229f-143">The handler can then execute the appropriate command.</span></span>

## <a name="avoiding-collisions-due-to-unqualified-verb-names"></a><span data-ttu-id="1229f-144">Evitar colisiones debido a nombres de verbo no completos</span><span class="sxs-lookup"><span data-stu-id="1229f-144">Avoiding Collisions Due to Unqualified Verb Names</span></span>

<span data-ttu-id="1229f-145">Dado que los verbos se registran por tipo, se puede usar el mismo nombre de verbo para los verbos en elementos diferentes.</span><span class="sxs-lookup"><span data-stu-id="1229f-145">Because verbs are registered per type, the same verb name can be used for verbs on different items.</span></span> <span data-ttu-id="1229f-146">Esto permite que las aplicaciones hagan referencia a verbos comunes independientes del tipo de elemento.</span><span class="sxs-lookup"><span data-stu-id="1229f-146">Doing so enables applications to refer to common verbs independent of the item type.</span></span> <span data-ttu-id="1229f-147">Aunque esta funcionalidad es útil, el uso de nombres no completos puede producir colisiones con varios fabricantes de software independientes (ISV) que elijan el mismo nombre de verbo.</span><span class="sxs-lookup"><span data-stu-id="1229f-147">While this functionality is useful, the use of unqualified names can result in collisions with multiple independent software vendors (ISVs) that choose the same verb name.</span></span> <span data-ttu-id="1229f-148">Para evitar esto, debe prefijar siempre los verbos con el nombre de ISV como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="1229f-148">To avoid this, always prefix verbs with the ISV name as follows:</span></span>

`ISV_Name.verb`

<span data-ttu-id="1229f-149">Use siempre un ProgID específico de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="1229f-149">Always use an application specific ProgID.</span></span> <span data-ttu-id="1229f-150">La adopción de la Convención de asignación de la extensión de nombre de archivo a un ProgID proporcionado por ISV evita posibles colisiones.</span><span class="sxs-lookup"><span data-stu-id="1229f-150">Adopting the convention of mapping the file name extension to an ISV provided ProgID avoids potential collisions.</span></span> <span data-ttu-id="1229f-151">Sin embargo, dado que algunos tipos de elemento no usan esta asignación, es necesario usar nombres únicos de proveedor.</span><span class="sxs-lookup"><span data-stu-id="1229f-151">However, because some item types do not use this mapping, there is a need for vendor-unique names.</span></span> <span data-ttu-id="1229f-152">Al agregar un verbo a un ProgID existente que ya tiene el verbo registrado, primero debe quitar la clave del registro del verbo anterior antes de agregar su propio verbo.</span><span class="sxs-lookup"><span data-stu-id="1229f-152">When adding a verb to an existing ProgID that might already have that verb registered, you must first remove the registry key for the old verb before adding your own verb.</span></span> <span data-ttu-id="1229f-153">Debe hacerlo para evitar la combinación de la información del verbo de los dos verbos.</span><span class="sxs-lookup"><span data-stu-id="1229f-153">You must do so to avoid merging the verb information from the two verbs.</span></span> <span data-ttu-id="1229f-154">Si no lo hace, se producirá un comportamiento imprevisible.</span><span class="sxs-lookup"><span data-stu-id="1229f-154">Failure to do so results in unpredictable behavior.</span></span>

## <a name="registering-a-shortcut-menu-handler-with-a-dynamic-verb"></a><span data-ttu-id="1229f-155">Registrar un controlador de menú contextual con un verbo dinámico</span><span class="sxs-lookup"><span data-stu-id="1229f-155">Registering a Shortcut Menu Handler with a Dynamic Verb</span></span>

<span data-ttu-id="1229f-156">Los controladores de menú contextual están asociados a un tipo de archivo o a una carpeta.</span><span class="sxs-lookup"><span data-stu-id="1229f-156">Shortcut menu handlers are associated with either a file type or a folder.</span></span> <span data-ttu-id="1229f-157">En el caso de los tipos de archivo, el controlador se registra en la subclave siguiente.</span><span class="sxs-lookup"><span data-stu-id="1229f-157">For file types, the handler is registered under the following subkey.</span></span>

```
HKEY_CLASSES_ROOT
   Program ID
      shellex
         ContextMenuHandlers
```

<span data-ttu-id="1229f-158">Para asociar un controlador de menú contextual con un tipo de archivo o una carpeta, primero cree una subclave en la subclave **ContextMenuHandlers** .</span><span class="sxs-lookup"><span data-stu-id="1229f-158">To associate a shortcut menu handler with either a file type or a folder, first create a subkey under the **ContextMenuHandlers** subkey.</span></span> <span data-ttu-id="1229f-159">Asigne un nombre a la subclave del controlador y establezca el valor predeterminado de la subclave en el formato de cadena del GUID del identificador de clase (CLSID) del controlador.</span><span class="sxs-lookup"><span data-stu-id="1229f-159">Name the subkey for the handler, and set the subkey's default value to the string form of the handler's class identifier (CLSID) GUID.</span></span>

<span data-ttu-id="1229f-160">Después, para asociar un controlador de menú contextual con distintos tipos de carpetas, registre el controlador del mismo modo que lo haría para un tipo de archivo, pero en la subclave *FolderType* , tal y como se muestra en el ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="1229f-160">Then to associate a shortcut menu handler with different kinds of folders, register the handler the same way you would for a file type, but under the *FolderType* subkey as shown in the following example.</span></span>

```
HKEY_CLASSES_ROOT
   FolderType
      shellex
         ContextMenuHandlers
```

<span data-ttu-id="1229f-161">Para obtener más información acerca de los tipos de carpetas para los que puede registrar controladores, consulte [registrar controladores de extensión de Shell](handlers.md).</span><span class="sxs-lookup"><span data-stu-id="1229f-161">For more information about about which folder types you can register handlers for, see [Registering Shell Extension Handlers](handlers.md).</span></span>

<span data-ttu-id="1229f-162">Si un tipo de archivo tiene un menú contextual asociado, al hacer doble clic en un objeto se inicia normalmente el comando predeterminado y no se llama al método [**IContextMenu:: QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) del controlador.</span><span class="sxs-lookup"><span data-stu-id="1229f-162">If a file type has a shortcut menu associated with it, then double-clicking an object normally launches the default command, and the handler's [**IContextMenu::QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) method is not called.</span></span> <span data-ttu-id="1229f-163">Para especificar que se debe llamar al método **IContextMenu:: QueryContextMenu** del controlador cuando se hace doble clic en un objeto, cree una subclave en la subclave **CLSID** del controlador, como se muestra aquí.</span><span class="sxs-lookup"><span data-stu-id="1229f-163">To specify that the handler's **IContextMenu::QueryContextMenu** method should be called when an object is double-clicked, create a subkey under the handler's **CLSID** subkey as shown here.</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      {00000000-1111-2222-3333-444444444444}
         shellex
            MayChangeDefaultMenu
```

<span data-ttu-id="1229f-164">Cuando se hace doble clic en un objeto asociado al controlador, se llama a [**IContextMenu:: QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) con la marca **CMF \_ DEFAULTONLY** establecida en el parámetro *uFlags* .</span><span class="sxs-lookup"><span data-stu-id="1229f-164">When an object associated with the handler is double-clicked, [**IContextMenu::QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) is called with the **CMF\_DEFAULTONLY** flag set in the *uFlags* parameter.</span></span>

<span data-ttu-id="1229f-165">Los controladores de menú contextual solo deben establecer la subclave **MayChangeDefaultMenu** si es posible que necesiten cambiar el verbo predeterminado del menú contextual.</span><span class="sxs-lookup"><span data-stu-id="1229f-165">Shortcut menu handlers should set the **MayChangeDefaultMenu** subkey only if they might need to change the shortcut menu's default verb.</span></span> <span data-ttu-id="1229f-166">Al establecer esta subclave, el sistema carga el archivo DLL del controlador cuando se hace doble clic en un elemento asociado.</span><span class="sxs-lookup"><span data-stu-id="1229f-166">Setting this subkey forces the system to load the handler's DLL when an associated item is double-clicked.</span></span> <span data-ttu-id="1229f-167">Si el controlador no cambia el verbo predeterminado, no debe establecer esta subclave, ya que esto hace que el sistema cargue el archivo DLL innecesariamente.</span><span class="sxs-lookup"><span data-stu-id="1229f-167">If your handler does not change the default verb, you should not set this subkey because doing so causes the system to load your DLL unnecessarily.</span></span>

<span data-ttu-id="1229f-168">En el ejemplo siguiente se muestran las entradas del registro que habilitan un controlador de menú contextual para un tipo de archivo. MYP.</span><span class="sxs-lookup"><span data-stu-id="1229f-168">The following example illustrates registry entries that enable a shortcut menu handler for an .myp file type.</span></span> <span data-ttu-id="1229f-169">La subclave **CLSID** del controlador incluye una subclave **MayChangeDefaultMenu** para garantizar que se llama al controlador cuando el usuario hace doble clic en un objeto relacionado.</span><span class="sxs-lookup"><span data-stu-id="1229f-169">The handler's **CLSID** subkey includes a **MayChangeDefaultMenu** subkey to guarantee that the handler is called when the user double-clicks a related object.</span></span>

```
HKEY_CLASSES_ROOT
   .myp
      (Default) = MyProgram.1
   CLSID
      {00000000-1111-2222-3333-444444444444}
         InProcServer32
            (Default) = C:\MyDir\MyCommand.dll
            ThreadingModel = Apartment
         shellex
            MayChangeDefaultMenu
   MyProgram.1
      (Default) = MyProgram Application
      shellex
         ContextMenuHandler
            MyCommand = {00000000-1111-2222-3333-444444444444}
```

## <a name="implementing-the-icontextmenu-interface"></a><span data-ttu-id="1229f-170">Implementar la interfaz IContextMenu</span><span class="sxs-lookup"><span data-stu-id="1229f-170">Implementing the IContextMenu Interface</span></span>

<span data-ttu-id="1229f-171">[**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) es el método más eficaz, pero también el más complicado de implementar.</span><span class="sxs-lookup"><span data-stu-id="1229f-171">[**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) is the most powerful but also the most complicated method to implement.</span></span> <span data-ttu-id="1229f-172">Se recomienda encarecidamente implementar un verbo utilizando uno de los métodos estáticos Verb.</span><span class="sxs-lookup"><span data-stu-id="1229f-172">We strongly recommend that you implement a verb by using one of the static verb methods.</span></span> <span data-ttu-id="1229f-173">Para obtener más información, vea [elegir un verbo estático o dinámico para el menú contextual](shortcut-choose-method.md).</span><span class="sxs-lookup"><span data-stu-id="1229f-173">For more information, see [Choosing a Static or Dynamic Verb for your Shortcut Menu](shortcut-choose-method.md).</span></span> <span data-ttu-id="1229f-174">[**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) tiene tres métodos, **GetCommandString**, **InvokeCommand** y **QueryContextMenu**, que se describen aquí en detalle.</span><span class="sxs-lookup"><span data-stu-id="1229f-174">[**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) has three methods, **GetCommandString**, **InvokeCommand**, and **QueryContextMenu**, which are discussed here in detail.</span></span>

### <a name="icontextmenugetcommandstring-method"></a><span data-ttu-id="1229f-175">IContextMenu:: GetCommandString (método)</span><span class="sxs-lookup"><span data-stu-id="1229f-175">IContextMenu::GetCommandString Method</span></span>

<span data-ttu-id="1229f-176">El método [**IContextMenu:: GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) del controlador se usa para devolver el nombre canónico de un verbo.</span><span class="sxs-lookup"><span data-stu-id="1229f-176">The handler's [**IContextMenu::GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) method is used to return the canonical name for a verb.</span></span> <span data-ttu-id="1229f-177">Este método es opcional.</span><span class="sxs-lookup"><span data-stu-id="1229f-177">This method is optional.</span></span> <span data-ttu-id="1229f-178">En Windows XP y versiones anteriores de Windows, cuando el explorador de Windows tiene una barra de estado, este método se usa para recuperar el texto de ayuda que se muestra en la barra de estado de un elemento de menú.</span><span class="sxs-lookup"><span data-stu-id="1229f-178">In Windows XP and earlier versions of Windows, when Windows Explorer has a Status bar, this method is used to retrieve the help text that is displayed in the Status bar for a menu item.</span></span>

<span data-ttu-id="1229f-179">El parámetro *idCmd* contiene el desplazamiento de identificador del comando que se definió cuando se llamó a [**IContextMenu:: QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) .</span><span class="sxs-lookup"><span data-stu-id="1229f-179">The *idCmd* parameter holds the identifier offset of the command that was defined when [**IContextMenu::QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) was called.</span></span> <span data-ttu-id="1229f-180">Si se solicita una cadena de ayuda, *uFlags* se establecerá en **GC \_ HELPTEXTW**.</span><span class="sxs-lookup"><span data-stu-id="1229f-180">If a help string is requested, *uFlags* will be set to **GCS\_HELPTEXTW**.</span></span> <span data-ttu-id="1229f-181">Copie la cadena de ayuda en el búfer de *pszName empiezan* , convirtiéndola en un **PWSTR**.</span><span class="sxs-lookup"><span data-stu-id="1229f-181">Copy the help string to the *pszName* buffer, casting it to a **PWSTR**.</span></span> <span data-ttu-id="1229f-182">La cadena de verbo se solicita estableciendo *uFlags* en **GC \_ VERBW**.</span><span class="sxs-lookup"><span data-stu-id="1229f-182">The verb string is requested by setting *uFlags* to **GCS\_VERBW**.</span></span> <span data-ttu-id="1229f-183">Copie la cadena adecuada en *pszName empiezan*, al igual que con la cadena de ayuda.</span><span class="sxs-lookup"><span data-stu-id="1229f-183">Copy the appropriate string to *pszName*, just as with the help string.</span></span> <span data-ttu-id="1229f-184">Los controladores de menú contextual no usan las marcas **GC \_ validatea** y **GC \_ VALIDATEW** .</span><span class="sxs-lookup"><span data-stu-id="1229f-184">The **GCS\_VALIDATEA** and **GCS\_VALIDATEW** flags are not used by shortcut menu handlers.</span></span>

<span data-ttu-id="1229f-185">En el ejemplo siguiente se muestra una implementación simple de [**IContextMenu:: GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) que corresponde al ejemplo [**IContextMenu:: QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) proporcionado en la sección del [método IContextMenu:: QueryContextMenu](#icontextmenuquerycontextmenu-method) de este tema.</span><span class="sxs-lookup"><span data-stu-id="1229f-185">The following example shows a simple implementation of [**IContextMenu::GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) that corresponds to the [**IContextMenu::QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) example given in the [IContextMenu::QueryContextMenu Method](#icontextmenuquerycontextmenu-method) section of this topic.</span></span> <span data-ttu-id="1229f-186">Dado que el controlador solo agrega un elemento de menú, solo hay un conjunto de cadenas que se pueden devolver.</span><span class="sxs-lookup"><span data-stu-id="1229f-186">Because the handler adds only one menu item, there is only one set of strings that can be returned.</span></span> <span data-ttu-id="1229f-187">El método comprueba si *idCmd* es válido y, si es así, devuelve la cadena solicitada.</span><span class="sxs-lookup"><span data-stu-id="1229f-187">The method tests whether *idCmd* is valid and, if it is, returns the requested string.</span></span>

<span data-ttu-id="1229f-188">La función [**StringCchCopy**](/windows/win32/api/strsafe/nf-strsafe-stringcchcopya) se usa para copiar la cadena solicitada en *pszName empiezan* para asegurarse de que la cadena copiada no supera el tamaño del búfer especificado por *cchName*.</span><span class="sxs-lookup"><span data-stu-id="1229f-188">The [**StringCchCopy**](/windows/win32/api/strsafe/nf-strsafe-stringcchcopya) function is used to copy the requested string to *pszName* to ensure that the copied string does not exceed the size of the buffer specified by *cchName*.</span></span> <span data-ttu-id="1229f-189">En este ejemplo solo se implementa la compatibilidad con los valores Unicode de *uFlags*, ya que solo se han utilizado en el explorador de Windows desde Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="1229f-189">This example only implements support for the Unicode values of *uFlags*, because only those have been used in Windows Explorer since Windows 2000.</span></span>


```C++
IFACEMETHODIMP CMenuExtension::GetCommandString(UINT idCommand, 
                                                UINT uFlags, 
                                                UINT *pReserved, 
                                                PSTR pszName, 
                                                UINT cchName)
{
    HRESULT hr = E_INVALIDARG;

    if (idCommand == IDM_DISPLAY)
    {
        switch (uFlags)
        {
            case GCS_HELPTEXTW:
                // Only useful for pre-Vista versions of Windows that 
                // have a Status bar.
                hr = StringCchCopyW(reinterpret_cast<PWSTR>(pszName), 
                                    cchName, 
                                    L"Display File Name");
                break; 

            case GCS_VERBW:
                // GCS_VERBW is an optional feature that enables a caller
                // to discover the canonical name for the verb passed in
                // through idCommand.
                hr = StringCchCopyW(reinterpret_cast<PWSTR>(pszName), 
                                    cchName, 
                                    L"DisplayFileName");
                break; 
        }
    }
    return hr;
}
```



### <a name="icontextmenuinvokecommand-method"></a><span data-ttu-id="1229f-190">IContextMenu:: InvokeCommand (método)</span><span class="sxs-lookup"><span data-stu-id="1229f-190">IContextMenu::InvokeCommand Method</span></span>

<span data-ttu-id="1229f-191">Se llama a este método cuando un usuario hace clic en un elemento de menú para indicar al controlador que ejecute el comando asociado.</span><span class="sxs-lookup"><span data-stu-id="1229f-191">This method is called when a user clicks a menu item to tell the handler to run the associated command.</span></span> <span data-ttu-id="1229f-192">El parámetro *pici* apunta a una estructura que contiene la información requerida.</span><span class="sxs-lookup"><span data-stu-id="1229f-192">The *pici* parameter points to a structure that contains the information required.</span></span>

<span data-ttu-id="1229f-193">Aunque *pici* se declara en ShlObj. h como una estructura [**CMINVOKECOMMANDINFO**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfo) , en la práctica suele apuntar a una estructura [**CMINVOKECOMMANDINFOEX**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfoex) .</span><span class="sxs-lookup"><span data-stu-id="1229f-193">Although *pici* is declared in Shlobj.h as a [**CMINVOKECOMMANDINFO**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfo) structure, in practice it often points to a [**CMINVOKECOMMANDINFOEX**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfoex) structure.</span></span> <span data-ttu-id="1229f-194">Esta estructura es una versión extendida de **CMINVOKECOMMANDINFO** y tiene varios miembros adicionales que permiten pasar cadenas Unicode.</span><span class="sxs-lookup"><span data-stu-id="1229f-194">This structure is an extended version of **CMINVOKECOMMANDINFO** and has several additional members that make it possible to pass Unicode strings.</span></span>

<span data-ttu-id="1229f-195">Compruebe el miembro **cbSize** de *pici* para determinar la estructura que se ha pasado.</span><span class="sxs-lookup"><span data-stu-id="1229f-195">Check the **cbSize** member of *pici* to determine which structure was passed in.</span></span> <span data-ttu-id="1229f-196">Si es una estructura [**CMINVOKECOMMANDINFOEX**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfoex) y el miembro **fMask** tiene establecida la **marca \_ \_ Unicode CMIC Mask** , convierta *pici* en **CMINVOKECOMMANDINFOEX**.</span><span class="sxs-lookup"><span data-stu-id="1229f-196">If it is a [**CMINVOKECOMMANDINFOEX**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfoex) structure and the **fMask** member has the **CMIC\_MASK\_UNICODE** flag set, cast *pici* to **CMINVOKECOMMANDINFOEX**.</span></span> <span data-ttu-id="1229f-197">Esto permite que la aplicación use la información Unicode contenida en los cinco últimos miembros de la estructura.</span><span class="sxs-lookup"><span data-stu-id="1229f-197">This enables your application to use the Unicode information contained in the last five members of the structure.</span></span>

<span data-ttu-id="1229f-198">El miembro **lpVerb** o **lpVerbW** de la estructura se usa para identificar el comando que se va a ejecutar.</span><span class="sxs-lookup"><span data-stu-id="1229f-198">The structure's **lpVerb** or **lpVerbW** member is used to identify the command to be executed.</span></span> <span data-ttu-id="1229f-199">Los comandos se identifican de una de las dos maneras siguientes:</span><span class="sxs-lookup"><span data-stu-id="1229f-199">Commands are identified in one of the following two ways:</span></span>

-   <span data-ttu-id="1229f-200">Por la cadena de verbo del comando</span><span class="sxs-lookup"><span data-stu-id="1229f-200">By the command's verb string</span></span>
-   <span data-ttu-id="1229f-201">Por el desplazamiento del identificador del comando</span><span class="sxs-lookup"><span data-stu-id="1229f-201">By the command's identifier offset</span></span>

<span data-ttu-id="1229f-202">Para distinguir entre estos dos casos, Compruebe la palabra de orden superior de **lpVerb** para el caso ANSI o **lpVerbW** para el caso de Unicode.</span><span class="sxs-lookup"><span data-stu-id="1229f-202">To distinguish between these two cases, check the high-order word of **lpVerb** for the ANSI case or **lpVerbW** for the Unicode case.</span></span> <span data-ttu-id="1229f-203">Si la palabra de orden superior es distinto de cero, **lpVerb** o **lpVerbW** contiene una cadena de verbo.</span><span class="sxs-lookup"><span data-stu-id="1229f-203">If the high-order word is nonzero, **lpVerb** or **lpVerbW** holds a verb string.</span></span> <span data-ttu-id="1229f-204">Si la palabra de orden superior es cero, el desplazamiento del comando se encuentra en la palabra de orden inferior de **lpVerb**.</span><span class="sxs-lookup"><span data-stu-id="1229f-204">If the high-order word is zero, the command offset is in the low-order word of **lpVerb**.</span></span>

<span data-ttu-id="1229f-205">En el ejemplo siguiente se muestra una implementación simple de [**IContextMenu:: InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) que corresponde a los ejemplos [**IContextMenu:: QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) y [**IContextMenu:: GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) especificados antes y después de esta sección.</span><span class="sxs-lookup"><span data-stu-id="1229f-205">The following example shows a simple implementation of [**IContextMenu::InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) that corresponds to the [**IContextMenu::QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) and [**IContextMenu::GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) examples given before and after this section.</span></span> <span data-ttu-id="1229f-206">El método determina primero la estructura que se va a pasar.</span><span class="sxs-lookup"><span data-stu-id="1229f-206">The method first determines which structure is being passed in.</span></span> <span data-ttu-id="1229f-207">A continuación, determina si el comando se identifica por su desplazamiento o por su verbo.</span><span class="sxs-lookup"><span data-stu-id="1229f-207">It then determines whether the command is identified by its offset or its verb.</span></span> <span data-ttu-id="1229f-208">Si **lpVerb** o **lpVerbW** contiene un verbo o desplazamiento válido, el método muestra un cuadro de mensaje.</span><span class="sxs-lookup"><span data-stu-id="1229f-208">If **lpVerb** or **lpVerbW** holds a valid verb or offset, the method displays a message box.</span></span>


```C++
STDMETHODIMP CShellExtension::InvokeCommand(LPCMINVOKECOMMANDINFO lpcmi)
{
    BOOL fEx = FALSE;
    BOOL fUnicode = FALSE;

    if(lpcmi->cbSize == sizeof(CMINVOKECOMMANDINFOEX))
    {
        fEx = TRUE;
        if((lpcmi->fMask & CMIC_MASK_UNICODE))
        {
            fUnicode = TRUE;
        }
    }

    if( !fUnicode && HIWORD(lpcmi->lpVerb))
    {
        if(StrCmpIA(lpcmi->lpVerb, m_pszVerb))
        {
            return E_FAIL;
        }
    }

    else if( fUnicode && HIWORD(((CMINVOKECOMMANDINFOEX *) lpcmi)->lpVerbW))
    {
        if(StrCmpIW(((CMINVOKECOMMANDINFOEX *)lpcmi)->lpVerbW, m_pwszVerb))
        {
            return E_FAIL;
        }
    }

    else if(LOWORD(lpcmi->lpVerb) != IDM_DISPLAY)
    {
        return E_FAIL;
    }

    else
    {
        MessageBox(lpcmi->hwnd,
                   "The File Name",
                   "File Name",
                   MB_OK|MB_ICONINFORMATION);
    }

    return S_OK;
}
```



### <a name="icontextmenuquerycontextmenu-method"></a><span data-ttu-id="1229f-209">IContextMenu:: QueryContextMenu (método)</span><span class="sxs-lookup"><span data-stu-id="1229f-209">IContextMenu::QueryContextMenu Method</span></span>

<span data-ttu-id="1229f-210">El shell llama a [**IContextMenu:: QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) para habilitar el controlador de menú contextual para agregar sus elementos de menú al menú.</span><span class="sxs-lookup"><span data-stu-id="1229f-210">The Shell calls [**IContextMenu::QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) to enable the shortcut menu handler to add its menu items to the menu.</span></span> <span data-ttu-id="1229f-211">Pasa el identificador **HMENU** en el parámetro *HMENU* .</span><span class="sxs-lookup"><span data-stu-id="1229f-211">It passes in the **HMENU** handle in the *hmenu* parameter.</span></span> <span data-ttu-id="1229f-212">El parámetro *indexMenu* se establece en el índice que se va a usar para el primer elemento de menú que se va a agregar.</span><span class="sxs-lookup"><span data-stu-id="1229f-212">The *indexMenu* parameter is set to the index to be used for the first menu item that is to be added.</span></span>

<span data-ttu-id="1229f-213">Los elementos de menú que agregue el controlador deben tener identificadores que se encuentren entre los valores de los parámetros *idCmdFirst* y *idCmdLast* .</span><span class="sxs-lookup"><span data-stu-id="1229f-213">Any menu items that are added by the handler must have identifiers that fall between the values in the *idCmdFirst* and *idCmdLast* parameters.</span></span> <span data-ttu-id="1229f-214">Normalmente, el primer identificador de comando se establece en *idCmdFirst*, que se incrementa en uno (1) para cada comando adicional.</span><span class="sxs-lookup"><span data-stu-id="1229f-214">Typically, the first command identifier is set to *idCmdFirst*, which is incremented by one (1) for each additional command.</span></span> <span data-ttu-id="1229f-215">Esta práctica le ayuda a evitar superar *idCmdLast* y maximiza el número de identificadores disponibles en caso de que el shell llame a más de un controlador.</span><span class="sxs-lookup"><span data-stu-id="1229f-215">This practice helps you avoid exceeding *idCmdLast* and maximizes the number of available identifiers in case the Shell calls more than one handler.</span></span>

<span data-ttu-id="1229f-216">El *desplazamiento de comandos* de un identificador de elemento es la diferencia entre el identificador y el valor de *idCmdFirst*.</span><span class="sxs-lookup"><span data-stu-id="1229f-216">An item identifier's *command offset* is the difference between the identifier and the value in *idCmdFirst*.</span></span> <span data-ttu-id="1229f-217">Almacene el desplazamiento de cada elemento que el controlador agrega al menú contextual porque el shell podría utilizarlo para identificar el elemento si después llama a [**IContextMenu:: GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) o [**IContextMenu:: InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand).</span><span class="sxs-lookup"><span data-stu-id="1229f-217">Store the offset of each item that your handler adds to the shortcut menu because the Shell might use it to identify the item if it subsequently calls [**IContextMenu::GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) or [**IContextMenu::InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand).</span></span>

<span data-ttu-id="1229f-218">También debe asignar un [verbo](launch.md) a cada comando que agregue.</span><span class="sxs-lookup"><span data-stu-id="1229f-218">You should also assign a [verb](launch.md) to each command you add.</span></span> <span data-ttu-id="1229f-219">Un verbo es una cadena que se puede utilizar en lugar del desplazamiento para identificar el comando cuando se llama a [**IContextMenu:: InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) .</span><span class="sxs-lookup"><span data-stu-id="1229f-219">A verb is a string that can be used instead of the offset to identify the command when [**IContextMenu::InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) is called.</span></span> <span data-ttu-id="1229f-220">También lo usan funciones como [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) para ejecutar comandos de menú contextual.</span><span class="sxs-lookup"><span data-stu-id="1229f-220">It is also used by functions such as [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) to execute shortcut menu commands.</span></span>

<span data-ttu-id="1229f-221">Hay tres marcas que se pueden pasar a través del parámetro *uFlags* que son relevantes para los controladores de menús contextuales.</span><span class="sxs-lookup"><span data-stu-id="1229f-221">There are three flags that can be passed in through the *uFlags* parameter that are relevant to shortcut menu handlers.</span></span> <span data-ttu-id="1229f-222">Se describen en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="1229f-222">They are described in the following table.</span></span>



| <span data-ttu-id="1229f-223">Marca</span><span class="sxs-lookup"><span data-stu-id="1229f-223">Flag</span></span>             | <span data-ttu-id="1229f-224">Descripción</span><span class="sxs-lookup"><span data-stu-id="1229f-224">Description</span></span>                                                                                                                                                                                                              |
|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1229f-225">CMF \_ DEFAULTONLY</span><span class="sxs-lookup"><span data-stu-id="1229f-225">CMF\_DEFAULTONLY</span></span> | <span data-ttu-id="1229f-226">El usuario ha seleccionado el comando predeterminado, normalmente haciendo doble clic en el objeto.</span><span class="sxs-lookup"><span data-stu-id="1229f-226">The user has selected the default command, usually by double-clicking the object.</span></span> <span data-ttu-id="1229f-227">[**IContextMenu:: QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) debe devolver el control al shell sin modificar el menú.</span><span class="sxs-lookup"><span data-stu-id="1229f-227">[**IContextMenu::QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) should return control to the Shell without modifying the menu.</span></span> |
| <span data-ttu-id="1229f-228">CMF \_ NOdefault</span><span class="sxs-lookup"><span data-stu-id="1229f-228">CMF\_NODEFAULT</span></span>   | <span data-ttu-id="1229f-229">Ningún elemento del menú debe ser el elemento predeterminado.</span><span class="sxs-lookup"><span data-stu-id="1229f-229">No item in the menu should be the default item.</span></span> <span data-ttu-id="1229f-230">El método debe agregar sus comandos al menú.</span><span class="sxs-lookup"><span data-stu-id="1229f-230">The method should add its commands to the menu.</span></span>                                                                                                                          |
| <span data-ttu-id="1229f-231">CMF \_ normal</span><span class="sxs-lookup"><span data-stu-id="1229f-231">CMF\_NORMAL</span></span>      | <span data-ttu-id="1229f-232">El menú contextual se mostrará normalmente.</span><span class="sxs-lookup"><span data-stu-id="1229f-232">The shortcut menu will be displayed normally.</span></span> <span data-ttu-id="1229f-233">El método debe agregar sus comandos al menú.</span><span class="sxs-lookup"><span data-stu-id="1229f-233">The method should add its commands to the menu.</span></span>                                                                                                                            |



 

<span data-ttu-id="1229f-234">Use [**InsertMenu**](/windows/win32/api/winuser/nf-winuser-insertmenua) o [**InsertMenuItem**](/windows/win32/api/winuser/nf-winuser-insertmenuitema) para agregar elementos de menú a la lista.</span><span class="sxs-lookup"><span data-stu-id="1229f-234">Use either [**InsertMenu**](/windows/win32/api/winuser/nf-winuser-insertmenua) or [**InsertMenuItem**](/windows/win32/api/winuser/nf-winuser-insertmenuitema) to add menu items to the list.</span></span> <span data-ttu-id="1229f-235">A continuación, devuelva un valor **HRESULT** con la gravedad establecida en **Severity \_ Success**.</span><span class="sxs-lookup"><span data-stu-id="1229f-235">Then return an **HRESULT** value with the severity set to **SEVERITY\_SUCCESS**.</span></span> <span data-ttu-id="1229f-236">Establezca el valor del código en el desplazamiento del identificador de comando más grande que se asignó, más uno (1).</span><span class="sxs-lookup"><span data-stu-id="1229f-236">Set the code value to the offset of the largest command identifier that was assigned, plus one (1).</span></span> <span data-ttu-id="1229f-237">Por ejemplo, supongamos que *idCmdFirst* está establecido en 5 y agrega tres elementos al menú con identificadores de comando de 5, 7 y 8.</span><span class="sxs-lookup"><span data-stu-id="1229f-237">For example, assume that *idCmdFirst* is set to 5 and you add three items to the menu with command identifiers of 5, 7, and 8.</span></span> <span data-ttu-id="1229f-238">El valor devuelto debe ser `MAKE_HRESULT(SEVERITY_SUCCESS, 0, 8 - 5 + 1)` .</span><span class="sxs-lookup"><span data-stu-id="1229f-238">The return value should be `MAKE_HRESULT(SEVERITY_SUCCESS, 0, 8 - 5 + 1)`.</span></span>

<span data-ttu-id="1229f-239">En el ejemplo siguiente se muestra una implementación simple de [**IContextMenu:: QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) que inserta un solo comando.</span><span class="sxs-lookup"><span data-stu-id="1229f-239">The following example shows a simple implementation of [**IContextMenu::QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) that inserts a single command.</span></span> <span data-ttu-id="1229f-240">El desplazamiento de identificador del comando es la visualización de IDM \_ , que se establece en cero.</span><span class="sxs-lookup"><span data-stu-id="1229f-240">The identifier offset for the command is IDM\_DISPLAY, which is set to zero.</span></span> <span data-ttu-id="1229f-241">Las variables **m \_ pszVerb** y **m \_ pwszVerb** son variables privadas que se usan para almacenar la cadena de verbo independiente del lenguaje asociada en los formatos ANSI y Unicode.</span><span class="sxs-lookup"><span data-stu-id="1229f-241">The **m\_pszVerb** and **m\_pwszVerb** variables are private variables used to store the associated language-independent verb string in both ANSI and Unicode formats.</span></span>


```C++
#define IDM_DISPLAY 0

STDMETHODIMP CMenuExtension::QueryContextMenu(HMENU hMenu,
                                              UINT indexMenu,
                                              UINT idCmdFirst,
                                              UINT idCmdLast,
                                              UINT uFlags)
{
    HRESULT hr;
    
    if(!(CMF_DEFAULTONLY & uFlags))
    {
        InsertMenu(hMenu, 
                   indexMenu, 
                   MF_STRING | MF_BYPOSITION, 
                   idCmdFirst + IDM_DISPLAY, 
                   "&Display File Name");

    
        
        hr = StringCbCopyA(m_pszVerb, sizeof(m_pszVerb), "display");
        hr = StringCbCopyW(m_pwszVerb, sizeof(m_pwszVerb), L"display");

        return MAKE_HRESULT(SEVERITY_SUCCESS, 0, USHORT(IDM_DISPLAY + 1));
    }

    return MAKE_HRESULT(SEVERITY_SUCCESS, 0, USHORT(0));
}
```



<span data-ttu-id="1229f-242">Para otras tareas de implementación de verbos, vea [crear controladores de menús contextuales](context-menu-handlers.md).</span><span class="sxs-lookup"><span data-stu-id="1229f-242">For other verb implementation tasks, see [Creating Context Menu Handlers](context-menu-handlers.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="1229f-243">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="1229f-243">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1229f-244">Menús contextuales y controladores de menú contextual</span><span class="sxs-lookup"><span data-stu-id="1229f-244">Shortcut (Context) Menus and Shortcut Menu Handlers</span></span>](context-menu.md)
</dt> <dt>

[<span data-ttu-id="1229f-245">Verbos y asociaciones de archivo</span><span class="sxs-lookup"><span data-stu-id="1229f-245">Verbs and File Associations</span></span>](fa-verbs.md)
</dt> <dt>

[<span data-ttu-id="1229f-246">Elegir un verbo estático o dinámico para el menú contextual</span><span class="sxs-lookup"><span data-stu-id="1229f-246">Choosing a Static or Dynamic Verb for your Shortcut Menu</span></span>](shortcut-choose-method.md)
</dt> <dt>

[<span data-ttu-id="1229f-247">Prácticas recomendadas para los controladores de menú contextual y varios verbos de selección</span><span class="sxs-lookup"><span data-stu-id="1229f-247">Best Practices for Shortcut Menu Handlers and Multiple Selection Verbs</span></span>](verbs-best-practices.md)
</dt> <dt>

[<span data-ttu-id="1229f-248">Crear controladores de menú contextual</span><span class="sxs-lookup"><span data-stu-id="1229f-248">Creating Shortcut Menu Handlers</span></span>](context-menu-handlers.md)
</dt> <dt>

[<span data-ttu-id="1229f-249">Referencia del menú contextual</span><span class="sxs-lookup"><span data-stu-id="1229f-249">Shortcut Menu Reference</span></span>](context-menu-reference.md)
</dt> </dl>

 

 
