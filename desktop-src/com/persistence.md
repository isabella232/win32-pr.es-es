---
title: Persistencia
description: Persistencia
ms.assetid: 4916ea52-a21c-4938-81cb-392b5ca1f6c1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ba5fc0c8e389c7babdf80b76719b39fc02d5604
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104078466"
---
# <a name="persistence"></a>Persistencia

Un control implementa una o varias interfaces de persistencia para admitir la persistencia de su estado. Por ejemplo, la interfaz [**IPersistStreamInit**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit) admite la persistencia basada en secuencias del estado del control. **IPersistStreamInit** es un reemplazo de [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream) y agrega un método de inicialización, [**InitNew**](/windows/desktop/api/OCIdl/nf-ocidl-ipersiststreaminit-initnew). Los otros métodos son los mismos en ambas interfaces. **IPersistStreamInit** no se deriva de **IPersistStream**; un objeto solo admite una de las dos interfaces en función de si requiere la capacidad de inicializar nuevas instancias de sí mismo.

Otras interfaces de persistencia que un control puede ofrecer incluyen: [**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage), [**IPersistMemory**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768210(v=vs.85)), [**IPersistPropertyBag**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768205(v=vs.85)), [**IPersistMoniker**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775042(v=vs.85)). El implementador de controles debe decidir qué tipos de persistencia son más importantes e implementar las interfaces de persistencia apropiadas. El implementador de controles también decide lo que se debe guardar. Por ejemplo, un control puede guardar los valores actuales de sus propiedades o su ubicación y tamaño dentro de su contenedor. El cliente decide qué interfaz prefiere usar.

Antes de cargar un control desde su estado persistente, un cliente puede comprobar la \_ marca OLEMISC SETCLIENTSITEFIRST para determinar si el control admite la obtención de sus propiedades de ambiente y sitio de cliente antes de cargar su estado persistente. Esta optimización puede ahorrar tiempo al crear una instancia de un control, ya que el control puede omitir sus valores persistentes en lugar de cargarlos solo para que se invaliden mediante las propiedades de ambiente proporcionadas por el cliente.

Un control también puede permitir guardar y restaurar su estado en un conjunto de propiedades OLE, un conjunto de identificadores y valores en un formato especificado. Esta característica puede ser útil con contenedores como Visual Basic, que guarda sus programas en forma de texto. Un control que desea admitir esta característica implementa [**IDataObject:: GetData**](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-getdata) y [**IDataObject:: SetData**](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-setdata) para pasar sus valores de propiedad hacia y desde el contenedor, respectivamente. Es el trabajo del contenedor convertir esta información en texto y guardarla. Los identificadores utilizados por el control corresponden a los nombres de propiedad y los valores del control. Vea el OLE CDK para ver la definición de este conjunto de propiedades.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Controles ActiveX](activex-controls.md)
</dt> </dl>

 

 