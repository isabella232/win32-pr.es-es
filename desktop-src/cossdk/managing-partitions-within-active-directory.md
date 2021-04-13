---
description: Como alternativa a la administración de particiones Active Directory a través de la herramienta administrativa usuarios y equipos Active Directory, puede administrar particiones COM+ mediante programación a través del uso de un conjunto de objetos COM+ en Active Directory interfaz del sistema (ADSI).
ms.assetid: 915b4643-cbda-433a-a383-65a6b0fd0874
title: Administrar particiones en Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6635e49b7d2833a1e6e177c25f9f2fb05ff0dff4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539285"
---
# <a name="managing-partitions-within-active-directory"></a>Administrar particiones en Active Directory

Como alternativa a la administración de particiones Active Directory a través de la herramienta administrativa usuarios y equipos Active Directory, puede administrar particiones COM+ mediante programación a través del uso de un conjunto de objetos COM+ en Active Directory interfaz del sistema (ADSI).

Independientemente de la técnica administrativa que elija para administrar particiones COM+, hay una secuencia general de pasos que deben seguir los administradores:

1.  Cree las nuevas particiones COM+ en Active Directory para el dominio.
2.  Crear conjuntos de particiones COM+ en Active Directory y asignarlos a las particiones COM+ recién creadas.
3.  Configure las particiones de Active Directory en el equipo local con el objeto COM+ adecuado. Al configurar una partición de Active Directory en un equipo local, se crea automáticamente una carpeta de **aplicaciones com+** en esa carpeta de partición.
4.  Instale las aplicaciones COM+ en las particiones COM+ apropiadas.

Todos los pasos anteriores se pueden realizar mediante programación, mediante un conjunto de interfaces de Active Directory denominadas ADSI. Los objetos disponibles para administrar las particiones que están disponibles en ADSI son los siguientes:

-   \_nombre de USERPARTITIONSETLINK de DS \_
-   \_nombre de PARTITIONLINK de DS \_
-   nombre de DS \_ objectId \_
-   \_nombre de DEFAULTPARTITIONLINK de DS \_
-   \_nombre de USERLINK de DS \_
-   \_nombre de PARTITIONSET de DS \_
-   \_nombre de partición de DS \_

Para obtener información sobre cómo crear y administrar particiones COM+ mediante el uso de las herramientas administrativas Active Directory usuarios y equipos y servicios de componentes, vea la ayuda en pantalla disponible en cada herramienta.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Recopilación de métricas de partición](collecting-partition-metrics.md)
</dt> <dt>

[Configuración de la memoria caché de partición](configuring-the-partition-cache.md)
</dt> <dt>

[Agrupar aplicaciones en particiones](grouping-applications-into-partitions.md)
</dt> <dt>

[Administrar particiones locales](managing-local-partitions.md)
</dt> <dt>

[Establecer derechos administrativos para una partición](setting-administrative-rights-for-a-partition.md)
</dt> </dl>

 

 



