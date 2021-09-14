---
title: Almacenamientos y Secuencias
description: Un objeto de almacenamiento es análogo a un directorio del sistema de archivos.
ms.assetid: 57b2a66d-e912-4879-b778-75f8461d211f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebc44a22779b4ae63ee7c39b55888d2ea23579f7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127073533"
---
# <a name="storages-and-streams"></a>Almacenamientos y Secuencias

Un objeto de almacenamiento es análogo a un directorio del sistema de archivos. Al igual que un directorio puede contener otros directorios y archivos, un objeto de almacenamiento puede contener otros objetos de almacenamiento y objetos de secuencia. Al igual que un directorio, un objeto de almacenamiento realiza un seguimiento de las ubicaciones y tamaños de los objetos de almacenamiento y los objetos de flujo anidados debajo de él.

Un objeto de secuencia es análogo a la noción tradicional de un archivo. Al igual que un archivo, una secuencia contiene datos almacenados como una secuencia consecutiva de bytes.

Un archivo compuesto COM consta de un objeto de almacenamiento raíz que contiene al menos un objeto de secuencia que representa sus datos nativos junto con uno o varios objetos de almacenamiento correspondientes a sus objetos vinculados e incrustados. El objeto de almacenamiento raíz se asigna a un nombre de archivo en cualquier sistema de archivos en el que resida. Cada uno de los objetos dentro del documento también se representa mediante un objeto de almacenamiento que contiene uno o varios objetos de flujo, y quizás también contiene uno o varios objetos de almacenamiento. De este modo, un documento puede constar de un número ilimitado de objetos anidados. Para obtener más información, vea [Compound Files](compound-files.md).

 

 




