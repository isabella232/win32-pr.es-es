---
title: Ver almacenamiento en caché
description: Ver almacenamiento en caché
ms.assetid: d19c111c-1367-43a2-97a9-35dc0ff5dcc8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 592c5bc2555e907cdc4e600465b807387c3a5548
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104421445"
---
# <a name="view-caching"></a>Ver almacenamiento en caché

Una aplicación contenedora debe ser capaz de obtener una presentación de un objeto con el fin de mostrarla o imprimirla para los usuarios cuando el documento está abierto, pero la aplicación de servidor del objeto no se está ejecutando o no está instalada en el equipo del usuario. No obstante, supongamos que los servidores de todos los objetos que se pueden encontrar en un documento se instalan en el equipo de cada usuario y que siempre se pueden ejecutar a petición es poco realista. El controlador de objetos predeterminado, que está disponible en todo momento, resuelve este dilema mediante el almacenamiento en caché de las presentaciones del objeto en el almacenamiento del documento y la manipulación de estas presentaciones en cualquier plataforma, independientemente de la disponibilidad del servidor de objetos en una instalación determinada del contenedor.

Los contenedores pueden mantener las presentaciones de dibujo de uno o más dispositivos de destino específicos, además de la necesaria para mantener el objeto en la pantalla. Además, si traslada el objeto de una plataforma a otra, OLE convierte automáticamente los formatos de datos del objeto en los que se admiten en la nueva plataforma. Por ejemplo, si mueve un objeto de Windows a Macintosh, OLE convertirá sus presentaciones de metarchivo en formatos PICT.

Para presentar una representación exacta de un objeto incrustado al usuario, la aplicación contenedora del objeto inicia un cuadro de diálogo con el controlador de objetos, solicitando datos e instrucciones de dibujo. Para poder satisfacer las solicitudes del contenedor, el controlador debe implementar las interfaces [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject), [**IViewObject2**](/windows/desktop/api/OleIdl/nn-oleidl-iviewobject2)y [**IOleCache**](/windows/desktop/api/OleIdl/nn-oleidl-iolecache) .

[**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) permite a una aplicación contenedora OLE obtener y enviar datos a los objetos incrustados o vinculados. Cuando los datos cambian en un objeto, esta interfaz proporciona una manera para que el objeto haga que sus nuevos datos estén disponibles para su contenedor y proporciona al contenedor una manera de actualizar los datos en su copia del objeto. (Para obtener una explicación de la transferencia de datos en general, vea el capítulo 4, Transferencia de datos).

La interfaz [**IViewObject2**](/windows/desktop/api/OleIdl/nn-oleidl-iviewobject2) es muy similar a la interfaz [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) , salvo que pide a un objeto que se dibuje en un contexto de dispositivo, como una pantalla, una impresora o un metarchivo, en lugar de moverse o copiar sus datos en la memoria o en algún otro medio de transferencia. El propósito de la interfaz es permitir a un contenedor OLE obtener representaciones de gráficos alternativas de sus objetos incrustados, cuyos datos ya tiene, evitando así la sobrecarga de tener que transferir instancias completamente nuevas de los mismos objetos de datos simplemente para obtener nuevas instrucciones de dibujo. En su lugar, la interfaz **IViewObject2** permite al contenedor pedir a un objeto que proporcione una representación gráfica de sí mismo dibujando en un contexto de dispositivo especificado por el contenedor.

Al llamar a la interfaz [**IViewObject2**](/windows/desktop/api/OleIdl/nn-oleidl-iviewobject2) , una aplicación contenedora también puede especificar que el objeto se dibuje en un dispositivo de destino distinto del que realmente se representará. Esto habilita el contenedor, según sea necesario, para generar representaciones diferentes a partir de un único objeto. Por ejemplo, el autor de la llamada podría solicitar al objeto que se componga para una impresora aunque el dibujo resultante se represente en la pantalla. El resultado, por supuesto, sería una vista previa de impresión del objeto.

La interfaz [**IViewObject2**](/windows/desktop/api/OleIdl/nn-oleidl-iviewobject2)también proporciona métodos que permiten a los contenedores registrarse para las notificaciones de cambio de vista. Al igual que con los datos y los avisos OLE, una conexión de consulta de vistas permite a un contenedor actualizar sus representaciones de un objeto por su propia comodidad en lugar de responder a una llamada del objeto. Por ejemplo, si una nueva versión de la aplicación de servidor de un objeto proporcionara vistas adicionales de los mismos datos, el controlador predeterminado del objeto llamaría a la implementación del contenedor de [**IAdviseSink:: OnViewChange**](/windows/desktop/api/ObjIdl/nf-objidl-iadvisesink-onviewchange) para que sepan que las nuevas presentaciones estaban disponibles. El contenedor recuperaría esta información del receptor de notificaciones solo cuando sea necesario.

Dado que los contextos de dispositivos Windows solo tienen significado dentro de un único proceso, no se pueden pasar punteros de [**IViewObject2**](/windows/desktop/api/OleIdl/nn-oleidl-iviewobject2) a través de los límites del proceso. Como resultado, no es necesario que los servidores locales y remotos de OLE implementen la interfaz, lo que no funcionaría correctamente aunque lo hicieran. Solo los controladores de objetos y los servidores en proceso implementan la interfaz **IViewObject2**. OLE proporciona una implementación predeterminada, que puede usar en sus propios servidores OLE en proceso y controladores de objetos simplemente agregando el controlador predeterminado de OLE. También puede escribir su propia implementación de **IViewObject2**.

Un objeto implementa la interfaz [**IOleCache**](/windows/desktop/api/OleIdl/nn-oleidl-iolecache) para permitir que el controlador sepa qué funcionalidades debe almacenar en caché. El controlador de objetos también posee la memoria caché y garantiza que se mantiene actualizada. Cuando el objeto incrustado entra en el estado de ejecución, el controlador establece las conexiones de consulta apropiadas en el objeto de servidor, que actúa como receptor. Las implementaciones de la interfaz [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) y [**IViewObject2**](/windows/desktop/api/OleIdl/nn-oleidl-iviewobject2)operan fuera de los datos almacenados en caché en el lado cliente. La implementación del controlador de **IViewObject2** es responsable de determinar qué formatos de datos se almacenan en memoria caché para satisfacer las solicitudes de dibujo del cliente. La implementación del controlador de **IDataObject** es responsable de obtener datos en varios formatos, etc., entre la memoria y la instancia de [**IStorage**](/windows/desktop/api/objidl/nn-objidl-istorage) subyacente del objeto incrustado. Los controladores personalizados pueden utilizar estas implementaciones agregando en el controlador predeterminado.

> [!Note]  
> La interfaz [**IViewObject2**](/windows/desktop/api/OleIdl/nn-oleidl-iviewobject2) es una extensión funcional simple de [**IViewObject**](/windows/desktop/api/OleIdl/nn-oleidl-iviewobject) y debe implementarse en lugar de la última interfaz, que ahora está obsoleta. Además de proporcionar los métodos **IViewObject** , la interfaz **IViewObject2** proporciona un solo miembro adicional, [**GetExtent**](/windows/desktop/api/OleIdl/nf-oleidl-iviewobject2-getextent), que permite a una aplicación contenedora obtener el tamaño de la presentación de un objeto de la memoria caché sin tener que trasladar primero el objeto al estado en ejecución con una llamada a [**IOleObject:: GetExtent**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getextent).

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Documentos compuestos](compound-documents.md)
</dt> </dl>

 

 