---
description: Todos los archivos que el módulo de mezcla entrega al paquete de instalación de destino deben almacenarse dentro de un archivo de archivador insertado como una secuencia dentro del archivo .msm. El nombre de este archivador siempre MergeModule.CABinet.
ms.assetid: 884df249-977e-4e8e-8978-15331a7c1d8a
title: Generación de MergeModule.CABarchivos de archivo de conjunto de elementos no cifrados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 962cf46b95db1fe186878d23a7cc7fcd1b91d3b2d202a85741eee7ef1c2bc7e7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119649655"
---
# <a name="generating-mergemodulecabinet-cabinet-files"></a>Generación de MergeModule.CABarchivos de archivo de conjunto de elementos no cifrados

Todos los archivos que el módulo de mezcla entrega al paquete de instalación de destino deben almacenarse dentro de un archivo de archivador insertado como una secuencia dentro del archivo .msm. El nombre de este archivador siempre MergeModule.CABinet.

Los nombres de los archivos del conjunto de MergeModule.CABdeben coincidir con [](file-table.md) las claves principales usadas en la tabla File del módulo de mezcla y deben cumplir la convención descrita en [Naming Primary Keys in Merge Module Databases](naming-primary-keys-in-merge-module-databases.md).

El instalador omite los archivos adicionales incluidos MergeModule.CABconjunto de integración que no aparecen en la tabla [File del módulo de mezcla](file-table.md). No es necesario que los números de secuencia de los archivos especificados en la tabla File sean consecutivos, pero deben seguir la misma secuencia que los archivos almacenados en MergeModule.CABinet. Para obtener más información, vea [Crear tablas de archivo de módulo de mezcla](authoring-merge-module-file-tables.md).

Esto significa que un único archivo de archivador puede contener todos los archivos necesarios para que un módulo de combinación admita varios idiomas. A todos los archivos de idioma se les pueden dar números de secuencia únicos en el gabinete y, a continuación, se puede usar una transformación de lenguaje para agregar o quitar archivos de la tabla Archivo para obtener un módulo de combinación para un idioma determinado. Para obtener más información, [vea Creación de módulos de combinación de varios lenguajes.](authoring-multiple-language-merge-modules.md)

MergeModule.CABconjunto de integración se puede agregar al módulo de combinación abriendo una tabla [ \_ Secuencias tabla](-streams-table.md). Por ejemplo, la herramienta Msidb.exe con el SDK del instalador de Windows se puede usar para agregar el conjunto de MergeModule.CABal módulo de combinación. Para obtener más información, vea [Incluir un archivo archivador en una instalación de](including-a-cabinet-file-in-an-installation.md).

 

 



