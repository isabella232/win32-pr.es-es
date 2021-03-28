---
description: Cómo implementar y registrar un controlador de colocación.
title: Cómo crear controladores de colocación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 081b4349ba36a12670458a453b0622475d59d755
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276750"
---
# <a name="how-to-create-drop-handlers"></a><span data-ttu-id="c9659-103">Cómo crear controladores de colocación</span><span class="sxs-lookup"><span data-stu-id="c9659-103">How to Create Drop Handlers</span></span>

<span data-ttu-id="c9659-104">De forma predeterminada, los archivos no son destinos de colocación.</span><span class="sxs-lookup"><span data-stu-id="c9659-104">By default, files are not drop targets.</span></span> <span data-ttu-id="c9659-105">Puede convertir los miembros de un [tipo de archivo](fa-file-types.md) en destinos de colocación implementando y registrando un *controlador de colocación*.</span><span class="sxs-lookup"><span data-stu-id="c9659-105">You can make the members of a [file type](fa-file-types.md) into drop targets by implementing and registering a *drop handler*.</span></span>

<span data-ttu-id="c9659-106">Si se registra un controlador de colocación para un tipo de archivo, se llama a este método cada vez que se arrastra un objeto o se coloca en un miembro del tipo de archivo.</span><span class="sxs-lookup"><span data-stu-id="c9659-106">If a drop handler is registered for a file type, it is called whenever an object is dragged over or dropped on a member of the file type.</span></span> <span data-ttu-id="c9659-107">El shell administra la operación mediante una llamada a los métodos adecuados en la interfaz [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) del controlador.</span><span class="sxs-lookup"><span data-stu-id="c9659-107">The Shell manages the operation by calling the appropriate methods on the handler's [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) interface.</span></span>

<span data-ttu-id="c9659-108">Los procedimientos generales para implementar y registrar un controlador de extensión de Shell se explican en [crear controladores de extensión de Shell](handlers.md).</span><span class="sxs-lookup"><span data-stu-id="c9659-108">The general procedures for implementing and registering a Shell extension handler are discussed in [Creating Shell Extension Handlers](handlers.md).</span></span> <span data-ttu-id="c9659-109">Este documento se centra en los aspectos de implementación que son específicos de los controladores de destino.</span><span class="sxs-lookup"><span data-stu-id="c9659-109">This document focuses on those aspects of implementation that are specific to drop handlers.</span></span>

## <a name="instructions"></a><span data-ttu-id="c9659-110">Instrucciones</span><span class="sxs-lookup"><span data-stu-id="c9659-110">Instructions</span></span>

### <a name="step-1-implementing-drop-handlers"></a><span data-ttu-id="c9659-111">Paso 1: implementar controladores de colocación</span><span class="sxs-lookup"><span data-stu-id="c9659-111">Step 1: Implementing Drop Handlers</span></span>

<span data-ttu-id="c9659-112">Al igual que todos los controladores de extensión de Shell, los controladores de colocación son objetos de modelo de objetos componentes (COM) en proceso implementados como archivos dll.</span><span class="sxs-lookup"><span data-stu-id="c9659-112">Like all Shell extension handlers, drop handlers are in-process Component Object Model (COM) objects implemented as DLLs.</span></span> <span data-ttu-id="c9659-113">Exportan dos interfaces además de [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown): [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) y [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget).</span><span class="sxs-lookup"><span data-stu-id="c9659-113">They export two interfaces in addition to [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown): [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) and [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget).</span></span>

<span data-ttu-id="c9659-114">El shell inicializa el controlador a través de su interfaz [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) .</span><span class="sxs-lookup"><span data-stu-id="c9659-114">The Shell initializes the handler through its [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) interface.</span></span> <span data-ttu-id="c9659-115">Utiliza esta interfaz para solicitar el identificador de clase (CLSID) del controlador y proporciona el nombre del archivo.</span><span class="sxs-lookup"><span data-stu-id="c9659-115">It uses this interface to request the handler's class identifier (CLSID) and provides it with the file's name.</span></span> <span data-ttu-id="c9659-116">Para obtener información general sobre cómo implementar controladores de extensión de Shell, incluida la interfaz **IPersistFile** , vea [crear controladores de extensión de Shell](handlers.md).</span><span class="sxs-lookup"><span data-stu-id="c9659-116">For a general discussion of how to implement Shell extension handlers, including the **IPersistFile** interface, see [Creating Shell Extension Handlers](handlers.md).</span></span>

<span data-ttu-id="c9659-117">Una vez inicializado el controlador de colocación, el shell llama al método adecuado en la interfaz [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) del controlador.</span><span class="sxs-lookup"><span data-stu-id="c9659-117">Once the drop handler is initialized, the Shell calls the appropriate method on the handler's [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) interface.</span></span>

### <a name="step-2-registering-drop-handlers"></a><span data-ttu-id="c9659-118">Paso 2: registrar controladores de colocación</span><span class="sxs-lookup"><span data-stu-id="c9659-118">Step 2: Registering Drop Handlers</span></span>

<span data-ttu-id="c9659-119">Los controladores de colocación se registran en la subclave de este tipo de archivo.</span><span class="sxs-lookup"><span data-stu-id="c9659-119">Drop handlers are registered under this file type's subkey.</span></span>

```
HKEY_CLASSES_ROOT
   ProgID
      shellex
         DropHandler
```

<span data-ttu-id="c9659-120">Cree una subclave de **DropHandler** denominada para el controlador y establezca el valor predeterminado de la subclave en la forma de cadena del GUID de CLSID del controlador.</span><span class="sxs-lookup"><span data-stu-id="c9659-120">Create a subkey of **DropHandler** named for the handler, and set the subkey's default value to the string form of the handler's CLSID GUID.</span></span> <span data-ttu-id="c9659-121">Para obtener información general sobre cómo registrar controladores de extensión de Shell, vea [crear controladores de extensión de Shell](handlers.md).</span><span class="sxs-lookup"><span data-stu-id="c9659-121">For a general discussion of how to register Shell extension handlers, see [Creating Shell Extension Handlers](handlers.md).</span></span>

<span data-ttu-id="c9659-122">En el ejemplo siguiente se muestran las entradas del registro que habilitan un controlador de colocación para un tipo de archivo. MYP de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="c9659-122">The following example illustrates registry entries that enable a drop handler for an example .myp file type.</span></span>

```
HKEY_CLASSES_ROOT
   .myp
      (Default) = MyProgram.1
   CLSID
      {00000000-1111-2222-3333-444444444444}
         InProcServer32
            (Default) = C:\MyDir\MyCommand.dll
            ThreadingModel = Apartment
   MyProgram.1
      (Default) = MyProgram Application
      shellex
         DropHandler
            (Default) = {00000000-1111-2222-3333-444444444444}
```

## <a name="related-topics"></a><span data-ttu-id="c9659-123">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c9659-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c9659-124">Creación de controladores de extensiones de shell</span><span class="sxs-lookup"><span data-stu-id="c9659-124">Creating Shell Extension Handlers</span></span>](handlers.md)
</dt> <dt>

[<span data-ttu-id="c9659-125">**IDropTarget**</span><span class="sxs-lookup"><span data-stu-id="c9659-125">**IDropTarget**</span></span>](/windows/win32/api/oleidl/nn-oleidl-idroptarget)
</dt> <dt>

[<span data-ttu-id="c9659-126">**IPersistFile**</span><span class="sxs-lookup"><span data-stu-id="c9659-126">**IPersistFile**</span></span>](/windows/win32/api/objidl/nn-objidl-ipersistfile)
</dt> </dl>

 

 
