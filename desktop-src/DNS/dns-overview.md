---
title: Introducción a DNS
description: DNS es un servicio estándar del sector que se usa para localizar equipos en una red basada en protocolo de Internet (IP).
ms.assetid: 98ecf24b-8bd5-4a75-a487-8af3080e8987
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5a47874606491c1baf5c52ca7934d7e0c3156a6ab99f9726e6c000d9eb3cb65
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119967475"
---
# <a name="dns-overview"></a>Introducción a DNS

DNS es un servicio estándar del sector que se usa para localizar equipos en una red basada en protocolo de Internet (IP). Las redes IP, como Internet y Windows 2000, se basan en direcciones basadas en números, como 207.46.131.137 para la información de los transbordadores en toda la red. Los usuarios de red se basan en nombres basados en caracteres, como `www.microsoft.com` . Por lo tanto, es necesario traducir las direcciones de caracteres o fáciles de usar ( ) en las direcciones basadas en números `www.microsoft.com` (207.46.131.137) que la red pueda reconocer. DNS es el servicio elegido en Windows 2000 para buscar recursos y traducirlos a sus direcciones IP correspondientes.

DNS usa una base de datos especializada de registros de recursos, que normalmente se conocen simplemente como RR, para responder a consultas de resolución de nombres de cliente. Antes de DNS, la resolución de nombres en Internet se lograba con el archivo [*de hosts*](h-gly.md), que se crean manualmente archivos que asociaban nombres de host con direcciones IP.

Cuando se agregó un nuevo cliente a la red, un administrador tenía que actualizar manualmente el archivo de hosts y, a continuación, copiar (replicar) ese archivo en todos los demás equipos de la red para que todos pudieran obtener acceso al nuevo host. A medida que Internet crece, esta forma de resolución de nombres era claramente insuficiente. era demasiado intensivo en la administración y no [*escalaba*](s-gly.md). El archivo de hosts se ha hecho más grande y, dado que ha usado un espacio de [*nombres*](f-gly.md) plano (vea también Espacio de [nombres),](name-space.md)no se pudo particionar y tuvo que distribuirse en su totalidad. La solución era DNS.

-   DNS reemplazó el espacio de nombres sin formato del archivo de hosts por [*un espacio de nombres jerárquico.*](h-gly.md) Con un espacio de nombres jerárquico, la información sobre los nombres de host y las direcciones IP se puede dividir y distribuir; por lo tanto, se logra la escalabilidad. Por ejemplo, en el dominio widgets.products.microsoft.com ficticio, la responsabilidad de la resolución de nombres se puede particionar para que varios servidores puedan controlar la resolución de nombres para diferentes partes del espacio de nombres:
    -   Un servidor puede ser responsable de resolver la primera parte (microsoft.com) y, a continuación, puede reenviar la solicitud de resolución de nombres al siguiente servidor DNS de la jerarquía.
    -   El siguiente servidor DNS puede ser responsable de resolver la siguiente parte del espacio de nombres (productos).
    -   Por último, la solicitud se puede reenviar a un tercer servidor DNS responsable de resolver la última parte del nombre (widgets).

Los servidores DNS de cada parte del espacio de nombres jerárquico deben mantener una base de datos de registros de recursos para los hosts, pero solo en su parte de la jerarquía. Por lo tanto, el servidor (o servidores) de la parte de productos de widgets.products.microsoft.com mantiene los RR solo para la parte de productos del espacio de nombres jerárquico, no para la parte microsoft.com o los widgets del espacio de nombres.

 

 




