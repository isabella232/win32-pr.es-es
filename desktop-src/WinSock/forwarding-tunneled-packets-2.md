---
description: Existe una limitación en el código que recibe paquetes encapsulados (tunelizados) y los desmultiplexa en una interfaz específica.
ms.assetid: 6148fca7-adf4-460d-afd6-79c43285af6c
title: Paquetes de túnel de reenvío IPv6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f95f88a90a358317cf46516808a96f93b792dd5d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907950"
---
# <a name="ipv6-forwarding-tunneled-packets"></a>Paquetes de túnel de reenvío IPv6

Existe una limitación en el código que recibe paquetes encapsulados (tunelizados) y los desmultiplexa en una interfaz específica. Si desea reenviar los paquetes de túnel recibidos a través de un túnel configurado, es necesario habilitar el reenvío en cualquier interfaz de 6 a 4, así como en la interfaz \# 2. Simplemente habilitar el reenvío en la interfaz \# 2 no funcionará. Normalmente, al configurar un enrutador, se habilita el reenvío en todas las interfaces excepto en bucle invertido.

 

 



