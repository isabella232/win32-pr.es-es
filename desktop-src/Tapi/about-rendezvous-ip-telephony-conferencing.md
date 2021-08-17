---
description: Los controles TAPI 3 Rendezvous proporcionan mecanismos para anunciar y detectar conferencias IP multimedia multipartes. A continuación se describe un conjunto de componentes e interfaces del Modelo de objetos componentes (COM) para implementar la conferencia.
ms.assetid: 0ca2edac-b507-497e-9e63-78a10466e2eb
title: Acerca de la conferencia de telefonía IP de Rendezvous
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 225f7842e0f7efdb97dcadc3d59adc8fa7e5adf0f73cd824b335500a5aa6c11d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117949300"
---
# <a name="about-rendezvous-ip-telephony-conferencing"></a>Acerca de la conferencia de telefonía IP de Rendezvous

\[Los controles e interfaces de conferencia de telefonía IP de Encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. La API de cliente RTC proporciona una funcionalidad similar.\]

Los controles TAPI 3 Rendezvous proporcionan mecanismos para anunciar y detectar conferencias IP multimedia multipartes. A continuación se describe un conjunto de componentes e interfaces del Modelo de objetos componentes (COM) para implementar la conferencia.

COM es el modelo de codificación básico para TAPI 3 y se supone que está familiarizado con él a lo largo de este documento. Para obtener información sobre COM, busque Platform Software Development Kit (SDK).

## <a name="features"></a>Características

-   Proporciona la abstracción de un directorio de conferencias para manipular anuncios de conferencias multimedia
-   Proporciona seguridad a través de la autenticación, el cifrado y una capa de control de acceso (ACL) por anuncio.
-   Proporciona un esquema común para un anuncio de conferencia, habilitando búsquedas por valores de atributo
-   Permite extensiones a través de un atributo mantenido por el proveedor (blob de conferencia) en el esquema
-   Proporciona un contenedor COM para la API de asignación de direcciones de multidifusión (MADCAP).

## <a name="architecture"></a>Arquitectura

Las descripciones y el diagrama siguientes ilustran aspectos clave de la arquitectura del sistema.

-   El cliente puede manipular conferencias almacenadas en un directorio dinámico ILS o un servidor NTDS mediante controles Rendezvous. El Protocolo ligero de acceso a directorios (LDAP) se usa para comunicarse con un servidor ILS.
-   Los controles Rendezvous proporcionan interfaces COM duales para scripting y programación.
-   Un servidor de Protocolo de anuncio de sesión (SAP) con acceso directo a Internet escucha los anuncios de conferencias en Internet y rellena los servidores dinámicos de ILS con la información de la conferencia. Del mismo modo, también anuncia las conferencias creadas localmente cuyo ámbito incluye Internet. (El servidor SAP no está planeado para Microsoft Windows 2000).

![arquitectura del sistema de encuentro](images/rend1.png)

 

 



