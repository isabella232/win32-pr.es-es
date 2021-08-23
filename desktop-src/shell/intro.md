---
description: La Windows de usuario proporciona a los usuarios acceso a una amplia variedad de objetos necesarios para ejecutar aplicaciones y administrar el sistema operativo.
title: Guía del desarrollador de Shell
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 8f88ef25-3645-4f54-9453-41f919c0fc0a
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 7e6fbef1a8e34746d3b430faa5cb03f93613bc7c35e047cdd35afeb4921a37fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119032303"
---
# <a name="shell-developers-guide"></a>Guía del desarrollador de Shell

La Windows de usuario proporciona a los usuarios acceso a una amplia variedad de objetos necesarios para ejecutar aplicaciones y administrar el sistema operativo. Los objetos más numerosos y conocidos son las carpetas y archivos que residen en unidades de disco del equipo. También hay una serie de objetos virtuales que permiten al usuario realizar tareas como enviar archivos a impresoras remotas o acceder a la papelera de reciclaje. El Shell organiza estos objetos en un espacio de nombres jerárquico y proporciona a los usuarios y las aplicaciones una manera coherente y eficaz de acceder a los objetos y administrarlos.

## <a name="in-this-section"></a>En esta sección

-   [Consideraciones de seguridad: Microsoft Windows Shell](sec-shell.md)
-   [Instrucciones para implementar extensiones de In-Process de datos](shell-and-managed-code.md)
-   [Versiones de shell y controles comunes](versions.md)
-   [Implementar las interfaces de objetos de carpeta básicas](nse-implement.md)
-   [Implementar un formato de archivo personalizado](customizing-file-types-bumper.md)
-   [Extensibilidad del shell (crear un origen de datos)](shell-extensibility-bumper.md)
-   [Implementación de Panel de control elementos](control-panel-applications.md)
-   [Compatibilidad con aplicaciones de Shell](application-support-bumper.md)
-   [Temas de Shell heredado](miscellaneous-topics-bumper.md)

## <a name="document-conventions"></a>Convenciones del documento

La Guía para desarrolladores de Shell sigue las convenciones habituales Windows documento del Kit de desarrollo de software (SDK). En concreto, se deben tener en cuenta dos convenciones:

-   El código de ejemplo omite el código de corrección de errores normal. Este código solo se ha quitado para que el código sea más legible. Debe incluir todo el código de corrección de errores adecuado en sus propias aplicaciones.
-   Para borrar las entradas del Registro de ejemplo, los nombres de clave, subclave y entrada, así como los valores, se muestran con una fuente estándar. Los nombres de elementos definidos por el usuario o la aplicación están en cursiva.

 

 



