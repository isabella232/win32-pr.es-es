---
description: En este ejemplo se muestra cómo localizar el paquete Windows Installer descrito en un ejemplo de instalación. El paquete de instalación original se ha cambiado de una versión en inglés al idioma francés.
ms.assetid: b14787fe-3179-47d7-8a15-da45987d613f
title: Un ejemplo de localización
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d5ae0b04e65383d665e2532d45f0cc2eed856a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667074"
---
# <a name="a-localization-example"></a>Un ejemplo de localización

En este ejemplo se muestra cómo localizar el paquete Windows Installer descrito en [un ejemplo de instalación](an-installation-example.md). El paquete de instalación original se ha cambiado de una versión en inglés al idioma francés.

El ejemplo de localización tiene las siguientes especificaciones:

-   La interfaz de usuario de instalación de la aplicación MNP2000 debe cambiarse de inglés a francés.
-   La versión en francés de MNP2000 incluye Readme.txt y Help.txt archivos escritos en el idioma francés.
-   La versión en francés incluye una lista de los agentes de viaje en Francia que pueden proporcionar vales al terreno de estacionamiento rojo. Esta lista (proporcionada como un nuevo archivo, Fre.txt) no forma parte de la versión en inglés.

El procedimiento general para localizar una instalación de se describe en la sección [localizar un paquete de Windows Installer](localizing-a-windows-installer-package.md).

Copie la versión en Inglés de MNP2000.msi y todos los archivos de código fuente descritos en [planificación de la instalación](planning-the-installation.md) en una nueva carpeta. Cambie el nombre del MNP2000.msi en la carpeta a MNPFren.msi. En las secciones siguientes, modificará esta copia para localizar la aplicación en francés.

[Continuar](checking-the-installation-database-code-page.md)

 

 



