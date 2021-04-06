---
description: Para obtener más información sobre el diagrama siguiente, vea la leyenda del diagrama de relaciones de entidades.
ms.assetid: ec4f585d-cbd5-4c25-aaf4-1c1333fd4587
title: Grupo de tablas principales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5a5cc87e80c60505025825353272699db574bd1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002858"
---
# <a name="core-tables-group"></a>Grupo de tablas principales

Para obtener más información sobre el diagrama siguiente, vea la [leyenda del diagrama de relaciones de entidades](entity-relationship-diagram-legend.md).

![Grupo de tablas principales](images/core.png)

El grupo principal consta de tablas que describen las características y los componentes fundamentales de la aplicación y el paquete del instalador. Por lo tanto, los desarrolladores de paquetes de instalación deben considerar cómo rellenar estas tablas en primer lugar, ya que la organización de gran parte de la base de datos se verá patente del contenido de este grupo.

-   En la [tabla de características](feature-table.md) se enumeran todas las características que pertenecen a la aplicación.
-   La [tabla de condiciones](condition-table.md) contiene las expresiones condicionales que determinan si se va a instalar una característica determinada.
-   En la [tabla FeatureComponents](featurecomponents-table.md) se describen los componentes que pertenecen a cada característica.
-   En la [tabla componente](component-table.md) se enumeran todos los componentes que pertenecen a la instalación.
-   En la [tabla directorio](directory-table.md) se enumeran los directorios que son necesarios durante la instalación. Dado que cada componente debe estar asociado a un solo directorio, la tabla de componentes está estrechamente relacionada con esta tabla y tiene una clave externa en la tabla de directorio.
-   En la [tabla PublishComponent](publishcomponent-table.md) se enumeran las características y los componentes que se publican para su uso por parte de otras aplicaciones. Los [componentes y las características](components-and-features.md) son los dos tipos de anuncios de características.
-   La [tabla MsiAssembly](msiassembly-table.md) especifica Windows Installer valores de .NET Framework ensamblados Common Language Runtime y ensamblados Win32.
-   La [tabla MsiAssemblyName](msiassemblyname-table.md) especifica el esquema de los elementos de un nombre de caché de ensamblados seguro para un ensamblado de Common Language Runtime o Win32.
-   La [tabla ComPlus](complus-table.md) contiene información necesaria para instalar aplicaciones com+.
-   La [tabla IsolatedComponent](isolatedcomponent-table.md) asocia el componente especificado en la columna de aplicación de componentes \_ (normalmente un archivo. exe) con el componente especificado en la \_ columna compartida componente (normalmente, un archivo dll compartido).
-   La [tabla de actualización](upgrade-table.md) contiene información necesaria durante las [actualizaciones principales](major-upgrades.md).

 

 



