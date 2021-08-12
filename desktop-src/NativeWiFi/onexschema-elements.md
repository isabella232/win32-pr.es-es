---
description: Un perfil 802.1X contiene los siguientes elementos de esquema.
ms.assetid: be3f1986-d0c2-47f6-b4dd-8defb89bd03a
title: Elementos de esquema de OneX
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c20e6bf2b15fa53e5567d02bf3a88135b66fe7de80a171310249ddb941aedb16
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118619990"
---
# <a name="onex-schema-elements"></a>Elementos de esquema de OneX

Un perfil 802.1X contiene los siguientes elementos de esquema. Todos los elementos de esquema de OneX se aplican a perfiles cableados e inalámbricos. La mayoría de los elementos con nombre están en el espacio de nombres `https://www.microsoft.com/networking/OneX/v1` , [**excepto EAPConfig (OneX),**](onexschema-eapconfig-onex-element.md) que se encuentra en el espacio de nombres `https://www.microsoft.com/provisioning/EapHostConfig` .

En la lista siguiente se muestran los elementos definidos en el orden en que los elementos aparecen en un perfil. Se aplica el orden de los elementos. No todos los elementos están en todos los perfiles, ya que algunos elementos son opcionales.

Esta lista no muestra todos los elementos posibles que pueden aparecer en un perfil, ya que los elementos se pueden agregar en **xs:any puntos de** inserción.

-   [**Onex**](onexschema-onex-element.md)
    -   [**cacheUserData (OneX)**](onexschema-cacheuserdata-onex-element.md)
    -   [**heldPeriod (OneX)**](onexschema-heldperiod-onex-element.md)
    -   [**authPeriod (OneX)**](onexschema-authperiod-onex-element.md)
    -   [**startPeriod (OneX)**](onexschema-startperiod-onex-element.md)
    -   [**maxStart (OneX)**](onexschema-maxstart-onex-element.md)
    -   [**maxAuthFailures (OneX)**](onexschema-maxauthfailures-onex-element.md)
    -   [**supplicantMode (OneX)**](onexschema-supplicantmode-onex-element.md)
    -   [**authMode (OneX)**](onexschema-authmode-onex-element.md)
    -   [**singleSignOn (OneX)**](onexschema-singlesignon-onex-element.md)
        -   [**type (singleSignOn)**](onexschema-type-singlesignon-element.md)
        -   [**maxDelay (singleSignOn)**](onexschema-maxdelay-singlesignon-element.md)
        -   [**userBasedVirtualLan (singleSignOn)**](onexschema-userbasedvirtuallan-singlesignon-element.md)
    -   [**EAPConfig (OneX)**](onexschema-eapconfig-onex-element.md)

 

 



