---
title: Usar Teredo con la aplicación auxiliar de IP
description: Una aplicación emplea la API auxiliar de protocolo de Internet (auxiliar de IP) para recopilar y proporcionar información importante relacionada con la configuración de red del equipo local.
ms.assetid: 67dbe639-aff5-4628-9471-63f50504962d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e5936ce9987262fe24cfd6cf718a426b6123b89
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792508"
---
# <a name="using-teredo-with-ip-helper"></a>Usar Teredo con la aplicación auxiliar de IP

Una aplicación emplea la API del ayudante para el [Protocolo de Internet](/windows/desktop/IpHlp/about-ip-helper) (auxiliar de IP) para recopilar y proporcionar información importante relacionada con la configuración de red del equipo local. Cuando se trabaja en la plataforma de Windows Vista, esta información incluye el puerto UDP dinámico asignado a la interfaz Teredo y los cambios que se pueden producir en el puerto designado.

La API auxiliar de IP utiliza las siguientes funciones para facilitar el uso de la interfaz Teredo:

-   [**GetTeredoPort**](/windows/desktop/api/netioapi/nf-netioapi-getteredoport)
-   [**NotifyTeredoPortChange**](/windows/desktop/api/netioapi/nf-netioapi-notifyteredoportchange)
-   [**NotifyStableUnicastIpAddressTable**](/windows/desktop/api/netioapi/nf-netioapi-notifystableunicastipaddresstable)

 

 