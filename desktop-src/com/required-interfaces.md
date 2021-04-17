---
title: Interfaces requeridas (COM)
description: Interfaces necesarias
ms.assetid: ae238882-d0c9-4120-b8a8-001bf9559cfa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0df483f8c8aa5eb5ecb6799b834fccab42f42ca1
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "105705093"
---
# <a name="required-interfaces-com"></a>Interfaces requeridas (COM)

En la tabla siguiente se enumeran las interfaces de contenedor de controles ActiveX y se indican las interfaces que son opcionales y cuáles son obligatorias y deben implementarse mediante contenedores de control.



| Interfaz                                                                      | ¿Necesario?      | Comentarios                                                                                                                                                                                                                                                                                                                                                     |
|--------------------------------------------------------------------------------|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IOleClientSite**](/windows/desktop/api/OleIdl/nn-oleidl-ioleclientsite)<br/>                            | Sí<br/> |                                                                                                                                                                                                                                                                                                                                                              |
| [**IAdviseSink**](/windows/desktop/api/ObjIdl/nn-objidl-iadvisesink)<br/>                                  | No<br/>  | Solo cuando el contenedor va a recibir notificaciones de cambio de datos (controles con [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject)), (b) ver notificación de cambios (controles que no están activos y tienen [**IViewObject**](/windows/desktop/api/OleIdl/nn-oleidl-iviewobject) o [**IViewObject2**](/windows/desktop/api/OleIdl/nn-oleidl-iviewobject2)) y (c) otras notificaciones de controles que actúan como objetos incrustados estándar.<br/> |
| [**IOleInPlaceSite**](/windows/desktop/api/OleIdl/nn-oleidl-ioleinplacesite)<br/>                          | Sí<br/> |                                                                                                                                                                                                                                                                                                                                                              |
| [**IOleControlSite**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrolsite)<br/>                          | Sí<br/> |                                                                                                                                                                                                                                                                                                                                                              |
| [**IOleInPlaceFrame**](/windows/desktop/api/OleIdl/nn-oleidl-ioleinplaceframe)<br/>                        | Sí<br/> |                                                                                                                                                                                                                                                                                                                                                              |
| [**IOleContainer**](/windows/desktop/api/OleIdl/nn-oleidl-iolecontainer)<br/>                              | Sí<br/> | Vea la nota 1<br/>                                                                                                                                                                                                                                                                                                                                        |
| **IDispatch** para propiedades de ambiente<br/>                                | Sí<br/> | Vea la nota 2 y [las propiedades de ambiente para los controles](ambient-properties-for-controls.md)<br/>                                                                                                                                                                                                                                                             |
| Controlar conjuntos de eventos<br/>                                                  | Sí<br/> | Consulte la nota 2.<br/>                                                                                                                                                                                                                                                                                                                                        |
| [**ISimpleFrameSite**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite)<br/>                        | No<br/>  | [**ISimpleFrameSite**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite) y la compatibilidad con fotogramas simples anidados es opcional.<br/>                                                                                                                                                                                                                                                    |
| [IPropertyNotifySink](data-binding-through-ipropertynotifysink.md)<br/> | No<br/>  | Solo es necesario para los contenedores que (a) tengan su propia interfaz de usuario de edición de propiedades, que requeriría la actualización cada vez que un control cambiara una propiedad o (b) deseara controlar \[ [](/windows/desktop/Midl/requestedit) \] los cambios de propiedad de requestedit y otras características de enlace de datos de este tipo.<br/>                                                                            |
| [IErrorInfo](/windows/win32/api/oaidl/nn-oaidl-ierrorinfo)<br/>       | Sí<br/> | Obligatorio si el contenedor admite interfaces duales. Vea la nota 2.<br/>                                                                                                                                                                                                                                                                                      |
| [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2)<br/>                            | No<br/>  | Se recomienda encarecidamente la compatibilidad.<br/>                                                                                                                                                                                                                                                                                                                  |



 

1.  [**IOleContainer**](/windows/desktop/api/OleIdl/nn-oleidl-iolecontainer) se implementa en el documento o el objeto de formulario (o analógico adecuado) que contiene los sitios del contenedor. Los controles usan **IOleContainer** para desplazarse a otros controles del mismo documento o formulario.
2.  La compatibilidad con interfaces duales no es obligatoria, pero se recomienda encarecidamente. Escribir contenedores de controles ActiveX para aprovechar las ventajas de las interfaces duales proporcionará un mejor rendimiento con los controles que ofrecen compatibilidad con la interfaz dual.

Los contenedores de controles ActiveX deben admitir excepciones de OLE Automation. Si un contenedor de controles admite interfaces duales, debe capturar las excepciones de automatización a través de [IErrorInfo](/windows/win32/api/oaidl/nn-oaidl-ierrorinfo).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Contenedores](containers.md)
</dt> </dl>

 

