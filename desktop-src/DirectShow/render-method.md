---
description: El método Render inicializa el gráfico de filtros de DVD.
ms.assetid: 910f1e3f-b3bb-498b-93da-3a974a3117e8
title: Método Render
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 677abab1c669642c1e51e0041c98949d923147c7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105677091"
---
# <a name="render-method"></a>Método Render

> [!Note]  
> Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003. En versiones posteriores podría modificarse o no estar disponible.

 

El `Render` método inicializa el gráfico de filtros de DVD.

``` syntax
MSWebDVD.Render(iRender = 0)
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="iRender"></span><span id="irender"></span><span id="IRENDER"></span>*iRender*
</dt> <dd>

Especifica un valor entero que indica si el gráfico de filtro se destruirá y se volverá a generar.



| Value | Descripción                                                                                         |
|-------|-----------------------------------------------------------------------------------------------------|
| 0     | El gráfico de filtro no se destruirá y se volverá a generar si ya existe. Este es el valor predeterminado. |
| 1     | El gráfico de filtro se destruirá y se volverá a generar si ya existe.                                |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Observaciones

El `Render` método permite al objeto **MSWebDVD** inicializar por completo el gráfico de filtros de DirectShow subyacente en el inicio. Esto elimina el leve retraso que, de lo contrario, se produce cuando el usuario emite el primer comando para reproducir un disco o para mostrar un menú. No hay ningún caso en el que `Render` sea necesario llamar antes de llamar a cualquier otro método. Por ejemplo, si la aplicación llama a [**PlayTitle**](playtitle-method.md) antes de que se haya inicializado el gráfico de filtros, el objeto **MSWebDVD** llama `Render` automáticamente a antes de intentar reproducir el disco.

 

 



