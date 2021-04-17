---
description: Los controles TAPI 3 Rendezvous proporcionan mecanismos para anunciar y detectar conferencias IP de multimedia multiparte. A continuación se describe un conjunto de componentes de modelo de objetos componentes (COM) e interfaces para implementar las conferencias.
ms.assetid: 0ca2edac-b507-497e-9e63-78a10466e2eb
title: Acerca de las conferencias de telefonía IP de Rendezvous
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4bd06fb848088a42e34bd7b176358a7507e3d2f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104566906"
---
# <a name="about-rendezvous-ip-telephony-conferencing"></a>Acerca de las conferencias de telefonía IP de Rendezvous

\[ Las interfaces y controles de conferencias de telefonía IP de encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y las versiones posteriores del sistema operativo. La API de cliente de RTC proporciona una funcionalidad similar.\]

Los controles TAPI 3 Rendezvous proporcionan mecanismos para anunciar y detectar conferencias IP de multimedia multiparte. A continuación se describe un conjunto de componentes de modelo de objetos componentes (COM) e interfaces para implementar las conferencias.

COM es el modelo de codificación básica para TAPI 3 y está familiarizado con él en este documento. Para obtener información sobre COM, busque el kit de desarrollo de software (SDK) de la plataforma.

## <a name="features"></a>Características

-   Proporciona la abstracción de un directorio de conferencias para manipular anuncios de conferencias multimedia
-   Proporciona seguridad a través de la autenticación, el cifrado y una capa de control de acceso (ACL) por anuncio.
-   Proporciona un esquema común para un anuncio de conferencia, habilitando búsquedas por valores de atributo
-   Permite extensiones a través de un atributo mantenido por el proveedor (BLOB de conferencia) en el esquema.
-   Proporciona un contenedor COM para la API de asignación de direcciones de multidifusión (MADCAP)

## <a name="architecture"></a>Architecture

En las descripciones y diagramas siguientes se muestran los aspectos clave de la arquitectura del sistema.

-   El cliente puede manipular las conferencias almacenadas en un directorio dinámico ILS o en un servidor NTDS mediante controles Rendezvous. El Protocolo ligero de acceso a directorios (LDAP) se usa para comunicarse con un servidor ILS.
-   Los controles Rendezvous proporcionan interfaces COM duales para el scripting y la programación.
-   Un servidor de protocolo de anuncio de sesión (SAP) con acceso directo a Internet escucha los anuncios de conferencias en Internet y rellena los servidores ILS dinámicos con la información de la Conferencia. De forma similar, también anuncia las conferencias creadas localmente cuyo ámbito incluye Internet. (El servidor SAP no está planeado para Microsoft Windows 2000).

![arquitectura del sistema Rendezvous](images/rend1.png)

 

 



