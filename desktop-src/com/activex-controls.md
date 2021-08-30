---
title: Controles ActiveX
description: Controles ActiveX
ms.assetid: e491b66c-d6ba-4476-8413-7a9e41c05e8d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50ed15af27b97b1f21a3b82907c5e4adcb74b9b0f588bb79c21c4b968da61822
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120097085"
---
# <a name="activex-controls"></a>Controles ActiveX

ActiveX controla la tecnología se encuentra en una base que consta de COM, objetos conectables, documentos compuestos, páginas de propiedades, automatización OLE, persistencia de objetos y objetos de fuente e imagen proporcionados por el sistema. Como se resume a continuación, cada una de estas tecnologías principales desempeña un papel en los controles.

<dl> <dt>

<span id="COM"></span><span id="com"></span>Com
</dt> <dd>

Un control es básicamente un objeto COM que expone la interfaz [**IUnknown,**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) a través de la cual los clientes pueden obtener punteros a sus otras interfaces. Los controles pueden admitir licencias a través [**de IClassFactory2 y**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2) el registro propio. Consulte [El modelo de objetos componentes](the-component-object-model.md) para obtener más información sobre COM, licencias y registro propio.

</dd> <dt>

<span id="Connectable_objects"></span><span id="connectable_objects"></span><span id="CONNECTABLE_OBJECTS"></span>Objetos conectables
</dt> <dd>

Los controles pueden admitir interfaces salientes a través de objetos conectables para que el control pueda comunicarse con su cliente. Por ejemplo, una interfaz saliente puede desencadenar una acción en el cliente, puede notificar al cliente de algún cambio en el control o puede solicitar permiso al cliente antes de que el control tome alguna acción. Consulte [Eventos en OBJETOS COM y Connectable para](events-in-com-and-connectable-objects.md) obtener más información sobre cómo funcionan los objetos conectables.

</dd> <dt>

<span id="Uniform_data_transfer"></span><span id="uniform_data_transfer"></span><span id="UNIFORM_DATA_TRANSFER"></span>Transferencia uniforme de datos
</dt> <dd>

Los controles pueden admitir que se arrastren y se suban dentro de un contenedor con ayuda de su contenedor. Vea [**IOleInPlaceObjectWindowless::GetDropTarget**](/windows/desktop/api/OCIdl/nf-ocidl-ioleinplaceobjectwindowless-getdroptarget) para obtener más información sobre cómo arrastrar y colocar.

</dd> <dt>

<span id="Compound_documents"></span><span id="compound_documents"></span><span id="COMPOUND_DOCUMENTS"></span>Documentos compuestos
</dt> <dd>

Un control puede ser un objeto activo en su lugar que se puede incrustar en un cliente que lo contiene. Un usuario final activa el control para iniciar una acción en la aplicación contenedora. Consulte [Documentos compuestos](compound-documents.md) para obtener más información sobre la activación en contexto y otras interfaces de documentos compuestos.

</dd> <dt>

<span id="Property_pages"></span><span id="property_pages"></span><span id="PROPERTY_PAGES"></span>Páginas de propiedades
</dt> <dd>

Los controles pueden proporcionar páginas de propiedades para que los usuarios finales puedan ver y cambiar las propiedades del control. Vea [Páginas de propiedades y Hojas de propiedades](property-pages-and-property-sheets.md) para obtener más información sobre cómo funcionan las páginas de propiedades.

</dd> <dt>

<span id="OLE_automation"></span><span id="ole_automation"></span><span id="OLE_AUTOMATION"></span>Automatización OLE
</dt> <dd>

Los controles pueden proporcionar programación a través de la automatización OLE para que los clientes puedan aprovechar las características del control a través de un lenguaje de programación proporcionado por el cliente. Consulte la sección Automatización OLE para obtener más información sobre la automatización OLE.

</dd> <dt>

<span id="Persistent_storage"></span><span id="persistent_storage"></span><span id="PERSISTENT_STORAGE"></span>Almacenamiento persistente
</dt> <dd>

Un control puede implementar una o varias interfaces de persistencia para admitir la persistencia de su estado. El implementador del control debe decidir qué tipos de persistencia son más importantes e implementar las interfaces de persistencia adecuadas. El cliente decide qué interfaz prefiere usar. Vea [El modelo de objetos componentes](the-component-object-model.md) para obtener más información sobre todas las interfaces de persistencia.

</dd> <dt>

<span id="Font_and_picture_objects"></span><span id="font_and_picture_objects"></span><span id="FONT_AND_PICTURE_OBJECTS"></span>Objetos de fuente e imagen
</dt> <dd>

Los controles pueden usar estos objetos proporcionados por el sistema para proporcionar una representación visual de sí mismos dentro del cliente. El objeto de fuente implementa varias interfaces, como [**IFont**](/windows/desktop/api/OCIdl/nn-ocidl-ifont) e [**IFontDisp.**](/windows/win32/api/ocidl/nn-ocidl-ifontdisp) Se puede crear un objeto de fuente [**con OleCreateFontIndirect**](/windows/desktop/api/OleCtl/nf-olectl-olecreatefontindirect). El objeto picture también implementa varias interfaces, incluidas [**IPicture**](/windows/desktop/api/OCIdl/nn-ocidl-ipicture) [**e IPictureDisp.**](/windows/win32/api/ocidl/nn-ocidl-ipicturedisp) Un objeto de imagen se puede crear [**mediante OleCreatePictureIndirect**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepictureindirect) y se puede cargar desde una secuencia [**con OleLoadPicture**](/windows/desktop/api/OleCtl/nf-olectl-oleloadpicture).

</dd> </dl>

Es importante comprender que estas características se pueden usar en cualquier objeto OLE. No es necesario implementar un control para poder usar estas características. Además, la única interfaz necesaria en un control es IUnknown. Opcionalmente, el control admite otras interfaces en función de la necesidad de admitir las características relacionadas.

Además de estas características, las siguientes interfaces y funciones son específicas de la tecnología de controles: [**IOleControl,**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrol) [**IOleControlSite,**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrolsite) [**ISimpleFrameSite**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite)y [**OleTranslateColor.**](/windows/desktop/api/OleCtl/nf-olectl-oletranslatecolor) También son específicos de los controles un conjunto de estándares para las propiedades y los métodos que un control o un contenedor de controles pueden admitir.

> [!Note]  
> La biblioteca del OleAut32.dll contiene implementaciones de las funciones ([**OleCreatePropertyFrame**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepropertyframe), [**OleCreatePropertyFrameIndirect,**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepropertyframeindirect) [**OleCreateFontIndirect,**](/windows/desktop/api/OleCtl/nf-olectl-olecreatefontindirect) [**OleCreatePictureIndirect,**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepictureindirect) [**OleLoadPicture**](/windows/desktop/api/OleCtl/nf-olectl-oleloadpicture)y [**OleTranslateColor**](/windows/desktop/api/OleCtl/nf-olectl-oletranslatecolor)). Además, OleAut32.dll contiene las implementaciones de los objetos de fuente e imagen estándar, así como una biblioteca de tipos para todas las interfaces usadas con controles, así como las estructuras de datos y los tipos de datos adicionales.

 

Para obtener más información, vea los temas siguientes:

-   [ActiveX Arquitectura de controles](activex-controls-architecture.md)
-   [ActiveX Interfaces de controles](activex-controls-interfaces.md)
-   [Propiedades y métodos](properties-and-methods.md)
-   [Eventos de control](control-events.md)
-   [Representación visual](visual-representation.md)
-   [Control de teclado para controles](keyboard-handling-for-controls.md)
-   [Persistencia](persistence.md)
-   [Registro y licencias](registration-and-licensing.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[ActiveX Directrices para controlar y controlar contenedores](activex-control-and-control-container-guidelines.md)
</dt> </dl>

 

 