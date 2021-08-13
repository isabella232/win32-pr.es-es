---
title: Sistema de archivos distribuido (DFS)
description: Las Sistema de archivos distribuido (DFS) proporcionan la capacidad de agrupar lógicamente recursos compartidos en varios servidores y de vincular recursos compartidos de forma transparente en un único espacio de nombres jerárquico. DFS organiza los recursos compartidos en una red en una estructura similar a un árbol.
ms.assetid: a29cde3e-483a-4658-94d4-27398f66abfb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 898d44ecfaeb99145570230e49156440dc9e2aac02051baa47bb496a0f58b2b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119380585"
---
# <a name="distributed-file-system-dfs-functions"></a>Sistema de archivos distribuido (DFS)

Las Sistema de archivos distribuido (DFS) proporcionan la capacidad de agrupar lógicamente recursos compartidos en varios servidores y de vincular recursos compartidos de forma transparente en un único espacio de nombres jerárquico. DFS organiza los recursos compartidos en una red en una estructura similar a un árbol.

DFS admite *espacios de nombres* DFS independientes, aquellos  con un servidor host y espacios de nombres basados en dominio que tienen varios servidores host y alta disponibilidad. Los datos de *topología DFS para* espacios de nombres basados en dominio se almacenan en Active Directory. Los datos incluyen la raíz DFS, los vínculos DFS y los destinos DFS.

Cada estructura de árbol DFS tiene uno o varios *destinos raíz.* El destino raíz es un servidor host que ejecuta el servicio DFS. Una estructura de árbol DFS puede contener uno o varios *vínculos DFS*. Cada vínculo DFS apunta a una o varias carpetas compartidas en la red. Puede agregar, modificar y eliminar vínculos DFS de un espacio de nombres DFS. Al quitar el último destino asociado a un vínculo DFS, DFS elimina el vínculo DFS en el espacio de nombres DFS. (En la documentación anterior, los vínculos DFS se denominaban puntos de unión).

Un vínculo DFS puede apuntar a una o varias carpetas compartidas; Las carpetas se denominan *destinos*. Cuando los usuarios acceden a un vínculo DFS, el servidor DFS selecciona un conjunto de destinos en función de la información del sitio de un cliente. El cliente tiene acceso al primer destino disponible del conjunto. Esto ayuda a distribuir las solicitudes de cliente entre los posibles destinos y puede proporcionar accesibilidad continua para los usuarios incluso cuando se producirá un error en algunos servidores.

Una aplicación puede usar las funciones DFS para:

- Agregue un vínculo DFS a una raíz DFS.
- Cree o quite espacios de nombres DFS independientes y basados en dominio.
- Agregue destinos a un vínculo DFS existente.
- Quite un vínculo DFS de una raíz DFS.
- Quitar un destino de un vínculo DFS.
- Ver y configurar información sobre raíces y vínculos DFS.

Para obtener una lista de las funciones DFS, [vea Sistema de archivos distribuido Functions](distributed-file-system-functions.md).

Para obtener una lista de las estructuras DFS, [vea Sistema de archivos distribuido estructuras](distributed-file-system-structures.md).

Los destinos en equipos que ejecutan Microsoft Windows pueden publicarse en un espacio de nombres DFS. También puede publicar los recursos compartidos que no son de Microsoft para los que los redireccionamientos de cliente están disponibles en un espacio de nombres DFS. Sin embargo, a diferencia de un recurso compartido que se publica en un servidor que ejecuta Windows Server, no pueden hospedar una raíz DFS ni proporcionar referencias a otros destinos DFS.

DFS usa el servicio de replicación de Windows Server para copiar los cambios entre destinos replicados. Los usuarios pueden modificar los archivos almacenados en un destino y el servicio de replicación de archivos propaga los cambios a los otros destinos designados. El servicio conserva el cambio más reciente en un documento o archivos.
