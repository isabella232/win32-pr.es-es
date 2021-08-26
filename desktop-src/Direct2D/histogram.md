---
title: Efecto histograma
description: Use el efecto histograma para generar un histograma para el mapa de bits de entrada en función del número especificado de cubos.
ms.assetid: 458E2334-F383-41DE-9479-601AC3007BF3
keywords:
- efecto histograma
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08477a832b2dbf758d26a16e78905f8530d4d4525205cbc85e9d138f8b3bded7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120044425"
---
# <a name="histogram-effect"></a>Efecto histograma

Use el efecto histograma para generar un histograma para el mapa de bits de entrada en función del número especificado de cubos.

El CLSID para este efecto es CLSID \_ D2D1Histogram.

-   [Ejemplo](#example)
-   [Propiedades de efecto](#effect-properties)
-   [Selectores de canales](#channel-selectors)
-   [Salida de datos](#data-output)
-   [Comentarios:](#remarks)
-   [Requisitos](#requirements)
-   [Temas relacionados](#related-topics)

## <a name="example"></a>Ejemplo



| Antes                                                     |
|------------------------------------------------------------|
| ![la imagen antes del efecto.](images/default-before.jpg) |
| Graph de los datos de salida del histograma                         |
| ![la imagen después de la transformación.](images/33-histogram.png) |



 


```C++
ComPtr<ID2D1Effect> histogramEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Histogram, &histogramEffect);

histogramEffect->SetInputEffect(0, m_2DAffineTransformEffectRight.Get());
histogramEffect->SetValue(D2D1_HISTOGRAM_PROP_CHANNEL_SELECT, D2D1_CHANNEL_SELECTOR_G);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(histogramEffect.Get());
m_d2dContext->EndDraw();

// The histogram data is only available once the effect has been 'drawn'.
int histogramBinCount;

HRESULT hr = histogramEffect->GetValue(D2D1_HISTOGRAM_PROP_NUM_BINS, &histogramBinCount);

float *histogramData = new float[histogramBinCount];
hr = histogramEffect->GetValue(D2D1_HISTOGRAM_PROP_HISTOGRAM_OUTPUT, 
                               reinterpret_cast<BYTE*>(histogramData), 
                               histogramBinCount * sizeof(float));
```



## <a name="effect-properties"></a>Propiedades de efecto

Esta es la ecuación para generar la salida.

![ecuación para generar la salida del efecto histograma.](images/histogram-formula.png)

*i* se evalúa de 0 al número de cubos. El efecto genera un histograma para los valores de píxel entre 0 y 1. Los valores fuera de este intervalo se fijan al intervalo. El intervalo de un cubo determinado depende del número de cubos. Este efecto funciona en píxeles de mapa de bits rectas. Los canales de color del mapa de bits de entrada se dividen por el canal alfa para calcular este efecto.



| Enumeración de nombre para mostrar e índice                                             | Tipo y valor predeterminado                                                   | Descripción                                                                                                                                                                                   |
|--------------------------------------------------------------------------------|--------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| NumBins<br/> CUBOS DE NÚMERO DE PROP DE \_ HISTOGRAMA D2D1 \_ \_ \_<br/>                 | UINT32<br/> 256<br/>                                         | Especifica el número de intervalos usados para el histograma. El intervalo de valores de intensidad que se encuentra en un cubo determinado depende del número de cubos especificados.                              |
| ChannelSelect<br/> SELECCIÓN DEL CANAL DE \_ PROP DEL \_ \_ HISTOGRAMA D2D1 \_<br/>     | SELECTOR DE CANALES D2D1 \_ \_<br/> SELECTOR DE CANALES D2D1 \_ \_ \_ R<br/> | Especifica el canal utilizado para generar el histograma. Este efecto tiene una única salida de datos correspondiente al canal especificado. Consulte [Selectores de canales](#channel-selectors) para obtener más información. |
| HistogramOutput<br/> SALIDA DEL \_ HISTOGRAMA DE PROP \_ \_ HISTOGRAMA D2D1 \_<br/> | Flotador\[\]<br/> Solo propiedad de salida.<br/>                    | Matriz de salida.                                                                                                                                                                             |



 

## <a name="channel-selectors"></a>Selectores de canales



| Enumeración                | Descripción                                                           |
|----------------------------|-----------------------------------------------------------------------|
| SELECTOR DE CANALES D2D1 \_ \_ \_ R | El efecto genera la salida del histograma en función del canal rojo.   |
| SELECTOR DE CANALES D2D1 \_ \_ \_ G | El efecto genera la salida del histograma en función del canal verde. |
| SELECTOR DE CANALES D2D1 \_ \_ \_ B | El efecto genera la salida del histograma en función del canal azul.  |
| SELECTOR DE CANALES D2D1 \_ \_ \_ A | El efecto genera la salida del histograma en función del canal alfa. |



 

## <a name="data-output"></a>Salida de datos

Este efecto genera float \[ \] , con el número de elementos correspondiente al número de contenedores especificados. Cada elemento de FLOAT \[ \] es un valor float. El valor del elemento corresponde al número de elementos de esa ubicación.

## <a name="remarks"></a>Comentarios

> [!Note]  
> Se produce un error en el método [**CreateEffect**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createeffect) si el dispositivo no admite DirectCompute y devuelve HRESULT = D2DERR \_ INSUFFICIENT DEVICE \_ \_ CAPABILITIES. Todas las tarjetas DirectX11 y DirectX10 que admiten DirectCompute pueden usar el efecto.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible | Windows 8 y actualización de plataforma para Windows 7 aplicaciones de \[ escritorio \| Windows store\] |
| Servidor mínimo compatible | Windows 8 y actualización de plataforma para Windows 7 aplicaciones de \[ escritorio \| Windows store\] |
| Header                   | d2d1effects.h                                                                      |
| Biblioteca                  | d2d1.lib, dxguid.lib                                                               |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

