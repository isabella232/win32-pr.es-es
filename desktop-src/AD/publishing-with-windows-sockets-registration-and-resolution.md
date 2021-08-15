---
title: Publicación con resolución de Windows de sockets de & de sockets
description: Windows Los servicios de Sockets pueden usar las API de registro y resolución (RnR) para publicar servicios y buscar servicios publicados con RnR.
ms.assetid: 95c16d0b-abbc-4407-ac31-d7de0b25bd74
ms.tgt_platform: multiple
keywords:
- Windows Registro de sockets y resolución de AD, publicación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a071a37d1d017e4c034f3eaab175889fdfcd1789d9f48aeac2c2943dfc8b4f1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118184929"
---
# <a name="publishing-with-windows-sockets-registration--resolution"></a>Publicación con resolución de Windows de sockets de & de sockets

Windows Los servicios de Sockets pueden usar las API de registro y resolución (RnR) para publicar servicios y buscar servicios publicados con RnR. La publicación de RnR se produce en dos pasos. El primer paso instala una clase de servicio que asocia un GUID con un nombre para el servicio. La clase de servicio puede contener datos de configuración específicos del servicio. A continuación, los servicios pueden publicarse como instancias de la clase de servicio. Cuando se publica, los clientes pueden consultar el servicio de directorio para las instancias de una clase determinada mediante las API de RnR y seleccionar una instancia a la que enlazar. Cuando una clase ya no es necesaria, se puede quitar.

 

 




