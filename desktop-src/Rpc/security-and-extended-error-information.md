---
title: Seguridad e información de error extendida
description: La información de error extendida ofrece datos muy útiles al solucionar un problema de RPC, pero muchas organizaciones con control de seguridad consideran estos datos confidenciales.
ms.assetid: ca6ef213-e59d-4b4e-ae7e-f5b20d11fd01
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b2029b40937dcef0622f6163e5e8f95b7006ade
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127473556"
---
# <a name="security-and-extended-error-information"></a>Seguridad e información de error extendida

La información de error extendida ofrece datos muy útiles al solucionar un problema de RPC, pero muchas organizaciones con control de seguridad consideran estos datos confidenciales. A la vista de estos problemas de seguridad, la información de error extendida está desactivada de forma predeterminada.

La información de error extendida se sigue generando cuando la información de error extendida está deshabilitada, pero la información nunca se transmite a través de los límites del proceso o del equipo. Este enfoque permite que las herramientas que tienen acceso al espacio de direcciones del proceso, como los depuradores, utilicen la información de errores. Cuando está activada, se genera información de error extendida y se puede enviar a través de los límites del proceso y del equipo. Actualmente, se usa información de error extendida para secuencias de protocolo orientadas a conexiones y RPC local (LRPC). Se implementa parcialmente para datagramas.

 

 




