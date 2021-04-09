---
description: Recopilación de métricas de partición
ms.assetid: 2dc35011-24fa-49df-9cf8-96db2de39efa
title: Recopilación de métricas de partición
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6467dfb9c891e7ae57505c8ec3815bfa99e49d8a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104152950"
---
# <a name="collecting-partition-metrics"></a>Recopilación de métricas de partición

En algunos casos, es posible que una organización desee recopilar información sobre el uso de aplicaciones COM+ con fines de supervisión, planeamiento de capacidad y contabilidad de recursos.

Por ejemplo, un proveedor de servicios de aplicaciones (ASP) podría querer cobrar un cliente por su uso de recursos. Para ello, COM+ le permite recopilar información de eventos y métricas por partición.

La manera de recopilar esta información para una partición específica es especificando, para cada interfaz de instrumentación de COM+, el miembro de ID. de partición dentro de la estructura de eventos estándar. La estructura de eventos es el primer valor de una interfaz de instrumentación de COM+. Para obtener más información, vea [interfaces de instrumentación de com+](com--instrumentation-interfaces.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Configuración de la memoria caché de partición](configuring-the-partition-cache.md)
</dt> <dt>

[Agrupar aplicaciones en particiones](grouping-applications-into-partitions.md)
</dt> <dt>

[Administrar particiones locales](managing-local-partitions.md)
</dt> <dt>

[Administrar particiones en Active Directory](managing-partitions-within-active-directory.md)
</dt> <dt>

[Establecer derechos administrativos para una partición](setting-administrative-rights-for-a-partition.md)
</dt> </dl>

 

 



