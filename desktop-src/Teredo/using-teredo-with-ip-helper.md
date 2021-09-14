---
title: Uso de Teredo con el asistente de IP
description: Una aplicación utiliza la API del asistente de protocolos de Internet (asistente de IP) para recopilar y proporcionar información importante sobre la configuración de red de la máquina local.
ms.assetid: 67dbe639-aff5-4628-9471-63f50504962d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e5936ce9987262fe24cfd6cf718a426b6123b89
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127168821"
---
# <a name="using-teredo-with-ip-helper"></a>Uso de Teredo con el asistente de IP

Una [aplicación utiliza](/windows/desktop/IpHlp/about-ip-helper) la API del asistente de protocolos de Internet (asistente de IP) para recopilar y proporcionar información importante sobre la configuración de red de la máquina local. Al funcionar en la plataforma Windows Vista, esta información incluye el puerto UDP dinámico asignado a la interfaz teredo y los cambios que pueden producirse en el puerto designado.

La API del asistente de IP utiliza las siguientes funciones para facilitar el uso de la interfaz de Teredo:

-   [**GetTeredoPort**](/windows/desktop/api/netioapi/nf-netioapi-getteredoport)
-   [**NotifyTeredoPortChange**](/windows/desktop/api/netioapi/nf-netioapi-notifyteredoportchange)
-   [**NotifyStableUnicastIpAddressTable**](/windows/desktop/api/netioapi/nf-netioapi-notifystableunicastipaddresstable)

 

 