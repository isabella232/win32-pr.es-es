---
description: Un módulo de combinación se puede aplicar a un archivo .msi para agregar directorios a la instalación, pero no puede reemplazar ni quitar ningún directorio existente.
ms.assetid: 5b808aa2-b2b2-4703-bd57-0b5e1e73b306
title: Creación de tablas de directorios de módulos de mezcla
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f90768dff191b729d482f8ddd58a821a6ed440e79fcd1453ff412aaf7b8a76fb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120086275"
---
# <a name="authoring-merge-module-directory-tables"></a>Creación de tablas de directorios de módulos de mezcla

Un módulo de combinación se puede aplicar a un archivo .msi para agregar directorios a la instalación, pero no puede reemplazar ni quitar ningún directorio existente. La [tabla Directory](directory-table.md) especifica el diseño de los directorios que el módulo de mezcla proporciona a la instalación de destino. Se requiere una tabla Directory en cada módulo de combinación.

Use las siguientes directrices al crear la tabla de directorios en un módulo de combinación. Para obtener más información, vea [Tabla de directorios](directory-table.md) [y Uso de la tabla de directorios](using-the-directory-table.md).

-   La estructura de directorios agregada por el módulo de combinación debe tener un único directorio raíz. La raíz debe denominarse TARGETDIR. El usuario puede cambiar el valor de TARGETDIR durante la combinación para especificar dónde adjuntar la estructura de directorios del módulo al árbol de directorios del destino.
-   Las tablas de módulos de mezcla distintas de la tabla Directory no deben hacer referencia directamente a las ubicaciones de directorio a TARGETDIR. La ubicación de este tipo de referencia cambia si el usuario cambia el valor de TARGETDIR.
-   Las tablas del módulo de combinación deben hacer referencia a la ubicación de un directorio secundario de TARGETDIR u otro directorio en el árbol del módulo de mezcla. Haga lo siguiente para especificar TARGETDIR como el elemento primario de un directorio en el módulo de combinación. Escriba el directorio en la columna Directorio y escriba TARGETDIR en la columna Directory \_ Parent (Primario del directorio). Use la notación "." de la columna DefaultDir para indicar que este directorio se encuentra en TARGETDIR sin un subdirectorio. Para obtener más información, [vea Usar la tabla de directorios](using-the-directory-table.md).
-   Los nombres de directorios agregados por el módulo de combinación deben usar las convenciones de nomenclatura descritas en Nomenclatura de claves principales en bases de datos [de módulos de mezcla](naming-primary-keys-in-merge-module-databases.md). Esto incluye directorios predefinidos por propiedades como la [**propiedad SystemFolder**](systemfolder.md) y [**la propiedad ProgramFilesFolder.**](programfilesfolder.md)
-   Anexe [*un GUID*](g-gly.md) a cada entrada de la tabla Directory (excepto TARGETDIR). Esto incluye entradas de tabla de directorio que especifican las propiedades [**systemFolder**](systemfolder.md) del instalador de Windows, por ejemplo, SystemFolder.00000000 \_ 0000 \_ \_ 0000 \_ 000000000000000000000000. La biblioteca Mergemod.dll agrega acciones personalizadas para establecer la **propiedad SystemFolder.**
-   Cuando se incluye un directorio predefinido en un módulo de combinación, la herramienta de combinación agrega automáticamente un tipo de acción [personalizada 51](custom-action-type-51.md) a la base de datos de destino. El autor del módulo de mezcla debe asegurarse de que también se incluye una tabla [CustomAction.](customaction-table.md) La tabla CustomAction puede estar vacía, pero esta tabla debe existir en la base de datos de destino y garantiza que los directorios predefinidos modificados se escriben en las ubicaciones correctas. Por ejemplo, cuando se incluye un directorio del sistema en un módulo de combinación, el autor del módulo de mezcla debe asegurarse de que existe una tabla de acción personalizada.

    Tenga en cuenta que el algoritmo de coincidencia para la generación de estas acciones personalizadas de tipo 51 solo comprueba que el nombre del directorio comienza con una de las propiedades [**SystemFolder predefinidas.**](systemfolder.md) No comprueba que el nombre del directorio sea exactamente igual a la propiedad de directorio. Cualquier directorio que comienza con uno de estos nombres de carpeta estándar obtiene una acción personalizada de tipo 51, incluso si el resto del nombre no es un GUID. Los autores deben tener cuidado de que esto no genere coincidencias de falsos positivos y generación de acciones personalizadas no deseadas en claves principales derivadas que comiencen por una de las **propiedades SystemFolder.**

A continuación se muestra un ejemplo de una tabla Directory en un módulo de combinación y los directorios resueltos esperados.



| Directorio                                              | Elemento primario \_ del directorio                                | DefaultDir  |
|--------------------------------------------------------|--------------------------------------------------|-------------|
| TARGETDIR                                              |                                                  | SourceDir   |
| Dir00.BC82E350 \_ C7FC \_ 11d1 \_ A848-006097ABDE17        | TARGETDIR                                        | .:MMM \_ Prog |
| SystemFolder.BC82E350 \_ C7FC \_ 11d1 \_ A848-006097ABDE17 | TARGETDIR                                        | MMM \_ Sys    |
| Dir02.BC82E350 \_ C7FC \_ 11d1 \_ A848-006097ABDE17        | Dir00.BC82E350 \_ C7FC \_ 11d1 \_ A848 \_ 006097ABDE17 | MFC \_ OCX    |



 

Se espera que un módulo de combinación con la tabla Directory anterior desenlame la siguiente estructura de directorios.



| Directorio                                              | Destino                                     | Source                                               |
|--------------------------------------------------------|--------------------------------------------|------------------------------------------------------|
| Dir00.BC82E350 \_ C7FC \_ 11d1 \_ A848-006097ABDE17        | \[Punto de instalación del módulo de mezcla\]\\         | \[MMM Prog del punto de origen \] \\ del módulo de \_ mezcla           |
| SystemFolder.BC82E350 \_ C7FC \_ 11d1 \_ A848-006097ABDE17 | \[SystemFolder\]\\                         | \[MMM Sys del punto de origen \] \\ del módulo de \_ mezcla            |
| Dir02.BC82E350 \_ C7FC \_ 11d1 \_ A848-006097ABDE17        | \[OCX mfc de punto \] \\ de instalación del módulo \_ de mezcla | \[Punto de origen del módulo de mezcla \] \\ MMM \_ Prog \\ MFC \_ OCX |



 

 

 



