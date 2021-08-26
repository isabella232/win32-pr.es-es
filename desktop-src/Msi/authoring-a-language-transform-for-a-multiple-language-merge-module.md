---
description: Cuando un módulo se combina en una base de datos que tiene un idioma predeterminado diferente, es posible que la herramienta de combinación tenga que aplicar una transformación de idioma al módulo para proporcionar el idioma final. Para obtener más información, vea Módulos de combinación de varios lenguajes.
ms.assetid: 51e8774e-f358-423f-a283-ad7beeabbbdb
title: Creación de una transformación de idioma para un módulo de combinación de varios idiomas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9cf9a9c2294d310959bcd82f13010c88eb513e40ad4536c4dbca61e50d260873
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120078065"
---
# <a name="authoring-a-language-transform-for-a-multiple-language-merge-module"></a>Creación de una transformación de idioma para un módulo de combinación de varios idiomas

Cuando un módulo se combina en una base de datos que tiene un idioma predeterminado diferente, es posible que la herramienta de combinación tenga que aplicar una transformación de idioma al módulo para proporcionar el idioma final. Para obtener más información, vea [Módulos de combinación de varios lenguajes.](multiple-language-merge-modules.md)

Las transformaciones de lenguaje se almacenan en el archivo .msm del módulo y deben tener el nombre y el formato: MergeModule.Lang \# \# \# \# . representa el LANGID de \# \# \# \# hasta cuatro [dígitos](localizing-the-error-and-actiontext-tables.md) del idioma final. Por ejemplo, MergeModule.Lang1033, MergeModule.Lang9 y MergeModule.Lang0 para transformaciones en inglés de EE. UU., inglés del mundo e idioma neutro. Son iguales que [las transformaciones insertadas](embedded-transforms.md) y puede agregarlas a los subalmacenamientos en el archivo .msm.

La transformación de idioma debe hacer lo siguiente:

-   Cambie el idioma predeterminado de la columna Idioma de [la tabla ModuleSignature](modulesignature-table.md) al nuevo idioma del módulo.
-   Cambie el idioma predeterminado de la columna Idioma de [la tabla ModuleComponents](modulecomponents-table.md) al nuevo idioma del módulo. La transformación puede agregar o quitar filas de esta tabla.
-   Si es necesario, cambie el idioma de la columna RequiredLanguage o agregue o elimine filas a la [tabla ModuleDependency](moduledependency-table.md).
-   Si es necesario, cambie el idioma de la columna ExcludedLanguage o agregue o elimine filas a la [tabla ModuleExclusion](moduleexclusion-table.md).
-   La transformación puede realizar cualquier operación de transformación válida en el módulo, incluida la adición o eliminación de componentes, archivos, entradas del Registro o acciones.

Tenga en cuenta que la aplicación de una transformación de idioma al abrir el módulo no cambia el idioma predeterminado ni los idiomas admitidos por el módulo, solo cambia el idioma que se solicita. Por lo [**tanto,**](template-summary.md) la propiedad Resumen de plantilla no cambia, ya debería enumerar todos los idiomas admitidos por el módulo con el idioma predeterminado enumerado primero.

Todos los archivos necesarios para todas las transformaciones de lenguaje posibles se almacenan normalmente en un único archivo de archivador incluido con el módulo. Dado que no es práctico hacer que la transformación de lenguaje modifique este archivo de [](file-table.md)archivador, es mejor usar una secuencia de archivos global en el archivo de archivador, la tabla de archivos y la transformación de lenguaje. Para obtener más información, [vea Ordenar la secuencia de archivos en la CAB de un módulo de combinación de varios lenguajes.](ordering-the-file-sequence-in-the-cab-of-a-multiple-language-merge-module.md)

 

 



