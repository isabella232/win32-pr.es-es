---
description: Tablet PC incluye tecnología para interactuar con los datos del lápiz de Tablet PC a medida que se recopilan.
ms.assetid: e026f860-be4d-40a5-b951-15b8be3cd626
title: Acceso y manipulación de la entrada del lápiz óptico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 333126f195154241333127ec585864bd9d592a08
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666204"
---
# <a name="accessing-and-manipulating-stylus-input"></a>Acceso y manipulación de la entrada del lápiz óptico

Tablet PC incluye tecnología para interactuar con los datos del lápiz de Tablet PC a medida que se recopilan. La clase [**RealTimeStylus**](realtimestylus-class.md) forma parte de las interfaces de programación de aplicaciones (API) de StylusInput, que proporcionan acceso al flujo de datos del lápiz de Tablet PC. Estas API permiten capturar, interrumpir y modificar la secuencia de forma independiente de la representación y la recopilación de entradas manuscritas.

Las API de StylusInput están diseñadas para:

-   Proporcionar acceso en tiempo real al flujo de datos del lápiz de Tablet PC.
-   Impedir que el subproceso de la interfaz de usuario (UI) bloquee la representación dinámica de la tinta al poner en cola los datos del paquete en el subproceso de la interfaz de usuario y hacer que la colección de tintas sea de
-   Aumente el rendimiento y reduzca el uso general de subprocesos con el objeto [**InkCollector**](inkcollector-class.md) , el objeto [**InkOverlay**](inkoverlay-class.md) , el control [InkPicture](inkpicture-control-reference.md) o el control [InkEdit](inkedit-control-reference.md) para recopilar la entrada de lápiz.

Las API de StylusInput no están diseñadas para funcionar con el objeto [**InkCollector**](inkcollector-class.md) , el objeto [**InkOverlay**](inkoverlay-class.md) , el control [InkPicture](inkpicture-control-reference.md) o el control [InkEdit](inkedit-control-reference.md) .

Si necesita interactuar directamente con el flujo de datos del lápiz de Tablet PC o si la aplicación puede bloquear la entrada manuscrita en tiempo real, use el objeto [**RealTimeStylus**](realtimestylus-class.md) . Use el objeto [**InkCollector**](inkcollector-class.md) , el objeto [**InkOverlay**](inkoverlay-class.md) , el control [InkPicture](inkpicture-control-reference.md) o el control [InkEdit](inkedit-control-reference.md) cuando el comportamiento predeterminado de estos objetos proporcione el comportamiento que necesita.

## <a name="in-this-section"></a>En esta sección

En las secciones siguientes se describen los elementos de las API de StylusInput:

-   [Arquitectura de las API de StylusInput](architecture-of-the-stylusinput-apis.md)
-   [Trabajar con las API de StylusInput](working-with-the-stylusinput-apis.md)
    -   [Trabajar con la clase RealTimeStylus](working-with-the-realtimestylus-class.md)
    -   [Complementos y la clase RealTimeStylus](plug-ins-and-the-realtimestylus-class.md)
    -   [Datos de complementos y clase RealTimeStylus](plug-in-data-and-the-realtimestylus-class.md)
    -   [Notas de implementación para las API de StylusInput](implementation-notes-for-the-stylusinput-apis.md)
    -   [Complementos de recopilación de tintas](ink-collection-plug-ins.md)
    -   [Complementos de representador dinámico](dynamic-renderer-plug-ins.md)
    -   [Complementos de reconocedor](recognizer-plug-ins.md)
-   [Consideraciones al usar las API de StylusInput](considerations-when-using-the-stylusinput-apis.md)
    -   [Consideraciones de diseño para las API de StylusInput](design-considerations-for-the-stylusinput-apis.md)
    -   [Consideraciones sobre los subprocesos para las API de StylusInput](threading-considerations-for-the-stylusinput-apis.md)

[El modelo RealTimeStylus en cascada](the-cascaded-realtimestylus-model.md)

-   [Consideraciones sobre el control de errores para las API de StylusInput](error-handling-considerations-for-the-stylusinput-apis.md)
-   [Consideraciones de rendimiento para las API de StylusInput](performance-considerations-for-the-stylusinput-apis.md)
-   [Consideraciones de confianza parcial para las API de StylusInput](partial-trust-considerations-for-the-stylusinput-apis.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ejemplo de complemento RealTimeStylus](realtimestylus-plug-in-sample.md)
</dt> <dt>

[Ejemplo de colección de tintas RealTimeStylus](realtimestylus-ink-collection-sample.md)
</dt> </dl>

 

 



