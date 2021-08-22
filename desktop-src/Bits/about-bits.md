---
title: Acerca de BITS
description: Use Servicio de transferencia inteligente en segundo plano (BITS) para transferir archivos de forma asincrónica entre un cliente y un servidor.
ms.assetid: 056007f4-6a71-4f8e-bf7d-17ed87088edf
keywords:
- Servicio de transferencia inteligente en segundo plano, descrito
- bits de la cola de transferencia
- transfer queue BITS , throttle
ms.topic: article
ms.date: 7/12/2019
ms.openlocfilehash: 53693b7087d647e8d6e89a8c81e09895dc3866b964642475466bbf8f52ddbae5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119529285"
---
# <a name="about-bits"></a>Acerca de BITS

Use Servicio de transferencia inteligente en segundo plano (BITS) para descargar o cargar archivos en servidores web HTTP o servidores de archivos SMB. 

BITS continúa transfiriendo archivos después de que se cierre una aplicación, siempre y cuando el usuario que inició la transferencia permanezca conectado y se mantenga una conexión de red. BITS no forzará una conexión de red. BITS reanuda las transferencias después de que se restablezca una conexión de red que se había perdido o después de que un usuario que había cerrado sesión de nuevo. Para obtener más información, vea [Usuarios y conexiones de red.](users-and-network-connections.md)

BITS es consciente del costo de red y la congestión actuales para que un trabajo en segundo plano interfiera lo menos posible con la experiencia en primer plano del usuario. BITS usa ancho de [banda de red](network-bandwidth.md) inactivo para transferir los archivos y aumentará o disminuirá la velocidad a la que se transfieren los archivos en función de la cantidad de ancho de banda de red inactivo disponible. Si una aplicación de red empieza a consumir más ancho de banda, BITS reduce la velocidad de transferencia para conservar la experiencia interactiva del usuario. BITS usa directivas de transferencia especificadas [por la aplicación](how-to-block-a-bits-job-from-downloading-over-an-expensive-connection.md) para evitar que los archivos se transfieran en conexiones de red costosas.

BITS también es consciente del uso de energía. A partir del Actualización de mayo de 2019 de Windows 10, BITS transferirá archivos [](/windows-hardware/design/device-experiences/modern-standby) cuando la máquina esté en modo de espera moderna y la máquina esté conectada.

La aplicación BITS puede usar los distintos niveles de [prioridad](/windows/desktop/api/Bits/ne-bits-bg_job_priority) de BITS para permitir que BITS elija de forma inteligente qué trabajos de transferencia se ejecutarán. Los trabajos con prioridad superior prevalecen sobre los trabajos con prioridad inferior. Los trabajos con el mismo nivel de prioridad comparten el período de transferencia, lo que evita que un trabajo grande bloquee los trabajos pequeños en la cola de transferencias. Los trabajos con prioridad inferior no reciben tiempo de transferencia hasta que todos los trabajos con prioridad superior se han completado o están en estado de error.

BITS usa Windows BranchCache para el almacenamiento en caché del mismo nivel. Para obtener más información, vea [Información general de BranchCache.](/previous-versions/windows/it-pro/windows-7/dd755969(v=ws.10))

Los desarrolladores Windows plataforma universal (UWP) deben usar [el Windows. API Networking.BackgroundTransfer](/uwp/api/Windows.Networking.BackgroundTransfer) y no la API de BITS.

Hay tres tipos de trabajos [**de transferencia.**](/windows/desktop/api/Bits/ne-bits-bg_job_type) Un trabajo de descarga descarga archivos en el cliente, un trabajo de carga carga un archivo en el servidor y un trabajo de carga y respuesta carga un archivo en el servidor y recibe un archivo de respuesta de la aplicación de servidor.

En los temas siguientes se proporciona información más detallada sobre BITS:

-   [Autenticación](authentication.md)
-   [Ciclo de vida de un trabajo de BITS](life-cycle-of-a-bits-job.md)
-   [Usuarios y conexiones de red](users-and-network-connections.md)
-   [Ancho de banda de red](network-bandwidth.md)
-   [Directivas de grupo](group-policies.md)
-   [Cuentas de servicio y BITS](service-accounts-and-bits.md)
-   [Tokens auxiliares para trabajos de transferencia de BITS](helper-tokens-for-bits-transfer-jobs.md)
-   [Coherencia de transferencia de archivos](file-transfer-consistency.md)
-   [Requisitos HTTP para descargas de BITS](http-requirements-for-bits-downloads.md)
-   [Requisitos de IIS para cargas de BITS](iis-requirements-for-bits-uploads.md)
-   [Limpieza de directorios virtuales](virtual-directory-cleanup.md)
-   [BITS y Restaurar sistema](bits-and-system-restore.md)
-   [Tipo de inicio de BITS](bits-startup-type.md)
-   [Conexión compartida a Internet](internet-connection-sharing.md)
-   [Almacenamiento en caché del mismo nivel](peer-caching.md)
-   [Seguridad, tokens y cuentas de administrador de BITS](user-account-control-and-bits.md)
-   [BITS Compact Server](bits-compact-server.md)

Use las [interfaces bits para](bits-interfaces.md) escribir aplicaciones que crean y supervisan trabajos de transferencia. Para obtener más información sobre el uso de las interfaces bits, consulte [Uso de BITS.](using-bits.md)