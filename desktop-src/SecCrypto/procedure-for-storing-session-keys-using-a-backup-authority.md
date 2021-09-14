---
description: Una aplicación que usa una entidad de copia de seguridad para almacenar claves de sesión normalmente sigue estos pasos.
ms.assetid: 859310ed-6000-44c8-92f7-974326ce0fc9
title: Almacenamiento de claves de sesión mediante una entidad de copia de seguridad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d59906874f384d4eed9e20d6a781b14e3feba313
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127170870"
---
# <a name="storing-session-keys-using-a-backup-authority"></a>Almacenamiento de claves de sesión mediante una entidad de copia de seguridad

Una aplicación que usa una entidad [*de copia de seguridad*](../secgloss/b-gly.md) para almacenar claves de sesión normalmente sigue estos pasos.

**Para usar una entidad de copia de seguridad**

1.  Cifre el archivo como de costumbre.
2.  Exporte [*la clave de sesión*](../secgloss/s-gly.md) usada para cifrar el archivo [](../secgloss/k-gly.md) en un blob de clave [*simple,*](../secgloss/s-gly.md)especificando que se usará su propia clave pública de intercambio de claves para cifrar el BLOB de clave. Almacene este blob de clave con el archivo cifrado.
3.  Vuelva a exportar la clave de sesión, esta vez especificando que la clave pública de la entidad de copia de seguridad se usará para cifrar el BLOB de clave. Envíe este BLOB de clave a la entidad de copia de seguridad, junto con la descripción de la clave, el número de serie, y así sucesivamente.

Si se [*pierde un par*](../secgloss/k-gly.md) de claves, [](../secgloss/b-gly.md) las claves se pueden recuperar de la entidad de copia de seguridad si se puede establecer la identidad del propietario de las claves. El procedimiento para establecer la identidad viene determinado por la directiva de la entidad de copia de seguridad determinada y no implica CryptoAPI.

Para obtener el código necesario para crear una clave de sesión y exportarla a un blob de clave [*simple*](../secgloss/s-gly.md) que se pueda escribir en un archivo de disco, vea Ejemplo [de programa C:](example-c-program-exporting-a-session-key.md)Exportación de una clave de sesión .

 

 
