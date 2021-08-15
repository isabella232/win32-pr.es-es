---
description: A continuación se muestra Sistema de archivos distribuido estructuras DFS
ms.assetid: f55ad3c0-0457-4d5a-a7d3-8eff744d573d
title: Sistema de archivos distribuido estructuras
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab1561a4586cc03304c6aa1c1e323eb42fd09766df0cc3c7210636367337873a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118541286"
---
# <a name="distributed-file-system-structures"></a>Sistema de archivos distribuido estructuras

Estas son las estructuras Sistema de archivos distribuido (DFS):

## <a name="in-this-section"></a>En esta sección

<dl> <dt>

[**DFS_GET_PKT_ENTRY_STATE_ARG**](/windows/win32/api/lmdfs/ns-lmdfs-dfs_get_pkt_entry_state_arg)
</dt> <dd>

Búfer de entrada usado con el [**FSCTL_DFS_GET_PKT_ENTRY_STATE**](fsctl-dfs-get-pkt-entry-state.md) de control de entrada
</dd> <dt>

[_DFS_INFO_1 estructura](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_1)
</dt> <dd>
Contiene el nombre de una raíz Sistema de archivos distribuido (DFS) o vínculo.

</dd> <dt>

[_DFS_INFO_2 estructura](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_2)
</dt> <dd>
Contiene información sobre una raíz Sistema de archivos distribuido (DFS) o un vínculo. Esta estructura contiene el nombre, el estado y el número de destinos DFS para la raíz o el vínculo.

</dd> <dt>

[_DFS_INFO_3 estructura](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_3)
</dt> <dd>
Contiene información sobre una raíz Sistema de archivos distribuido (DFS) o un vínculo. Esta estructura contiene el nombre, el estado, el número de destinos DFS e información sobre cada destino de la raíz o vínculo.

</dd> <dt>

[_DFS_INFO_4 estructura](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_4)
</dt> <dd>
Contiene información sobre una raíz Sistema de archivos distribuido (DFS) o un vínculo. Esta estructura contiene el nombre, el estado, **el GUID,** el tiempo de espera, el número de destinos y la información sobre cada destino de la raíz o vínculo.

</dd> <dt>

[_DFS_INFO_5 estructura](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_5)
</dt> <dd>
Contiene información sobre una raíz Sistema de archivos distribuido (DFS) o un vínculo. Esta estructura contiene el nombre, el estado, **el GUID,** el tiempo de espera, las propiedades namespace/root/link, el tamaño de los metadatos y el número de destinos para la raíz o el vínculo.

</dd> <dt>

[_DFS_INFO_6 estructura](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_6)
</dt> <dd>
Contiene información sobre una raíz Sistema de archivos distribuido (DFS) o un vínculo. Esta estructura contiene el nombre, el estado, **el GUID,** el tiempo de espera, las propiedades de espacio de nombres, raíz o vínculo, el tamaño de los metadatos, el número de destinos y la información sobre cada destino de la raíz o vínculo.

</dd> <dt>

[_DFS_INFO_7 estructura](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_7)
</dt> <dd>
Contiene información sobre un espacio de nombres DFS. Esta estructura contiene el **GUID de versión para** los metadatos del espacio de nombres .

</dd> <dt>

[_DFS_INFO_8 estructura](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_8)
</dt> <dd>
Contiene el nombre, el estado, **el GUID,** el tiempo de espera, las marcas de propiedad, el tamaño de los metadatos, la información de destino DFS y el descriptor de seguridad del punto de reanción de vínculos para una raíz o vínculo.

</dd> <dt>

[_DFS_INFO_9 estructura](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_9)
</dt> <dd>
Contiene el nombre, el estado, **el GUID,** el tiempo de espera, las marcas de propiedad, el tamaño de los metadatos, la información de destino DFS, el descriptor de seguridad del punto de reanción de vínculos y una lista de destinos DFS para una raíz o vínculo.

</dd> <dt>

[_DFS_INFO_50 estructura](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_50)
</dt> <dd>
Contiene la versión de metadatos DFS y las funcionalidades de un espacio de nombres DFS existente.

</dd> <dt>

[_DFS_INFO_100 estructura](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_100)
</dt> <dd>
Contiene un comentario asociado a una raíz Sistema de archivos distribuido (DFS) o un vínculo.

</dd> <dt>

[_DFS_INFO_101 estructura](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_101)
</dt> <dd>
Describe el estado del almacenamiento en una raíz DFS, un vínculo, un destino raíz o un destino de vínculo.

</dd> <dt>

[_DFS_INFO_102 estructura](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_102)
</dt> <dd>
Contiene un valor de tiempo de espera para asociarlo a una raíz Sistema de archivos distribuido (DFS) o a un vínculo en una raíz DFS con nombre.

</dd> <dt>

[_DFS_INFO_103 estructura](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_103)
</dt> <dd>
Contiene propiedades que establecen comportamientos específicos para una raíz o vínculo DFS.

</dd> <dt>

[_DFS_INFO_104 estructura](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_104)
</dt> <dd>
Contiene la prioridad de un destino raíz DFS o un destino de vínculo.

</dd> <dt>

[_DFS_INFO_105 estructura](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_105)
</dt> <dd>
Contiene información sobre una raíz o vínculo DFS, incluidos los comportamientos de comentario, estado, tiempo de espera y DFS especificados por marcas de propiedad.

</dd> <dt>

[_DFS_INFO_106 estructura](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_106)
</dt> <dd>
Contiene el estado de almacenamiento y la prioridad de un destino raíz DFS o un destino de vínculo. Esta estructura solo se usa con la [**función NetDfsSetInfo.**](netdfssetinfo.md)

</dd> <dt>

[_DFS_INFO_107 estructura](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_107)
</dt> <dd>
Contiene información sobre una raíz o vínculo DFS, incluidos el comentario, el estado, el tiempo de espera, las marcas de propiedad y el descriptor de seguridad del punto de reanción de vínculos.

</dd> <dt>

[_DFS_INFO_150 estructura](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_150)
</dt> <dd>
Contiene el descriptor de seguridad para el punto de rean aproximado de un vínculo DFS.

</dd> <dt>

[_DFS_INFO_200 estructura](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_200)
</dt> <dd>
Contiene el nombre de un espacio de nombres Sistema de archivos distribuido basado en dominio (DFS).

</dd> <dt>

[_DFS_INFO_300 estructura](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_300)
</dt> <dd>
Contiene el nombre y el tipo (basado en dominio o independiente) de un espacio de nombres DFS.

</dd> <dt>

[_DFS_STORAGE_INFO estructura](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_storage_info)
</dt> <dd>
Contiene información sobre una raíz DFS o un destino de vínculo en un espacio de nombres DFS o desde la memoria caché mantenida por el cliente DFS.

</dd> <dt>

[_DFS_STORAGE_INFO_1 estructura](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_storage_info_1)
</dt> <dd>
Contiene información sobre un destino DFS, incluidos el nombre del servidor de destino DFS y el nombre del recurso compartido, así como el estado y la prioridad del destino.

</dd> <dt>

[_DFS_SUPPORTED_NAMESPACE_VERSION_INFO estructura](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_supported_namespace_version_info)
</dt> <dd>
Contiene información de versión para un espacio de nombres DFS.

</dd> <dt>

[_DFS_TARGET_PRIORITY estructura](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_target_priority)
</dt> <dd>
Contiene la clase de prioridad y el rango de un destino DFS específico.

</dd> </dl>
