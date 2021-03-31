---
description: En la tabla siguiente se identifican los tipos básicos de acciones personalizadas y se muestran los valores que se encuentran en los campos tipo, origen y destino de la tabla CustomAction para cada tipo.
ms.assetid: 8713451e-c0e7-4bec-bfb6-dfe4125d5a44
title: Tipos de acciones personalizadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c5b10ffd42d2f6fecf06e0732a8960c84bea2e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913074"
---
# <a name="custom-action-types"></a>Tipos de acciones personalizadas

En la tabla siguiente se identifican los tipos básicos de acciones personalizadas y se muestran los valores que se encuentran en los campos tipo, origen y destino de la tabla [CustomAction](customaction-table.md) para cada tipo. Las acciones personalizadas básicas se pueden modificar incluyendo bits de marca opcionales en la columna tipo. Para obtener descripciones de las opciones y los valores, vea lo siguiente:

-   [Opciones de procesamiento de devolución de acción personalizada](custom-action-return-processing-options.md)
-   [Opciones de programación de la ejecución de acciones personalizadas](custom-action-execution-scheduling-options.md)
-   [Opciones de ejecución de la acción personalizada In-Script](custom-action-in-script-execution-options.md)
-   [Opción de desinstalación de revisión de acción personalizada](custom-action-patch-uninstall-option.md)

Use los vínculos al tipo de acción personalizada básico para obtener una descripción y las opciones disponibles para cada tipo.



| Tipo de acción personalizada básica                                                                                                                           | Tipo | Source                                                                                                                              | Destino                                                                                                                                     |
|----------------------------------------------------------------------------------------------------------------------------------------------------|------|-------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [Tipo de acción personalizada 1](custom-action-type-1.md) Archivo DLL almacenado en un flujo de tabla binaria.<br/>                                               | 1    | Clave a tabla [binaria](binary-table.md) .                                                                                            | Punto de entrada de DLL.                                                                                                                           |
| [Tipo de acción personalizada 2](custom-action-type-2.md) Archivo EXE almacenado en un flujo de tabla binaria.<br/>                                               | 2    | Clave a tabla [binaria](binary-table.md) .                                                                                            | Cadena de línea de comandos.                                                                                                                       |
| [Tipo de acción personalizada 5](custom-action-type-5.md) Archivo JScript almacenado en un flujo de tabla binaria.<br/>                                           | 5    | Clave a tabla [binaria](binary-table.md) .                                                                                            | Función opcional de JScript a la que se puede llamar.                                                                                           |
| [Tipo de acción personalizada 6](custom-action-type-6.md) Archivo VBScript almacenado en una secuencia de tabla binaria.<br/>                                          | 6    | Clave a tabla [binaria](binary-table.md) .                                                                                            | Función de VBScript opcional a la que se puede llamar.                                                                                          |
| [Tipo de acción personalizada 17](custom-action-type-17.md) Archivo DLL que se instala con un producto.<br/>                                            | 17   | Clave de la tabla de [archivos](file-table.md) .                                                                                                | Punto de entrada de DLL.                                                                                                                           |
| [Tipo de acción personalizada 18](custom-action-type-18.md) Archivo EXE que se instala con un producto.<br/>                                            | 18   | Clave de la tabla de [archivos](file-table.md) .                                                                                                | Cadena de línea de comandos.                                                                                                                       |
| [Tipo de acción personalizada 19](custom-action-type-19.md) Muestra un mensaje de error especificado y devuelve un error, finalizando la instalación.<br/> | 19   | En blanco                                                                                                                               | Cadena de texto [con formato](formatted.md) . El mensaje literal o un índice en la tabla de [errores](error-table.md) .                           |
| [Tipo de acción personalizada 21](custom-action-type-21.md) Archivo JScript que se instala con un producto.<br/>                                        | 21   | Clave de la tabla de [archivos](file-table.md) .                                                                                                | Función opcional de JScript a la que se puede llamar.                                                                                           |
| [Tipo de acción personalizada 22](custom-action-type-22.md) Archivo VBScript que se instala con un producto.<br/>                                       | 22   | Clave de la tabla de [archivos](file-table.md) .                                                                                                | Función de VBScript opcional a la que se puede llamar.                                                                                          |
| [Tipo de acción personalizada 34](custom-action-type-34.md) Archivo EXE que tiene una ruta de acceso que hace referencia a un directorio.<br/>                                       | 34   | Clave de la tabla de [directorio](directory-table.md) . Este es el directorio de trabajo para la ejecución.                                         | Se [da formato](formatted.md) a la columna de destino y contiene la ruta de acceso completa y el nombre del archivo ejecutable seguido de argumentos opcionales. |
| [Tipo de acción personalizada 35](custom-action-type-35.md) Conjunto de directorios con texto con formato.<br/>                                                    | 35   | Clave de la tabla de [directorio](directory-table.md) . El directorio designado se establece mediante la cadena con formato en el campo de destino.   | Cadena de texto con formato.                                                                                                                   |
| [Tipo de acción personalizada 37](custom-action-type-37.md) Texto JScript almacenado en esta tabla de secuencia.<br/>                                           | 37   | Null                                                                                                                                | Cadena de código JScript.                                                                                                                  |
| [Tipo de acción personalizada 38](custom-action-type-38.md) Texto de VBScript almacenado en esta tabla de secuencia.<br/>                                          | 38   | Null                                                                                                                                | Cadena de código VBScript.                                                                                                                 |
| [Tipo de acción personalizada 50](custom-action-type-50.md) Archivo EXE que tiene una ruta de acceso especificada por un valor de propiedad.<br/>                                 | 50   | Nombre de propiedad o clave en la tabla de [propiedades](property-table.md) .                                                                       | Cadena de línea de comandos.                                                                                                                       |
| [Tipo de acción personalizada 51](custom-action-type-51.md) Conjunto de propiedades con texto con formato.<br/>                                                     | 51   | Nombre o clave de la propiedad en la tabla de [propiedades](property-table.md) . Esta propiedad se establece mediante la cadena con formato en el campo de destino. | Cadena de texto con formato.                                                                                                                   |
| [Tipo de acción personalizada 53](custom-action-type-53.md) Texto JScript especificado por un valor de propiedad.<br/>                                           | 53   | Nombre de propiedad o clave en la tabla de [propiedades](property-table.md) .                                                                       | Función opcional de JScript a la que se puede llamar.                                                                                           |
| [Tipo de acción personalizada 54](custom-action-type-54.md) Texto de VBScript especificado por un valor de propiedad.<br/>                                          | 54   | Nombre de propiedad o clave en la tabla de [propiedades](property-table.md) .                                                                       | Función de VBScript opcional a la que se puede llamar.                                                                                          |



 

Además, se usan los siguientes tipos de acciones personalizadas con instalaciones simultáneas:

-   [Tipo de acción personalizada 7](custom-action-type-7.md)
-   [Tipo de acción personalizada 23](custom-action-type-23.md)
-   [Tipo de acción personalizada 39](custom-action-type-39.md)

 

 




