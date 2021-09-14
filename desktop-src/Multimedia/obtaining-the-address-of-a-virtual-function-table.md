---
title: Obtener la dirección de una tabla de función virtual
description: Obtener la dirección de una tabla de función virtual
ms.assetid: c9e9e2df-75e6-4684-a465-6905e76b10a2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c0d618e75d2c3a4fcc2550fca7cb90bd2a51d2f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127169629"
---
# <a name="obtaining-the-address-of-a-virtual-function-table"></a>Obtener la dirección de una tabla de función virtual

En una aplicación escrita en el lenguaje de programación C, puede recuperar la dirección de la estructura **IAVIStreamVtbl** mediante la función NewBall. Esta función devuelve la dirección de una estructura que contiene un puntero a **IAVIStreamVtbl**. La información siguiente **al puntero IAVIStreamVtbl** especifica los datos usados internamente por AVIBall. El controlador de secuencias puede anexar su propia información después del **puntero IAVIStreamVtbl.** Esta información se devuelve en llamadas posteriores al controlador de secuencias.


```C++
PAVISTREAM WINAPI NewBall(VOID) 
{ 
    PAVIBALL pball; 
    pball = (PAVIBALL) GlobalAllocPtr(GHND, sizeof(AVIBALL)); 
    if (!pball) 
        return 0; 
    pball->lpvtbl = &AVIBallHandler; 
    pball->lpvtbl->Create((PAVISTREAM) pball, 0, 0); 
    return (PAVISTREAM) pball; 
} 
```



 

 




