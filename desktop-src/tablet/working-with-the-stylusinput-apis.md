---
description: La clase RealTimeStylus permite interactuar con el flujo de datos desde el lápiz de tableta. Para interactuar con el flujo de datos, agregue un objeto RealTimeStylus a la aplicación y agregue complementos al objeto RealTimeStylus.
ms.assetid: 4009aeac-d290-4ea5-a6f5-199010acc84d
title: Trabajar con las API StylusInput
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 676752f242aa428b583390d7c3d38c952b4c0edb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127467947"
---
# <a name="working-with-the-stylusinput-apis"></a>Trabajar con las API StylusInput

La [**clase RealTimeStylus**](realtimestylus-class.md) permite interactuar con el flujo de datos desde el lápiz de tableta. Para interactuar con el flujo de datos, agregue un objeto **RealTimeStylus** a la aplicación y agregue complementos al objeto **RealTimeStylus.**

Los complementos pueden modificar los datos asociados con los paquetes en el aire, el lápiz óptico hacia abajo, los paquetes y los métodos de notificación de lápiz óptico. Los complementos pueden cancelar los métodos de notificación de paquetes y paquetes en el aire. Los complementos también pueden agregar datos de aplicación a la secuencia en forma de [objetos CustomStylusData.](/previous-versions/ms575208(v=vs.100)) En la lista siguiente se ofrecen ideas para categorías comunes de complementos que puede usar o crear.

-   Complemento de filtro: objeto que quita o cancela de forma selectiva los datos del flujo de datos del lápiz de tableta.
-   Complemento modificador: objeto que modifica los datos de forma selectiva en el flujo de datos del lápiz de tableta.
-   Complemento de representador dinámico: objeto que muestra los datos del lápiz de tableta en tiempo real mientras lo controla el objeto [**RealTimeStylus.**](realtimestylus-class.md) Más adelante, para eventos como una actualización de formulario, el complemento de representador dinámico o un complemento de colección de entrada de lápiz podrían volver a dibujar la entrada de lápiz.
-   Complemento de reconocedor: objeto que examina el movimiento del lápiz de tableta en busca de gestos, escritura a mano u otros glifos.
-   Complemento de recopilador de lápiz: objeto que a partir del flujo de datos del lápiz de tableta crea y almacena la entrada de lápiz.
-   Complemento contenedor: complemento que actúa como interfaz entre el objeto [**RealTimeStylus**](realtimestylus-class.md) y otro complemento u objeto como una manera de modificar el comportamiento del objeto encapsulado.

Tanto los complementos de representador dinámico como de colección de entrada de lápiz se pueden crear para representarse en varios contextos, como en un archivo, una secuencia o en un dispositivo de visualización. La entrada de lápiz también se puede almacenar en varios formatos, como un objeto [Ink,](/previous-versions/aa515768(v=msdn.10)) un archivo Formato de intercambio de gráficos (GIF) notificado, un archivo Ink Serialized Format (ISF) u otros formatos.

Se proporcionan dos complementos con las API StylusInput: la [**clase DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) y la [**clase GestureRecognizer.**](gesturerecognizer-class.md) La **clase DynamicRenderer** proporciona una representación básica de los datos de entrada de lápiz en tiempo real y se simplifica para tener un impacto mínimo en el rendimiento. La **clase GestureRecognizer** proporciona reconocimiento de gestos para la [**clase RealTimeStylus.**](realtimestylus-class.md)

## <a name="in-this-section"></a>En esta sección

-   [Trabajar con la clase RealTimeStylus](working-with-the-realtimestylus-class.md)
-   [Complementos y la clase RealTimeStylus](plug-ins-and-the-realtimestylus-class.md)
-   [Datos de complementos y clase RealTimeStylus](plug-in-data-and-the-realtimestylus-class.md)
-   [Notas de implementación de las API StylusInput](implementation-notes-for-the-stylusinput-apis.md)
-   [Complementos de ink-collection](ink-collection-plug-ins.md)
-   [Complementos de representador dinámico](dynamic-renderer-plug-ins.md)
-   [Complementos de recognizer](recognizer-plug-ins.md)

 

 
