---
description: Cuando un módulo se combina en una base de datos que tiene un idioma predeterminado diferente, es posible que la herramienta de combinación tenga que aplicar una transformación de lenguaje al módulo para proporcionar el lenguaje final. Para obtener más información, vea módulos de combinación en varios idiomas.
ms.assetid: 51e8774e-f358-423f-a283-ad7beeabbbdb
title: Crear una transformación de idioma para un módulo de combinación de varios idiomas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 970c8908ddbf89e31f0fc7a415358bb887f0838e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276519"
---
# <a name="authoring-a-language-transform-for-a-multiple-language-merge-module"></a>Crear una transformación de idioma para un módulo de combinación de varios idiomas

Cuando un módulo se combina en una base de datos que tiene un idioma predeterminado diferente, es posible que la herramienta de combinación tenga que aplicar una transformación de lenguaje al módulo para proporcionar el lenguaje final. Para obtener más información, vea [módulos de combinación en varios idiomas](multiple-language-merge-modules.md).

Las transformaciones del lenguaje se almacenan en el archivo. MSM del módulo y deben tener el nombre y el formato: módulo CRT. lang \# \# \# \# . \# \# \# \# Representa el [LANGID](localizing-the-error-and-actiontext-tables.md) de hasta cuatro dígitos del idioma final. Por ejemplo, módulo CRT. Lang1033, módulo CRT. Lang9 y módulo CRT. Lang0 para las transformaciones con el Inglés de EE. UU., el inglés mundial y el idioma neutro. Son las mismas que las [transformaciones incrustadas](embedded-transforms.md) y se pueden agregar a los subalmacénes en el archivo. msm.

La transformación de idioma debe hacer lo siguiente:

-   Cambie el idioma predeterminado en la columna idioma de la [tabla ModuleSignature](modulesignature-table.md) al nuevo lenguaje del módulo.
-   Cambie el idioma predeterminado en la columna idioma de la [tabla ModuleComponents](modulecomponents-table.md) por el nuevo idioma del módulo. La transformación puede Agregar o quitar filas de esta tabla.
-   Si es necesario, cambie el idioma de la columna RequiredLanguage, o agregue o elimine filas, a la [tabla ModuleDependency](moduledependency-table.md).
-   Si es necesario, cambie el idioma de la columna ExcludedLanguage, o agregue o elimine filas, a la [tabla ModuleExclusion](moduleexclusion-table.md).
-   La transformación puede realizar cualquier operación de transformación válida en el módulo, incluida la adición o eliminación de componentes, archivos, entradas del registro o acciones.

Tenga en cuenta que la aplicación de una transformación de idioma al abrir el módulo no cambia el idioma predeterminado o los idiomas que admite el módulo, sino que simplemente cambia el idioma que se solicita. Por lo tanto, la propiedad de [**Resumen de plantilla**](template-summary.md) no cambia, ya que debe mostrar todos los idiomas admitidos por el módulo con el idioma predeterminado que se muestra en primer lugar.

Todos los archivos necesarios para todas las transformaciones de lenguaje posibles se almacenan normalmente en un único archivo. cab incluido con el módulo. Dado que no es práctico que la transformación de idioma modifique este archivo. cab, es mejor usar una secuencia de archivos global en el archivo. cab, la [tabla de archivos](file-table.md)y la transformación de idioma. Para obtener más información, consulte [ordenar la secuencia de archivos en el archivo. cab de un módulo de combinación de varios idiomas](ordering-the-file-sequence-in-the-cab-of-a-multiple-language-merge-module.md) .

 

 



