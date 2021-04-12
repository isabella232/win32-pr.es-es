---
title: Servicios de devolución de llamada de ventana
description: Servicios de devolución de llamada de ventana
ms.assetid: 227602e5-7ea1-4afd-ac88-cfeabe746d1f
keywords:
- audio multimedia, servicios de devolución de llamada de ventana
- servicios de devolución de llamada de Windows y audio
- Mezcladores de audio, servicios de devolución de llamada de ventana
- mezcladores, servicios de devolución de llamada de ventanas
- servicios de devolución de llamada de ventana
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48faf2dd94b61f5d4fc47e073fe0f3875bcbb503
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104487647"
---
# <a name="window-callback-services"></a>Servicios de devolución de llamada de ventana

Los servicios del mezclador proporcionan servicios de devolución de llamada de ventana para que la aplicación pueda procesar los mensajes de los controladores del mezclador. Para usar estos servicios, especifique la marca de la ventana de devolución de llamada \_ en el parámetro *fdwOpen* y un identificador de ventana en el parámetro *DwCallback* de la función [**mixerOpen**](/windows/win32/api/mmeapi/nf-mmeapi-mixeropen) . Los mensajes de controlador se envían a la función de procedimiento de ventana para la ventana identificada por el identificador de *dwCallback*. Los mensajes son específicos del tipo de dispositivo de audio.

 

 