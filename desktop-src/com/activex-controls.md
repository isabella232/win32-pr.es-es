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
# <a name="activex-controls"></a>Controles ActiveX

La tecnología de controles ActiveX se sitúa en una base compuesta por COM, objetos conectables, documentos compuestos, páginas de propiedades, automatización OLE, persistencia de objetos y objetos de fuente e imagen proporcionados por el sistema. Como se resume a continuación, cada una de estas tecnologías principales desempeña un papel en los controles.

<dl> <dt>

<span id="COM"></span><span id="com"></span>COM
</dt> <dd>

Un control es esencialmente un objeto COM que expone la interfaz [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) , a través de la cual los clientes pueden obtener punteros a sus otras interfaces. Los controles pueden admitir licencias a través de [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2) y el registro automático. Vea [el modelo de objetos componentes](the-component-object-model.md) para obtener más información sobre com, licencias y registro automático.

</dd> <dt>

<span id="Connectable_objects"></span><span id="connectable_objects"></span><span id="CONNECTABLE_OBJECTS"></span>Objetos conectables
</dt> <dd>

Los controles pueden admitir interfaces salientes a través de objetos conectables para que el control pueda comunicarse con su cliente. Por ejemplo, una interfaz de salida puede desencadenar una acción en el cliente, puede notificar al cliente algún cambio en el control o puede solicitar permiso al cliente antes de que el control realice alguna acción. Vea [eventos en com y objetos conectables](events-in-com-and-connectable-objects.md) para obtener más información sobre cómo funcionan los objetos conectables.

</dd> <dt>

<span id="Uniform_data_transfer"></span><span id="uniform_data_transfer"></span><span id="UNIFORM_DATA_TRANSFER"></span>Transferencia de datos uniforme
</dt> <dd>

Los controles pueden admitir arrastrarlos y colocarlos dentro de un contenedor con la ayuda de su contenedor. Vea [**IOleInPlaceObjectWindowless:: GetDropTarget**](/windows/desktop/api/OCIdl/nf-ocidl-ioleinplaceobjectwindowless-getdroptarget) para obtener más información sobre la función de arrastrar y colocar.

</dd> <dt>

<span id="Compound_documents"></span><span id="compound_documents"></span><span id="COMPOUND_DOCUMENTS"></span>Documentos compuestos
</dt> <dd>

Un control puede ser un objeto activo en contexto que se puede incrustar en un cliente contenedor. Un usuario final activa el control para iniciar una acción en la aplicación contenedora. Vea [documentos compuestos](compound-documents.md) para obtener más información sobre la activación en contexto y otras interfaces de documentos compuestos.

</dd> <dt>

<span id="Property_pages"></span><span id="property_pages"></span><span id="PROPERTY_PAGES"></span>Páginas de propiedades
</dt> <dd>

Los controles pueden proporcionar páginas de propiedades para que los usuarios finales puedan ver y cambiar las propiedades del control. Consulte [páginas de propiedades y hojas de propiedades](property-pages-and-property-sheets.md) para obtener más información sobre cómo funcionan las páginas de propiedades.

</dd> <dt>

<span id="OLE_automation"></span><span id="ole_automation"></span><span id="OLE_AUTOMATION"></span>Automatización OLE
</dt> <dd>

Los controles pueden proporcionar programación a través de la automatización OLE para que los clientes puedan aprovechar las características del control a través de un lenguaje de programación proporcionado por el cliente. Consulte la sección OLE Automation para obtener más información sobre la automatización OLE.

</dd> <dt>

<span id="Persistent_storage"></span><span id="persistent_storage"></span><span id="PERSISTENT_STORAGE"></span>Almacenamiento persistente
</dt> <dd>

Un control puede implementar una o varias interfaces de persistencia para admitir la persistencia de su estado. El implementador de controles debe decidir qué tipos de persistencia son más importantes e implementar las interfaces de persistencia apropiadas. El cliente decide qué interfaz prefiere usar. Vea [el modelo de objetos componentes](the-component-object-model.md) para obtener más información sobre todas las interfaces de persistencia.

</dd> <dt>

<span id="Font_and_picture_objects"></span><span id="font_and_picture_objects"></span><span id="FONT_AND_PICTURE_OBJECTS"></span>Objetos de fuente e imagen
</dt> <dd>

Los controles pueden utilizar estos objetos proporcionados por el sistema para proporcionar una representación visual de ellos mismos en el cliente. El objeto Font implementa varias interfaces, entre las que se incluyen [**IFont**](/windows/desktop/api/OCIdl/nn-ocidl-ifont) y [**IFontDisp**](/windows/win32/api/ocidl/nn-ocidl-ifontdisp). Se puede crear un objeto Font con [**OleCreateFontIndirect**](/windows/desktop/api/OleCtl/nf-olectl-olecreatefontindirect). El objeto Picture también implementa varias interfaces, entre las que se incluyen [**IPicture**](/windows/desktop/api/OCIdl/nn-ocidl-ipicture) y [**IPictureDisp**](/windows/win32/api/ocidl/nn-ocidl-ipicturedisp). Se puede crear un objeto de imagen mediante [**OleCreatePictureIndirect**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepictureindirect) y se puede cargar desde un flujo con [**OleLoadPicture**](/windows/desktop/api/OleCtl/nf-olectl-oleloadpicture).

</dd> </dl>

Es importante comprender que estas características se pueden utilizar en cualquier objeto OLE. No es necesario implementar un control para utilizar estas características. Además, la única interfaz necesaria en un control es IUnknown. El control admite opcionalmente otras interfaces en función de la necesidad de admitir las características relacionadas.

Además de estas características, las siguientes interfaces y funciones son específicas de la tecnología de controles: [**IOleControl**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrol), [**IOleControlSite**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrolsite), [**ISimpleFrameSite**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite)y [**OleTranslateColor**](/windows/desktop/api/OleCtl/nf-olectl-oletranslatecolor). También son un conjunto de estándares para las propiedades y los métodos que un contenedor de control o control puede admitir.

> [!Note]  
> La biblioteca del sistema OleAut32.dll contiene implementaciones de las funciones ([**OleCreatePropertyFrame**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepropertyframe), [**OleCreatePropertyFrameIndirect**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepropertyframeindirect), [**OleCreateFontIndirect**](/windows/desktop/api/OleCtl/nf-olectl-olecreatefontindirect), [**OleCreatePictureIndirect**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepictureindirect), [**OleLoadPicture**](/windows/desktop/api/OleCtl/nf-olectl-oleloadpicture)y [**OleTranslateColor**](/windows/desktop/api/OleCtl/nf-olectl-oletranslatecolor)). Además, OleAut32.dll contiene las implementaciones de los objetos de imagen y fuente estándar, así como una biblioteca de tipos para todas las interfaces utilizadas con controles, así como las estructuras de datos y los tipos de datos adicionales.

 

Para obtener más información, vea los temas siguientes:

-   [Arquitectura de controles ActiveX](activex-controls-architecture.md)
-   [Interfaces de controles ActiveX](activex-controls-interfaces.md)
-   [Propiedades y métodos](properties-and-methods.md)
-   [Eventos de control](control-events.md)
-   [Representación visual](visual-representation.md)
-   [Control de teclado para controles](keyboard-handling-for-controls.md)
-   [Persistencia](persistence.md)
-   [Registro y licencias](registration-and-licensing.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Directrices para el contenedor de controles y controles ActiveX](activex-control-and-control-container-guidelines.md)
</dt> </dl>

 

 