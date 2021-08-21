---
title: Publicación de servicios COM+
description: Los servicios basados en COM proporcionan un proxy de aplicación en forma de un paquete Windows instalador de aplicaciones (MSI).
ms.assetid: 38200a22-bea5-4967-a51a-e777b34f299d
ms.tgt_platform: multiple
keywords:
- Publicación de servicios COM+
- Active Directory, usar, publicar un servicio, servicios COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91801bbfcbf8efa34ac0b79477dd9d859fc2ed34a8d40bcf0bd829f82cfd571a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119025433"
---
# <a name="publishing-com-services"></a>Publicación de servicios COM+

Los servicios basados en COM proporcionan un proxy de aplicación en forma de un paquete Windows instalador de aplicaciones (MSI). Este .msi archivo contiene el nombre del servidor que se va a usar y otros elementos necesarios, como proxy/stubs y bibliotecas de tipos necesarios para la marshalling. El complemento Servicios de componentes genera automáticamente estos servidores proxy de aplicación para aplicaciones de servidor COM+.

Los servidores proxy de aplicación se publican en objetos de directiva Active Directory mediante el Editor directiva de grupo aplicaciones. No se requiere ninguna intervención especial en la aplicación cliente. La cuenta de equipo o usuario del equipo cliente debe estar en una unidad organizativa configurada para usar el objeto de directiva en el que se publican los servidores proxy de aplicación. El enlazador COM busca automáticamente el servidor por medio del directorio cuando el cliente establece una instancia de los objetos en cuestión.

 

 




