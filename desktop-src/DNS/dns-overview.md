---
title: Introducción a DNS
description: DNS es un servicio estándar del sector que se usa para buscar equipos en una red basada en protocolo de Internet (IP).
ms.assetid: 98ecf24b-8bd5-4a75-a487-8af3080e8987
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 470807a5775b022834a3ca2f0ee3f91db8bdd5de
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/10/2021
ms.locfileid: "104280219"
---
# <a name="dns-overview"></a>Introducción a DNS

DNS es un servicio estándar del sector que se usa para buscar equipos en una red basada en protocolo de Internet (IP). Las redes IP, como las redes Internet y Windows 2000, se basan en direcciones basadas en números, como 207.46.131.137 para la información de transbordador a través de la red. Los usuarios de la red se basan en nombres basados en caracteres, como `www.microsoft.com` . Por lo tanto, es necesario traducir las direcciones de caracteres o descriptivas ( `www.microsoft.com` ) en las direcciones basadas en números (207.46.131.137) que la red puede reconocer. DNS es el servicio preferido en Windows 2000 para localizar recursos y traducirlos en sus direcciones IP correspondientes.

DNS utiliza una base de datos especializada de registros de recursos, que se suele denominar simplemente RRs, para responder a las consultas de resolución de nombres de cliente. Antes de DNS, la resolución de nombres en Internet se logra con el [*archivo de hosts*](h-gly.md), que son archivos creados manualmente que asocian los nombres de host con direcciones IP.

Cuando se agrega un nuevo cliente a la red, un administrador tenía que actualizar manualmente el archivo de hosts y, a continuación, copiar (replicar) el archivo en todos los demás equipos de la red para que todos los hosts nuevos pudieran ser accesibles. A medida que el Internet aumentó, esta forma de resolución de nombres era claramente insuficiente; era un uso intensivo de la administración y no [*escalaba*](s-gly.md). El archivo de hosts tiene un tamaño más grande, y dado que usó un [*espacio de nombres sin formato*](f-gly.md) (vea también [espacio de nombres](name-space.md)), no se pudo particionar y debía distribuirse en su totalidad. La solución era DNS.

-   DNS ha reemplazado el espacio de nombres sin formato del archivo de host por un [*espacio de nombres jerárquico*](h-gly.md). Con un espacio de nombres jerárquico, se pueden particionar y distribuir información sobre los nombres de host y las direcciones IP. por lo tanto, se logra la escalabilidad. Por ejemplo, en el dominio widgets.products.microsoft.com ficticio, se puede crear una partición de la responsabilidad de la resolución de nombres para que varios servidores puedan controlar la resolución de nombres para diferentes partes del espacio de nombres:
    -   Un servidor puede ser responsable de resolver la primera parte (microsoft.com) y, a continuación, puede reenviar la solicitud de resolución de nombres al siguiente servidor DNS de la jerarquía.
    -   El siguiente servidor DNS puede ser responsable de resolver la siguiente parte del espacio de nombres (productos).
    -   Por último, la solicitud se puede reenviar a un tercer servidor DNS responsable de resolver la última parte del nombre (widgets).

Los servidores DNS de cada parte del espacio de nombres jerárquico necesitan mantener una base de datos de registros de recursos para los hosts, pero solo en su parte de la jerarquía. Por lo tanto, el servidor (o servidores) de la parte productos de widgets.products.microsoft.com mantiene los RRs solo para los productos que forman parte del espacio de nombres jerárquico, no de la parte microsoft.com o de los widgets del espacio de nombres.

 

 




