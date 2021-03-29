---
title: Seguridad e información de error ampliada
description: La información de error extendida ofrece datos muy útiles a la hora de solucionar problemas de RPC, pero muchos de ellos se consideran confidenciales en las organizaciones con seguridad.
ms.assetid: ca6ef213-e59d-4b4e-ae7e-f5b20d11fd01
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b2029b40937dcef0622f6163e5e8f95b7006ade
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103779087"
---
# <a name="security-and-extended-error-information"></a>Seguridad e información de error ampliada

La información de error extendida ofrece datos muy útiles a la hora de solucionar problemas de RPC, pero muchos de ellos se consideran confidenciales en las organizaciones con seguridad. En consideración de estos problemas de seguridad, la información de error ampliada está desactivada de forma predeterminada.

La información de error extendida se sigue generando cuando la información de error extendida está deshabilitada, pero la información nunca se transmite a través de los límites de proceso o equipo. Este enfoque permite que la información de errores sea utilizada por herramientas que tienen acceso al espacio de direcciones de proceso, como depuradores. Cuando está activada, se genera información de error extendida que se puede enviar a través de los límites del proceso y del equipo. Actualmente, la información de error extendida se usa para las secuencias de protocolos orientados a conexiones y RPC local (LRPC). Se implementa parcialmente para los datagramas.

 

 




