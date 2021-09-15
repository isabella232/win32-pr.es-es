---
title: Monikers asincrónicos
description: Monikers asincrónicos
ms.assetid: 24c50f7b-f085-4086-aa44-81e5cab011cb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e19323af3a972a2b83a290176a4b26fb79382da0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127574133"
---
# <a name="asynchronous-monikers"></a>Monikers asincrónicos

La arquitectura de moniker OLE proporciona un modelo de programación coherente y extensible para trabajar con objetos de Internet, proporcionar métodos para analizar nombres, representar localizadores de recursos universales (URL) como nombres imprimibles y buscar y enlazar a los objetos representados por cadenas de dirección URL. (Consulte también [URL Monikers).](url-monikers.md) Sin embargo, los monikers OLE estándar (en particular, los monikers item, file y pointer) no son adecuados para Internet porque son sincrónicos y devuelven un puntero a un objeto o su almacenamiento solo en el momento en que todos los datos están disponibles. En función de la cantidad de datos que se descargarán, el enlace de forma sincrónica puede vincular la interfaz de usuario del cliente durante períodos prolongados.

Internet requiere nuevos enfoques para el diseño de aplicaciones. Las aplicaciones deben poder realizar todas las operaciones de red costosas de forma asincrónica para evitar detener la interfaz de usuario. Una aplicación debe ser capaz de desencadenar una operación y recibir una notificación cuando se completa o parcialmente. En ese momento, la aplicación debe tener la opción de continuar con el paso siguiente de la operación o proporcionar información adicional según sea necesario. A medida que avanza una descarga, una aplicación también debe poder proporcionar a los usuarios información de progreso y la oportunidad de cancelar la operación en cualquier momento.

Los monikers asincrónicos proporcionan estas funcionalidades, así como varios niveles de comportamiento de enlace asincrónico, a la vez que proporcionan compatibilidad con versiones anteriores para aplicaciones que no son conscientes o no requieren un comportamiento asincrónico. Otra tecnología OLE, el almacenamiento asincrónico, funciona con monikers asincrónicos para proporcionar la descarga asincrónica del estado persistente de un objeto de Internet. El moniker asincrónico desencadena la operación de enlace y configura los componentes necesarios, incluidos los objetos de almacenamiento y secuencia, los objetos de matriz de bytes y los receptores de notificación. Una vez conectados los componentes, el moniker se sale del camino y el resto del enlace se ejecuta principalmente entre los componentes que implementan los componentes de almacenamiento asincrónico y el objeto .

Para obtener más información, vea los temas siguientes:

-   [Monikers asincrónicos y sincrónicos](./asynchronous-vs.-synchronous-monikers.md)
-   [Enlace asincrónico y sincrónico](./asynchronous-vs.-synchronous-binding.md)
-   [Datos asincrónicos y sincrónicos Storage](./asynchronous-vs.-synchronous-storage.md)
-   [Modelo de extracción de datos y modelo Data-Push datos](./data-pull-model-vs.-data-push-model.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[URL Monikers](url-monikers.md)
</dt> </dl>

 

 