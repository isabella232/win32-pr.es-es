---
title: Uso del localizador de Microsoft
description: Microsoft Locator es el servicio de nombres predeterminado. La biblioteca en tiempo de ejecución rpc la usa para buscar programas de servidor en sistemas host de servidor.
ms.assetid: 8481de50-4e72-432d-aef7-524f18f5c9c4
keywords:
- Llamada a procedimiento remoto RPC, tareas, mediante localizador de Microsoft
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f64a5c54c09ee344ffdba46f9f44a546ab866557bc861b206868ad6d3992896b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119010743"
---
# <a name="using-microsoft-locator"></a>Uso del localizador de Microsoft

Microsoft Locator es el servicio de nombres predeterminado. La biblioteca en tiempo de ejecución rpc la usa para buscar programas de servidor en sistemas host de servidor.

**Nota**  El localizador RPC de Microsoft no se admite en Windows Vista y sistemas operativos posteriores.

Antes de Windows 2000, Microsoft Locator no proporcionaba entradas de servicio de nombres persistentes. Todas las entradas del servicio de nombres se almacenaron en una memoria caché en el equipo host del programa de servidor. El localizador usó un mecanismo de difusión para detectar la ubicación de los servidores solicitada por los clientes. Cada vez que se apaga el sistema host, se pierden todas las entradas del servicio de nombres.

A partir del lanzamiento de Windows 2000, Microsoft Locator ahora admite entradas de servicio de nombres persistentes. Para ello, el sistema emplea un servicio de directorio distribuido para almacenar las entradas del servicio de nombres. Este mecanismo tiene varias ventajas:

-   **Persistencia.** Ya no es necesario que los programas de servidor exporten su información de enlace al servicio de nombres cada vez que se inician. El servicio de nombres ahora almacena la información hasta que el programa de servidor del administrador de red la quita explícitamente.
-   **Eficiencia.** Al eliminar la mayoría de la difusión para las entradas del servicio de nombres, el localizador reduce el tráfico de red. También busca las entradas del servicio de nombres más rápidamente.
-   **Interoperabilidad entre dominios.** Los clientes ahora pueden realizar solicitudes de servicio de nombres en varios dominios.

Las versiones actuales de Microsoft Locator son compatibles con versiones anteriores. Por ejemplo, un sistema host de servidor que ejecuta el localizador que se distribuye con Windows 2000 puede funcionar correctamente en una red que contiene sistemas host de servidor que ejecutan el localizador que se distribuye con Windows NT 4.0.

Con el lanzamiento de Windows 2000, Microsoft Locator ahora admite entradas de servicio de nombres para grupos de usuarios. También proporciona la capacidad de crear perfiles de usuario.

Además, la versión actual de Microsoft Locator admite el uso de listas de Access Control en las entradas del servicio de nombres. Esta capacidad mejora la seguridad de la red.

Plug and Play soporte técnico se incluye ahora en Microsoft Locator. Por lo tanto, puede controlar de forma transparente Plug and Play eventos como cambios de dominio. Para obtener más información, [**vea RpcNsBindingExportPnP**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingexportpnpa) y [**RpcNsBindingUnexportPnP.**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingunexportpnpa)

 

 




