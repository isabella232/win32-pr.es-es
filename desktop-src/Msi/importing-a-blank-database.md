---
description: Para reproducir el ejemplo, debe copiar o crear con una herramienta de software un archivo de base Windows instalador.
ms.assetid: e239bbe4-3290-40f0-9f28-0e8aa4ed23f8
title: Importar una base de datos en blanco
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d3d2c0a7b0fa8d6364a9eef66b830f94e3523c2dfece9c6e1ec459d146ace11
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118946602"
---
# <a name="importing-a-blank-database"></a>Importar una base de datos en blanco

Para reproducir el ejemplo, debe copiar o crear con una herramienta de software un archivo de base Windows instalador. Se proporciona una base de datos de instalación totalmente Schema.msi, con los componentes del SDK de Windows para Windows [instalador de .](platform-sdk-components-for-windows-installer-developers.md) El SDK también proporciona una base de datos parcialmente en blanco, uisample.msi, que contiene las tablas de secuencias sugeridas y los datos necesarios para una interfaz de usuario simple. Realice una copia de uisample.msi y muévela al mismo directorio que contiene la carpeta Bloc de notas que creó en [Planear la instalación](planning-the-installation.md)de . Cambie el nombre del archivo MNP2000.msi. Tanto el archivo de base de datos de instalación como los archivos de origen deben encontrarse en la raíz del mismo directorio. Por ejemplo:

C: \\ Ejemplo \\MNP2000.msi

C: \\ Ejemplo \\ Bloc de notas\\

Si no usa Uisample.msi, debe obtener una base de datos en blanco, como Schema.msi, y especificar información para la instalación mediante una herramienta de edición de base de datos como Orca, que se proporciona con el SDK, u otro editor de bases de datos.

[Continuar](specifying-directory-structure.md)

 

 



