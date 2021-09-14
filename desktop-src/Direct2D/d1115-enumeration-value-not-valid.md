---
title: Valor de enumeración D1115 no válido
description: Valor de enumeración D1115 no válido
ms.assetid: cfffd2b8-a7d3-4a60-8586-81d8435936a6
keywords:
- Valor de enumeración D1115 no válido de Direct2D
topic_type:
- apiref
api_name:
- D1115 Enumeration Value Not Valid
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: edcfe70c67e61a3b8bfc435adfdaa017a1c62b22
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127164097"
---
# <a name="d1115-enumeration-value-not-valid"></a>D1115: El valor de enumeración no es válido

El parámetro \[ *con* \] valor para \[ *el* método \] *interface*:: no es un valor de enumeración válido.

## <a name="placeholders"></a>Marcadores de posición

<dl> <dt>

<span id="parameter"></span><span id="PARAMETER"></span>*Parámetro*
</dt> <dd>

Nombre del parámetro que recibió el tipo inesperado.

</dd> <dt>

<span id="value"></span><span id="VALUE"></span>*Valor*
</dt> <dd>

Valor de enumeración no válido.

</dd> <dt>

<span id="interface"></span><span id="INTERFACE"></span>*Interfaz*
</dt> <dd>

Nombre de la interfaz a la que pertenece *el* método.

</dd> <dt>

<span id="method"></span><span id="METHOD"></span>*Método*
</dt> <dd>

Nombre del método que recibió el valor de enumeración no válido.

</dd> </dl> 




 

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se especifica un valor de [**enumeración D2D1 \_ RENDER TARGET \_ \_ TYPE**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_type) de 30, que está fuera del intervalo esperado.


```C++
        hr = m_pD2DFactory->CreateHwndRenderTarget(
            D2D1::RenderTargetProperties((D2D1_RENDER_TARGET_TYPE)(30)),
            D2D1::HwndRenderTargetProperties(m_hwnd, size),
            &m_pRenderTarget
            );
```



En este ejemplo se genera el siguiente mensaje de depuración:

``` syntax
D2D DEBUG ERROR - The parameter [renderTargetProperties->type] with value [30] 
for ID2D1Factory::CreateHwndRenderTarget is not a valid enumeration value.
```

## <a name="possible-causes"></a>Causas posibles

Un parámetro usó un valor de enumeración no válido.

## <a name="fixes"></a>Correcciones

Use un valor de enumeración válido.

> [!Note]  
> La capa de depuración comprueba actualmente solo los valores de enumeración individuales; no comprueba si una combinación bit a bit es válida.

 

 

 
