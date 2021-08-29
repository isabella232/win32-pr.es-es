---
description: El método Render inicializa el gráfico de filtro de DVD.
ms.assetid: 910f1e3f-b3bb-498b-93da-3a974a3117e8
title: Método Render
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f1aa3abc4453478cd9d6399cb984dfd808b24e31168b8d2ab89b085a6070bb9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119904515"
---
# <a name="render-method"></a>Método Render

> [!Note]  
> Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003. En versiones posteriores podría modificarse o no estar disponible.

 

El `Render` método inicializa el gráfico de filtro de DVD.

``` syntax
MSWebDVD.Render(iRender = 0)
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="iRender"></span><span id="irender"></span><span id="IRENDER"></span>*iRender*
</dt> <dd>

Especifica un valor entero que indica si el gráfico de filtro se destruirá y volverá a generar.



| Value | Descripción                                                                                         |
|-------|-----------------------------------------------------------------------------------------------------|
| 0     | El gráfico de filtros no se destruirá y volverá a generar si ya existe. Este es el valor predeterminado. |
| 1     | El gráfico de filtro se destruirá y volverá a generar si ya existe.                                |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Comentarios

El `Render` método permite que el objeto **MSWebDVD** inicialice completamente el gráfico DirectShow filtro subyacente durante el inicio. Esto elimina el ligero retraso que, de lo contrario, se produce cuando el usuario emite el primer comando para reproducir un disco o mostrar un menú. No hay ningún caso en el que `Render` sea necesario llamar a antes de llamar a cualquier otro método. Por ejemplo, si la aplicación llama a [**PlayTitle**](playtitle-method.md) antes de inicializar el gráfico de filtros, el objeto **MSWebDVD** llama automáticamente antes de intentar reproducir `Render` el disco.

 

 



