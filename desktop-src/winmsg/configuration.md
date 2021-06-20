---
description: En esta sección de referencia se describe la configuración de Windows y mensajes. Obtenga información sobre los elementos de visualización y las métricas del sistema.
ms.assetid: aba21473-07cc-4de9-a310-ad9b43c133eb
title: Configuración (Windows y mensajes)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffa516e87aa7d338d4e2fd46a160fcbd6dadb305
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406348"
---
# <a name="configuration-windows-and-messages"></a>Configuración (Windows y mensajes)

*Los elementos de* visualización son las partes de una ventana y la pantalla que aparecen en la pantalla de presentación del sistema. *Las métricas del* sistema son las dimensiones de varios elementos de presentación. Las métricas típicas del sistema incluyen el ancho del borde de la ventana, el alto del icono, y así sucesivamente. Las métricas del sistema también describen otros aspectos del sistema, como si se instala un mouse, se admiten caracteres de doble byte o se instala una versión de depuración del sistema operativo. La [**función GetSystemMetrics**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) recupera la métrica del sistema especificada.

Las aplicaciones también pueden recuperar y establecer el color de los elementos de ventana, como menús, barras de desplazamiento y botones, mediante las funciones [**GetSysColor**](/windows/desktop/api/winuser/nf-winuser-getsyscolor) y [**SetSysColors,**](/windows/desktop/api/winuser/nf-winuser-setsyscolors) respectivamente.

La [**función SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) recupera o establece varios atributos del sistema, como el tiempo de doble clic, el tiempo de espera del protector de pantalla, el ancho del borde de la ventana y el patrón de escritorio. Cuando una aplicación usa **SystemParametersInfo** para establecer un parámetro, el cambio tiene lugar inmediatamente. Esta función también permite que las aplicaciones actualicen el perfil de usuario, por lo que los cambios en el sistema se conservarán cuando se reinicie el sistema.

 

 
