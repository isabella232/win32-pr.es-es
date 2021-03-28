---
description: Puede usar una extensión de espacio de nombres para permitir que los usuarios examinen el contenido de un archivo en lugar de que se muestre como una carpeta. Las extensiones de este orden se suelen usar para mostrar el contenido de los miembros de un tipo de archivo.
title: Cómo mostrar una vista raíz de un archivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30ee16f3ce50cd79800dd98aa53256591d1f79d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909546"
---
# <a name="how-to-display-a-rooted-view-of-a-file"></a><span data-ttu-id="6d75b-104">Cómo mostrar una vista raíz de un archivo</span><span class="sxs-lookup"><span data-stu-id="6d75b-104">How to Display a Rooted View of a File</span></span>

<span data-ttu-id="6d75b-105">Puede usar una extensión de espacio de nombres para permitir que los usuarios examinen el contenido de un archivo en lugar de que se muestre como una carpeta.</span><span class="sxs-lookup"><span data-stu-id="6d75b-105">You can use a namespace extension to allow users to browse the contents of a file rather than have it presented as a folder.</span></span> <span data-ttu-id="6d75b-106">Las extensiones de este orden se suelen usar para mostrar el contenido de los miembros de un [tipo de archivo](fa-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="6d75b-106">Extensions of this sort are typically used to display the contents of the members of a [file type](fa-file-types.md).</span></span> <span data-ttu-id="6d75b-107">Por ejemplo, los miembros de un tipo de archivo pueden contener varios archivos o imágenes comprimidos, organizados en una jerarquía.</span><span class="sxs-lookup"><span data-stu-id="6d75b-107">For instance, the members of a file type might contain multiple compressed files or images, organized in a hierarchy.</span></span> <span data-ttu-id="6d75b-108">En lugar de escribir una aplicación para permitir al usuario ver el contenido de este tipo de archivo, en su lugar, puede escribir una extensión de espacio de nombres y dejar que el explorador de Windows controle la pantalla.</span><span class="sxs-lookup"><span data-stu-id="6d75b-108">Rather than write an application to allow the user to view the contents of such a file, you can instead write a namespace extension and let Windows Explorer handle the display.</span></span>

<span data-ttu-id="6d75b-109">Debe usar una vista con raíz para que una extensión muestre el contenido de un archivo.</span><span class="sxs-lookup"><span data-stu-id="6d75b-109">You must use a rooted view in order to have an extension display the contents of a file.</span></span> <span data-ttu-id="6d75b-110">La forma más común de proporcionar una vista raíz de los miembros de un tipo de archivo es definir un [verbo de menú contextual](context.md) que inicie una instancia de Explorer.exe.</span><span class="sxs-lookup"><span data-stu-id="6d75b-110">The most common way to provide a rooted view of the members of a file type is to define a [shortcut menu verb](context.md) that launches an instance of Explorer.exe.</span></span> <span data-ttu-id="6d75b-111">Al hacer que este verbo sea el verbo predeterminado, al hacer doble clic también se abrirá una vista raíz del archivo.</span><span class="sxs-lookup"><span data-stu-id="6d75b-111">By making this verb the default verb, a double-click will also open a rooted view of the file.</span></span> <span data-ttu-id="6d75b-112">Puede definir un verbo para todos los miembros del tipo de archivo [modificando el registro](context.md)o definir de forma dinámica los verbos cada archivo implementando un [controlador de menú contextual](context-menu-handlers.md).</span><span class="sxs-lookup"><span data-stu-id="6d75b-112">You can either define a verb for all members of the file type by [modifying the registry](context.md), or dynamically define verbs on a file-by-file basis by implementing a [shortcut menu handler](context-menu-handlers.md).</span></span>

## <a name="instructions"></a><span data-ttu-id="6d75b-113">Instrucciones</span><span class="sxs-lookup"><span data-stu-id="6d75b-113">Instructions</span></span>


<span data-ttu-id="6d75b-114">En el ejemplo siguiente se muestra cómo utilizar el registro para proporcionar una vista con raíz de los miembros de un tipo de archivo modificando el registro.</span><span class="sxs-lookup"><span data-stu-id="6d75b-114">The following example illustrates how to use the registry to provide a rooted view of the members of a file type by modifying the registry.</span></span> <span data-ttu-id="6d75b-115">La entrada del registro de ejemplo es una modificación de uno de los ejemplos de extensión de los [menús contextuales](context.md).</span><span class="sxs-lookup"><span data-stu-id="6d75b-115">The sample registry entry is a modification of one of the examples in [Extending Shortcut Menus](context.md).</span></span> <span data-ttu-id="6d75b-116">Las entradas del registro definen archivos con una extensión de nombre de archivo. MYP como un tipo de archivo y usan el verbo **examinar** para iniciar una vista con raíz de los miembros de ese tipo.</span><span class="sxs-lookup"><span data-stu-id="6d75b-116">The registry entries define files with an .myp file name extension as a file type, and use the **browse** verb to launch a rooted view of members of that type.</span></span>

```
HKEY_CLASSES_ROOT
   .myp
      (Default) = MyProgram.1
   MyProgram.1
      (Default) = MyProgram Application
      Shell
         (Default) = browse
         browse
            command
               (Default) = %SYSTEMROOT%\explorer.exe /e,/root,{Extension CLSID}, "%1"
```

<span data-ttu-id="6d75b-117">Puede usar el mismo verbo para iniciar mediante programación una vista raíz de un miembro del tipo de archivo mediante una llamada a la función [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) .</span><span class="sxs-lookup"><span data-stu-id="6d75b-117">You can use the same verb to programmatically launch a rooted view of a member of the file type by calling the [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) function.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6d75b-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6d75b-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6d75b-119">Especificar la ubicación de una extensión de espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="6d75b-119">Specifying a Namespace Extension's Location</span></span>](nse-junction.md)
</dt> <dt>

[<span data-ttu-id="6d75b-120">Cómo abrir una vista con raíz de un punto de unión a través del registro</span><span class="sxs-lookup"><span data-stu-id="6d75b-120">How to Open a Rooted View of a Junction Point Through the Registry</span></span>](how-to-use-a-junction-point-to-open-a-rooted-view.md)
</dt> <dt>

[<span data-ttu-id="6d75b-121">Cómo abrir una vista con raíz de un punto de unión a través de un archivo de acceso directo</span><span class="sxs-lookup"><span data-stu-id="6d75b-121">How to Open a Rooted View of a Junction Point Through a Shortcut File</span></span>](how-to-use-a-shortcut-file-to-open-a-rooted-view.md)
</dt> <dt>

[<span data-ttu-id="6d75b-122">**ShellExecute**</span><span class="sxs-lookup"><span data-stu-id="6d75b-122">**ShellExecute**</span></span>](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea)
</dt> </dl>

 

 



