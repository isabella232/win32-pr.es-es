---
description: Para reproducir el ejemplo, debe copiar o crear con una herramienta de software un archivo de base de datos Windows Installer.
ms.assetid: e239bbe4-3290-40f0-9f28-0e8aa4ed23f8
title: Importar una base de datos en blanco
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b654b0de118013e8f211a9b06e896cc3f486faf
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074444"
---
# <a name="importing-a-blank-database"></a>Importar una base de datos en blanco

Para reproducir el ejemplo, debe copiar o crear con una herramienta de software un archivo de base de datos Windows Installer. Se proporciona una base de datos de instalación totalmente Schema.msi, con los componentes del SDK de Windows para Windows [instalador de .](platform-sdk-components-for-windows-installer-developers.md) El SDK también proporciona una base de datos parcialmente en blanco, uisample.msi, que contiene las tablas de secuencias sugeridas y los datos necesarios para una interfaz de usuario simple. Realice una copia de uisample.msi y muévela al mismo directorio que contiene la carpeta Bloc de notas que creó en [Planear la instalación](planning-the-installation.md)de . Cambie el nombre del archivo MNP2000.msi. Tanto el archivo de base de datos de instalación como los archivos de origen deben encontrarse en la raíz del mismo directorio. Por ejemplo:

C: \\ Ejemplo \\MNP2000.msi

C: \\ Ejemplo \\ Bloc de notas\\

Si no usa Uisample.msi, debe obtener una base de datos en blanco, como Schema.msi, y especificar información para la instalación mediante una herramienta de edición de base de datos como Orca, que se proporciona con el SDK, u otro editor de bases de datos.

[Continuar](specifying-directory-structure.md)

 

 



