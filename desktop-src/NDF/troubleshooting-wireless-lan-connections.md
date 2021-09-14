---
title: Solución de problemas de conexiones LAN inalámbricas
description: En este escenario, un usuario está intentando conectarse a una LAN inalámbrica, pero no puede conectarse. Puede usar Netsh y Monitor de red para recopilar y ver seguimientos con el fin de ayudar a determinar por qué se ha podido realizar la conexión.
ms.assetid: 558dae83-aa16-4751-a497-d7a0da01ce5d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55878afcee0091634415d4dbc465d1b143f46057
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074198"
---
# <a name="troubleshooting-wireless-lan-connections"></a>Solución de problemas de conexiones LAN inalámbricas

En este escenario, un usuario está intentando conectarse a una LAN inalámbrica, pero no puede conectarse. Puede usar Netsh y Monitor de red para recopilar y ver seguimientos con el fin de ayudar a determinar por qué se ha podido realizar la conexión.

En primer lugar, puede usar netsh para iniciar un seguimiento. Al escribir **netsh trace start scenario = wlan tracefile=wlanwpp.etl,** se inicia el seguimiento de todos los proveedores habilitados en el escenario de WLAN, guardando los resultados en un archivo denominado wlanwpp.etl. Después de intentar conectarse a la LAN inalámbrica, al escribir **netsh trace stop** finaliza y correlaciona el archivo de seguimiento.

A continuación, puede abrir el archivo wlanwpp.etl en Monitor de red. Los eventos se agrupan por identificador de actividad en el panel izquierdo.

![solución de problemas de conexiones lan inalámbricas mediante el monitor de red (1)](images/1wlan.png)

El ETL contiene muchos seguimientos de otros proveedores de red que están habilitados. Puede aplicar un filtro para mostrar solo los eventos que son relevantes para el proveedor **WLAN \_ MicrosoftWindowsWlanAutoConfig.**

![solución de problemas de conexiones lan inalámbricas mediante el monitor de red (2)](images/2wlan.png)

Una vez aplicado el filtro, puede revisar los eventos del resumen del marco para identificar un evento que parezca pertinente. Después de seleccionar el evento, haga clic con el botón derecho y seleccione Buscar conversaciones y, a continuación, haga clic en NetEvent.

![solución de problemas de conexiones lan inalámbricas mediante el monitor de red (3)](images/3wlan.png)

Expandir los elementos bajo un identificador de actividad en el panel izquierdo le permitirá ver todos los demás proveedores pertinentes para el intento de conexión. Para ver los eventos de otros proveedores, se quitan todos los filtros haciendo clic **en Quitar en** el panel **Mostrar** filtro. Los seguimientos se pueden analizar desplazando por el resumen del marco y seleccionando eventos adicionales según sea necesario para recopilar más información. En este caso, el panel Detalles del marco proporciona información de que el error se debe a un error de intercambio de claves, lo más probable es que el usuario escriba la clave de paso incorrecta.

 

 




