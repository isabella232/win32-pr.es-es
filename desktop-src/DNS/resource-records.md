---
title: Registros de recursos
description: Un registro de recursos, que normalmente se conoce como un RR, es la unidad de la entrada de información en archivos de zona DNS. Los RRs son los bloques de creación básicos de la información del nombre del host y de la dirección IP, y se usan para resolver todas las consultas DNS.
ms.assetid: c64907c2-ebd3-4550-9454-13f51a6d7ca6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05b667b95a8ede32018e1aad7de375e77a890487
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103778336"
---
# <a name="resource-records"></a>Registros de recursos

Un registro de recursos, que normalmente se conoce como un RR, es la unidad de la entrada de información en archivos de zona DNS. Los RRs son los bloques de creación básicos de la información del nombre del host y de la dirección IP, y se usan para resolver todas las consultas DNS. Los registros de recursos existen tantos tipos para proporcionar servicios extendidos de resolución de nombres.

Los distintos tipos de RRs tienen formatos diferentes, ya que contienen datos diferentes. Sin embargo, en general, muchos RRs comparten un formato común, como se muestra en el siguiente ejemplo de registros de recursos de dirección. En el siguiente ejemplo ficticio se explican los campos que se encuentran en un registro de recursos A:

``` syntax
microsoft.com. 600 IN A 150.150.150.1
```

-   El primer campo (microsoft.com) denota el propietario.
-   El segundo campo (600) es el parámetro de período de vida (TTL), en segundos.
-   El tercer campo (en) es el campo de clase que representa la familia de protocolos, que casi siempre está en, para la clase de Internet.
-   El cuarto campo (A) es el tipo de recurso que representa el RR.
-   El quinto campo (150.150.150.1) son los datos de recursos o RDATA. Este campo es un tipo de variable que proporciona información adecuada para el tipo de recurso. en este caso, se trata de una dirección IP de 32 bits.

Los siguientes tipos de registro de recursos se usan normalmente en DNS:

-   Inicio de autoridad (SOA)
-   Servidor de nombres (NS)
-   [*Registro de puntero*](p-gly.md) (PTR)
-   Dirección (A)
-   Dirección IPv6 (AAAA)
-   Intercambio de correo (MX)
-   [*Nombre canónico*](c-gly.md) (CNAME)
-   Windows Internet Naming Service (WINS)
-   Búsqueda inversa de WINS (WINSr)

Hay muchos otros tipos de registros de recursos en DNS. Para obtener más información, vea [Referencia del proveedor WMI de DNS](dns-wmi-provider-reference.md).

 

 




