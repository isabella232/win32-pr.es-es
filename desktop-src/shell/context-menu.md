---
description: En esta sección se describe la creación de menús contextuales (contexto) y la implementación de controladores de menú contextual (verbo).
title: Menús contextuales y controladores de menú contextual
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 956f3b10-2bc6-4f1f-a6ed-7184f94b545a
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 286dd9c860ae79e5124439439da97f206b4aa436
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275243"
---
# <a name="shortcut-context-menus-and-shortcut-menu-handlers"></a>Menús contextuales y controladores de menú contextual

En esta sección se describe la creación de menús contextuales (contexto) y la implementación de controladores de menú contextual (verbo).

Esta sección sobre los tipos de archivo y las asociaciones de archivo está organizada de la siguiente manera:

-   [Verbos y asociaciones de archivo](fa-verbs.md)
-   [Elegir un método de menú contextual estático o dinámico](shortcut-choose-method.md)
-   [Prácticas recomendadas para los controladores de menú contextual y varios verbos](verbs-best-practices.md)
-   [Crear controladores de menú contextual](context-menu-handlers.md)
-   [Crear menús en cascada estáticos](creating-static-cascading-menus.md)
-   [Cómo suprimir y controlar la visibilidad de los verbos](how-to-suppress-and-control-visibility.md)
-   [Cómo emplear el modelo de selección de verbos](how-to-employ-the-verb-selection-model.md)
-   [Cómo usar atributos de elemento](how-to-use-item-attributes.md)
-   [Cómo implementar verbos personalizados para carpetas a través de Desktop.ini](how-to-implement-custom-verbs-for-folders-through-desktop-ini.md)
-   [Personalización de un menú contextual mediante verbos dinámicos](shortcut-menu-using-dynamic-verbs.md)
-   [Cómo implementar la interfaz IContextMenu](how-to-implement-the-icontextmenu-interface.md)
-   [Referencia del menú contextual](context-menu-reference.md)

## <a name="additional-resources"></a>Recursos adicionales

Para obtener información sobre los conceptos relacionados, vea los temas siguientes:

-   [Introducción a las asociaciones de archivo](fa-intro.md).
-   Para extender el shell con controladores de tipo de archivo, vea [crear controladores de extensión de Shell](handlers.md).
-   Para crear un almacén de datos de Shell, vea [implementar las interfaces de objeto de carpeta básicas](nse-implement.md).

Para obtener documentación de referencia relacionada, vea los temas siguientes:

-   Para ejecutar un verbo en un elemento de Shell, vea el método [**InvokeVerb**](folderitem-invokeverb.md) .
-   Para recuperar una colección de verbos que se pueden ejecutar en un elemento de Shell, vea el método [**verbs**](folderitem-verbs.md) .
-   Para realizar una operación en un archivo especificado, vea las funciones [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) o [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) .

 

 



