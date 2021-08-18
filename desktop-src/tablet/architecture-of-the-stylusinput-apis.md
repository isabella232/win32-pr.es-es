---
description: Las API StylusInput permiten interactuar con el flujo de datos de lápiz de tableta. Para interactuar con el flujo de datos, agregue un objeto RealTimeStylus a la aplicación y agregue complementos al objeto RealTimeStylus.
ms.assetid: 88bab0ab-df9f-4813-9a9f-9a137813f0b4
title: Arquitectura de las API StylusInput
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 961d6e3e94d47054afb28948685fce5fe1cafe9cbb0fa2f36e5a2d8508f28b9b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119093168"
---
# <a name="architecture-of-the-stylusinput-apis"></a>Arquitectura de las API StylusInput

Las API StylusInput permiten interactuar con el flujo de datos de lápiz de tableta. Para interactuar con el flujo de datos, agregue un objeto [**RealTimeStylus**](realtimestylus-class.md) a la aplicación y agregue complementos al objeto **RealTimeStylus.**

Se proporcionan dos complementos en las API StylusInput. El [**objeto DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) implementa la [**interfaz IStylusSyncPlugin.**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) El **objeto DynamicRenderer** representa la entrada de lápiz en tiempo real, a medida que se dibuja. El [**objeto GestureRecognizer**](gesturerecognizer-class.md) implementa las interfaces **IStylusSyncPlugin** [**e IStylusAsyncPlugin.**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) El **objeto GestureRecognizer** reconoce los gestos de la aplicación.

## <a name="definitions"></a>Definiciones

Los términos siguientes se usan en las secciones que describen las API StylusInput:

Complemento sincrónico

Clase que implementa la interfaz [**IStylusSyncPlugin.**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) Normalmente, el objeto [**RealTimeStylus**](realtimestylus-class.md) llama directamente a los complementos sincrónicos.

Complemento asincrónico

Clase que implementa la [**interfaz IStylusAsyncPlugin.**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) Normalmente, se llama a los complementos asincrónicos en el subproceso de la interfaz de usuario (UI) de la aplicación.

Colección de complementos sincrónica

Colección [StylusSyncPluginCollection,](/previous-versions/ms824788(v=msdn.10)) que es una colección ordenada de [objetos IStylusSyncPlugin.](/previous-versions/ms824751(v=msdn.10)) Una colección de complementos sincrónica normalmente hace referencia a la colección asignada a la [propiedad SyncPluginCollection](/previous-versions/ms824833(v=msdn.10)) de un [objeto RealTimeStylus.](/previous-versions/ms824830(v=msdn.10)) Solo se pueden agregar complementos sincrónicos a una colección de complementos sincrónica.

Colección asincrónica de complementos

Colección [StylusAsyncPluginCollection,](/previous-versions/ms824808(v=msdn.10)) que es una colección ordenada de [objetos IStylusAsyncPlugin.](/previous-versions/ms824768(v=msdn.10)) Una colección de complementos asincrónica normalmente hace referencia a la colección asignada a la [propiedad AsyncPluginCollection](/previous-versions/ms824831(v=msdn.10)) de un [objeto RealTimeStylus.](/previous-versions/ms824830(v=msdn.10)) Solo se pueden agregar complementos asincrónicos a una colección asincrónica de complementos.

## <a name="synchronous-and-asynchronous-plug-ins"></a>Complementos sincrónicos y asincrónicos

El [**objeto RealTimeStylus**](realtimestylus-class.md) está diseñado para proporcionar acceso en tiempo real al flujo de datos desde un lápiz de tableta. Cree o use complementos sincrónicos para tareas que requieran acceso en tiempo real al flujo de datos y que no sean exigentes, como el filtrado de paquetes. Cree o use complementos asincrónicos para tareas que no requieren acceso en tiempo real al flujo de datos, como para crear y almacenar trazos en un [**objeto InkDisp.**](inkdisp-class.md)

Ciertas tareas pueden ser exigentes computacionalmente, pero requieren acceso en tiempo real al flujo de datos, como el reconocimiento de gestos de varias pulsaciones. Para satisfacer estas necesidades, las API StylusInput proporcionan un modelo [**RealTimeStylus**](realtimestylus-class.md) en cascada que permite usar dos objetos **RealTimeStylus,** cada uno de ellos en su propio subproceso. Para obtener más información sobre el modelo **RealTimeStylus** en cascada, vea [The Cascaded RealTimeStylus Model](the-cascaded-realtimestylus-model.md).

Para obtener más información sobre el uso y la creación de complementos, vea [Trabajar con las API StylusInput](working-with-the-stylusinput-apis.md).

## <a name="the-tablet-pen-data-stream"></a>Flujo de datos del lápiz de tableta

El [**objeto RealTimeStylus**](realtimestylus-class.md) tiene dos colas internas que llevan los datos del lápiz de tableta, la cola de entrada y la cola de salida. Los datos del lápiz se convierten en instancias de las clases del espacio [de nombres Microsoft.StylusInput.PluginData.](/previous-versions/ms823992(v=msdn.10)) En la lista siguiente se describe cómo el **objeto RealTimeStylus** controla los datos del lápiz de tableta:

El [**objeto RealTimeStylus**](realtimestylus-class.md) comprueba primero los objetos de datos de complemento en su cola de entrada y, a continuación, desde el flujo de datos del lápiz de tableta.

El [**objeto RealTimeStylus**](realtimestylus-class.md) envía un objeto de datos de complemento a los objetos de su colección de complementos sincrónica. Cada complemento sincrónico puede agregar datos a la cola de entrada o salida.

Una vez enviado el objeto de datos del complemento a todos los miembros de la colección de complementos sincrónica, el objeto de datos del complemento se coloca en la cola de salida del objeto [**RealTimeStylus.**](realtimestylus-class.md)

A [**continuación, el objeto RealTimeStylus**](realtimestylus-class.md) comprueba si hay que procesar el siguiente objeto de datos del complemento.

Aunque la cola de salida del objeto [**RealTimeStylus**](realtimestylus-class.md) contiene datos, el objeto **RealTimeStylus** envía un objeto de datos de complemento desde su cola de salida a los objetos de su colección de complementos asincrónica. Cada complemento asincrónico puede agregar datos a la cola de entrada o salida. Sin embargo, dado que los complementos asincrónicos se ejecutan en el subproceso de interfaz de usuario, los datos se agregan a la cola en relación con los datos del lápiz actual que el objeto **RealTimeStylus** está procesando y no en relación con los datos que el complemento asincrónico está procesando.

En el diagrama siguiente se muestra el flujo de datos de lápiz de tableta a través del objeto [**RealTimeStylus**](realtimestylus-class.md) y sus colecciones de complementos.

![flujo de datos de lápiz de tableta a través del objeto realtimestylus y sus colecciones de complementos](images/5a698bc9-833b-4b24-9fa2-70be0ca61032.gif)

En este diagrama, los círculos con las etiquetas "A" y "B" representan datos de lápiz de tableta que ya se han agregado a la cola de salida del objeto [**RealTimeStylus**](realtimestylus-class.md) y que aún no se han enviado a la colección asincrónica de complementos. El círculo con la etiqueta "C" representa los datos del lápiz de tableta que el **objeto RealTimeStylus** está procesando actualmente. Se envía a la colección de complementos sincrónica y se coloca en la cola de salida. El círculo vacío representa la posición en la cola de salida donde se agregan los datos futuros del lápiz de tableta.

Para obtener más información sobre cómo se agregan datos específicos a la cola y se procesan, vea Datos de complemento y la clase [RealTimeStylus](plug-in-data-and-the-realtimestylus-class.md).

## <a name="the-stylusinput-apis"></a>Las API StylusInput

Las API de StylusInput residen principalmente en los espacios de nombres [Microsoft.StylusInput](/previous-versions/ms824750(v=msdn.10)) y [Microsoft.StylusInput.PluginData.](/previous-versions/ms823992(v=msdn.10)) Sin embargo, las API StylusInput también hacen referencia a algunas clases del espacio de nombres [Microsoft.Ink,](/previous-versions/ms826516(v=msdn.10)) como la clase [Tablet,](/previous-versions/ms827783(v=msdn.10)) la colección [TabletPropertyDescriptionCollection](/previous-versions/ms827760(v=msdn.10)) y las enumeraciones [ApplicationGesture](/previous-versions/ms827547(v=msdn.10)) [y SystemGesture.](/previous-versions/ms827134(v=msdn.10))

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

[Trabajar con las API StylusInput](working-with-the-stylusinput-apis.md)
</dt> <dt>

[Modelo RealTimeStylus en cascada](the-cascaded-realtimestylus-model.md)
</dt> </dl>

 

 
