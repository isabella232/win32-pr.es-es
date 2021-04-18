---
description: Los módulos de combinación son esencialmente archivos. msi simplificados, que es la extensión de nombre de archivo de un paquete de instalación de Windows Installer. Un módulo de combinación estándar tiene una extensión de nombre de archivo. msm.
ms.assetid: 580fe58a-4636-4f9a-a68d-4fd0e281e949
title: Acerca de los módulos de combinación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c70d416b89f0979d5651480a05052e95b4d32e2f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360633"
---
# <a name="about-merge-modules"></a>Acerca de los módulos de combinación

Los módulos de combinación son esencialmente archivos. msi simplificados, que es la extensión de nombre de archivo de un paquete de instalación de Windows Installer. Un módulo de combinación estándar tiene una extensión de nombre de archivo. msm.

Un módulo de combinación no se puede instalar por sí solo porque carece de algunas tablas de base de datos vitales que se encuentran en una base de datos de instalación. Los módulos de combinación también contienen tablas adicionales que son únicas de sí mismos. Para instalar la información proporcionada por un módulo de combinación con una aplicación, primero se debe mezclar el módulo en el archivo. msi de la aplicación.

Un módulo de combinación consta de las siguientes partes:

-   [Base de datos de módulo de mezcla](merge-module-database.md) que contiene las propiedades de instalación y la lógica de configuración que entrega el módulo de combinación.
-   Referencia de la [secuencia de información de resumen del módulo de combinación que](merge-module-summary-information-stream-reference.md) describe el módulo.
-   Un archivo. cab de [MergeModule.CABinet](mergemodule-cabinet.md) almacenado como una secuencia dentro del módulo de combinación. Este archivo. cab contiene todos los archivos necesarios para los componentes que entrega el módulo de combinación.

[Varios módulos de combinación de lenguajes](multiple-language-merge-modules.md) pueden proporcionar componentes a un paquete de instalación en varios idiomas. En un módulo de combinación de varios idiomas, la base de datos contiene las propiedades de instalación y la lógica para más de un idioma y el MergeModule.CABarchivo. cab de inet incluye todos los archivos necesarios para instalar componentes con todos los idiomas admitidos por el módulo.

 

 



