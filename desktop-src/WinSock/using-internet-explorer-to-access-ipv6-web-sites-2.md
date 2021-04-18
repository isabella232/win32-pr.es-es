---
description: "Microsoft Internet Explorer admite el uso de IPv6 para conectar y obtener acceso a sitios habilitados para IPv6 (servidores web y servidores FTP, por ejemplo) cuando se cumplen las siguientes circunstancias: el equipo host que ejecuta Internet Explorer debe tener IPv6 instalado y habilitado. Al conectarse a un host que está fuera de la subred local, la interfaz que proporciona la conectividad debe tener asignada una dirección IPv6 enrutable. Cuando se conecta a la dirección de bucle invertido IPv6 (:: 1) o a un destino local de vínculo, no se requiere una dirección IPv6 enrutable. Si la dirección URL solicitada contiene un nombre (por ejemplo, www.contoso.com), la consulta del sistema de nombres de dominio (DNS) para ese nombre debe devolver una o más direcciones IPv6. Si la dirección URL solicitada contiene una dirección IPv6 (:: 1, por ejemplo), la dirección IPv6 debe ir entre corchetes (https:// \\[ :: 1 \\] ). Los identificadores de ámbito, a veces denominados índices de zona, se admiten como parte de la dirección IPv6. El identificador de ámbito se usa para determinar qué interfaz de red se va a usar al enviar la solicitud en equipos con varias interfaces de red. El identificador de ámbito se especifica mediante el carácter '% ' después de la dirección IPv6 principal (fe80:: 1% 11, por ejemplo). Sin embargo, el carácter '% ' debe ser de escape en la dirección URL utilizada con Internet Explorer. Por ejemplo, el ámbito ID 11 en una dirección local de vínculo se especificaría como https:// \\[ fe80:: 1% 2511 \\] cuando se usa Internet Explorer. Esta capacidad de usar direcciones IPv6 en una dirección URL es compatible con Internet Explorer 7 y versiones posteriores."
ms.assetid: c3a8303a-50d6-4deb-a371-171ac0a7c5a9
title: Usar Internet Explorer para tener acceso a sitios web de IPv6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6d11e7b207de132441d2152a4e0593b20bc00d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706944"
---
# <a name="using-internet-explorer-to-access-ipv6-websites"></a>Usar Internet Explorer para tener acceso a sitios web de IPv6

Microsoft Internet Explorer admite el uso de IPv6 para conectarse y acceder a sitios habilitados para IPv6 (por ejemplo, servidores web y servidores FTP) cuando se cumplen las siguientes circunstancias:

-   El equipo host que ejecuta Internet Explorer debe tener IPv6 instalado y habilitado.
    -   Al conectarse a un host que está fuera de la subred local, la interfaz que proporciona la conectividad debe tener asignada una dirección IPv6 enrutable.
    -   Cuando se conecta a la dirección de bucle invertido IPv6 (:: 1) o a un destino local de vínculo, no se requiere una dirección IPv6 enrutable.
-   Si la dirección URL solicitada contiene un nombre (por ejemplo, www.contoso.com), la consulta del sistema de nombres de dominio (DNS) para ese nombre debe devolver una o más direcciones IPv6.
-   Si la dirección URL solicitada contiene una dirección IPv6 (:: 1, por ejemplo), la dirección IPv6 debe ir entre corchetes (https:// \[ :: 1 \] ). Los identificadores de ámbito, a veces denominados índices de zona, se admiten como parte de la dirección IPv6. El identificador de ámbito se usa para determinar qué interfaz de red se va a usar al enviar la solicitud en equipos con varias interfaces de red. El identificador de ámbito se especifica mediante el carácter '% ' después de la dirección IPv6 principal (fe80:: 1% 11, por ejemplo). Sin embargo, el carácter '% ' debe ser de escape en la dirección URL utilizada con Internet Explorer. Por ejemplo, el ámbito ID 11 en una dirección local de vínculo se especificaría como https:// \[ fe80:: 1% 2511 \] cuando se usa Internet Explorer. Esta capacidad de usar direcciones IPv6 en una dirección URL es compatible con Internet Explorer 7 y versiones posteriores.

> [!Note]  
> Si Internet Explorer está configurado para usar un servidor proxy, el servidor proxy debe tener asignada una dirección IPv6 y el servidor proxy debe ser capaz de proxy las direcciones IPv6. El servidor proxy se utilizaría para conectarse a un host externo mediante IPv6. Normalmente se omitirá el servidor proxy para la dirección de bucle invertido IPv6 y las direcciones locales de vínculo IPv6.

 

 

 



