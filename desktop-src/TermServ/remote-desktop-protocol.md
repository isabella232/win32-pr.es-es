---
title: Protocolo de escritorio remoto
description: El protocolo Escritorio remoto de Microsoft (RDP) proporciona funciones de pantalla y entrada remotas a través de conexiones de red para Windows basadas en aplicaciones que se ejecutan en un servidor.
ms.assetid: 442c3c7f-d04b-4dcd-945d-f6e0168c59d5
ms.tgt_platform: multiple
keywords:
- Protocolo de escritorio remoto (RDP) Servicios de Escritorio remoto
- RDP (consulte Protocolo de escritorio remoto)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7895163a5ee92a6cc756dca9b097db8498d02e70
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127374682"
---
# <a name="remote-desktop-protocol"></a>Protocolo de escritorio remoto

El protocolo Escritorio remoto de Microsoft (RDP) proporciona funciones de pantalla y entrada remotas a través de conexiones de red para Windows basadas en aplicaciones que se ejecutan en un servidor. RDP está diseñado para admitir diferentes tipos de topologías de red y varios protocolos LAN.

> [!Note]  
> Este tema es para desarrolladores de software. Si busca información de usuario para la Escritorio remoto, consulte [Windows Support (Compatibilidad con Windows usuario).](https://windows.microsoft.com/windows/support#1TC=windows-8) Si busca información profesional de TI para Escritorio remoto, consulte Servicios de Escritorio remoto [en TechNet](/windows/deployment/deploy-whats-new).

 

## <a name="basic-architecture"></a>Arquitectura básica

RDP se basa en la familia de protocolos ITU T.120 y en una extensión de . RDP es un protocolo compatible con varios canales que permite canales virtuales independientes para transportar datos de presentación y comunicación del dispositivo desde el servidor, así como datos cifrados del mouse y el teclado del cliente. RDP proporciona una base extensible y admite hasta 64 000 canales independientes para la transmisión de datos y aprovisiona para la transmisión multipunto.

En el servidor, RDP usa su propio controlador de vídeo para representar la salida de la presentación mediante la construcción de la información de representación en paquetes de red mediante el protocolo RDP y su envío a través de la red al cliente. En el cliente, RDP recibe datos de representación e interpreta los paquetes en las correspondientes llamadas API de la interfaz de dispositivo gráfico (GDI) de Microsoft Windows. Para la ruta de acceso de entrada, los eventos de mouse y teclado del cliente se redirigen desde el cliente al servidor. En el servidor, RDP usa su propio controlador de teclado y mouse para recibir estos eventos de teclado y mouse.

En una sesión Escritorio remoto, todas las variables de entorno (por ejemplo, las variables que determinan la profundidad de color y la habilitación y deshabilitación del papel tapiz) se determinan mediante la configuración RCP-Tcp conexión. Esto se aplica a todas las funciones [](remote-desktop-web-connection-reference.md) y métodos que establecen variables de entorno en la referencia de Conexión web a Escritorio remoto y la Servicios de Escritorio remoto [del proveedor WMI .](terminal-services-wmi-provider-reference.md)

## <a name="features"></a>Características

Microsoft RDP incluye las siguientes características y funcionalidades:

<dl> <dt>

<span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>Cifrado
</dt> <dd>

RDP usa el cifrado RC4 de RSA Security, un cifrado de flujo diseñado para cifrar eficazmente pequeñas cantidades de datos. RC4 está diseñado para proteger las comunicaciones a través de redes. Los administradores pueden optar por cifrar los datos mediante una clave de 56 o 128 bits.

</dd> <dt>

<span id="Bandwidth_reduction_features"></span><span id="bandwidth_reduction_features"></span><span id="BANDWIDTH_REDUCTION_FEATURES"></span>Características de reducción de ancho de banda
</dt> <dd>

RDP admite varios mecanismos para reducir la cantidad de datos transmitidos a través de una conexión de red. Los mecanismos incluyen la compresión de datos, el almacenamiento en caché persistente de mapas de bits y el almacenamiento en caché de glifos y fragmentos en ram. La caché de mapas de bits persistente puede proporcionar una mejora sustancial en el rendimiento en conexiones de ancho de banda bajo, especialmente cuando se ejecutan aplicaciones que hacen un uso amplio de mapas de bits grandes.

</dd> <dt>

<span id="Roaming_disconnect"></span><span id="roaming_disconnect"></span><span id="ROAMING_DISCONNECT"></span>Desconexión de itinerancia
</dt> <dd>

Un usuario puede desconectarse manualmente de una sesión de Escritorio remoto sin cerrar sesión. El usuario se vuelve a conectar automáticamente a su sesión desconectada cuando vuelve a iniciar sesión en el sistema, ya sea desde el mismo dispositivo o desde otro dispositivo. Cuando una red o un error de cliente finalizan inesperadamente la sesión de un usuario, el usuario se desconecta pero no se cierra.

</dd> <dt>

<span id="Clipboard_mapping"></span><span id="clipboard_mapping"></span><span id="CLIPBOARD_MAPPING"></span>Asignación del Portapapeles
</dt> <dd>

Los usuarios pueden eliminar, copiar y pegar texto y gráficos entre las aplicaciones que se ejecutan en el equipo local y las que se ejecutan en una sesión de Escritorio remoto, y entre sesiones.

</dd> <dt>

<span id="Print_redirection"></span><span id="print_redirection"></span><span id="PRINT_REDIRECTION"></span>Redirección de impresión
</dt> <dd>

Las aplicaciones que se ejecutan en una sesión de Escritorio remoto se pueden imprimir en una impresora conectada al dispositivo cliente.

</dd> <dt>

<span id="Virtual_channels"></span><span id="virtual_channels"></span><span id="VIRTUAL_CHANNELS"></span>Canales virtuales
</dt> <dd>

Mediante el uso de la arquitectura de canal virtual RDP, se pueden aumentar las aplicaciones existentes y se pueden desarrollar nuevas aplicaciones para agregar características que requieren comunicaciones entre el dispositivo cliente y una aplicación que se ejecuta en una sesión de Escritorio remoto.

</dd> <dt>

<span id="Remote_control"></span><span id="remote_control"></span><span id="REMOTE_CONTROL"></span>Teledirigido
</dt> <dd>

El personal de soporte técnico del equipo puede ver y controlar una sesión de Escritorio remoto. Compartir los gráficos de entrada y visualización entre dos sesiones de Escritorio remoto ofrece a una persona de soporte técnico la capacidad de diagnosticar y resolver problemas de forma remota.

</dd> <dt>

<span id="Network_load_balancing"></span><span id="network_load_balancing"></span><span id="NETWORK_LOAD_BALANCING"></span>Equilibrio de carga de red
</dt> <dd>

RDP aprovecha el equilibrio de carga de red (NLB), siempre que esté disponible.

</dd> </dl>

Además, RDP contiene las siguientes características:

-   Compatibilidad con el color de 24 bits.
-   Rendimiento mejorado en conexiones de acceso telefónico de baja velocidad a través de un ancho de banda reducido.
-   Autenticación con tarjeta inteligente mediante Servicios de Escritorio remoto.
-   Enlace de teclado. La capacidad de dirigir combinaciones Windows claves especiales, en modo de pantalla completa, al equipo local o a un equipo remoto.
-   Redireccionamiento de sonido, unidad, puerto e impresora de red. Los sonidos que se producen en el equipo remoto se pueden escuchar en el equipo cliente que ejecuta el cliente RDC y las unidades de cliente local serán visibles para la sesión de Escritorio remoto.

 

 