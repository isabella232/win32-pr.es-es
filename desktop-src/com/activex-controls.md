---
title: Controles ActiveX
description: Controles ActiveX
ms.assetid: e491b66c-d6ba-4476-8413-7a9e41c05e8d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b75aabfbf2b81b4a4d3a45a1868a6eebf6fd4e6
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104421437"
---
# <a name="activex-controls"></a><span data-ttu-id="f576c-103">Controles ActiveX</span><span class="sxs-lookup"><span data-stu-id="f576c-103">ActiveX Controls</span></span>

<span data-ttu-id="f576c-104">La tecnología de controles ActiveX se sitúa en una base compuesta por COM, objetos conectables, documentos compuestos, páginas de propiedades, automatización OLE, persistencia de objetos y objetos de fuente e imagen proporcionados por el sistema.</span><span class="sxs-lookup"><span data-stu-id="f576c-104">ActiveX controls technology rests on a foundation consisting of COM, connectable objects, compound documents, property pages, OLE automation, object persistence, and system-provided font and picture objects.</span></span> <span data-ttu-id="f576c-105">Como se resume a continuación, cada una de estas tecnologías principales desempeña un papel en los controles.</span><span class="sxs-lookup"><span data-stu-id="f576c-105">As summarized below, each of these core technologies plays a role in controls.</span></span>

<dl> <dt>

<span data-ttu-id="f576c-106"><span id="COM"></span><span id="com"></span>COM</span><span class="sxs-lookup"><span data-stu-id="f576c-106"><span id="COM"></span><span id="com"></span>COM</span></span>
</dt> <dd>

<span data-ttu-id="f576c-107">Un control es esencialmente un objeto COM que expone la interfaz [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) , a través de la cual los clientes pueden obtener punteros a sus otras interfaces.</span><span class="sxs-lookup"><span data-stu-id="f576c-107">A control is essentially a COM object that exposes the [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) interface, through which clients can obtain pointers to its other interfaces.</span></span> <span data-ttu-id="f576c-108">Los controles pueden admitir licencias a través de [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2) y el registro automático.</span><span class="sxs-lookup"><span data-stu-id="f576c-108">Controls can support licensing through [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2) and self-registration.</span></span> <span data-ttu-id="f576c-109">Vea [el modelo de objetos componentes](the-component-object-model.md) para obtener más información sobre com, licencias y registro automático.</span><span class="sxs-lookup"><span data-stu-id="f576c-109">See [The Component Object Model](the-component-object-model.md) for more information on COM, licensing, and self-registration.</span></span>

</dd> <dt>

<span data-ttu-id="f576c-110"><span id="Connectable_objects"></span><span id="connectable_objects"></span><span id="CONNECTABLE_OBJECTS"></span>Objetos conectables</span><span class="sxs-lookup"><span data-stu-id="f576c-110"><span id="Connectable_objects"></span><span id="connectable_objects"></span><span id="CONNECTABLE_OBJECTS"></span>Connectable objects</span></span>
</dt> <dd>

<span data-ttu-id="f576c-111">Los controles pueden admitir interfaces salientes a través de objetos conectables para que el control pueda comunicarse con su cliente.</span><span class="sxs-lookup"><span data-stu-id="f576c-111">Controls can support outgoing interfaces through connectable objects so that the control can communicate with its client.</span></span> <span data-ttu-id="f576c-112">Por ejemplo, una interfaz de salida puede desencadenar una acción en el cliente, puede notificar al cliente algún cambio en el control o puede solicitar permiso al cliente antes de que el control realice alguna acción.</span><span class="sxs-lookup"><span data-stu-id="f576c-112">For example, an outgoing interface can trigger an action in the client, can notify the client of some change in the control, or can request permission from the client before the control takes some action.</span></span> <span data-ttu-id="f576c-113">Vea [eventos en com y objetos conectables](events-in-com-and-connectable-objects.md) para obtener más información sobre cómo funcionan los objetos conectables.</span><span class="sxs-lookup"><span data-stu-id="f576c-113">See [Events in COM and Connectable Objects](events-in-com-and-connectable-objects.md) for more information on how connectable objects work.</span></span>

</dd> <dt>

<span data-ttu-id="f576c-114"><span id="Uniform_data_transfer"></span><span id="uniform_data_transfer"></span><span id="UNIFORM_DATA_TRANSFER"></span>Transferencia de datos uniforme</span><span class="sxs-lookup"><span data-stu-id="f576c-114"><span id="Uniform_data_transfer"></span><span id="uniform_data_transfer"></span><span id="UNIFORM_DATA_TRANSFER"></span>Uniform data transfer</span></span>
</dt> <dd>

<span data-ttu-id="f576c-115">Los controles pueden admitir arrastrarlos y colocarlos dentro de un contenedor con la ayuda de su contenedor.</span><span class="sxs-lookup"><span data-stu-id="f576c-115">Controls can support being dragged and dropped within a container with help from their container.</span></span> <span data-ttu-id="f576c-116">Vea [**IOleInPlaceObjectWindowless:: GetDropTarget**](/windows/desktop/api/OCIdl/nf-ocidl-ioleinplaceobjectwindowless-getdroptarget) para obtener más información sobre la función de arrastrar y colocar.</span><span class="sxs-lookup"><span data-stu-id="f576c-116">See [**IOleInPlaceObjectWindowless::GetDropTarget**](/windows/desktop/api/OCIdl/nf-ocidl-ioleinplaceobjectwindowless-getdroptarget) for more information on drag and drop.</span></span>

</dd> <dt>

<span data-ttu-id="f576c-117"><span id="Compound_documents"></span><span id="compound_documents"></span><span id="COMPOUND_DOCUMENTS"></span>Documentos compuestos</span><span class="sxs-lookup"><span data-stu-id="f576c-117"><span id="Compound_documents"></span><span id="compound_documents"></span><span id="COMPOUND_DOCUMENTS"></span>Compound documents</span></span>
</dt> <dd>

<span data-ttu-id="f576c-118">Un control puede ser un objeto activo en contexto que se puede incrustar en un cliente contenedor.</span><span class="sxs-lookup"><span data-stu-id="f576c-118">A control can be an in-place active object that can be embedded in a containing client.</span></span> <span data-ttu-id="f576c-119">Un usuario final activa el control para iniciar una acción en la aplicación contenedora.</span><span class="sxs-lookup"><span data-stu-id="f576c-119">An end-user activates the control to initiate an action in the container application.</span></span> <span data-ttu-id="f576c-120">Vea [documentos compuestos](compound-documents.md) para obtener más información sobre la activación en contexto y otras interfaces de documentos compuestos.</span><span class="sxs-lookup"><span data-stu-id="f576c-120">See [Compound Documents](compound-documents.md) for more information on in-place activation and other compound document interfaces.</span></span>

</dd> <dt>

<span data-ttu-id="f576c-121"><span id="Property_pages"></span><span id="property_pages"></span><span id="PROPERTY_PAGES"></span>Páginas de propiedades</span><span class="sxs-lookup"><span data-stu-id="f576c-121"><span id="Property_pages"></span><span id="property_pages"></span><span id="PROPERTY_PAGES"></span>Property pages</span></span>
</dt> <dd>

<span data-ttu-id="f576c-122">Los controles pueden proporcionar páginas de propiedades para que los usuarios finales puedan ver y cambiar las propiedades del control.</span><span class="sxs-lookup"><span data-stu-id="f576c-122">Controls can provide property pages so end users can view and change the control's properties.</span></span> <span data-ttu-id="f576c-123">Consulte [páginas de propiedades y hojas de propiedades](property-pages-and-property-sheets.md) para obtener más información sobre cómo funcionan las páginas de propiedades.</span><span class="sxs-lookup"><span data-stu-id="f576c-123">See [Property Pages and Property Sheets](property-pages-and-property-sheets.md) for more information on how property pages work.</span></span>

</dd> <dt>

<span data-ttu-id="f576c-124"><span id="OLE_automation"></span><span id="ole_automation"></span><span id="OLE_AUTOMATION"></span>Automatización OLE</span><span class="sxs-lookup"><span data-stu-id="f576c-124"><span id="OLE_automation"></span><span id="ole_automation"></span><span id="OLE_AUTOMATION"></span>OLE automation</span></span>
</dt> <dd>

<span data-ttu-id="f576c-125">Los controles pueden proporcionar programación a través de la automatización OLE para que los clientes puedan aprovechar las características del control a través de un lenguaje de programación proporcionado por el cliente.</span><span class="sxs-lookup"><span data-stu-id="f576c-125">Controls can provide programmability through OLE automation so clients can take advantage of the control's features through a programming language supplied by the client.</span></span> <span data-ttu-id="f576c-126">Consulte la sección OLE Automation para obtener más información sobre la automatización OLE.</span><span class="sxs-lookup"><span data-stu-id="f576c-126">See the OLE Automation section for more information on OLE automation.</span></span>

</dd> <dt>

<span data-ttu-id="f576c-127"><span id="Persistent_storage"></span><span id="persistent_storage"></span><span id="PERSISTENT_STORAGE"></span>Almacenamiento persistente</span><span class="sxs-lookup"><span data-stu-id="f576c-127"><span id="Persistent_storage"></span><span id="persistent_storage"></span><span id="PERSISTENT_STORAGE"></span>Persistent storage</span></span>
</dt> <dd>

<span data-ttu-id="f576c-128">Un control puede implementar una o varias interfaces de persistencia para admitir la persistencia de su estado.</span><span class="sxs-lookup"><span data-stu-id="f576c-128">A control can implement one or more of several persistence interfaces to support persistence of its state.</span></span> <span data-ttu-id="f576c-129">El implementador de controles debe decidir qué tipos de persistencia son más importantes e implementar las interfaces de persistencia apropiadas.</span><span class="sxs-lookup"><span data-stu-id="f576c-129">The control implementer must decide what kinds of persistence are most important and implement the appropriate persistence interfaces.</span></span> <span data-ttu-id="f576c-130">El cliente decide qué interfaz prefiere usar.</span><span class="sxs-lookup"><span data-stu-id="f576c-130">The client decides which interface it prefers to use.</span></span> <span data-ttu-id="f576c-131">Vea [el modelo de objetos componentes](the-component-object-model.md) para obtener más información sobre todas las interfaces de persistencia.</span><span class="sxs-lookup"><span data-stu-id="f576c-131">See [The Component Object Model](the-component-object-model.md) for more information on all the persistence interfaces.</span></span>

</dd> <dt>

<span data-ttu-id="f576c-132"><span id="Font_and_picture_objects"></span><span id="font_and_picture_objects"></span><span id="FONT_AND_PICTURE_OBJECTS"></span>Objetos de fuente e imagen</span><span class="sxs-lookup"><span data-stu-id="f576c-132"><span id="Font_and_picture_objects"></span><span id="font_and_picture_objects"></span><span id="FONT_AND_PICTURE_OBJECTS"></span>Font and picture objects</span></span>
</dt> <dd>

<span data-ttu-id="f576c-133">Los controles pueden utilizar estos objetos proporcionados por el sistema para proporcionar una representación visual de ellos mismos en el cliente.</span><span class="sxs-lookup"><span data-stu-id="f576c-133">Controls can use these system provided objects to provide a visual representation of themselves within the client.</span></span> <span data-ttu-id="f576c-134">El objeto Font implementa varias interfaces, entre las que se incluyen [**IFont**](/windows/desktop/api/OCIdl/nn-ocidl-ifont) y [**IFontDisp**](/windows/win32/api/ocidl/nn-ocidl-ifontdisp).</span><span class="sxs-lookup"><span data-stu-id="f576c-134">The font object implements several interfaces, including [**IFont**](/windows/desktop/api/OCIdl/nn-ocidl-ifont) and [**IFontDisp**](/windows/win32/api/ocidl/nn-ocidl-ifontdisp).</span></span> <span data-ttu-id="f576c-135">Se puede crear un objeto Font con [**OleCreateFontIndirect**](/windows/desktop/api/OleCtl/nf-olectl-olecreatefontindirect).</span><span class="sxs-lookup"><span data-stu-id="f576c-135">A font object can be created with [**OleCreateFontIndirect**](/windows/desktop/api/OleCtl/nf-olectl-olecreatefontindirect).</span></span> <span data-ttu-id="f576c-136">El objeto Picture también implementa varias interfaces, entre las que se incluyen [**IPicture**](/windows/desktop/api/OCIdl/nn-ocidl-ipicture) y [**IPictureDisp**](/windows/win32/api/ocidl/nn-ocidl-ipicturedisp).</span><span class="sxs-lookup"><span data-stu-id="f576c-136">The picture object also implements several interfaces, including [**IPicture**](/windows/desktop/api/OCIdl/nn-ocidl-ipicture) and [**IPictureDisp**](/windows/win32/api/ocidl/nn-ocidl-ipicturedisp).</span></span> <span data-ttu-id="f576c-137">Se puede crear un objeto de imagen mediante [**OleCreatePictureIndirect**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepictureindirect) y se puede cargar desde un flujo con [**OleLoadPicture**](/windows/desktop/api/OleCtl/nf-olectl-oleloadpicture).</span><span class="sxs-lookup"><span data-stu-id="f576c-137">A picture object can be created using [**OleCreatePictureIndirect**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepictureindirect) and can loaded from a stream with [**OleLoadPicture**](/windows/desktop/api/OleCtl/nf-olectl-oleloadpicture).</span></span>

</dd> </dl>

<span data-ttu-id="f576c-138">Es importante comprender que estas características se pueden utilizar en cualquier objeto OLE.</span><span class="sxs-lookup"><span data-stu-id="f576c-138">It is important to understand that these features can be used in any OLE object.</span></span> <span data-ttu-id="f576c-139">No es necesario implementar un control para utilizar estas características.</span><span class="sxs-lookup"><span data-stu-id="f576c-139">One does not need to implement a control in order to use these features.</span></span> <span data-ttu-id="f576c-140">Además, la única interfaz necesaria en un control es IUnknown.</span><span class="sxs-lookup"><span data-stu-id="f576c-140">Also, the only required interface on a control is IUnknown.</span></span> <span data-ttu-id="f576c-141">El control admite opcionalmente otras interfaces en función de la necesidad de admitir las características relacionadas.</span><span class="sxs-lookup"><span data-stu-id="f576c-141">The control optionally supports other interfaces based on the need to support the related features.</span></span>

<span data-ttu-id="f576c-142">Además de estas características, las siguientes interfaces y funciones son específicas de la tecnología de controles: [**IOleControl**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrol), [**IOleControlSite**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrolsite), [**ISimpleFrameSite**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite)y [**OleTranslateColor**](/windows/desktop/api/OleCtl/nf-olectl-oletranslatecolor).</span><span class="sxs-lookup"><span data-stu-id="f576c-142">In addition to these features, the following interfaces and functions are specific to controls technology: [**IOleControl**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrol), [**IOleControlSite**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrolsite), [**ISimpleFrameSite**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite), and [**OleTranslateColor**](/windows/desktop/api/OleCtl/nf-olectl-oletranslatecolor).</span></span> <span data-ttu-id="f576c-143">También son un conjunto de estándares para las propiedades y los métodos que un contenedor de control o control puede admitir.</span><span class="sxs-lookup"><span data-stu-id="f576c-143">Also specific to controls are a set of standards for properties and methods that a control or a control container can support.</span></span>

> [!Note]  
> <span data-ttu-id="f576c-144">La biblioteca del sistema OleAut32.dll contiene implementaciones de las funciones ([**OleCreatePropertyFrame**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepropertyframe), [**OleCreatePropertyFrameIndirect**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepropertyframeindirect), [**OleCreateFontIndirect**](/windows/desktop/api/OleCtl/nf-olectl-olecreatefontindirect), [**OleCreatePictureIndirect**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepictureindirect), [**OleLoadPicture**](/windows/desktop/api/OleCtl/nf-olectl-oleloadpicture)y [**OleTranslateColor**](/windows/desktop/api/OleCtl/nf-olectl-oletranslatecolor)).</span><span class="sxs-lookup"><span data-stu-id="f576c-144">The system library OleAut32.dll contains implementations of the functions ([**OleCreatePropertyFrame**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepropertyframe), [**OleCreatePropertyFrameIndirect**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepropertyframeindirect), [**OleCreateFontIndirect**](/windows/desktop/api/OleCtl/nf-olectl-olecreatefontindirect), [**OleCreatePictureIndirect**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepictureindirect), [**OleLoadPicture**](/windows/desktop/api/OleCtl/nf-olectl-oleloadpicture), and [**OleTranslateColor**](/windows/desktop/api/OleCtl/nf-olectl-oletranslatecolor)).</span></span> <span data-ttu-id="f576c-145">Además, OleAut32.dll contiene las implementaciones de los objetos de imagen y fuente estándar, así como una biblioteca de tipos para todas las interfaces utilizadas con controles, así como las estructuras de datos y los tipos de datos adicionales.</span><span class="sxs-lookup"><span data-stu-id="f576c-145">In addition, OleAut32.dll contains the implementations of the standard font and picture objects, as well as a type library for all the interfaces used with controls as well as the additional data structures and data types.</span></span>

 

<span data-ttu-id="f576c-146">Para obtener más información, vea los temas siguientes:</span><span class="sxs-lookup"><span data-stu-id="f576c-146">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="f576c-147">Arquitectura de controles ActiveX</span><span class="sxs-lookup"><span data-stu-id="f576c-147">ActiveX Controls Architecture</span></span>](activex-controls-architecture.md)
-   [<span data-ttu-id="f576c-148">Interfaces de controles ActiveX</span><span class="sxs-lookup"><span data-stu-id="f576c-148">ActiveX Controls Interfaces</span></span>](activex-controls-interfaces.md)
-   [<span data-ttu-id="f576c-149">Propiedades y métodos</span><span class="sxs-lookup"><span data-stu-id="f576c-149">Properties and Methods</span></span>](properties-and-methods.md)
-   [<span data-ttu-id="f576c-150">Eventos de control</span><span class="sxs-lookup"><span data-stu-id="f576c-150">Control Events</span></span>](control-events.md)
-   [<span data-ttu-id="f576c-151">Representación visual</span><span class="sxs-lookup"><span data-stu-id="f576c-151">Visual Representation</span></span>](visual-representation.md)
-   [<span data-ttu-id="f576c-152">Control de teclado para controles</span><span class="sxs-lookup"><span data-stu-id="f576c-152">Keyboard Handling for Controls</span></span>](keyboard-handling-for-controls.md)
-   [<span data-ttu-id="f576c-153">Persistencia</span><span class="sxs-lookup"><span data-stu-id="f576c-153">Persistence</span></span>](persistence.md)
-   [<span data-ttu-id="f576c-154">Registro y licencias</span><span class="sxs-lookup"><span data-stu-id="f576c-154">Registration and Licensing</span></span>](registration-and-licensing.md)

## <a name="related-topics"></a><span data-ttu-id="f576c-155">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f576c-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f576c-156">Directrices para el contenedor de controles y controles ActiveX</span><span class="sxs-lookup"><span data-stu-id="f576c-156">ActiveX Control and Control Container Guidelines</span></span>](activex-control-and-control-container-guidelines.md)
</dt> </dl>

 

 