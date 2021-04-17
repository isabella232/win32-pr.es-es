---
description: Comience a crear el paquete de actualización copiando el paquete de instalación y el árbol de directorio de origen del producto original.
ms.assetid: 279f0ab6-a6fc-4594-af6c-5a69d6167300
title: Importar la base de datos de instalación original
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 390a51e1ef068124fcdf85142ab01406d92f9a85
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105652854"
---
# <a name="importing-original-installation-database"></a>Importar la base de datos de instalación original

Comience a crear el paquete de actualización copiando el paquete de instalación y el árbol de directorio de origen del producto original. Las instrucciones para crear el paquete de instalación para MNP2000 se proporcionan en [un ejemplo de instalación](an-installation-example.md). Debe copiar el contenido de las carpetas siguientes:

C: \\MNP2000.msi de ejemplo \\

C: \\ Bloc de notas de ejemplo \\\\

C: \\ \\ binario de ejemplo\\

C: \\ icono de muestra \\\\

Actualice el contenido de la carpeta del Bloc de notas para que coincida con el origen descrito en [planeación de una actualización principal](planning-a-major-upgrade.md). Quite todos los archivos de código fuente obsoletos, como Baseball.txt, y reemplácelos por los archivos actualizados, como Baseba01.txt. Agregue los nuevos archivos adicionales proporcionados por la actualización, como Opera01.txt.

Cambie el nombre de MNP2000.msi a MNP2001.msi. En los pasos siguientes, usará un editor de tablas para modificar esta base de datos en el archivo. msi de la actualización. Las tablas de base de datos que no se modifican explícitamente en las secciones siguientes son idénticas a las tablas de la base de datos del producto original, MNP2000.msi.

[Continuar](updating-directory-structure-for-an-upgrade.md)

 

 



