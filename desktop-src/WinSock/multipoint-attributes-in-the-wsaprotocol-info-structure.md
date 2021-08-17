---
title: Atributos multipunto en WSAPROTOCOL_INFO
description: Entre los atributos de varios puntos de la estructura INFO de WSAPROTOCOL se incluyen \_ XP1 \_ SUPPORT \_ MULTIPOINT, XP1 MULTIPOINT CONTROL PLANE y \_ \_ \_ XP1 \_ MULTIPOINT DATA \_ \_ PLANE.
ms.assetid: f1bd5aa1-e705-4eaf-9436-fed0ea03f113
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1275b6da00258be10b071bc9b2399abaf5dd608583f3d81a0fdb16af493824ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117741109"
---
# <a name="multipoint-attributes-in-wsaprotocol_info"></a>Atributos multipunto en WSAPROTOCOL_INFO

Se definen tres parámetros de atributo en la estructura [**\_ INFO de WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) para distinguir los distintos esquemas usados en los planos de control y datos, respectivamente:

-   XP1 SUPPORT MULTIPOINT con un valor de 1 indica que esta entrada de protocolo admite comunicaciones multipunto y que los dos parámetros siguientes \_ \_ son significativos.
-   XP1 MULTIPOINT CONTROL PLANE indica si el plano de control tiene raíz \_ \_ \_ (valor = 1) o no raíz (valor = 0).
-   XP1 MULTIPOINT DATA PLANE indica si el plano de datos tiene raíz \_ \_ \_ (valor = 1) o no raíz (valor = 0).

Dos entradas info de [**WSAPROTOCOL \_**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) estarían presentes si un protocolo multipunto admite planos de datos raíz y no raíz, una entrada para cada uno.

 

 
