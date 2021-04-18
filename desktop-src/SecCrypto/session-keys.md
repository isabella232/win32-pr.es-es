---
description: Las claves de sesión son claves que se generan para usarse en una sola sesión de comunicación.
ms.assetid: 18bf2023-084d-400d-b60d-1ba51ce6a2bc
title: Claves de sesión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db4089f9ab5a0ae6889463c1b24c2eecb376c7f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688420"
---
# <a name="session-keys"></a>Claves de sesión

[*Las claves de sesión*](../secgloss/s-gly.md) son claves que se generan para usarse en una sola sesión de comunicación. Las claves de sesión se cambian con frecuencia y se descartan cuando ya no se necesitan. Por ejemplo, TLS usa una clave de sesión independiente para cada conexión y S/MIME usa una clave de sesión independiente para cada mensaje de correo electrónico. Normalmente, se usa una [*clave simétrica*](../secgloss/s-gly.md) como clave de sesión.

Las claves de sesión son volátiles. Las aplicaciones pueden guardar estas claves para su uso posterior o para su transmisión a otros usuarios. Para obtener más información, consulte [almacenamiento de claves criptográficas y Exchange](cryptographic-key-storage-and-exchange.md).

 

 
