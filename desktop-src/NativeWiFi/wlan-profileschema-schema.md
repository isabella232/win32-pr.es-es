---
description: Define un perfil de WLAN usado por el servicio de configuración automática de WiFi nativo.
ms.assetid: 8312d213-1d01-4bd0-a8d9-65ca23560888
title: Esquema de WLAN_profile
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d484215ca53ddcd97dbef4adf4aac17cd8457b3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154107"
---
# <a name="wlan_profile-schema"></a>Esquema de Perfil de WLAN \_

El esquema de Perfil de WLAN \_ define un perfil de WLAN que usa el servicio de configuración automática de WiFi nativo.

El servicio de configuración automática acepta perfiles inalámbricos del agente de directiva de grupo, la interfaz de scripting (**netsh**), la interfaz de usuario o la interfaz de configuración Flash de USB.

Un perfil recibido de uno de estos sistemas se asigna al esquema de \_ Perfil de WLAN y se almacena en el almacén de perfiles. Los perfiles se pueden exportar desde el almacén de perfiles mediante comandos Netsh o mediante elementos de la API como [**WlanGetProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetprofile).

El elemento raíz de un perfil de WLAN es el elemento [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) . Cada perfil tendrá exactamente un elemento raíz. El elemento **WLANProfile** se encuentra en el espacio de nombres `https://www.microsoft.com/networking/WLAN/profile/v1` .

Para ver los perfiles de WLAN de ejemplo, consulte [ejemplos de perfiles inalámbricos](wireless-profile-samples.md).

-   [Elementos de esquema de Perfil de WLAN \_](wlan-profileschema-elements.md)
-   [\_Tipos simples de esquema de Perfil de WLAN](wlan-profileschema-simple-types.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Comandos Netsh para la red de área local inalámbrica (WLAN)](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc755301(v=ws.10))
</dt> </dl>

 

 
