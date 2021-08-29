---
description: La clase RealTimeStylus forma parte de las interfaces de programación de aplicaciones (API) StylusInput. En las secciones siguientes se describen los elementos clave de la clase RealTimeStylus y las API StylusInput.
ms.assetid: 6385c387-5b11-4719-a6ec-e0bebe875348
title: Trabajar con la clase RealTimeStylus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d11f61390c39284ccee235294612b621ac09c8d766fd1e7e18686d1bf479c553
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119708235"
---
# <a name="working-with-the-realtimestylus-class"></a>Trabajar con la clase RealTimeStylus

La [**clase RealTimeStylus**](realtimestylus-class.md) forma parte de las interfaces de programación de aplicaciones (API) StylusInput. En las secciones siguientes se describen los elementos clave **de la clase RealTimeStylus** y las API StylusInput.

## <a name="instantiating-the-realtimestylus-class"></a>Creación de instancias de la clase RealTimeStylus

Al crear un [**objeto RealTimeStylus,**](realtimestylus-class.md) tiene la opción de adjuntarlo a un identificador de ventana o a un control . Asociar el **objeto RealTimeStylus** a un identificador de ventana requiere permisos adicionales. Para obtener más información sobre estos permisos, vea Consideraciones de confianza [parcial para las API StylusInput](partial-trust-considerations-for-the-stylusinput-apis.md).

> [!Note]  
> No se puede asociar [**el objeto RealTimeStylus**](realtimestylus-class.md) a una ventana o control en un proceso diferente.

 

Si usa el constructor predeterminado, cree un objeto [**RealTimeStylus**](realtimestylus-class.md) que solo pueda aceptar la entrada de otro **objeto RealTimeStylus.** Para obtener más información sobre cómo conectar dos **objetos RealTimeStylus,** vea [The Cascaded RealTimeStylus Model](the-cascaded-realtimestylus-model.md).

El [**objeto RealTimeStylus**](realtimestylus-class.md) implementa la [interfaz IDisposable.](/dotnet/api/system.idisposable)

## <a name="extending-the-realtimestylus-class"></a>Extensión de la clase RealTimeStylus

Para permitir que los complementos interactúen con el flujo de datos desde el lápiz de tableta, el objeto [**RealTimeStylus**](realtimestylus-class.md) mantiene dos colecciones de complementos, a las que pueden acceder los métodos [**GetStylusSyncPlugin**](/windows/desktop/api/RTSCom/nf-rtscom-irealtimestylus-getstylussyncplugin) y [**GetStylusAsyncPlugin**](/windows/desktop/api/RTSCom/nf-rtscom-irealtimestylus-getstylusasyncplugin) en C++ y las propiedades [SyncPluginCollection](/previous-versions/ms824833(v=msdn.10)) y [AsyncPluginCollection](/previous-versions/ms824831(v=msdn.10)) en código administrado. Puede agregar un complemento llamando a [**AddStylusSyncPlugin**](/windows/desktop/api/RTSCom/nf-rtscom-irealtimestylus-addstylussyncplugin) o al método [**AddStylusAsyncPlugin**](/windows/desktop/api/RTSCom/nf-rtscom-irealtimestylus-addstylusasyncplugin) de la colección dentro de la propiedad adecuada. Para obtener más información sobre cómo crear y usar complementos, vea Complementos y [la clase RealTimeStylus](plug-ins-and-the-realtimestylus-class.md). Para obtener información sobre cómo decidir si se va a crear un complemento sincrónico o asincrónico para una tarea determinada, vea Consideraciones de [subprocesos](threading-considerations-for-the-stylusinput-apis.md) para las API StylusInput y Consideraciones de rendimiento para las [API StylusInput](performance-considerations-for-the-stylusinput-apis.md).

Los complementos sincrónicos deben implementar la interfaz [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) y los complementos asincrónicos deben implementar la [**interfaz IStylusAsyncPlugin.**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) Cada complemento tiene una propiedad [**IStylusSyncPlugin.DataInterest**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-datainterest) o [**IStylusAsyncPlugin.DataInterest.**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-datainterest) El [**objeto RealTimeStylus**](realtimestylus-class.md) solo llama a los métodos de notificación del complemento para los métodos en los que se ha suscrito el complemento. Para obtener más información sobre los métodos de notificación, vea [Datos de complemento y la clase RealTimeStylus](plug-in-data-and-the-realtimestylus-class.md).

El [**objeto RealTimeStylus**](realtimestylus-class.md) implementa la [**interfaz IStylusAsyncPlugin.**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) La única manera de crear una instancia de un objeto **RealTimeStylus** que acepte la entrada de otro objeto **RealTimeStylus** es usar el constructor predeterminado e implementar el modelo **RealTimeStylus** en cascada. Para obtener más información sobre cómo conectar dos **objetos RealTimeStylus,** vea [The Cascaded RealTimeStylus Model](the-cascaded-realtimestylus-model.md).

El [**objeto RealTimeStylus**](realtimestylus-class.md) tiene dos colas internas que llevan los datos del lápiz de tableta, la cola de entrada y la cola de salida. Los datos del lápiz se convierten en instancias de las clases del espacio [de nombres Microsoft.StylusInput.PluginData.](/previous-versions/ms574862(v=vs.100)) En la lista siguiente se describe cómo el **objeto RealTimeStylus** controla los datos del lápiz de tableta.

1.  El [**objeto RealTimeStylus**](realtimestylus-class.md) comprueba primero los objetos de datos de complemento en su cola de entrada y, a continuación, desde el flujo de datos del lápiz de tableta.
2.  El [**objeto RealTimeStylus**](realtimestylus-class.md) envía un objeto de datos de complemento a los objetos de su colección de complementos sincrónica. Cada complemento sincrónico puede agregar datos a la cola de entrada o salida.
3.  Una vez que el objeto de datos del complemento se ha enviado a todos los miembros de la colección de complementos sincrónica, el objeto de datos del complemento se coloca en la cola de salida del objeto [**RealTimeStylus.**](realtimestylus-class.md)
4.  A [**continuación, el objeto RealTimeStylus**](realtimestylus-class.md) comprueba si hay que procesar el siguiente objeto de datos del complemento.
5.  Aunque la cola de salida del objeto [**RealTimeStylus**](realtimestylus-class.md) contiene datos, el objeto **RealTimeStylus** envía un objeto de datos de complemento desde su cola de salida a los objetos de su colección de complementos asincrónica. Cada complemento asincrónico puede agregar datos a la cola de entrada o salida, pero dado que los complementos asincrónicos se ejecutan en el subproceso de la interfaz de usuario (UI), los datos se agregan a la cola en relación con los datos del lápiz actual que el objeto **RealTimeStylus** está procesando y no en relación con los datos que el complemento asincrónico está procesando.

En el diagrama siguiente se muestra el flujo de datos de lápiz de tableta a través del objeto [**RealTimeStylus**](realtimestylus-class.md) y sus colecciones de complementos.

![ilustración que muestra el flujo de datos de lápiz de pc de tableta](images/5a698bc9-833b-4b24-9fa2-70be0ca61032.gif)

En este diagrama, los círculos con las letras "A" y "B" representan datos de lápiz de tableta que ya se han agregado a la cola de salida del objeto [**RealTimeStylus**](realtimestylus-class.md) y que aún no se han enviado a la colección asincrónica de complementos. El círculo con letra "C" representa los datos del lápiz de tableta que el objeto **RealTimeStylus** está procesando actualmente. Se envía a la colección de complementos sincrónica y se coloca en la cola de salida. El círculo vacío representa la posición en la cola de salida donde se agregan los datos futuros del lápiz de tableta.

Para obtener más información sobre cómo se agregan datos específicos a la cola y se procesan, vea Datos de complemento y la clase [RealTimeStylus](plug-in-data-and-the-realtimestylus-class.md).

A continuación se muestra un escenario mínimo para usar el [**objeto RealTimeStylus**](realtimestylus-class.md) en un formulario que recopila lápiz.

1.  Cree un formulario que implemente la [**interfaz IStylusAsyncPlugin.**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin)
2.  Cree un [**objeto RealTimeStylus**](realtimestylus-class.md) asociado a un control en el formulario.
3.  Establezca interés en las notificaciones StylusDown, Packets y StylusUp en la propiedad [**IStylusAsyncPlugin.DataInterest del**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-datainterest) formulario.
4.  En los métodos [**StylusDown,**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-stylusdown) [**Packets**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-packets)y [**StylusUp**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-stylusup) del formulario, agregue código para controlar el lápiz óptico hacia abajo, los paquetes y las notificaciones de lápiz óptico que se envían desde el objeto [**RealTimeStylus**](realtimestylus-class.md) del formulario.

Para obtener un ejemplo de este tipo de aplicación, vea realTimeStylus Ink Collection Sample ( Ejemplo de colección de [lápiz de RealTimeStylus).](realtimestylus-ink-collection-sample.md)

## <a name="working-with-tablet-objects"></a>Trabajar con objetos de tableta

Cada objeto [**RealTimeStylus**](realtimestylus-class.md) habilitado mantiene una lista de identificadores únicos para los objetos [**de tableta**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) con los que puede interactuar. El objeto **RealTimeStylus** expone dos métodos para traducir entre el identificador único y el objeto **Tablet:** los métodos [**GetTabletContextIdFromTablet**](/windows/desktop/api/RTSCom/nf-rtscom-irealtimestylus-gettabletcontextidfromtablet) y [**GetTabletFromTabletContextId.**](/windows/desktop/api/RTSCom/nf-rtscom-irealtimestylus-gettabletfromtabletcontextid)

El [objeto TabletPropertyDescription](/previous-versions/ms827769(v=msdn.10)) (en código administrado) contiene una propiedad [PacketPropertyId](/previous-versions/ms827780(v=msdn.10)) y una [estructura TabletPropertyMetrics](/previous-versions/ms827781(v=msdn.10)) que describe el intervalo, la resolución y las unidades de la propiedad para un objeto [**Tablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) específico. El método [**GetDesiredPacketDescription**](/windows/desktop/api/RTSCom/nf-rtscom-irealtimestylus-getdesiredpacketdescription) del objeto [**RealTimeStylus**](realtimestylus-class.md) devuelve una matriz de identificadores únicos globales (GUID) para las propiedades de paquete que el objeto **RealTimeStylus** reenvía a sus complementos cuando esas propiedades de paquete están disponibles. Para modificar el conjunto de propiedades de paquete que el objeto **RealTimeStylus** pasa a sus complementos, llame al método [**SetDesiredPacketDescription**](/windows/desktop/api/RTSCom/nf-rtscom-irealtimestylus-setdesiredpacketdescription) del objeto **RealTimeStylus.** El [método GetTabletPropertyDescriptionCollection](/previous-versions/ms825935(v=msdn.10)) (en código administrado) del objeto **RealTimeStylus** toma un identificador de tableta único y devuelve una colección de [objetos TabletPropertyDescription.](/previous-versions/ms827760(v=msdn.10)) Estas propiedades de paquete representan el subconjunto de propiedades compatibles con la tableta que devuelve el **método GetDesiredPacketDescription.**

Para obtener una lista de los GUID de propiedad de paquete estándar, vea la [clase PacketPropertyGuids Constants.](packetpropertyguids-constants.md)

## <a name="special-considerations"></a>Consideraciones especiales

En la lista siguiente se describen otros puntos que se deben tener en cuenta al usar el objeto [**RealTimeStylus**](realtimestylus-class.md) con un [**objeto Tablet.**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet)

-   Solo [**se puede llamar al método SetDesiredPacketDescription**](/windows/desktop/api/RTSCom/nf-rtscom-irealtimestylus-setdesiredpacketdescription) mientras el objeto [**Tablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) está deshabilitado. El [**objeto RealTimeStylus**](realtimestylus-class.md) puede modificar la lista de propiedades de paquete deseadas; Por lo tanto, llame al [**método GetDesiredPacketDescription**](/windows/desktop/api/RTSCom/nf-rtscom-irealtimestylus-getdesiredpacketdescription) después de llamar al método **SetDesiredPacketDescription** para determinar qué propiedades de paquete puede reenviar el objeto **RealTimeStylus** a sus complementos. Solo se garantiza que una tableta admita los **valores X**, **Y** y **PacketStatus** para [PacketProperty](packetproperty-guids.md). Por lo tanto, es posible que el diseño del complemento tenga en cuenta la recepción de menos propiedades de paquete de las deseadas.
-   Solo se puede llamar al método [GetTabletPropertyDescriptionCollection](/previous-versions/ms825935(v=msdn.10)) (para código administrado) mientras el objeto [**RealTimeStylus**](realtimestylus-class.md) está habilitado. Dado que la notificación se puede enviar a los complementos asincrónicos una vez deshabilitado el objeto **RealTimeStylus,** es posible que deba almacenar en caché la información de cada [**objeto Tablet.**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) El método GetTabletPropertyDescriptionCollection devuelve una lista de las propiedades de paquete deseadas que son compatibles con la tableta especificada.
-   Cuando el [**objeto RealTimeStylus**](realtimestylus-class.md) está habilitado, cada complemento recibe una llamada a su [**método RealTimeStylusEnabled.**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-realtimestylusenabled) El [objeto RealTimeStylusEnabledData](/previous-versions/ms824229(v=msdn.10)) pasado en la notificación contiene una colección de los identificadores de contexto para las tabletas disponibles en el momento en que se habilita el objeto **RealTimeStylus.**
-   Cuando una tableta que el objeto [**RealTimeStylus**](realtimestylus-class.md) puede usar se agrega o quita del tablet PC mientras el objeto **RealTimeStylus** está habilitado, el objeto **RealTimeStylus** notifica a sus complementos que se ha agregado o quitado un objeto [**Tablet.**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) Para obtener más información, [vea Datos de complemento y la clase RealTimeStylus](plug-in-data-and-the-realtimestylus-class.md).

## <a name="working-with-tablet-pens"></a>Trabajar con tabletas lápices

El [**objeto RealTimeStylus**](realtimestylus-class.md) pasa información sobre el lápiz de tableta a sus complementos en varios de los métodos de notificación. La información sobre el lápiz de tableta se representa mediante un [objeto Stylus,](/previous-versions/ms824824(v=msdn.10)) obtenido a través del [**método GetStyluses.**](/windows/desktop/api/RTSCom/nf-rtscom-irealtimestylus-getstyluses) Este objeto es una representación del lápiz de tableta en el momento en que se recopilaron los datos. Dado que los complementos reciben los datos del lápiz de tableta como parte del flujo de datos del lápiz de tableta, los complementos deben usar la información del objeto Stylus en lugar de comprobar el estado actual de un lápiz de tableta determinado a través de la [**clase Cursor.**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) Para obtener información sobre cómo se pasan los datos del lápiz de tableta y del botón de lápiz de tableta a los complementos, vea Datos de complementos y la clase [RealTimeStylus](plug-in-data-and-the-realtimestylus-class.md).

Para obtener una matriz de los objetos [Stylus](/previous-versions/ms824824(v=msdn.10)) que ha encontrado el objeto [**RealTimeStylus**](realtimestylus-class.md) desde que se ha habilitado por última vez, use el método [**GetStyluses**](/windows/desktop/api/RTSCom/nf-rtscom-irealtimestylus-getstyluses) del objeto **RealTimeStyluss.**

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Microsoft.Ink.Tablet](/previous-versions/ms827783(v=msdn.10))
</dt> <dt>

[Microsoft.StylusInput.RealTimeStylus](/previous-versions/ms585724(v=vs.100))
</dt> <dt>

[Modelo RealTimeStylus en cascada](the-cascaded-realtimestylus-model.md)
</dt> <dt>

[Consideraciones de confianza parcial para las API StylusInput](partial-trust-considerations-for-the-stylusinput-apis.md)
</dt> <dt>

[Datos de complementos y clase RealTimeStylus](plug-in-data-and-the-realtimestylus-class.md)
</dt> <dt>

[Consideraciones sobre subprocesos para las API StylusInput](threading-considerations-for-the-stylusinput-apis.md)
</dt> </dl>

 

 
