---
description: XP1 \_ admiten \_ \_ los parámetros de Multipoint, plano de control MULTIpoint \_ y XP1 Multipoint de XP1 \_ \_ \_ \_ en la estructura de información de Winsock WSAPROTOCOL \_ .
ms.assetid: 62f5b8b0-a404-49d1-b163-026f79a46845
title: Atributos en WSAPROTOCOL_INFO estructura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e39ea2905da3228860d4fe22f5a0f0d954ce0624
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715143"
---
# <a name="attributes-in-wsaprotocol_info-structure"></a>Atributos en la \_ estructura de información de WSAPROTOCOL

En la compatibilidad con la taxonomía descrita anteriormente, se usan tres parámetros de atributo en la estructura de [**\_ información de WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) para distinguir los esquemas utilizados en los planos de control y de datos, respectivamente:

-   XP1 \_ support \_ multipoint con un valor de 1 indica que esta entrada de protocolo admite comunicaciones multipunto y que los dos parámetros siguientes son significativos.
-   \_ \_ \_ El plano de control Multipoint de XP1 indica si el plano de control es de raíz (valor = 1) o no raíz (valor = 0).
-   \_ \_ \_ El plano de datos Multipoint de XP1 indica si el plano de datos tiene raíz (valor = 1) o no raíz (valor = 0).

Tenga en cuenta que dos entradas de [**\_ información de WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) estarán presentes si un protocolo Multipoint admitía los planos de datos raíz y no raíz, una entrada para cada uno.

La aplicación puede utilizar [**WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa) para detectar si se admiten las comunicaciones multipunto para un protocolo determinado y, si es así, cómo se admite con respecto al control y a los planos de datos, respectivamente.

 

 
