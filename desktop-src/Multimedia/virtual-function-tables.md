---
title: Tablas de función virtual
description: Tablas de función virtual
ms.assetid: 1b7c6da6-3156-46fe-a9ca-0c1717fe28b5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a784a027f7e1120d8e7092aa5dd6c0f5c0e958b3
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124372548"
---
# <a name="virtual-function-tables"></a>Tablas de función virtual

Una tabla de función virtual es una matriz de punteros a los métodos que admite un objeto . Si usa C, un objeto aparece como una estructura cuyo primer miembro es un puntero a la tabla de funciones virtuales (**lpVtbl**); Es decir, el primer miembro apunta a una matriz que contiene punteros de función. Todos los métodos toman un puntero a la tabla de funciones como primer parámetro. Por lo tanto, en el ejemplo siguiente se llama **al método Read** de un objeto **pStream:**


```C++
pStream->lpVtbl->Read(pStream, parameters) 
 
```



En C+ + , el puntero a la tabla de funciones virtuales, *el puntero this,* es implícito. Lo siguiente es equivalente al ejemplo anterior cuando se usa C+ +:


```C++
pStream->Read(parameters) 
 
```



 

 




