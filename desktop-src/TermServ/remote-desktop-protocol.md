---
title: Protocolo de escritorio remoto
description: El protocolo de Escritorio remoto de Microsoft (RDP) proporciona funciones de entrada y visualización remotas a través de conexiones de red para aplicaciones basadas en Windows que se ejecutan en un servidor.
ms.assetid: 442c3c7f-d04b-4dcd-945d-f6e0168c59d5
ms.tgt_platform: multiple
keywords:
- Protocolo de escritorio remoto (RDP) Servicios de Escritorio remoto
- RDP (consulte Protocolo de escritorio remoto)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7895163a5ee92a6cc756dca9b097db8498d02e70
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105685734"
---
# <a name="remote-desktop-protocol"></a>Protocolo de escritorio remoto

El protocolo de Escritorio remoto de Microsoft (RDP) proporciona funciones de entrada y visualización remotas a través de conexiones de red para aplicaciones basadas en Windows que se ejecutan en un servidor. RDP está diseñado para admitir distintos tipos de topologías de red y varios protocolos de LAN.

> [!Note]  
> Este tema está destinado a los desarrolladores de software. Si busca información de usuario para Escritorio remoto, consulte [soporte técnico de Windows](https://windows.microsoft.com/windows/support#1TC=windows-8). Si está buscando información profesional de TI para Escritorio remoto, consulte [servicios de escritorio remoto en TechNet](/windows/deployment/deploy-whats-new).

 

## <a name="basic-architecture"></a>Arquitectura básica

RDP se basa en y en una extensión de la familia de protocolos ITU T. 120. RDP es un protocolo compatible con varios canales que permite canales virtuales independientes para llevar la comunicación del dispositivo y los datos de presentación del servidor, así como datos del mouse y del teclado del cliente cifrados. RDP proporciona una base extensible y admite hasta 64.000 canales independientes para la transmisión de datos y aprovisionaciones para la transmisión multipunto.

En el servidor, RDP usa su propio controlador de vídeo para representar la salida de la presentación mediante la creación de la información de representación en paquetes de red mediante el protocolo RDP y su envío a través de la red al cliente. En el cliente, RDP recibe datos de representación e interpreta los paquetes en las llamadas a la API de la interfaz de dispositivo gráfico (GDI) de Microsoft Windows correspondiente. En la ruta de acceso de entrada, los eventos del mouse y del teclado del cliente se redirigen desde el cliente al servidor. En el servidor, RDP usa su propio controlador de teclado y de mouse para recibir estos eventos de teclado y de mouse.

En una sesión de Escritorio remoto, todas las variables de entorno (por ejemplo, las variables que determinan la profundidad de color y el fondo para habilitar y deshabilitar) se determinan mediante la configuración de conexión RCP-Tcp. Esto se aplica a todas las funciones y métodos que establecen variables de entorno en la [conexión web a escritorio remoto referencia](remote-desktop-web-connection-reference.md) y la [interfaz del proveedor de WMI servicios de escritorio remoto](terminal-services-wmi-provider-reference.md).

## <a name="features"></a>Características

Microsoft RDP incluye las siguientes características y capacidades:

<dl> <dt>

<span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>Cifra
</dt> <dd>

RDP usa el cifrado RC4 de seguridad de RSA, un cifrado de flujo diseñado para cifrar de forma eficaz cantidades pequeñas de datos. RC4 está diseñado para comunicaciones seguras a través de redes. Los administradores pueden elegir cifrar los datos mediante una clave de 56 o 128 bits.

</dd> <dt>

<span id="Bandwidth_reduction_features"></span><span id="bandwidth_reduction_features"></span><span id="BANDWIDTH_REDUCTION_FEATURES"></span>Características de reducción de ancho de banda
</dt> <dd>

RDP admite varios mecanismos para reducir la cantidad de datos transmitidos a través de una conexión de red. Los mecanismos incluyen la compresión de datos, el almacenamiento en caché persistente de mapas de bits y el almacenamiento en caché de glifos y fragmentos en la RAM. La caché de mapa de bits persistente puede proporcionar una mejora sustancial en el rendimiento de las conexiones de ancho de banda bajo, especialmente cuando se ejecutan aplicaciones que hacen un uso extensivo de mapas de bits grandes.

</dd> <dt>

<span id="Roaming_disconnect"></span><span id="roaming_disconnect"></span><span id="ROAMING_DISCONNECT"></span>Desconexión de itinerancia
</dt> <dd>

Un usuario puede desconectarse manualmente de una sesión de escritorio remoto sin cerrar sesión. El usuario se vuelve a conectar automáticamente a la sesión desconectada cuando vuelve a iniciar sesión en el sistema, ya sea desde el mismo dispositivo o desde otro dispositivo. Cuando una sesión de usuario termina inesperadamente debido a un error de red o de cliente, el usuario se desconecta pero no se cierra.

</dd> <dt>

<span id="Clipboard_mapping"></span><span id="clipboard_mapping"></span><span id="CLIPBOARD_MAPPING"></span>Asignación del portapapeles
</dt> <dd>

Los usuarios pueden eliminar, copiar y pegar texto y gráficos entre aplicaciones que se ejecutan en el equipo local y que se ejecutan en una sesión de escritorio remoto, y entre sesiones.

</dd> <dt>

<span id="Print_redirection"></span><span id="print_redirection"></span><span id="PRINT_REDIRECTION"></span>Redirección de impresión
</dt> <dd>

Las aplicaciones que se ejecutan en una sesión de escritorio remoto pueden imprimir en una impresora conectada al dispositivo cliente.

</dd> <dt>

<span id="Virtual_channels"></span><span id="virtual_channels"></span><span id="VIRTUAL_CHANNELS"></span>Canales virtuales
</dt> <dd>

Mediante el uso de la arquitectura de canal virtual de RDP, se pueden aumentar las aplicaciones existentes y se pueden desarrollar nuevas aplicaciones para agregar características que requieran comunicaciones entre el dispositivo cliente y una aplicación que se ejecute en una sesión de escritorio remoto.

</dd> <dt>

<span id="Remote_control"></span><span id="remote_control"></span><span id="REMOTE_CONTROL"></span>Control remoto
</dt> <dd>

El personal de soporte técnico de equipos puede ver y controlar una sesión de escritorio remoto. Compartir entradas y mostrar gráficos entre dos sesiones de escritorio remoto ofrece a una persona de soporte técnico la capacidad de diagnosticar y resolver problemas de forma remota.

</dd> <dt>

<span id="Network_load_balancing"></span><span id="network_load_balancing"></span><span id="NETWORK_LOAD_BALANCING"></span>Equilibrio de carga de red
</dt> <dd>

RDP aprovecha el equilibrio de carga de red (NLB), si está disponible.

</dd> </dl>

Además, RDP contiene las siguientes características:

-   Compatibilidad con color de 24 bits.
-   Rendimiento mejorado en conexiones de acceso telefónico de baja velocidad a través de un ancho de banda reducido.
-   Autenticación mediante tarjeta inteligente a través de Servicios de Escritorio remoto.
-   Enlace de teclado. La capacidad de dirigir combinaciones especiales de teclas de Windows, en modo de pantalla completa, al equipo local o a un equipo remoto.
-   Redirección de sonido, unidad, puerto e impresora de red. Los sonidos que se producen en el equipo remoto pueden escucharse en el equipo cliente que ejecuta el cliente RDC y las unidades de cliente locales estarán visibles para la sesión de escritorio remoto.

 

 