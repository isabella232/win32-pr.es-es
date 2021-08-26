---
description: En este tema se describe cómo una aplicación puede cambiar mediante programación la configuración de la imagen y la cámara en un dispositivo de captura de vídeo.
ms.assetid: f789db78-292e-4092-a5dc-1906845fb1dd
title: Configuración de la calidad del vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5987352eb329410efd3fc74d6bf12539e968da8e24d2f0a65af9c9ac7b5cb85
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119871775"
---
# <a name="configure-the-video-quality"></a>Configuración de la calidad del vídeo

En este tema se describe cómo una aplicación puede cambiar mediante programación la configuración de la imagen y la cámara en un dispositivo de captura de vídeo.

-   [ProcAmp Configuración](#procamp-settings)
-   [Configuración de la cámara](#camera-settings)
-   [Temas relacionados](#related-topics)

## <a name="procamp-settings"></a>ProcAmp Configuración

Windows Las cámaras de vídeo del modelo de controlador (WDM) pueden admitir propiedades que controlan la calidad de la imagen:

-   Compensación de retroiluminación
-   Luminosidad
-   Compare
-   Ganar
-   Gamma
-   Matiz
-   Saturación
-   Nitidez
-   Balance de blancos

Estas propiedades se controlan a través de [**la interfaz IAMVideoProcAmp.**](/windows/desktop/api/Strmif/nn-strmif-iamvideoprocamp) Use esta interfaz como se muestra a continuación:

1.  Llame [**a QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) en el filtro de captura para [**la interfaz IAMVideoProcAmp.**](/windows/desktop/api/Strmif/nn-strmif-iamvideoprocamp)
2.  Para cada propiedad que quiera establecer, llame al [**método IAMVideoProcAmp::GetRange.**](/windows/desktop/api/Strmif/nf-strmif-iamvideoprocamp-getrange) Las propiedades se especifican mediante la [**enumeración VideoProcAmpProperty.**](/windows/win32/api/strmif/ne-strmif-videoprocampproperty) Si se produce un error en el método **GetRange,** significa que la cámara no admite esa propiedad determinada.
3.  Si [**GetRange se**](/windows/desktop/api/Strmif/nf-strmif-iamvideoprocamp-getrange) realiza correctamente, devuelve el intervalo de valores admitidos para la propiedad , el valor predeterminado y el incremento mínimo.
4.  Para obtener el valor actual de una propiedad, llame a [**IAMVideoProcAmp::Get**](/windows/desktop/api/Strmif/nf-strmif-iamvideoprocamp-get).
5.  Para establecer una propiedad, llame al [**método IAMVideoProcAmp::Set.**](/windows/desktop/api/Strmif/nf-strmif-iamvideoprocamp-set) Para restaurar una propiedad a su valor predeterminado, llame a [**GetRange**](/windows/desktop/api/Strmif/nf-strmif-iamvideoprocamp-getrange) para buscar el valor predeterminado y pasar ese valor al **método Set.**

No es necesario detener el gráfico de filtros al establecer las propiedades.

El código siguiente configura un control trackbar para que se pueda usar para establecer el brillo. El intervalo de la barra de seguimiento corresponde al intervalo de brillo que admite el dispositivo y la posición de la barra de seguimiento corresponde a la configuración de brillo inicial del dispositivo.


```C++
HWND hTrackbar; // Handle to the trackbar control. 
// Initialize hTrackbar (not shown).

// Query the capture filter for the IAMVideoProcAmp interface.
IAMVideoProcAmp *pProcAmp = 0;
hr = pCap->QueryInterface(IID_IAMVideoProcAmp, (void**)&pProcAmp);
if (FAILED(hr))
{
    // The device does not support IAMVideoProcAmp, so disable the control.
    EnableWindow(hTrackbar, FALSE);
}
else
{
    long Min, Max, Step, Default, Flags, Val;

    // Get the range and default value. 
    hr = m_pProcAmp->GetRange(VideoProcAmp_Brightness, &Min, &Max, &Step,
        &Default, &Flags);
    if (SUCCEEDED(hr))
    {
        // Get the current value.
        hr = m_pProcAmp->Get(VideoProcAmp_Brightness, &Val, &Flags);
    }
    if (SUCCEEDED(hr))
    {
        // Set the trackbar range and position.
        SendMessage(hTrackbar, TBM_SETRANGE, TRUE, MAKELONG(Min, Max));
        SendMessage(hTrackbar, TBM_SETPOS, TRUE, Val);
        EnableWindow(hTrackbar, TRUE);
    }
    else
    {
        // This property is not supported, so disable the control.
        EnableWindow(hTrackbar, FALSE);
    }
}
```



## <a name="camera-settings"></a>Configuración de la cámara

La [**interfaz IAMCameraControl**](/windows/desktop/api/Strmif/nn-strmif-iamcameracontrol) es similar a [**IAMVideoProcAmp,**](/windows/desktop/api/Strmif/nn-strmif-iamvideoprocamp)pero controla varios ajustes en la propia cámara:

-   Exposure
-   Foco
-   Iris
-   Movimiento panorámico
-   Rodillo
-   Inclinación
-   Zoom

Para usar esta interfaz, siga los mismos pasos que se usan [**para IAMVideoProcAmp**](/windows/desktop/api/Strmif/nn-strmif-iamvideoprocamp):

1.  Consulte el filtro de captura para [**IAMCameraControl.**](/windows/desktop/api/Strmif/nn-strmif-iamcameracontrol)
2.  Llame [**a IAMCameraControl::GetRange**](/windows/desktop/api/Strmif/nf-strmif-iamcameracontrol-getrange) para buscar qué configuración se admite y el intervalo posible para cada configuración.
3.  Llame [**a IAMCameraControl::Get**](/windows/desktop/api/Strmif/nf-strmif-iamcameracontrol-get) para obtener el valor actual de una configuración.
4.  Llame [**a IAMCameraControl::Set**](/windows/desktop/api/Strmif/nf-strmif-iamcameracontrol-set) para establecer el valor.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Configuración de un dispositivo de captura de vídeo](configuring-a-video-capture-device.md)
</dt> </dl>

 

 
