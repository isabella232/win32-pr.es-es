---
description: Una clave maestra es material de datos clave del que se derivan otras claves.
ms.assetid: c8445f74-659a-470b-9007-07ea98d36dcd
title: Crear la clave maestra
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b35a6aef52525bdce622355ede4ae9723f7cd8b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541011"
---
# <a name="creating-the-master-key"></a>Crear la clave maestra

Una [*clave maestra*](../secgloss/m-gly.md) es material de datos clave del que se derivan otras claves. Según el protocolo y el conjunto de cifrado usado, la clave maestra puede tener entre 5 y 48 bytes de longitud. Para el [](../secgloss/r-gly.md) / CSP [*Schannel*](../secgloss/s-gly.md) de RSA, la clave maestra la crea el lado cliente y se transfiere al servidor en un sobre RSA. En el caso de un CSP [*Diffie-Hellman*](../secgloss/d-gly.md)/Schannel, la clave maestra se crea mediante la realización de un intercambio de claves Diffie-Hellman.

El código para crear e intercambiar claves maestras se muestra en:

-   [Código de cliente de Diffie-Hellman para crear la clave maestra](diffie-hellman-client-code-for-creating-the-master-key.md)
-   [Código de servidor Diffie-Hellman para crear la clave maestra](diffie-hellman-server-code-for-creating-the-master-key.md)
-   [Código de cliente de RSA para crear la clave maestra](rsa-client-code-for-creating-the-master-key.md)
-   [Código de servidor RSA para crear la clave maestra](rsa-server-code-for-creating-the-master-key.md)
-   [Especificar los algoritmos](specifying-the-algorithms.md)

 

 
