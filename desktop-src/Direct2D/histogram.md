---
title: Efecto de histograma
description: Use el efecto histograma para generar un histograma para el mapa de bits de entrada en función del número especificado de ubicaciones.
ms.assetid: 458E2334-F383-41DE-9479-601AC3007BF3
keywords:
- efecto de histograma
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b654ffb2b830914b00a59490ceb429b5de9c51cb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422230"
---
# <a name="histogram-effect"></a>Efecto de histograma

Use el efecto histograma para generar un histograma para el mapa de bits de entrada en función del número especificado de ubicaciones.

El CLSID para este efecto es CLSID \_ D2D1Histogram.

-   [Ejemplo](#example)
-   [Propiedades del efecto](#effect-properties)
-   [Selectores de canal](#channel-selectors)
-   [Salida de datos](#data-output)
-   [Comentarios:](#remarks)
-   [Requisitos](#requirements)
-   [Temas relacionados](#related-topics)

## <a name="example"></a>Ejemplo



| Antes                                                     |
|------------------------------------------------------------|
| ![imagen anterior al efecto.](images/default-before.jpg) |
| Gráfico de los datos de salida del histograma                         |
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



## <a name="effect-properties"></a>Propiedades del efecto

Esta es la ecuación para generar la salida.

![la ecuación para generar el resultado del efecto del histograma.](images/histogram-formula.png)

*i* se evalúa desde 0 hasta el número de ubicaciones. El efecto genera un histograma para los valores de píxel entre 0 y 1. Los valores que se encuentran fuera de este intervalo se fijan al intervalo. El intervalo de un depósito determinado depende del número de depósitos. Este efecto funciona en píxeles de mapa de bits directos. Los canales de color del mapa de bits de entrada se dividen por el canal alfa para calcular este efecto.



| Enumeración de índice y nombre para mostrar                                             | Tipo y valor predeterminado                                                   | Descripción                                                                                                                                                                                   |
|--------------------------------------------------------------------------------|--------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| NumBins<br/> D2D1 \_ de \_ prop número de propiedades de histograma \_ \_<br/>                 | UINT32<br/> 256<br/>                                         | Especifica el número de ubicaciones utilizadas para el histograma. El intervalo de valores de intensidad que se encuentran en un depósito determinado depende del número de depósitos especificados.                              |
| ChannelSelect<br/> \_Selección de \_ canal de prop de histograma D2D1 \_ \_<br/>     | \_Selector de canal de D2D1 \_<br/> Selector de canal de D2D1 \_ \_ \_ R<br/> | Especifica el canal usado para generar el histograma. Este efecto tiene una única salida de datos correspondiente al canal especificado. Consulte [selectores de canal](#channel-selectors) para obtener más información. |
| HistogramOutput<br/> \_Salida del \_ histograma de prop de histograma D2D1 \_ \_<br/> | FLOT\[\]<br/> Solo propiedad de salida.<br/>                    | Matriz de salida.                                                                                                                                                                             |



 

## <a name="channel-selectors"></a>Selectores de canal



| Enumeración                | Descripción                                                           |
|----------------------------|-----------------------------------------------------------------------|
| Selector de canal de D2D1 \_ \_ \_ R | El efecto genera la salida del histograma en función del canal rojo.   |
| Selector de canal de D2D1 \_ \_ \_ G | El efecto genera la salida del histograma en función del canal verde. |
| Selector de canal de D2D1 \_ \_ \_ B | El efecto genera la salida del histograma en función del canal azul.  |
| \_ \_ Selector de canal \_ de D2D1 A | El efecto genera la salida del histograma en función del canal alfa. |



 

## <a name="data-output"></a>Salida de datos

Este efecto da como resultado un \[ \] valor Float, con el número de elementos correspondientes al número de ubicaciones especificadas. Cada elemento de FLOAT \[ \] es float. El valor del elemento corresponde al número de elementos de esa ubicación.

## <a name="remarks"></a>Observaciones

> [!Note]  
> El método [**CreateEffect**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createeffect) genera un error si el dispositivo no admite DirectCompute y devuelve HRESULT = D2DERR \_ insuficientes \_ funcionalidades del dispositivo \_ . Todas las tarjetas DirectX11 y DirectX10 que admiten DirectCompute pueden usar el efecto.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible | Windows 8 y actualización de la plataforma para aplicaciones de escritorio de Windows 7 aplicaciones de la \[ \| tienda Windows\] |
| Servidor mínimo compatible | Windows 8 y actualización de la plataforma para aplicaciones de escritorio de Windows 7 aplicaciones de la \[ \| tienda Windows\] |
| Encabezado                   | d2d1effects. h                                                                      |
| Biblioteca                  | d2d1. lib, dxguid. lib                                                               |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

