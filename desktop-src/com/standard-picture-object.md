---
title: Objeto de imagen estándar
description: Objeto de imagen estándar
ms.assetid: 2df9e0a7-444b-454c-983a-82e82b9ed9d1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e8a711fc0c33cf5e99b0db6e90941dbe855289b
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "103995658"
---
# <a name="standard-picture-object"></a>Objeto de imagen estándar

El objeto de imagen estándar proporciona una abstracción independiente del idioma para las imágenes GDI: mapas de bits, iconos, metaarchivos y metaarchivos mejorados. Al igual que con el objeto de fuente estándar, el sistema proporciona una implementación estándar de este objeto. Sus interfaces principales son [**IPicture**](/windows/desktop/api/OCIdl/nn-ocidl-ipicture) y [**IPictureDisp**](/windows/win32/api/ocidl/nn-ocidl-ipicturedisp), lo que se deriva de **IDispatch** para proporcionar acceso a las propiedades de la imagen a través de la automatización OLE. Se crea un objeto de imagen nuevo con [**OleCreatePictureIndirect**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepictureindirect).

El objeto Picture también admite la interfaz de salida [**IPropertyNotifySink**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertynotifysink) para que un cliente pueda determinar cuándo cambian las propiedades de la imagen. En consecuencia, el objeto Picture también admite [**IConnectionPointContainer**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpointcontainer) y un punto de conexión para **IPropertyNotifySink**.

El objeto Picture también admite [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream) para que pueda guardarse y cargarse a sí mismo desde una instancia de [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream). Un objeto que usa un objeto de imagen internamente normalmente guardaría y cargaría la imagen como parte del propio control de persistencia del objeto. La función [**OleLoadPicture**](/windows/desktop/api/OleCtl/nf-olectl-oleloadpicture) simplifica la creación de un objeto de imagen basado en el contenido de la secuencia.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Propiedades del control](control-properties.md)
</dt> </dl>

 

 