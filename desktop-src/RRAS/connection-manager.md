---
title: Administrador de conexiones
description: Los clientes que deseen desarrollar marcadores personalizados mediante la API del servicio de acceso remoto pueden investigar el administrador de conexiones de Microsoft y el kit de administración de Connection Manager.
ms.assetid: c3227aea-ba36-44f6-b69d-2c6aa4be360e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7959482542630b6dc90149971df08f7944f83fc
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/20/2020
ms.locfileid: "104077380"
---
# <a name="connection-manager"></a>Administrador de conexiones

Los clientes que deseen desarrollar marcadores personalizados mediante la API del servicio de acceso remoto pueden investigar el administrador de conexiones de Microsoft y el kit de administración de Connection Manager. El administrador de conexiones es el cliente de acceso remoto administrado de Microsoft. Permite a un administrador crear un paquete de configuración de acceso remoto que se va a distribuir a los usuarios remotos del administrador. Para obtener más información sobre el administrador de conexiones y el kit de administración de Connection Manager, vea la ayuda en pantalla de Microsoft Windows 2000 Server y los sistemas operativos posteriores.

Puede encontrar el código fuente de una acción personalizada del administrador de conexiones de ejemplo en el kit de desarrollo de software (SDK) completo de la plataforma. El SDK de la plataforma se puede descargar en el [sitio web de Microsoft](https://msdn.microsoft.com/windowsserver/bb980924.aspx). Después de la instalación, la ruta de acceso al código de ejemplo es% install path% \\ Microsoft SDK \\ Samples \\ netds \\ ras \\ ConnectionManager, donde% install path% designa el directorio de instalación base del SDK de la plataforma (por ejemplo, C: \\ archivos de programa).

Las acciones personalizadas permiten que el cliente de acceso remoto realice acciones específicas en varios puntos del proceso de conexión. La acción personalizada que se muestra en el ejemplo ajusta automáticamente la configuración del servidor proxy para una conexión basada en la dirección del servidor de la conexión. Los clientes pueden usar este ejemplo como punto de partida para crear sus propias acciones personalizadas.

 

 




