---
description: La clase RealTimeStylus permite interactuar con el flujo de datos desde el lápiz de tableta. Para interactuar con el flujo de datos, agregue un objeto RealTimeStylus a la aplicación y complementos al objeto RealTimeStylus.
ms.assetid: 4009aeac-d290-4ea5-a6f5-199010acc84d
title: Trabajar con las API StylusInput
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 143cb885cda16542a65aa096cdf95eb8a187b4f760a916a895887737ec63d7e5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119842845"
---
# <a name="working-with-the-stylusinput-apis"></a>Trabajar con las API StylusInput

La [**clase RealTimeStylus**](realtimestylus-class.md) permite interactuar con el flujo de datos desde el lápiz de tableta. Para interactuar con el flujo de datos, agregue un objeto **RealTimeStylus** a la aplicación y complementos al objeto **RealTimeStylus.**

Los complementos pueden modificar los datos asociados con los paquetes en el aire, la aplicación de lápiz óptico, los paquetes y los métodos de notificación de lápiz. Los complementos pueden cancelar los métodos de notificación de paquetes y paquetes en el aire. Los complementos también pueden agregar datos de aplicación al flujo en forma de [objetos CustomStylusData.](/previous-versions/ms575208(v=vs.100)) En la lista siguiente se ofrecen ideas para las categorías comunes de complementos que puede usar o crear.

-   Complemento de filtro: objeto que quita o cancela selectivamente los datos del flujo de datos del lápiz de tableta.
-   Complemento modificador: objeto que modifica selectivamente los datos del flujo de datos del lápiz de tableta.
-   Complemento de representador dinámico: objeto que muestra los datos del lápiz de tableta en tiempo real a medida que lo controla el objeto [**RealTimeStylus.**](realtimestylus-class.md) Más adelante, para eventos como una actualización de formulario, el complemento de representador dinámico o un complemento de colección de entrada de lápiz podría volver a dibujar la entrada de lápiz.
-   Complemento de reconocedor: objeto que examina el movimiento del lápiz de tableta en busca de gestos, escritura a mano u otros glifos.
-   Complemento de recopilador de lápiz: objeto que, a partir del flujo de datos de lápiz de tableta, crea y almacena la entrada de lápiz.
-   Complemento contenedor: complemento que actúa como interfaz entre el objeto [**RealTimeStylus**](realtimestylus-class.md) y otro complemento u objeto como una manera de modificar el comportamiento del objeto encapsulado.

Tanto el representador dinámico como los complementos de colección de entrada de lápiz se pueden crear para representar en varios contextos, como en un archivo, una secuencia o en un dispositivo de visualización. Ink también se puede almacenar en varios formatos, como un objeto [Ink,](/previous-versions/aa515768(v=msdn.10)) un archivo Formato de intercambio de gráficos (GIF) Formato de intercambio de gráficos, un archivo Ink Serialized Format (ISF) u otros formatos.

Se proporcionan dos complementos con las API StylusInput: la [**clase DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) y la [**clase GestureRecognizer.**](gesturerecognizer-class.md) La **clase DynamicRenderer** proporciona una representación básica de los datos de entrada de lápiz en tiempo real y se simplifica para tener un impacto mínimo en el rendimiento. La **clase GestureRecognizer proporciona** reconocimiento de gestos para la clase [**RealTimeStylus.**](realtimestylus-class.md)

## <a name="in-this-section"></a>En esta sección

-   [Trabajar con la clase RealTimeStylus](working-with-the-realtimestylus-class.md)
-   [Complementos y la clase RealTimeStylus](plug-ins-and-the-realtimestylus-class.md)
-   [Datos de complementos y clase RealTimeStylus](plug-in-data-and-the-realtimestylus-class.md)
-   [Notas de implementación de las API StylusInput](implementation-notes-for-the-stylusinput-apis.md)
-   [Complementos de ink-collection](ink-collection-plug-ins.md)
-   [Complementos de representador dinámico](dynamic-renderer-plug-ins.md)
-   [Complementos de Recognizer](recognizer-plug-ins.md)

 

 
