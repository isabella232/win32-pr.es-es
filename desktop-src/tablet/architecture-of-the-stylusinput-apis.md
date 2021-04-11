---
description: Las API de StylusInput permiten interactuar con el flujo de datos del lápiz de Tablet PC. Para interactuar con el flujo de datos, agregue un objeto RealTimeStylus a la aplicación y agregue complementos al objeto RealTimeStylus.
ms.assetid: 88bab0ab-df9f-4813-9a9f-9a137813f0b4
title: Arquitectura de las API de StylusInput
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eeda6a6a0269e8306aed6a6b6de4c1bbe33bc46f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104156744"
---
# <a name="architecture-of-the-stylusinput-apis"></a>Arquitectura de las API de StylusInput

Las API de StylusInput permiten interactuar con el flujo de datos del lápiz de Tablet PC. Para interactuar con el flujo de datos, agregue un objeto [**RealTimeStylus**](realtimestylus-class.md) a la aplicación y agregue complementos al objeto **RealTimeStylus** .

Se proporcionan dos complementos en las API de StylusInput. El objeto [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) implementa la interfaz [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) . El objeto **DynamicRenderer** representa la entrada de lápiz en tiempo real, a medida que se dibuja. El objeto [**GestureRecognizer**](gesturerecognizer-class.md) implementa las interfaces **IStylusSyncPlugin** y [**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) . El objeto **GestureRecognizer** reconoce los gestos de la aplicación.

## <a name="definitions"></a>Definiciones

Los siguientes términos se usan en las secciones que describen las API de StylusInput:

Complemento sincrónico

Una clase que implementa la interfaz [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) . Normalmente, el objeto [**RealTimeStylus**](realtimestylus-class.md) llama directamente a los complementos sincrónicos.

Complemento asincrónico

Una clase que implementa la interfaz [**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) . En general, se llama a los complementos asincrónicos en el subproceso de la interfaz de usuario (IU) de la aplicación.

Colección de complementos sincrónicos

Colección [StylusSyncPluginCollection](/previous-versions/ms824788(v=msdn.10)) , que es una colección ordenada de objetos [IStylusSyncPlugin](/previous-versions/ms824751(v=msdn.10)) . Normalmente, una colección de complementos sincrónicos hace referencia a la colección asignada a la propiedad [SyncPluginCollection](/previous-versions/ms824833(v=msdn.10)) de un objeto [RealTimeStylus](/previous-versions/ms824830(v=msdn.10)) . Solo se pueden agregar complementos sincrónicos a una colección de complementos sincrónicos.

Colección de complementos asincrónica

Colección [StylusAsyncPluginCollection](/previous-versions/ms824808(v=msdn.10)) , que es una colección ordenada de objetos [IStylusAsyncPlugin](/previous-versions/ms824768(v=msdn.10)) . Normalmente, una colección de complementos asincrónica hace referencia a la colección asignada a la propiedad [AsyncPluginCollection](/previous-versions/ms824831(v=msdn.10)) de un objeto [RealTimeStylus](/previous-versions/ms824830(v=msdn.10)) . Solo se pueden agregar complementos asincrónicos a una colección de complementos asincrónica.

## <a name="synchronous-and-asynchronous-plug-ins"></a>Complementos sincrónicos y asincrónicos

El objeto [**RealTimeStylus**](realtimestylus-class.md) está diseñado para proporcionar acceso en tiempo real al flujo de datos desde un lápiz de Tablet PC. Cree o use complementos sincrónicos para tareas que requieran acceso en tiempo real al flujo de datos y que se despidan computacionalmente, por ejemplo, para el filtrado de paquetes. Cree o use complementos asincrónicos para tareas que no requieran acceso en tiempo real al flujo de datos, por ejemplo, para crear y almacenar los trazos en un objeto [**InkDisp**](inkdisp-class.md) .

Es posible que algunas tareas estén exigiendo cálculo, pero que requieran acceso en tiempo real al flujo de datos, como el reconocimiento de gestos de varios trazos. Para satisfacer estas necesidades, las API de StylusInput proporcionan un modelo [**RealTimeStylus**](realtimestylus-class.md) en cascada que le permite usar dos objetos **RealTimeStylus** , cada uno de los cuales se ejecuta en su propio subproceso. Para obtener más información sobre el modelo **RealTimeStylus** en cascada, vea [el modelo RealTimeStylus en cascada](the-cascaded-realtimestylus-model.md).

Para obtener más información sobre cómo usar y crear complementos, consulte [trabajar con las API de StylusInput](working-with-the-stylusinput-apis.md).

## <a name="the-tablet-pen-data-stream"></a>El flujo de datos del lápiz de Tablet PC

El objeto [**RealTimeStylus**](realtimestylus-class.md) tiene dos colas internas que llevan los datos del lápiz de Tablet PC, la cola de entrada y la cola de salida. Los datos del lápiz se convierten en instancias de las clases del espacio de nombres [Microsoft. StylusInput. PluginData](/previous-versions/ms823992(v=msdn.10)) . En la lista siguiente se describe cómo el objeto **RealTimeStylus** controla los datos del lápiz de Tablet PC:

El objeto [**RealTimeStylus**](realtimestylus-class.md) comprueba primero los objetos de datos de complemento en su cola de entrada y después desde el flujo de datos del lápiz de Tablet PC.

El objeto [**RealTimeStylus**](realtimestylus-class.md) envía un objeto de datos de complemento a los objetos de su colección de complementos sincrónicos. Cada complemento sincrónico puede agregar datos a la cola de entrada o de salida.

Una vez que el objeto de datos del complemento se ha enviado a todos los miembros de la colección de complementos sincrónicos, el objeto de datos del complemento se coloca en la cola de salida del objeto [**RealTimeStylus**](realtimestylus-class.md) .

A continuación, el objeto [**RealTimeStylus**](realtimestylus-class.md) comprueba el siguiente objeto de datos del complemento que se va a procesar.

Mientras que la cola de salida del objeto [**RealTimeStylus**](realtimestylus-class.md) contiene datos, el objeto **RealTimeStylus** envía un objeto de datos de complemento desde su cola de salida a los objetos de su colección de complementos asincrónica. Cada complemento asincrónico puede agregar datos a la cola de entrada o de salida. Sin embargo, dado que los complementos asincrónicos se ejecutan en el subproceso de la interfaz de usuario, los datos se agregan a la cola en relación con los datos de lápiz actuales que procesa el objeto **RealTimeStylus** y no con respecto a los datos que procesa el complemento asincrónico.

En el diagrama siguiente se ilustra el flujo de datos del lápiz de Tablet PC a través del objeto [**RealTimeStylus**](realtimestylus-class.md) y sus colecciones de complementos.

![flujo de datos del lápiz de Tablet PC a través del objeto RealTimeStylus y sus colecciones de complementos](images/5a698bc9-833b-4b24-9fa2-70be0ca61032.gif)

En este diagrama, los círculos con la etiqueta "A" y "B" representan los datos del lápiz de Tablet PC que ya se han agregado a la cola de salida del objeto [**RealTimeStylus**](realtimestylus-class.md) y que todavía no se han enviado a la colección de complementos asincrónica. El círculo con la etiqueta "C" representa los datos del lápiz de Tablet PC que está procesando actualmente el objeto **RealTimeStylus** . Se envía a la colección de complementos sincrónicos y se coloca en la cola de salida. El círculo vacío representa la posición en la cola de salida donde se agregan los datos futuros del lápiz de Tablet PC.

Para obtener más información sobre cómo se agregan datos específicos a la cola y se procesan, vea [datos de complemento y la clase RealTimeStylus](plug-in-data-and-the-realtimestylus-class.md).

## <a name="the-stylusinput-apis"></a>Las API de StylusInput

Las API de StylusInput residen principalmente en los espacios de nombres [Microsoft. StylusInput](/previous-versions/ms824750(v=msdn.10)) y [Microsoft. StylusInput. PluginData](/previous-versions/ms823992(v=msdn.10)) . Sin embargo, las API de StylusInput también hacen referencia a algunas clases del espacio de nombres [Microsoft. Ink](/previous-versions/ms826516(v=msdn.10)) , como la clase [tableta](/previous-versions/ms827783(v=msdn.10)) , la colección [TabletPropertyDescriptionCollection](/previous-versions/ms827760(v=msdn.10)) y las enumeraciones [ApplicationGesture](/previous-versions/ms827547(v=msdn.10)) y [SystemGesture](/previous-versions/ms827134(v=msdn.10)) .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85))
</dt> <dt>

[**GestureRecognizer**](gesturerecognizer-class.md)
</dt> <dt>

[**RealTimeStylus**](realtimestylus-class.md)
</dt> <dt>

[**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin)
</dt> <dt>

[**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin)
</dt> <dt>

[Trabajar con las API de StylusInput](working-with-the-stylusinput-apis.md)
</dt> <dt>

[El modelo RealTimeStylus en cascada](the-cascaded-realtimestylus-model.md)
</dt> </dl>

 

 
