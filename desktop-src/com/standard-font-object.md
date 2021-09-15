---
title: Objeto de fuente estándar
description: Objeto de fuente estándar
ms.assetid: f9b54dc4-24d4-4eb7-b43f-c481d64e52df
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd0fbe2509dd85c1d15b40dc8008dba60d948b5c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127466612"
---
# <a name="standard-font-object"></a>Objeto de fuente estándar

La propiedad de fuente ambiente estándar proporcionada por el contenedor y la propiedad de fuente estándar proporcionada por el control proporcionan un objeto de fuente estándar. Es decir, estas fuentes estándar suministran un **puntero IDispatch** a un objeto de fuente estándar.

El objeto de fuente es una implementación proporcionada por el sistema de un conjunto de interfaces sobre la compatibilidad con fuentes GDI subyacente. Un objeto de fuente se crea a través de la función de API [**OleCreateFontIndirect dada**](/windows/desktop/api/OleCtl/nf-olectl-olecreatefontindirect) una [**estructura FONTDESC.**](/windows/win32/api/olectl/ns-olectl-fontdesc) El objeto font admite varias propiedades de lectura y escritura, así como métodos personalizados a través de su interfaz [**IFont**](/windows/desktop/api/OCIdl/nn-ocidl-ifont), y admite el mismo conjunto de propiedades (pero no los métodos) a través de una interfaz [**IFontDisp**](/windows/win32/api/ocidl/nn-ocidl-ifontdisp)de dispinterface. La interfaz dispinterface se usa para las propiedades de fuente mencionadas anteriormente. Las propiedades corresponden a los atributos de fuente GDI que se describen en la [**estructura LOGFONT.**](/windows/win32/api/dimm/ns-dimm-logfonta)

El objeto de fuente también admite la interfaz de salida [**IPropertyNotifySink**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertynotifysink) para que un cliente pueda determinar cuándo cambian las propiedades de fuente. Dado que el objeto de fuente admite al menos una interfaz saliente, también implementa [**IConnectionPointContainer**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpointcontainer) y un punto de conexión para **IPropertyNotifySink** para este propósito.

El objeto font proporciona una propiedad hFont que es un identificador Windows fuente que se ajusta a los demás atributos especificados para la fuente. El objeto de fuente retrasa la realización de esta fuente cuando sea posible, por lo que establecer consecutivamente dos propiedades en una fuente no hará que se haga una fuente intermedia. Además, como optimización, el objeto de fuente estándar mantiene una caché de identificadores de fuente. Dos objetos de fuente en el mismo proceso que tienen propiedades idénticas devolverán el mismo identificador de fuente. El objeto font puede quitar fuentes de esta caché a su voluntad, lo que presenta consideraciones especiales para los clientes que usan esta propiedad hFont. Consulte [**IFont::get \_ hFont para**](/windows/desktop/api/OCIdl/nf-ocidl-ifont-get_hfont) obtener más detalles.

El objeto de fuente también admite [**IPersistStream,**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream) de forma que puede guardarse y cargarse desde una instancia de [**IStream.**](/windows/desktop/api/objidl/nn-objidl-istream) Cualquier otro objeto que use un objeto de fuente internamente normalmente guardaría y cargaría la fuente como parte del propio control de persistencia del objeto.

Además, el objeto font admite [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) a través del cual proporciona un conjunto de propiedades que contiene valores con tipo para cada propiedad de fuente.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Propiedades del control](control-properties.md)
</dt> </dl>

 

 