---
description: En la tabla siguiente se identifican los tipos básicos de acciones personalizadas y se muestran los valores que se encuentran en los campos Tipo, Origen y Destino de la tabla CustomAction para cada tipo.
ms.assetid: 8713451e-c0e7-4bec-bfb6-dfe4125d5a44
title: Tipos de acción personalizados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf0be8a9465c9a3567a867bab911d7539e8700219515c86bb5a8fc2b7d5eff68
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118624310"
---
# <a name="custom-action-types"></a>Tipos de acción personalizados

En la tabla siguiente se identifican los tipos básicos de acciones personalizadas y se muestran los valores que se encuentran en los campos Tipo, Origen y Destino de la [tabla CustomAction](customaction-table.md) para cada tipo. Las acciones personalizadas básicas se pueden modificar mediante la inclusión de bits de marca opcionales en la columna Tipo. Para obtener descripciones de las opciones y los valores, vea lo siguiente:

-   [Opciones de procesamiento de devolución de acciones personalizadas](custom-action-return-processing-options.md)
-   [Opciones de programación de ejecución de acciones personalizadas](custom-action-execution-scheduling-options.md)
-   [Opciones de ejecución de In-Script acción personalizada](custom-action-in-script-execution-options.md)
-   [Opción de desinstalación de revisiones de acción personalizada](custom-action-patch-uninstall-option.md)

Use los vínculos al tipo de acción personalizado básico para obtener una descripción y las opciones disponibles para cada tipo.



| Tipo de acción personalizada básica                                                                                                                           | Tipo | Source                                                                                                                              | Destino                                                                                                                                     |
|----------------------------------------------------------------------------------------------------------------------------------------------------|------|-------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [Tipo de acción personalizada 1](custom-action-type-1.md) Archivo DLL almacenado en una secuencia de tabla binaria.<br/>                                               | 1    | Clave en [tabla](binary-table.md) binaria.                                                                                            | Punto de entrada dll.                                                                                                                           |
| [Tipo de acción personalizada 2](custom-action-type-2.md) Archivo EXE almacenado en una secuencia de tabla binaria.<br/>                                               | 2    | Clave en [tabla](binary-table.md) binaria.                                                                                            | Cadena de línea de comandos.                                                                                                                       |
| [Acción personalizada Tipo 5](custom-action-type-5.md)JScript archivo almacenado en una secuencia de tabla binaria.<br/>                                           | 5    | Clave en [tabla](binary-table.md) binaria.                                                                                            | Función de JScript opcional a la que se puede llamar.                                                                                           |
| [Tipo de acción personalizada 6](custom-action-type-6.md) Archivo VBScript almacenado en una secuencia de tabla binaria.<br/>                                          | 6    | Clave en [tabla](binary-table.md) binaria.                                                                                            | Función de VBScript opcional a la que se puede llamar.                                                                                          |
| [Tipo de acción personalizada 17](custom-action-type-17.md) Archivo DLL que se instala con un producto.<br/>                                            | 17   | Clave en [tabla de](file-table.md) archivos.                                                                                                | Punto de entrada dll.                                                                                                                           |
| [Tipo de acción personalizada 18](custom-action-type-18.md) Archivo EXE que se instala con un producto.<br/>                                            | 18   | Clave en [tabla de](file-table.md) archivos.                                                                                                | Cadena de línea de comandos.                                                                                                                       |
| [Tipo de acción personalizada 19](custom-action-type-19.md) Muestra un mensaje de error especificado y devuelve un error, finalizando la instalación.<br/> | 19   | En blanco                                                                                                                               | [Cadena de texto](formatted.md) con formato. Mensaje literal o índice de la [tabla Error.](error-table.md)                           |
| [Acción personalizada Tipo 21](custom-action-type-21.md)JScript archivo que se instala con un producto.<br/>                                        | 21   | Clave en [tabla de](file-table.md) archivos.                                                                                                | Función de JScript opcional a la que se puede llamar.                                                                                           |
| [Tipo de acción personalizada 22](custom-action-type-22.md) Archivo VBScript que se instala con un producto.<br/>                                       | 22   | Clave en [tabla de](file-table.md) archivos.                                                                                                | Función de VBScript opcional a la que se puede llamar.                                                                                          |
| [Tipo de acción personalizada 34](custom-action-type-34.md) Archivo EXE que tiene una ruta de acceso que hace referencia a un directorio.<br/>                                       | 34   | Clave en la [tabla de](directory-table.md) directorios. Este es el directorio de trabajo para su ejecución.                                         | La columna Destino tiene [formato](formatted.md) y contiene la ruta de acceso completa y el nombre del archivo ejecutable seguido de argumentos opcionales. |
| [Tipo de acción personalizada 35](custom-action-type-35.md) Directorio establecido con texto con formato.<br/>                                                    | 35   | Clave de la tabla [Directory.](directory-table.md) El directorio designado se establece mediante la cadena con formato en el campo Destino.   | Cadena de texto con formato.                                                                                                                   |
| [Acción personalizada Tipo 37](custom-action-type-37.md)JScript texto almacenado en esta tabla de secuencia.<br/>                                           | 37   | Null                                                                                                                                | Cadena de JScript código.                                                                                                                  |
| [Tipo de acción personalizada 38](custom-action-type-38.md) Texto de VBScript almacenado en esta tabla de secuencia.<br/>                                          | 38   | Null                                                                                                                                | Cadena de código VBScript.                                                                                                                 |
| [Tipo de acción personalizada 50](custom-action-type-50.md) Archivo EXE que tiene una ruta de acceso especificada por un valor de propiedad.<br/>                                 | 50   | Nombre de propiedad o clave de la [tabla](property-table.md) Property.                                                                       | Cadena de línea de comandos.                                                                                                                       |
| [Tipo de acción personalizada 51](custom-action-type-51.md) Propiedad establecida con texto con formato.<br/>                                                     | 51   | Nombre de propiedad o clave de la [tabla](property-table.md) Property. Esta propiedad se establece mediante la cadena con formato en el campo Destino. | Cadena de texto con formato.                                                                                                                   |
| [Acción personalizada Tipo 53](custom-action-type-53.md)JScript texto especificado por un valor de propiedad.<br/>                                           | 53   | Nombre de propiedad o clave de la [tabla](property-table.md) Property.                                                                       | Función de JScript opcional a la que se puede llamar.                                                                                           |
| [Tipo de acción personalizada 54](custom-action-type-54.md) Texto de VBScript especificado por un valor de propiedad.<br/>                                          | 54   | Nombre de propiedad o clave de la [tabla](property-table.md) Property.                                                                       | Función de VBScript opcional a la que se puede llamar.                                                                                          |



 

Además, se usan los siguientes tipos de acciones personalizadas con instalaciones simultáneas:

-   [Tipo de acción personalizada 7](custom-action-type-7.md)
-   [Tipo de acción personalizada 23](custom-action-type-23.md)
-   [Tipo de acción personalizada 39](custom-action-type-39.md)

 

 




