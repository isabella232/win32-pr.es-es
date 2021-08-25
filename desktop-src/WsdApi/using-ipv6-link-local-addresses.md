---
description: El direccionamiento local del vínculo IPv6 en los mensajes SOAP proporciona un desafío único, ya que las direcciones locales de vínculo IPv6 requieren que un identificador de ámbito sea significativo, pero el identificador de ámbito solo tiene significado para el equipo local.
ms.assetid: 63495335-e447-4564-b669-0896c7aac63f
title: Uso de direcciones locales de vínculo iPv6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e10c1719e4e6d374e7afd859b80cd1bc14c4c841cb7dceee149f14d0acb777f9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119897165"
---
# <a name="using-ipv6-link-local-addresses"></a>Uso de direcciones locales de vínculo iPv6

El direccionamiento local del vínculo IPv6 en los mensajes SOAP proporciona un desafío único, ya que las direcciones locales de vínculo IPv6 requieren que un identificador de ámbito sea significativo, pero el identificador de ámbito solo tiene significado para el equipo local. Todas las implementaciones de cliente y dispositivo deben quitar el identificador de ámbito antes de enviar una dirección local de vínculo IPv6 en un mensaje SOAP. Además, cuando se recibe una dirección local de vínculo IPv6 en un mensaje, se debe conocer la interfaz en la que se recibió el mensaje para que se pueda reconstruir la dirección local del vínculo completo con el identificador de ámbito.

 

 



