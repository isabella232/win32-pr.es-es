---
title: Interfaces necesarias (COM)
description: Obtenga información sobre las interfaces de contenedor de controles ActiveX que pueden o deben implementarse mediante contenedores de control.
ms.assetid: ae238882-d0c9-4120-b8a8-001bf9559cfa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55015ee5837754c073d2590144687131c285bb80
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407648"
---
# <a name="required-interfaces-com"></a>Interfaces necesarias (COM)

En la tabla siguiente se enumeran las interfaces del contenedor de controles ActiveX y se denota qué interfaces son opcionales y cuáles son obligatorias y deben implementarse mediante contenedores de control.



| Interfaz                                                                      | ¿Necesario?      | Comentarios                                                                                                                                                                                                                                                                                                                                                     |
|--------------------------------------------------------------------------------|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IOleClientSite**](/windows/desktop/api/OleIdl/nn-oleidl-ioleclientsite)<br/>                            | Sí<br/> |                                                                                                                                                                                                                                                                                                                                                              |
| [**IAdviseSink**](/windows/desktop/api/ObjIdl/nn-objidl-iadvisesink)<br/>                                  | No<br/>  | Solo cuando el contenedor desea (a) notificaciones de cambio de datos (controles con [**IDataObject),**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject)(b) ver notificación de cambios (controles que no están activos y tienen [**IViewObject**](/windows/desktop/api/OleIdl/nn-oleidl-iviewobject) o [**IViewObject2)**](/windows/desktop/api/OleIdl/nn-oleidl-iviewobject2)y (c) otras notificaciones de controles que actúan como objetos incrustados estándar.<br/> |
| [**IOleInPlaceSite**](/windows/desktop/api/OleIdl/nn-oleidl-ioleinplacesite)<br/>                          | Sí<br/> |                                                                                                                                                                                                                                                                                                                                                              |
| [**IOleControlSite**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrolsite)<br/>                          | Sí<br/> |                                                                                                                                                                                                                                                                                                                                                              |
| [**IOleInPlaceFrame**](/windows/desktop/api/OleIdl/nn-oleidl-ioleinplaceframe)<br/>                        | Sí<br/> |                                                                                                                                                                                                                                                                                                                                                              |
| [**IOleContainer**](/windows/desktop/api/OleIdl/nn-oleidl-iolecontainer)<br/>                              | Sí<br/> | Consulte la nota 1<br/>                                                                                                                                                                                                                                                                                                                                        |
| **IDispatch para** propiedades de ambiente<br/>                                | Sí<br/> | Vea la nota 2 y [Propiedades ambientales de los controles.](ambient-properties-for-controls.md)<br/>                                                                                                                                                                                                                                                             |
| Controlar conjuntos de eventos<br/>                                                  | Sí<br/> | Consulte la nota 2.<br/>                                                                                                                                                                                                                                                                                                                                        |
| [**ISimpleFrameSite**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite)<br/>                        | No<br/>  | [**ISimpleFrameSite y la**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite) compatibilidad con marcos simples anidados es opcional.<br/>                                                                                                                                                                                                                                                    |
| [IPropertyNotifySink](data-binding-through-ipropertynotifysink.md)<br/> | No<br/>  | Solo es necesario para los contenedores que (a) tienen su propia interfaz de usuario de edición de propiedades, lo que requeriría actualizar cada vez que un control cambiase una propiedad o (b) desea controlar los cambios de propiedad requestedit y otras características de enlace de \[ [](/windows/desktop/Midl/requestedit) \] datos.<br/>                                                                            |
| [IErrorInfo](/windows/win32/api/oaidl/nn-oaidl-ierrorinfo)<br/>       | Sí<br/> | Obligatorio si el contenedor admite interfaces duales. Vea la nota 2.<br/>                                                                                                                                                                                                                                                                                      |
| [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2)<br/>                            | No<br/>  | Se recomienda encarecidamente la compatibilidad.<br/>                                                                                                                                                                                                                                                                                                                  |



 

1.  [**IOleContainer**](/windows/desktop/api/OleIdl/nn-oleidl-iolecontainer) se implementa en el documento o objeto de formulario (o análogo adecuado) que contiene los sitios de contenedor. Los controles **usan IOleContainer** para navegar a otros controles en el mismo documento o formulario.
2.  La compatibilidad con interfaces duales no es obligatoria, pero se recomienda encarecidamente. La escritura de contenedores de controles ActiveX para aprovechar las ventajas de las interfaces duales ofrece un mejor rendimiento con controles que ofrecen compatibilidad con interfaces duales.

Los contenedores de controles ActiveX deben admitir excepciones de OLE Automation. Si un contenedor de controles admite interfaces duales, debe capturar excepciones de automatización a través [de IErrorInfo](/windows/win32/api/oaidl/nn-oaidl-ierrorinfo).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Contenedores](containers.md)
</dt> </dl>

 

