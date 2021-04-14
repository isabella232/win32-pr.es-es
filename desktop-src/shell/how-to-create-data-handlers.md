---
description: Extender el Portapapeles con controladores de formato de datos personalizados.
title: Cómo crear controladores de datos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33ecc08769068d975c1fa16ef1385f362c67e43c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997709"
---
# <a name="how-to-create-data-handlers"></a><span data-ttu-id="12df8-103">Cómo crear controladores de datos</span><span class="sxs-lookup"><span data-stu-id="12df8-103">How to Create Data Handlers</span></span>

<span data-ttu-id="12df8-104">Cuando un archivo se copia en el portapapeles o se arrastra y se coloca, el shell crea un objeto de datos que admite diversos formatos estándar del [portapapeles](dragdrop.md).</span><span class="sxs-lookup"><span data-stu-id="12df8-104">When a file is copied to the clipboard or dragged and dropped, the Shell creates a data object that supports a variety of standard [clipboard formats](dragdrop.md).</span></span> <span data-ttu-id="12df8-105">En el caso de los archivos que son de un tipo de archivo específico, puede ampliar los formatos de Portapapeles disponibles implementando y registrando un *controlador de datos*.</span><span class="sxs-lookup"><span data-stu-id="12df8-105">For files that are of a specific file type, you can extend the available clipboard formats by implementing and registering a *data handler*.</span></span> <span data-ttu-id="12df8-106">Cuando se transfiere un archivo del tipo de archivo, el shell delega las llamadas a la interfaz [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) del objeto de datos al controlador de datos si se usa uno de los formatos personalizados.</span><span class="sxs-lookup"><span data-stu-id="12df8-106">When a file of the file type is transferred, the Shell delegates calls to the data object's [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) interface to the data handler if one of the custom formats is used.</span></span>

<span data-ttu-id="12df8-107">Los procedimientos generales para implementar y registrar un controlador de extensión de Shell se explican en [crear controladores de extensión de Shell](handlers.md).</span><span class="sxs-lookup"><span data-stu-id="12df8-107">The general procedures for implementing and registering a Shell extension handler are discussed in [Creating Shell Extension Handlers](handlers.md).</span></span> <span data-ttu-id="12df8-108">Este documento se centra en los aspectos de la implementación que son específicos de los controladores de datos.</span><span class="sxs-lookup"><span data-stu-id="12df8-108">This document focuses on those aspects of implementation that are specific to data handlers.</span></span>

-   [<span data-ttu-id="12df8-109">Implementar controladores de datos</span><span class="sxs-lookup"><span data-stu-id="12df8-109">Implementing Data Handlers</span></span>](#step-1-implementing-data-handlers)
-   [<span data-ttu-id="12df8-110">Registrar controladores de datos</span><span class="sxs-lookup"><span data-stu-id="12df8-110">Registering Data Handlers</span></span>](#step-2-registering-data-handlers)
-   [<span data-ttu-id="12df8-111">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="12df8-111">Related topics</span></span>](#related-topics)

## <a name="instructions"></a><span data-ttu-id="12df8-112">Instrucciones</span><span class="sxs-lookup"><span data-stu-id="12df8-112">Instructions</span></span>

### <a name="step-1-implementing-data-handlers"></a><span data-ttu-id="12df8-113">Paso 1: implementación de controladores de datos</span><span class="sxs-lookup"><span data-stu-id="12df8-113">Step 1: Implementing Data Handlers</span></span>

<span data-ttu-id="12df8-114">Al igual que todos los controladores de extensión de Shell, los controladores de datos son objetos del modelo de objetos componentes (COM) en proceso implementados como archivos dll.</span><span class="sxs-lookup"><span data-stu-id="12df8-114">Like all Shell extension handlers, data handlers are in-process Component Object Model (COM) objects implemented as DLLs.</span></span> <span data-ttu-id="12df8-115">Exportan dos interfaces además de [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown): [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) y [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject).</span><span class="sxs-lookup"><span data-stu-id="12df8-115">They export two interfaces in addition to [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown): [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) and [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject).</span></span>

<span data-ttu-id="12df8-116">El shell inicializa el controlador a través de su interfaz [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) .</span><span class="sxs-lookup"><span data-stu-id="12df8-116">The Shell initializes the handler through its [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) interface.</span></span> <span data-ttu-id="12df8-117">Utiliza esta interfaz para solicitar el identificador de clase (CLSID) del controlador y proporciona el nombre del archivo.</span><span class="sxs-lookup"><span data-stu-id="12df8-117">It uses this interface to request the handler's class identifier (CLSID) and provides it with the file's name.</span></span> <span data-ttu-id="12df8-118">Para obtener información general sobre cómo implementar controladores de extensión de Shell, incluida la interfaz **IPersistFile** , vea [crear controladores de extensión de Shell](handlers.md).</span><span class="sxs-lookup"><span data-stu-id="12df8-118">For a general discussion of how to implement Shell extension handlers, including the **IPersistFile** interface, see [Creating Shell Extension Handlers](handlers.md).</span></span>

<span data-ttu-id="12df8-119">Una vez inicializado el controlador de datos, el shell delega las llamadas desde el objeto de datos a la interfaz [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) del controlador si se usa uno de los formatos personalizados.</span><span class="sxs-lookup"><span data-stu-id="12df8-119">Once the data handler is initialized, the Shell delegates calls from the data object to the handler's [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) interface if one of the custom formats is used.</span></span>

### <a name="step-2-registering-data-handlers"></a><span data-ttu-id="12df8-120">Paso 2: registrar controladores de datos</span><span class="sxs-lookup"><span data-stu-id="12df8-120">Step 2: Registering Data Handlers</span></span>

<span data-ttu-id="12df8-121">Los controladores de datos se registran en la subclave *ProgID* del tipo de archivo, como se muestra aquí: **HKEY \_ classes \_ root** \\ *ProgID* \\ **shellex** \\  .</span><span class="sxs-lookup"><span data-stu-id="12df8-121">Data handlers are registered under the file type's *ProgID* subkey as shown here: **HKEY\_CLASSES\_ROOT**\\*ProgID*\\**shellex**\\**DataHandler**</span></span>

<span data-ttu-id="12df8-122">Cree una subclave denominada para el controlador en el **identificador** de objeto y establezca el valor predeterminado de la subclave de ese controlador en la forma de cadena del GUID de CLSID del controlador.</span><span class="sxs-lookup"><span data-stu-id="12df8-122">Create a subkey named for the handler under **DataHandler** and set the default value of that handler's subkey to the string form of the handler's CLSID GUID.</span></span> <span data-ttu-id="12df8-123">Para obtener información general sobre cómo registrar controladores de extensión de Shell, vea [crear controladores de extensión de Shell](handlers.md).</span><span class="sxs-lookup"><span data-stu-id="12df8-123">For a general discussion of how to register Shell extension handlers, see [Creating Shell Extension Handlers](handlers.md).</span></span>

<span data-ttu-id="12df8-124">En el ejemplo siguiente se muestran las entradas del registro que habilitan un controlador de datos para un tipo de archivo. MYP de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="12df8-124">The following example illustrates registry entries that enable a data handler for an example .myp file type.</span></span>

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
      Shellex
         DataHandler
            (Default) = {00000000-1111-2222-3333-444444444444}
```

## <a name="related-topics"></a><span data-ttu-id="12df8-125">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="12df8-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="12df8-126">Creación de controladores de extensiones de shell</span><span class="sxs-lookup"><span data-stu-id="12df8-126">Creating Shell Extension Handlers</span></span>](handlers.md)
</dt> <dt>

[<span data-ttu-id="12df8-127">**IPersistFile**</span><span class="sxs-lookup"><span data-stu-id="12df8-127">**IPersistFile**</span></span>](/windows/win32/api/objidl/nn-objidl-ipersistfile)
</dt> <dt>

[<span data-ttu-id="12df8-128">**IDataObject**</span><span class="sxs-lookup"><span data-stu-id="12df8-128">**IDataObject**</span></span>](/windows/win32/api/objidl/nn-objidl-idataobject)
</dt> </dl>

 

 
