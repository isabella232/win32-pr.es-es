---
description: Los complementos de la clase RealTimeStylus deben implementar la interfaz IStylusSyncPlugin o IStylusAsyncPlugin, o ambas.
ms.assetid: 827ac817-e0e6-4750-9d48-b939ccd5e679
title: Datos de complementos y clase RealTimeStylus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dac0540d90f291acfef27a09df08ffff645c280d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127361019"
---
# <a name="plug-in-data-and-the-realtimestylus-class"></a>Datos de complementos y clase RealTimeStylus

Los complementos de la clase [**RealTimeStylus**](realtimestylus-class.md) deben implementar la interfaz [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) o [**IStylusAsyncPlugin,**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) o ambas. Aunque tiene que implementar todos los métodos de interfaz de complemento, el complemento solo recibe llamadas en los métodos marcados en la propiedad [Microsoft.StylusInput.IStylusSyncPlugin.DataInterest](/previous-versions/ms574887(v=vs.100)) o [Microsoft.StylusInput.IStylusAsyncPlugin.DataInterest.](/previous-versions/ms574886(v=vs.100))

Los métodos definidos en las interfaces usan objetos del espacio de nombres [Microsoft.StylusInput.PluginData](/previous-versions/ms823992(v=msdn.10)) para pasar los datos del lápiz a los complementos. En la tabla siguiente se describen los objetos de datos que son parámetros en los métodos de notificación y se muestra el [valor DataInterestMask](/previous-versions/ms824787(v=msdn.10)) asociado a la notificación.



| Datos de complemento                                                                                          | Valor de DataInterestMask     | Descripción                                                                                                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------------|----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [CustomStylusData](/previous-versions/ms824747(v=msdn.10))                     | **CustomStylusDataAdded**  | Datos de aplicación personalizados que agrega un complemento.<br/>                                                                                                                                                                                                 |
| [ErrorData](/previous-versions/ms824740(v=msdn.10))                                   | **Error**                  | Información de error que el [**objeto RealTimeStylus**](realtimestylus-class.md) agrega en respuesta a una excepción no controlada en uno de sus complementos.<br/>                                                                                          |
| [InAirPacketsData](/previous-versions/ms824592(v=msdn.10))                     | **InAirPackets**           | Información de paquetes para el movimiento del lápiz mientras el lápiz está en el aire sobre el digitalizador.<br/>                                                                                                                                                         |
| [PacketsData](/previous-versions/ms824590(v=msdn.10))                               | **Paquetes**                | Información de paquetes para el movimiento del lápiz mientras el lápiz está tocándose el digitalizador.<br/>                                                                                                                                                             |
| [RealTimeStylusDisabledData](/previous-versions/ms824576(v=msdn.10)) | **RealTimeStylusDisabled** | Información que agrega el objeto [**RealTimeStylus**](realtimestylus-class.md) cuando se deshabilita.<br/>                                                                                                                                        |
| [RealTimeStylusEnabledData](/previous-versions/ms824229(v=msdn.10))   | **RealTimeStylusEnabled**  | Información que [**el objeto RealTimeStylus**](realtimestylus-class.md) agrega cuando se habilita.<br/>                                                                                                                                         |
| [StylusButtonDownData](/previous-versions/ms824181(v=msdn.10))             | **StylusButtonDown**       | Información sobre el botón de lápiz óptico concreto que se está pulsando.<br/>                                                                                                                                                                        |
| [StylusButtonUpData](/previous-versions/ms824172(v=msdn.10))                 | **StylusButtonUp**         | Información sobre el botón de lápiz óptico concreto que se va a liberar.<br/>                                                                                                                                                                       |
| [StylusDownData](/previous-versions/ms585582(v=vs.100))                                   | **StylusDown**             | La información de paquetes de un lápiz óptico cuando el lápiz óptico se pondrá en contacto con el digitalizador.<br/>                                                                                                                                                      |
| [StylusInRangeData](/previous-versions/ms824090(v=msdn.10))                   | **StylusInRange**          | Información sobre el lápiz óptico concreto que está especificando el área de entrada del objeto [**RealTimeStylus**](realtimestylus-class.md) o especificando el intervalo de detección del digitalizador encima del área de entrada del objeto **RealTimeStylus.**<br/> |
| [StylusOutOfRangeData](/previous-versions/ms824072(v=msdn.10))             | **StylusOutOfRange**       | Información sobre el lápiz óptico concreto que sale del área de entrada del objeto [**RealTimeStylus**](realtimestylus-class.md) o deja el intervalo de detección del digitalizador por encima del área de entrada del objeto **RealTimeStylus.**<br/>   |
| [StylusUpData](/previous-versions/ms824057(v=msdn.10))                             | **StylusUp**               | Información de paquetes para un lápiz óptico a medida que el lápiz óptico se eleva del digitalizador.<br/>                                                                                                                                                                  |
| [SystemGestureData](/previous-versions/ms824019(v=msdn.10))                   | **SystemGesture**          | Información que [**agrega el objeto RealTimeStylus**](realtimestylus-class.md) cuando detecta un gesto del sistema.<br/>                                                                                                                                 |
| [TabletAddedData](/previous-versions/ms824010(v=msdn.10))                       | **Tableta agregada**            | Información sobre el [objeto Tablet](/previous-versions/ms827783(v=msdn.10)) que se va a agregar.<br/>                                                                                                                                                |
| [TabletRemovedData](/previous-versions/ms823997(v=msdn.10))                   | **TabletRemoved**          | Información sobre el [objeto Tablet](/previous-versions/ms827783(v=msdn.10)) que se va a quitar.<br/>                                                                                                                                              |



 

Para obtener información sobre cómo el [**objeto RealTimeStylus**](realtimestylus-class.md) controla el flujo de datos de lápiz de tableta, vea Trabajar con la clase [RealTimeStylus](working-with-the-realtimestylus-class.md).

## <a name="data-interest"></a>Interés de datos

El objeto [**RealTimeStylus**](realtimestylus-class.md) comprueba la propiedad [Microsoft.StylusInput.IStylusSyncPlugin.DataInterest](/previous-versions/ms574887(v=vs.100)) o [Microsoft.StylusInput.IStylusAsyncPlugin.DataInterest](/previous-versions/ms574886(v=vs.100)) de un complemento cuando el complemento se agrega a la colección de complementos sincrónica o asincrónica del objeto **RealTimeStylus.** Por lo tanto, debe usar la propiedad DataInterest para suscribirse a todas las notificaciones que usa esta instancia del complemento, aunque con poca frecuencia, pero no a ninguna de las notificaciones que nunca usa esta instancia del complemento. En el caso de las notificaciones que el complemento solo usa ocasionalmente, compruebe primero el estado del complemento en el método de notificación y devuelva si el complemento no usa la notificación en su estado actual.

Un complemento solo recibe llamadas en métodos marcados en la propiedad [Microsoft.StylusInput.IStylusSyncPlugin.DataInterest](/previous-versions/ms574887(v=vs.100)) o [Microsoft.StylusInput.IStylusAsyncPlugin.DataInterest del](/previous-versions/ms574886(v=vs.100)) complemento. Para obtener más información sobre los valores posibles de la propiedad **DataInterest** de un complemento, vea la [enumeración DataInterestMask.](/previous-versions/ms824787(v=msdn.10))

## <a name="timing"></a>Control de tiempo

Los datos se ponen en cola en el objeto [**RealTimeStylus**](realtimestylus-class.md) antes de pasarse a los complementos de la colección asincrónica de complementos. En la lista siguiente se describen algunas situaciones que puede que deba tener en cuenta al diseñar un complemento asincrónico.

-   Cuando el [**objeto RealTimeStylus**](realtimestylus-class.md) está deshabilitado, el complemento asincrónico puede recibir otras notificaciones en cola antes de llamar a su método [RealTimeStylusDisabled.](/previous-versions/ms824774(v=msdn.10)) En esta situación, las llamadas desde el complemento a algunos de los métodos y propiedades del objeto **RealTimeStylus** inician una excepción. La información relevante para el complemento debe almacenarse en caché cuando el **objeto RealTimeStylus** está habilitado.
-   El método [ClearStylusQueues](/previous-versions/ms825781(v=msdn.10)) del objeto [**RealTimeStylus**](realtimestylus-class.md) puede quitar información de la cola de salida. Por lo tanto, los complementos asincrónicos no pueden confiar en recibir todas las notificaciones pertinentes.
-   Cuando se quita un objeto [Tablet](/previous-versions/ms827783(v=msdn.10)) que está disponible para el objeto [**RealTimeStylus,**](realtimestylus-class.md) el complemento asincrónico puede recibir una notificación de lápiz en cola para la tableta antes de llamar a su método [TabletRemoved.](/previous-versions/bb361092(v=vs.100)) En esta situación, no funciona la llamada al método [GetTabletPropertyDescriptionCollection](/previous-versions/ms825935(v=msdn.10)) del objeto **RealTimeStylus.** La información relevante para el complemento debe almacenarse en caché cuando el objeto **RealTimeStylus** está habilitado o cuando se agrega una nueva tableta.

En función de la aplicación, puede mejorar el rendimiento al deshabilitar un [**objeto RealTimeStylus.**](realtimestylus-class.md) Cuando la propiedad [Enabled](/previous-versions/ms824832(v=msdn.10)) del objeto **RealTimeStylus** se establece en **FALSE,** los datos de las colas de entrada y salida se procesan hasta que las colas están vacías. Puede llamar al método [ClearStylusQueues](/previous-versions/ms825781(v=msdn.10)) del objeto **RealTimeStylus** para borrar las colas antes de deshabilitar el objeto **RealTimeStylus.**

## <a name="enabled-and-disabled-data"></a>Datos habilitados y deshabilitados

Cuando el objeto [**RealTimeStylus**](realtimestylus-class.md) está habilitado, cada complemento recibe una llamada a su método [Microsoft.StylusInput.IStylusSyncPlugin.RealTimeStylusEnabled](/previous-versions/ms824758(v=msdn.10)) o [Microsoft.StylusInput.IStylusAsyncPlugin.RealTimeStylusEnabled.](/previous-versions/ms824775(v=msdn.10)) El **objeto RealTimeStylusEnabledData** pasado en la notificación contiene una colección de los identificadores de contexto para las tabletas disponibles en el momento en que se habilita el objeto **RealTimeStylus.**

> [!Note]  
> Dado que los datos de complemento para la colección asincrónica de complementos del objeto [**RealTimeStylus**](realtimestylus-class.md) están en cola, los complementos asincrónicos pueden recibir datos antes de recibir una llamada a su método [RealTimeStylusDisabled,](/previous-versions/ms824774(v=msdn.10)) pero después de deshabilitar el objeto **RealTimeStylus.** Tenga en cuenta que algunos de los métodos y propiedades del objeto **RealTimeStylus** inician una excepción si el objeto **RealTimeStylus** está deshabilitado.

 

El objeto [**RealTimeStylus**](realtimestylus-class.md) llama a los métodos [Microsoft.StylusInput.IStylusSyncPlugin.RealTimeStylusEnabled](/previous-versions/ms824758(v=msdn.10)) y [Microsoft.StylusInput.IStylusSyncPlugin.RealTimeStylusDisabled](/previous-versions/ms824757(v=msdn.10)) en el subproceso desde el que está habilitado el objeto **RealTimeStylus** o desde el que se agrega el complemento sincrónico.

Por lo general, agregue o quite complementos mientras el [**objeto RealTimeStylus**](realtimestylus-class.md) está deshabilitado. Para obtener más información sobre cómo agregar y quitar complementos al objeto **RealTimeStylus,** vea Complementos y la clase [RealTimeStylus](plug-ins-and-the-realtimestylus-class.md).

## <a name="tablet-data"></a>Datos de tableta

Cuando una tableta que el objeto [**RealTimeStylus**](realtimestylus-class.md) puede usar se agrega o quita del tablet PC mientras el objeto **RealTimeStylus** está habilitado, el objeto **RealTimeStylus** notifica a sus complementos que se ha agregado o quitado un objeto [Tablet.](/previous-versions/ms827783(v=msdn.10)) Cada **objeto RealTimeStylus** mantiene una lista de identificadores únicos para los objetos de tableta con los que puede interactuar. El **objeto RealTimeStylus** tiene dos métodos para traducir entre el identificador único y el objeto Tablet, los métodos [GetTabletContextIdFromTablet](/previous-versions/ms825922(v=msdn.10)) y [GetTabletFromTabletContextId.](/previous-versions/ms825929(v=msdn.10))

> [!Note]  
> La información sobre una tableta ya no está disponible en el [**objeto RealTimeStylus**](realtimestylus-class.md) después de quitar la tableta del equipo tableta.

 

## <a name="tablet-pen-data"></a>Datos del lápiz de tableta

El [**objeto RealTimeStylus**](realtimestylus-class.md) pasa información sobre el lápiz de tableta a sus complementos en varios de los métodos de notificación. La información sobre el lápiz de tableta se representa mediante un [objeto Stylus.](/previous-versions/ms824824(v=msdn.10)) Este objeto es una instantánea del estado del lápiz de tableta en el momento en que se recopilaron los datos. Dado que los complementos reciben los datos del lápiz de tableta como parte del flujo de datos del lápiz de tableta, los complementos deben usar la información del objeto Stylus en lugar de comprobar el estado actual de un lápiz de tableta determinado a través de la [clase Cursor.](/previous-versions/ms839521(v=msdn.10))

Cada [objeto Stylus](/previous-versions/ms824824(v=msdn.10)) contiene el identificador de contexto de la tableta que generó los datos.

## <a name="system-gesture-data"></a>Datos de gestos del sistema

El [**objeto RealTimeStylus**](realtimestylus-class.md) recibe datos sobre los gestos del sistema a medida que son reconocidos por tablet PC. En la tabla siguiente se describe el orden en el que se producen los objetos [SystemGestureData](/previous-versions/ms824019(v=msdn.10)) en el flujo de datos del lápiz de tableta en relación con otros datos de lápiz de tableta.




| <a href="/previous-versions/ms827134(v=msdn.10)">SystemGesture</a> | Objetos que preceden al <a href="/previous-versions/ms824019(v=msdn.10)">objeto SystemGestureData</a> | Objetos que vienen después del <a href="/previous-versions/ms824019(v=msdn.10)">objeto SystemGestureData</a> | 
|--------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <strong>Pulsar</strong> | Objeto <a href="/previous-versions/ms824107(v=msdn.10)">StylusDownData.</a><br /> | Objeto [StylusUpData.](/previous-versions/ms824057(v=msdn.10))<br /> | 
| <strong>DoubleTap</strong> | El <a href="/previous-versions/ms824107(v=msdn.10)">objeto StylusDownData,</a> el <a href="/previous-versions/ms824019(v=msdn.10)">objeto SystemGestureData</a> para el gesto del sistema <strong>Tap</strong> y los [objetos StylusUpData.](/previous-versions/ms824057(v=msdn.10))<br /> | Segundo <a href="/previous-versions/ms824107(v=msdn.10)">objeto StylusDownData.</a><br /> | 
| <strong>RightTap</strong> | El <a href="/previous-versions/ms824107(v=msdn.10)">objeto StylusDownData</a> y <a href="/previous-versions/ms824019(v=msdn.10)">el objeto SystemGestureData</a> para el <strong>miembro HoldEnter</strong> de la <a href="/previous-versions/ms827134(v=msdn.10)">enumeración SystemGesure.</a><br /> | Objeto [StylusUpData.](/previous-versions/ms824057(v=msdn.10))<br /> | 
| <strong>Arrastrar</strong> | Objeto <a href="/previous-versions/ms824107(v=msdn.10)">StylusDownData.</a><br /> | Objeto [StylusUpData.](/previous-versions/ms824057(v=msdn.10))<br /> | 
| <strong>RightDrag</strong> | Objeto <a href="/previous-versions/ms824107(v=msdn.10)">StylusDownData.</a><br /> | Objeto [StylusUpData.](/previous-versions/ms824057(v=msdn.10))<br /> | 
| <strong>HoldEnter</strong> | Objeto <a href="/previous-versions/ms824107(v=msdn.10)">StylusDownData.</a><br /> | Objeto [StylusUpData.](/previous-versions/ms824057(v=msdn.10))<br /><blockquote>[!Note]<br />Este gesto del sistema no se reconoce si el usuario comienza un gesto del sistema <strong>Arrastrar</strong> o <strong>A</strong> la derecha.</blockquote><br /> | 
| <strong>HoldLeave</strong> | Sin implementar.<br /> | Sin implementar.<br /> | 
| <strong>HoverEnter</strong> | Varios <a href="/previous-versions/ms824592(v=msdn.10)">objetos InAirPacketsData</a> de baja velocidad media.<br /> | <blockquote>[!Note]<br />Puede haber un retraso apreciable antes de recibir el gesto del sistema <strong>HoverEnter.</strong> El <a href="realtimestylus-class.md"><strong>objeto RealTimeStylus</strong></a> solo recibe estos datos si el objeto <strong>RealTimeStylus</strong> está asociado a la ventana o control que está directamente debajo del lápiz en el momento del gesto del sistema.</blockquote><br /> | 
| <strong>HoverLeave</strong> | El <a href="/previous-versions/ms824019(v=msdn.10)">objeto SystemGestureData para</a> el gesto del sistema <strong>HoverEnter</strong> y varios <a href="/previous-versions/ms824592(v=msdn.10)">objetos InAirPacketsData</a> de una velocidad media suficiente.<br /> | <blockquote>[!Note]<br />Puede haber un retraso apreciable antes de recibir el gesto del sistema <strong>HoverLeave.</strong> El <a href="realtimestylus-class.md"><strong>objeto RealTimeStylus</strong></a> solo recibe estos datos si el objeto <strong>RealTimeStylus</strong> está asociado a la ventana o control que está directamente debajo del lápiz en el momento del gesto del sistema.</blockquote><br /> | 




 

## <a name="custom-stylus-data"></a>Datos de lápiz óptico personalizados

Los datos de lápiz óptico personalizados se pueden agregar al objeto [**RealTimeStylus**](realtimestylus-class.md) llamando al [método AddCustomStylusDataToQueue.](/previous-versions/ms825761(v=msdn.10)) Los datos de lápiz óptico personalizados se pueden agregar a las colas del objeto **RealTimeStylus** en uno de estos tres lugares.

-   Cuando el parámetro *queue* se establece en **Output**, los datos personalizados se agregan a la cola de salida del objeto [**RealTimeStylus**](realtimestylus-class.md) después de que la colección de complementos sincrónicos procese actualmente los datos.
-   Cuando el parámetro *queue* se establece en **OutputImmediate,** los datos personalizados se agregan a la cola de salida del objeto [**RealTimeStylus**](realtimestylus-class.md) antes de que la colección de complementos sincrónica procese actualmente los datos.
-   Cuando el parámetro *queue* se establece en **Input**, los datos personalizados se agregan a la cola de entrada del objeto [**RealTimeStylus**](realtimestylus-class.md) y se envían a la colección de complementos sincrónica antes de los nuevos datos del flujo de datos del lápiz de tableta.

En cada uno de los casos anteriores, los datos agregados por complementos posteriores en la colección de complementos sincrónica se agregan después de los datos agregados por complementos anteriores.

> [!Note]  
> Si la llamada al método [AddCustomStylusDataToQueue](/previous-versions/ms825761(v=msdn.10)) se realiza desde un complemento sincrónico en respuesta a una llamada a uno de sus [**métodos IStylusSyncPlugin,**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) los datos del lápiz óptico personalizado se agregan al flujo de datos del lápiz de tableta de una manera predecible. De lo contrario, se agrega a la cola en relación con los datos de lápiz actuales que el objeto [**RealTimeStylus**](realtimestylus-class.md) está procesando y no con respecto a los datos que el complemento asincrónico está procesando. El método AddCustomStylusDataToQueue produce una excepción si el objeto **RealTimeStylus** está deshabilitado.

 

Los datos de lápiz óptico personalizados se agregan a la cola como un objeto [CustomStylusData](/previous-versions/ms824747(v=msdn.10)) y los complementos reciben estos datos a través de su método [Microsoft.StylusInput.IStylusSyncPlugin.CustomStylusDataAdded](/previous-versions/ms824753(v=msdn.10)) o [Microsoft.StylusInput.IStylusAsyncPlugin.CustomStylusDataAdded.](/previous-versions/ms824770(v=msdn.10))

Los [**objetos DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) y [**GestureRecognizer**](gesturerecognizer-class.md) pueden agregar datos de lápiz óptico personalizados a la cola. Para obtener más información sobre **DynamicRenderer** y los objetos **GestureRecognizer,** vea [Complementos](dynamic-renderer-plug-ins.md) de representador dinámico y complementos [de Recognizer](recognizer-plug-ins.md).

El objeto [**RealTimeStylus**](realtimestylus-class.md) llama al método [Microsoft.StylusInput.IStylusSyncPlugin.CustomStylusDataAdded](/previous-versions/ms824753(v=msdn.10)) en el subproceso desde el que recibe la llamada a su método [AddCustomStylusDataToQueue.](/previous-versions/ms825761(v=msdn.10))

En el diagrama siguiente se muestra la adición de datos de lápiz óptico personalizados a la cola de salida con el parámetro *queue* establecido en **Output**.

![ilustración que muestra el flujo de datos de lápiz personalizado a la cola de salida ](images/27bc3672-41bc-432e-bf41-18e4ccec78f5.gif)

En este diagrama, los círculos con las letras "A" y "B" representan datos de lápiz de tableta que ya se han agregado a la cola de salida del objeto [**RealTimeStylus**](realtimestylus-class.md) y que aún no se han enviado a la colección asincrónica de complementos. El círculo con la letra "C" representa los datos del lápiz de tableta que el objeto **RealTimeStylus** está procesando actualmente. Se envía a la colección de complementos sincrónica y se coloca en la cola de salida. Los círculos numerados "1", "2" y "3" representan datos de lápiz óptico personalizados que se han agregado a la cola de salida mediante el primer, segundo y tercer complemento sincrónico respectivamente en respuesta a los datos del lápiz de tableta representados por "C". Los complementos han agregado los datos de lápiz óptico personalizados con el parámetro *queue* establecido en **StylusQueues.** El círculo vacío representa la posición en la cola de salida donde se agregan los datos futuros del lápiz de tableta.

En el diagrama siguiente se muestra la adición de datos de lápiz óptico personalizados a la cola de salida con el parámetro *queue* establecido en **OutputImmediate**.

![Diagrama que muestra el flujo de datos del lápiz óptico personalizado a la cola de salida.](images/bcf45325-5557-47a2-af43-142c7684e482.gif)

En este diagrama, los círculos con las letras "A" y "B" representan datos de lápiz de tableta que ya se han agregado a la cola de salida del objeto [**RealTimeStylus**](realtimestylus-class.md) y que aún no se han enviado a la colección asincrónica de complementos. El círculo con la letra "C" representa los datos del lápiz de tableta que el objeto **RealTimeStylus** está procesando actualmente. Se envía a la colección de complementos sincrónica y se coloca en la cola de salida. Los círculos numerados "1", "2" y "3" representan datos de lápiz óptico personalizados que se han agregado a la cola de salida mediante el primer, segundo y tercer complemento sincrónico respectivamente en respuesta a los datos del lápiz de tableta representados por "C". Los complementos han agregado los datos de lápiz óptico personalizados con el parámetro *queue* establecido en **OutputImmediate.** El círculo vacío representa la posición en la cola de salida donde se agregan los datos futuros del lápiz de tableta.

En el diagrama siguiente se muestra la adición de datos de lápiz óptico personalizados a la cola de entrada.

![ilustración que muestra el flujo de datos de lápiz personalizado a la cola de salida](images/5dd2cfcc-1086-49b0-a0d5-9276c13c7f61.gif)

En este diagrama, los círculos con las letras "A" y "B" representan datos de lápiz de tableta que ya se han agregado a la cola de salida del objeto [**RealTimeStylus**](realtimestylus-class.md) y que aún no se han enviado a la colección asincrónica de complementos. El círculo con la letra "C" representa los datos del lápiz de tableta que el objeto **RealTimeStylus** está procesando actualmente. Se envía a la colección de complementos sincrónica y se coloca en la cola de salida. Los círculos numerados "1", "2" y "3" representan datos de lápiz óptico personalizados que se han agregado a la cola de entrada mediante el primer, segundo y tercer complemento sincrónico, respectivamente, en respuesta a los datos del lápiz de tableta representados por "C". Los complementos han agregado los datos del lápiz óptico personalizados con el parámetro *queue* establecido en **Input**. A continuación, los datos del lápiz óptico personalizado numerados "1" se pasan a los complementos sincrónicos y, a continuación, a la cola de salida antes de que los datos del lápiz óptico personalizado numerados "2" y "3", que se procese antes de que se procese el siguiente lápiz de tableta. El círculo vacío representa la posición en la cola de salida donde se agregan los datos futuros del lápiz de tableta.

## <a name="error-data"></a>Datos de error

Cuando un complemento produce una excepción, se interrumpe el flujo normal de datos. El [**objeto RealTimeStylus**](realtimestylus-class.md) genera un [objeto ErrorData](/previous-versions/ms824740(v=msdn.10)) y llama a:

-   El [método Microsoft.StylusInput.IStylusSyncPlugin.Error](/previous-versions/ms824754(v=msdn.10)) o [Microsoft.StylusInput.IStylusAsyncPlugin.Error](/previous-versions/ms824771(v=msdn.10)) del complemento que produjo la excepción.
-   El [método Microsoft.StylusInput.IStylusSyncPlugin.Error](/previous-versions/ms824754(v=msdn.10)) o [Microsoft.StylusInput.IStylusAsyncPlugin.Error](/previous-versions/ms824771(v=msdn.10)) de los complementos restantes de esa colección.

Si el complemento que produjo la excepción es un complemento sincrónico, el objeto [ErrorData](/previous-versions/ms824740(v=msdn.10)) se agrega a la cola de salida. A [**continuación, el objeto RealTimeStylus**](realtimestylus-class.md) reanuda el procesamiento normal de los datos originales.

En el diagrama siguiente se muestra la adición de datos de error a los datos del lápiz de tableta.

![flujo de datos de lápiz óptico personalizado a la cola de salida con la adición de datos de error](images/c2f79abe-aeb5-498f-b389-1fad9bf01a13.gif)

En este diagrama, los círculos con las letras "A" y "B" representan datos de lápiz de tableta que ya se han agregado a la cola de salida del objeto [**RealTimeStylus**](realtimestylus-class.md) y que aún no se han enviado a la colección asincrónica de complementos. El círculo con la letra "C" representa los datos del lápiz de tableta que el objeto **RealTimeStylus** está procesando actualmente. El círculo con la letra "e" representa un objeto [ErrorData](/previous-versions/ms824740(v=msdn.10)) generado por el objeto **RealTimeStylus** cuando el segundo complemento sincrónico, El complemento sincrónico 2, produce una excepción mientras procesa "C". A continuación, el objeto **RealTimeStylus** pausa su procesamiento de "C" y pasa "e" al complemento que generó la excepción y todos los complementos posteriores. A continuación, el objeto **RealTimeStylus** coloca "e" en la cola de salida y reanuda su procesamiento de "C", que se pasa a los complementos restantes de la colección de complementos sincrónicos y se coloca en la cola de salida después de "e". El círculo vacío representa la posición en la cola de salida donde se agregan los datos futuros del lápiz de tableta.

Si un complemento produce una excepción desde su método Error, el objeto [**RealTimeStylus**](realtimestylus-class.md) detecta la excepción, pero no genera un [nuevo objeto ErrorData.](/previous-versions/ms824740(v=msdn.10)) Esto es para evitar la recursividad.

Los datos de error se agregan a la cola de salida después de los datos de lápiz óptico personalizados que se agregan en la posición **OutputImmediate** antes de la excepción que creó los datos de error y antes de los datos de lápiz óptico personalizados que se agregan en la posición **OutputImmediate** mediante complementos posteriores en la colección de complementos sincrónica.

En el diagrama siguiente se muestra cómo se agregan los datos de error a la cola de salida en relación con los datos personalizados que se agregan a la **cola OutputImmediate.**

![datos de error agregados a la cola de salida en relación con los datos personalizados agregados a la cola outputimmediate.](images/b00320c4-6fe7-439d-9855-e5f131feeb69.gif)

En este diagrama, los círculos con las letras "A" y "B" representan datos de lápiz de tableta que ya se han agregado a la cola de salida del objeto [**RealTimeStylus**](realtimestylus-class.md) y que aún no se han enviado a la colección asincrónica de complementos. El círculo con la letra "C" representa los datos del lápiz de tableta que el objeto **RealTimeStylus** está procesando actualmente. Los círculos numerados "1", "2" y "3" se agregan mediante el primer, segundo y tercer complemento sincrónico respectivamente a la cola **OutputImmediate** en respuesta a los datos representados por el círculo con la letra "C". El círculo con la letra "e" representa los datos de error generados en respuesta a una excepción producida por el segundo complemento después de que el segundo complemento agregara datos personalizados a la cola de salida en la **posición OutputImmediate.**

Si algún complemento sincrónico agrega datos de lápiz óptico personalizados a la cola de entrada en respuesta a los datos de error, los datos se agregan inmediatamente antes de los datos de error. Si alguno de los complementos sincrónicos agrega datos  de lápiz óptico personalizados a la cola de salida en la posición salida en respuesta a los datos de error, los datos se agregan inmediatamente después de los datos de error.

El [**objeto RealTimeStylus**](realtimestylus-class.md) llama al método [Microsoft.StylusInput.IStylusSyncPlugin.Error](/previous-versions/ms824754(v=msdn.10)) en el subproceso desde el que se produce la excepción.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Microsoft.Ink.Tablet](/previous-versions/ms827783(v=msdn.10))
</dt> <dt>

[Microsoft.StylusInput.PluginData](/previous-versions/ms823992(v=msdn.10))
</dt> <dt>

[Microsoft.StylusInput.DataInterestMask](/previous-versions/ms575174(v=vs.100))
</dt> <dt>

[Microsoft.StylusInput.RealTimeStylus](/previous-versions/ms824830(v=msdn.10))
</dt> <dt>

[Trabajar con la clase RealTimeStylus](working-with-the-realtimestylus-class.md)
</dt> </dl>

 

 
