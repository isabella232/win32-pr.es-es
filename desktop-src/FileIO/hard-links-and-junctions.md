---
description: Describe los vínculos duros y las uniones.
ms.assetid: f9e40a86-a4a6-4524-8045-312da72dc655
title: Vínculos duros y uniones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b8d1444db977dd95419e4cb004d2b3cb811da9f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069931"
---
# <a name="hard-links-and-junctions"></a>Vínculos duros y uniones

Hay tres tipos de vínculos de archivo admitidos en el sistema de archivos NTFS: vínculos duros, uniones y vínculos simbólicos. Este tema es una introducción a los vínculos duros y las uniones. Para obtener información sobre los vínculos simbólicos, vea [Crear vínculos simbólicos.](creating-symbolic-links.md)

## <a name="hard-links"></a>Vínculos físicos

Un *vínculo fuerte es* la representación del sistema de archivos de un archivo por el que más de una ruta de acceso hace referencia a un único archivo en el mismo volumen. Para crear un vínculo duro, use la [**función CreateHardLink.**](/windows/desktop/api/WinBase/nf-winbase-createhardlinka) Los cambios realizados en ese archivo son visibles al instante para las aplicaciones que acceden a él a través de los vínculos duros que hacen referencia a él. Sin embargo, la información de tamaño y atributo de entrada del directorio solo se actualiza para el vínculo a través del cual se realizó el cambio. Tenga en cuenta que los atributos del archivo se reflejan en todos los vínculos duros a ese archivo y los cambios en los atributos de ese archivo se propagan a todos los vínculos duros. Por ejemplo, si restablece el atributo READONLY en un vínculo duro para eliminar ese vínculo duro concreto y hay varios vínculos duros al archivo real, deberá restablecer el bit READONLY en el archivo desde uno de los vínculos duros restantes para devolver el archivo y todos los vínculos duros restantes al estado READONLY.

Por ejemplo, en un sistema en el que C: y D: son unidades locales y Z: es una unidad de red asignada a un recurso compartido de compás, se permiten las siguientes referencias \\ \\ como un vínculo \\ duro:

-   C: \\ dira \\ethel.txt vinculado a C: \\ dirb \\ dirc \\lucy.txt
-   D: \\ dir1 \\tinker.txt a D: \\ dir2 \\ dirx \\bell.txt
-   C: \\ diry \\ bob.bak vinculado a C: \\ dir2 \\mina.txt

Los siguientes elementos no son:

-   C: \\ dira vinculado a C: \\ dirb
-   C: \\ dira \\ethel.txt vinculado a D: \\ dirb \\lucy.txt
-   C: \\ dira \\ethel.txt vinculado a Z: \\ dirb \\lucy.txt

Para eliminar un vínculo duro, use la [**función DeleteFile.**](/windows/desktop/api/FileAPI/nf-fileapi-deletefilea) Puede eliminar vínculos duros en cualquier orden, independientemente del orden en el que se creen.

## <a name="junctions"></a>Uniones

Una *unión* (también denominada vínculo *flexible)* difiere de un vínculo físico en que los objetos de almacenamiento a los que hace referencia son directorios independientes y una unión puede vincular directorios ubicados en diferentes volúmenes locales en el mismo equipo. De lo contrario, las uniones funcionan de forma idéntica a los vínculos duros. Las uniones se implementan a través [de puntos de reanción.](reparse-points.md)

Suponiendo las mismas condiciones en la sección Vínculos duros, se permiten las referencias siguientes como uniones:

-   C: \\ dira vinculado a C: \\ dirb \\ dirc
-   C: \\ dirx vinculado a D: \\ diry

Los siguientes elementos no son:

-   C: \\ dira \\one.txt vinculado a C: \\ dirb \\two.txt
-   C: \\ dir1 vinculado a Z: \\ dir2

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Crear vínculos simbólicos](creating-symbolic-links.md)
</dt> </dl>

 

 



