---
description: Define un perfil DE WLAN utilizado por el servicio AutoConfig de Wi-Fi nativo.
ms.assetid: 8312d213-1d01-4bd0-a8d9-65ca23560888
title: WLAN_profile esquema
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 91bd1a5d04bcc265f2b9ba7c0533bb0beb4e2c861f01c8b5e286d59f8b4bcfc3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118619072"
---
# <a name="wlan_profile-schema"></a>Esquema de \_ perfil WLAN

El esquema \_ del perfil DE WLAN define un perfil DE WLAN utilizado por el servicio AutoConfig de Wi-Fi nativo.

El servicio AutoConfig acepta perfiles inalámbricos del agente de directiva de grupo, la interfaz de scripting **(netsh),** la interfaz de usuario o la interfaz de configuración flash USB.

Un perfil recibido de uno de estos sistemas se asigna al esquema de perfil WLAN \_ y se almacena en el almacén de perfiles. Los perfiles se pueden exportar desde el almacén de perfiles mediante comandos netsh o mediante elementos de API como [**WlanGetProfile.**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetprofile)

El elemento raíz de un perfil WLAN es [**el elemento WLANProfile.**](wlan-profileschema-wlanprofile-element.md) Cada perfil tendrá exactamente un elemento raíz. El **elemento WLANProfile** está en el espacio de nombres `https://www.microsoft.com/networking/WLAN/profile/v1` .

Para ver los perfiles WLAN de ejemplo, consulte [Ejemplos de perfiles inalámbricos.](wireless-profile-samples.md)

-   [Elementos de esquema del perfil WLAN \_](wlan-profileschema-elements.md)
-   [Tipos simples de esquema de perfil WLAN \_](wlan-profileschema-simple-types.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Comandos Netsh para red inalámbrica de área local (wlan)](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc755301(v=ws.10))
</dt> </dl>

 

 
