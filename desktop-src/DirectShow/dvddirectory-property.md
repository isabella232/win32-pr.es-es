---
description: La propiedad DVDDirectory establece o recupera el directorio actual del volumen de DVD actual.
ms.assetid: 0dbfdf28-cda5-41b2-82ce-114d9b940d91
title: Propiedad DVDDirectory
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36515c931fb8669db814886dfff12a4bf85bde28
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103906630"
---
# <a name="dvddirectory-property"></a><span data-ttu-id="f00dc-103">Propiedad DVDDirectory</span><span class="sxs-lookup"><span data-stu-id="f00dc-103">DVDDirectory Property</span></span>

> [!Note]  
> <span data-ttu-id="f00dc-104">Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="f00dc-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="f00dc-105">En versiones posteriores podría modificarse o no estar disponible.</span><span class="sxs-lookup"><span data-stu-id="f00dc-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="f00dc-106">La `DVDDirectory` propiedad establece o recupera el directorio actual del volumen de DVD actual.</span><span class="sxs-lookup"><span data-stu-id="f00dc-106">The `DVDDirectory` property sets or retrieves the current directory of the current DVD volume.</span></span>

``` syntax
[ sDirPath = ] MSWebDVD.DVDDirectory
```

## <a name="return-value"></a><span data-ttu-id="f00dc-107">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f00dc-107">Return Value</span></span>

<span data-ttu-id="f00dc-108">Devuelve un valor de cadena que indica la ruta de acceso al directorio raíz del DVD.</span><span class="sxs-lookup"><span data-stu-id="f00dc-108">Returns a string value indicating the path to the DVD root directory.</span></span>

## <a name="remarks"></a><span data-ttu-id="f00dc-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f00dc-109">Remarks</span></span>

<span data-ttu-id="f00dc-110">Esta propiedad es de lectura/escritura y no tiene ningún valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="f00dc-110">This property is read/write with no default value.</span></span> <span data-ttu-id="f00dc-111">Use este método para establecer la ruta de acceso raíz cuando hay más de una unidad de DVD en un sistema.</span><span class="sxs-lookup"><span data-stu-id="f00dc-111">Use this method to set the root path when there is more than one DVD drive on a system.</span></span> <span data-ttu-id="f00dc-112">Cuando solo hay una unidad en el sistema y su letra de unidad es superior a "C", el objeto MSWebDVD lo encuentra automáticamente.</span><span class="sxs-lookup"><span data-stu-id="f00dc-112">When there is only one drive on the system and its drive letter is higher than "C", the MSWebDVD object finds it automatically.</span></span> <span data-ttu-id="f00dc-113">En el caso de un disco de DVD-Video estándar, la ruta de acceso raíz debe incluir el directorio de vídeo de TS \_ :</span><span class="sxs-lookup"><span data-stu-id="f00dc-113">For a standard DVD-Video disc, the root path should include the ts\_video directory:</span></span>


```VB
MSWebDVD.DVDDirectory = "e:\\video_ts"
```



<span data-ttu-id="f00dc-114">Algunos volúmenes de DVD pueden tener su vídeo en un directorio cuyo nombre no sea "vídeo \_ TS".</span><span class="sxs-lookup"><span data-stu-id="f00dc-114">Some DVD volumes may have their video in a directory named something other than "video\_ts."</span></span> <span data-ttu-id="f00dc-115">La idea general es que un "volumen de DVD" adicional (el conjunto de. IFO.</span><span class="sxs-lookup"><span data-stu-id="f00dc-115">The general idea is that an additional "DVD volume" (the set of .IFO.</span></span> <span data-ttu-id="f00dc-116">VOB, y. Los archivos BUP que normalmente se almacenarían en el \_ Directorio de vídeo TS se pueden colocar en un subdirectorio del disco. Al cambiar la raíz para que apunte a este directorio, MSWebDVD funcionará en este volumen de DVD independiente.</span><span class="sxs-lookup"><span data-stu-id="f00dc-116">VOB, and .BUP files that would normally be stored in the VIDEO\_TS directory) can be placed in a subdirectory on the disc. By changing the root to point to this directory, MSWebDVD will operate on this separate DVD volume.</span></span> <span data-ttu-id="f00dc-117">Hay disponible un nuevo conjunto de menús, títulos, etc., independientemente de los títulos de la raíz de TS de vídeo \_ , que ya no serán accesibles.</span><span class="sxs-lookup"><span data-stu-id="f00dc-117">A new set of menus, titles, and so on will be available, independent of the titles in the VIDEO\_TS root, which will no longer be accessible.</span></span> <span data-ttu-id="f00dc-118">Estos directorios se denominan "directorios ocultos".</span><span class="sxs-lookup"><span data-stu-id="f00dc-118">Such directories are called "hidden directories."</span></span> <span data-ttu-id="f00dc-119">En el ejemplo siguiente se muestra cómo establecer un directorio oculto como raíz, donde "Hidden" es un marcador de posición para el nombre que los autores del disco han asignado al directorio.</span><span class="sxs-lookup"><span data-stu-id="f00dc-119">The following example shows how to set a hidden directory as the root, where "hidden" is a placeholder for whatever name the disc authors have given to the directory.</span></span>


```VB
MSWebDVD.DVDDirectory = "d:\\webdvd\\hidden"
```



 

 



