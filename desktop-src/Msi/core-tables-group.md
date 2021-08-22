---
description: Para obtener más información sobre el diagrama siguiente, vea la leyenda del diagrama de relación de entidad.
ms.assetid: ec4f585d-cbd5-4c25-aaf4-1c1333fd4587
title: Grupo de tablas principales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8a8704a13e71f019e3d0686384057d3f209de06530c97bda6f0a63ff352d4db
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118948549"
---
# <a name="core-tables-group"></a>Grupo de tablas principales

Para obtener más información sobre el diagrama siguiente, vea la leyenda del diagrama [de relación de entidad](entity-relationship-diagram-legend.md).

![grupo de tablas principales](images/core.png)

El grupo principal consta de tablas que describen las características y componentes fundamentales de la aplicación y el paquete del instalador. Por lo tanto, los desarrolladores de paquetes de instalación deben considerar primero cómo rellenar estas tablas porque la organización de gran parte de la base de datos se hará evidente a partir del contenido de este grupo.

-   En [la tabla Características](feature-table.md) se enumeran todas las características que pertenecen a la aplicación.
-   La [tabla Condition](condition-table.md) contiene las expresiones condicionales que determinan si se instalará o no una característica determinada.
-   En [la tabla FeatureComponents](featurecomponents-table.md) se describen los componentes que pertenecen a cada característica.
-   En [la tabla Componente](component-table.md) se enumeran todos los componentes que pertenecen a la instalación.
-   En [la tabla Directorio](directory-table.md) se enumeran los directorios necesarios durante la instalación. Dado que cada componente debe estar asociado a un solo directorio, la tabla Component está estrechamente relacionada con esta tabla y tiene una clave externa a la tabla Directory.
-   En [la tabla PublishComponent se](publishcomponent-table.md) enumeran las características y los componentes que se publican para su uso por parte de otras aplicaciones. [Componentes y características son](components-and-features.md) los dos tipos de anuncios de características.
-   La [tabla MsiAssembly especifica](msiassembly-table.md) Windows installer para .NET Framework ensamblados de Common Language Runtime y ensamblados Win32.
-   La [tabla MsiAssemblyName](msiassemblyname-table.md) especifica el esquema para los elementos de un nombre de caché de ensamblados segura para un ensamblado de Common Language Runtime o Win32.
-   La [tabla Complus contiene](complus-table.md) la información necesaria para instalar aplicaciones COM+.
-   La tabla [IsolatedComponent](isolatedcomponent-table.md) asocia el componente especificado en la columna Aplicación de componentes (normalmente un .exe) con el componente especificado en la columna Component Shared (normalmente un \_ archivo DLL \_ compartido).
-   La [tabla Upgrade contiene](upgrade-table.md) la información necesaria durante las actualizaciones [principales.](major-upgrades.md)

 

 



