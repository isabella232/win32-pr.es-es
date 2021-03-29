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
# <a name="storages-and-streams"></a><span data-ttu-id="7ad1e-103">Almacenamiento y secuencias</span><span class="sxs-lookup"><span data-stu-id="7ad1e-103">Storages and Streams</span></span>

<span data-ttu-id="7ad1e-104">Un objeto de almacenamiento es análogo a un directorio del sistema de archivos.</span><span class="sxs-lookup"><span data-stu-id="7ad1e-104">A storage object is analogous to a file system directory.</span></span> <span data-ttu-id="7ad1e-105">Del mismo modo que un directorio puede contener otros directorios y archivos, un objeto de almacenamiento puede contener otros objetos de almacenamiento y objetos de secuencia.</span><span class="sxs-lookup"><span data-stu-id="7ad1e-105">Just as a directory can contain other directories and files, a storage object can contain other storage objects and stream objects.</span></span> <span data-ttu-id="7ad1e-106">También como un directorio, un objeto de almacenamiento realiza un seguimiento de las ubicaciones y los tamaños de los objetos de almacenamiento y los objetos de secuencia anidados debajo.</span><span class="sxs-lookup"><span data-stu-id="7ad1e-106">Also like a directory, a storage object tracks the locations and sizes of the storage objects and stream objects nested beneath it.</span></span>

<span data-ttu-id="7ad1e-107">Un objeto de secuencia es análogo a la noción tradicional de un archivo.</span><span class="sxs-lookup"><span data-stu-id="7ad1e-107">A stream object is analogous to the traditional notion of a file.</span></span> <span data-ttu-id="7ad1e-108">Al igual que un archivo, una secuencia contiene datos almacenados como una secuencia consecutiva de bytes.</span><span class="sxs-lookup"><span data-stu-id="7ad1e-108">Like a file, a stream contains data stored as a consecutive sequence of bytes.</span></span>

<span data-ttu-id="7ad1e-109">Un archivo compuesto COM se compone de un objeto de almacenamiento raíz que contiene al menos un objeto de flujo que representa sus datos nativos junto con uno o más objetos de almacenamiento correspondientes a sus objetos vinculados e incrustados.</span><span class="sxs-lookup"><span data-stu-id="7ad1e-109">A COM compound file consists of a root storage object containing at least one stream object representing its native data along with one or more storage objects corresponding to its linked and embedded objects.</span></span> <span data-ttu-id="7ad1e-110">El objeto de almacenamiento raíz se asigna a un nombre de archivo en cualquier sistema de archivos en el que se encuentre.</span><span class="sxs-lookup"><span data-stu-id="7ad1e-110">The root storage object maps to a file name in whatever file system it happens to reside.</span></span> <span data-ttu-id="7ad1e-111">Cada uno de los objetos incluidos en el documento también se representa mediante un objeto de almacenamiento que contiene uno o más objetos de flujo y quizás también contiene uno o varios objetos de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="7ad1e-111">Each of the objects inside the document also is represented by a storage object containing one or more stream objects, and perhaps also containing one or more storage objects.</span></span> <span data-ttu-id="7ad1e-112">De esta manera, un documento puede constar de un número ilimitado de objetos anidados.</span><span class="sxs-lookup"><span data-stu-id="7ad1e-112">In this way, a document can consist of an unlimited number of nested objects.</span></span> <span data-ttu-id="7ad1e-113">Para obtener más información, vea [archivos compuestos](compound-files.md).</span><span class="sxs-lookup"><span data-stu-id="7ad1e-113">For more information, see [Compound Files](compound-files.md).</span></span>

 

 




