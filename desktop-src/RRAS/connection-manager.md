---
title: Administrador de conexiones
description: Es posible que los clientes que pretenden desarrollar marcador personalizados mediante la API del servicio de acceso remoto quieran investigar Microsoft Connection Manager y el Kit de administración de Connection Manager.
ms.assetid: c3227aea-ba36-44f6-b69d-2c6aa4be360e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc20979ecd99f904aef158738d49ce1e5bc5a25309288db83dfc99de05959234
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117791589"
---
# <a name="connection-manager"></a>Administrador de conexiones

Es posible que los clientes que pretenden desarrollar marcador personalizados mediante la API del servicio de acceso remoto quieran investigar Microsoft Connection Manager y el Kit de administración de Connection Manager. Connection Manager es el cliente de acceso remoto administrado de Microsoft. Permite que un administrador compile un paquete de configuración de acceso remoto para distribuirlo a los usuarios remotos del administrador. Para obtener más información sobre Connection Manager y el Kit de administración de Connection Manager, consulte la ayuda en línea de Microsoft Windows 2000 Server y sistemas operativos posteriores.

Puede encontrar el código fuente de un ejemplo de Connection Manager acción personalizada en el Kit de desarrollo de software (SDK) de plataforma completo. El SDK de plataforma se puede descargar en el sitio [web de Microsoft](https://msdn.microsoft.com/windowsserver/bb980924.aspx). Después de la instalación, la ruta de acceso al código de ejemplo es %Ruta de instalación% Ejemplos del SDK de \\ Microsoft netds Ras ConnectionManager, donde %Ruta de instalación% designa el directorio de instalación base del SDK de plataforma \\ \\ \\ \\ (por ejemplo, C: Archivos de \\ programa).

Las acciones personalizadas hacen posible que el cliente de acceso remoto realice acciones específicas en varios puntos del proceso de conexión. La acción personalizada que se muestra en el ejemplo ajusta automáticamente la configuración del servidor proxy para una conexión en función de la dirección del servidor de la conexión. Los clientes pueden usar este ejemplo como punto de partida para crear sus propias acciones personalizadas.

 

 




