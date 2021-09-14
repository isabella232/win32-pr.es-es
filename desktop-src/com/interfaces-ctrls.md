---
title: Interfaces (controles y páginas de propiedades)
description: Las interfaces siguientes se usan para crear objetos COM estándar y páginas de propiedades.
ms.assetid: f0d655b3-fa92-4553-ba21-617649a922a0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e143ab1793eaf0335bbcf04093707bdc359e868e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126965207"
---
# <a name="interfaces-controls-and-property-pages"></a>Interfaces (controles y páginas de propiedades)

Las interfaces siguientes se usan para crear objetos COM estándar y páginas de propiedades.



| Interfaz                                             | Descripción                                                                                                                                                                                                  |
|-------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IFont**](/windows/desktop/api/OCIdl/nn-ocidl-ifont)                                | Proporciona un contenedor alrededor de un Windows de fuente.                                                                                                                                                             |
| [**IFontDisp**](/windows/win32/api/ocidl/nn-ocidl-ifontdisp)                        | Expone las propiedades de un objeto de fuente a través de Automation. Proporciona un subconjunto de los métodos [**IFont.**](/windows/desktop/api/OCIdl/nn-ocidl-ifont)                                                                                           |
| [**IOleControl**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrol)                    | Proporciona las características para admitir funciones mnemotécnicas de teclado, propiedades ambientales y eventos en objetos de control.                                                                                                  |
| [**IOleControlSite**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrolsite)            | Proporciona los métodos que permiten a un objeto de sitio administrar cada control incrustado dentro de un contenedor.                                                                                                           |
| [**IPerPropertyBrowsing**](/windows/desktop/api/OCIdl/nn-ocidl-iperpropertybrowsing)  | Recupera la información de las páginas de propiedades que ofrece un objeto .                                                                                                                                        |
| [**IPicture**](/windows/desktop/api/OCIdl/nn-ocidl-ipicture)                          | Administra un objeto de imagen y sus propiedades. Los objetos de imagen proporcionan una abstracción neutra del lenguaje para mapas de bits, iconos y metarchivos.                                                                       |
| [**IPictureDisp**](/windows/win32/api/ocidl/nn-ocidl-ipicturedisp)                  | Expone las propiedades del objeto de imagen a través de Automation. Proporciona un subconjunto de la funcionalidad disponible a través de [**métodos IPicture.**](/windows/desktop/api/OCIdl/nn-ocidl-ipicture)                                                |
| [**IPointer Puede**](/windows/desktop/api/OCIdl/nn-ocidl-ipointerinactive)          | Permite que un objeto permanezca inactivo la mayor parte del tiempo, pero sigue participando en la interacción con el mouse, incluida la arrastrar y colocar.                                                                         |
| [**Iprint**](/windows/desktop/api/DocObj/nn-docobj-iprint)                              | Habilita documentos compuestos en documentos generales y activos en particular para admitir la impresión mediante programación.                                                                                                   |
| [**IPropertyNotifySink**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertynotifysink)    | Implementado por un objeto receptor para recibir notificaciones sobre los cambios de propiedad de un objeto que admite [**IPropertyNotifySink**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertynotifysink) como interfaz saliente.                       |
| [**IPropertyPage**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertypage)                | Proporciona las características principales de un objeto de página de propiedades que administra una página determinada dentro de una hoja de propiedades.                                                                                                 |
| [**IPropertyPage2**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertypage2)              | Extensión de [**IPropertyPage para**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertypage) admitir la selección inicial de una propiedad en una página.                                                                                                 |
| [**IPropertyPageSite**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertypagesite)        | Proporciona las características principales de un objeto de sitio de página de propiedades.                                                                                                                                                  |
| [**IQuickActivate**](/windows/desktop/api/OCIdl/nn-ocidl-iquickactivate)              | Permite a los controles y contenedores evitar cuellos de botella de rendimiento al cargar controles. Combina el protocolo de enlace en tiempo de carga o en tiempo de inicialización entre el control y su contenedor en una sola llamada. |
| [**ISimpleFrameSite**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite)          | Proporciona controles de marco simples que actúan como contenedores simples para otros controles anidados.                                                                                                                      |
| [**ISpecifyPropertyPage**](/windows/desktop/api/OCIdl/nn-ocidl-ispecifypropertypages) | Indica que un objeto admite páginas de propiedades.                                                                                                                                                            |



 

 

 
