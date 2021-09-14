---
description: El grupo del Registro de Windows installer contiene información sobre las entradas del Registro.
ms.assetid: 31a75c20-79e4-4bcf-bcc1-34a7d191fa90
title: Grupo de tablas del Registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8ba14bdc2bc5668ce2de3ec66172c75c176ab41
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069681"
---
# <a name="registry-tables-group"></a>Grupo de tablas del Registro

![grupo de tablas del Registro](images/registry.png)

Para obtener más información sobre este diagrama, vea la leyenda del diagrama [de relación de entidad](entity-relationship-diagram-legend.md).

El instalador tiene tablas específicas para los distintos tipos de entradas del Registro. Al rellenar el grupo de tablas del Registro, es importante intentar [](registry-table.md) minimizar el número de entradas que se incluyen en la tabla del Registro y maximizar el uso de otras tablas del Registro específicas. Esto se debe a que el instalador no puede distinguir entre diferentes tipos de entradas del Registro en la tabla Registro y no puede usar la lógica interna necesaria para aprovechar al máximo todas las características del instalador, como anunciar [*.*](a-gly.md) La creación de entradas del Registro com y relacionadas con el shell de esta manera también proporciona una organización más lógica y puede ayudar a minimizar el registro erróneo de información del servidor COM.

En la ilustración se muestra el grupo de entradas del Registro de tablas, así como las tablas [Componente](component-table.md), [Tabla de características](feature-table.md)y [Archivo](file-table.md). Aunque estos últimos no están directamente implicados en la rellenar el registro, se incluyen en la ilustración porque son esenciales para la lógica del grupo de entrada del Registro.

El grupo de entrada del Registro contiene las siguientes tablas de entradas específicas del Registro.

-   La [tabla Extensión contiene](extension-table.md) todas las extensiones de nombre de archivo que usa la aplicación junto con sus características y componentes asociados.
-   La [tabla Verbo asocia](verb-table.md) la información del verbo de comando a las extensiones de nombre de archivo enumeradas en la tabla De [extensión](extension-table.md). Esto proporciona un vínculo indirecto entre la tabla Verbo y Característica necesaria para el anuncio de características.
-   La [tabla TypeLib proporciona](typelib-table.md) información que el instalador coloca en el Registro para el registro de bibliotecas de tipos. Las entradas de la biblioteca de tipos no se escriben en el momento del anuncio. El instalador escribe las entradas de la biblioteca de tipos en el momento en que se instalan los componentes asociados a la biblioteca.
-   La [tabla MIME](mime-table.md) asocia un tipo de contexto MIME con un CLSID o una extensión de nombre de archivo. Esto proporciona una ruta de acceso entre mime y tabla de características necesaria para el anuncio de características.
-   La [tabla SelfReg proporciona](selfreg-table.md) la información necesaria para registrar módulos de forma independiente. El instalador proporciona el registro automático solo por compatibilidad con versiones anteriores y no se recomienda como método para rellenar el registro; sin embargo, si hay algún módulo en la aplicación que deba registrarse por sí mismo, use la tabla SelfReg.
-   La [tabla Class](class-table.md) se usa para registrar los IDs de clase y otra información para los objetos COM. Esta tabla contiene información relacionada con el servidor COM que se debe generar como parte del anuncio del producto.
-   La [tabla ProgId](progid-table.md) asocia los identificadores de programa a los identificadores de clase.
-   La [tabla AppId se](appid-table.md) usa para registrar valores comunes de seguridad y configuración para objetos DCOM.
-   La [tabla Environment](environment-table.md) se usa para establecer los valores de las variables de entorno y, en Windows 2000, la tabla Environment también escribe en el Registro.
-   La [tabla Registro](registry-table.md) contiene cualquier otra información que la aplicación necesite colocar en el registro del sistema. Esto incluiría la configuración predeterminada, la información o los datos del usuario o el registro COM no admitido por las tablas anteriores.
-   La [tabla RemoveRegistry contiene](removeregistry-table.md) la información del Registro que la aplicación debe eliminar del registro del sistema en el momento de la instalación.

 

 



