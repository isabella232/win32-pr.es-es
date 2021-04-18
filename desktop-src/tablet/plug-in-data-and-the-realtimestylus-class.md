---
description: Los complementos de la clase RealTimeStylus deben implementar la interfaz IStylusSyncPlugin o IStylusAsyncPlugin, o ambos.
ms.assetid: 827ac817-e0e6-4750-9d48-b939ccd5e679
title: Datos de complementos y clase RealTimeStylus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 372b3d297edbad6d339285f45e92118184fa2cfc
ms.sourcegitcommit: ee06501cc29132927ade9813e0888aaa4decc487
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/28/2021
ms.locfileid: "104569809"
---
# <a name="plug-in-data-and-the-realtimestylus-class"></a>Datos de complementos y clase RealTimeStylus

Los complementos de la clase [**RealTimeStylus**](realtimestylus-class.md) deben implementar la interfaz [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) o [**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) , o ambos. Aunque tiene que implementar todos los métodos de interfaz de complemento, el complemento solo recibe llamadas en métodos marcados en la propiedad complementos [Microsoft. StylusInput. IStylusSyncPlugin. Interest](/previous-versions/ms574887(v=vs.100)) o [Microsoft. StylusInput. IStylusAsyncPlugin. Interest](/previous-versions/ms574886(v=vs.100)) .

Los métodos definidos en las interfaces usan objetos en el espacio de nombres [Microsoft. StylusInput. PluginData](/previous-versions/ms823992(v=msdn.10)) para pasar los datos de lápiz a los complementos. En la tabla siguiente se describen los objetos de datos que son parámetros de los métodos de notificación y se muestra el valor de [DataInterestMask](/previous-versions/ms824787(v=msdn.10)) asociado a la notificación.



| Datos de complemento                                                                                          | Valor DataInterestMask     | Descripción                                                                                                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------------|----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [CustomStylusData](/previous-versions/ms824747(v=msdn.10))                     | **CustomStylusDataAdded**  | Datos de aplicación personalizados que agrega un complemento.<br/>                                                                                                                                                                                                 |
| [Datoserror](/previous-versions/ms824740(v=msdn.10))                                   | **Error**                  | Información de error que el objeto [**RealTimeStylus**](realtimestylus-class.md) agrega como respuesta a una excepción no controlada en uno de sus complementos.<br/>                                                                                          |
| [InAirPacketsData](/previous-versions/ms824592(v=msdn.10))                     | **InAirPackets**           | Información de paquetes para el movimiento del lápiz mientras el lápiz está en el aire por encima del digitalizador.<br/>                                                                                                                                                         |
| [PacketsData](/previous-versions/ms824590(v=msdn.10))                               | **Paquetes**                | Información de paquetes para el movimiento del lápiz mientras el lápiz toca el digitalizador.<br/>                                                                                                                                                             |
| [RealTimeStylusDisabledData](/previous-versions/ms824576(v=msdn.10)) | **RealTimeStylusDisabled** | Información que el objeto [**RealTimeStylus**](realtimestylus-class.md) agrega cuando se deshabilita.<br/>                                                                                                                                        |
| [RealTimeStylusEnabledData](/previous-versions/ms824229(v=msdn.10))   | **RealTimeStylusEnabled**  | Información que el objeto [**RealTimeStylus**](realtimestylus-class.md) agrega cuando se habilita.<br/>                                                                                                                                         |
| [StylusButtonDownData](/previous-versions/ms824181(v=msdn.10))             | **StylusButtonDown**       | Información sobre el botón específico del lápiz óptico que se está presionando.<br/>                                                                                                                                                                        |
| [StylusButtonUpData](/previous-versions/ms824172(v=msdn.10))                 | **StylusButtonUp**         | Información sobre el botón específico del lápiz que se va a liberar.<br/>                                                                                                                                                                       |
| [StylusDownData](/previous-versions/ms585582(v=vs.100))                                   | **StylusDown**             | La información de paquetes de un lápiz óptico a medida que el lápiz óptico se pone en contacto con el digitalizador.<br/>                                                                                                                                                      |
| [StylusInRangeData](/previous-versions/ms824090(v=msdn.10))                   | **StylusInRange**          | Información sobre el lápiz específico que está entrando en el área de entrada del objeto [**RealTimeStylus**](realtimestylus-class.md) o especificando el intervalo de detección del digitalizador por encima del área de entrada del objeto **RealTimeStylus** .<br/> |
| [StylusOutOfRangeData](/previous-versions/ms824072(v=msdn.10))             | **StylusOutOfRange**       | Información sobre el lápiz específico que sale del área de entrada del objeto [**RealTimeStylus**](realtimestylus-class.md) o que sale del intervalo de detección del digitalizador por encima del área de entrada del objeto **RealTimeStylus** .<br/>   |
| [StylusUpData](/previous-versions/ms824057(v=msdn.10))                             | **StylusUp**               | La información de paquetes para un lápiz óptico como el lápiz se levanta del digitalizador.<br/>                                                                                                                                                                  |
| [SystemGestureData](/previous-versions/ms824019(v=msdn.10))                   | **SystemGesture**          | Información que el objeto [**RealTimeStylus**](realtimestylus-class.md) agrega cuando detecta un gesto del sistema.<br/>                                                                                                                                 |
| [TabletAddedData](/previous-versions/ms824010(v=msdn.10))                       | **TabletAdded**            | Información sobre el objeto de [tableta](/previous-versions/ms827783(v=msdn.10)) que se va a agregar.<br/>                                                                                                                                                |
| [TabletRemovedData](/previous-versions/ms823997(v=msdn.10))                   | **TabletRemoved**          | Información sobre el objeto de [tableta](/previous-versions/ms827783(v=msdn.10)) que se va a quitar.<br/>                                                                                                                                              |



 

Para obtener información sobre cómo el objeto [**RealTimeStylus**](realtimestylus-class.md) controla el flujo de datos del lápiz de Tablet PC, vea [trabajar con la clase RealTimeStylus](working-with-the-realtimestylus-class.md).

## <a name="data-interest"></a>Interés de datos

El objeto [**RealTimeStylus**](realtimestylus-class.md) comprueba la propiedad [Microsoft. StylusInput. IStylusSyncPlugin. Interest](/previous-versions/ms574887(v=vs.100)) o [Microsoft. StylusInput. IStylusAsyncPlugin. de interés](/previous-versions/ms574886(v=vs.100)) de un complemento cuando el complemento se agrega a la colección de complementos sincrónica o asincrónica del objeto **RealTimeStylus** . Por lo tanto, debe usar la propiedad de interés para suscribirse a todas las notificaciones que utiliza esta instancia de su complemento, pero con poca frecuencia, pero no a ninguna de las notificaciones que esta instancia del complemento nunca usa. En el caso de las notificaciones que el complemento solo usa ocasionalmente, compruebe primero el estado del complemento en el método de notificación y devuelva si el complemento no utiliza la notificación en su estado actual.

Un complemento solo recibe llamadas en métodos marcados en la propiedad [Microsoft. StylusInput. IStylusSyncPlugin. Interest](/previous-versions/ms574887(v=vs.100)) o [Microsoft. StylusInput. IStylusAsyncPlugin. Interest](/previous-versions/ms574886(v=vs.100)) del complemento. Para obtener más información acerca de los posibles valores de la propiedad de los datos de **interés** de un complemento, vea la enumeración [DataInterestMask](/previous-versions/ms824787(v=msdn.10)) .

## <a name="timing"></a>Control de tiempo

Los datos se ponen en cola en el objeto [**RealTimeStylus**](realtimestylus-class.md) antes de pasarlos a los complementos de la colección de complementos asincrónica. En la lista siguiente se describen algunas situaciones en las que es posible que tenga que tener en cuenta al diseñar un complemento asincrónico.

-   Cuando el objeto [**RealTimeStylus**](realtimestylus-class.md) está deshabilitado, el complemento asincrónico puede recibir otras notificaciones en cola antes de que se llame a su método [RealTimeStylusDisabled](/previous-versions/ms824774(v=msdn.10)) . En esta situación, las llamadas desde el complemento a algunos de los métodos y propiedades del objeto **RealTimeStylus** producen una excepción. La información relevante para el complemento debe almacenarse en caché cuando el objeto **RealTimeStylus** está habilitado.
-   El método [ClearStylusQueues](/previous-versions/ms825781(v=msdn.10)) del objeto [**RealTimeStylus**](realtimestylus-class.md) puede quitar información de la cola de salida. Por lo tanto, los complementos asincrónicos no pueden confiar en recibir todas las notificaciones pertinentes.
-   Cuando se quita un objeto de [Tablet PC](/previous-versions/ms827783(v=msdn.10)) que está disponible para el objeto [**RealTimeStylus**](realtimestylus-class.md) , el complemento asincrónico puede recibir la notificación del lápiz en cola para la tableta antes de que se llame a su método [TabletRemoved](/previous-versions/bb361092(v=vs.100)) . En esta situación, la llamada al método [GetTabletPropertyDescriptionCollection](/previous-versions/ms825935(v=msdn.10)) del objeto **RealTimeStylus** no funciona. La información relevante para el complemento debe almacenarse en caché cuando el objeto **RealTimeStylus** está habilitado o cuando se agrega una nueva tableta.

Dependiendo de la aplicación, puede mejorar el rendimiento al deshabilitar un objeto [**RealTimeStylus**](realtimestylus-class.md) . Cuando la propiedad [Enabled](/previous-versions/ms824832(v=msdn.10)) del objeto **RealTimeStylus** está establecida en **false**, los datos de las colas de entrada y salida se procesan hasta que las colas están vacías. Puede llamar al método [ClearStylusQueues](/previous-versions/ms825781(v=msdn.10)) del objeto **RealTimeStylus** para borrar las colas antes de deshabilitar el objeto **RealTimeStylus** .

## <a name="enabled-and-disabled-data"></a>Datos habilitados y deshabilitados

Cuando el objeto [**RealTimeStylus**](realtimestylus-class.md) está habilitado, cada complemento recibe una llamada a su método [Microsoft. StylusInput. IStylusSyncPlugin. RealTimeStylusEnabled](/previous-versions/ms824758(v=msdn.10)) o [Microsoft. StylusInput. IStylusAsyncPlugin. RealTimeStylusEnabled](/previous-versions/ms824775(v=msdn.10)) . El objeto **RealTimeStylusEnabledData** pasado en la notificación contiene una colección de los identificadores de contexto para las tabletas disponibles en el momento en que se habilita el objeto **RealTimeStylus** .

> [!Note]  
> Dado que los datos del complemento de la colección de complementos asincrónicos del objeto [**RealTimeStylus**](realtimestylus-class.md) están en cola, los complementos asincrónicos pueden recibir datos antes de recibir una llamada a su método [RealTimeStylusDisabled](/previous-versions/ms824774(v=msdn.10)) , pero después de que el objeto **RealTimeStylus** esté deshabilitado. Tenga en cuenta que algunos de los métodos y propiedades del objeto **RealTimeStylus** producen una excepción si el objeto **RealTimeStylus** está deshabilitado.

 

El objeto [**RealTimeStylus**](realtimestylus-class.md) llama a los métodos [Microsoft. StylusInput. IStylusSyncPlugin. RealTimeStylusEnabled](/previous-versions/ms824758(v=msdn.10)) y [Microsoft. StylusInput. IStylusSyncPlugin. RealTimeStylusDisabled](/previous-versions/ms824757(v=msdn.10)) en el subproceso en el que está habilitado el objeto **RealTimeStylus** o desde el que se agrega el complemento sincrónico.

Por lo general, agregar o quitar complementos mientras el objeto [**RealTimeStylus**](realtimestylus-class.md) está deshabilitado. Para obtener más información sobre cómo agregar y quitar complementos en el objeto **RealTimeStylus** , vea [Complementos y la clase RealTimeStylus](plug-ins-and-the-realtimestylus-class.md).

## <a name="tablet-data"></a>Datos de Tablet PC

Cuando se agrega o se quita una tableta que puede usar el objeto [**RealTimeStylus**](realtimestylus-class.md) en Tablet PC mientras el objeto **RealTimeStylus** está habilitado, el objeto **RealTimeStylus** notifica a sus complementos que se ha agregado o quitado un objeto de [tableta](/previous-versions/ms827783(v=msdn.10)) . Cada objeto **RealTimeStylus** mantiene una lista de identificadores únicos para los objetos de Tablet PC con los que puede interactuar. El objeto **RealTimeStylus** tiene dos métodos para la conversión entre el identificador único y el objeto de tableta, los métodos [GetTabletContextIdFromTablet](/previous-versions/ms825922(v=msdn.10)) y [GetTabletFromTabletContextId](/previous-versions/ms825929(v=msdn.10)) .

> [!Note]  
> La información sobre una tableta ya no está disponible en el objeto [**RealTimeStylus**](realtimestylus-class.md) después de quitar la tableta del Tablet PC.

 

## <a name="tablet-pen-data"></a>Datos del lápiz de Tablet PC

El objeto [**RealTimeStylus**](realtimestylus-class.md) pasa información sobre el lápiz de Tablet PC a sus complementos en una serie de métodos de notificación. La información sobre el lápiz de Tablet PC se representa mediante un objeto de [lápiz](/previous-versions/ms824824(v=msdn.10)) . Este objeto es una instantánea del estado del lápiz de Tablet PC en el momento en que se recopilaron los datos. Dado que los complementos reciben los datos del lápiz de Tablet PC como parte del flujo de datos del lápiz de Tablet PC, los complementos deben usar la información del objeto de lápiz en lugar de comprobar el estado actual de un lápiz de Tablet PC determinado a través de la clase [cursor](/previous-versions/ms839521(v=msdn.10)) .

Cada objeto de [lápiz](/previous-versions/ms824824(v=msdn.10)) contiene el identificador de contexto de Tablet PC que generó los datos.

## <a name="system-gesture-data"></a>Datos de gestos del sistema

El objeto [**RealTimeStylus**](realtimestylus-class.md) recibe datos acerca de los gestos del sistema, ya que los reconoce Tablet PC. En la tabla siguiente se describe el orden en que se producen los objetos [SystemGestureData](/previous-versions/ms824019(v=msdn.10)) en el flujo de datos del lápiz de Tablet PC con respecto a otros datos del lápiz de Tablet PC.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><a href="/previous-versions/ms827134(v=msdn.10)">SystemGesture</a></th>
<th>Objetos que preceden al objeto <a href="/previous-versions/ms824019(v=msdn.10)">SystemGestureData</a></th>
<th>Objetos que van después del objeto <a href="/previous-versions/ms824019(v=msdn.10)">SystemGestureData</a></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Pulsar</strong></td>
<td>El objeto <a href="/previous-versions/ms824107(v=msdn.10)">StylusDownData</a> .<br/></td>
<td>El objeto [StylusUpData](/previous-versions/ms824057(v=msdn.10)) .<br/></td>
</tr>
<tr class="even">
<td><strong>DoubleTap</strong></td>
<td>El objeto <a href="/previous-versions/ms824107(v=msdn.10)">StylusDownData</a> , el objeto <a href="/previous-versions/ms824019(v=msdn.10)">SystemGestureData</a> para el gesto del sistema <strong>TAP</strong> y los objetos [StylusUpData](/previous-versions/ms824057(v=msdn.10)) .<br/></td>
<td>El segundo objeto <a href="/previous-versions/ms824107(v=msdn.10)">StylusDownData</a> .<br/></td>
</tr>
<tr class="odd">
<td><strong>RightTap</strong></td>
<td>El objeto <a href="/previous-versions/ms824107(v=msdn.10)">StylusDownData</a> y el objeto <a href="/previous-versions/ms824019(v=msdn.10)">SystemGestureData</a> para el miembro <strong>HoldEnter</strong> de la enumeración <a href="/previous-versions/ms827134(v=msdn.10)">SystemGesure</a> .<br/></td>
<td>El objeto [StylusUpData](/previous-versions/ms824057(v=msdn.10)) .<br/></td>
</tr>
<tr class="even">
<td><strong>Arrastre</strong></td>
<td>El objeto <a href="/previous-versions/ms824107(v=msdn.10)">StylusDownData</a> .<br/></td>
<td>El objeto [StylusUpData](/previous-versions/ms824057(v=msdn.10)) .<br/></td>
</tr>
<tr class="odd">
<td><strong>RightDrag</strong></td>
<td>El objeto <a href="/previous-versions/ms824107(v=msdn.10)">StylusDownData</a> .<br/></td>
<td>El objeto [StylusUpData](/previous-versions/ms824057(v=msdn.10)) .<br/></td>
</tr>
<tr class="even">
<td><strong>HoldEnter</strong></td>
<td>El objeto <a href="/previous-versions/ms824107(v=msdn.10)">StylusDownData</a> .<br/></td>
<td>El objeto [StylusUpData](/previous-versions/ms824057(v=msdn.10)) .<br/>
<blockquote>
[!Note]<br />
Este gesto del sistema no se reconoce si el usuario inicia un gesto del sistema de <strong>arrastrar</strong> o <strong>RightDrag</strong> .
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><strong>HoldLeave</strong></td>
<td>Sin implementar.<br/></td>
<td>Sin implementar.<br/></td>
</tr>
<tr class="even">
<td><strong>HoverEnter</strong></td>
<td>Varios objetos <a href="/previous-versions/ms824592(v=msdn.10)">InAirPacketsData</a> de velocidad media baja.<br/></td>
<td><blockquote>
[!Note]<br />
Puede haber un retraso apreciable antes de recibir el gesto del sistema <strong>HoverEnter</strong> . El objeto <a href="realtimestylus-class.md"><strong>RealTimeStylus</strong></a> solo recibe estos datos si el objeto <strong>RealTimeStylus</strong> se adjunta a la ventana o control que está directamente debajo del lápiz en el momento del gesto del sistema.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><strong>HoverLeave</strong></td>
<td>El objeto <a href="/previous-versions/ms824019(v=msdn.10)">SystemGestureData</a> para el gesto del sistema <strong>HoverEnter</strong> y varios objetos <a href="/previous-versions/ms824592(v=msdn.10)">InAirPacketsData</a> de velocidad media suficiente.<br/></td>
<td><blockquote>
[!Note]<br />
Puede haber un retraso apreciable antes de recibir el gesto del sistema <strong>HoverLeave</strong> . El objeto <a href="realtimestylus-class.md"><strong>RealTimeStylus</strong></a> solo recibe estos datos si el objeto <strong>RealTimeStylus</strong> se adjunta a la ventana o control que está directamente debajo del lápiz en el momento del gesto del sistema.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

## <a name="custom-stylus-data"></a>Datos personalizados del lápiz

Los datos personalizados del lápiz se pueden agregar al objeto [**RealTimeStylus**](realtimestylus-class.md) llamando al método [AddCustomStylusDataToQueue](/previous-versions/ms825761(v=msdn.10)) . Los datos personalizados del lápiz se pueden agregar a las colas del objeto **RealTimeStylus** en uno de tres lugares.

-   Cuando el parámetro *Queue* se establece en **Output**, los datos personalizados se agregan a la cola de salida del objeto [**RealTimeStylus**](realtimestylus-class.md) después de los datos que la colección de complementos sincrónicos procesa actualmente.
-   Cuando el parámetro *Queue* se establece en **OutputImmediate**, los datos personalizados se agregan a la cola de salida del objeto [**RealTimeStylus**](realtimestylus-class.md) antes de los datos que la colección de complementos sincrónicos procesa actualmente.
-   Cuando el parámetro *Queue* se establece en **Input**, los datos personalizados se agregan a la cola de entrada del objeto [**RealTimeStylus**](realtimestylus-class.md) y se envían a la colección de complementos sincrónicos antes que los nuevos datos del flujo de datos del lápiz de Tablet PC.

En cada uno de los casos anteriores, los datos agregados por complementos posteriores en la colección de complementos sincrónicos se agregan después de los datos agregados por los complementos anteriores.

> [!Note]  
> Si la llamada al método [AddCustomStylusDataToQueue](/previous-versions/ms825761(v=msdn.10)) se realiza desde un complemento sincrónico en respuesta a una llamada a uno de sus métodos [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) , los datos del lápiz personalizado se agregan al flujo de datos del lápiz de Tablet PC de una manera predecible. de lo contrario, se agrega a la cola en relación con los datos actuales del lápiz que está procesando el objeto [**RealTimeStylus**](realtimestylus-class.md) y no con respecto a los datos que procesa el complemento asincrónico. El método AddCustomStylusDataToQueue produce una excepción si el objeto **RealTimeStylus** está deshabilitado.

 

Los datos personalizados del lápiz se agregan a la cola como un objeto [CustomStylusData](/previous-versions/ms824747(v=msdn.10)) y los complementos reciben estos datos a través del método [Microsoft. StylusInput. IStylusSyncPlugin. CustomStylusDataAdded](/previous-versions/ms824753(v=msdn.10)) o [Microsoft. StylusInput.](/previous-versions/ms824770(v=msdn.10)) IStylusAsyncPlugin. CustomStylusDataAdded.

Los objetos [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) y [**GestureRecognizer**](gesturerecognizer-class.md) pueden agregar datos de lápiz personalizados a la cola. Para obtener más información sobre los objetos **DynamicRenderer** y **GestureRecognizer** , consulte complementos [de representadores dinámicos](dynamic-renderer-plug-ins.md) y complementos de [reconocedor](recognizer-plug-ins.md).

El objeto [**RealTimeStylus**](realtimestylus-class.md) llama al método [Microsoft. StylusInput. IStylusSyncPlugin. CustomStylusDataAdded](/previous-versions/ms824753(v=msdn.10)) en el subproceso del que recibe la llamada a su método [AddCustomStylusDataToQueue](/previous-versions/ms825761(v=msdn.10)) .

En el diagrama siguiente se muestra la adición de datos de lápiz personalizados a la cola de salida con el parámetro *Queue* establecido en **Output**.

![Ilustración que muestra el flujo de datos del lápiz óptico personalizado a la cola de salida ](images/27bc3672-41bc-432e-bf41-18e4ccec78f5.gif)

En este diagrama, los círculos "A" y "B" representan los datos del lápiz de Tablet PC que ya se han agregado a la cola de salida del objeto [**RealTimeStylus**](realtimestylus-class.md) y que todavía no se han enviado a la colección de complementos asincrónica. La letra "C" de círculo representa los datos del lápiz de Tablet PC que está procesando actualmente el objeto **RealTimeStylus** . Se envía a la colección de complementos sincrónicos y se coloca en la cola de salida. Los círculos numerados "1", "2" y "3" representan los datos del lápiz óptico que se han agregado a la cola de salida por el primer, segundo y tercer complementos sincrónicos, respectivamente, en respuesta a los datos del lápiz de Tablet PC representados por "C". Los complementos han agregado los datos personalizados del lápiz con el parámetro *Queue* establecido en **StylusQueues**. El círculo vacío representa la posición en la cola de salida donde se agregan los datos futuros del lápiz de Tablet PC.

En el diagrama siguiente se muestra la adición de datos de lápiz personalizados a la cola de salida con el parámetro *Queue* establecido en **OutputImmediate**.

![Diagrama que muestra el flujo de datos del lápiz personalizado a la cola de salida.](images/bcf45325-5557-47a2-af43-142c7684e482.gif)

En este diagrama, los círculos "A" y "B" representan los datos del lápiz de Tablet PC que ya se han agregado a la cola de salida del objeto [**RealTimeStylus**](realtimestylus-class.md) y que todavía no se han enviado a la colección de complementos asincrónica. La letra "C" de círculo representa los datos del lápiz de Tablet PC que está procesando actualmente el objeto **RealTimeStylus** . Se envía a la colección de complementos sincrónicos y se coloca en la cola de salida. Los círculos numerados "1", "2" y "3" representan los datos del lápiz óptico que se han agregado a la cola de salida por el primer, segundo y tercer complementos sincrónicos, respectivamente, en respuesta a los datos del lápiz de Tablet PC representados por "C". Los complementos han agregado los datos personalizados del lápiz con el parámetro *Queue* establecido en **OutputImmediate**. El círculo vacío representa la posición en la cola de salida donde se agregan los datos futuros del lápiz de Tablet PC.

En el diagrama siguiente se muestra la adición de datos de lápiz personalizados a la cola de entrada.

![Ilustración que muestra el flujo de datos del lápiz óptico personalizado a la cola de salida](images/5dd2cfcc-1086-49b0-a0d5-9276c13c7f61.gif)

En este diagrama, los círculos "A" y "B" representan los datos del lápiz de Tablet PC que ya se han agregado a la cola de salida del objeto [**RealTimeStylus**](realtimestylus-class.md) y que todavía no se han enviado a la colección de complementos asincrónica. La letra "C" de círculo representa los datos del lápiz de Tablet PC que está procesando actualmente el objeto **RealTimeStylus** . Se envía a la colección de complementos sincrónicos y se coloca en la cola de salida. Los círculos numerados "1", "2" y "3" representan los datos del lápiz óptico que se han agregado a la cola de entrada por el primer, segundo y tercer complementos sincrónicos, respectivamente, en respuesta a los datos del lápiz de Tablet PC representados por "C". Los complementos han agregado los datos personalizados del lápiz con el parámetro *Queue* establecido en **Input**. A continuación, se pasan los datos del lápiz óptico con el número "1" a los complementos sincrónicos y, a continuación, a la cola de salida antes de que los datos del lápiz personalizado tengan el número "2" y "3", que se procesan antes de que se procesen los siguientes datos del lápiz de Tablet PC. El círculo vacío representa la posición en la cola de salida donde se agregan los datos futuros del lápiz de Tablet PC.

## <a name="error-data"></a>Datos de error

Cuando un complemento inicia una excepción, se interrumpe el flujo de datos normal. El objeto [**RealTimeStylus**](realtimestylus-class.md) genera un objeto [datoserror](/previous-versions/ms824740(v=msdn.10)) y llama a:

-   El método [Microsoft. StylusInput. IStylusSyncPlugin. error](/previous-versions/ms824754(v=msdn.10)) o [Microsoft. StylusInput. IStylusAsyncPlugin. error](/previous-versions/ms824771(v=msdn.10)) del complemento que produjo la excepción.
-   El método [Microsoft. StylusInput. IStylusSyncPlugin. error](/previous-versions/ms824754(v=msdn.10)) o [Microsoft. StylusInput. IStylusAsyncPlugin. error](/previous-versions/ms824771(v=msdn.10)) del resto de complementos de la colección.

Si el complemento que inició la excepción es un complemento sincrónico, el objeto [datoserror](/previous-versions/ms824740(v=msdn.10)) se agrega a la cola de salida. Después, el objeto [**RealTimeStylus**](realtimestylus-class.md) reanuda el procesamiento normal de los datos originales.

En el diagrama siguiente se muestra la adición de datos de error a los datos del lápiz de Tablet PC.

![flujo de datos del lápiz óptico personalizado a la cola de salida con la adición de datos de error](images/c2f79abe-aeb5-498f-b389-1fad9bf01a13.gif)

En este diagrama, los círculos "A" y "B" representan los datos del lápiz de Tablet PC que ya se han agregado a la cola de salida del objeto [**RealTimeStylus**](realtimestylus-class.md) y que todavía no se han enviado a la colección de complementos asincrónica. La letra "C" de círculo representa los datos del lápiz de Tablet PC que está procesando actualmente el objeto **RealTimeStylus** . La letra "e" en un círculo representa un objeto [datoserror](/previous-versions/ms824740(v=msdn.10)) generado por el objeto **RealTimeStylus** cuando el segundo complemento sincrónico, el complemento sincrónico 2, produce una excepción mientras está procesando "C". A continuación, el objeto **RealTimeStylus** pone en pausa su procesamiento de "C" y pasa "e" al complemento que generó la excepción y todos los complementos posteriores. A continuación, el objeto **RealTimeStylus** coloca "e" en la cola de salida y reanuda su procesamiento de "C", que se pasa a los complementos restantes de la colección de complementos sincrónicos y se coloca en la cola de salida después de "e". El círculo vacío representa la posición en la cola de salida donde se agregan los datos futuros del lápiz de Tablet PC.

Si un complemento produce una excepción de su método de error, el objeto [**RealTimeStylus**](realtimestylus-class.md) detecta la excepción pero no genera un nuevo objeto [datoserror](/previous-versions/ms824740(v=msdn.10)) . Esto es para evitar la recursividad.

Los datos de error se agregan a la cola de salida después de cualquier dato de lápiz personalizado que se agregue en la posición **OutputImmediate** antes de la excepción que creó los datos de error y antes de cualquier dato de lápiz personalizado que se agregue en la posición **OutputImmediate** por complementos posteriores en la colección de complementos sincrónicos.

En el diagrama siguiente se muestra cómo se agregan los datos de error a la cola de salida en relación con los datos personalizados que se agregan a la cola **OutputImmediate** .

![datos de error agregados a la cola de salida en relación con los datos personalizados agregados a la cola outputimmediate.](images/b00320c4-6fe7-439d-9855-e5f131feeb69.gif)

En este diagrama, los círculos "A" y "B" representan los datos del lápiz de Tablet PC que ya se han agregado a la cola de salida del objeto [**RealTimeStylus**](realtimestylus-class.md) y que todavía no se han enviado a la colección de complementos asincrónica. La letra "C" de círculo representa los datos del lápiz de Tablet PC que está procesando actualmente el objeto **RealTimeStylus** . Los círculos numerados con "1", "2" y "3" se agregan por el primer, segundo y tercer complementos sincrónicos, respectivamente, a la cola **OutputImmediate** en respuesta a los datos representados por la letra "C" del círculo. La letra "e" de Circle representa los datos de error generados en respuesta a una excepción producida por el segundo complemento después del segundo complemento agregando datos personalizados a la cola de salida en la posición **OutputImmediate** .

Si cualquier complemento sincrónico agrega datos de lápiz personalizados a la cola de entrada en respuesta a los datos de error, los datos se agregan inmediatamente antes de los datos de error. Si alguno de los complementos sincrónicos agrega datos de lápiz personalizados a la cola de salida en la posición de **salida** en respuesta a los datos de error, los datos se agregan inmediatamente después de los datos de error.

El objeto [**RealTimeStylus**](realtimestylus-class.md) llama al método [Microsoft. StylusInput. IStylusSyncPlugin. error](/previous-versions/ms824754(v=msdn.10)) en el subproceso del que se produce la excepción.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Microsoft. Ink. Tablet](/previous-versions/ms827783(v=msdn.10))
</dt> <dt>

[Microsoft. StylusInput. PluginData](/previous-versions/ms823992(v=msdn.10))
</dt> <dt>

[Microsoft. StylusInput. DataInterestMask](/previous-versions/ms575174(v=vs.100))
</dt> <dt>

[Microsoft. StylusInput. RealTimeStylus](/previous-versions/ms824830(v=msdn.10))
</dt> <dt>

[Trabajar con la clase RealTimeStylus](working-with-the-realtimestylus-class.md)
</dt> </dl>

 

 
