---
description: Control de gráficos de filtro mediante C
ms.assetid: 56e41f0a-2ea6-422c-8d3f-7849e91e3731
title: Control de gráficos de filtro mediante C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ce6d78875c6b0d5f028ea89dfbd2b061285f1c1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127161571"
---
# <a name="controlling-filter-graphs-using-c"></a>Control de gráficos de filtro mediante C

Si está escribiendo una aplicación DirectShow en C (en lugar de C++), debe usar un puntero vtable para llamar a métodos. En el ejemplo siguiente se muestra cómo llamar al **método IUnknown::QueryInterface** desde una aplicación escrita en C:


```C++
pGraph->lpVtbl->QueryInterface(pGraph, &IID_IMediaEvent, (void **)&pEvent);
```



A continuación se muestra la llamada equivalente en C++:


```C++
pGraph->QueryInterface(IID_IMediaEvent, (void **)&pEvent);
```



En C, las interfaces COM se definen como estructuras. El **miembro lpVtbl** es un puntero a una tabla de métodos de interfaz (vtable). Todos los métodos toman un parámetro adicional, que es un puntero a la interfaz .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Apéndices](appendixes.md)
</dt> </dl>

 

 



