---
description: La lista siguiente contiene las características compatibles con TAPI MSP.
ms.assetid: e36bba94-1fa7-4514-9f8a-bcd690b04d73
title: Características admitidas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00d10fd9ac787483b8dfa6e15046a733992adb97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275430"
---
# <a name="features-supported"></a>Características admitidas

La lista siguiente contiene las características compatibles con TAPI MSP.

-   Implementa un MSP que controla una dirección única por cada instancia del MSP. Se administran varias direcciones similares mediante la creación de instancias del MSP varias veces. Esto simplifica considerablemente la implementación de las clases de MSP y base.
-   Implementa todas las interfaces de MSPI, incluidas [**ITMSPAddress**](/windows/desktop/api/msp/nn-msp-itmspaddress), [**ITTerminalSupport**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport), [**ITStreamControl**](/windows/win32/api/tapi3if/nn-tapi3if-itstreamcontrol)y [**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream).
-   Implementa terminales estáticos listos para usar para audio y vídeo.
-   Implementa clases base de terminal genéricas. Estas clases base de terminal se usan en las implementaciones de terminal estáticos mencionadas anteriormente y en las implementaciones de terminales dinámicos que se encuentran en Termmgr.dll. El MSP también puede usarlos para implementar terminales adicionales.
-   Utiliza el administrador de Terminal Server para controlar los terminales dinámicos. Crea terminales dinámicos en un subproceso de trabajo con un bombeo de mensajes (para que las aplicaciones de consola gratuitas no tengan que procesar mensajes de ventana para los terminales de representación de vídeo y para simplificar los problemas de sincronización).
-   Admite llamadas que usan un gráfico de filtro por secuencia.
-   Implementa el control de eventos de gráfico.
-   Utiliza las API de agrupación de subprocesos, junto con un subproceso de trabajo propio, para controlar eventos.
-   Usa las API de seguimiento de Windows 2000 (originalmente desarrolladas para el proyecto de enrutamiento) junto con lógica adicional para proporcionar un mecanismo de registro flexible y genérico que puede registrar simultáneamente en cualquier combinación de lo siguiente: un usuario o depurador en modo kernel; una ventana de consola independiente con mensajes de registro separados por componente; un archivo de registro.
-   Ejecuta un subproceso libre.

 

 
