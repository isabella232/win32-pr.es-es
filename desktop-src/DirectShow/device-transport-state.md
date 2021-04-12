---
description: Estado de transporte del dispositivo
ms.assetid: 15edded0-207c-41e8-81fe-deb6335045eb
title: Estado de transporte del dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05f52ea846c79be6cb2d011b635da358f7ecd0a2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104423163"
---
# <a name="device-transport-state"></a>Estado de transporte del dispositivo

Para recuperar el estado actual del dispositivo, como reproducir, pausar o detener, llame al método [**IAMExtTransport:: get \_ mode**](/windows/desktop/api/Strmif/nf-strmif-iamexttransport-get_mode) . El método recupera una constante que indica el estado del dispositivo:



| Value                    | Estado del dispositivo |
|--------------------------|--------------|
| \_reproducción en modo Ed \_           | Reproducir         |
| \_detención del modo de Ed \_           | Stop         |
| modo de ED \_ \_ congelar         | Pausar        |
| \_modo Ed \_ FF             | Avance rápido |
| \_modo Ed \_ Rebo            | Rebobinar       |
| \_registro en modo Ed \_         | Registro       |
| inmovilización de registros en \_ modo Ed \_ \_ | Grabar-pausar |



 

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

[Control de una videocámara DV](controlling-a-dv-camcorder.md)
</dt> </dl>

 

 



