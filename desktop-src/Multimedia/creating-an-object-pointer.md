---
title: Crear un puntero de objeto
description: Crear un puntero de objeto
ms.assetid: b66a2725-6ba1-4aea-b165-fe3f4da00375
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f57451e2781a94642e61365d3a6c694758f4056
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104268608"
---
# <a name="creating-an-object-pointer"></a><span data-ttu-id="c4790-103">Crear un puntero de objeto</span><span class="sxs-lookup"><span data-stu-id="c4790-103">Creating an Object Pointer</span></span>

<span data-ttu-id="c4790-104">AVIBall usa la siguiente estructura como puntero de objeto.</span><span class="sxs-lookup"><span data-stu-id="c4790-104">AVIBall uses the following structure as its object pointer.</span></span> <span data-ttu-id="c4790-105">El primer miembro de esta estructura apunta a la tabla de funciones virtuales que usa AVIBall para tener acceso a sus funciones.</span><span class="sxs-lookup"><span data-stu-id="c4790-105">The first member of this structure points to the virtual function table that AVIBall uses to access its functions.</span></span> <span data-ttu-id="c4790-106">Las aplicaciones pueden convertir esta estructura en el tipo de datos PAVISTREAM.</span><span class="sxs-lookup"><span data-stu-id="c4790-106">Applications can cast this structure to the PAVISTREAM data type.</span></span> <span data-ttu-id="c4790-107">Los métodos que usan el tipo de datos PAVISTREAM solo usan el puntero a la tabla de función virtual.</span><span class="sxs-lookup"><span data-stu-id="c4790-107">Methods that use the PAVISTREAM data type use only the pointer to the virtual function table.</span></span> <span data-ttu-id="c4790-108">Los miembros que siguen al puntero a la tabla de función virtual se usan internamente mediante AVIBall.</span><span class="sxs-lookup"><span data-stu-id="c4790-108">The members following the pointer to the virtual function table are used internally by AVIBall.</span></span>


```C++
typedef struct 
{ 
    IAVIStreamVtbl FAR * lpvtbl; 
 
    // Ball instance data. 
    ULONG     ulRefCount; 
    DWORD     fccType;  // is this audio/video? 
    int        width;    // size, in pixels, of each frame 
    int        height; 
    int        length;   // length, in frames 
    int        size; 
    COLORREF    color;    // ball color 
} AVIBALL, FAR * PAVIBALL; 

```



 

 




