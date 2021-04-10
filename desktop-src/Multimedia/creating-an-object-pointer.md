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
# <a name="creating-an-object-pointer"></a>Crear un puntero de objeto

AVIBall usa la siguiente estructura como puntero de objeto. El primer miembro de esta estructura apunta a la tabla de funciones virtuales que usa AVIBall para tener acceso a sus funciones. Las aplicaciones pueden convertir esta estructura en el tipo de datos PAVISTREAM. Los métodos que usan el tipo de datos PAVISTREAM solo usan el puntero a la tabla de función virtual. Los miembros que siguen al puntero a la tabla de función virtual se usan internamente mediante AVIBall.


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



 

 




