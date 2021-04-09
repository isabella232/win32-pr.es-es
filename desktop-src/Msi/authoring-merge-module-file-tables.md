---
description: En cada módulo de combinación se requiere una tabla de archivos y debe haber un registro para cada archivo que el módulo de combinación está entregando al paquete de instalación de destino.
ms.assetid: 436933c7-6e5d-4b4e-9147-c60a26871dbe
title: Crear tablas de archivos de módulo de combinación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e2687ed69c1a0362f96db896a5fdf4237ac4681
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082544"
---
# <a name="authoring-merge-module-file-tables"></a>Crear tablas de archivos de módulo de combinación

En cada módulo de combinación se requiere una [tabla de archivos](file-table.md) y debe haber un registro para cada archivo que el módulo de combinación está entregando al paquete de instalación de destino. Cuando el módulo de fusión mediante combinación se combina en un archivo. msi, cada archivo de la tabla de archivos de módulo de combinación se almacena en un [*archivo. cab*](c-gly.md) en el archivo. msm. El nombre del archivo. cab en un módulo de combinación es siempre el siguiente: MergeModule.CABinet.

Para obtener más información, consulte [generación de archivos. cab de MergeModule.CABinet](generating-mergemodule-cabinet-cabinet-files.md).

-   Dado que los archivos de un módulo de combinación siempre se almacenan dentro de un archivo. cab, no es necesario establecer las marcas de bits **msidbFileAttributesNoncompressed** o **msidbFileAttributesCompressed** en la columna Attributes de la [tabla File](file-table.md).
-   Los nombres de los archivos de MergeModule.CABinet deben coincidir con la clave principal de la [tabla de archivos](file-table.md)del módulo de combinación.

    La columna de archivo es la clave principal de la [tabla de archivos](file-table.md) y las entradas de este campo deben seguir la Convención que se describe en [asignar nombres a las claves principales en las bases de datos de módulos de combinación](naming-primary-keys-in-merge-module-databases.md).

-   Los números de secuencia de archivo se especifican en la columna Sequence de la [tabla File](file-table.md).

    Los archivos deben aparecer en la [tabla de archivos](file-table.md) del módulo de combinación en la misma secuencia en la que se almacenan en MergeModule.CABinet. No es necesario que los números de secuencia de los archivos sean consecutivos, pero deben seguir la misma secuencia que los archivos que se almacenan en el archivo. Por ejemplo, el primer, segundo y tercer archivo almacenados en el archivo. cab pueden tener los números de secuencia 100, 200 y 300.

-   El instalador omite los archivos adicionales incluidos en MergeModule.CABinet que no aparecen en la [tabla de archivos](file-table.md).

    Un archivo contenedor puede contener todos los archivos necesarios para un módulo de combinación que admita varios idiomas mediante transformaciones. A todos los archivos de idioma se les puede asignar un número de secuencia único en el archivo. cab y, a continuación, una transformación puede Agregar o quitar archivos de la [tabla de archivos](file-table.md) cuando sea necesario para un idioma específico. Para obtener más información, vea [crear módulos de combinación en varios lenguajes](authoring-multiple-language-merge-modules.md).

Para obtener más información, vea [File Table](file-table.md).

 

 



