---
description: Controlar gráficos de filtro mediante C
ms.assetid: 56e41f0a-2ea6-422c-8d3f-7849e91e3731
title: Controlar gráficos de filtro mediante C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e234413f7642d7349c2bf378d1aded97b399e252117b0793f90335de8643912e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119073759"
---
# <a name="controlling-filter-graphs-using-c"></a>Controlar gráficos de filtro mediante C

Si está escribiendo una aplicación DirectShow en C (en lugar de C++), debe usar un puntero vtable para llamar a métodos. En el ejemplo siguiente se muestra cómo llamar al **método IUnknown::QueryInterface** desde una aplicación escrita en C:


```C++
pGraph->lpVtbl->QueryInterface(pGraph, &IID_IMediaEvent, (void **)&pEvent);
```



A continuación se muestra la llamada equivalente en C++:


```C++
pGraph->QueryInterface(IID_IMediaEvent, (void **)&pEvent);
```



En C, las interfaces COM se definen como estructuras. El **miembro lpVtbl** es un puntero a una tabla de métodos de interfaz (la tabla virtual). Todos los métodos toman un parámetro adicional, que es un puntero a la interfaz .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Apéndices](appendixes.md)
</dt> </dl>

 

 



