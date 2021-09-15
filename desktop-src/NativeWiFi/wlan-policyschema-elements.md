---
description: Un perfil de directiva DE LAN inalámbrica Wi-Fi (WLAN) nativo se compone de los siguientes elementos de esquema.
ms.assetid: e3f45b02-6aea-4df3-938e-c13e7c52ca04
title: WLAN_policy de esquema
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8346aab6aba209933b20790cf3747d5c0944f972
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127473700"
---
# <a name="wlan_policy-schema-elements"></a>Elementos de esquema de directiva WLAN \_

Un perfil de directiva DE LAN inalámbrica Wi-Fi (WLAN) nativo se compone de los siguientes elementos de esquema. Todos los elementos con nombre están en el espacio de nombres `https://www.microsoft.com/networking/WLAN/policy/v1` .

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

 

 



