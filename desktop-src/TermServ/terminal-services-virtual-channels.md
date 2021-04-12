---
title: Servicios de Escritorio remoto canales virtuales
description: Los canales virtuales son extensiones de software que se pueden usar para agregar mejoras funcionales a una aplicación Servicios de Escritorio remoto.
ms.assetid: f7bdebec-ecc3-4f28-9327-f0d2f169c142
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ce78331841a41502aa337de19e9879d42d85fe1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357028"
---
# <a name="remote-desktop-services-virtual-channels"></a>Servicios de Escritorio remoto canales virtuales

Los *canales virtuales* son extensiones de software que se pueden usar para agregar mejoras funcionales a una aplicación servicios de escritorio remoto. Algunos ejemplos de mejoras funcionales pueden ser: compatibilidad con tipos especiales de hardware, audio u otras adiciones a la funcionalidad básica proporcionada por el [Protocolo de escritorio remoto](remote-desktop-protocol.md) de servicios de escritorio remoto (RDP). El protocolo RDP proporciona administración multiplexada de varios canales virtuales.

## <a name="in-this-section"></a>En esta sección

<dl> <dt>

[Uso de Servicios de Escritorio remoto canales virtuales](using-terminal-services-virtual-channels.md)
</dt> <dd>

Para implementar un canal virtual, se proporcionan los módulos de servidor y cliente de la aplicación de un canal virtual.

</dd> <dt>

[Referencia de canales virtuales dinámicos](dynamic-virtual-channels-reference.md)
</dt> <dd>

Servicios de Escritorio remoto admite las interfaces de cliente de canal virtual dinámico (DVC).

</dd> <dt>

[Referencia de canales virtuales de gráficos](graphics-virtual-channels-reference.md)
</dt> <dd>

La referencia de canales virtuales de gráficos contiene elementos de programación que permiten crear un canal de gráficos virtual.

</dd> </dl>

Una aplicación de canal virtual tiene dos partes: un módulo de cliente y un módulo de servidor. El módulo de servidor es un programa ejecutable que se ejecuta en el servidor de host de sesión de Escritorio remoto (host de sesión de escritorio remoto). El módulo cliente es un archivo DLL que se debe cargar en la memoria del equipo cliente cuando se ejecuta el programa cliente de Conexión a Escritorio remoto (RDC).

Los canales virtuales pueden agregar mejoras funcionales a un cliente Conexión a Escritorio remoto (RDC), independientemente del protocolo RDP. Con la compatibilidad con canales virtuales, se pueden agregar nuevas características sin tener que actualizar el software de cliente o servidor, o el protocolo RDP.

Se han identificado cuatro clases principales de usuarios de canales virtuales:

-   Controladores generales de modo kernel, como controladores serie o de impresora.
-   Redirección del sistema de archivos (este es solo un caso especial de un controlador de modo kernel general).
-   Aplicaciones en modo de usuario, por ejemplo, de cortar y pegar de forma remota.
-   Dispositivos de audio.

Para obtener más información, consulte [uso de servicios de escritorio remoto canales virtuales](using-terminal-services-virtual-channels.md).

Si ha habilitado una aplicación de canales virtuales en la implementación de Servicios de Escritorio remoto, puede hacer que la aplicación esté disponible para los equipos cliente que tengan acceso al servidor host de sesión de escritorio remoto por medio de la Escritorio remoto control ActiveX de Microsoft. Para obtener más información, vea [canales virtuales que admiten scripts](scriptable-virtual-channels.md) y [usar el control ActiveX escritorio remoto con canales virtuales](using-the-remote-desktop-activex-control-with-virtual-channels.md).

 

 




