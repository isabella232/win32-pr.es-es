---
description: Tablet PC incluye tecnología para interactuar con los datos de lápiz de tableta a medida que se recopilan.
ms.assetid: e026f860-be4d-40a5-b951-15b8be3cd626
title: Acceso y manipulación de la entrada de lápiz óptico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7df56b690a8b7459f42e7d692e47dff4e9f1c00330e02cc0c912d7a3ca3dda02
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118452071"
---
# <a name="accessing-and-manipulating-stylus-input"></a>Acceso y manipulación de la entrada de lápiz óptico

Tablet PC incluye tecnología para interactuar con los datos de lápiz de tableta a medida que se recopilan. La [**clase RealTimeStylus**](realtimestylus-class.md) forma parte de las interfaces de programación de aplicaciones (API) StylusInput, que proporcionan acceso al flujo de datos del lápiz de tableta. Estas API permiten capturar, interrumpir y modificar la secuencia independientemente de la representación y la recopilación de lápiz.

Las API StylusInput están diseñadas para:

-   Proporcione acceso en tiempo real al flujo de datos del lápiz de tableta.
-   Evitar que el subproceso de la interfaz de usuario bloquee la representación de entrada de lápiz dinámica mediante la cola de los datos de paquetes en el subproceso de la interfaz de usuario y la realización de una colección de entrada de lápiz en un único subproceso.
-   Aumente el rendimiento y reduzca el uso general del subproceso con el uso del objeto [**InkCollector,**](inkcollector-class.md) el objeto [**InkOverlay,**](inkoverlay-class.md) el control [InkPicture](inkpicture-control-reference.md) o el control [InkEdit](inkedit-control-reference.md) para recopilar la entrada de lápiz.

Las API StylusInput no están diseñadas para funcionar con el objeto [**InkCollector,**](inkcollector-class.md) el objeto [**InkOverlay,**](inkoverlay-class.md) el control [InkPicture](inkpicture-control-reference.md) o el control [InkEdit.](inkedit-control-reference.md)

Cuando necesite interactuar directamente con el flujo de datos de lápiz de tableta o cuando la aplicación pueda bloquear la entrada de entrada en tiempo real, use el objeto [**RealTimeStylus.**](realtimestylus-class.md) Use el [**objeto InkCollector,**](inkcollector-class.md) el [**objeto InkOverlay,**](inkoverlay-class.md) el control [InkPicture](inkpicture-control-reference.md) o el control [InkEdit](inkedit-control-reference.md) cuando el comportamiento predeterminado de estos objetos proporciona el comportamiento que necesita.

## <a name="in-this-section"></a>En esta sección

En las secciones siguientes se describen los elementos de las API StylusInput:

-   [Arquitectura de las API StylusInput](architecture-of-the-stylusinput-apis.md)
-   [Trabajar con las API StylusInput](working-with-the-stylusinput-apis.md)
    -   [Trabajar con la clase RealTimeStylus](working-with-the-realtimestylus-class.md)
    -   [Complementos y la clase RealTimeStylus](plug-ins-and-the-realtimestylus-class.md)
    -   [Datos de complementos y clase RealTimeStylus](plug-in-data-and-the-realtimestylus-class.md)
    -   [Notas de implementación de las API StylusInput](implementation-notes-for-the-stylusinput-apis.md)
    -   [Complementos de ink-collection](ink-collection-plug-ins.md)
    -   [Complementos de representador dinámico](dynamic-renderer-plug-ins.md)
    -   [Complementos de recognizer](recognizer-plug-ins.md)
-   [Consideraciones al usar las API StylusInput](considerations-when-using-the-stylusinput-apis.md)
    -   [Consideraciones de diseño para las API StylusInput](design-considerations-for-the-stylusinput-apis.md)
    -   [Consideraciones sobre subprocesos para las API StylusInput](threading-considerations-for-the-stylusinput-apis.md)

[Modelo RealTimeStylus en cascada](the-cascaded-realtimestylus-model.md)

-   [Consideraciones sobre el control de errores para las API StylusInput](error-handling-considerations-for-the-stylusinput-apis.md)
-   [Consideraciones de rendimiento para las API StylusInput](performance-considerations-for-the-stylusinput-apis.md)
-   [Consideraciones de confianza parcial para las API StylusInput](partial-trust-considerations-for-the-stylusinput-apis.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ejemplo de complemento RealTimeStylus](realtimestylus-plug-in-sample.md)
</dt> <dt>

[Ejemplo de colección de lápiz de RealTimeStylus](realtimestylus-ink-collection-sample.md)
</dt> </dl>

 

 



