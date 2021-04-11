---
title: Acerca de BITS
description: Utilice Servicio de transferencia inteligente en segundo plano (BITS) para transferir archivos de forma asincrónica entre un cliente y un servidor.
ms.assetid: 056007f4-6a71-4f8e-bf7d-17ed87088edf
keywords:
- Servicio de transferencia inteligente en segundo plano, descrito
- BITS de la cola de transferencia
- BITS de la cola de transferencia, limitación
ms.topic: article
ms.date: 7/12/2019
ms.openlocfilehash: b1ac0f587b496692ec1c2e62be06c0e64766a205
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104149313"
---
# <a name="about-bits"></a>Acerca de BITS

Utilice Servicio de transferencia inteligente en segundo plano (BITS) para descargar o cargar archivos en servidores Web HTTP o servidores de archivos SMB. 

BITS continúa transfiriendo archivos después de que una aplicación se cierre siempre que el usuario que inició la transferencia permanezca en la sesión y se mantenga una conexión de red. BITS no forzará una conexión de red. BITS reanuda las transferencias después de que se vuelva a establecer una conexión de red que se ha perdido o después de que un usuario haya cerrado la sesión en los registros. Para obtener más información, consulte [usuarios y conexiones de red](users-and-network-connections.md).

BITS es consciente del costo de red actual y de la congestión de forma que un trabajo en segundo plano interfiera lo menos posible con la experiencia de primer plano del usuario. BITS usa el [ancho de banda de red](network-bandwidth.md) inactivo para transferir los archivos y aumenta o disminuye la velocidad a la que se transfieren los archivos en función de la cantidad de ancho de banda de red inactivo disponible. Si una aplicación de red empieza a consumir más ancho de banda, BITS reduce la velocidad de transferencia para conservar la experiencia interactiva del usuario. BITS usa [directivas de transferencia](how-to-block-a-bits-job-from-downloading-over-an-expensive-connection.md) especificadas por la aplicación para evitar que los archivos se transfieran en conexiones de red costosas.

BITS también está atento al uso de energía. A partir de la actualización 2019 de Windows 10, BITS transferirá los archivos cuando el equipo esté en modo de [espera moderno](/windows-hardware/design/device-experiences/modern-standby) y el equipo esté conectado.

La aplicación BITS puede usar los distintos [niveles de prioridad](/windows/desktop/api/Bits/ne-bits-bg_job_priority) de bits para permitir que bits seleccione de forma inteligente los trabajos de transferencia que se ejecutarán. Los trabajos con prioridad superior prevalecen sobre los trabajos con prioridad inferior. Los trabajos con el mismo nivel de prioridad comparten el período de transferencia, lo que evita que un trabajo grande bloquee los trabajos pequeños en la cola de transferencias. Los trabajos con prioridad inferior no reciben tiempo de transferencia hasta que todos los trabajos con prioridad superior se han completado o están en estado de error.

BITS usa Windows BranchCache para el almacenamiento en caché del mismo nivel. Para obtener más información, vea la información [General de BranchCache](/previous-versions/windows/it-pro/windows-7/dd755969(v=ws.10)).

Los desarrolladores de Plataforma universal de Windows (UWP) deben usar la API [Windows. networking. BackgroundTransfer](/uwp/api/Windows.Networking.BackgroundTransfer) y no la API de bits.

Hay tres tipos de [**trabajos de transferencia**](/windows/desktop/api/Bits/ne-bits-bg_job_type). Un trabajo de descarga descarga archivos en el cliente, un trabajo de carga carga un archivo en el servidor y un trabajo de carga y respuesta carga un archivo en el servidor y recibe un archivo de respuesta de la aplicación de servidor.

En los temas siguientes se proporciona información más detallada sobre BITS:

-   [Autenticación](authentication.md)
-   [Ciclo de vida de un trabajo de BITS](life-cycle-of-a-bits-job.md)
-   [Usuarios y conexiones de red](users-and-network-connections.md)
-   [Ancho de banda de red](network-bandwidth.md)
-   [Directivas de grupo](group-policies.md)
-   [Cuentas de servicio y BITS](service-accounts-and-bits.md)
-   [Tokens de aplicación auxiliar para trabajos de transferencia de BITS](helper-tokens-for-bits-transfer-jobs.md)
-   [Coherencia de la transferencia de archivos](file-transfer-consistency.md)
-   [Requisitos HTTP para descargas de BITS](http-requirements-for-bits-downloads.md)
-   [Requisitos de IIS para cargas de BITS](iis-requirements-for-bits-uploads.md)
-   [Limpieza del directorio virtual](virtual-directory-cleanup.md)
-   [BITS y restauración del sistema](bits-and-system-restore.md)
-   [Tipo de inicio de BITS](bits-startup-type.md)
-   [Conexión compartida a Internet](internet-connection-sharing.md)
-   [Almacenamiento en caché del mismo nivel](peer-caching.md)
-   [Seguridad de BITS, tokens y cuentas de administrador](user-account-control-and-bits.md)
-   [Servidor BITS compacto](bits-compact-server.md)

Use las [interfaces](bits-interfaces.md) de bits para escribir aplicaciones que crean y supervisan trabajos de transferencia. Para obtener información detallada sobre el uso de las interfaces de BITS, vea [usar bits](using-bits.md).