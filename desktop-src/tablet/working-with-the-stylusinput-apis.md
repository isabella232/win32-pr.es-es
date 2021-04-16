---
description: La clase RealTimeStylus permite interactuar con el flujo de datos desde el lápiz de Tablet PC. Para interactuar con el flujo de datos, agregue un objeto RealTimeStylus a la aplicación y agregue complementos al objeto RealTimeStylus.
ms.assetid: 4009aeac-d290-4ea5-a6f5-199010acc84d
title: Trabajar con las API de StylusInput
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 676752f242aa428b583390d7c3d38c952b4c0edb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696324"
---
# <a name="working-with-the-stylusinput-apis"></a>Trabajar con las API de StylusInput

La clase [**RealTimeStylus**](realtimestylus-class.md) permite interactuar con el flujo de datos desde el lápiz de Tablet PC. Para interactuar con el flujo de datos, agregue un objeto **RealTimeStylus** a la aplicación y agregue complementos al objeto **RealTimeStylus** .

Los complementos pueden modificar los datos asociados a los métodos de notificación de los paquetes en el aire, el estilete hacia abajo, los paquetes y el registro de entradas de lápiz. Los complementos pueden cancelar los métodos de notificación de paquetes en Air y de paquetes. Los complementos también pueden agregar datos de la aplicación a la secuencia en forma de objetos [CustomStylusData](/previous-versions/ms575208(v=vs.100)) . En la lista siguiente se ofrecen ideas para las categorías comunes de complementos que puede querer usar o crear.

-   Complemento de filtros: objeto que quita o cancela datos de forma selectiva en el flujo de datos del lápiz de Tablet PC.
-   Complemento modificador: objeto que modifica los datos de forma selectiva en el flujo de datos del lápiz de Tablet PC.
-   Complemento de representador dinámico: objeto que muestra los datos del lápiz de Tablet PC en tiempo real, tal como lo controla el objeto [**RealTimeStylus**](realtimestylus-class.md) . Más adelante, para eventos como la actualización de un formulario, el complemento representador dinámico o un complemento de la colección de tintas podrían volver a dibujar la tinta.
-   Complemento de reconocedor: objeto que examina el movimiento del lápiz de Tablet PC en busca de gestos, escritura a mano u otros glifos.
-   Complemento de recopilador de tinta: un objeto que desde el flujo de datos del lápiz de Tablet PC crea y almacena la tinta.
-   Complemento de contenedor: un complemento que actúa como una interfaz entre el objeto [**RealTimeStylus**](realtimestylus-class.md) y otro complemento u objeto como una forma de modificar el comportamiento del objeto ajustado.

Se pueden crear complementos de representación dinámica y de colección de tintas para representar varios contextos, como un archivo, una secuencia o un dispositivo de pantalla. La entrada manuscrita también puede almacenarse en diversos formatos, como un objeto de [entrada manuscrita](/previous-versions/aa515768(v=msdn.10)) , un archivo de formato de intercambio de gráficos enriquecido (GIF), un archivo de formato serializado de tinta (ISF) u otros formatos.

Se proporcionan dos complementos con las API de StylusInput: la clase [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) y la clase [**GestureRecognizer**](gesturerecognizer-class.md) . La clase **DynamicRenderer** proporciona una representación básica de los datos de entrada de lápiz en tiempo real y se optimiza para tener un impacto mínimo en el rendimiento. La clase **GestureRecognizer** proporciona reconocimiento de gestos para la clase [**RealTimeStylus**](realtimestylus-class.md) .

## <a name="in-this-section"></a>En esta sección

-   [Trabajar con la clase RealTimeStylus](working-with-the-realtimestylus-class.md)
-   [Complementos y la clase RealTimeStylus](plug-ins-and-the-realtimestylus-class.md)
-   [Datos de complementos y clase RealTimeStylus](plug-in-data-and-the-realtimestylus-class.md)
-   [Notas de implementación para las API de StylusInput](implementation-notes-for-the-stylusinput-apis.md)
-   [Complementos de recopilación de tintas](ink-collection-plug-ins.md)
-   [Complementos de representador dinámico](dynamic-renderer-plug-ins.md)
-   [Complementos de reconocedor](recognizer-plug-ins.md)

 

 
