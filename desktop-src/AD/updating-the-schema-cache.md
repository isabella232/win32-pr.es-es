---
title: Actualización de la caché de esquemas
description: Toda la información que se escribe en un servidor Active Directory se valida con el esquema.
ms.assetid: 948f8ec5-7207-4566-bd79-60cdd54231bf
ms.tgt_platform: multiple
keywords:
- Actualización de la caché de esquemas de AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff477ce97aab2e0e49522309d386a7e1c37b31e3b8171ef20c626fdaaa5b53a8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119024533"
---
# <a name="updating-the-schema-cache"></a>Actualización de la caché de esquemas

Toda la información que se escribe en un servidor Active Directory se valida con el esquema. El esquema se mantiene en memoria en los servidores de directorio (controladores de dominio) por motivos de rendimiento. La versión en memoria se actualiza automáticamente una vez actualizada la versión en disco. La actualización automática se produce cinco minutos después de aplicar el último cambio. Al aplicar otro cambio al esquema en la ventana de 5 minutos, se restablece el temporizador durante otros 5 minutos. Este comportamiento mantiene la caché coherente, pero puede resultar confusa, ya que los cambios no aparecen en el esquema hasta que se actualiza la memoria caché, aunque se aplicaron en el disco.

Para actualizar la caché de esquema de Active Directory después de una actualización de esquema, o si desea usar la actualización de esquema para las operaciones que no son de esquema inmediatamente, agregue el atributo **schemaUpdateNow** (es un atributo operativo) al DSE raíz (DN en blanco) con el valor 1. Una actualización de caché de esquema se iniciará inmediatamente. La llamada está bloqueando. Si la llamada se devuelve sin errores, la memoria caché se actualiza y todas las actualizaciones de esquema están listas para usarse. Una devolución de error indica que la actualización de caché no se ha producido correctamente. Las aplicaciones que deben usar esta característica deben estar diseñadas para dar cabida a la escritura de bloqueo, especialmente para proporcionar comentarios al usuario, si el programa o script se ejecuta de forma interactiva.

El ejemplo de código siguiente es un script LDIFDE de ejemplo que muestra cómo desencadenar una recarga de caché.

``` syntax
dn:
changetype: modify
add: schemaUpdateNow
schemaUpdateNow: 1
-
```

Para obtener más información sobre cómo actualizar la caché de esquemas mediante programación, vea Código de [ejemplo para actualizar la caché de esquemas.](example-code-for-updating-the-schema-cache.md)

 

 




