---
title: Notificación de datos
description: A veces es necesario informar a los objetos que consumen datos de un origen externo cuando cambian los datos de ese origen.
ms.assetid: 286a1ecf-5255-4443-a17d-5ffa55ed0be1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49df9e6bb7d9b15192473b18114fe7fcd69ecedf
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "105705041"
---
# <a name="data-notification"></a>Notificación de datos

A veces es necesario informar a los objetos que consumen datos de un origen externo cuando cambian los datos de ese origen. Por ejemplo, se debe notificar a un visor de cintas de tablero de cotizaciones que se base en los datos de una hoja de cálculo cuando cambien los datos para que pueda actualizar su presentación. De forma similar, un documento compuesto necesita información sobre los cambios de datos en los objetos incrustados para que pueda actualizar sus cachés de datos. En casos como este, en el que es deseable la actualización dinámica de los datos, los orígenes de datos requieren algún mecanismo para notificar a los consumidores de datos los cambios a medida que se producen sin obligar a los consumidores a quitar todo el código con el fin de actualizar los datos. Idealmente, una vez que se ha notificado que se ha producido un cambio en el origen de datos, un objeto consumidor puede solicitar una copia actualizada en su tiempo de ocio.

El mecanismo de COM para controlar las notificaciones asincrónicas de este tipo es un objeto denominado receptor de notificaciones, que es simplemente cualquier objeto COM que implementa una interfaz denominada [**IAdviseSink**](/windows/desktop/api/ObjIdl/nn-objidl-iadvisesink). Los consumidores de datos implementan **IAdviseSink**. Se registran para recibir notificaciones mediante la entrega de un puntero al objeto de datos de interés.

Las interfaces [**IAdviseSink**](/windows/desktop/api/ObjIdl/nn-objidl-iadvisesink) exponen los métodos siguientes para recibir notificaciones asincrónicas:



| Método                                                      | Notifica al receptor de notificaciones que                                            |
|-------------------------------------------------------------|--------------------------------------------------------------------------|
| [**OnDataChange**](/windows/desktop/api/ObjIdl/nf-objidl-iadvisesink-ondatachange)<br/> | Los datos del objeto que realiza la llamada han cambiado.<br/>                        |
| [**OnViewChange**](/windows/desktop/api/ObjIdl/nf-objidl-iadvisesink-onviewchange)<br/> | Las instrucciones para dibujar el objeto que realiza la llamada han cambiado.<br/> |
| [**OnRename**](/windows/desktop/api/ObjIdl/nf-objidl-iadvisesink-onrename)<br/>         | El moniker del objeto que realiza la llamada ha cambiado.<br/>                     |
| [**OnSave**](/windows/desktop/api/ObjIdl/nf-objidl-iadvisesink-onsave)<br/>             | El objeto que realiza la llamada se ha guardado en el almacenamiento persistente.<br/>      |
| [**OnClose**](/windows/desktop/api/ObjIdl/nf-objidl-iadvisesink-onclose)<br/>           | El objeto que realiza la llamada se ha cerrado.<br/>                           |



 

Como indica la tabla, la interfaz [**IAdviseSink**](/windows/desktop/api/ObjIdl/nn-objidl-iadvisesink) expone métodos para notificar al receptor de notificaciones de eventos distintos de los cambios en los datos del objeto que realiza la llamada. El objeto que realiza la llamada también puede notificar al receptor el modo en que se dibujan los cambios, o bien se le cambia el nombre, se guarda o se cierra. Estas otras notificaciones se utilizan principalmente o por completo en el contexto de documentos compuestos, aunque el mecanismo de notificación es idéntico. Para obtener más información sobre las notificaciones de documentos compuestos, vea "documentos compuestos".

Con el fin de aprovechar el receptor de notificaciones, un origen de datos debe implementar [**IDataObject::D Advise**](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-dadvise), [**IDataObject::D unvise**](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-dunadvise)y [**IDataObject:: EnumDAdvise**](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-enumdadvise). Un consumidor de datos llama a **DAdvise** método para notificar a un objeto de datos que desea recibir una notificación cuando cambien los datos del objeto. El objeto consumidor llama al método **DUnadvise** para anular esta conexión. Cualquier entidad interesada puede llamar al método **EnumDAdvise** para conocer el número de objetos que tienen una conexión de consulta con un objeto de datos.

Cuando los datos cambian en el origen, el objeto de datos llama a [**IAdviseSink:: OnDataChange**](/windows/desktop/api/ObjIdl/nf-objidl-iadvisesink-ondatachange) en todos los consumidores de datos que se han registrado para recibir notificaciones. Para realizar un seguimiento de las conexiones de consulta y administrar el envío de notificaciones, los orígenes de datos se basan en un objeto denominado titular de una notificación de *datos*. Puede crear su propio titular de notificaciones de datos mediante la implementación de la interfaz [**IDataAdviseHolder**](/windows/desktop/api/ObjIdl/nn-objidl-idataadviseholder) . O bien, puede dejar que COM lo haga por usted mediante una llamada a la función auxiliar [**CreateDataAdviseHolder**](/windows/win32/api/ole2/nf-ole2-createdataadviseholder).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Transferencia de datos](data-transfer.md)
</dt> </dl>

 

