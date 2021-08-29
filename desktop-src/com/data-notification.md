---
title: Notificación de datos
description: Los objetos que consumen datos de un origen externo a veces deben estar informados cuando cambian los datos de ese origen.
ms.assetid: 286a1ecf-5255-4443-a17d-5ffa55ed0be1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5d90e9548e39fbfcbfcc6438b22f747bc0045e157de42451001df18bf76df4c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119854635"
---
# <a name="data-notification"></a>Notificación de datos

Los objetos que consumen datos de un origen externo a veces deben estar informados cuando cambian los datos de ese origen. Por ejemplo, es necesario notificar a un visor de cintas de ticker de acciones que se basa en los datos de alguna hoja de cálculo cuando esos datos cambian para que pueda actualizar su presentación. De forma similar, un documento compuesto necesita información sobre los cambios de datos en sus objetos incrustados para que pueda actualizar sus cachés de datos. En casos como este, donde la actualización dinámica de datos es deseable, los orígenes de datos requieren algún mecanismo para notificar a los consumidores de datos los cambios a medida que se producen sin obligar a los consumidores a quitar todo para actualizar sus datos. Idealmente, después de recibir una notificación de que se ha producido un cambio en el origen de datos, un objeto consumidor puede solicitar una copia actualizada en su momento.

El mecanismo de COM para controlar las notificaciones asincrónicas de este tipo es un objeto denominado receptor de asesoramiento, que es simplemente cualquier objeto COM que implementa una interfaz denominada [**IAdviseSink**](/windows/desktop/api/ObjIdl/nn-objidl-iadvisesink). Los consumidores de datos implementan **IAdviseSink**. Se registran para recibir notificaciones mediante la entrega de un puntero al objeto de datos de interés.

Las [**interfaces IAdviseSink**](/windows/desktop/api/ObjIdl/nn-objidl-iadvisesink) exponen los métodos siguientes para recibir notificaciones asincrónicas:



| Método                                                      | Notifica al receptor del aviso que                                            |
|-------------------------------------------------------------|--------------------------------------------------------------------------|
| [**OnDataChange**](/windows/desktop/api/ObjIdl/nf-objidl-iadvisesink-ondatachange)<br/> | Los datos del objeto que realiza la llamada han cambiado.<br/>                        |
| [**OnViewChange**](/windows/desktop/api/ObjIdl/nf-objidl-iadvisesink-onviewchange)<br/> | Las instrucciones para dibujar el objeto que realiza la llamada han cambiado.<br/> |
| [**OnRename**](/windows/desktop/api/ObjIdl/nf-objidl-iadvisesink-onrename)<br/>         | El moniker del objeto que realiza la llamada ha cambiado.<br/>                     |
| [**OnSave**](/windows/desktop/api/ObjIdl/nf-objidl-iadvisesink-onsave)<br/>             | El objeto que realiza la llamada se ha guardado en el almacenamiento persistente.<br/>      |
| [**OnClose**](/windows/desktop/api/ObjIdl/nf-objidl-iadvisesink-onclose)<br/>           | Se ha cerrado el objeto que realiza la llamada.<br/>                           |



 

Como indica la tabla, la interfaz [**IAdviseSink**](/windows/desktop/api/ObjIdl/nn-objidl-iadvisesink) expone métodos para notificar al receptor de notificaciones de eventos distintos de los cambios en los datos del objeto que realiza la llamada. El objeto que realiza la llamada también puede notificar al receptor cuando cambia la forma en que se dibuja, o se le cambia el nombre, se guarda o se cierra. Estas otras notificaciones se usan principalmente o completamente en el contexto de documentos compuestos, aunque el mecanismo de notificación es idéntico. Para obtener más información sobre las notificaciones de documentos compuestos, vea "Documentos compuestos".

Para aprovechar las ventajas del receptor advise, un origen de datos debe implementar [**IDataObject::D Advise**](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-dadvise), [**IDataObject::D Unadvise**](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-dunadvise)e [**IDataObject::EnumDAdvise**](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-enumdadvise). Un consumidor de datos llama a **DAdvise** mothod para notificar a un objeto de datos que desea recibir una notificación cuando cambian los datos del objeto. El objeto de consumo llama al **método DUnadvise** para desmontar esta conexión. Cualquier parte interesada puede llamar al método **EnumDAdvise** para obtener información sobre el número de objetos que tienen una conexión de asesoramiento con un objeto de datos.

Cuando los datos cambian en el origen, el objeto de datos llama a [**IAdviseSink::OnDataChange**](/windows/desktop/api/ObjIdl/nf-objidl-iadvisesink-ondatachange) en todos los consumidores de datos que se han registrado para recibir notificaciones. Para realizar un seguimiento de las conexiones de asesoramiento y administrar el envío de notificaciones, los orígenes de datos se basan en un objeto denominado titular *del aviso de datos*. Puede crear su propio titular de asesoramiento de datos mediante la implementación de la [**interfaz IDataAdviseHolder.**](/windows/desktop/api/ObjIdl/nn-objidl-idataadviseholder) O bien, puede dejar que COM lo haga por usted llamando a la función auxiliar [**CreateDataAdviseHolder**](/windows/win32/api/ole2/nf-ole2-createdataadviseholder).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Transferencia de datos](data-transfer.md)
</dt> </dl>

 

