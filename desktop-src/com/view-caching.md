---
title: Visualización del almacenamiento en caché
description: Visualización del almacenamiento en caché
ms.assetid: d19c111c-1367-43a2-97a9-35dc0ff5dcc8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b155c0a9d3229db85a52b0589c4854bdee9a2e8e4171e231480036c512af737
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047692"
---
# <a name="view-caching"></a>Visualización del almacenamiento en caché

Una aplicación contenedora debe ser capaz de obtener una presentación de un objeto con el fin de mostrarlo o imprimirlo para los usuarios cuando el documento está abierto, pero la aplicación de servidor del objeto no se está ejecutando o no está instalada en el equipo del usuario. Sin embargo, suponer que los servidores de todos los objetos que podrían encontrarse en un documento están instalados en el equipo de cada usuario y siempre se pueden ejecutar a petición no es realista. El controlador de objetos predeterminado, que está disponible en todo momento, resuelve este desafío almacenando en caché las presentaciones de objetos en el almacenamiento del documento y manipulando estas presentaciones en cualquier plataforma independientemente de la disponibilidad del servidor de objetos en cualquier instalación concreta del contenedor.

Los contenedores pueden mantener presentaciones de dibujo para uno o varios dispositivos de destino específicos, además del necesario para mantener el objeto en pantalla. Además, si portar el objeto de una plataforma a otra, OLE convierte automáticamente los formatos de datos del objeto en los admitidos en la nueva plataforma. Por ejemplo, si mueve un objeto de Windows a Macintosh, OLE convertirá sus presentaciones de metarchivo a formatos DE NIF.

Para presentar al usuario una representación precisa de un objeto incrustado, la aplicación contenedora del objeto inicia un diálogo con el controlador de objetos, solicitando datos e instrucciones de dibujo. Para poder satisfacer las solicitudes del contenedor, el controlador debe implementar las interfaces [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject), [**IViewObject2**](/windows/desktop/api/OleIdl/nn-oleidl-iviewobject2)e [**IOleCache.**](/windows/desktop/api/OleIdl/nn-oleidl-iolecache)

[**IDataObject permite**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) que una aplicación contenedora OLE obtenga datos de y envíe datos a sus objetos incrustados o vinculados. Cuando los datos cambian en un objeto, esta interfaz proporciona una manera de que el objeto haga que sus nuevos datos estén disponibles para su contenedor y proporciona al contenedor una manera de actualizar los datos en su copia del objeto. (Para obtener una explicación de la transferencia de datos en general, vea el capítulo 4, Transferencia de datos).

La interfaz [**IViewObject2**](/windows/desktop/api/OleIdl/nn-oleidl-iviewobject2) es muy parecido a la interfaz [**IDataObject,**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) salvo que pide a un objeto que se dibuje en un contexto de dispositivo, como una pantalla, impresora o metarchivo, en lugar de mover o copiar sus datos en la memoria o en algún otro medio de transferencia. El propósito de la interfaz es permitir que un contenedor OLE obtenga representaciones gráficas alternativas de sus objetos incrustados, cuyos datos ya tiene, lo que evita la sobrecarga de tener que transferir instancias completamente nuevas de los mismos objetos de datos simplemente para obtener nuevas instrucciones de dibujo. En su lugar, la **interfaz IViewObject2** permite que el contenedor pida a un objeto que proporcione una representación gráfica de sí mismo dibujando en un contexto de dispositivo especificado por el contenedor.

Al llamar a la [**interfaz IViewObject2,**](/windows/desktop/api/OleIdl/nn-oleidl-iviewobject2) una aplicación contenedora también puede especificar que el objeto se dibuje en un dispositivo de destino diferente del en el que se representará realmente. Esto permite que el contenedor, según sea necesario, genere diferentes representaciones a partir de un solo objeto. Por ejemplo, el autor de la llamada podría pedir al objeto que se componga para una impresora, aunque el dibujo resultante se represente en pantalla. Por supuesto, el resultado sería una vista previa de impresión del objeto.

La [**interfaz IViewObject2**](/windows/desktop/api/OleIdl/nn-oleidl-iviewobject2)también proporciona métodos que permiten que los contenedores se registren para las notificaciones de cambio de vista. Al igual que con los datos y los avisos OLE, una conexión de consulta de vistas permite a un contenedor actualizar sus representaciones de un objeto por su comodidad, en lugar de responder a una llamada desde el objeto . Por ejemplo, si una nueva versión de la aplicación de servidor de un objeto fuera a ofrecer vistas adicionales de los mismos datos, el controlador predeterminado del objeto llamaría a la implementación de cada contenedor de [**IAdviseSink::OnViewChange**](/windows/desktop/api/ObjIdl/nf-objidl-iadvisesink-onviewchange) para que sepan que las nuevas presentaciones estaban disponibles. El contenedor recuperaría esta información del receptor de asesoramiento solo cuando sea necesario.

Dado Windows contextos de dispositivo solo tienen significado dentro de un único proceso, no se pueden pasar punteros [**IViewObject2**](/windows/desktop/api/OleIdl/nn-oleidl-iviewobject2) a través de los límites del proceso. Como resultado, los servidores locales y remotos OLE no necesitan ningún tipo de implementación de la interfaz, lo que no funcionaría correctamente aunque lo hicieran. Solo los controladores de objetos y los servidores en proceso implementan la **interfaz IViewObject2.** OLE proporciona una implementación predeterminada, que puede usar en sus propios servidores ole en proceso y controladores de objetos simplemente agregando el controlador predeterminado OLE. O bien, puede escribir su propia implementación de **IViewObject2.**

Un objeto implementa la interfaz [**IOleCache**](/windows/desktop/api/OleIdl/nn-oleidl-iolecache) para que el controlador sepa qué funcionalidades debe almacenar en caché. El controlador de objetos también posee la memoria caché y se asegura de que se mantiene actualizada. A medida que el objeto incrustado entra en estado de ejecución, el controlador configura las conexiones de aviso adecuadas en el objeto de servidor, y actúa como receptor. Las [**implementaciones de interfaz IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) [**e IViewObject2**](/windows/desktop/api/OleIdl/nn-oleidl-iviewobject2)funcionan fuera de los datos almacenados en caché en el lado cliente. La implementación del controlador de **IViewObject2** es responsable de determinar qué formatos de datos almacenar en caché para satisfacer las solicitudes de dibujo del cliente. La implementación del controlador de **IDataObject** es responsable de obtener datos en varios formatos, etc., entre la memoria y la instancia [**de IStorage**](/windows/desktop/api/objidl/nn-objidl-istorage) subyacente del objeto incrustado. Los controladores personalizados pueden usar estas implementaciones agregando en el controlador predeterminado.

> [!Note]  
> La [**interfaz IViewObject2**](/windows/desktop/api/OleIdl/nn-oleidl-iviewobject2) es una extensión funcional simple de [**IViewObject**](/windows/desktop/api/OleIdl/nn-oleidl-iviewobject) y debe implementarse en lugar de la última interfaz, que ahora está obsoleta. Además de proporcionar los métodos **IViewObject,** la interfaz **IViewObject2** proporciona un único miembro adicional, [**GetExtent**](/windows/desktop/api/OleIdl/nf-oleidl-iviewobject2-getextent), que permite a una aplicación contenedora obtener el tamaño de la presentación de un objeto de la memoria caché sin tener que mover primero el objeto al estado en ejecución con una llamada a [**IOleObject::GetExtent.**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getextent)

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Documentos compuestos](compound-documents.md)
</dt> </dl>

 

 