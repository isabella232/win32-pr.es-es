---
description: "Microsoft Internet Explorer admite el uso de IPv6 para conectarse y acceder a sitios habilitados para IPv6 (servidores web y servidores FTP, por ejemplo) cuando se cumplen las siguientes circunstancias: La máquina host que ejecuta Internet Explorer debe tener IPv6 instalado y habilitado. Al conectarse a un host que está fuera de la subred local, la interfaz que proporciona la conectividad debe tener asignada una dirección IPv6 enrutable. Al conectarse a la dirección de bucleback IPv6 (::1) o a un destino local de vínculo, no se requiere una dirección IPv6 enrutable. Si la dirección URL solicitada contiene un nombre (www.contoso.com, por ejemplo), la consulta sistema de nombres de dominio (DNS) para ese nombre debe devolver una o varias direcciones IPv6. Si la dirección URL solicitada contiene una dirección IPv6 (::1, por ejemplo), la dirección IPv6 debe estar entre corchetes (https:// \\[ ::1 \\] ). Los ID de ámbito, a veces denominados índices de zona, se admiten como parte de la dirección IPv6. El identificador de ámbito se usa para determinar qué interfaz de red usar al enviar la solicitud en equipos con varias interfaces de red. El identificador de ámbito se especifica mediante el carácter '%' después de la dirección IPv6 principal (fe80::1%11, por ejemplo). Sin embargo, el carácter '%' debe tener caracteres de escape en la dirección URL usada con Internet Explorer. Por ejemplo, el identificador de ámbito 11 en una dirección local de vínculo se especificaría como \\[ https:// fe80::1%2511 cuando se \\] usa Internet Explorer. Esta capacidad de usar direcciones IPv6 en una dirección URL se admite en Internet Explorer 7 y versiones posteriores."
ms.assetid: c3a8303a-50d6-4deb-a371-171ac0a7c5a9
title: Uso Internet Explorer para acceder a sitios web IPv6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6d11e7b207de132441d2152a4e0593b20bc00d3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127361308"
---
# <a name="using-internet-explorer-to-access-ipv6-websites"></a>Uso Internet Explorer para acceder a sitios web IPv6

Microsoft Internet Explorer admite el uso de IPv6 para conectarse y acceder a sitios habilitados para IPv6 (servidores web y servidores FTP, por ejemplo) cuando se cumplen las siguientes circunstancias:

-   La máquina host que Internet Explorer debe tener IPv6 instalado y habilitado.
    -   Al conectarse a un host que está fuera de la subred local, la interfaz que proporciona la conectividad debe tener asignada una dirección IPv6 enrutable.
    -   Al conectarse a la dirección de bucleback IPv6 (::1) o a un destino local de vínculo, no se requiere una dirección IPv6 enrutable.
-   Si la dirección URL solicitada contiene un nombre (www.contoso.com, por ejemplo), la consulta sistema de nombres de dominio (DNS) para ese nombre debe devolver una o varias direcciones IPv6.
-   Si la dirección URL solicitada contiene una dirección IPv6 (::1, por ejemplo), la dirección IPv6 debe estar entre corchetes (https:// \[ ::1 \] ). Los ID de ámbito, a veces denominados índices de zona, se admiten como parte de la dirección IPv6. El identificador de ámbito se usa para determinar qué interfaz de red usar al enviar la solicitud en equipos con varias interfaces de red. El identificador de ámbito se especifica mediante el carácter '%' después de la dirección IPv6 principal (fe80::1%11, por ejemplo). Sin embargo, el carácter '%' debe tener caracteres de escape en la dirección URL usada con Internet Explorer. Por ejemplo, el identificador de ámbito 11 en una dirección local de vínculo se especificaría como \[ https:// fe80::1%2511 cuando se \] usa Internet Explorer. Esta capacidad de usar direcciones IPv6 en una dirección URL se admite en Internet Explorer 7 y versiones posteriores.

> [!Note]  
> Si Internet Explorer está configurado para usar un servidor proxy, el servidor proxy debe tener asignada una dirección IPv6 y el servidor proxy debe poder usar direcciones IPv6 de proxy. El servidor proxy se usaría para conectarse a un host externo mediante IPv6. Normalmente, el servidor proxy se omitiría para la dirección de bucle inverso IPv6 y las direcciones locales del vínculo IPv6.

 

 

 



