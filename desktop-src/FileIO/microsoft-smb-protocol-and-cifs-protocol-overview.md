---
description: Describe la implementación de Microsoft del Protocolo de bloque de mensajes del servidor (SMB).
ms.assetid: 641017fa-3721-40aa-b13c-e26c8b61ce5c
title: Información general sobre el protocolo SMB de Microsoft y el protocolo CIFS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30326221694ce843733f6da7a6ad49c8dff336ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001105"
---
# <a name="microsoft-smb-protocol-and-cifs-protocol-overview"></a>Información general sobre el protocolo SMB de Microsoft y el protocolo CIFS

El protocolo de bloque de mensajes del servidor (SMB) es un protocolo de uso compartido de archivos de red y, tal y como se implementa en Microsoft Windows, se conoce como protocolo SMB de Microsoft. El conjunto de paquetes de mensajes que define una versión determinada del Protocolo se denomina dialecto. El protocolo de sistema de archivos de Internet común (CIFS) es un dialecto de SMB. Tanto SMB como CIFS también están disponibles en las máquinas virtuales, en varias versiones de UNIX y en otros sistemas operativos.

La referencia técnica a CIFS está disponible en Microsoft Corporation en el [Protocolo de acceso a archivos de Common Internet File System (CIFS)](/openspecs/windows_protocols/ms-cifs/d416ff7c-c536-406e-a951-4f04b2fd1d2b).

Aunque su finalidad principal es el uso compartido de archivos, la funcionalidad adicional del protocolo SMB de Microsoft incluye lo siguiente:

-   [Negociación de dialectos](microsoft-smb-protocol-dialects.md)
-   Determinar otros servidores de protocolo SMB de Microsoft en la red o la exploración de red
-   Impresión a través de una red
-   [Autenticación de acceso a archivos, directorios y recursos compartidos](microsoft-smb-protocol-authentication.md)
-   Bloqueo de archivos y registros
-   Notificación de cambio de archivo y directorio
-   Control de atributos de archivo extendidos
-   Compatibilidad con Unicode
-   [Bloqueos oportunistas](opportunistic-locks.md)

En el modelo de red OSI, el protocolo SMB de Microsoft se usa con más frecuencia como un nivel de aplicación o un protocolo de capa de presentación, y se basa en protocolos de nivel inferior para el transporte. El protocolo de nivel de transporte con el que se usa con más frecuencia el protocolo SMB de Microsoft es NetBIOS sobre TCP/IP ([NBT](/previous-versions//bb870909(v=vs.85))). Sin embargo, el protocolo SMB de Microsoft también se puede usar sin un protocolo de transporte independiente la combinación de Microsoft SMB Protocol/NBT normalmente se utiliza por motivos de compatibilidad con versiones anteriores.

El protocolo SMB de Microsoft es una implementación cliente-servidor y consta de un conjunto de paquetes de datos, cada uno de los cuales contiene una solicitud enviada por el cliente o una respuesta enviada por el servidor. Estos paquetes se pueden clasificar ampliamente de la manera siguiente:

-   Los paquetes de control de sesión establecen y interrumpen una conexión a los recursos de servidor compartidos.
-   Los paquetes de acceso a archivos tienen acceso a archivos y directorios del servidor remoto y los manipulan.
-   Los paquetes de mensajes generales envían datos a colas de impresión, procesadores de mensajes y canalizaciones con nombre, y proporcionan datos sobre el estado de las colas de impresión.

Algunos paquetes de mensajes se pueden agrupar y enviar en una transmisión para reducir la latencia de respuesta y aumentar el ancho de banda de red. Esto se denomina "procesamiento por lotes". La sección del [escenario de intercambio de paquetes del protocolo SMB de Microsoft](microsoft-smb-protocol-packet-exchange-scenario.md) describe un ejemplo de una sesión del protocolo SMB de Microsoft que usa el procesamiento por lotes de paquetes.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                                             | Descripción                                                                                                                                                                                                                                                                 |
|-------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Dialectos del protocolo SMB de Microsoft](microsoft-smb-protocol-dialects.md)<br/>                                 | Para establecer una conexión entre un cliente y un servidor mediante el protocolo SMB de Microsoft, primero debe determinar el dialecto con el nivel más alto de funcionalidad que admiten tanto el cliente como el servidor.<br/>                                                      |
| [Autenticación de protocolo SMB de Microsoft](microsoft-smb-protocol-authentication.md)<br/>                     | El modelo de seguridad que se usa en el protocolo SMB de Microsoft es idéntico al utilizado por otras variantes de SMB, y consta de dos niveles de usuario y recurso compartido de seguridad. Un recurso compartido es un archivo, un directorio o una impresora a los que pueden tener acceso los clientes del protocolo SMB de Microsoft.<br/> |
| [Escenario de intercambio de paquetes del protocolo SMB de Microsoft](microsoft-smb-protocol-packet-exchange-scenario.md)<br/> | Ejemplo de intercambio de paquetes del protocolo SMB de Microsoft entre un cliente y un servidor.<br/>                                                                                                                                                                               |



 

 

