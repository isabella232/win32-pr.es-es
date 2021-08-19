---
description: Varios módulos de lenguaje pueden entregar componentes con varios idiomas diferentes como un único archivo compuesto.
ms.assetid: b3a0b635-49c7-4f95-b31f-6c8688466dd2
title: Módulos de combinación de varios idiomas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17f32d219e1071cd431117919d3eb3f3361d30213f59a26f9ec2cdf2e81e591b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118943426"
---
# <a name="multiple-language-merge-modules"></a>Módulos de combinación de varios idiomas

Varios módulos de lenguaje pueden entregar componentes con varios idiomas diferentes como un único archivo compuesto. El diseño y la funcionalidad de varios módulos de combinación de lenguajes es similar a los módulos de lenguaje único. Un módulo de combinación de varios idiomas tiene más de un idioma enumerado en la [**propiedad Resumen de**](template-summary.md) plantilla. La base de datos de un módulo de combinación de varios idiomas contiene toda la información de configuración de varios idiomas. El MergeModule.CABde conjunto de cambios dentro de un módulo de combinación de varios idiomas contiene todos los archivos de todos los idiomas admitidos.

Al aplicar un archivo .msm de varios idiomas a un archivo .msi, debe indicar el idioma final del paquete de instalación después de la combinación. En el caso de un módulo de combinación [](file-table.md) de lenguaje único, la tabla Archivo del módulo de mezcla muestra todos los archivos presentes en el MergeModule.CABde conjunto de cambios. En el caso de un módulo de combinación de varios idiomas, MergeModule.CABinet contiene todos los archivos para cada idioma admitido por el módulo, pero solo el subconjunto de archivos para el idioma final entra en la tabla File del módulo. La herramienta de combinación debe asegurarse de que el módulo proporciona el subconjunto de información y archivos necesarios para el idioma final solicitado.

Cada módulo de combinación tiene un idioma predeterminado especificado en la columna Language de la [tabla ModuleSignature](modulesignature-table.md). El idioma predeterminado de un módulo de combinación también se muestra como el primer idioma, o solo, en la [**propiedad Resumen de**](template-summary.md) plantilla. Según el idioma final solicitado y el idioma predeterminado del módulo, la herramienta de combinación puede aplicar transformaciones de idioma a un módulo de combinación de varios idiomas para que se pueda abrir en el idioma solicitado o una aproximación del idioma solicitado. Las transformaciones de lenguaje se incrustan dentro del módulo merge. Las herramientas de combinación deben aplicar transformaciones de lenguaje en cumplimiento de las siguientes reglas generales:

-   Si los idiomas predeterminados y finales son los mismos, el módulo se puede combinar sin usar transformaciones de lenguaje.
-   Si el idioma predeterminado es 0 (un módulo neutral del idioma), el módulo se puede combinar sin usar transformaciones de idioma.
-   Si el idioma final no es el idioma predeterminado, la herramienta de combinación debe aplicar una de las transformaciones de lenguaje incrustadas en el módulo para cambiar el módulo al idioma final o a una aproximación del idioma final.

Por ejemplo, no se requiere ninguna transformación de idioma si el idioma final es 1033 (inglés de EE. UU.) y el idioma predeterminado del módulo es 1033 (inglés de EE. UU.), 0 (idioma neutro) o 9 (inglés genérico).

Las transformaciones de idioma son necesarias si el idioma final es 1033 (inglés de EE. UU.) y el idioma predeterminado es 1031 (alemán). En este caso, la herramienta de combinación puede buscar primero en el módulo de varios idiomas una transformación de idioma insertado a 1033 (inglés de EE. UU.). Si se produce un error, puede buscar una transformación en un idioma con un LANGID principal correspondiente, incluso si el LANGID secundario no coincide. Por ejemplo, si la herramienta no encuentra una transformación a 1033 (inglés de EE. UU.), busca una transformación a 9 (inglés genérico). Si se produce un error, la herramienta de combinación busca una transformación en 0 (idioma neutro). Si se produce un error en todas estas búsquedas para una transformación adecuada, el módulo no se puede abrir.

Para obtener más información, vea [Creación de módulos de combinación de varios lenguajes.](authoring-multiple-language-merge-modules.md)

 

 



