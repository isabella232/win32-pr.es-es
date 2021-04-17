---
description: Agrupar aplicaciones en particiones
ms.assetid: bdfe2428-9769-4bcb-b74e-a141ba67a67e
title: Agrupar aplicaciones en particiones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28b35c726662d7dbe2cf039678ba5cdb4f94eeea
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677243"
---
# <a name="grouping-applications-into-partitions"></a>Agrupar aplicaciones en particiones

A la hora de decidir cómo agrupar las aplicaciones en particiones, los administradores deben tener en cuenta ciertas reglas y restricciones, entre las que se incluyen las siguientes:

-   Una aplicación se puede instalar en una o varias particiones.
-   Solo puede existir una instancia de un componente determinado en una aplicación.

## <a name="public-and-private-components"></a>Componentes públicos y privados

Existen otras restricciones a la hora de decidir cómo agrupar aplicaciones COM+. Estas restricciones se aplican a los componentes públicos y privados dentro de una aplicación. Los componentes de la aplicación generalmente pueden ser públicos o privados. Sin embargo, al agrupar las aplicaciones en particiones, los administradores deben tener en cuenta algunas restricciones en relación con los componentes públicos y privados. En la tabla siguiente se enumeran estas restricciones.



| Si una aplicación es:              | A continuación, los componentes de una partición pueden:                                                                                   |
|------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| Una aplicación de servidor<br/>    | Público y privado.<br/>                                                                                           |
| Una aplicación de biblioteca<br/>   | Solo público. De lo contrario, la aplicación llamadores podría tener los mismos componentes, lo que crearía ambigüedad.<br/> |
| En la partición global<br/> | Solo público. Esto garantiza la compatibilidad con versiones anteriores.<br/>                                                             |



 

## <a name="application-ids"></a>Identificadores de aplicación

Todas las aplicaciones COM+ instaladas en un equipo tienen un identificador de aplicación único. Sin embargo, los nombres de aplicación solo deben ser únicos en una sola partición y no en todo el equipo.

En la tabla siguiente se muestra lo que sucede con el identificador de la aplicación cuando una aplicación se importa en una partición o se exporta desde una partición.



| Si una aplicación es:                                              | Después, el identificador de la aplicación:                    |
|--------------------------------------------------------------------|---------------------------------------------|
| Importado a la partición global<br/>                        | Sigue siendo el mismo<br/>                 |
| Importado a una partición distinta de la partición global<br/> | Cambiado<br/>                       |
| Exportado<br/>                                                | Se incluye en el archivo exportado<br/> |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Recopilación de métricas de partición](collecting-partition-metrics.md)
</dt> <dt>

[Configuración de la memoria caché de partición](configuring-the-partition-cache.md)
</dt> <dt>

[Administrar particiones locales](managing-local-partitions.md)
</dt> <dt>

[Administrar particiones en Active Directory](managing-partitions-within-active-directory.md)
</dt> <dt>

[Establecer derechos administrativos para una partición](setting-administrative-rights-for-a-partition.md)
</dt> </dl>

 

 




