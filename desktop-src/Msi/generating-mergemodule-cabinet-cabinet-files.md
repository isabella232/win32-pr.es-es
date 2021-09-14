---
description: Todos los archivos que el módulo de mezcla entrega al paquete de instalación de destino deben almacenarse dentro de un archivo de archivador insertado como una secuencia dentro del archivo .msm. El nombre de este archivador es siempre MergeModule.CABinet.
ms.assetid: 884df249-977e-4e8e-8978-15331a7c1d8a
title: Generar archivos de archivador MergeModule.CABinet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a26eb9bb3daf92d81e21267b2f56706b74d9179
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074736"
---
# <a name="generating-mergemodulecabinet-cabinet-files"></a>Generar archivos de archivador MergeModule.CABinet

Todos los archivos que el módulo de mezcla entrega al paquete de instalación de destino deben almacenarse dentro de un archivo de archivador insertado como una secuencia dentro del archivo .msm. El nombre de este archivador es siempre MergeModule.CABinet.

Los nombres de los archivos de MergeModule.CABinet deben coincidir [](file-table.md) con las claves principales usadas en la tabla File del módulo de mezcla y deben cumplir la convención descrita en [Naming Primary Keys in Merge Module Databases](naming-primary-keys-in-merge-module-databases.md).

El instalador omite los archivos adicionales incluidos en MergeModule.CABinet que no aparecen en la tabla [Archivo del módulo de mezcla](file-table.md). No es necesario que los números de secuencia de los archivos especificados en la tabla File sean consecutivos, pero deben seguir la misma secuencia que los archivos almacenados en MergeModule.CABinet. Para obtener más información, vea [Crear tablas de archivo de módulo de mezcla](authoring-merge-module-file-tables.md).

Esto significa que un único archivo de archivador puede contener todos los archivos necesarios para que un módulo de combinación admita varios idiomas. A todos los archivos de idioma se les pueden dar números de secuencia únicos en el archivador y, a continuación, se puede usar una transformación de idioma para agregar o quitar archivos de la tabla Archivo para obtener un módulo de combinación para un idioma determinado. Para obtener más información, [vea Creación de módulos de combinación de varios lenguajes.](authoring-multiple-language-merge-modules.md)

MergeModule.CABinet se puede agregar al módulo merge abriendo una tabla [ \_ Secuencias tabla](-streams-table.md). Por ejemplo, la herramienta Msidb.exe con el SDK del instalador de Windows se puede usar para agregar MergeModule.CABinet al módulo merge. Para obtener más información, vea [Incluir un archivo archivador en una instalación de](including-a-cabinet-file-in-an-installation.md).

 

 



