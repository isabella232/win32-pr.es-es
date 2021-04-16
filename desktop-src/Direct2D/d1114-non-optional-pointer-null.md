---
title: D1114 puntero no opcional nulo
ms.assetid: 62f0f247-8359-4f75-b3ce-195202d491d5
description: 'El parámetro de la interfaz:: Method no es opcional. Se pasó un puntero nulo. Esto hará que se bloquee Direct2D.'
keywords:
- D1114 un puntero no opcional NULL Direct2D
topic_type:
- apiref
api_name:
- D1114 Non Optional Pointer NULL
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: abf8f070e339f2dcda5f818f5ffd5386c33d0e29
ms.sourcegitcommit: 80ee822f6ebcbcc8f60042e0d14a39ef6989c731
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/27/2021
ms.locfileid: "105650229"
---
# <a name="d1114-non-optional-pointer-null"></a>D1114: puntero nulo no opcional

El \[ *parámetro* Parameter \] para *interface*::*Method* no es opcional. Se pasó un puntero **nulo** . Esto hará que se bloquee Direct2D.

### <a name="placeholders"></a>Marcadores de posición

<dl> <dt>

<span id="parameter"></span><span id="PARAMETER"></span>*parámetro*
</dt> <dd>

Nombre del parámetro que contiene el puntero **nulo** .

</dd> <dt>

<span id="interface"></span><span id="INTERFACE"></span>*interfaz*
</dt> <dd>

Nombre de la interfaz a la que pertenece el *método* .

</dd> <dt>

<span id="method"></span><span id="METHOD"></span>*forma*
</dt> <dd>

Nombre del método que recibió el parámetro no válido.

</dd> </dl> 




 

### <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra que el método [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) recibe un puntero NULL para el parámetro *Geometry* no opcional.


```C++
        m_pRenderTarget->FillGeometry(NULL, m_pYellowGreenBrush);
```



Este ejemplo genera el siguiente mensaje de depuración:

``` syntax
D2D DEBUG ERROR - The parameter [geometry] for ID2D1RenderTarget::FillGeometry is not optional. 
A NULL pointer was passed. This will cause Direct2D to crash.
```

## <a name="possible-causes"></a>Causas posibles

Se pasó un puntero NULL para un parámetro no opcional.

## <a name="fixes"></a>Correcciones

Asegúrese de que un parámetro no opcional no tiene un puntero nulo.

 

 
