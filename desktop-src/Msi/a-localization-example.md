---
description: En este ejemplo se muestra cómo encontrar el paquete Windows Installer descrito en Un ejemplo de instalación. El paquete de instalación original se cambia de una versión en inglés a francés.
ms.assetid: b14787fe-3179-47d7-8a15-da45987d613f
title: Ejemplo de localización
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4ef7ae0fdfa13ffa95956262250b0cb0c7db33c2b7ccd7741136d88b6727a2c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118382245"
---
# <a name="a-localization-example"></a>Ejemplo de localización

En este ejemplo se muestra cómo encontrar el paquete Windows installer descrito en [Un ejemplo de instalación](an-installation-example.md). El paquete de instalación original se cambia de una versión en inglés a francés.

El ejemplo de localización tiene las especificaciones siguientes:

-   La interfaz de usuario de instalación de la aplicación MNP2000 debe cambiarse de inglés a francés.
-   La versión en francés de MNP2000 incluye Readme.txt y Help.txt archivos escritos en francés.
-   La versión en francés incluye una lista de agentes de viajes en Francia que pueden proporcionar entradas a Red Park Campos. Esta lista (proporcionada como un nuevo archivo, Fre.txt) no forma parte de la versión en inglés.

El procedimiento general para la localización de una instalación se describe en la sección [Localización de un Windows installer .](localizing-a-windows-installer-package.md)

Copie la versión en inglés de MNP2000.msi y todos los archivos de origen descritos en Planning the Installation into a new folder [(Planeación](planning-the-installation.md) de la instalación en una carpeta nueva). Cambie el nombre de la MNP2000.msi de la carpeta a MNPFren.msi. En las secciones siguientes modificará esta copia para que localice la aplicación en francés.

[Continuar](checking-the-installation-database-code-page.md)

 

 



