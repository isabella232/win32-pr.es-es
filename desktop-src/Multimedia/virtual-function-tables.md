---
title: Tablas de funciones virtuales
description: Tablas de funciones virtuales
ms.assetid: 1b7c6da6-3156-46fe-a9ca-0c1717fe28b5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31b403debddeecbbfe099224943ac6cdf0a1875dff9c19ea08a96e9cb029875a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118135502"
---
# <a name="virtual-function-tables"></a>Tablas de funciones virtuales

Una tabla de función virtual es una matriz de punteros a los métodos que admite un objeto. Si usa C, un objeto aparece como una estructura cuyo primer miembro es un puntero a la tabla de función virtual (**lpVtbl**); es decir, el primer miembro apunta a una matriz que contiene punteros de función. Todos los métodos toman un puntero a la tabla de funciones como primer parámetro. Por lo tanto, en el ejemplo siguiente se llama **al método Read** de un objeto **pStream:**


```C++
pStream->lpVtbl->Read(pStream, parameters) 
 
```



En C+ + , el puntero a la tabla de función virtual, *el puntero this,* es implícito. Lo siguiente es equivalente al ejemplo anterior cuando se usa C+ +:


```C++
pStream->Read(parameters) 
 
```



 

 




