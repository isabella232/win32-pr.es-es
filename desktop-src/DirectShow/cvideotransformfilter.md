---
description: La clase CVideoTransformFilter está diseñada principalmente como una clase base para los filtros de descompresor de AVI.
ms.assetid: 8eb87f9f-24b3-4dbe-a390-54db993d2724
title: Clase CVideoTransformFilter
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CVideoTransformFilter
api_type:
- COM
api_location: ''
ms.openlocfilehash: 360f46eb7242de01d5e734c5efa17399f23adf7d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103906865"
---
# <a name="cvideotransformfilter-class"></a>Clase CVideoTransformFilter

![jerarquía de clases cvideotransformfilter](images/vtsip01.png)

La `CVideoTransformFilter` clase está diseñada principalmente como una clase base para los filtros de descompresor de AVI. Esta clase agrega compatibilidad para el control de calidad a la clase [**CTransformFilter**](ctransformfilter.md) . El método **Receive** del filtro puede decidir quitar fotogramas, en función de los mensajes de calidad del representador y las medidas de rendimiento que el filtro recopila mientras se transmite por secuencias.

Si el filtro quita un fotograma, sigue colocando fotogramas hasta que llega al siguiente fotograma clave. En el caso de las secuencias MPEG, el filtro no distingue entre fotogramas B y fotogramas P.



| Variables de miembro protegidas                                                      | Descripción                                                                                    |
|---------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [**m \_ bQualityChanged**](cvideotransformfilter-m-bqualitychanged.md)           | Indica si el filtro ha quitado fotogramas.                                               |
| [**m \_ bSkipping**](cvideotransformfilter-m-bskipping.md)                       | Indica si el filtro está quitando actualmente fotogramas.                                     |
| [**m \_ itrAvgDecode**](cvideotransformfilter-m-itravgdecode.md)                 | Promedio de tiempo que ha tardado en descodificar un marco.                                         |
| [**m \_ itrLate**](cvideotransformfilter-m-itrlate.md)                           | Indica el nivel de finalización de las muestras en el representador.                                   |
| [**m \_ nFramesSinceKeyFrame**](cvideotransformfilter-m-nframessincekeyframe.md) | Número de fotogramas que ha recibido el filtro desde el último fotograma clave.                    |
| [**m \_ nKeyFramePeriod**](cvideotransformfilter-m-nkeyframeperiod.md)           | El intervalo observado más grande entre fotogramas clave.                                              |
| [**m \_ nWaitForKey**](cvideotransformfilter-m-nwaitforkey.md)                   | Número máximo actual de fotogramas Delta que se van a quitar.                                            |
| [**m \_ tDecodeStart**](cvideotransformfilter-m-tdecodestart.md)                 | Período de tiempo que se tardó en descodificar el ejemplo más reciente.                                  |
| Métodos protegidos                                                               | Descripción                                                                                    |
| [**AbortPlayback**](cvideotransformfilter-abortplayback.md)                    | Se usa para indicar un error de streaming.                                                              |
| [**AlterQuality**](cvideotransformfilter-alterquality.md)                      | Notifica al filtro que se ha solicitado un cambio de calidad.                                        |
| [**Aparecen**](cvideotransformfilter-receive.md)                                | Recibe un ejemplo multimedia, lo procesa y entrega un ejemplo de salida al filtro de nivel inferior. |
| [**ShouldSkipFrame**](cvideotransformfilter-shouldskipframe.md)                | Determina si el filtro debe quitar un ejemplo especificado.                                  |
| [**StartStreaming**](cvideotransformfilter-startstreaming.md)                  | Se le llama cuando el filtro cambia al estado de pausa.                                           |
| Métodos públicos                                                                  | Descripción                                                                                    |
| [**CVideoTransformFilter**](cvideotransformfilter-cvideotransformfilter.md)    | Método de constructor.                                                                            |
| [**EndFlush**](cvideotransformfilter-endflush.md)                              | Finaliza una operación de vaciado.                                                                        |



 

 

 



