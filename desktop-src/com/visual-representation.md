---
title: Representación visual
description: Un control admite el posicionamiento y la visualización dentro de su contenedor a través de la tecnología de documentos compuestos y la tecnología de arrastrar y colocar ole que implica tanto el control como su contenedor.
ms.assetid: a7940560-360c-4c0d-9ac1-d051adb0b83e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9711dccbc7aa17f0b4a2ff228b2e2e4421e5083b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160514"
---
# <a name="visual-representation"></a>Representación visual

Un control admite el posicionamiento y la visualización dentro de su contenedor a través de la tecnología de documentos compuestos y la tecnología de arrastrar y colocar ole que implica tanto el control como su contenedor. El control debe ser capaz de dibujarse mientras el contenedor administra la posición del control y su tamaño.

Los controles se agregan a las funciones básicas proporcionadas por los documentos OLE. Un control llama al método [**IOleClientSite::RequestNewObjectLayout**](/windows/desktop/api/OleIdl/nf-oleidl-ioleclientsite-requestnewobjectlayout) de su cliente para decir a su contenedor que quiere cambiar su tamaño. El cliente llama al [**IOleObject::GetExtent**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getextent) del control para obtener el nuevo tamaño y llama a [**IOleInPlaceObject::SetObjectRects**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceobject-setobjectrects) para establecer el control en su nuevo tamaño.

Los controles que solo admiten [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream) o [**IPersistStreamInit**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit) no admiten el almacenamiento en caché a través de [**IOleCache2**](/windows/desktop/api/OleIdl/nn-oleidl-iolecache2) porque la memoria caché requiere compatibilidad con [**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage). Sin embargo, estos controles deben proporcionar una manera de que el cliente represente el control a través de [**IDataObject::GetData**](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-getdata) para que el cliente pueda crear y administrar opcionalmente su propia memoria caché de los datos de presentación para el control.

Los controles usan el tipo HIMETRIC para sus coordenadas. Sin embargo, diferentes contenedores pueden usar sistemas de coordenadas diferentes. El contenedor quiere recibir coordenadas en su propio sistema, pero el control no sabe necesariamente qué coordenadas usa su contenedor. Para comunicarse correctamente, el control necesita una manera de convertir valores en las coordenadas de su contenedor. El contenedor proporciona un objeto de sitio con [**el método IOleControlSite::TransformCoords.**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-transformcoords) El control llama primero a este método en el sitio cliente de su contenedor para convertir sus coordenadas en las coordenadas adecuadas para el contenedor. A continuación, puede pasar las coordenadas convertida al contenedor.

Los controles pueden llamar a [**IOleControlSite::LockInPlaceActive**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-lockinplaceactive) en el objeto de sitio del contenedor para evitar que el contenedor intente degradar el control fuera del estado activo en el lugar. La degradación del control de esta manera hace que el control se desactive y se destruya su ventana, por lo que si el control debe mantener su ventana durante un tiempo conocido, puede llamar a **LockInPlaceActive** para garantizar su estado.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Controles ActiveX](activex-controls.md)
</dt> </dl>

 

 




