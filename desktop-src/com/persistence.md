---
title: Persistencia
description: Persistencia
ms.assetid: 4916ea52-a21c-4938-81cb-392b5ca1f6c1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3c8600307bfe6c29f72fb9d29e633358062c4e8c1c61da8898173cf190f1d08
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119500335"
---
# <a name="persistence"></a>Persistencia

Un control implementa una o varias interfaces de persistencia para admitir la persistencia de su estado. Por ejemplo, la [**interfaz IPersistStreamInit**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit) admite la persistencia basada en secuencias del estado del control. **IPersistStreamInit es** un sustituto de [**IPersistStream y**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream) agrega un método de inicialización, [**InitNew.**](/windows/desktop/api/OCIdl/nf-ocidl-ipersiststreaminit-initnew) Los otros métodos son los mismos en ambas interfaces. **IPersistStreamInit** no se deriva de **IPersistStream**; Un objeto solo admite una de las dos interfaces en función de si requiere la capacidad de inicializar nuevas instancias de sí mismo.

Otras interfaces de persistencia que un control puede ofrecer son: [**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage), [**IPersistMemory,**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768210(v=vs.85)) [**IPersistPropertyBag**](/windows/win32/api/ocidl/nn-ocidl-ipersistpropertybag), [**IPersistMoniker**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775042(v=vs.85)). El implementador del control debe decidir qué tipos de persistencia son más importantes e implementar las interfaces de persistencia adecuadas. El implementador del control también decide qué guardar. Por ejemplo, un control puede guardar los valores actuales de sus propiedades o su ubicación y tamaño dentro de su contenedor. El cliente decide qué interfaz prefiere usar.

Antes de cargar un control desde su estado persistente, un cliente puede comprobar la marca OLEMISC SETCLIENTSITEFIRST para determinar si el control admite la obtención de sus propiedades de sitio cliente y ambiente antes de cargar su \_ estado persistente. Esta optimización puede ahorrar tiempo al crear instancias de un control, ya que el control puede omitir sus valores persistentes en lugar de cargarlos solo para que se invaliden por las propiedades de ambiente proporcionadas por el cliente.

Un control también puede admitir guardar y restaurar su estado en un conjunto de propiedades OLE, un conjunto de identificadores y valores en un formato especificado. Esta característica puede ser útil con contenedores como Visual Basic, que guarda sus programas en un formato textual. Un control que desea admitir esta característica implementa [**IDataObject::GetData**](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-getdata) e [**IDataObject::SetData**](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-setdata) para pasar sus valores de propiedad hacia y desde el contenedor, respectivamente. Es el trabajo del contenedor convertir esta información en texto y guardarla. Los identificadores utilizados por el control corresponden a los nombres de propiedad y los valores del control. Vea OLE CDK para obtener la definición de este conjunto de propiedades.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Controles ActiveX](activex-controls.md)
</dt> </dl>

 

 