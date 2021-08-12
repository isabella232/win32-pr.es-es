---
description: Un perfil de directiva de LAN inalámbrica Wi-Fi (WLAN) nativo se compone de los siguientes elementos de esquema.
ms.assetid: e3f45b02-6aea-4df3-938e-c13e7c52ca04
title: WLAN_policy de esquema
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 92bfca66e1eff2c8c180968c83b5dbb565d1d4aa27ace1ba89d1c70634d6e7b0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118619550"
---
# <a name="wlan_policy-schema-elements"></a>Elementos de esquema de directiva WLAN \_

Un perfil de directiva de LAN inalámbrica Wi-Fi (WLAN) nativo se compone de los siguientes elementos de esquema. Todos los elementos con nombre están en el espacio de nombres `https://www.microsoft.com/networking/WLAN/policy/v1` .

En la lista siguiente se muestran los elementos definidos en el orden en que los elementos aparecen en un perfil. Se aplica el orden de los elementos. No todos los elementos están en todos los perfiles, ya que algunos elementos son opcionales.

Esta lista no muestra todos los elementos posibles que pueden aparecer en un perfil, ya que los elementos se pueden agregar en **xs:any puntos de** inserción.

-   [**WLANPolicy**](wlan-policyschema-wlanpolicy-element.md)
    -   [**name (WLANPolicy)**](wlan-policyschema-name-wlanpolicy-element.md)
    -   [**description (WLANPolicy)**](wlan-policyschema-description-wlanpolicy-element.md)
    -   [**globalFlags (WLANPolicy)**](wlan-policyschema-globalflags-wlanpolicy-element.md)
        -   [**enableAutoConfig (globalFlags)**](wlan-policyschema-enableautoconfig-globalflags-element.md)
        -   [**showDeniedNetwork (globalFlags)**](wlan-policyschema-showdeniednetwork-globalflags-element.md)
        -   [**allowEveryoneToCreateAllUserProfiles (globalFlags)**](wlan-policyschema-alloweveryonetocreatealluserprofiles-globalflags-element.md)
    -   [**networkFilter (WLANPolicy)**](wlan-policyschema-networkfilter-wlanpolicy-element.md)
        -   [**allowList (networkFilter)**](wlan-policyschema-allowlist-networkfilter-element.md)
            -   [**network (allowList)**](wlan-policyschema-network-allowlist-element.md)
                -   [**networkName (networkItemType)**](wlan-policyschema-networkname-networkitemtype-element.md)
                -   [**networkType (networkItemType)**](wlan-policyschema-networktype-networkitemtype-element.md)
        -   [**blockList (networkFilter)**](wlan-policyschema-blocklist-networkfilter-element.md)
            -   [**network (blockList)**](wlan-policyschema-network-blocklist-element.md)
                -   [**networkName (networkItemType)**](wlan-policyschema-networkname-networkitemtype-element.md)
                -   [**networkType (networkItemType)**](wlan-policyschema-networktype-networkitemtype-element.md)
        -   [**denyAllIBSS (networkFilter)**](wlan-policyschema-denyallibss-networkfilter-element.md)
        -   [**denyAllESS (networkFilter)**](wlan-policyschema-denyalless-networkfilter-element.md)
    -   [**profileList (WLANPolicy)**](wlan-policyschema-profilelist-wlanpolicy-element.md)

 

 



