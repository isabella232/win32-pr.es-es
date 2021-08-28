---
description: La lista siguiente contiene las características compatibles con TAPI MSP.
ms.assetid: e36bba94-1fa7-4514-9f8a-bcd690b04d73
title: Características admitidas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32f0a37664a578bd091ce9972c1979dc7d22f4db33ab2f8eb803bc2c83642f47
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120080515"
---
# <a name="features-supported"></a>Características admitidas

La lista siguiente contiene las características compatibles con TAPI MSP.

-   Implementa un MSP que controla una única dirección por instancia del MSP. Varias direcciones de tipo se controlan mediante la creación de instancias del MSP varias veces. Esto simplifica en gran medida la implementación del MSP y las clases base.
-   Implementa todas las interfaces MSPI, incluidas [**ITMSPAddress,**](/windows/desktop/api/msp/nn-msp-itmspaddress) [**ITTerminalSupport,**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport) [**ITStreamControl**](/windows/win32/api/tapi3if/nn-tapi3if-itstreamcontrol)e [**ITStream.**](/windows/win32/api/tapi3if/nn-tapi3if-itstream)
-   Implementa terminales estáticos listos para usar para audio y vídeo.
-   Implementa clases base de terminal genéricas. Estas clases base de terminal las usan las implementaciones de terminal estático mencionadas anteriormente y las implementaciones de terminales dinámicos que se encuentran en Termmgr.dll. El MSP también puede usarlos para implementar terminales adicionales.
-   Usa Terminal Manager para controlar terminales dinámicos. Crea terminales dinámicos en un subproceso de trabajo con un bombeo de mensajes (para liberar a las aplicaciones de consola de tener que procesar mensajes de ventana para terminales de representación de vídeo y para simplificar los problemas de sincronización).
-   Admite llamadas que usan un gráfico de filtros por secuencia.
-   Implementa el control de eventos de grafo.
-   Usa las API de agrupación de subprocesos, junto con un subproceso de trabajo propio, para controlar eventos.
-   Usa las API de seguimiento de Windows 2000 (desarrolladas originalmente para el proyecto de enrutamiento) junto con lógica adicional para proporcionar un mecanismo de registro genérico flexible que puede registrar simultáneamente en cualquier combinación de lo siguiente: un depurador en modo de kernel o usuario; una ventana de consola independiente con mensajes de registro separados por componente; un archivo de registro.
-   Ejecuta subprocesos libres.

 

 
