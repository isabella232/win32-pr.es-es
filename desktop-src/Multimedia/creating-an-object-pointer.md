---
title: Crear un puntero de objeto
description: Crear un puntero de objeto
ms.assetid: b66a2725-6ba1-4aea-b165-fe3f4da00375
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f57451e2781a94642e61365d3a6c694758f4056
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124371672"
---
# <a name="creating-an-object-pointer"></a>Crear un puntero de objeto

AVIBall usa la siguiente estructura como puntero de objeto. El primer miembro de esta estructura apunta a la tabla de funciones virtuales que USA AVIBall para acceder a sus funciones. Las aplicaciones pueden convertir esta estructura al tipo de datos PAVISTREAM. Los métodos que usan el tipo de datos PAVISTREAM usan solo el puntero a la tabla de funciones virtuales. AVIBall usa internamente los miembros que sigue al puntero a la tabla de funciones virtuales.


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



 

 




