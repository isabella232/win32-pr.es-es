---
title: Generador incorrecto D1108
ms.assetid: eb851118-0541-4c9a-a22d-b98f041852bb
description: La fábrica 1 asignó el recurso y se usó con la fábrica 2.
keywords:
- D1108 Factoría incorrecta Direct2D
topic_type:
- apiref
api_name:
- D1108 Wrong Factory
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 463909abeda1410804fa4b842dbdc829c3a74271
ms.sourcegitcommit: 4e94fc75fad7b2a0f3c92a26f97e89924e59b7a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/24/2021
ms.locfileid: "122786739"
---
# <a name="d1108-wrong-factory"></a>D1108: fábrica incorrecta

La fábrica \[ *1* asignó el recurso de recursos \] \[  \] y se usó con la \[ *fábrica 2.* \]

## <a name="placeholders"></a>Marcadores de posición

<dl> <dt>

<span id="resource"></span><span id="RESOURCE"></span>*Recursos*
</dt> <dd>

Dirección de la interfaz.

</dd> <dt>

<span id="factory_1"></span><span id="FACTORY_1"></span>*factory 1*
</dt> <dd>

Dirección del generador que asignó el *recurso*.

</dd> <dt>

<span id="factory_2"></span><span id="FACTORY_2"></span>*factory 2*
</dt> <dd>

Dirección del generador con el que se *usó* el recurso.

</dd> </dl> 




 

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se crean primero dos objetos [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) habilitados para depuración; A continuación, crea una geometría a partir del primer generador y un pincel del segundo generador. Por último, llama a [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry), pasando la geometría y el pincel.


```C++
        // If you set the options.debugLevel to D2D1_DEBUG_LEVEL_NONE,
        // the debug layer is not enabled.
#if defined(DEBUG) || defined(_DEBUG)
        D2D1_FACTORY_OPTIONS options;
        options.debugLevel = D2D1_DEBUG_LEVEL_INFORMATION;

        hr = D2D1CreateFactory(
            D2D1_FACTORY_TYPE_SINGLE_THREADED,
            options,
            &m_pD2DFactory
            );
#else
        hr = D2D1CreateFactory(
            D2D1_FACTORY_TYPE_SINGLE_THREADED,
            &m_pD2DFactory
            );
#endif


        // Domain violation. Create a second Direct2D factory.
        options.debugLevel = D2D1_DEBUG_LEVEL_INFORMATION;
        hr = D2D1CreateFactory(
            D2D1_FACTORY_TYPE_SINGLE_THREADED,
            options,
            &m_pD2DFactory1
            );

        // Create a geometry from the second factory.
        hr = m_pD2DFactory1->CreateRectangleGeometry(
            D2D1::RectF(100, 50, 400, 160),
            &m_pRectangleGeometry
            );
```





<table>
<colgroup>
<col  />
</colgroup>
<thead>
<tr class="header">
<th>C++</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>        // Create a render target from the first factory.
        hr = m_pD2DFactory->CreateHwndRenderTarget(
            D2D1::RenderTargetProperties(),
            D2D1::HwndRenderTargetProperties(m_hwnd, size),
            &m_pRenderTarget
            );</code></pre></td>
</tr>
</tbody>
</table>



<table>
<colgroup>
<col  />
</colgroup>
<thead>
<tr class="header">
<th>C++</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>        if (SUCCEEDED(hr))
        {
            hr = m_pRenderTarget->CreateSolidColorBrush(
                D2D1::ColorF(D2D1::ColorF::Black, 1.0f),
                &m_pBlackBrush
                );
        }</code></pre></td>
</tr>
</tbody>
</table>



<table>
<colgroup>
<col  />
</colgroup>
<thead>
<tr class="header">
<th>C++</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>        m_pRenderTarget->FillGeometry(
            m_pRectangleGeometry,   //The rectangle geometry created from the second factory.
            m_pBlackBrush   //The black brush created from the first factory.
            );</code></pre></td>
</tr>
</tbody>
</table>



En este ejemplo se genera el siguiente mensaje de depuración:


```
 D2D DEBUG ERROR - The resource [003BD628] was allocated 
by factory [002ED698] and used with factory [002ED470].
```



## <a name="possible-causes"></a>Causas posibles

Uso de recursos no válidos. Un recurso asignado por una factoría se usó con otro generador.

 

 
