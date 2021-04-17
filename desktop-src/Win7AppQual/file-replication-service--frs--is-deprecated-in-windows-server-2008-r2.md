---
description: .
ms.assetid: 18a03469-737a-4905-9851-f7961c46b867
title: El servicio de replicación de archivos (FRS) está en desuso en Windows Server 2008 R2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af3acf7eb6310f2c296abfd5eb1db0f30c4b48dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716130"
---
# <a name="file-replication-service-frs-is-deprecated-in-windows-server-2008-r2"></a>El servicio de replicación de archivos (FRS) está en desuso en Windows Server 2008 R2

## <a name="platform"></a>Plataforma

 **Servidores:** Windows Server 2008 R2  

## <a name="feature-impact"></a>Impacto en las características

 **Gravedad:** Calidad  
**Frecuencia:** Calidad  


## <a name="description"></a>Descripción

En Windows Server 2008 R2, el servicio de replicación de archivos (FRS) no se puede usar para replicar carpetas Sistema de archivos distribuido (DFS) o datos personalizados (no SYSVOL). Un controlador de dominio de Windows Server 2008 R2 puede seguir usando FRS para replicar el contenido del recurso compartido SYSVOL en un dominio que usa FRS para replicar el recurso compartido SYSVOL entre controladores de dominio. Sin embargo, los servidores de Windows Server 2008 R2 no pueden usar FRS para replicar el contenido de ningún conjunto de réplicas aparte del recurso compartido SYSVOL. El servicio Replicación DFS es un sustituto de FRS y se puede usar para replicar el contenido del recurso compartido SYSVOL, carpetas DFS y otros datos personalizados (no SYSVOL). Migre todos los conjuntos de réplicas FRS que no sean de SYSVOL a Replicación DFS. También se recomienda encarecidamente migrar la replicación del recurso compartido SYSVOL de FRS a Replicación DFS porque Replicación DFS es más robusta, escalable y tiene un mejor rendimiento de replicación que FRS.

## <a name="manifestation"></a>Manifestación

La replicación de FRS de datos personalizados se interrumpirá de una actualización en contexto. La única manera de recuperarse de esta situación sería volver a instalar un sistema operativo anterior en el servidor y reinicializar la replicación de FRS. No se permite a los servidores que se han actualizado a Windows Server 2008 R2 participar en grupos de replicación FRS existentes.

## <a name="mitigation-of-impact"></a>Mitigación del impacto

Para evitar problemas que pueden producirse como resultado de estos cambios, migre los conjuntos de replicación FRS personalizados a Replicación DFS. El servicio Replicación DFS tiene muchas ventajas con respecto a FRS, como herramientas de administración mejoradas, mayor rendimiento y administración delegada.

## <a name="links-to-other-resources"></a>Vínculos a otros recursos

-   [FRS Overview](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc754297(v=ws.11))
-   [Replicación del sistema de archivos distribuido: preguntas más frecuentes](/windows-server/storage/dfs-replication/dfsr-faq)
-   [Guía de migración de replicación de SYSVOL: Replicación de FRS a DFS](/windows-server/storage/dfs-replication/migrate-sysvol-to-dfsr)

 

 
