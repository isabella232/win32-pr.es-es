---
title: Solución de problemas de conexiones a Internet
description: En este escenario, un usuario está intentando explorar www.msn.com con el protocolo HTTPS, pero no puede conectarse. Puede usar netsh y Monitor de red para recopilar y ver seguimientos con el fin de ayudar a determinar por qué se produjo un error en la conexión.
ms.assetid: e10fcc24-4670-461c-a145-3910c102e81f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 753636c1186243a96e3cef5a4ab73244556daec4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903358"
---
# <a name="troubleshooting-internet-connections"></a>Solución de problemas de conexiones a Internet

En este escenario, un usuario está intentando explorar www.msn.com con el protocolo HTTPS, pero no puede conectarse. Puede usar netsh y Monitor de red para recopilar y ver seguimientos con el fin de ayudar a determinar por qué se produjo un error en la conexión.

En primer lugar, puede usar Netsh para iniciar un seguimiento. Al escribir **netsh Trace Start Scenario = InternetClient de seguimiento = MSN. ETL** se inicia el seguimiento de todos los proveedores habilitados en el escenario InternetClient y guarda los resultados en un archivo denominado MSN. ETL. Después de usar un explorador Web para intentar llegar a www.msn.com, escribir **netsh Trace STOP** finaliza y correlaciona el archivo de seguimiento.

Después, puede abrir el archivo MSN. ETL en Monitor de red. Los eventos se agrupan por ID. de actividad en el panel izquierdo. Con la descripción del filtro **. Contains ("MSN")** mostrará solo los eventos que incluyen la cadena "MSN" en la descripción del protocolo.

![solución de problemas de conexiones a Internet con el monitor de red (1)](images/internetclient1.png)

A continuación, puede revisar los eventos en el Resumen de fotogramas para identificar un evento que parezca relevante. Después de seleccionar el evento, haga clic con el botón derecho y seleccione Buscar conversaciones y, luego, haga clic en UTEvent para seleccionar la conversación en el nivel de UTEvent.

![solución de problemas de conexiones a Internet con el monitor de red (2)](images/internetclient2.png)

A continuación, se resalta la actividad normalizada asociada en el panel izquierdo, en este caso UTEvent ActivityID 397.

![solución de problemas de conexiones a Internet con el monitor de red (3)](images/internetclient3.png)

Al usar Monitor de red para ver y filtrar la información de seguimiento, el número de eventos que se van a examinar se ha reducido de 1989 a 96.

 

 




