---
description: Describe la implementación de Microsoft del protocolo bloque de mensajes del servidor (SMB).
ms.assetid: 641017fa-3721-40aa-b13c-e26c8b61ce5c
title: Introducción al protocolo SMB de Microsoft y al protocolo CIFS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09702c719d4e4c5225b35691d7e23980c90c959b7096d7995f3d60b3ef0b204b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118951154"
---
# <a name="microsoft-smb-protocol-and-cifs-protocol-overview"></a>Introducción al protocolo SMB de Microsoft y al protocolo CIFS

El protocolo bloque de mensajes del servidor (SMB) es un protocolo de uso compartido de archivos de red y, como se implementa en Microsoft Windows se conoce como protocolo SMB de Microsoft. El conjunto de paquetes de mensajes que define una versión determinada del protocolo se denomina dialecto. El protocolo common Internet File System (CIFS) es un dialecto de SMB. SMB y CIFS también están disponibles en VMS, varias versiones de Unix y otros sistemas operativos.

La referencia técnica a CIFS está disponible en Microsoft Corporation protocolo de acceso a archivos de [Common Internet File System (CIFS).](/openspecs/windows_protocols/ms-cifs/d416ff7c-c536-406e-a951-4f04b2fd1d2b)

Aunque su propósito principal es el uso compartido de archivos, la funcionalidad adicional del Protocolo SMB de Microsoft incluye lo siguiente:

-   [Negociación de dialectos](microsoft-smb-protocol-dialects.md)
-   Determinar otros servidores del Protocolo SMB de Microsoft en la red o examinar la red
-   Impresión a través de una red
-   [Autenticación de acceso a archivos, directorios y recurso compartido](microsoft-smb-protocol-authentication.md)
-   Bloqueo de archivos y registros
-   Notificación de cambio de archivos y directorios
-   Control extendido de atributos de archivo
-   Compatibilidad con Unicode
-   [Bloqueos oportunistas](opportunistic-locks.md)

En el modelo de red OSI, el protocolo SMB de Microsoft se usa con mayor frecuencia como capa de aplicación o protocolo de capa de presentación, y se basa en protocolos de nivel inferior para el transporte. El protocolo de capa de transporte con el que se suele usar el Protocolo SMB de Microsoft es NetBIOS sobre TCP/IP[(NBT).](/previous-versions//bb870909(v=vs.85)) Sin embargo, el Protocolo SMB de Microsoft también se puede usar sin un protocolo de transporte independiente; la combinación del Protocolo SMB de Microsoft/NBT se suele usar para la compatibilidad con versiones anteriores.

El Protocolo SMB de Microsoft es una implementación cliente-servidor y consta de un conjunto de paquetes de datos, cada uno de los que contiene una solicitud enviada por el cliente o una respuesta enviada por el servidor. Estos paquetes se pueden clasificar ampliamente de la siguiente manera:

-   Paquetes de control de sesión Establece e interrumpe una conexión a los recursos de servidor compartido.
-   Paquetes de acceso a archivos Accede y manipula archivos y directorios en el servidor remoto.
-   Paquetes de mensajes generales Envía datos para imprimir colas, mailslots y canalizaciones con nombre, y proporciona datos sobre el estado de las colas de impresión.

Algunos paquetes de mensajes se pueden agrupar y enviar en una transmisión para reducir la latencia de respuesta y aumentar el ancho de banda de red. Esto se denomina "procesamiento por lotes". En [la sección Escenario de paquetes Exchange](microsoft-smb-protocol-packet-exchange-scenario.md) SMB de Microsoft se describe un ejemplo de una sesión del protocolo SMB de Microsoft que usa el procesamiento por lotes de paquetes.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                                             | Descripción                                                                                                                                                                                                                                                                 |
|-------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Dialectos del protocolo SMB de Microsoft](microsoft-smb-protocol-dialects.md)<br/>                                 | Para establecer una conexión entre un cliente y un servidor mediante el Protocolo SMB de Microsoft, primero debe determinar el dialecto con el nivel más alto de funcionalidad que admiten el cliente y el servidor.<br/>                                                      |
| [Autenticación de protocolo SMB de Microsoft](microsoft-smb-protocol-authentication.md)<br/>                     | El modelo de seguridad usado en el protocolo SMB de Microsoft es idéntico al que usan otras variantes de SMB y consta de dos niveles de usuario de seguridad y recurso compartido. Un recurso compartido es un archivo, directorio o impresora al que pueden acceder los clientes del Protocolo SMB de Microsoft.<br/> |
| [Escenario de paquetes de protocolo SMB Exchange Microsoft](microsoft-smb-protocol-packet-exchange-scenario.md)<br/> | Ejemplo de intercambio de paquetes del Protocolo SMB de Microsoft entre un cliente y un servidor.<br/>                                                                                                                                                                               |



 

 

