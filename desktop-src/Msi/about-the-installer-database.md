---
description: La base de datos de Windows Installer se compone de muchas tablas interrelacionadas que forman una base de datos relacional de la información necesaria para instalar un grupo de aplicaciones.
ms.assetid: 3352dd8f-c082-4c4b-98be-5823c8b28f07
title: Acerca de la base de datos del instalador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7f0ee2cc326f85d964ac3d845b97751a48fbb91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909153"
---
# <a name="about-the-installer-database"></a>Acerca de la base de datos del instalador

La base de datos de Windows Installer se compone de muchas tablas interrelacionadas que forman una base de datos relacional de la información necesaria para instalar un grupo de aplicaciones. Dado que la base de datos es relacional, las tablas se vinculan a través de los datos de los valores de clave principal y de clave externa. Esto proporciona un método eficaz para cambiar el proceso de instalación y significa que los usuarios pueden personalizar más fácilmente una aplicación grande o un grupo de aplicaciones. Las tablas de base de datos reflejan el diseño general de todo el grupo de aplicaciones, entre las que se incluyen:

-   Características disponibles
-   Componentes
-   Relación entre características y componentes
-   Configuración necesaria del registro
-   Interfaz de usuario para la aplicación

Para crear una base de datos de instalación, debe rellenar las tablas con toda la información sobre las aplicaciones y el proceso de instalación. La creación manual de todas estas tablas se convierte en una tarea grande incluso para una instalación de tamaño moderado. por lo tanto, algunas herramientas de terceros están disponibles para ayudar a crear la base de datos del instalador. En las secciones siguientes se describen los grupos de tablas de bases de datos relacionadas.

[Grupo de tablas principales](core-tables-group.md)

[Grupo de tablas de archivos](file-tables-group.md)

[Grupo de tablas del registro](registry-tables-group.md)

[Grupo tablas del sistema](system-tables-group.md)

[Grupo de tablas de localizador](locator-tables-group.md)

[Grupo de tablas de información de programas](program-information-tables-group.md)

[Grupo de tablas de procedimientos de instalación](installation-procedure-tables-group.md)

[Leyenda de diagrama de relación de entidades](entity-relationship-diagram-legend.md)

[Archivos de archivo de texto](text-archive-files.md)

Para obtener una lista completa de todas las tablas de una base de datos de instalación, vea [tablas de base de datos](database-tables.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Versiones publicadas, herramientas y redistribuibles](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



