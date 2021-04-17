---
description: La característica de particiones de COM+ incluye una memoria caché de partición. Esta memoria caché almacena las asignaciones de usuario a partición y está diseñado para evitar el acceso repetitivo Active Directory.
ms.assetid: 8c3a269d-1933-4df6-aefb-f1f5587f1f42
title: Configuración de la memoria caché de partición
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1389cc2685861e06d1b5c86baf2ad7b5fa9bd038
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705377"
---
# <a name="configuring-the-partition-cache"></a>Configuración de la memoria caché de partición

La característica de particiones de COM+ incluye una memoria caché de partición. Esta memoria caché almacena las asignaciones de usuario a partición y está diseñado para evitar el acceso repetitivo Active Directory.

## <a name="changing-cache-size"></a>Cambiar el tamaño de la memoria caché

La memoria caché de particiones consta de tres tablas, cuyo tamaño se puede modificar para mejorar el rendimiento. Estas tablas constan del número de entradas de SID en la memoria caché, el número de entradas de uo en la memoria caché y el número de entradas de partición en la memoria caché.

Para cambiar estos tamaños de tabla, los administradores pueden modificar los valores de una clave del registro. La clave del registro y sus valores son los siguientes:

**HKLM \\ software \\ Microsoft \\ COM3 \\ PartitionCache**



| Valores clave                         | Descripción                                                                                                                                                                                                                                                                                                                                                                                                  |
|------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **NumSidEntries**<br/>       | Contiene el \_ valor de REG DWORD para el número de entradas de SID en la memoria caché (valor predeterminado = 512). Este valor debe establecerse en un valor mayor que el número de identidades únicas en las que se atenderá una máquina en la ventana de tiempo de invalidación de la memoria caché.<br/>                                                                                                                                                  |
| **NumNameEntries**<br/>      | Contiene el \_ valor de REG DWORD para el número de entradas de nombre de unidad organizativa en la memoria caché (valor predeterminado = 64). Este valor debe establecerse en un valor mayor que el número de nombres de Uo únicos en los que se atenderá un equipo en la ventana de tiempo de invalidación de caché.<br/>                                                                                                                                                 |
| **NumPartitionEntries**<br/> | Contiene el \_ valor de REG DWORD para el número de entradas de partición en la memoria caché (valor predeterminado = 1024).<br/> En la ventana de tiempo de invalidación de caché, el valor DWORD se debe establecer en un número mayor que el número de particiones únicas en las que se atenderá un equipo. Esto se debe a que el contexto de un componente puede incluir un identificador de partición para una partición que no reside en ese equipo. <br/> |
| **EntryExpiration**<br/>     | Contiene el \_ valor de REG DWORD para el recuento de pasos (cada TIC = ~ 7 minutos) hasta que una entrada de caché deja de ser válida (valor predeterminado = 4 (~ 28 minutos)).<br/>                                                                                                                                                                                                                                                          |



 

## <a name="flushing-the-cache"></a>Vaciar la memoria caché

Dado que COM+ almacena en caché la partición predeterminada para los usuarios, es posible que desee llamar a este método después de cambiar la partición predeterminada para un usuario en el Active Directory. Los administradores pueden hacerlo mediante programación llamando al método [**FlushPartitionCache**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-flushpartitioncache) .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Recopilación de métricas de partición](collecting-partition-metrics.md)
</dt> <dt>

[Agrupar aplicaciones en particiones](grouping-applications-into-partitions.md)
</dt> <dt>

[Administrar particiones locales](managing-local-partitions.md)
</dt> <dt>

[Administrar particiones en Active Directory](managing-partitions-within-active-directory.md)
</dt> <dt>

[Establecer derechos administrativos para una partición](setting-administrative-rights-for-a-partition.md)
</dt> </dl>

 

 




