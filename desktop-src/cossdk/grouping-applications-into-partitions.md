---
description: Agrupación de aplicaciones en particiones
ms.assetid: bdfe2428-9769-4bcb-b74e-a141ba67a67e
title: Agrupación de aplicaciones en particiones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28b35c726662d7dbe2cf039678ba5cdb4f94eeea
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160496"
---
# <a name="grouping-applications-into-partitions"></a>Agrupación de aplicaciones en particiones

A la hora de decidir cómo agrupar aplicaciones en particiones, los administradores deben tener en cuenta ciertas reglas y restricciones, incluidas las siguientes:

-   Una aplicación se puede instalar en una o varias particiones.
-   Solo puede existir una instancia de un componente determinado en una aplicación.

## <a name="public-and-private-components"></a>Componentes públicos y privados

Existen otras restricciones al decidir cómo agrupar aplicaciones COM+. Estas restricciones pertenecen a componentes públicos frente a privados dentro de una aplicación. Por lo general, los componentes de la aplicación pueden ser públicos o privados. Sin embargo, al agrupar aplicaciones en particiones, los administradores deben tener en cuenta algunas restricciones en torno a los componentes públicos y privados. En la tabla siguiente se enumeran estas restricciones.



| Si una aplicación es:              | A continuación, los componentes de una partición pueden ser:                                                                                   |
|------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| Una aplicación de servidor<br/>    | Pública y privada.<br/>                                                                                           |
| Una aplicación de biblioteca<br/>   | Solo público. De lo contrario, la aplicación de llamadores podría tener los mismos componentes, lo que crearía ambigüedad.<br/> |
| En la partición global<br/> | Solo público. Esto garantiza la compatibilidad con versiones anteriores.<br/>                                                             |



 

## <a name="application-ids"></a>IDs de aplicación

Cada aplicación COM+ instalada en un equipo tiene un identificador de aplicación único. Sin embargo, los nombres de aplicación solo deben ser únicos dentro de una sola partición y no en todo el equipo.

En la tabla siguiente se muestra lo que sucede con el identificador de aplicación cuando una aplicación se importa en una partición o se exporta desde una partición.



| Si una aplicación es:                                              | A continuación, el identificador de la aplicación:                    |
|--------------------------------------------------------------------|---------------------------------------------|
| Importado a la partición global<br/>                        | Sigue siendo el mismo<br/>                 |
| Importado a una partición que no sea la partición global<br/> | Se ha cambiado<br/>                       |
| Exportado<br/>                                                | Se incluye en el archivo exportado.<br/> |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Recopilación de métricas de partición](collecting-partition-metrics.md)
</dt> <dt>

[Configuración de la caché de particiones](configuring-the-partition-cache.md)
</dt> <dt>

[Administración de particiones locales](managing-local-partitions.md)
</dt> <dt>

[Administración de particiones dentro de Active Directory](managing-partitions-within-active-directory.md)
</dt> <dt>

[Establecer derechos administrativos para una partición](setting-administrative-rights-for-a-partition.md)
</dt> </dl>

 

 




