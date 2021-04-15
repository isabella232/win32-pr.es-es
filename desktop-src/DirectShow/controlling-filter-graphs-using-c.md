---
description: Controlar gráficos de filtros mediante C
ms.assetid: 56e41f0a-2ea6-422c-8d3f-7849e91e3731
title: Controlar gráficos de filtros mediante C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ce6d78875c6b0d5f028ea89dfbd2b061285f1c1
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104422988"
---
# <a name="controlling-filter-graphs-using-c"></a>Controlar gráficos de filtros mediante C

Si está escribiendo una aplicación de DirectShow en C (en lugar de C++), debe usar un puntero vtable para llamar a métodos. En el ejemplo siguiente se muestra cómo llamar al método **IUnknown:: QueryInterface** desde una aplicación escrita en C:


```C++
pGraph->lpVtbl->QueryInterface(pGraph, &IID_IMediaEvent, (void **)&pEvent);
```



A continuación se muestra la llamada equivalente en C++:


```C++
pGraph->QueryInterface(IID_IMediaEvent, (void **)&pEvent);
```



En C, las interfaces COM se definen como estructuras. El miembro **lpVtbl** es un puntero a una tabla de métodos de interfaz (vtable). Todos los métodos toman un parámetro adicional, que es un puntero a la interfaz.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Apéndices](appendixes.md)
</dt> </dl>

 

 



