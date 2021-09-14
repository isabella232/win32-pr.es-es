---
description: La característica de particiones COM+ incluye una caché de particiones. Esta memoria caché almacena asignaciones de usuario a partición y está diseñada para evitar el acceso Active Directory repetitivos.
ms.assetid: 8c3a269d-1933-4df6-aefb-f1f5587f1f42
title: Configuración de la caché de particiones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1389cc2685861e06d1b5c86baf2ad7b5fa9bd038
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126965179"
---
# <a name="configuring-the-partition-cache"></a>Configuración de la caché de particiones

La característica de particiones COM+ incluye una caché de particiones. Esta memoria caché almacena asignaciones de usuario a partición y está diseñada para evitar el acceso Active Directory repetitivos.

## <a name="changing-cache-size"></a>Cambiar el tamaño de la caché

La caché de particiones consta de tres tablas, cuyo tamaño se puede modificar para mejorar el rendimiento. Estas tablas constan del número de entradas de SID en la memoria caché, el número de entradas de unidad organizativa en la memoria caché y el número de entradas de partición en la memoria caché.

Para cambiar estos tamaños de tabla, los administradores pueden modificar los valores de una clave del Registro. La clave del Registro y sus valores son los siguientes:

**HKLM \\ SOFTWARE \\ Microsoft \\ COM3 \\ PartitionCache**



| Valores clave                         | Descripción                                                                                                                                                                                                                                                                                                                                                                                                  |
|------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **NumSidEntries**<br/>       | Contiene el valor REG DWORD para el número de entradas de SID en la \_ memoria caché (default=512). Este valor debe establecerse en un valor mayor que el número de identidades únicas que una máquina va a atender en el período de tiempo de invalidación de caché.<br/>                                                                                                                                                  |
| **NumNameEntries**<br/>      | Contiene el valor REG \_ DWORD para el número de entradas de nombre de unidad organizativa en la memoria caché (default=64). Este valor debe establecerse en un valor mayor que el número de nombres de unidad organizativa únicos que una máquina va a atender en el período de tiempo de invalidación de caché.<br/>                                                                                                                                                 |
| **NumPartitionEntries**<br/> | Contiene el valor \_ REG DWORD para el número de entradas de partición en la memoria caché (default=1024).<br/> En el período de tiempo de invalidación de caché, el valor DWORD debe establecerse en un número mayor que el número de particiones únicas que va a atender una máquina. Esto se debe a que el contexto de un componente puede incluir un identificador de partición para una partición que no reside en esa máquina. <br/> |
| **EntryExpiration**<br/>     | Contiene el valor REG DWORD para el recuento de tics (cada paso = ~7 minutos) hasta que una entrada de caché deja de ser válida \_ (default=4 (~28 minutos)).<br/>                                                                                                                                                                                                                                                          |



 

## <a name="flushing-the-cache"></a>Vaciar la memoria caché

Dado que COM+ almacena en caché la partición predeterminada para los usuarios, es posible que desee llamar a este método después de cambiar la partición predeterminada para un usuario de la Active Directory. Los administradores pueden hacerlo mediante programación llamando al [**método FlushPartitionCache.**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-flushpartitioncache)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Recopilación de métricas de partición](collecting-partition-metrics.md)
</dt> <dt>

[Agrupación de aplicaciones en particiones](grouping-applications-into-partitions.md)
</dt> <dt>

[Administración de particiones locales](managing-local-partitions.md)
</dt> <dt>

[Administración de particiones en Active Directory](managing-partitions-within-active-directory.md)
</dt> <dt>

[Establecer derechos administrativos para una partición](setting-administrative-rights-for-a-partition.md)
</dt> </dl>

 

 




