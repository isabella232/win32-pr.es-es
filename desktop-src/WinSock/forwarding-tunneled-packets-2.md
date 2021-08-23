---
description: Hay una limitación en el código que recibe paquetes encapsulados (tunelados) y los desmultiplexa a una interfaz específica.
ms.assetid: 6148fca7-adf4-460d-afd6-79c43285af6c
title: Reenvío de paquetes con túnel IPv6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42138c746ea9d0ec8ea61bc3801b84a97a6bdd4c6fb6de0871e6b74447fdf28b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132438"
---
# <a name="ipv6-forwarding-tunneled-packets"></a>Reenvío de paquetes con túnel IPv6

Hay una limitación en el código que recibe paquetes encapsulados (tunelados) y los desmultiplexa a una interfaz específica. Si desea reenviar los paquetes tunelados recibidos a través de un túnel configurado, es necesario habilitar el reenvío en cualquier interfaz de 6 sobre 4, así como en la \# interfaz 2. Solo habilitar el reenvío en la \# interfaz 2 no funcionará. Normalmente, al configurar un enrutador, habilitaría el reenvío en todas las interfaces, excepto en bucles.

 

 



