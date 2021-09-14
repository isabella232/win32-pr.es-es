---
title: Standard Picture (Objeto)
description: Standard Picture (Objeto)
ms.assetid: 2df9e0a7-444b-454c-983a-82e82b9ed9d1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e8a711fc0c33cf5e99b0db6e90941dbe855289b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127253197"
---
# <a name="standard-picture-object"></a>Standard Picture (Objeto)

El objeto de imagen estándar proporciona una abstracción independiente del lenguaje para imágenes GDI: mapas de bits, iconos, metarchivos y metarchivos mejorados. Al igual que con el objeto de fuente estándar, el sistema proporciona una implementación estándar de este objeto. Sus interfaces principales son [**IPicture**](/windows/desktop/api/OCIdl/nn-ocidl-ipicture) e [**IPictureDisp,**](/windows/win32/api/ocidl/nn-ocidl-ipicturedisp)que se derivan de **IDispatch** para proporcionar acceso a las propiedades de la imagen a través de la automatización OLE. Se crea un objeto de imagen con [**OleCreatePictureIndirect**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepictureindirect).

El objeto picture también admite la interfaz saliente [**IPropertyNotifySink**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertynotifysink) para que un cliente pueda determinar cuándo cambian las propiedades de la imagen. En consecuencia, el objeto picture también admite [**IConnectionPointContainer**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpointcontainer) y un punto de conexión para **IPropertyNotifySink.**

El objeto picture también admite [**IPersistStream para**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream) que pueda guardarse y cargarse desde una instancia [**de IStream**](/windows/desktop/api/objidl/nn-objidl-istream). Un objeto que usa internamente un objeto de imagen normalmente guardaría y cargaría la imagen como parte del propio control de persistencia del objeto. La [**función OleLoadPicture**](/windows/desktop/api/OleCtl/nf-olectl-oleloadpicture) simplifica la creación de un objeto de imagen basado en el contenido de la secuencia.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Propiedades del control](control-properties.md)
</dt> </dl>

 

 