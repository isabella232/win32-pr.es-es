---
title: Monikers asincrónicos
description: Monikers asincrónicos
ms.assetid: 24c50f7b-f085-4086-aa44-81e5cab011cb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d9e9b5e427df882b7e0be84507b79c9113a46e44dad614e571a831fedecedff
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119859655"
---
# <a name="asynchronous-monikers"></a>Monikers asincrónicos

La arquitectura de moniker OLE proporciona un modelo de programación coherente y extensible para trabajar con objetos de Internet, proporcionar métodos para analizar nombres, representar localizadores de recursos universales (URL) como nombres imprimibles y buscar y enlazar a los objetos representados por cadenas de dirección URL. (Consulte también [URL Monikers).](url-monikers.md) Sin embargo, los monikers OLE estándar (en particular, los monikers de elementos, archivos y punteros) no son adecuados para Internet porque son sincrónicos y devuelven un puntero a un objeto o su almacenamiento solo en el momento en que todos los datos están disponibles. Dependiendo de la cantidad de datos que se descargarán, el enlace sincrónicamente puede vincular la interfaz de usuario del cliente durante períodos prolongados.

Internet requiere nuevos enfoques para el diseño de aplicaciones. Las aplicaciones deben poder realizar todas las operaciones de red costosas de forma asincrónica para evitar detener la interfaz de usuario. Una aplicación debe ser capaz de desencadenar una operación y recibir una notificación en caso de finalización completa o parcial. En ese momento, la aplicación debe tener la opción de continuar con el paso siguiente de la operación o proporcionar información adicional según sea necesario. A medida que avanza una descarga, una aplicación también debe poder proporcionar a los usuarios información de progreso y la oportunidad de cancelar la operación en cualquier momento.

Los monikers asincrónicos proporcionan estas funcionalidades, así como varios niveles de comportamiento de enlace asincrónico, a la vez que proporcionan compatibilidad con versiones anteriores para aplicaciones que no son conscientes o no requieren un comportamiento asincrónico. Otra tecnología OLE, el almacenamiento asincrónico, funciona con monikers asincrónicos para proporcionar la descarga asincrónica del estado persistente de un objeto de Internet. El moniker asincrónico desencadena la operación de enlace y configura los componentes necesarios, incluidos los objetos de almacenamiento y secuencia, los objetos de matriz de bytes y los receptores de notificación. Una vez conectados los componentes, el moniker se sale del camino y el resto del enlace se ejecuta principalmente entre los componentes que implementan los componentes de almacenamiento asincrónicos y el objeto .

Para obtener más información, vea los temas siguientes:

-   [Monikers asincrónicos y sincrónicos](./asynchronous-vs.-synchronous-monikers.md)
-   [Enlace asincrónico y sincrónico](./asynchronous-vs.-synchronous-binding.md)
-   [Datos asincrónicos y sincrónicos Storage](./asynchronous-vs.-synchronous-storage.md)
-   [Modelo de extracción de datos y Data-Push modelo](./data-pull-model-vs.-data-push-model.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[URL Monikers](url-monikers.md)
</dt> </dl>

 

 