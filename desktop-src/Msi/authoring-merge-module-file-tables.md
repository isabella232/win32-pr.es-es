---
description: Se requiere una tabla de archivos en cada módulo de combinación y debe tener un registro para cada archivo que el módulo de mezcla entrega al paquete de instalación de destino.
ms.assetid: 436933c7-6e5d-4b4e-9147-c60a26871dbe
title: Creación de tablas de archivos de módulo de mezcla
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 715fe570a96015f62e45b0c2924b2a83be8eefc067e5d054decd59110b7797c2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120045475"
---
# <a name="authoring-merge-module-file-tables"></a>Creación de tablas de archivos de módulo de mezcla

Se [requiere una tabla](file-table.md) de archivos en cada módulo de combinación y debe tener un registro para cada archivo que el módulo de mezcla entrega al paquete de instalación de destino. Cuando el módulo de combinación se combina en un archivo .msi, todos los [](c-gly.md) archivos de la tabla de archivos del módulo de combinación se almacenan dentro de un archivo de archivador en el archivo .msm. El nombre del gabinete en un módulo de combinación es siempre el siguiente: MergeModule.CABinet.

Para obtener más información, vea [Generating MergeModule.CABinet Cabinet Files](generating-mergemodule-cabinet-cabinet-files.md).

-   Dado que los archivos de un módulo de combinación siempre se almacenan dentro de un archivo contenedor, no es necesario establecer las marcas de bits **msidbFileAttributesNoncompressed** o **msidbFileAttributesCompressed** en la columna Atributos de la tabla [de archivos](file-table.md).
-   Los nombres de los archivos del MergeModule.CABdeben coincidir con la clave principal de la tabla de archivos [del módulo de mezcla.](file-table.md)

    La columna Archivo es la [](file-table.md) clave principal de la tabla de archivos y las entradas de este campo deben seguir la convención que se describe en Nomenclatura de claves principales en bases de datos de [módulos de mezcla](naming-primary-keys-in-merge-module-databases.md).

-   Los números de secuencia de archivo se especifican en la columna Secuencia de la [tabla de archivos](file-table.md).

    Los archivos deben aparecer en [](file-table.md) la tabla de archivos del módulo de combinación en la misma secuencia que se almacenan MergeModule.CABconjunto de inet. No es necesario que los números de secuencia de los archivos sean consecutivos, pero deben seguir la misma secuencia que los archivos almacenados dentro del archivador. Por ejemplo, el primer, segundo y tercer archivo almacenado en el gabinete puede tener los números de secuencia 100, 200 y 300.

-   El instalador omite los archivos adicionales incluidos en MergeModule.CABque no aparecen en la [tabla de archivos](file-table.md).

    Un archivo de archivador puede contener todos los archivos necesarios para un módulo de combinación que admita varios idiomas mediante transformaciones. A todos los archivos de lenguaje se les puede dar un número de [](file-table.md) secuencia único en el gabinete y, a continuación, una transformación puede agregar o quitar archivos de la tabla de archivos cuando sea necesario para un idioma específico. Para obtener más información, vea [Creación de módulos de combinación de varios lenguajes.](authoring-multiple-language-merge-modules.md)

Para obtener más información, vea [Tabla de archivos](file-table.md).

 

 



