---
description: Configuración
ms.assetid: aba21473-07cc-4de9-a310-ad9b43c133eb
title: Configuración (ventanas y mensajes)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bac66d2ba25e81582734eb13148d2651b276ea01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278628"
---
# <a name="configuration-windows-and-messages"></a>Configuración (ventanas y mensajes)

Los *elementos de visualización* son los elementos de una ventana y la pantalla que aparecen en la pantalla de presentación del sistema. Las *métricas del sistema* son las dimensiones de varios elementos de visualización. Las métricas típicas del sistema incluyen el ancho del borde de la ventana, el alto del icono, etc. Las métricas del sistema también describen otros aspectos del sistema, como, por ejemplo, si hay un mouse instalado, se admiten caracteres de doble byte o se instala una versión de depuración del sistema operativo. La función [**GetSystemMetrics**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) recupera la métrica del sistema especificada.

Las aplicaciones también pueden recuperar y establecer el color de los elementos de ventana, como los menús, las barras de desplazamiento y los botones, mediante las funciones [**GetSysColor**](/windows/desktop/api/winuser/nf-winuser-getsyscolor) y [**SetSysColors**](/windows/desktop/api/winuser/nf-winuser-setsyscolors) , respectivamente.

La función [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) recupera o establece varios atributos del sistema, como el tiempo de doble clic, el tiempo de espera del protector de pantalla, el ancho del borde de la ventana y el patrón de escritorio. Cuando una aplicación usa **SystemParametersInfo** para establecer un parámetro, el cambio tiene lugar inmediatamente. Esta función también permite a las aplicaciones actualizar el perfil de usuario, por lo que los cambios en el sistema se conservarán cuando se reinicie el sistema.

 

 
