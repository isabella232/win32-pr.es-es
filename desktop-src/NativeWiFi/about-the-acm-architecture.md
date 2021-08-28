---
description: Acerca de la arquitectura de ACM
ms.assetid: 4a5c0085-0e7b-424d-9205-5ec39518a088
title: Acerca de la arquitectura de ACM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d75b6b365970c34174facd035ddf38c625e3e4fac72f011e612998c46e9bee3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119065185"
---
# <a name="about-the-acm-architecture"></a>Acerca de la arquitectura de ACM

El módulo de configuración automática (ACM) es el nuevo componente de configuración inalámbrica para Windows Vista. Windows XP con Service Pack 3 (SP3) y la API de LAN inalámbrica para Windows XP con Service Pack 2 (SP2) usa el servicio Configuración inalámbrica cero (WZC) en su lugar.

El ACM examina las redes periódicamente y usa un proceso iterativo para seleccionar y conectarse a la red más preferida del intervalo, si esa red tiene una interfaz habilitada para la conexión automática. El ACM también guarda y recupera perfiles de red, que contienen ACM, módulo específico de medios (MSM), seguridad y configuración de proveedor de hardware independiente (IHV). Estos perfiles de red son para la configuración automática.

La configuración automática admite la configuración global y por interfaz y los perfiles de red. La configuración global y los perfiles de red se configuran si la máquina se ha unido a un dominio con un objeto de directiva de grupo (GPO) en el nivel de dominio o en el nivel de unidad organizativa (OU) en la jerarquía Active Directory (AD). Estos perfiles y configuraciones de directiva de grupo son de solo lectura, se aplican a cada interfaz 802.11 del sistema y siempre tienen prioridad sobre la configuración por interfaz y por usuario y los perfiles de red. Los perfiles de directiva de grupo se colocan en la parte superior de la lista de perfiles de red preferidos en cada interfaz de red 802.11.

La arquitectura de ACM es extensible. Los IHV pueden implementar funcionalidad inalámbrica propia sin modificar el marco nativo 802.11 proporcionado. Las estructuras y funciones de control IHV expuestas permiten esta extensibilidad.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de Wi-Fi nativo](about-native-wifi.md)
</dt> </dl>

 

 



