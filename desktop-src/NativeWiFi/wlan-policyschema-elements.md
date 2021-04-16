---
description: Un perfil de directiva de LAN inalámbrica WIFI (WLAN) nativo se compone de los siguientes elementos de esquema.
ms.assetid: e3f45b02-6aea-4df3-938e-c13e7c52ca04
title: WLAN_policy elementos de esquema
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8346aab6aba209933b20790cf3747d5c0944f972
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541043"
---
# <a name="wlan_policy-schema-elements"></a>Elementos de esquema de directiva de WLAN \_

Un perfil de directiva de LAN inalámbrica WIFI (WLAN) nativo se compone de los siguientes elementos de esquema. Todos los elementos con nombre se encuentran en el espacio de nombres `https://www.microsoft.com/networking/WLAN/policy/v1` .

En la lista siguiente se muestran los elementos definidos en el orden en que los elementos aparecen en un perfil. Se aplica el orden de los elementos. No todos los elementos están en cada perfil, ya que algunos elementos son opcionales.

En esta lista no se muestran todos los elementos posibles que pueden aparecer en un perfil, ya que los elementos se pueden agregar en **xs: cualquier** punto de inserción.

-   [**WLANPolicy**](wlan-policyschema-wlanpolicy-element.md)
    -   [**nombre (WLANPolicy)**](wlan-policyschema-name-wlanpolicy-element.md)
    -   [**Descripción (WLANPolicy)**](wlan-policyschema-description-wlanpolicy-element.md)
    -   [**Indicadores_globales (WLANPolicy)**](wlan-policyschema-globalflags-wlanpolicy-element.md)
        -   [**enableAutoConfig (Indicadores_globales)**](wlan-policyschema-enableautoconfig-globalflags-element.md)
        -   [**showDeniedNetwork (Indicadores_globales)**](wlan-policyschema-showdeniednetwork-globalflags-element.md)
        -   [**allowEveryoneToCreateAllUserProfiles (Indicadores_globales)**](wlan-policyschema-alloweveryonetocreatealluserprofiles-globalflags-element.md)
    -   [**networkFilter (WLANPolicy)**](wlan-policyschema-networkfilter-wlanpolicy-element.md)
        -   [**Permitidos (networkFilter)**](wlan-policyschema-allowlist-networkfilter-element.md)
            -   [**red (permitidos)**](wlan-policyschema-network-allowlist-element.md)
                -   [**networkName (networkItemType)**](wlan-policyschema-networkname-networkitemtype-element.md)
                -   [**networkType (networkItemType)**](wlan-policyschema-networktype-networkitemtype-element.md)
        -   [**listas de bloqueo (networkFilter)**](wlan-policyschema-blocklist-networkfilter-element.md)
            -   [**red (bloqueo de listas)**](wlan-policyschema-network-blocklist-element.md)
                -   [**networkName (networkItemType)**](wlan-policyschema-networkname-networkitemtype-element.md)
                -   [**networkType (networkItemType)**](wlan-policyschema-networktype-networkitemtype-element.md)
        -   [**denyAllIBSS (networkFilter)**](wlan-policyschema-denyallibss-networkfilter-element.md)
        -   [**denyAllESS (networkFilter)**](wlan-policyschema-denyalless-networkfilter-element.md)
    -   [**profileList (WLANPolicy)**](wlan-policyschema-profilelist-wlanpolicy-element.md)

 

 



