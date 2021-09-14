---
description: Comience a crear el paquete de actualización copiando el paquete de instalación y el árbol de directorio de origen del del producto original.
ms.assetid: 279f0ab6-a6fc-4594-af6c-5a69d6167300
title: Importar la base de datos de instalación original
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 390a51e1ef068124fcdf85142ab01406d92f9a85
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074441"
---
# <a name="importing-original-installation-database"></a>Importar la base de datos de instalación original

Comience a crear el paquete de actualización copiando el paquete de instalación y el árbol de directorio de origen del del producto original. Las instrucciones para crear el paquete de instalación para MNP2000 se proporcionan en [Un ejemplo de instalación](an-installation-example.md). Debe copiar el contenido de las carpetas siguientes:

C: \\ Ejemplo \\MNP2000.msi

C: \\ Ejemplo \\ Bloc de notas\\

C: Binario \\ de \\ ejemplo\\

C: Icono \\ de \\ ejemplo\\

Actualice el contenido de la carpeta Bloc de notas para que coincidan con el origen descrito en [Planning a Major Upgrade](planning-a-major-upgrade.md). Quite todos los archivos de origen obsoletos, como Baseball.txt, y reemplace por los archivos actualizados, como Baseba01.txt. Agregue los nuevos archivos adicionales proporcionados por la actualización, como Opera01.txt.

Cambie MNP2000.msi nombre a MNP2001.msi. En los pasos posteriores usará un editor de tablas para modificar esta base de datos en .msi archivo para la actualización. Las tablas de base de datos que no se modifican explícitamente en las secciones posteriores son idénticas a las tablas de la base de datos del producto original, MNP2000.msi.

[Continuar](updating-directory-structure-for-an-upgrade.md)

 

 



