---
title: Objeto de fuente estándar
description: Objeto de fuente estándar
ms.assetid: f9b54dc4-24d4-4eb7-b43f-c481d64e52df
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd0fbe2509dd85c1d15b40dc8008dba60d948b5c
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104078406"
---
# <a name="standard-font-object"></a>Objeto de fuente estándar

La propiedad de fuente ambiente estándar proporcionada por el contenedor y la propiedad de fuente estándar proporcionada por el control proporcionan un objeto de fuente estándar. Es decir, estas fuentes estándar proporcionan un puntero **IDispatch** a un objeto de fuente estándar.

El objeto Font es una implementación proporcionada por el sistema de un conjunto de interfaces sobre la compatibilidad con fuentes GDI subyacentes. Se crea un objeto de fuente a través de la función de API [**OleCreateFontIndirect**](/windows/desktop/api/OleCtl/nf-olectl-olecreatefontindirect) dada una estructura [**FONTDESC**](/windows/win32/api/olectl/ns-olectl-fontdesc) . El objeto Font admite varias propiedades de lectura y escritura, así como métodos personalizados a través de su interfaz [**IFont**](/windows/desktop/api/OCIdl/nn-ocidl-ifont), y admite el mismo conjunto de propiedades (pero no los métodos) a través de una interfaz dispinterface [**IFontDisp**](/windows/win32/api/ocidl/nn-ocidl-ifontdisp). La dispinterface se usa para las propiedades de fuente mencionadas previamente. Las propiedades corresponden a los atributos de fuente GDI que se describen en la estructura [**LOGFONT**](/windows/win32/api/dimm/ns-dimm-logfonta) .

El objeto Font también admite la interfaz de salida [**IPropertyNotifySink**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertynotifysink) para que un cliente pueda determinar cuándo cambian las propiedades de fuente. Puesto que el objeto de fuente admite al menos una interfaz de salida, también implementa [**IConnectionPointContainer**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpointcontainer) y un punto de conexión para **IPropertyNotifySink** con este fin.

El objeto Font proporciona una propiedad hFont que es un identificador de fuente de Windows que se ajusta a los demás atributos especificados para la fuente. El objeto de fuente retrasa la espera de esta fuente siempre que sea posible, por lo que establecer consecutivamente dos propiedades en una fuente no hará que se produzca una fuente intermedia. Además, como optimización, el objeto de fuente estándar mantiene una memoria caché de identificadores de fuente. Dos objetos Font en el mismo proceso que tienen propiedades idénticas devolverán el mismo identificador de fuente. El objeto Font puede quitar fuentes de esta caché en, lo que presenta consideraciones especiales para los clientes que usan esta propiedad hFont. Consulte [**IFont:: get \_ hFont**](/windows/desktop/api/OCIdl/nf-ocidl-ifont-get_hfont) para obtener más información.

El objeto Font también admite [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream) para que pueda guardarse y cargarse a sí mismo desde una instancia de [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream). Cualquier otro objeto que use internamente un objeto Font normalmente guardaría y cargaría la fuente como parte del control de persistencia propio del objeto.

Además, el objeto Font admite [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) a través de la cual proporciona un conjunto de propiedades que contiene valores con tipo para cada propiedad de fuente.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Propiedades del control](control-properties.md)
</dt> </dl>

 

 