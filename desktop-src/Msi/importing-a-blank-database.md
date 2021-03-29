---
description: Para reproducir el ejemplo, debe copiar, o crear con una herramienta de software, un archivo de base de datos de Windows Installer.
ms.assetid: e239bbe4-3290-40f0-9f28-0e8aa4ed23f8
title: Importar una base de datos en blanco
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b654b0de118013e8f211a9b06e896cc3f486faf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277744"
---
# <a name="importing-a-blank-database"></a>Importar una base de datos en blanco

Para reproducir el ejemplo, debe copiar, o crear con una herramienta de software, un archivo de base de datos de Windows Installer. Se proporciona una base de datos de instalación totalmente vacía, Schema.msi, con los [componentes Windows SDK para Windows Installer desarrolladores](platform-sdk-components-for-windows-installer-developers.md). El SDK también proporciona una base de datos parcialmente vacía, uisample.msi, que contiene las tablas y los datos de secuencia sugeridos necesarios para una interfaz de usuario sencilla. Realice una copia de uisample.msi y muévala en el mismo directorio que contiene la carpeta del Bloc de notas que ha creado en [el planeamiento de la instalación](planning-the-installation.md). Cambie el nombre del archivo MNP2000.msi. El archivo de base de datos de instalación y los archivos de código fuente deben estar ubicados en la raíz del mismo directorio. Por ejemplo:

C: \\MNP2000.msi de ejemplo \\

C: \\ Bloc de notas de ejemplo \\\\

Si no usa Uisample.msi, debe obtener una base de datos en blanco, como Schema.msi, y especificar información para la instalación mediante una herramienta de edición de bases de datos como orca, que se proporciona con el SDK u otro editor de base de datos.

[Continuar](specifying-directory-structure.md)

 

 



