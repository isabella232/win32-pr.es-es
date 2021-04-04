---
title: Solución de problemas de conexiones LAN inalámbricas
description: En este escenario, un usuario está intentando conectarse a una LAN inalámbrica, pero no puede conectarse. Puede usar netsh y Monitor de red para recopilar y ver seguimientos con el fin de ayudar a determinar por qué se produjo un error en la conexión.
ms.assetid: 558dae83-aa16-4751-a497-d7a0da01ce5d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55878afcee0091634415d4dbc465d1b143f46057
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076195"
---
# <a name="troubleshooting-wireless-lan-connections"></a>Solución de problemas de conexiones LAN inalámbricas

En este escenario, un usuario está intentando conectarse a una LAN inalámbrica, pero no puede conectarse. Puede usar netsh y Monitor de red para recopilar y ver seguimientos con el fin de ayudar a determinar por qué se produjo un error en la conexión.

En primer lugar, puede usar Netsh para iniciar un seguimiento. Escribiendo **netsh Trace Start Scenario = WLAN seguimiento = wlanwpp. ETL** inicia el seguimiento de todos los proveedores habilitados en el escenario de WLAN y guarda los resultados en un archivo denominado wlanwpp. ETL. Después de intentar conectarse a la LAN inalámbrica, escribir **netsh Trace STOP** finaliza y correlaciona el archivo de seguimiento.

Después, puede abrir el archivo wlanwpp. ETL en Monitor de red. Los eventos se agrupan por ID. de actividad en el panel izquierdo.

![solución de problemas de conexiones LAN inalámbricas mediante el monitor de red (1)](images/1wlan.png)

ETL contiene muchos seguimientos de otros proveedores de red que están habilitados. Puede aplicar un filtro para mostrar solo los eventos que son relevantes para el proveedor **de \_ MicrosoftWindowsWlanAutoConfig de WLAN** .

![solución de problemas de conexiones LAN inalámbricas mediante el monitor de red (2)](images/2wlan.png)

Una vez aplicado el filtro, puede revisar los eventos en el resumen del marco para identificar un evento que parezca relevante. Después de seleccionar el evento, haga clic con el botón derecho y seleccione Buscar conversaciones y, a continuación, haga clic en NetEvent.

![solución de problemas de conexiones LAN inalámbricas mediante el monitor de red (3)](images/3wlan.png)

La expansión de los elementos en un ID. de actividad en el panel izquierdo le permitirá ver todos los demás proveedores relevantes para el intento de conexión. Para ver los eventos de otros proveedores, se quitan todos los filtros haciendo clic en **quitar** en el panel **Mostrar filtro** . Los seguimientos se pueden analizar desplazándose por el resumen del marco y seleccionando eventos adicionales según sea necesario para recopilar más información. En este caso, el panel Detalles del marco proporciona información de que el error se debe a un error de intercambio de claves, probablemente debido a que el usuario escribe la clave de paso equivocada.

 

 




