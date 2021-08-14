---
title: Uso de Teredo con el asistente de IP
description: Una aplicación utiliza la API del asistente de protocolos de Internet (asistente de IP) para recopilar y proporcionar información importante sobre la configuración de red de la máquina local.
ms.assetid: 67dbe639-aff5-4628-9471-63f50504962d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e977dd585f9759a4eef93daca55e0ff95abdc98085393577afabb4ae6e5908ac
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119990806"
---
# <a name="using-teredo-with-ip-helper"></a>Uso de Teredo con el asistente de IP

Una [aplicación utiliza](/windows/desktop/IpHlp/about-ip-helper) la API del asistente de protocolos de Internet (asistente de IP) para recopilar y proporcionar información importante sobre la configuración de red de la máquina local. Al funcionar en la plataforma Windows Vista, esta información incluye el puerto UDP dinámico asignado a la interfaz Teredo y los cambios que pueden producirse en el puerto designado.

La API del asistente de IP utiliza las siguientes funciones para facilitar el uso de la interfaz Teredo:

-   [**GetTeredoPort**](/windows/desktop/api/netioapi/nf-netioapi-getteredoport)
-   [**NotifyTeredoPortChange**](/windows/desktop/api/netioapi/nf-netioapi-notifyteredoportchange)
-   [**NotifyStableUnicastIpAddressTable**](/windows/desktop/api/netioapi/nf-netioapi-notifystableunicastipaddresstable)

 

 