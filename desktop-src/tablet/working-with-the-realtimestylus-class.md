---
description: La clase RealTimeStylus forma parte de las interfaces de programación de aplicaciones (API) de StylusInput. En las secciones siguientes se describen los elementos clave de la clase RealTimeStylus y las API de StylusInput.
ms.assetid: 6385c387-5b11-4719-a6ec-e0bebe875348
title: Trabajar con la clase RealTimeStylus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 919c4de38cb0835996928c877ca4c42faf6a5f96
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810472"
---
# <a name="working-with-the-realtimestylus-class"></a>Trabajar con la clase RealTimeStylus

La clase [**RealTimeStylus**](realtimestylus-class.md) forma parte de las interfaces de programación de aplicaciones (API) de StylusInput. En las secciones siguientes se describen los elementos clave de la clase **RealTimeStylus** y las API de StylusInput.

## <a name="instantiating-the-realtimestylus-class"></a>Crear instancias de la clase RealTimeStylus

Al crear un objeto [**RealTimeStylus**](realtimestylus-class.md) , tiene la opción de adjuntarlo a un identificador de ventana o a un control. La Asociación del objeto **RealTimeStylus** a un identificador de ventana requiere permisos adicionales. Para obtener más información sobre estos permisos, vea [consideraciones de confianza parcial para las API de StylusInput](partial-trust-considerations-for-the-stylusinput-apis.md).

> [!Note]  
> No se puede adjuntar el objeto [**RealTimeStylus**](realtimestylus-class.md) a una ventana o control en un proceso diferente.

 

Si usa el constructor predeterminado, crea un objeto [**RealTimeStylus**](realtimestylus-class.md) que solo puede aceptar la entrada de otro objeto **RealTimeStylus** . Para obtener más información sobre cómo conectar dos objetos **RealTimeStylus** , vea [el modelo RealTimeStylus en cascada](the-cascaded-realtimestylus-model.md).

El objeto [**RealTimeStylus**](realtimestylus-class.md) implementa la interfaz [IDisposable](/dotnet/api/system.idisposable) .

## <a name="extending-the-realtimestylus-class"></a>Extender la clase RealTimeStylus

Para permitir que los complementos interactúen con el flujo de datos desde el lápiz de Tablet PC, el objeto [**RealTimeStylus**](realtimestylus-class.md) mantiene dos colecciones de complementos, a las que se puede tener acceso mediante los métodos [**GetStylusSyncPlugin**](/windows/desktop/api/RTSCom/nf-rtscom-irealtimestylus-getstylussyncplugin) y [**GetStylusAsyncPlugin**](/windows/desktop/api/RTSCom/nf-rtscom-irealtimestylus-getstylusasyncplugin) en C++ y las propiedades [SyncPluginCollection](/previous-versions/ms824833(v=msdn.10)) y [AsyncPluginCollection](/previous-versions/ms824831(v=msdn.10)) en código administrado. Puede Agregar un complemento llamando al método [**AddStylusSyncPlugin**](/windows/desktop/api/RTSCom/nf-rtscom-irealtimestylus-addstylussyncplugin) o [**AddStylusAsyncPlugin**](/windows/desktop/api/RTSCom/nf-rtscom-irealtimestylus-addstylusasyncplugin) de la colección en la propiedad adecuada. Para obtener más información sobre la creación y el uso de complementos, vea [Complementos y la clase RealTimeStylus](plug-ins-and-the-realtimestylus-class.md). Para obtener información sobre cómo crear un complemento sincrónico o asincrónico para una tarea determinada, consulte [consideraciones de subprocesos para las API de StylusInput](threading-considerations-for-the-stylusinput-apis.md) y [consideraciones de rendimiento para las API de StylusInput](performance-considerations-for-the-stylusinput-apis.md).

Los complementos sincrónicos deben implementar la interfaz [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) y los complementos asincrónicos deben implementar la interfaz [**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) . Cada complemento tiene una propiedad [**IStylusSyncPlugin. Interest**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-datainterest) o [**IStylusAsyncPlugin. Interest**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-datainterest) . El objeto [**RealTimeStylus**](realtimestylus-class.md) solo llama a los métodos de notificación del complemento para los métodos en los que se ha suscrito el complemento. Para obtener más información sobre los métodos de notificación, vea [datos de complemento y la clase RealTimeStylus](plug-in-data-and-the-realtimestylus-class.md).

El objeto [**RealTimeStylus**](realtimestylus-class.md) implementa la interfaz [**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) . La única manera de crear una instancia de un objeto **RealTimeStylus** que acepta la entrada de otro objeto **RealTimeStylus** es usar el constructor predeterminado e implementar el modelo **RealTimeStylus** en cascada. Para obtener más información sobre cómo conectar dos objetos **RealTimeStylus** , vea [el modelo RealTimeStylus en cascada](the-cascaded-realtimestylus-model.md).

El objeto [**RealTimeStylus**](realtimestylus-class.md) tiene dos colas internas que llevan los datos del lápiz de Tablet PC, la cola de entrada y la cola de salida. Los datos del lápiz se convierten en instancias de las clases del espacio de nombres [Microsoft. StylusInput. PluginData](/previous-versions/ms574862(v=vs.100)) . En la lista siguiente se describe cómo el objeto **RealTimeStylus** controla los datos del lápiz de Tablet PC.

1.  El objeto [**RealTimeStylus**](realtimestylus-class.md) comprueba primero los objetos de datos de complemento en su cola de entrada y después desde el flujo de datos del lápiz de Tablet PC.
2.  El objeto [**RealTimeStylus**](realtimestylus-class.md) envía un objeto de datos de complemento a los objetos de su colección de complementos sincrónicos. Cada complemento sincrónico puede agregar datos a la cola de entrada o de salida.
3.  Una vez que el objeto de datos del complemento se ha enviado a todos los miembros de la colección de complementos sincrónicos, el objeto de datos del complemento se coloca en la cola de salida del objeto [**RealTimeStylus**](realtimestylus-class.md) .
4.  A continuación, el objeto [**RealTimeStylus**](realtimestylus-class.md) comprueba el siguiente objeto de datos del complemento que se va a procesar.
5.  Mientras que la cola de salida del objeto [**RealTimeStylus**](realtimestylus-class.md) contiene datos, el objeto **RealTimeStylus** envía un objeto de datos de complemento desde su cola de salida a los objetos de su colección de complementos asincrónica. Cada complemento asincrónico puede agregar datos a la cola de entrada o de salida, pero como los complementos asincrónicos se ejecutan en el subproceso de la interfaz de usuario (IU), los datos se agregan a la cola en relación con los datos de lápiz actuales que el objeto **RealTimeStylus** procesa y no con respecto a los datos que procesa el complemento asincrónico.

En el diagrama siguiente se ilustra el flujo de datos del lápiz de Tablet PC a través del objeto [**RealTimeStylus**](realtimestylus-class.md) y sus colecciones de complementos.

![illustratiom que muestra el flujo de datos del lápiz de Tablet PC](images/5a698bc9-833b-4b24-9fa2-70be0ca61032.gif)

En este diagrama, los círculos "A" y "B" representan los datos del lápiz de Tablet PC que ya se han agregado a la cola de salida del objeto [**RealTimeStylus**](realtimestylus-class.md) y que todavía no se han enviado a la colección de complementos asincrónica. La letra "C" de círculo representa los datos del lápiz de Tablet PC que está procesando actualmente el objeto **RealTimeStylus** . Se envía a la colección de complementos sincrónicos y se coloca en la cola de salida. El círculo vacío representa la posición en la cola de salida donde se agregan los datos futuros del lápiz de Tablet PC.

Para obtener más información sobre cómo se agregan datos específicos a la cola y se procesan, vea [datos de complemento y la clase RealTimeStylus](plug-in-data-and-the-realtimestylus-class.md).

A continuación se indica un escenario mínimo para usar el objeto [**RealTimeStylus**](realtimestylus-class.md) en un formulario que recopila entradas manuscritas.

1.  Cree un formulario que implemente la interfaz [**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) .
2.  Cree un objeto [**RealTimeStylus**](realtimestylus-class.md) adjunto a un control en el formulario.
3.  Establezca interés en las notificaciones StylusDown, packets y StylusUp en la propiedad [**IStylusAsyncPlugin. Interest**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-datainterest) del formulario.
4.  En los métodos [**StylusDown**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-stylusdown), [**packets**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-packets)y [**StylusUp**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-stylusup) del formulario, agregue código para controlar el lápiz hacia abajo, los paquetes y las notificaciones del lápiz óptico que se envían desde el objeto [**RealTimeStylus**](realtimestylus-class.md) del formulario.

Para obtener un ejemplo de este tipo de aplicación, vea el [ejemplo de colección de tintas RealTimeStylus](realtimestylus-ink-collection-sample.md).

## <a name="working-with-tablet-objects"></a>Trabajar con objetos de Tablet PC

Cada objeto [**RealTimeStylus**](realtimestylus-class.md) habilitado mantiene una lista de identificadores únicos para los objetos de [**Tablet PC**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) con los que puede interactuar. El objeto **RealTimeStylus** expone dos métodos para la conversión entre el identificador único y el objeto de **tableta** : los métodos [**GetTabletContextIdFromTablet**](/windows/desktop/api/RTSCom/nf-rtscom-irealtimestylus-gettabletcontextidfromtablet) y [**GetTabletFromTabletContextId**](/windows/desktop/api/RTSCom/nf-rtscom-irealtimestylus-gettabletfromtabletcontextid) .

El objeto [TabletPropertyDescription](/previous-versions/ms827769(v=msdn.10)) (en código administrado) contiene una propiedad [PacketPropertyId](/previous-versions/ms827780(v=msdn.10)) y una estructura [TabletPropertyMetrics](/previous-versions/ms827781(v=msdn.10)) que describe el intervalo, la resolución y las unidades de la propiedad de un objeto de [**tableta**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) específico. El método [**GetDesiredPacketDescription**](/windows/desktop/api/RTSCom/nf-rtscom-irealtimestylus-getdesiredpacketdescription) del objeto [**RealTimeStylus**](realtimestylus-class.md) devuelve una matriz de identificadores únicos globales (GUID) para las propiedades de paquete que el objeto **RealTimeStylus** reenvía a sus complementos cuando esas propiedades de paquete están disponibles. Para modificar el conjunto de propiedades de paquete que el objeto **RealTimeStylus** pasa a sus complementos, llame al método [**SetDesiredPacketDescription**](/windows/desktop/api/RTSCom/nf-rtscom-irealtimestylus-setdesiredpacketdescription) del objeto **RealTimeStylus** . El método [GetTabletPropertyDescriptionCollection](/previous-versions/ms825935(v=msdn.10)) (en código administrado) del objeto **RealTimeStylus** toma un identificador de tableta único y devuelve una colección de objetos [TabletPropertyDescription](/previous-versions/ms827760(v=msdn.10)) . Estas propiedades de paquete representan el subconjunto de propiedades admitidas por la tableta devueltas por el método **GetDesiredPacketDescription** .

Para obtener una lista de los GUID de propiedad de paquete estándar, vea la clase [PacketPropertyGuids constantes](packetpropertyguids-constants.md) .

## <a name="special-considerations"></a>Consideraciones especiales

En la lista siguiente se describen otros puntos que se deben tener en cuenta al usar el objeto [**RealTimeStylus**](realtimestylus-class.md) con un objeto de [**tableta**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) .

-   Solo se puede llamar al método [**SetDesiredPacketDescription**](/windows/desktop/api/RTSCom/nf-rtscom-irealtimestylus-setdesiredpacketdescription) mientras el objeto de [**tableta**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) está deshabilitado. El objeto [**RealTimeStylus**](realtimestylus-class.md) puede modificar la lista de propiedades de paquete deseadas. por lo tanto, llame al método [**GetDesiredPacketDescription**](/windows/desktop/api/RTSCom/nf-rtscom-irealtimestylus-getdesiredpacketdescription) después de la llamada al método **SetDesiredPacketDescription** para determinar qué propiedades de paquete pueden reenviar el objeto **RealTimeStylus** a sus complementos. Solo se garantiza que una tableta admita los valores **X**, **y** y **PacketStatus** de [PacketProperty](packetproperty-guids.md). Por lo tanto, es posible que el diseño del complemento tenga que tener en cuenta la recepción de menos propiedades de paquete de las deseadas.
-   Solo se puede llamar al método [GetTabletPropertyDescriptionCollection](/previous-versions/ms825935(v=msdn.10)) (para código administrado) mientras el objeto [**RealTimeStylus**](realtimestylus-class.md) está habilitado. Dado que se puede enviar una notificación a los complementos asincrónicos después de que se haya deshabilitado el objeto **RealTimeStylus** , puede que tenga que almacenar en caché la información de cada objeto de [**tableta**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) . El método GetTabletPropertyDescriptionCollection devuelve una lista de las propiedades de paquete deseadas admitidas por la tableta especificada.
-   Cuando el objeto [**RealTimeStylus**](realtimestylus-class.md) está habilitado, cada complemento recibe una llamada a su método [**RealTimeStylusEnabled**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-realtimestylusenabled) . El objeto [RealTimeStylusEnabledData](/previous-versions/ms824229(v=msdn.10)) pasado en la notificación contiene una colección de los identificadores de contexto para las tabletas disponibles en el momento en que se habilita el objeto **RealTimeStylus** .
-   Cuando se agrega o se quita una tableta que puede usar el objeto [**RealTimeStylus**](realtimestylus-class.md) en Tablet PC mientras el objeto **RealTimeStylus** está habilitado, el objeto **RealTimeStylus** notifica a sus complementos que se ha agregado o quitado un objeto de [**tableta**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) . Para obtener más información, vea [datos de complemento y la clase RealTimeStylus](plug-in-data-and-the-realtimestylus-class.md).

## <a name="working-with-tablet-pens"></a>Trabajar con lápices de Tablet PC

El objeto [**RealTimeStylus**](realtimestylus-class.md) pasa información sobre el lápiz de Tablet PC a sus complementos en una serie de métodos de notificación. La información sobre el lápiz de Tablet PC está representada por un objeto de [lápiz óptico](/previous-versions/ms824824(v=msdn.10)) , a través del método [**GetStyluses**](/windows/desktop/api/RTSCom/nf-rtscom-irealtimestylus-getstyluses) . Este objeto es una representación del lápiz de Tablet PC en el momento en que se recopilaron los datos. Dado que los complementos reciben los datos del lápiz de Tablet PC como parte del flujo de datos del lápiz de Tablet PC, los complementos deben usar la información del objeto de lápiz en lugar de comprobar el estado actual de un lápiz de Tablet PC determinado a través de la clase [**cursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) . Para obtener información sobre cómo se pasan los datos del botón lápiz de Tablet PC y lápiz de Tablet PC a los complementos, vea [datos de complemento y la clase RealTimeStylus](plug-in-data-and-the-realtimestylus-class.md).

Para obtener una matriz de los objetos de [lápiz óptico](/previous-versions/ms824824(v=msdn.10)) que ha encontrado el objeto [**RealTimeStylus**](realtimestylus-class.md) desde que se habilitó por última vez, use el método [**GetStyluses**](/windows/desktop/api/RTSCom/nf-rtscom-irealtimestylus-getstyluses) del objeto **RealTimeStylus** .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Microsoft. Ink. Tablet](/previous-versions/ms827783(v=msdn.10))
</dt> <dt>

[Microsoft. StylusInput. RealTimeStylus](/previous-versions/ms585724(v=vs.100))
</dt> <dt>

[El modelo RealTimeStylus en cascada](the-cascaded-realtimestylus-model.md)
</dt> <dt>

[Consideraciones de confianza parcial para las API de StylusInput](partial-trust-considerations-for-the-stylusinput-apis.md)
</dt> <dt>

[Datos de complementos y clase RealTimeStylus](plug-in-data-and-the-realtimestylus-class.md)
</dt> <dt>

[Consideraciones sobre los subprocesos para las API de StylusInput](threading-considerations-for-the-stylusinput-apis.md)
</dt> </dl>

 

 
