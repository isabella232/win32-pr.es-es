---
description: Acerca de la arquitectura ACM
ms.assetid: 4a5c0085-0e7b-424d-9205-5ec39518a088
title: Acerca de la arquitectura ACM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f037a1823f7045ccaf1dc573c6d213beeebe0a63
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279005"
---
# <a name="about-the-acm-architecture"></a>Acerca de la arquitectura ACM

El módulo de configuración automática (ACM) es el nuevo componente de configuración inalámbrica para Windows Vista. En su lugar, Windows XP con Service Pack 3 (SP3) y la API de LAN inalámbrica para Windows XP con Service Pack 2 (SP2) usan el servicio de configuración inalámbrica rápida (WZC).

ACM examina las redes periódicamente y usa un proceso iterativo para seleccionar y conectarse a la red más preferida en el intervalo, si esa red tiene una interfaz habilitada para la conexión automática. ACM también guarda y recupera perfiles de red, que contienen la configuración de ACM, el módulo específico de medios (MSM), la seguridad y la configuración de proveedor de hardware independiente (IHV). Estos perfiles de red son para la configuración automática.

La configuración automática es compatible con los perfiles de red y la configuración global y por interfaz. La configuración global y los perfiles de red se configuran si el equipo se ha unido a un dominio con un objeto de directiva de grupo (GPO) en el nivel de dominio o en el nivel de unidad organizativa (OU) de la jerarquía de Active Directory (AD). Estos perfiles y la configuración de directiva de grupo son de solo lectura, se aplican a cada interfaz 802,11 en el sistema y siempre tienen prioridad sobre la configuración por interfaz y los perfiles de red y la configuración por usuario. Los perfiles de directiva de grupo se colocan en la parte superior de la lista de perfiles de red preferidos en cada interfaz de red 802,11.

La arquitectura ACM es extensible. Los IHV pueden implementar la funcionalidad inalámbrica de propiedad sin modificar el marco 802,11 nativo proporcionado. Las estructuras y funciones de control de IHV expuestas habilitan esta extensibilidad.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de WiFi nativo](about-native-wifi.md)
</dt> </dl>

 

 



