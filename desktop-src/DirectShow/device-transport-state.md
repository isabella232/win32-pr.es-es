---
description: Estado de transporte de dispositivos
ms.assetid: 15edded0-207c-41e8-81fe-deb6335045eb
title: Estado de transporte de dispositivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99ea7c3d6cba8363826c0fdab3cf411f0d68d6e284832a75c02cac3b1eefa770
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118952954"
---
# <a name="device-transport-state"></a>Estado de transporte de dispositivos

Para recuperar el estado actual del dispositivo, como reproducir, pausar o detener, llame al método [**IAMExtTransport::get \_ Mode.**](/windows/desktop/api/Strmif/nf-strmif-iamexttransport-get_mode) El método recupera una constante que indica el estado del dispositivo:



| Value                    | Estado del dispositivo |
|--------------------------|--------------|
| REPRODUCCIÓN EN MODO ED \_ \_           | Reproducir         |
| ED \_ MODE \_ STOP           | Stop         |
| INMOVILIZACIÓN \_ DEL MODO \_ ED         | Pausar        |
| ED \_ MODE \_ FF             | Avance rápido |
| ED \_ MODE \_ REW            | Rebobinar       |
| REGISTRO DE \_ MODO \_ ED         | Registro       |
| INMOVILIZACIÓN DE \_ REGISTROS \_ EN MODO \_ ED | Pausa de registros |



 

El código siguiente comprueba el estado del dispositivo:


```C++
LONG State;
hr = MyDevCap.pTransport->get_Mode(&State);
if (SUCCEEDED(hr))
{
    switch (State)
    {
        case ED_MODE_PLAY:
        // ... 
    }
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Control de una videocamba de DV](controlling-a-dv-camcorder.md)
</dt> </dl>

 

 



