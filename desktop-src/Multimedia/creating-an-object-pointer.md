---
title: Crear un puntero de objeto
description: Crear un puntero de objeto
ms.assetid: b66a2725-6ba1-4aea-b165-fe3f4da00375
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 586ba0b8c9ee261e29f21ed58c84193f4cc89d1399c62d75d82a2c0a49075dcc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119144688"
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



 

 




