---
description: Interfaces de dispositivos externos para cámaras de vídeo DV
ms.assetid: 001321c5-70c7-4baa-ba5a-1e424ca0d647
title: Interfaces de dispositivos externos para cámaras de vídeo DV
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb80a89356a18d25f1fb3536cdc8f6e95be4e1947433d1c0437f1d80d47c8008
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119651525"
---
# <a name="external-device-interfaces-for-dv-camcorders"></a>Interfaces de dispositivos externos para cámaras de vídeo DV

El [filtro captura de vídeo de WDM](wdm-video-capture-filter.md) expone tres interfaces para controlar una cámara de vídeo.



| Etiqueta | Valor |
|------------------------------------------------|-------------------------------------------------|
| [**IAMExtDevice**](/windows/desktop/api/Strmif/nn-strmif-iamextdevice)           | Interfaz base para el control de dispositivo externo. |
| [**IAMExtTransport**](/windows/desktop/api/Strmif/nn-strmif-iamexttransport)     | Controla las funciones de VCR.                     |
| [**IAMTimecodeReader**](/windows/desktop/api/Strmif/nn-strmif-iamtimecodereader) | Lee el código de tiempo del dispositivo.                 |



 

> [!Note]  
> Para usar estas interfaces con el controlador de cámara de vídeo MSDV, incluya el archivo de encabezado XPrtDefs.h en el proyecto.

 

Después de seleccionar un dispositivo de captura y crear una instancia del filtro de captura, consulte el filtro para estas interfaces. En el ejemplo siguiente se declara una estructura personalizada que contiene los punteros de interfaz, junto con valores booleanos que especifican la disponibilidad de cada interfaz:


```C++
struct _MyDevCap
{
    IAMExtDevice       *pDevice;
    IAMExtTransport    *pTransport;
    IAMTimecodeReader  *pTimecode;
    BOOL                bHasDevice;
    BOOL                bHasTransport;
    BOOL                bHasTimecode;
} MyDevCap;

HRESULT hr;
IBaseFilter *pDVCam;  // Pointer to the capture filter.

// Create an instance of the capture filter (not shown).

hr = pDVCam->QueryInterface(IID_IAMExtDevice, (void **)&MyDevCap.pDevice);
MyDevCap.bHasDevice = (SUCCEEDED(hr));

hr = pDVCam->QueryInterface(IID_IAMExtTransport, (void **)&MyDevCap.pTransport);
MyDevCap.bHasTransport = (SUCCEEDED(hr));

hr = pDVCam->QueryInterface(IID_IAMTimecodeReader, (void **)&MyDevCap.pTimecode);
MyDevCap.bHasTimecode = (SUCCEEDED(hr));
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Control de una videocamba de DV](controlling-a-dv-camcorder.md)
</dt> </dl>

 

 



