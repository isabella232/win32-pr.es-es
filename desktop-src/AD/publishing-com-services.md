---
title: Publicar servicios COM+
description: Los servicios basados en COM proporcionan un proxy de aplicación en forma de paquete de Windows Installer (MSI).
ms.assetid: 38200a22-bea5-4967-a51a-e777b34f299d
ms.tgt_platform: multiple
keywords:
- Publicar servicios COM+
- Active Directory, usar, publicar un servicio, servicios COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9044b72b4a604a4d863315963cd097be67f6afce
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075108"
---
# <a name="publishing-com-services"></a>Publicar servicios COM+

Los servicios basados en COM proporcionan un proxy de aplicación en forma de paquete de Windows Installer (MSI). Este archivo. msi contiene el nombre del servidor que se va a usar y otros elementos necesarios, como el proxy o los códigos auxiliares y las bibliotecas de tipos necesarios para la serialización. El complemento Servicios de componentes genera automáticamente estos proxies de aplicación para las aplicaciones de servidor COM+.

Los proxies de aplicación se publican en objetos de directiva en Active Directory mediante el editor de directiva de grupo. No se requiere ninguna intervención especial en la aplicación cliente. La cuenta de equipo o de usuario en el equipo cliente debe estar en una unidad organizativa configurada para usar el objeto de directiva en el que se publican los proxies de aplicación. El enlazador COM busca automáticamente el servidor por medio del directorio cuando el cliente establece una instancia de los objetos afectados.

 

 




