---
title: Funciones de Sistema de archivos distribuido
description: A continuación se muestran las funciones de Sistema de archivos distribuido (DFS).
ms.assetid: 8f86b717-fe26-4550-8b71-8f7df5ca6022
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 463c085115f6d3e88f9a3be80a890caa0aacb340
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496577"
---
# <a name="distributed-file-system-functions"></a>Funciones de Sistema de archivos distribuido

A continuación se muestran las funciones de Sistema de archivos distribuido (DFS).

## <a name="in-this-section"></a>En esta sección

<dl> <dt>

[NetDfsAdd](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsadd)
</dt> <dd>
Crea un nuevo vínculo de Sistema de archivos distribuido (DFS) o agrega destinos a un vínculo existente en un espacio de nombres DFS.

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
Crea un nuevo espacio de nombres de Sistema de archivos distribuido independiente (DFS).

</dd> <dt>

[NetDfsEnum](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsenum)
</dt> <dd>
Enumera los espacios de nombres de Sistema de archivos distribuido (DFS) hospedados en un servidor o vínculos DFS de un espacio de nombres hospedado por un servidor.

</dd> <dt>

[NetDfsGetClientInfo](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetclientinfo)
</dt> <dd>
Recupera información acerca de una raíz o un vínculo de Sistema de archivos distribuido (DFS) de la memoria caché mantenida por el cliente DFS.

</dd> <dt>

[NetDfsGetFtContainerSecurity](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetftcontainersecurity)
</dt> <dd>
Recupera el descriptor de seguridad del objeto contenedor de los espacios de nombres DFS basados en dominio en el dominio de Active Directory especificado.

</dd> <dt>

[NetDfsGetInfo](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetinfo)
</dt> <dd>
Recupera información sobre una raíz o un vínculo de Sistema de archivos distribuido (DFS) especificado en un espacio de nombres DFS.

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
Cambia el nombre de un vínculo DFS o lo mueve.

</dd> <dt>

[NetDfsRemove](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsremove)
</dt> <dd>
Quita un vínculo de Sistema de archivos distribuido (DFS) o un destino de vínculo específico de un vínculo DFS en un espacio de nombres DFS. Al quitar un destino de vínculo específico, se quita el vínculo en sí si se quita el último destino de vínculo del vínculo.

</dd> <dt>

[NetDfsRemoveFtRoot](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsremoveftroot)
</dt> <dd>
Quita el destino de raíz especificado de un espacio de nombres de Sistema de archivos distribuido basado en dominio (DFS). Si se quita el último destino raíz del espacio de nombres DFS, la función también elimina el espacio de nombres DFS. Se puede eliminar un espacio de nombres DFS sin eliminar primero todos los vínculos que contiene.

</dd> <dt>

[NetDfsRemoveFtRootForced](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsremoveftrootforced)
</dt> <dd>
Quita el destino de raíz especificado de un espacio de nombres de Sistema de archivos distribuido basado en dominio (DFS), incluso si el servidor de destino raíz está sin conexión. Si se quita el último destino raíz del espacio de nombres DFS, la función también elimina el espacio de nombres DFS. Se puede eliminar un espacio de nombres DFS sin eliminar primero todos los vínculos que contiene.

> [!Note]
> La función [**NetDfsRemoveFtRootForced**](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsremoveftrootforced) no actualiza el registro en el servidor de destino raíz DFS. Para obtener más información, vea la sección Comentarios.

</dd> <dt>

[NetDfsRemoveRootTarget](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsremoveroottarget)
</dt> <dd>
Quita un destino de raíz DFS de un espacio de nombres DFS basado en dominio. Si el destino raíz es el último destino raíz en el espacio de nombres DFS, esta función quita el espacio de nombres DFS. Esta función también se puede usar para quitar un espacio de nombres DFS independiente.

</dd> <dt>

[NetDfsRemoveStdRoot](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsremovestdroot)
</dt> <dd>
Elimina un espacio de nombres de Sistema de archivos distribuido independiente (DFS).

</dd> <dt>

[NetDfsSetClientInfo](/windows/desktop/api/lmdfs/nf-lmdfs-netdfssetclientinfo)
</dt> <dd>
Modifica información acerca de una raíz o un vínculo de Sistema de archivos distribuido (DFS) en la caché mantenido por el cliente DFS.

</dd> <dt>

[NetDfsSetFtContainerSecurity](/windows/desktop/api/lmdfs/nf-lmdfs-netdfssetftcontainersecurity)
</dt> <dd>
Establece el descriptor de seguridad del objeto contenedor de los espacios de nombres DFS basados en dominio en el dominio de Active Directory especificado.

</dd> <dt>

[NetDfsSetInfo](/windows/desktop/api/lmdfs/nf-lmdfs-netdfssetinfo)
</dt> <dd>
Establece o modifica la información sobre una raíz específica del Sistema de archivos distribuido (DFS), el destino de la raíz, el vínculo o el destino del vínculo.

</dd> <dt>

[NetDfsSetSecurity](/windows/desktop/api/lmdfs/nf-lmdfs-netdfssetsecurity)
</dt> <dd>
Establece el descriptor de seguridad para el objeto raíz del espacio de nombres DFS especificado.

</dd> <dt>

[NetDfsSetStdContainerSecurity](/windows/desktop/api/lmdfs/nf-lmdfs-netdfssetstdcontainersecurity)
</dt> <dd>
Establece el descriptor de seguridad para el objeto contenedor del espacio de nombres DFS independiente especificado.

</dd> </dl>

Tenga en cuenta que una aplicación que invoca cualquiera de las funciones puede hacer que el servidor de espacio de nombres DFS local que atiende a la llamada de función realice una sincronización completa de los metadatos de espacio de nombres relacionados desde el maestro de emulador de PDC para ese dominio. Esta sincronización completa puede producirse incluso cuando se configura el modo de escalabilidad de raíz para ese espacio de nombres.
