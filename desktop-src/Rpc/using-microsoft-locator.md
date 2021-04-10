---
title: Uso del localizador de Microsoft
description: El localizador de Microsoft es el servicio de nombres predeterminado. La biblioteca en tiempo de ejecución de RPC la usa para buscar programas de servidor en sistemas host de servidor.
ms.assetid: 8481de50-4e72-432d-aef7-524f18f5c9c4
keywords:
- RPC llamada a procedimiento remoto, tareas, uso del localizador de Microsoft
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 236dce18b9286150581af925935222f3c9b3f862
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903470"
---
# <a name="using-microsoft-locator"></a>Uso del localizador de Microsoft

El localizador de Microsoft es el servicio de nombres predeterminado. La biblioteca en tiempo de ejecución de RPC la usa para buscar programas de servidor en sistemas host de servidor.

**Nota:**    Microsoft RPC Locator no es compatible con Windows Vista y sistemas operativos posteriores.

Antes de Windows 2000, el localizador de Microsoft no proporcionaba entradas del servicio de nombres persistentes. Todas las entradas del servicio de nombres se almacenan en una memoria caché en el equipo host del programa servidor. El localizador usó un mecanismo de difusión para detectar la ubicación de los servidores según lo soliciten los clientes. Siempre que se apague el sistema host, se perderán todas las entradas del servicio de nombres.

A partir de la versión de Windows 2000, el localizador de Microsoft ahora admite entradas de servicio de nombres persistentes. Para ello, el sistema emplea un servicio de directorio distribuido para almacenar las entradas del servicio de nombres. Este mecanismo tiene varias ventajas:

-   **Persistence.** Ya no es necesario que los programas de servidor exporten su información de enlace al servicio de nombres cada vez que se inician. El servicio de nombres almacena ahora la información hasta que el programa de servidor en el administrador de red la quita explícitamente.
-   **Eficiente.** Al eliminar la mayoría de las entradas del servicio de nombres, el localizador reduce el tráfico de red. También busca entradas del servicio de nombres más rápidamente.
-   **Interoperabilidad entre dominios.** Los clientes ahora pueden realizar solicitudes de servicio de nombres en varios dominios.

Las versiones actuales del localizador de Microsoft son compatibles con versiones anteriores. Por ejemplo, un sistema host de servidor que ejecute el localizador que se incluye con Windows 2000 puede funcionar correctamente en una red que contenga sistemas host de servidor que ejecuten el localizador que se incluye con Windows NT 4,0.

Con el lanzamiento de Windows 2000, el localizador de Microsoft ahora admite entradas de servicio de nombres para grupos de usuarios. También ofrece la posibilidad de crear perfiles de usuario.

Además, la versión actual del localizador de Microsoft admite el uso de listas de Access Control en entradas del servicio de nombres. Esta capacidad mejora la seguridad de la red.

La compatibilidad con Plug and Play se incluye ahora en el localizador de Microsoft. Por lo tanto, puede controlar de forma transparente los eventos de Plug and Play, como los cambios de dominio. Para obtener más información, vea [**RpcNsBindingExportPnP**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingexportpnpa) y [**RpcNsBindingUnexportPnP**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingunexportpnpa).

 

 




