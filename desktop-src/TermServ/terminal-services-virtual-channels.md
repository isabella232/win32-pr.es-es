---
title: Servicios de Escritorio remoto canales virtuales
description: Los canales virtuales son extensiones de software que se pueden usar para agregar mejoras funcionales a una Servicios de Escritorio remoto aplicación.
ms.assetid: f7bdebec-ecc3-4f28-9327-f0d2f169c142
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2898288ee60ea409e3220dc7295f9baa704d804ddea2af5ef344a595ccd01c57
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119869785"
---
# <a name="remote-desktop-services-virtual-channels"></a>Servicios de Escritorio remoto canales virtuales

*Los canales* virtuales son extensiones de software que se pueden usar para agregar mejoras funcionales a una Servicios de Escritorio remoto aplicación. Algunos ejemplos de mejoras funcionales pueden ser: compatibilidad con tipos especiales de hardware, audio u otras adiciones a la funcionalidad principal proporcionada por Servicios de Escritorio remoto [Protocolo de escritorio remoto](remote-desktop-protocol.md) (RDP). El protocolo RDP proporciona administración multiplexada de varios canales virtuales.

## <a name="in-this-section"></a>En esta sección

<dl> <dt>

[Uso Servicios de Escritorio remoto canales virtuales](using-terminal-services-virtual-channels.md)
</dt> <dd>

Para implementar un canal virtual, proporcione los módulos de servidor y cliente de la aplicación de un canal virtual.

</dd> <dt>

[Referencia de canales virtuales dinámicos](dynamic-virtual-channels-reference.md)
</dt> <dd>

Las interfaces de cliente de canal virtual dinámico (DVC) son compatibles con Servicios de Escritorio remoto.

</dd> <dt>

[Referencia de canales virtuales de gráficos](graphics-virtual-channels-reference.md)
</dt> <dd>

La referencia de canales virtuales de gráficos contiene elementos de programación que permiten crear un canal de gráficos virtuales.

</dd> </dl>

Una aplicación de canal virtual tiene dos partes: un módulo de cliente y un módulo de servidor. El módulo de servidor es un programa ejecutable que se ejecuta en el Escritorio remoto host de sesión de Escritorio remoto. El módulo de cliente es un archivo DLL que se debe cargar en memoria en el equipo cliente cuando se ejecuta el Conexión a Escritorio remoto cliente de Conexión a Escritorio remoto (RDC).

Los canales virtuales pueden agregar mejoras funcionales a un cliente Conexión a Escritorio remoto (RDC), independientemente del protocolo RDP. Con la compatibilidad con canales virtuales, se pueden agregar nuevas características sin tener que actualizar el software de cliente o servidor, ni el protocolo RDP.

Se han identificado cuatro clases principales de usuarios de canales virtuales:

-   Controladores generales en modo kernel, como controladores serie o de impresora.
-   Redireccionamiento del sistema de archivos (esto es simplemente un caso especial de un controlador en modo kernel general).
-   Aplicaciones en modo de usuario, por ejemplo, cortar y pegar de forma remota.
-   Dispositivos de audio.

Para obtener más información, vea [Using Servicios de Escritorio remoto Virtual Channels](using-terminal-services-virtual-channels.md).

Si ha habilitado una aplicación de canales virtuales en la implementación de Servicios de Escritorio remoto, puede hacer que la aplicación esté disponible para los equipos cliente que acceden al servidor host de sesión de Escritorio remoto mediante el control Escritorio remoto microsoft ActiveX. Para obtener más información, vea [Canales virtuales](scriptable-virtual-channels.md) que se pueden incluir en scripts y [Uso del control Escritorio remoto ActiveX con canales virtuales.](using-the-remote-desktop-activex-control-with-virtual-channels.md)

 

 




