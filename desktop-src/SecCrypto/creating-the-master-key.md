---
description: Una clave maestra es material de datos clave del que se derivan otras claves.
ms.assetid: c8445f74-659a-470b-9007-07ea98d36dcd
title: Creación de la clave maestra
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7dea47c64348f89563340a4e25d411ed3174ee9d18ba1705d9707eab6b39633b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119876542"
---
# <a name="creating-the-master-key"></a>Creación de la clave maestra

Una [*clave maestra es*](../secgloss/m-gly.md) material de datos clave del que se derivan otras claves. Según el protocolo y el conjunto de cifrado usados, la clave maestra puede tener una longitud de entre 5 y 48 bytes. Para [*el CSP de*](../secgloss/r-gly.md) / [*Schannel*](../secgloss/s-gly.md) de RSA, el lado cliente crea la clave maestra y se transfiere al servidor en un sobre RSA. En el caso de un CSP [*diffie-Hellman*](../secgloss/d-gly.md)/Schannel, la clave maestra se crea realizando una Diffie-Hellman de claves.

El código para crear e intercambiar claves maestras se muestra en:

-   [Código de cliente Diffie-Hellman para crear la clave maestra](diffie-hellman-client-code-for-creating-the-master-key.md)
-   [Diffie-Hellman Server Code for Creating the Master Key](diffie-hellman-server-code-for-creating-the-master-key.md)
-   [Código de cliente RSA para crear la clave maestra](rsa-client-code-for-creating-the-master-key.md)
-   [Código del servidor RSA para crear la clave maestra](rsa-server-code-for-creating-the-master-key.md)
-   [Especificar los algoritmos](specifying-the-algorithms.md)

 

 
