---
description: Al transformar el código de actualización de celdas life, se han descubierto varias directrices para escribir aplicaciones de red de alto rendimiento.
ms.assetid: 2c5d0610-88b5-437e-acde-214553121380
title: Procedimientos recomendados para aplicaciones interactivas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 497fc56419f8859b7490671590b4589092c4c5b37047a01b0bf80cee9bf8c213
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119996905"
---
# <a name="best-practices-for-interactive-applications"></a>Procedimientos recomendados para aplicaciones interactivas

Al transformar el código de actualización de celdas life, se han descubierto varias directrices para escribir aplicaciones de red de alto rendimiento. Algunas estrategias generales que se deben aplicar al escribir estos tipos de aplicaciones son:

-   Haga que el flujo de datos sea lo más posible, en lugar de ir en fragmentos.
-   Use algunas transacciones grandes en lugar de otras pequeñas. Las transacciones grandes también se pueden transmitir de forma eficaz.
-   Reconozca que la red es un recurso lento y poco confiable y desarrolle cada aplicación para minimizar su dependencia de la red.
-   Use una representación bien diseñada de los datos en la red. La representación de datos debe ser independiente de la arquitectura del equipo, no contener ninguna fat y, posiblemente, estar comprimida.
-   Durante la inicialización y el apagado, no haga que el usuario espere a que la red se inicie o se apague. La inicialización relacionada con la red puede tardar un tiempo relativamente largo. Separe el código de red no crítico.
-   Controle los errores según corresponda a su impacto. No todos los errores son críticos. Implemente mecanismos de recuperación y proporcione comentarios de usuario no negativos.
-   Use llamadas a procedimiento remoto (RPC) solo cuando sea necesario. RPC es sincrónico en Windows Me/98 y siempre da como resultado protocolos de chatty y fat cuando se usa para enviar pequeñas cantidades de datos.
-   Mida la sobrecarga de red mediante Netstat; es posible que se haya queprenda la sorpresa de lo que revelan las medidas.
-   Pruebe la aplicación en una variedad de redes, especialmente en redes lentas o propensas a pérdidas. Las redes LAN inalámbricas, los módems y las redes privadas virtuales (VPN) a través de Internet son buenas redes para las pruebas.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Aplicaciones de sockets Windows alto rendimiento](high-performance-windows-sockets-applications-2.md)
</dt> </dl>

 

 



