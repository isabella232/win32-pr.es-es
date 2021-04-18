---
description: En la transformación del código de actualización de la celda de vida, se han descubierto varias instrucciones para escribir aplicaciones de red de alto rendimiento.
ms.assetid: 2c5d0610-88b5-437e-acde-214553121380
title: Prácticas recomendadas para aplicaciones interactivas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89764cf19de223f4622edd947c8122bc7fe8b11a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715140"
---
# <a name="best-practices-for-interactive-applications"></a>Prácticas recomendadas para aplicaciones interactivas

En la transformación del código de actualización de la celda de vida, se han descubierto varias instrucciones para escribir aplicaciones de red de alto rendimiento. Algunas de las estrategias generales que se deben aplicar al escribir estos tipos de aplicaciones son:

-   Haga que el flujo de datos sea lo máximo posible, en lugar de pasar por fragmentos.
-   Use algunas transacciones grandes en lugar de muchas pequeñas. Las transacciones grandes también se pueden transmitir de forma eficaz.
-   Reconozca que la red es un recurso lento y confiable, y desarrolle cada aplicación para minimizar su dependencia en la red.
-   Usar una representación bien diseñada de los datos de la red. La representación de los datos debe ser independiente de la arquitectura del equipo, no contener ninguna FAT y, posiblemente, estar comprimida.
-   Durante la inicialización y el cierre, no haga que el usuario espere a que la red se inicie o se apague. La inicialización relacionada con la red puede tardar bastante tiempo. Separe el código de red no crítico.
-   Controlar los errores según corresponda. No todos los errores son críticos. Implementar mecanismos de recuperación y proporcionar comentarios de los usuarios no intrusivos.
-   Use llamadas a procedimiento remoto (RPC) solo cuando sea necesario. RPC es sincrónico en Windows Me/98 y siempre da como resultado la conversación y los protocolos FAT cuando se usa para enviar pequeñas cantidades de datos.
-   Mida la sobrecarga de la red mediante netstat; es posible que se sorprenda de lo que se revela en las mediciones.
-   Pruebe la aplicación en una gran variedad de redes, especialmente en redes lentas o propensas a pérdidas. Las redes LAN inalámbricas, los módems y las redes privadas virtuales (VPN) a través de Internet son buenas redes para las pruebas.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Aplicaciones de Windows Sockets de alto rendimiento](high-performance-windows-sockets-applications-2.md)
</dt> </dl>

 

 



