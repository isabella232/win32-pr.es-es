---
title: Servicios de devolución de llamada de ventana
description: Servicios de devolución de llamada de ventana
ms.assetid: 227602e5-7ea1-4afd-ac88-cfeabe746d1f
keywords:
- audio multimedia, servicios de devolución de llamada de ventana
- audio, servicios de devolución de llamada de ventana
- mezcladores de audio, servicios de devolución de llamada de ventana
- mezcladores, servicios de devolución de llamada de ventana
- servicios de devolución de llamada de ventana
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0248928d339dc6c1737ee9dc47f72bac0fb42fe76774e6062177c29064b44257
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119781415"
---
# <a name="window-callback-services"></a>Servicios de devolución de llamada de ventana

Los servicios mezcladores proporcionan servicios de devolución de llamada de ventana para que la aplicación pueda procesar mensajes de controladores mezcladores. Para usar estos servicios, especifique la marca CALLBACK WINDOW en el parámetro fdwOpen y un identificador de ventana en el \_ *parámetro dwCallback* de la [**función mixerOpen.**](/windows/win32/api/mmeapi/nf-mmeapi-mixeropen)  Los mensajes de controlador se envían a la función de procedimiento de ventana para la ventana identificada por el identificador en *dwCallback*. Los mensajes son específicos del tipo de dispositivo de audio.

 

 