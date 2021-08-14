---
title: Solución de problemas de conexiones a Internet
description: En este escenario, un usuario está intentando ir a www.msn.com mediante el protocolo https, pero no puede conectarse. Puede usar Netsh y Monitor de red para recopilar y ver seguimientos con el fin de ayudar a determinar por qué se ha fallado la conexión.
ms.assetid: e10fcc24-4670-461c-a145-3910c102e81f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fadeefe0413a5a6be5d3ec7f5676ef346e21bc1f4b9e4c3cca026b54d761784
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118133405"
---
# <a name="troubleshooting-internet-connections"></a>Solución de problemas de conexiones a Internet

En este escenario, un usuario está intentando ir a www.msn.com mediante el protocolo https, pero no puede conectarse. Puede usar Netsh y Monitor de red para recopilar y ver seguimientos con el fin de ayudar a determinar por qué se ha fallado la conexión.

En primer lugar, puede usar netsh para iniciar un seguimiento. Al escribir **netsh trace start scenario = InternetClient tracefile=msn.etl,** se inicia el seguimiento de todos los proveedores habilitados en el escenario InternetClient, guardando los resultados en un archivo denominado msn.etl. Después de usar un explorador web para intentar acceder a www.msn.com, al escribir **netsh trace stop** finaliza y correlaciona el archivo de seguimiento.

A continuación, puede abrir el archivo msn.etl en Monitor de red. Los eventos se agrupan por identificador de actividad en el panel izquierdo. Con el filtro **description.contains("msn")** solo se mostrarán los eventos que incluyen la cadena "msn" en su descripción del protocolo.

![solución de problemas de conexiones a Internet mediante el monitor de red (1)](images/internetclient1.png)

A continuación, puede revisar los eventos en el resumen del marco para identificar un evento que parece relevante. Después de seleccionar el evento, haga clic con el botón derecho y seleccione Buscar conversaciones y, a continuación, haga clic en UTEvent para seleccionar la conversación en el nivel UTEvent.

![solución de problemas de conexiones a Internet mediante el monitor de red (2)](images/internetclient2.png)

A continuación, se resalta la actividad normalizada asociada en el panel izquierdo, en este caso UTEvent ActivityID 397.

![solución de problemas de conexiones a Internet mediante el monitor de red (3)](images/internetclient3.png)

Al usar Monitor de red para ver y filtrar la información de seguimiento, el número de eventos que se examinarán se ha reducido de 1989 a 96.

 

 




