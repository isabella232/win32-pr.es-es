---
title: Tablas de funciones virtuales
description: Tablas de funciones virtuales
ms.assetid: 1b7c6da6-3156-46fe-a9ca-0c1717fe28b5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a784a027f7e1120d8e7092aa5dd6c0f5c0e958b3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105651290"
---
# <a name="virtual-function-tables"></a>Tablas de funciones virtuales

Una tabla de funciones virtuales es una matriz de punteros a los métodos que admite un objeto. Si está utilizando C, un objeto aparece como una estructura cuyo primer miembro es un puntero a la tabla de función virtual (**lpVtbl**); es decir, el primer miembro apunta a una matriz que contiene punteros de función. Todos los métodos toman un puntero a la tabla de funciones como primer parámetro. Por lo tanto, en el ejemplo siguiente se llama al método **Read** de un objeto **pStream** :


```C++
pStream->lpVtbl->Read(pStream, parameters) 
 
```



En C + +, el puntero a la tabla de función virtual, el puntero *this* , es implícito. Lo siguiente es equivalente al ejemplo anterior al usar C + +:


```C++
pStream->Read(parameters) 
 
```



 

 




