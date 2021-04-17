---
description: Cada archivo que se entrega al paquete de instalación de destino mediante el módulo de combinación debe almacenarse en un archivo. cab incrustado como una secuencia dentro del archivo. msm. El nombre de este archivo. cab siempre es MergeModule.CABinet.
ms.assetid: 884df249-977e-4e8e-8978-15331a7c1d8a
title: Generación de archivos. cab de MergeModule.CABinet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a26eb9bb3daf92d81e21267b2f56706b74d9179
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667786"
---
# <a name="generating-mergemodulecabinet-cabinet-files"></a>Generación de archivos. cab de MergeModule.CABinet

Cada archivo que se entrega al paquete de instalación de destino mediante el módulo de combinación debe almacenarse en un archivo. cab incrustado como una secuencia dentro del archivo. msm. El nombre de este archivo. cab siempre es MergeModule.CABinet.

Los nombres de los archivos de MergeModule.CABinet deben coincidir con las claves principales que se usan en la [tabla de archivos](file-table.md) del módulo de combinación y deben cumplir la Convención descrita en [naming Keys Primary in Merge Module Databases](naming-primary-keys-in-merge-module-databases.md).

El instalador omite los archivos adicionales incluidos en MergeModule.CABinet que no aparecen en la [tabla de archivos](file-table.md)del módulo de combinación. No es necesario que los números de secuencia de los archivos especificados en la tabla de archivos sean consecutivos, pero deben seguir la misma secuencia que los archivos almacenados en MergeModule.CABinet. Para obtener más información, vea [crear tablas de archivos de módulo de combinación](authoring-merge-module-file-tables.md).

Esto significa que un único archivo contenedor puede contener todos los archivos necesarios para que un módulo de combinación admita varios idiomas. Todos los archivos de idioma pueden tener números de secuencia únicos en el archivo. cab y, a continuación, se puede usar una transformación de idioma para agregar o quitar archivos de la tabla de archivos con el fin de obtener un módulo de combinación para un idioma determinado. Para obtener más información, vea [crear módulos de combinación en varios lenguajes](authoring-multiple-language-merge-modules.md).

MergeModule.CABinet se puede Agregar al módulo de fusión mediante combinación abriendo una [ \_ tabla de secuencias](-streams-table.md)temporales. Por ejemplo, la herramienta Msidb.exe proporcionado con el SDK de Windows Installer se puede usar para agregar el MergeModule.CABinet al módulo de combinación. Para obtener más información, vea [incluir un archivo. cab en una instalación de](including-a-cabinet-file-in-an-installation.md).

 

 



