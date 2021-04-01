---
description: El Grupo registro de tablas Windows Installer contiene información sobre las entradas del registro.
ms.assetid: 31a75c20-79e4-4bcf-bcc1-34a7d191fa90
title: Grupo de tablas del registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8ba14bdc2bc5668ce2de3ec66172c75c176ab41
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909454"
---
# <a name="registry-tables-group"></a>Grupo de tablas del registro

![Grupo de tablas del registro](images/registry.png)

Para obtener más información sobre este diagrama, vea la [leyenda del diagrama de relaciones de entidades](entity-relationship-diagram-legend.md).

El instalador tiene tablas específicas para los diferentes tipos de entradas del registro. Al rellenar el grupo de tablas del registro, es importante intentar minimizar el número de entradas que se incluyen en la [tabla del registro](registry-table.md) y maximizar el uso de las demás tablas del registro específicas. Esto se debe a que el instalador no puede distinguir entre diferentes tipos de entradas del registro en la tabla del registro y no puede usar la lógica interna necesaria para sacar el máximo partido de todas las características del instalador, como [*publicidad*](a-gly.md). La creación de entradas del registro relacionadas con COM y Shell de este modo también proporciona una organización más lógica y puede ayudar a minimizar el registro erróneo de información del servidor COM.

En la ilustración se muestra el grupo de entradas del registro de tablas, así como la [tabla de componentes](component-table.md), la [tabla de características](feature-table.md)y la tabla de [archivos](file-table.md). Aunque esto último no implica directamente el rellenado del registro, se incluyen en la figura porque son esenciales para la lógica del grupo de entradas del registro.

El grupo de entradas del registro contiene las siguientes tablas de entradas específicas del registro.

-   La [tabla de extensión](extension-table.md) contiene todas las extensiones de nombre de archivo que usa la aplicación junto con sus características y componentes asociados.
-   La [tabla Verb](verb-table.md) asocia información de verbo de comando con las extensiones de nombre de archivo enumeradas en la [tabla de extensión](extension-table.md). Esto proporciona un vínculo indirecto entre el verbo y la tabla de características necesarios para el anuncio de características.
-   La [tabla typelib](typelib-table.md) proporciona información que el instalador coloca en el registro para el registro de bibliotecas de tipos. Las entradas de la biblioteca de tipos no se escriben en el momento del anuncio. El instalador escribe las entradas de la biblioteca de tipos en el momento en que se instalan los componentes asociados a la biblioteca.
-   La [tabla MIME](mime-table.md) asocia un tipo de contexto MIME a un CLSID o una extensión de nombre de archivo. Esto proporciona una ruta de acceso entre la tabla de características y MIME necesaria para el anuncio de características.
-   La [tabla SelfReg](selfreg-table.md) proporciona la información necesaria para el registro automático de módulos. El instalador proporciona el registro automático solo por motivos de compatibilidad con versiones anteriores y no se recomienda como método para rellenar el registro; sin embargo, si hay algún módulo en la aplicación que deba registrarse, use la tabla SelfReg.
-   La [tabla de clases](class-table.md) se utiliza para registrar identificadores de clase y otra información para objetos com. Esta tabla contiene información relacionada con el servidor COM que se debe generar como parte del anuncio del producto.
-   La [tabla ProgID](progid-table.md) asocia los identificadores de programa a los identificadores de clase.
-   La [tabla AppID](appid-table.md) se utiliza para registrar opciones de configuración y seguridad comunes para objetos DCOM.
-   La [tabla de entorno](environment-table.md) se utiliza para establecer los valores de las variables de entorno y, en Windows 2000, la tabla de entorno también escribe en el registro.
-   La [tabla del registro](registry-table.md) contiene cualquier otra información que la aplicación necesite incluir en el registro del sistema. Esto incluiría la configuración predeterminada, la información de usuario o los datos, o el registro COM no admitido por las tablas anteriores.
-   La [tabla RemoveRegistry](removeregistry-table.md) contiene la información del registro que la aplicación necesita para eliminar del registro del sistema en el momento de la instalación.

 

 



