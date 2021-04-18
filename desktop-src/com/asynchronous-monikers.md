---
title: Monikers asincrónicos
description: Monikers asincrónicos
ms.assetid: 24c50f7b-f085-4086-aa44-81e5cab011cb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e19323af3a972a2b83a290176a4b26fb79382da0
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "105714473"
---
# <a name="asynchronous-monikers"></a>Monikers asincrónicos

La arquitectura de moniker de OLE proporciona un modelo de programación coherente y extensible para trabajar con objetos de Internet, proporcionando métodos para analizar nombres, que representan localizadores de recursos universales (URL) como nombres imprimibles, y localizar y enlazar a los objetos representados por cadenas de dirección URL. (Consulte también [monikers de dirección URL](url-monikers.md)). Sin embargo, los monikers estándar de OLE (especialmente, los monikers de elementos, archivos y punteros) no son adecuados para Internet porque son sincrónicos y devuelven un puntero a un objeto o su almacenamiento solo en ese momento, ya que todos los datos están disponibles. Dependiendo de la cantidad de datos que se van a descargar, el enlace de forma sincrónica puede asociar la interfaz de usuario del cliente durante períodos prolongados.

Internet requiere nuevos enfoques para el diseño de aplicaciones. Las aplicaciones deben poder realizar todas las operaciones de red costosas de forma asincrónica para evitar la detención de la interfaz de usuario. Una aplicación debe ser capaz de desencadenar una operación y recibir notificaciones sobre la finalización completa o parcial. En ese momento, la aplicación debe elegir entre continuar con el siguiente paso de la operación o proporcionar información adicional según sea necesario. A medida que se lleva a cabo una descarga, una aplicación también debe ser capaz de proporcionar información de progreso y la oportunidad de cancelar la operación en cualquier momento.

Los monikers asincrónicos proporcionan estas capacidades, así como varios niveles de comportamiento de enlace asincrónico, a la vez que proporcionan compatibilidad con versiones anteriores para las aplicaciones que no se reconocen o que no requieren un comportamiento asincrónico. Otra tecnología OLE, almacenamiento asincrónico, funciona con monikers asincrónicos para proporcionar descarga asincrónica del estado persistente de un objeto de Internet. El moniker asincrónico desencadena la operación de enlace y configura los componentes necesarios, incluidos los objetos de almacenamiento y de secuencia, los objetos de matriz de bytes y los receptores de notificación. Una vez que los componentes están conectados, el moniker sale del camino y el resto del enlace se ejecuta principalmente entre los componentes que implementan los componentes de almacenamiento asincrónico y el objeto.

Para obtener más información, vea los temas siguientes:

-   [Monikers asincrónicos y sincrónicos](./asynchronous-vs.-synchronous-monikers.md)
-   [Enlace asincrónico y sincrónico](./asynchronous-vs.-synchronous-binding.md)
-   [Almacenamiento asincrónico y sincrónico](./asynchronous-vs.-synchronous-storage.md)
-   [Modelo de extracción de datos y modelo de Data-Push](./data-pull-model-vs.-data-push-model.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Monikers de URL](url-monikers.md)
</dt> </dl>

 

 