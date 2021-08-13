---
description: Los módulos de combinación se simplifican .msi archivos, que es la extensión de nombre de archivo para un Windows instalación del instalador. Un módulo de combinación estándar tiene una extensión de nombre de archivo .msm.
ms.assetid: 580fe58a-4636-4f9a-a68d-4fd0e281e949
title: Acerca de los módulos de combinación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca3e6c0ec1d4d7073d85984539ce54b47de92885a64570bc1de709be64748b22
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118640167"
---
# <a name="about-merge-modules"></a>Acerca de los módulos de combinación

Los módulos de combinación se simplifican .msi archivos, que es la extensión de nombre de archivo para un Windows instalación del instalador. Un módulo de combinación estándar tiene una extensión de nombre de archivo .msm.

Un módulo de combinación no se puede instalar por sí solo porque carece de algunas tablas de base de datos vitales que están presentes en una base de datos de instalación. Los módulos de combinación también contienen tablas adicionales que son únicas para sí mismos. Para instalar la información que entrega un módulo de combinación con una aplicación, primero debe combinarse en el archivo de .msi aplicación.

Un módulo de combinación consta de las siguientes partes:

-   Base [de datos de módulos de mezcla](merge-module-database.md) que contiene las propiedades de instalación y la lógica de instalación que entrega el módulo de mezcla.
-   Referencia [de flujo de información de resumen del módulo de mezcla](merge-module-summary-information-stream-reference.md) que describe el módulo.
-   Un [MergeModule.CABarchivo de archivador de](mergemodule-cabinet.md) conjunto almacenado como una secuencia dentro del módulo de combinación. Este archivador contiene todos los archivos requeridos por los componentes entregados por el módulo de combinación.

[Varios módulos de combinación de](multiple-language-merge-modules.md) idiomas pueden entregar componentes a un paquete de instalación en varios idiomas. En un módulo de combinación de varios idiomas, la base de datos contiene las propiedades de instalación y la lógica para más de un idioma, y el archivador de conjunto de MergeModule.CABincluye todos los archivos necesarios para instalar componentes con todos los idiomas admitidos por el módulo.

 

 



