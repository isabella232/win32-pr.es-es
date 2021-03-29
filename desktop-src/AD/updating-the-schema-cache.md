---
title: Actualización de la caché de esquema
description: Toda la información que se escribe en un servidor de Active Directory se valida con respecto al esquema.
ms.assetid: 948f8ec5-7207-4566-bd79-60cdd54231bf
ms.tgt_platform: multiple
keywords:
- Actualización de la caché de esquema AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2bf915d00b463b81a331ffe39b342f620a50417
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103773051"
---
# <a name="updating-the-schema-cache"></a>Actualización de la caché de esquema

Toda la información que se escribe en un servidor de Active Directory se valida con respecto al esquema. El esquema se mantiene en memoria en los servidores de directorio (controladores de dominio) por motivos de rendimiento. La versión en memoria se actualiza automáticamente después de actualizar la versión en el disco. La actualización automática se produce cinco minutos después de aplicar el último cambio; al aplicar otro cambio en el esquema en la ventana de 5 minutos, se restablece el temporizador durante otros cinco minutos. Este comportamiento mantiene la coherencia de la memoria caché, pero puede resultar confuso, ya que los cambios no aparecen en el esquema hasta que se actualice la memoria caché, aunque se hayan aplicado en el disco.

Para actualizar la memoria caché de esquemas de Active Directory después de una actualización de esquema, o si desea utilizar la actualización de esquema para las operaciones que no son de esquema inmediatamente, agregue el atributo **schemaUpdateNow** (es un atributo operativo) al DSE raíz (DN en blanco) con el valor 1. Una actualización de la caché de esquema se iniciará inmediatamente. La llamada está bloqueando. Si la llamada devuelve sin ningún error, la memoria caché se actualiza y todas las actualizaciones del esquema están listas para usarse. Un error devuelto indica que la actualización de la memoria caché no se ha realizado correctamente. Las aplicaciones que deben usar esta característica deben diseñarse para adaptarse a la escritura de bloqueo, especialmente en el caso de los comentarios de los usuarios, si el programa o el script se ejecutan de forma interactiva.

El ejemplo de código siguiente es un script de LDIFDE de ejemplo que muestra cómo desencadenar una recarga de caché.

``` syntax
dn:
changetype: modify
add: schemaUpdateNow
schemaUpdateNow: 1
-
```

Para obtener más información sobre cómo actualizar la caché de esquema mediante programación, vea [el código de ejemplo para actualizar la caché de esquema](example-code-for-updating-the-schema-cache.md).

 

 




