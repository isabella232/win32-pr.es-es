---
title: Atributos multipunto en WSAPROTOCOL_INFO
description: Los atributos multipunto de la \_ estructura WSAPROTOCOL info incluyen XP1 support Multipoint \_ \_ , XP1 \_ Multipoint \_ control \_ Plane y XP1 \_ Multipoint \_ Data \_ Plane.
ms.assetid: f1bd5aa1-e705-4eaf-9436-fed0ea03f113
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: baedcd07f53db462eb090217b53d93a1a4aa8c34
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809728"
---
# <a name="multipoint-attributes-in-wsaprotocol_info"></a>Atributos multipunto en WSAPROTOCOL_INFO

Se definen tres parámetros de atributo en la estructura de [**\_ información de WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) para distinguir los distintos esquemas que se usan en los planos de control y de datos, respectivamente:

-   XP1 \_ support \_ multipoint con un valor de 1 indica que esta entrada de protocolo admite comunicaciones multipunto y que los dos parámetros siguientes son significativos.
-   \_ \_ \_ El plano de control Multipoint de XP1 indica si el plano de control es de raíz (valor = 1) o no raíz (valor = 0).
-   \_ \_ \_ El plano de datos Multipoint de XP1 indica si el plano de datos tiene raíz (valor = 1) o no raíz (valor = 0).

Dos entradas de [**\_ información de WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) estarán presentes si un protocolo Multipoint admitía los planos de datos raíz y no raíz, una entrada para cada uno.

 

 
