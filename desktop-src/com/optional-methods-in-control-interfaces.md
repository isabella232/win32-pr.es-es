---
title: Métodos opcionales en interfaces de control
description: Métodos opcionales en interfaces de control
ms.assetid: a26f7078-9286-4b21-b924-4b03d3849909
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e92303b9e4e6a5edd295d0895a9121eee70ea05ae2a8967a9346ea26b153e8b1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119859295"
---
# <a name="optional-methods-in-control-interfaces"></a>Métodos opcionales en interfaces de control

Implementar una interfaz no significa necesariamente implementar todos los métodos de esa interfaz para hacer algo más que devolver E NOTIMPL o \_ S OK según \_ corresponda. En la tabla siguiente se identifican los métodos de las interfaces enumeradas en el tema [What Support for an Interface Means](what-support-for-an-interface-means.md) que un control puede implementar de esta manera. Cualquier método que no aparezca aquí debe implementarse por completo si se admite la interfaz .



| IOleControl                                                                                                   | Comentarios                                                                       |
|---------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [**GetControlInfo**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-getcontrolinfo), [ **OnMnemonic**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-onmnemonic)<br/> | Obligatorio para los controles con mnemonics.<br/>                              |
| [**IOleControl::OnAmbientPropertyChange**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-onambientpropertychange)<br/>                | Obligatorio para los controles que usan propiedades ambientales.<br/>                 |
| [**IOleControl::FreezeEvents**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-freezeevents)<br/>                                      | Consulte [Event Freezing (Inmovilización de eventos)](event-freezing.md)<br/>                            |
| IOleObject                                                                                                    |                                                                                |
| [**SetMoniker**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-setmoniker)<br/>                                                        | Obligatorio si el control no está marcado con OLEMISC \_ CANTLINKINSIDE<br/> |
| [**GetMoniker**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getmoniker)<br/>                                                        | Obligatorio si el control no está marcado con OLEMISC \_ CANTLINKINSIDE<br/> |
| [**InitFromData**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-initfromdata)<br/>                                                    | Opcionales<br/>                                                            |
| [**GetClipboardData**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getclipboarddata)<br/>                                            | Opcionales<br/>                                                            |
| [**SetExtent**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-setextent)<br/>                                                          | Solo obligatorio para DVASPECT \_ CONTENT<br/>                                |
| [**GetExtent**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getextent)<br/>                                                          | Solo obligatorio para DVASPECT \_ CONTENT<br/>                                |
| [**SetColorScheme**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-setcolorscheme)<br/>                                                | Opcionales<br/>                                                            |
| [**DoVerb**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-doverb)<br/>                                                                | Vea la nota 1.<br/>                                                          |
| IOleInPlaceObject                                                                                             |                                                                                |
| [**ContextSensitiveHelp**](/windows/desktop/api/OleIdl/nf-oleidl-iolewindow-contextsensitivehelp)<br/>                                    | Opcionales<br/>                                                            |
| [**ReactivateAndUndo**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceobject-reactivateandundo)<br/>                                   | Opcionales<br/>                                                            |
| IOleInPlaceActiveObject                                                                                       |                                                                                |
| [**ContextSensitiveHelp**](/windows/desktop/api/OleIdl/nf-oleidl-iolewindow-contextsensitivehelp)<br/>                                    | Opcionales<br/>                                                            |
| IViewObject2                                                                                                  |                                                                                |
| [**Freeze**](/windows/desktop/api/OleIdl/nf-oleidl-iviewobject-freeze)<br/>                                                               | Opcionales<br/>                                                            |
| [**Descongelar**](/windows/desktop/api/OleIdl/nf-oleidl-iviewobject-unfreeze)<br/>                                                           | Opcionales<br/>                                                            |
| [**GetColorSet**](/windows/desktop/api/OleIdl/nf-oleidl-iviewobject-getcolorset)<br/>                                                     | Opcionales<br/>                                                            |
| IPersistStream, IPersistStreamInit, IPersistMemory                                                            |                                                                                |
| [**GetSizeMax**](/windows/desktop/api/ObjIdl/nf-objidl-ipersiststream-getsizemax)<br/>                                                    | Consulte la nota 2.<br/>                                                          |



 

1.  Un control con páginas de propiedades debe admitir [**IOleObject::D oVerb para**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-doverb) los verbos OLEIVERB PROPERTIES y \_ OLEIVERB \_ PRIMARY. Un control que pueda estar activo debe admitir **DoVerb para** el verbo \_ OLEIVERB INPLACEACTIVATE. Un control que pueda estar activo en la interfaz de usuario también debe admitir **DoVerb para** el verbo OLEIVERB \_ UIACTIVATE.
2.  Si un control admite [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream) o [**IPersistStreamInit**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit) y puede devolver un valor preciso, debe hacerlo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Controles](controls.md)
</dt> </dl>

 

 





