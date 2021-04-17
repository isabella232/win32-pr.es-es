---
title: Interfaces (controles y páginas de propiedades)
description: Las interfaces siguientes se utilizan para crear objetos COM estándar y páginas de propiedades.
ms.assetid: f0d655b3-fa92-4553-ba21-617649a922a0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e143ab1793eaf0335bbcf04093707bdc359e868e
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "105714523"
---
# <a name="interfaces-controls-and-property-pages"></a>Interfaces (controles y páginas de propiedades)

Las interfaces siguientes se utilizan para crear objetos COM estándar y páginas de propiedades.



| Interfaz                                             | Descripción                                                                                                                                                                                                  |
|-------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IFont**](/windows/desktop/api/OCIdl/nn-ocidl-ifont)                                | Proporciona un contenedor alrededor de un objeto de fuente de Windows.                                                                                                                                                             |
| [**IFontDisp**](/windows/win32/api/ocidl/nn-ocidl-ifontdisp)                        | Expone las propiedades de un objeto Font a través de la automatización. Proporciona un subconjunto de los métodos [**IFont**](/windows/desktop/api/OCIdl/nn-ocidl-ifont) .                                                                                           |
| [**IOleControl**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrol)                    | Proporciona las características para admitir teclas de teclado, propiedades de ambiente y eventos en objetos de control.                                                                                                  |
| [**IOleControlSite**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrolsite)            | Proporciona los métodos que permiten a un objeto de sitio administrar cada control incrustado dentro de un contenedor.                                                                                                           |
| [**IPerPropertyBrowsing**](/windows/desktop/api/OCIdl/nn-ocidl-iperpropertybrowsing)  | Recupera la información de las páginas de propiedades ofrecidas por un objeto.                                                                                                                                        |
| [**IPicture**](/windows/desktop/api/OCIdl/nn-ocidl-ipicture)                          | Administra un objeto de imagen y sus propiedades. Los objetos de imagen proporcionan una abstracción independiente del idioma para los mapas de bits, los iconos y los metaarchivos.                                                                       |
| [**IPictureDisp**](/windows/win32/api/ocidl/nn-ocidl-ipicturedisp)                  | Expone las propiedades del objeto de imagen a través de la automatización. Proporciona un subconjunto de la funcionalidad disponible a través de los métodos [**IPicture**](/windows/desktop/api/OCIdl/nn-ocidl-ipicture) .                                                |
| [**IPointerInactive**](/windows/desktop/api/OCIdl/nn-ocidl-ipointerinactive)          | Permite que un objeto permanezca inactivo la mayor parte del tiempo, pero todavía participa en la interacción con el mouse, lo que incluye arrastrar y colocar.                                                                         |
| [**IPrint**](/windows/desktop/api/DocObj/nn-docobj-iprint)                              | Habilita los documentos compuestos en los documentos generales y activos, en concreto, para admitir la impresión mediante programación.                                                                                                   |
| [**IPropertyNotifySink**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertynotifysink)    | Implementado por un objeto receptor para recibir notificaciones sobre los cambios de propiedad de un objeto que admite [**IPropertyNotifySink**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertynotifysink) como interfaz de salida.                       |
| [**IPropertyPage**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertypage)                | Proporciona las características principales de un objeto de página de propiedades que administra una página determinada dentro de una hoja de propiedades.                                                                                                 |
| [**IPropertyPage2**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertypage2)              | Una extensión de [**IPropertyPage**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertypage) para admitir la selección inicial de una propiedad en una página.                                                                                                 |
| [**IPropertyPageSite**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertypagesite)        | Proporciona las características principales para un objeto de sitio de página de propiedades.                                                                                                                                                  |
| [**IQuickActivate**](/windows/desktop/api/OCIdl/nn-ocidl-iquickactivate)              | Permite a los controles y contenedores evitar cuellos de botella de rendimiento en la carga de controles. Combina el protocolo de enlace de tiempo de carga o de inicialización entre el control y su contenedor en una única llamada. |
| [**ISimpleFrameSite**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite)          | Proporciona controles de marco sencillos que actúan como contenedores simples para otros controles anidados.                                                                                                                      |
| [**ISpecifyPropertyPage**](/windows/desktop/api/OCIdl/nn-ocidl-ispecifypropertypages) | Indica que un objeto admite páginas de propiedades.                                                                                                                                                            |



 

 

 
