---
description: Al transformar el código de actualización de celdas life, se han descubierto varias directrices para escribir aplicaciones de red de alto rendimiento.
ms.assetid: 2c5d0610-88b5-437e-acde-214553121380
title: Procedimientos recomendados para aplicaciones interactivas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89764cf19de223f4622edd947c8122bc7fe8b11a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127566861"
---
# <a name="best-practices-for-interactive-applications"></a>Procedimientos recomendados para aplicaciones interactivas

Al transformar el código de actualización de celdas life, se han descubierto varias directrices para escribir aplicaciones de red de alto rendimiento. Algunas estrategias generales que se deben aplicar al escribir estos tipos de aplicaciones son:

-   Haga que el flujo de datos sea lo más posible, en lugar de ir en fragmentos.
-   Use algunas transacciones grandes en lugar de muchas pequeñas. Las transacciones grandes también se pueden transmitir de forma eficaz.
-   Reconozca que la red es un recurso lento y poco confiable y desarrolle cada aplicación para minimizar su dependencia de la red.
-   Use una representación bien diseñada de los datos en la red. La representación de datos debe ser independiente de la arquitectura del equipo, no contener ninguna fat y, posiblemente, estar comprimida.
-   Durante la inicialización y el apagado, no haga que el usuario espere a que la red se inicie o se apague. La inicialización relacionada con la red puede tardar un tiempo relativamente largo. Separe el código de red no crítico.
-   Controle los errores según corresponda para su impacto. No todos los errores son críticos. Implemente mecanismos de recuperación y proporcione comentarios de usuario no intrusivos.
-   Use llamadas a procedimiento remoto (RPC) solo cuando corresponda. RPC es sincrónico en Windows Me/98 y siempre da como resultado protocolos chaty y fat cuando se usan para enviar pequeñas cantidades de datos.
-   Medir la sobrecarga de red mediante Netstat; es posible que le sorprenda lo que revelan sus medidas.
-   Pruebe la aplicación en una variedad de redes, especialmente lentas o propensas a pérdidas. Las redes LAN inalámbricas, los módems y las redes privadas virtuales (VPN) a través de Internet son buenas redes para las pruebas.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Aplicaciones de sockets Windows alto rendimiento](high-performance-windows-sockets-applications-2.md)
</dt> </dl>

 

 



