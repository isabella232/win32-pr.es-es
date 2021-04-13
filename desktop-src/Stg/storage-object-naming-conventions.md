---
title: Convenciones de nomenclatura de objetos de almacenamiento
description: Los nombres de los objetos de flujo y de almacenamiento se asignan según un conjunto de convenciones.
ms.assetid: 72e87c6a-cce5-4456-8336-c657e65c0a34
keywords:
- Strctd de almacenamiento estructurado STG, aspectos básicos y convenciones de nomenclatura de objetos de almacenamiento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2e828674f4165bdb54dc2ec06748ab4165e75e2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418441"
---
# <a name="storage-object-naming-conventions"></a><span data-ttu-id="cfe7a-104">Convenciones de nomenclatura de objetos de almacenamiento</span><span class="sxs-lookup"><span data-stu-id="cfe7a-104">Storage Object Naming Conventions</span></span>

<span data-ttu-id="cfe7a-105">Los nombres de los objetos de flujo y de almacenamiento se asignan según un conjunto de convenciones.</span><span class="sxs-lookup"><span data-stu-id="cfe7a-105">Storage and stream objects are named according to a set of conventions.</span></span>

<span data-ttu-id="cfe7a-106">El nombre de un objeto de almacenamiento raíz es el nombre real del archivo en el sistema de archivos subyacente.</span><span class="sxs-lookup"><span data-stu-id="cfe7a-106">The name of a root storage object is the actual name of the file in the underlying file system.</span></span> <span data-ttu-id="cfe7a-107">Se ajusta a las convenciones y restricciones que impone el sistema de archivos.</span><span class="sxs-lookup"><span data-stu-id="cfe7a-107">It conforms to the conventions and restrictions that the file system imposes.</span></span> <span data-ttu-id="cfe7a-108">Las cadenas de nombre de archivo que se pasan a los métodos y funciones relacionados con el almacenamiento se pasan al sistema de archivos, no se interpretan y sin modificar.</span><span class="sxs-lookup"><span data-stu-id="cfe7a-108">File name strings passed to storage-related methods and functions are passed on, uninterpreted and unchanged, to the file system.</span></span>

<span data-ttu-id="cfe7a-109">El nombre de un elemento anidado contenido dentro de un objeto de almacenamiento se administra mediante la implementación del objeto de almacenamiento determinado.</span><span class="sxs-lookup"><span data-stu-id="cfe7a-109">The name of a nested element contained within a storage object is managed by the implementation of the particular storage object.</span></span> <span data-ttu-id="cfe7a-110">Todas las implementaciones de objetos de almacenamiento deben admitir nombres de elementos anidados 32 caracteres de longitud (incluido el terminador **null** ), aunque algunas implementaciones podrían admitir nombres más largos.</span><span class="sxs-lookup"><span data-stu-id="cfe7a-110">All implementations of storage objects must support nested element names 32 characters in length (including the **NULL** terminator), although some implementations might support longer names.</span></span> <span data-ttu-id="cfe7a-111">Si el objeto de almacenamiento realiza una conversión de mayúsculas y minúsculas definida por la implementación.</span><span class="sxs-lookup"><span data-stu-id="cfe7a-111">Whether the storage object does any case conversion is implementation-defined.</span></span> <span data-ttu-id="cfe7a-112">Como resultado, las aplicaciones que definen nombres de elementos deben elegir nombres que sean aceptables tanto si se realiza la conversión de mayúsculas o minúsculas como si no.</span><span class="sxs-lookup"><span data-stu-id="cfe7a-112">As a result, applications that define element names must choose names that are acceptable whether or not case conversion is performed.</span></span> <span data-ttu-id="cfe7a-113">La implementación COM de archivos compuestos admite nombres con una longitud máxima de 32 caracteres y no realiza ninguna conversión de mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="cfe7a-113">The COM implementation of compound files supports names with a maximum length of 32 characters, and does not perform any case conversion.</span></span>

 

 




