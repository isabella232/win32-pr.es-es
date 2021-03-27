---
description: La interfaz de usuario de Windows proporciona a los usuarios acceso a una gran variedad de objetos necesarios para ejecutar aplicaciones y administrar el sistema operativo.
title: Guía del desarrollador de Shell
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 8f88ef25-3645-4f54-9453-41f919c0fc0a
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 1be17ca90b7138294be3e1b34fa3fcb4dcb4227a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997293"
---
# <a name="shell-developers-guide"></a>Guía del desarrollador de Shell

La interfaz de usuario de Windows proporciona a los usuarios acceso a una gran variedad de objetos necesarios para ejecutar aplicaciones y administrar el sistema operativo. El más conocido de estos objetos son las carpetas y los archivos que residen en las unidades de disco del equipo. También hay una serie de objetos virtuales que permiten al usuario realizar tareas como el envío de archivos a las impresoras remotas o el acceso a la papelera de reciclaje. El shell organiza estos objetos en un espacio de nombres jerárquico y proporciona a los usuarios y las aplicaciones una manera coherente y eficaz de obtener acceso a los objetos y administrarlos.

## <a name="in-this-section"></a>En esta sección

-   [Consideraciones de seguridad: Shell de Microsoft Windows](sec-shell.md)
-   [Instrucciones para implementar extensiones de In-Process](shell-and-managed-code.md)
-   [Versiones de Shell y controles comunes](versions.md)
-   [Implementar las interfaces de objeto de carpeta básicas](nse-implement.md)
-   [Implementar un formato de archivo personalizado](customizing-file-types-bumper.md)
-   [Extensibilidad de Shell (creación de un origen de datos)](shell-extensibility-bumper.md)
-   [Implementar elementos del panel de control](control-panel-applications.md)
-   [Compatibilidad con aplicaciones de Shell](application-support-bumper.md)
-   [Temas de Shell heredados](miscellaneous-topics-bumper.md)

## <a name="document-conventions"></a>Convenciones del documento

La guía para desarrolladores de Shell sigue las convenciones de documentos habituales del kit de desarrollo de software (SDK) de Windows. Deben tenerse en cuentan dos convenciones en particular:

-   El código de ejemplo omite el código normal de corrección de errores. Este código solo se ha quitado para que el código sea más legible. Debe incluir todo el código de corrección de errores adecuado en sus propias aplicaciones.
-   Para que las entradas del registro de ejemplo sean claras, los nombres de clave, subclaves y entradas, así como los valores se muestran con una fuente estándar. Los nombres de los elementos definidos por el usuario o por la aplicación están en cursiva.

 

 



