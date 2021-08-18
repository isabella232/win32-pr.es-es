---
title: Interfaces de documentos compuestos
description: Interfaces de documentos compuestos
ms.assetid: 3192ee58-55fd-43cb-b7d5-7270e91b8131
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e146bf26ef8d0c5c2fc189255389982a7e737a0556343cb095217c55ff8d712
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119410515"
---
# <a name="compound-document-interfaces"></a>Interfaces de documentos compuestos

En las tablas siguientes se muestran las interfaces implementadas por contenedores OLE, servidores OLE y objetos de documento compuestos. Las interfaces necesarias deben implementarse en los componentes para los que se enumeran. Todas las demás características son opcionales. Sin embargo, si desea incluir una característica determinada en la aplicación, debe implementar las interfaces que se muestran para esa característica en la tabla siguiente. Todas las demás interfaces solo son necesarias si se incluye una característica determinada.

En la tabla siguiente se enumeran los comportamientos obligatorios y opcionales de los contenedores OLE y las interfaces que debe implementar para cada uno de ellos.



| Comportamiento                               | Interfaces                                                                                                                                                              |
|----------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Comportamientos necesarios<br/>          | [**IOleClientSite**](/windows/desktop/api/OleIdl/nn-oleidl-ioleclientsite)<br/> [**IAdviseSink**](/windows/desktop/api/ObjIdl/nn-objidl-iadvisesink)<br/>                                                                       |
| Filtrado de mensajes<br/>           | [**IMessageFilter**](/windows/desktop/api/ObjIdl/nn-objidl-imessagefilter)<br/>                                                                                                                     |
| Vinculación<br/>                     | ninguno<br/>                                                                                                                                                         |
| Vinculación a objetos incrustados<br/> | [**IOleItemContainer**](/windows/desktop/api/OleIdl/nn-oleidl-ioleitemcontainer)<br/> [**IPersistFile**](/windows/desktop/api/ObjIdl/nn-objidl-ipersistfile)<br/> [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory)<br/>             |
| Activación en contexto<br/>         | [**IOleInPlaceSite**](/windows/desktop/api/OleIdl/nn-oleidl-ioleinplacesite)<br/> [**IOleInPlaceFrame**](/windows/desktop/api/OleIdl/nn-oleidl-ioleinplaceframe)<br/> [**IOleInPlaceObject**](/windows/desktop/api/OleIdl/nn-oleidl-ioleinplaceobject)<br/> |
| Arrastrar y colocar<br/>               | [**IDropSource**](/windows/desktop/api/OleIdl/nn-oleidl-idropsource)<br/> [**IDropTarget**](/windows/desktop/api/OleIdl/nn-oleidl-idroptarget)<br/> [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject)<br/>                               |



 

En la tabla siguiente se enumeran los comportamientos obligatorios y opcionales para los servidores OLE y sus objetos de documento compuestos y qué interfaces debe implementar para cada uno de ellos. La tabla distingue los servidores OLE y sus objetos para aclarar qué componente implementa qué interfaces. En la tabla también se anotan los distintos requisitos de los objetos proporcionados por los servidores fuera de proceso frente a los servidores en proceso.



| Característica                        | OLE Server                                                                                                                                | Objeto (fuera de proceso)                                                                                                                         | Objeto (en proceso)                                                                                                                                                                                                                         |
|--------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Comportamientos necesarios             | [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory)<br/>                                                                                         | [**IOleObject**](/windows/desktop/api/OleIdl/nn-oleidl-ioleobject)<br/> [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject)<br/> [**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage)<br/> | [**IOleObject**](/windows/desktop/api/OleIdl/nn-oleidl-ioleobject)<br/> [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject)<br/> [**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage)<br/> [**IViewObject2**](/windows/desktop/api/OleIdl/nn-oleidl-iviewobject2)<br/> [**IOleCache2**](/windows/desktop/api/OleIdl/nn-oleidl-iolecache2)<br/> |
| Filtrado de mensajes<br/>   | [**IMessageFilter**](/windows/desktop/api/ObjIdl/nn-objidl-imessagefilter)<br/>                                                                                       |                                                                                                                                                 |                                                                                                                                                                                                                                             |
| Vinculación<br/>             | [**IOleItemContainer**](/windows/desktop/api/OleIdl/nn-oleidl-ioleitemcontainer)<br/> [**IPersistFile**](/windows/desktop/api/ObjIdl/nn-objidl-ipersistfile)<br/>                                 |                                                                                                                                                 | [**IOleLink**](/windows/desktop/api/OleIdl/nn-oleidl-iolelink)<br/> [**IExternalConnection**](/windows/win32/api/objidlbase/nn-objidlbase-iexternalconnection)<br/>                                                                                                                                       |
| Activación en contexto<br/> |                                                                                                                                           | [**IOleInPlaceObject**](/windows/desktop/api/OleIdl/nn-oleidl-ioleinplaceobject)<br/> [**IOleInPlaceActiveObject**](/windows/desktop/api/OleIdl/nn-oleidl-ioleinplaceactiveobject)<br/>                 | [**IOleInPlaceObject**](/windows/desktop/api/OleIdl/nn-oleidl-ioleinplaceobject)<br/> [**IOleInPlaceActiveObject**](/windows/desktop/api/OleIdl/nn-oleidl-ioleinplaceactiveobject)<br/>                                                                                                             |
| Arrastrar y colocar<br/>       | [**IDropSource**](/windows/desktop/api/OleIdl/nn-oleidl-idropsource)<br/> [**IDropTarget**](/windows/desktop/api/OleIdl/nn-oleidl-idroptarget)<br/> [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject)<br/> |                                                                                                                                                 |                                                                                                                                                                                                                                             |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Documentos compuestos](compound-documents.md)
</dt> </dl>

 

