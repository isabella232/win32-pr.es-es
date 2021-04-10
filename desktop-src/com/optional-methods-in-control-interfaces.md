---
title: Métodos opcionales en interfaces de control
description: Métodos opcionales en interfaces de control
ms.assetid: a26f7078-9286-4b21-b924-4b03d3849909
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1409b1c8d22f85a48829c07155e03379fc79103c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994008"
---
# <a name="optional-methods-in-control-interfaces"></a>Métodos opcionales en interfaces de control

La implementación de una interfaz no implica necesariamente la implementación de todos los métodos de esa interfaz para hacer nada más que devolver E \_ NOTIMPL o S \_ correctos según corresponda. En la tabla siguiente se identifican los métodos de las interfaces enumeradas en el tema [qué compatibilidad con una interfaz significa](what-support-for-an-interface-means.md) que un control puede implementar de esta manera. Cualquier método que no aparezca aquí debe estar totalmente implementado si se admite la interfaz.



| IOleControl                                                                                                   | Comentarios                                                                       |
|---------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [**GetControlInfo**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-getcontrolinfo), [ **mnemotécnico**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-onmnemonic)<br/> | Obligatorio para los controles con teclas de tecla.<br/>                              |
| [**IOleControl:: OnAmbientPropertyChange**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-onambientpropertychange)<br/>                | Obligatorio para los controles que usan propiedades de ambiente.<br/>                 |
| [**IOleControl:: FreezeEvents**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-freezeevents)<br/>                                      | Vea [inmovilización de eventos](event-freezing.md)<br/>                            |
| IOleObject                                                                                                    |                                                                                |
| [**SetMoniker**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-setmoniker)<br/>                                                        | Obligatorio si el control no está marcado con OLEMISC \_ CANTLINKINSIDE<br/> |
| [**GetMoniker**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getmoniker)<br/>                                                        | Obligatorio si el control no está marcado con OLEMISC \_ CANTLINKINSIDE<br/> |
| [**InitFromData**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-initfromdata)<br/>                                                    | Opcionales<br/>                                                            |
| [**GetClipboardData**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getclipboarddata)<br/>                                            | Opcionales<br/>                                                            |
| [**SetExtent**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-setextent)<br/>                                                          | Obligatorio solo para contenido de DVASPECT \_<br/>                                |
| [**GetExtent**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getextent)<br/>                                                          | Obligatorio solo para contenido de DVASPECT \_<br/>                                |
| [**SetColorScheme**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-setcolorscheme)<br/>                                                | Opcionales<br/>                                                            |
| [**Doverb**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-doverb)<br/>                                                                | Vea la nota 1<br/>                                                          |
| IOleInPlaceObject                                                                                             |                                                                                |
| [**ContextSensitiveHelp**](/windows/desktop/api/OleIdl/nf-oleidl-iolewindow-contextsensitivehelp)<br/>                                    | Opcionales<br/>                                                            |
| [**ReactivateAndUndo**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceobject-reactivateandundo)<br/>                                   | Opcionales<br/>                                                            |
| IOleInPlaceActiveObject                                                                                       |                                                                                |
| [**ContextSensitiveHelp**](/windows/desktop/api/OleIdl/nf-oleidl-iolewindow-contextsensitivehelp)<br/>                                    | Opcionales<br/>                                                            |
| IViewObject2                                                                                                  |                                                                                |
| [**Inmovilizar**](/windows/desktop/api/OleIdl/nf-oleidl-iviewobject-freeze)<br/>                                                               | Opcionales<br/>                                                            |
| [**Liberar**](/windows/desktop/api/OleIdl/nf-oleidl-iviewobject-unfreeze)<br/>                                                           | Opcionales<br/>                                                            |
| [**GetColorSet**](/windows/desktop/api/OleIdl/nf-oleidl-iviewobject-getcolorset)<br/>                                                     | Opcionales<br/>                                                            |
| IPersistStream, IPersistStreamInit, IPersistMemory                                                            |                                                                                |
| [**GetSizeMax**](/windows/desktop/api/ObjIdl/nf-objidl-ipersiststream-getsizemax)<br/>                                                    | Consulte la nota 2.<br/>                                                          |



 

1.  Un control con páginas de propiedades debe admitir [**IOleObject::D overb**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-doverb) para las \_ propiedades OLEIVERB y los \_ verbos principales OLEIVERB. Un control que puede estar activo debe ser **compatible con doverb para** el \_ verbo OLEIVERB INPLACEACTIVATE. Un control que puede estar **activo en la** interfaz de usuario también debe admitir doverb para el verbo OLEIVERB \_ UIACTIVATE.
2.  Si un control admite [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream) o [**IPersistStreamInit**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit) y puede devolver un valor preciso, debe hacerlo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Controles](controls.md)
</dt> </dl>

 

 





