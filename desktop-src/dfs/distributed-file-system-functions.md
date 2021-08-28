---
title: Sistema de archivos distribuido Functions
description: Estas son las funciones Sistema de archivos distribuido (DFS).
ms.assetid: 8f86b717-fe26-4550-8b71-8f7df5ca6022
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da3fd41879293f376dfdb3d769d5152b2e747fc6e387f8f9538854d4d3e06e7a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120096725"
---
# <a name="distributed-file-system-functions"></a>Sistema de archivos distribuido Functions

Estas son las funciones Sistema de archivos distribuido (DFS).

## <a name="in-this-section"></a>En esta sección

<dl> <dt>

[NetDfsAdd](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsadd)
</dt> <dd>
Crea un nuevo vínculo Sistema de archivos distribuido (DFS) o agrega destinos a un vínculo existente en un espacio de nombres DFS.

</dd> <dt>

[NetDfsAddFtRoot](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsaddftroot)
</dt> <dd>
Crea un nuevo espacio de nombres de Sistema de archivos distribuido basado en dominio (DFS). Si el espacio de nombres ya existe, la función le agrega el destino raíz especificado.

</dd> <dt>

[NetDfsAddRootTarget](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsaddroottarget)
</dt> <dd>
Crea un espacio de nombres DFS independiente o basado en dominio o agrega un nuevo destino raíz a un espacio de nombres basado en dominio existente.

</dd> <dt>

[NetDfsAddStdRoot](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsaddstdroot)
</dt> <dd>
Crea un nuevo espacio de nombres Sistema de archivos distribuido independiente (DFS).

</dd> <dt>

[NetDfsEnum](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsenum)
</dt> <dd>
Enumera los espacios de Sistema de archivos distribuido (DFS) hospedados en un servidor o vínculos DFS de un espacio de nombres hospedado por un servidor.

</dd> <dt>

[NetDfsGetClientInfo](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetclientinfo)
</dt> <dd>
Recupera información sobre una raíz Sistema de archivos distribuido dfs (DFS) de la memoria caché mantenida por el cliente DFS.

</dd> <dt>

[NetDfsGetFtContainerSecurity](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetftcontainersecurity)
</dt> <dd>
Recupera el descriptor de seguridad del objeto contenedor para los espacios de nombres DFS basados en dominio del dominio Active Directory dominio.

</dd> <dt>

[NetDfsGetInfo](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetinfo)
</dt> <dd>
Recupera información sobre una raíz o vínculo Sistema de archivos distribuido dfs (DFS) especificado en un espacio de nombres DFS.

</dd> <dt>

[NetDfsGetSecurity](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetsecurity)
</dt> <dd>
Recupera el descriptor de seguridad para el objeto raíz del espacio de nombres DFS especificado.

</dd> <dt>

[NetDfsGetStdContainerSecurity](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetstdcontainersecurity)
</dt> <dd>
Recupera el descriptor de seguridad para el objeto contenedor del espacio de nombres DFS independiente especificado.

</dd> <dt>

[NetDfsGetSupportedNamespaceVersion](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetsupportednamespaceversion)
</dt> <dd>
Determina el número de versión de metadatos admitido.

</dd> <dt>

[NetDfsMove](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsmove)
</dt> <dd>
Cambia el nombre o mueve un vínculo DFS.

</dd> <dt>

[NetDfsRemove](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsremove)
</dt> <dd>
Quita un vínculo Sistema de archivos distribuido (DFS) o un destino de vínculo específico de un vínculo DFS en un espacio de nombres DFS. Al quitar un destino de vínculo específico, el propio vínculo se quita si se quita el último destino de vínculo del vínculo.

</dd> <dt>

[NetDfsRemoveFtRoot](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsremoveftroot)
</dt> <dd>
Quita el destino raíz especificado de un espacio de nombres Sistema de archivos distribuido dominio (DFS). Si se quita el último destino raíz del espacio de nombres DFS, la función también elimina el espacio de nombres DFS. Un espacio de nombres DFS se puede eliminar sin eliminar primero todos los vínculos que contiene.

</dd> <dt>

[NetDfsRemoveFtRootForced](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsremoveftrootforced)
</dt> <dd>
Quita el destino raíz especificado de un espacio de nombres de Sistema de archivos distribuido basado en dominio (DFS), incluso si el servidor de destino raíz está sin conexión. Si se quita el último destino raíz del espacio de nombres DFS, la función también elimina el espacio de nombres DFS. Un espacio de nombres DFS se puede eliminar sin eliminar primero todos los vínculos que contiene.

> [!Note]
> La [**función NetDfsRemoveFtRootForced**](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsremoveftrootforced) no actualiza el Registro en el servidor de destino raíz DFS. Para obtener más información, vea la sección Comentarios.

</dd> <dt>

[NetDfsRemoveRootTarget](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsremoveroottarget)
</dt> <dd>
Quita un destino raíz DFS de un espacio de nombres DFS basado en dominio. Si el destino raíz es el último destino raíz del espacio de nombres DFS, esta función quita el espacio de nombres DFS. Esta función también se puede usar para quitar un espacio de nombres DFS independiente.

</dd> <dt>

[NetDfsRemoveStdRoot](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsremovestdroot)
</dt> <dd>
Elimina un espacio de nombres Sistema de archivos distribuido independiente (DFS).

</dd> <dt>

[NetDfsSetClientInfo](/windows/desktop/api/lmdfs/nf-lmdfs-netdfssetclientinfo)
</dt> <dd>
Modifica la información sobre una raíz Sistema de archivos distribuido (DFS) o un vínculo en la memoria caché mantenida por el cliente DFS.

</dd> <dt>

[NetDfsSetFtContainerSecurity](/windows/desktop/api/lmdfs/nf-lmdfs-netdfssetftcontainersecurity)
</dt> <dd>
Establece el descriptor de seguridad del objeto contenedor para los espacios de nombres DFS basados en dominio en el Active Directory especificado.

</dd> <dt>

[NetDfsSetInfo](/windows/desktop/api/lmdfs/nf-lmdfs-netdfssetinfo)
</dt> <dd>
Establece o modifica información sobre una raíz de Sistema de archivos distribuido (DFS) específica, el destino raíz, el vínculo o el destino de vínculo.

</dd> <dt>

[NetDfsSetSecurity](/windows/desktop/api/lmdfs/nf-lmdfs-netdfssetsecurity)
</dt> <dd>
Establece el descriptor de seguridad para el objeto raíz del espacio de nombres DFS especificado.

</dd> <dt>

[NetDfsSetStdContainerSecurity](/windows/desktop/api/lmdfs/nf-lmdfs-netdfssetstdcontainersecurity)
</dt> <dd>
Establece el descriptor de seguridad para el objeto contenedor del espacio de nombres DFS independiente especificado.

</dd> </dl>

Tenga en cuenta que una aplicación que invoca cualquiera de las funciones puede provocar indirectamente que el servidor de espacio de nombres DFS local que da servicio a la llamada de función realice una sincronización completa de los metadatos del espacio de nombres relacionado del maestro del emulador de PDC para ese dominio. Esta sincronización completa puede producirse incluso cuando el modo de escalabilidad raíz está configurado para ese espacio de nombres.
