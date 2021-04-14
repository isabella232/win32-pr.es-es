---
description: A continuación se muestran las Sistema de archivos distribuido estructuras DFS
ms.assetid: f55ad3c0-0457-4d5a-a7d3-8eff744d573d
title: Sistema de archivos distribuido estructuras
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42fc3351402c4721952cbfc4dc3fe3c6ac6d3a76
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496582"
---
# <a name="distributed-file-system-structures"></a>Sistema de archivos distribuido estructuras

A continuación se muestran las estructuras Sistema de archivos distribuido (DFS):

## <a name="in-this-section"></a>En esta sección

<dl> <dt>

[**DFS_GET_PKT_ENTRY_STATE_ARG**](/windows/win32/api/lmdfs/ns-lmdfs-dfs_get_pkt_entry_state_arg)
</dt> <dd>

Búfer de entrada utilizado con el código de control de [**FSCTL_DFS_GET_PKT_ENTRY_STATE**](fsctl-dfs-get-pkt-entry-state.md)
</dd> <dt>

[Estructura de _DFS_INFO_1](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_1)
</dt> <dd>
Contiene el nombre de una raíz o vínculo de Sistema de archivos distribuido (DFS).

</dd> <dt>

[Estructura de _DFS_INFO_2](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_2)
</dt> <dd>
Contiene información acerca de un vínculo o una raíz de Sistema de archivos distribuido (DFS). Esta estructura contiene el nombre, el estado y el número de destinos DFS para la raíz o el vínculo.

</dd> <dt>

[Estructura de _DFS_INFO_3](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_3)
</dt> <dd>
Contiene información acerca de un vínculo o una raíz de Sistema de archivos distribuido (DFS). Esta estructura contiene el nombre, el estado, el número de destinos DFS e información sobre cada destino de la raíz o vínculo.

</dd> <dt>

[Estructura de _DFS_INFO_4](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_4)
</dt> <dd>
Contiene información acerca de un vínculo o una raíz de Sistema de archivos distribuido (DFS). Esta estructura contiene el nombre, el estado, el **GUID**, el tiempo de espera, el número de destinos e información sobre cada destino de la raíz o el vínculo.

</dd> <dt>

[Estructura de _DFS_INFO_5](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_5)
</dt> <dd>
Contiene información acerca de un vínculo o una raíz de Sistema de archivos distribuido (DFS). Esta estructura contiene el nombre, el estado, el **GUID**, el tiempo de espera, las propiedades de espacio de nombres/raíz/vínculo, el tamaño de los metadatos y el número de destinos para la raíz o el vínculo.

</dd> <dt>

[Estructura de _DFS_INFO_6](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_6)
</dt> <dd>
Contiene información acerca de un vínculo o una raíz de Sistema de archivos distribuido (DFS). Esta estructura contiene el nombre, el estado, el **GUID**, el tiempo de espera, las propiedades de espacio de nombres/raíz/vínculo, el tamaño de los metadatos, el número de destinos e información sobre cada destino de la raíz o el vínculo.

</dd> <dt>

[Estructura de _DFS_INFO_7](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_7)
</dt> <dd>
Contiene información sobre un espacio de nombres DFS. Esta estructura contiene el **GUID** de la versión de los metadatos para el espacio de nombres.

</dd> <dt>

[Estructura de _DFS_INFO_8](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_8)
</dt> <dd>
Contiene el nombre, el estado, el **GUID**, el tiempo de espera, las marcas de propiedad, el tamaño de los metadatos, la información de destino DFS y el descriptor de seguridad del punto de análisis de vínculos para una raíz o vínculo.

</dd> <dt>

[Estructura de _DFS_INFO_9](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_9)
</dt> <dd>
Contiene el nombre, el estado, el **GUID**, el tiempo de espera, las marcas de propiedad, el tamaño de los metadatos, la información de destino DFS, el descriptor de seguridad del punto de reanálisis de vínculos y una lista de destinos DFS para un vínculo o raíz.

</dd> <dt>

[Estructura de _DFS_INFO_50](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_50)
</dt> <dd>
Contiene la versión de metadatos de DFS y las capacidades de un espacio de nombres DFS existente.

</dd> <dt>

[Estructura de _DFS_INFO_100](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_100)
</dt> <dd>
Contiene un comentario asociado a una raíz o vínculo de Sistema de archivos distribuido (DFS).

</dd> <dt>

[Estructura de _DFS_INFO_101](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_101)
</dt> <dd>
Describe el estado de almacenamiento en una raíz DFS, un vínculo, un destino raíz o un destino de vínculo.

</dd> <dt>

[Estructura de _DFS_INFO_102](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_102)
</dt> <dd>
Contiene un valor de tiempo de espera para asociar a una raíz de Sistema de archivos distribuido (DFS) o un vínculo en una raíz DFS con nombre.

</dd> <dt>

[Estructura de _DFS_INFO_103](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_103)
</dt> <dd>
Contiene propiedades que establecen comportamientos específicos para una raíz o vínculo DFS.

</dd> <dt>

[Estructura de _DFS_INFO_104](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_104)
</dt> <dd>
Contiene la prioridad de un destino de raíz DFS o destino de vínculo.

</dd> <dt>

[Estructura de _DFS_INFO_105](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_105)
</dt> <dd>
Contiene información sobre una raíz o vínculo DFS, incluidos los comportamientos de comentario, estado, tiempo de espera y DFS especificados por las marcas de propiedades.

</dd> <dt>

[Estructura de _DFS_INFO_106](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_106)
</dt> <dd>
Contiene el estado y la prioridad de almacenamiento de un destino de raíz DFS o destino de vínculo. Esta estructura solo se usa con la función [**NetDfsSetInfo**](netdfssetinfo.md) .

</dd> <dt>

[Estructura de _DFS_INFO_107](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_107)
</dt> <dd>
Contiene información acerca de una raíz o vínculo DFS, incluidos los comentarios, el estado, el tiempo de espera, las marcas de propiedad y el descriptor de seguridad del punto de reanálisis de vínculos.

</dd> <dt>

[Estructura de _DFS_INFO_150](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_150)
</dt> <dd>
Contiene el descriptor de seguridad para el punto de reanálisis de un vínculo DFS.

</dd> <dt>

[Estructura de _DFS_INFO_200](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_200)
</dt> <dd>
Contiene el nombre de un espacio de nombres de Sistema de archivos distribuido basado en dominio (DFS).

</dd> <dt>

[Estructura de _DFS_INFO_300](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_300)
</dt> <dd>
Contiene el nombre y el tipo (basado en dominio o independiente) de un espacio de nombres DFS.

</dd> <dt>

[Estructura de _DFS_STORAGE_INFO](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_storage_info)
</dt> <dd>
Contiene información acerca de un destino de vínculo o raíz DFS en un espacio de nombres DFS o desde la memoria caché mantenida por el cliente DFS.

</dd> <dt>

[Estructura de _DFS_STORAGE_INFO_1](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_storage_info_1)
</dt> <dd>
Contiene información sobre un destino DFS, incluido el nombre del servidor de destino DFS y el nombre del recurso compartido, así como el estado y la prioridad del destino.

</dd> <dt>

[Estructura de _DFS_SUPPORTED_NAMESPACE_VERSION_INFO](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_supported_namespace_version_info)
</dt> <dd>
Contiene información de versión de un espacio de nombres DFS.

</dd> <dt>

[Estructura de _DFS_TARGET_PRIORITY](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_target_priority)
</dt> <dd>
Contiene la clase de prioridad y el rango de un destino DFS específico.

</dd> </dl>
