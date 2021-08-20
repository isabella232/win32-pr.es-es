---
title: Consideraciones de seguridad de punto de control
description: Al crear un punto de control, debe tener en cuenta los siguientes problemas de seguridad.
ms.assetid: 3281b4c3-d730-4273-9031-840a6ac655ce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85378d7f530177bb42a6751a13f643bad984e994ae65178c0ab06cd5ce4792a3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118126012"
---
# <a name="control-point-security-considerations"></a>Consideraciones de seguridad de punto de control

Al crear un punto de control, debe tener en cuenta los siguientes problemas de seguridad.

-   Todas las búsquedas de puntos de control se envían de forma predeterminada con un TTL de 1. Esto significa que solo se detectan los dispositivos dentro de la misma subred. Puede configurar un TTL superior en el Registro.
-   La descripción del dispositivo y del servicio de un dispositivo solo se descarga si está presente en el mismo dispositivo que envió el anuncio del dispositivo.
-   Un dispositivo solo se envía a las solicitudes de control y suscripción si sus direcciones URL de control y suscripción están en el mismo dispositivo que envió los anuncios del dispositivo.

 

 




