---
description: En este ejemplo se muestra cómo encontrar el paquete Windows installer descrito en Un ejemplo de instalación. El paquete de instalación original se cambia de una versión de inglés a francés.
ms.assetid: b14787fe-3179-47d7-8a15-da45987d613f
title: Un ejemplo de localización
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4ef7ae0fdfa13ffa95956262250b0cb0c7db33c2b7ccd7741136d88b6727a2c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118382245"
---
# <a name="a-localization-example"></a>Un ejemplo de localización

En este ejemplo se muestra cómo encontrar el paquete Windows Installer descrito en [Un ejemplo de instalación](an-installation-example.md). El paquete de instalación original se cambia de una versión de inglés a francés.

El ejemplo de localización tiene las siguientes especificaciones:

-   La interfaz de usuario de instalación de la aplicación MNP2000 debe cambiarse de inglés a francés.
-   La versión en francés de MNP2000 incluye archivos Readme.txt y Help.txt escritos en francés.
-   La versión en francés incluye una lista de agentes de viajes en Francia que pueden proporcionar entradas a Red Park Arena. Esta lista (que se proporciona como un nuevo archivo, Fre.txt) no forma parte de la versión en inglés.

El procedimiento general para la localización de una instalación se describe en la sección [Localizing a Windows Installer Package](localizing-a-windows-installer-package.md).

Copie la versión en inglés de MNP2000.msi y todos los archivos de origen descritos en [Planeamiento](planning-the-installation.md) de la instalación en una carpeta nueva. Cambie el nombre de la MNP2000.msi de la carpeta a MNPFren.msi. En las secciones siguientes modificará esta copia para que la aplicación se localice en francés.

[Continuar](checking-the-installation-database-code-page.md)

 

 



