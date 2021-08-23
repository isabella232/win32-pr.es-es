---
description: Recopilación de métricas de partición
ms.assetid: 2dc35011-24fa-49df-9cf8-96db2de39efa
title: Recopilación de métricas de partición
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8168972a0bac0b4eb79c5adde3530d1a0673469adff6b66b4c1b31cc6446bca2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047693"
---
# <a name="collecting-partition-metrics"></a>Recopilación de métricas de partición

En algunos casos, es posible que una organización quiera recopilar información sobre el uso de aplicaciones COM+ con fines de supervisión, planeamiento de capacidad y contabilidad de recursos.

Por ejemplo, un proveedor de servicios de aplicaciones (ASP) podría querer cobrar a un cliente por su uso de recursos. Para ello, COM+ permite recopilar información de eventos y métricas por partición.

La manera de recopilar esta información para una partición específica es especificando, para cada interfaz de instrumentación com+, el miembro de identificador de partición dentro de la estructura de eventos estándar. La estructura de eventos es el primer valor de una interfaz de instrumentación COM+. Para obtener más información, [vea Interfaces de instrumentación de COM+.](com--instrumentation-interfaces.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Configuración de la caché de particiones](configuring-the-partition-cache.md)
</dt> <dt>

[Agrupación de aplicaciones en particiones](grouping-applications-into-partitions.md)
</dt> <dt>

[Administración de particiones locales](managing-local-partitions.md)
</dt> <dt>

[Administración de particiones dentro de Active Directory](managing-partitions-within-active-directory.md)
</dt> <dt>

[Establecer derechos administrativos para una partición](setting-administrative-rights-for-a-partition.md)
</dt> </dl>

 

 



