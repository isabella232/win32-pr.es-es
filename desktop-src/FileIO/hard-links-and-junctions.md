---
description: Describe los vínculos físicos y las uniones.
ms.assetid: f9e40a86-a4a6-4524-8045-312da72dc655
title: Vínculos físicos y uniones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b8d1444db977dd95419e4cb004d2b3cb811da9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688464"
---
# <a name="hard-links-and-junctions"></a>Vínculos físicos y uniones

En el sistema de archivos NTFS se admiten tres tipos de vínculos de archivo: vínculos físicos, uniones y vínculos simbólicos. En este tema se ofrece información general sobre vínculos físicos y uniones. Para obtener información acerca de los vínculos simbólicos, consulte [crear vínculos simbólicos](creating-symbolic-links.md).

## <a name="hard-links"></a>Vínculos físicos

Un *vínculo físico* es la representación del sistema de archivos de un archivo por el que hay más de una ruta de acceso que hace referencia a un único archivo en el mismo volumen. Para crear un vínculo físico, utilice la función [**CreateHardLink**](/windows/desktop/api/WinBase/nf-winbase-createhardlinka) . Cualquier cambio que se realice en ese archivo es visible al instante en las aplicaciones que acceden a él a través de los vínculos físicos que hacen referencia a él. Sin embargo, el tamaño de la entrada de directorio y la información de atributos solo se actualizan para el vínculo a través del que se realizó el cambio. Tenga en cuenta que los atributos del archivo se reflejan en todos los vínculos físicos a ese archivo y los cambios en los atributos de ese archivo se propagan a todos los vínculos físicos. Por ejemplo, si restablece el atributo READONLY de un vínculo físico para eliminar ese vínculo físico concreto y hay varios vínculos físicos en el archivo real, deberá restablecer el bit de solo lectura en el archivo de uno de los vínculos físicos restantes para volver a colocar el archivo y todos los vínculos físicos restantes en el estado de solo lectura.

Por ejemplo, en un sistema donde C: y D: son unidades locales y Z: es una unidad de red asignada a \\ \\ Fred \\ Share, se permiten las siguientes referencias como un vínculo físico:

-   C: \\ dira \\ethel.txt vinculado a c \\ : \\ DIRB DIRC \\lucy.txt
-   D: \\ dir1 \\tinker.txt a D: \\ dir2 \\ DirX \\bell.txt
-   C: \\ DirY \\ Bob. bak vinculado a c: \\ dir2 \\mina.txt

Los siguientes elementos no son:

-   C: \\ dira vinculado a c: \\ DIRB
-   C: \\ dira \\ethel.txt vinculado a D \\ : \\ DIRBlucy.txt
-   C: \\ dira \\ethel.txt vinculado a Z \\ : \\ DIRBlucy.txt

Para eliminar un vínculo físico, utilice la función [**DeleteFile**](/windows/desktop/api/FileAPI/nf-fileapi-deletefilea) . Puede eliminar los vínculos físicos en cualquier orden, independientemente del orden en el que se hayan creado.

## <a name="junctions"></a>Uniones

Una *Unión* (también llamada *Soft Link*) difiere de un vínculo físico en que los objetos de almacenamiento a los que hace referencia son directorios independientes, y una Unión puede vincular directorios ubicados en diferentes volúmenes locales en el mismo equipo. De lo contrario, las uniones funcionan de manera idéntica a los vínculos físicos. Las uniones se implementan a través de [puntos de reanálisis](reparse-points.md).

Suponiendo las mismas condiciones en la sección de vínculos físicos, se permiten las siguientes referencias como uniones:

-   C: \\ dira vinculado a c: \\ DIRB \\ DIRC
-   C: \\ Celda DirX vinculada a D: \\ DirY

Los siguientes elementos no son:

-   C: \\ dira \\one.txt vinculado a C \\ : \\ DIRBtwo.txt
-   C: \\ dir1 vinculado a Z: \\ dir2

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Crear vínculos simbólicos](creating-symbolic-links.md)
</dt> </dl>

 

 



