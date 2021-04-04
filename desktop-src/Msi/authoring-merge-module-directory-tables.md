---
description: Un módulo de combinación se puede aplicar a un archivo. msi para agregar directorios a la instalación, pero no puede reemplazar o quitar directorios existentes.
ms.assetid: 5b808aa2-b2b2-4703-bd57-0b5e1e73b306
title: Crear tablas del directorio del módulo de combinación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98332f2c0bda10a5cc076f0ec80df3bf4b2e05aa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909074"
---
# <a name="authoring-merge-module-directory-tables"></a>Crear tablas del directorio del módulo de combinación

Un módulo de combinación se puede aplicar a un archivo. msi para agregar directorios a la instalación, pero no puede reemplazar o quitar directorios existentes. La [tabla de directorios](directory-table.md) especifica el diseño de los directorios que el módulo de combinación proporciona a la instalación de destino. Se requiere una tabla de directorio en cada módulo de combinación.

Utilice las siguientes directrices para crear la tabla de directorio en un módulo de combinación. Para obtener más información, consulte [tabla de directorios](directory-table.md) y [uso de la tabla de directorios](using-the-directory-table.md).

-   La estructura de directorios agregada por el módulo de combinación debe tener un único directorio raíz. La raíz debe tener el nombre TARGETDIR. El usuario puede cambiar el valor de TARGETDIR durante la combinación para especificar dónde se debe adjuntar la estructura de directorios del módulo en el árbol de directorios del destino.
-   Las tablas del módulo de combinación que no sean la tabla del directorio no deben hacer referencia directamente a las ubicaciones del directorio en TARGETDIR. La ubicación de esta referencia cambia si el usuario cambia el valor de TARGETDIR.
-   Las tablas del módulo de combinación deben hacer referencia a la ubicación de un directorio secundario de TARGETDIR, o a otro directorio del árbol del módulo de combinación. Haga lo siguiente para especificar TARGETDIR como elemento primario de un directorio en el módulo de combinación. Escriba el directorio en la columna directorio y escriba TARGETDIR en la \_ columna principal del directorio. Use la notación "." de la columna DefaultDir para indicar que este directorio se encuentra en TARGETDIR sin un subdirectorio. Para obtener más información, consulte [uso de la tabla de directorios](using-the-directory-table.md).
-   Los nombres de los directorios agregados por el módulo de combinación deben usar las convenciones de nomenclatura descritas en [naming Keys Primary in Merge Module Databases](naming-primary-keys-in-merge-module-databases.md). Esto incluye los directorios predefinidos por propiedades como la propiedad [**carpetadelsistema**](systemfolder.md) y la propiedad [**ProgramFilesFolder**](programfilesfolder.md) .
-   Anexe un [*GUID*](g-gly.md) a cada entrada de la tabla del directorio (excepto el targetdir). Esto incluye las entradas de la tabla de directorios que especifican Windows Installer propiedades [**carpetadelsistema**](systemfolder.md) , por ejemplo, carpetadelsistema. 00000000 0000 0000 0000 \_ \_ \_ \_ 000000000000. La biblioteca Mergemod.dll agrega acciones personalizadas para establecer la propiedad **carpetadelsistema** .
-   Cuando se incluye un directorio predefinido en un módulo de combinación, la herramienta de combinación agrega automáticamente un [tipo de acción personalizada 51](custom-action-type-51.md) a la base de datos de destino. El autor del módulo de combinación debe asegurarse de que también se incluye una [tabla CustomAction](customaction-table.md) . La tabla CustomAction puede estar vacía, pero es necesario que esta tabla exista en la base de datos de destino y se asegure de que los directorios predefinidos modificados se escriben en las ubicaciones correctas. Por ejemplo, cuando un directorio del sistema se incluye en un módulo de combinación, el autor del módulo de combinación debe asegurarse de que existe una tabla de acción personalizada.

    Tenga en cuenta que el algoritmo de búsqueda de coincidencias para la generación de estas acciones personalizadas de tipo 51 solo comprueba que el nombre del directorio comienza por una de las propiedades predefinidas de [**carpetadelsistema**](systemfolder.md) . No comprueba que el nombre del directorio es exactamente igual a la propiedad Directory. Cualquier directorio que comience con uno de estos nombres de carpeta estándar obtiene una acción personalizada Type 51, incluso si el resto del nombre no es un GUID. Los autores deben tener cuidado de que esto no genere coincidencias de falsos positivos y la generación de una acción personalizada no deseada en claves principales derivadas que comiencen por una de las propiedades de **carpetadelsistema** .

El siguiente es un ejemplo de una tabla de directorio en un módulo de combinación y los directorios resueltos esperados.



| Directorio                                              | Directorio \_ primario                                | DefaultDir  |
|--------------------------------------------------------|--------------------------------------------------|-------------|
| TARGETDIR                                              |                                                  | SourceDir   |
| Dir00. BC82E350 \_ C7FC \_ 11D1 \_ A848-006097ABDE17        | TARGETDIR                                        | .: Progreso de MMM \_ |
| Carpetadelsistema. BC82E350 \_ C7FC \_ 11D1 \_ A848-006097ABDE17 | TARGETDIR                                        | DD \_ de MMM    |
| Dir02. BC82E350 \_ C7FC \_ 11D1 \_ A848-006097ABDE17        | Dir00. BC82E350 \_ C7FC \_ 11D1 \_ A848 \_ 006097ABDE17 | OCX de MFC \_    |



 

Se espera que un módulo de combinación con la tabla de directorio anterior dé como resultado la siguiente estructura de directorios.



| Directorio                                              | Destino                                     | Source                                               |
|--------------------------------------------------------|--------------------------------------------|------------------------------------------------------|
| Dir00. BC82E350 \_ C7FC \_ 11D1 \_ A848-006097ABDE17        | \[Punto de instalación del módulo de combinación\]\\         | \[Progreso del punto de origen del módulo de combinación \] \\ \_           |
| Carpetadelsistema. BC82E350 \_ C7FC \_ 11D1 \_ A848-006097ABDE17 | \[Carpetadelsistema\]\\                         | \[\] \\ DD sys del punto de origen del módulo de combinación \_            |
| Dir02. BC82E350 \_ C7FC \_ 11D1 \_ A848-006097ABDE17        | \[Punto de instalación del módulo de combinación, \] \\ ocx de MFC \_ | \[Punto de origen del módulo de combinación \] \\ \_ \\ \_ |



 

 

 



