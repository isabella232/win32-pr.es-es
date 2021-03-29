---
title: Almacenamiento y secuencias
description: Un objeto de almacenamiento es análogo a un directorio del sistema de archivos.
ms.assetid: 57b2a66d-e912-4879-b778-75f8461d211f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebc44a22779b4ae63ee7c39b55888d2ea23579f7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103773890"
---
# <a name="storages-and-streams"></a>Almacenamiento y secuencias

Un objeto de almacenamiento es análogo a un directorio del sistema de archivos. Del mismo modo que un directorio puede contener otros directorios y archivos, un objeto de almacenamiento puede contener otros objetos de almacenamiento y objetos de secuencia. También como un directorio, un objeto de almacenamiento realiza un seguimiento de las ubicaciones y los tamaños de los objetos de almacenamiento y los objetos de secuencia anidados debajo.

Un objeto de secuencia es análogo a la noción tradicional de un archivo. Al igual que un archivo, una secuencia contiene datos almacenados como una secuencia consecutiva de bytes.

Un archivo compuesto COM se compone de un objeto de almacenamiento raíz que contiene al menos un objeto de flujo que representa sus datos nativos junto con uno o más objetos de almacenamiento correspondientes a sus objetos vinculados e incrustados. El objeto de almacenamiento raíz se asigna a un nombre de archivo en cualquier sistema de archivos en el que se encuentre. Cada uno de los objetos incluidos en el documento también se representa mediante un objeto de almacenamiento que contiene uno o más objetos de flujo y quizás también contiene uno o varios objetos de almacenamiento. De esta manera, un documento puede constar de un número ilimitado de objetos anidados. Para obtener más información, vea [archivos compuestos](compound-files.md).

 

 




