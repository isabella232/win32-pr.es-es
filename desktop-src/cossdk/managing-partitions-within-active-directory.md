---
description: Como alternativa a la administración de particiones Active Directory a través de la herramienta administrativa Usuarios y equipos de Active Directory, puede administrar particiones COM+ mediante programación mediante el uso de un conjunto de objetos COM+ dentro de Active Directory System Interface (ADSI).
ms.assetid: 915b4643-cbda-433a-a383-65a6b0fd0874
title: Administración de particiones dentro de Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a87c0aebc9ca52dee005a0343e504756e3e117c3e012098e529fb6d52033428f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120070585"
---
# <a name="managing-partitions-within-active-directory"></a>Administración de particiones dentro de Active Directory

Como alternativa a la administración de particiones Active Directory a través de la herramienta administrativa Usuarios y equipos de Active Directory, puede administrar particiones COM+ mediante programación mediante el uso de un conjunto de objetos COM+ dentro de Active Directory System Interface (ADSI).

Independientemente de la técnica administrativa que elija para administrar particiones COM+, hay una secuencia general de pasos que los administradores deben seguir:

1.  Cree las nuevas particiones COM+ Active Directory para el dominio.
2.  Cree conjuntos de particiones COM+ Active Directory y asízcátelos a las particiones COM+ recién creadas.
3.  Configure las Active Directory en el equipo local, mediante el objeto COM+ adecuado. Al configurar una partición Active Directory en un equipo local, se crea automáticamente una carpeta **aplicaciones COM+** en esa carpeta de partición.
4.  Instale las aplicaciones COM+ en las particiones COM+ adecuadas.

Todos los pasos anteriores se pueden realizar mediante programación, mediante un conjunto de interfaces Active Directory llamadas ADSI. Los objetos disponibles para administrar particiones que están disponibles en ADSI son los siguientes:

-   NOMBRE \_ DE VÍNCULO USERPARTITIONSET DE DS \_
-   NOMBRE DEL VÍNCULO \_ DE PARTICIÓN DE DS \_
-   NOMBRE DE OBJECTID de DS \_ \_
-   NOMBRE \_ DEFAULTPARTITIONLINK DE DS \_
-   NOMBRE DE VÍNCULO DE USUARIO DE DS \_ \_
-   NOMBRE DEL \_ CONJUNTO DE PARTICIONES DE DS \_
-   NOMBRE DE PARTICIÓN DE DS \_ \_

Para obtener información sobre cómo crear y administrar particiones COM+ mediante el uso de las herramientas administrativas Usuarios y equipos de Active Directory y Servicios de componentes, consulte la ayuda en línea disponible desde dentro de cada herramienta.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Recopilación de métricas de partición](collecting-partition-metrics.md)
</dt> <dt>

[Configuración de la caché de particiones](configuring-the-partition-cache.md)
</dt> <dt>

[Agrupación de aplicaciones en particiones](grouping-applications-into-partitions.md)
</dt> <dt>

[Administración de particiones locales](managing-local-partitions.md)
</dt> <dt>

[Establecer derechos administrativos para una partición](setting-administrative-rights-for-a-partition.md)
</dt> </dl>

 

 



