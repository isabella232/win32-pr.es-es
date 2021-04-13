---
description: Una aplicación que utiliza una entidad de seguridad para almacenar las claves de sesión suele seguir estos pasos.
ms.assetid: 859310ed-6000-44c8-92f7-974326ce0fc9
title: Almacenar claves de sesión mediante una entidad de seguridad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d59906874f384d4eed9e20d6a781b14e3feba313
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104360744"
---
# <a name="storing-session-keys-using-a-backup-authority"></a>Almacenar claves de sesión mediante una entidad de seguridad

Una aplicación que utiliza una [*entidad de seguridad*](../secgloss/b-gly.md) para almacenar las claves de sesión suele seguir estos pasos.

**Para usar una autoridad de copia de seguridad**

1.  Cifre el archivo como de costumbre.
2.  Exporte la [*clave de sesión*](../secgloss/s-gly.md) usada para cifrar el archivo en un [*BLOB de clave simple*](../secgloss/s-gly.md), especificando que su propia [*clave pública de intercambio de claves*](../secgloss/k-gly.md) se usará para cifrar el BLOB de clave. Almacene este BLOB de clave con el archivo cifrado.
3.  Vuelva a exportar la clave de sesión, esta vez especificando que se utilizará la clave pública de la entidad de copia de seguridad para cifrar el BLOB de clave. Envíe este BLOB de clave a la entidad de seguridad, junto con la descripción de la clave, el número de serie, etc.

Si se pierde un [*par de claves*](../secgloss/k-gly.md) , las claves se pueden recuperar de la [*entidad de seguridad*](../secgloss/b-gly.md) si se puede establecer la identidad del propietario de las claves. El procedimiento para establecer la identidad viene determinado por la Directiva de la entidad de seguridad concreta y no implica CryptoAPI.

Para el código necesario para crear una clave de sesión y exportar esa clave a un [*BLOB de clave simple*](../secgloss/s-gly.md) que se puede escribir en un archivo de disco, vea el [ejemplo C programa: exportar una clave de sesión](example-c-program-exporting-a-session-key.md).

 

 
