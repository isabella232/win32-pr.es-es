---
title: Consideraciones de seguridad de punto de control
description: Al crear un punto de control, debe tener en cuenta los siguientes problemas de seguridad.
ms.assetid: 3281b4c3-d730-4273-9031-840a6ac655ce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0165ad0c8a721b10d5cc34c49947a98f2c15d1de
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994442"
---
# <a name="control-point-security-considerations"></a>Consideraciones de seguridad de punto de control

Al crear un punto de control, debe tener en cuenta los siguientes problemas de seguridad.

-   De forma predeterminada, todas las búsquedas de puntos de control se envían con un TTL de 1. Esto significa que solo se detectan los dispositivos dentro de la misma subred. Puede configurar un TTL superior en el registro.
-   La descripción del dispositivo y del servicio de un dispositivo solo se descarga si está presente en el mismo dispositivo que envió el anuncio del dispositivo.
-   Un dispositivo solo envía solicitudes de control y suscripción si las direcciones URL de control y suscripción se encuentran en el mismo dispositivo que envió los anuncios del dispositivo.

 

 




