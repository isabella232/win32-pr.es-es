---
description: XP1 ADMITE los parámetros de atributo MULTIPOINT, XP1 MULTIPOINT CONTROL PLANE y XP1 MULTIPOINT DATA PLANE en la estructura INFO \_ \_ de \_ \_ \_ \_ \_ \_ Winsock WSAPROTOCOL. \_
ms.assetid: 62f5b8b0-a404-49d1-b163-026f79a46845
title: Atributos en WSAPROTOCOL_INFO estructura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb502c0f29f09604f80e5437774f2b481cef238aaf34f566e78886127dae1027
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119898555"
---
# <a name="attributes-in-wsaprotocol_info-structure"></a>Atributos de la estructura INFO de WSAPROTOCOL \_

Para admitir la taxonomía descrita anteriormente, se usan tres parámetros de atributo en la estructura INFO de [**WSAPROTOCOL \_**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) para distinguir los esquemas usados en los planos de control y de datos, respectivamente:

-   XP1 SUPPORT MULTIPOINT con un valor de 1 indica que esta entrada de protocolo admite comunicaciones multipunto y que los dos parámetros siguientes \_ \_ son significativos.
-   XP1 MULTIPOINT CONTROL PLANE indica si el plano de control tiene raíz \_ \_ \_ (valor = 1) o no raíz (valor = 0).
-   XP1 MULTIPOINT DATA PLANE indica si el plano de datos tiene raíz \_ \_ \_ (valor = 1) o no raíz (valor = 0).

Tenga en cuenta que dos entradas info de [**WSAPROTOCOL \_**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) estarían presentes si un protocolo multipunto admite planos de datos raíz y no raíz, una entrada para cada uno.

La aplicación puede usar [**WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa) para detectar si se admiten comunicaciones multipunto para un protocolo determinado y, si es así, cómo se admite con respecto al control y los planos de datos, respectivamente.

 

 
