---
description: En la tabla siguiente se identifican los límites de tamaño de los distintos elementos del registro.
ms.assetid: a6d3a884-f181-46a5-b655-226c68792e08
title: Límites de tamaño de elementos del registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 262609a64e60536dcfc41f29e5d94ea499158861
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667594"
---
# <a name="registry-element-size-limits"></a><span data-ttu-id="f4572-103">Límites de tamaño de elementos del registro</span><span class="sxs-lookup"><span data-stu-id="f4572-103">Registry Element Size Limits</span></span>

<span data-ttu-id="f4572-104">En la tabla siguiente se identifican los límites de tamaño de los distintos elementos del registro.</span><span class="sxs-lookup"><span data-stu-id="f4572-104">The following table identifies the size limits for the various registry elements.</span></span>



| <span data-ttu-id="f4572-105">Elemento Registry</span><span class="sxs-lookup"><span data-stu-id="f4572-105">Registry Element</span></span> | <span data-ttu-id="f4572-106">Límite de tamaño</span><span class="sxs-lookup"><span data-stu-id="f4572-106">Size Limit</span></span>                                                                                                                                            |
|------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f4572-107">Nombre de clave</span><span class="sxs-lookup"><span data-stu-id="f4572-107">Key name</span></span>         | <span data-ttu-id="f4572-108">255 caracteres.</span><span class="sxs-lookup"><span data-stu-id="f4572-108">255 characters.</span></span> <span data-ttu-id="f4572-109">El nombre de clave incluye la ruta de acceso absoluta de la clave en el registro, que siempre comienza en una clave base, por ejemplo, HKEY \_ local \_ Machine.</span><span class="sxs-lookup"><span data-stu-id="f4572-109">The key name includes the absolute path of the key in the registry, always starting at a base key, for example, HKEY\_LOCAL\_MACHINE.</span></span> |
| <span data-ttu-id="f4572-110">Nombre del valor</span><span class="sxs-lookup"><span data-stu-id="f4572-110">Value name</span></span>       | <span data-ttu-id="f4572-111">16.383 caracteres **Windows 2000:** 260 caracteres ANSI o 16.383 caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="f4572-111">16,383 characters **Windows 2000:** 260 ANSI characters or 16,383 Unicode characters.</span></span><br/>                                                       |
| <span data-ttu-id="f4572-112">Value</span><span class="sxs-lookup"><span data-stu-id="f4572-112">Value</span></span>            | <span data-ttu-id="f4572-113">Memoria disponible (formato más reciente) 1 MB (formato estándar)</span><span class="sxs-lookup"><span data-stu-id="f4572-113">Available memory (latest format)1 MB (standard format)</span></span><br/>                                                                                     |
| <span data-ttu-id="f4572-114">Árbol</span><span class="sxs-lookup"><span data-stu-id="f4572-114">Tree</span></span>             | <span data-ttu-id="f4572-115">Un árbol del registro puede tener un nivel de 512 niveles de profundidad.</span><span class="sxs-lookup"><span data-stu-id="f4572-115">A registry tree can be 512 levels deep.</span></span> <span data-ttu-id="f4572-116">Puede crear hasta 32 niveles a la vez a través de una única llamada API del registro.</span><span class="sxs-lookup"><span data-stu-id="f4572-116">You can create up to 32 levels at a time through a single registry API call.</span></span>                                  |



 

<span data-ttu-id="f4572-117">Los valores largos (más de 2.048 bytes) deben almacenarse en un archivo y la ubicación del archivo debe estar almacenada en el registro.</span><span class="sxs-lookup"><span data-stu-id="f4572-117">Long values (more than 2,048 bytes) should be stored in a file, and the location of the file should be stored in the registry.</span></span> <span data-ttu-id="f4572-118">Esto ayuda a que el registro funcione de forma eficaz.</span><span class="sxs-lookup"><span data-stu-id="f4572-118">This helps the registry perform efficiently.</span></span>

<span data-ttu-id="f4572-119">La ubicación del archivo puede ser el nombre de un valor o los datos de un valor.</span><span class="sxs-lookup"><span data-stu-id="f4572-119">The file location can be the name of a value or the data of a value.</span></span> <span data-ttu-id="f4572-120">Cada barra diagonal inversa de la cadena de ubicación debe ir precedida de otra barra diagonal inversa como carácter de escape.</span><span class="sxs-lookup"><span data-stu-id="f4572-120">Each backslash in the location string must be preceded by another backslash as an escape character.</span></span> <span data-ttu-id="f4572-121">Por ejemplo, especifique "C: \\ \\ myDir mi \\ \\ archivo" para almacenar la cadena "c: \\ myDir \\ .</span><span class="sxs-lookup"><span data-stu-id="f4572-121">For example, specify "C:\\\\mydir\\\\myfile" to store the string "C:\\mydir\\myfile".</span></span> <span data-ttu-id="f4572-122">Una ubicación de archivo también puede ser el nombre de una clave si está dentro del límite de 255 caracteres para los nombres de clave y no contiene barras diagonales inversas, que no se permiten en los nombres de clave.</span><span class="sxs-lookup"><span data-stu-id="f4572-122">A file location can also be the name of a key if it is within the 255-character limit for key names and does not contain backslashes, which are not allowed in key names.</span></span>

 

 




