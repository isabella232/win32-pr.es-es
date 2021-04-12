---
title: Publicación con la resolución de & de registro de Windows Sockets
description: Los servicios de Windows Sockets pueden usar las API de registro y resolución (RnR) para publicar servicios y buscar servicios publicados con RnR.
ms.assetid: 95c16d0b-abbc-4407-ac31-d7de0b25bd74
ms.tgt_platform: multiple
keywords:
- Registro y resolución de Windows Sockets AD, publicación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e722d83447bd97e3964a9a0cc85df45ffd27faba
ms.sourcegitcommit: 460af18ea55f4b12d47d5b8d4b883896e21adf00
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/04/2019
ms.locfileid: "104487207"
---
# <a name="publishing-with-windows-sockets-registration--resolution"></a>Publicación con la resolución de & de registro de Windows Sockets

Los servicios de Windows Sockets pueden usar las API de registro y resolución (RnR) para publicar servicios y buscar servicios publicados con RnR. La publicación de RnR se produce en dos pasos. En el primer paso se instala una clase de servicio que asocia un GUID con un nombre para el servicio. La clase de servicio puede contener datos de configuración específicos del servicio. Después, los servicios pueden publicarse como instancias de la clase de servicio. Cuando se publican, los clientes pueden consultar el servicio de directorio en busca de instancias de una clase determinada mediante las API de RnR y seleccionar una instancia de a la que enlazar. Cuando ya no se necesita una clase, se puede quitar.

 

 




