---
description: Varios módulos de idioma pueden ofrecer componentes con varios lenguajes como un único archivo compuesto.
ms.assetid: b3a0b635-49c7-4f95-b31f-6c8688466dd2
title: Módulos de combinación en varios idiomas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d414cce484022bf81647110ac032d0db270d383
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001602"
---
# <a name="multiple-language-merge-modules"></a>Módulos de combinación en varios idiomas

Varios módulos de idioma pueden ofrecer componentes con varios lenguajes como un único archivo compuesto. El diseño y la funcionalidad de varios módulos de combinación de lenguajes son similares a los módulos de un solo idioma. Un módulo de combinación de varios idiomas tiene más de un idioma enumerado en la propiedad Resumen de la [**plantilla**](template-summary.md) . La base de datos de un módulo de combinación de varios idiomas contiene toda la información de instalación de varios idiomas. El MergeModule.CABarchivo. cab de inet dentro de un módulo de combinación de varios idiomas contiene todos los archivos de todos los idiomas admitidos.

Al aplicar un archivo. MSM de varios idiomas a un archivo. msi, debe indicar el idioma final del paquete de instalación después de la combinación. En el caso de un módulo de combinación de un solo idioma, la [tabla de archivos](file-table.md) del módulo de combinación muestra todos los archivos presentes en el archivo. cab de MergeModule.CABinet. En el caso de un módulo de combinación de varios idiomas, MergeModule.CABinet contiene todos los archivos para cada idioma admitido por el módulo, pero solo el subconjunto de archivos del lenguaje final entra en la tabla de archivos del módulo. La herramienta de combinación debe asegurarse de que el módulo proporcione el subconjunto de información y los archivos necesarios para el idioma final solicitado.

Cada módulo de combinación tiene un idioma predeterminado especificado en la columna idioma de la [tabla ModuleSignature](modulesignature-table.md). El idioma predeterminado de un módulo de combinación también se muestra como el primer o único idioma en la propiedad de Resumen de la [**plantilla**](template-summary.md) . En función del lenguaje final solicitado y del idioma predeterminado del módulo, la herramienta de combinación puede aplicar transformaciones de idioma a un módulo de combinación de varios idiomas para que se pueda abrir en el idioma solicitado o en una aproximación del idioma solicitado. Las transformaciones del lenguaje se incrustan dentro del módulo de combinación. Las herramientas de combinación deben aplicar transformaciones de idioma para que cumplan las siguientes reglas generales:

-   Si los lenguajes predeterminado y final son los mismos, el módulo se puede combinar sin usar transformaciones del lenguaje.
-   Si el idioma predeterminado es 0 (un módulo independiente del lenguaje), el módulo se puede combinar sin usar transformaciones del lenguaje.
-   Si el lenguaje final no es el predeterminado, la herramienta de combinación debe aplicar una de las transformaciones del lenguaje incrustadas en el módulo para cambiar el módulo al idioma final o a una aproximación del lenguaje final.

Por ejemplo, no es necesario realizar transformaciones de lenguaje si el idioma final es 1033 (Inglés de EE. UU.) y el idioma predeterminado del módulo es 1033 (Inglés de EE. UU.), 0 (idioma neutro) o 9 (en inglés genérico).

Las transformaciones de lenguaje son necesarias si el último idioma es 1033 (Inglés de EE. UU.) y el idioma predeterminado es 1031 (alemán). En este caso, la herramienta de combinación puede buscar primero en el módulo de varios idiomas para una transformación de lenguaje incrustado en 1033 (Inglés de EE. UU.). Si se produce un error, puede buscar una transformación en un idioma con un LANGID principal coincidente, aunque el LANGID secundario no coincida. Por ejemplo, si la herramienta no encuentra una transformación en 1033 (Inglés de EE. UU.), busca una transformación en 9 (Inglés genérico). Si esto no funciona, la herramienta de combinación busca una transformación en 0 (idioma neutro). Si se produce un error en todas estas búsquedas de una transformación adecuada, el módulo no se abre.

Para obtener más información, vea [crear módulos de combinación en varios lenguajes](authoring-multiple-language-merge-modules.md).

 

 



