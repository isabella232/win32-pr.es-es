---
description: La clase CVideoTransformFilter está diseñada principalmente como una clase base para filtros de descompresión AVI.
ms.assetid: 8eb87f9f-24b3-4dbe-a390-54db993d2724
title: CVideoTransformFilter (clase)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127266436"
---
# <a name="cvideotransformfilter-class"></a>CVideoTransformFilter (clase)

![Jerarquía de clases cvideotransformfilter](images/vtsip01.png)

La `CVideoTransformFilter` clase está diseñada principalmente como una clase base para filtros de descompresión AVI. Esta clase agrega compatibilidad con el control de calidad a la [**clase CTransformFilter.**](ctransformfilter.md) El método **Receive** del filtro puede decidir quitar fotogramas, en función de los mensajes de calidad del representador y las medidas de rendimiento que el filtro recopila mientras se transmite.

Si el filtro quita un fotograma, continúa quitando fotogramas hasta que alcanza el siguiente fotograma clave. En el caso de las secuencias MPEG, el filtro no distingue entre fotogramas B y fotogramas P.



| Variables miembro protegidas                                                      | Descripción                                                                                    |
|---------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [**m \_ bQualityChanged**](cvideotransformfilter-m-bqualitychanged.md)           | Indica si el filtro ha eliminado marcos.                                               |
| [**m \_ bSkipping**](cvideotransformfilter-m-bskipping.md)                       | Indica si el filtro está quitando fotogramas actualmente.                                     |
| [**m \_ itrAvgDecode**](cvideotransformfilter-m-itravgdecode.md)                 | Duración media del tiempo que ha llevado descodificar un fotograma.                                         |
| [**m \_ itrLate**](cvideotransformfilter-m-itrlate.md)                           | Indica la demora con la que llegan las muestras al representador.                                   |
| [**m \_ nFramesSinceKeyFrame**](cvideotransformfilter-m-nframessincekeyframe.md) | Número de fotogramas que ha recibido el filtro desde el último fotograma clave.                    |
| [**m \_ nKeyFramePeriod**](cvideotransformfilter-m-nkeyframeperiod.md)           | Intervalo observado más grande entre fotogramas clave.                                              |
| [**m \_ nWaitForKey**](cvideotransformfilter-m-nwaitforkey.md)                   | Número máximo actual de fotogramas delta que se quitarán.                                            |
| [**m \_ tDecodeStart**](cvideotransformfilter-m-tdecodestart.md)                 | Tiempo que tardó en descodificar el ejemplo más reciente.                                  |
| Métodos protegidos                                                               | Descripción                                                                                    |
| [**AbortPlayback**](cvideotransformfilter-abortplayback.md)                    | Se usa para señalar un error de streaming.                                                              |
| [**AlterQuality**](cvideotransformfilter-alterquality.md)                      | Notifica al filtro que se solicita un cambio de calidad.                                        |
| [**Recepción**](cvideotransformfilter-receive.md)                                | Recibe un ejemplo multimedia, lo procesa y entrega un ejemplo de salida al filtro de nivel inferior. |
| [**ShouldSkipFrame**](cvideotransformfilter-shouldskipframe.md)                | Determina si el filtro debe quitar un ejemplo especificado.                                  |
| [**StartStreaming**](cvideotransformfilter-startstreaming.md)                  | Se llama cuando el filtro cambia al estado en pausa.                                           |
| Métodos públicos                                                                  | Descripción                                                                                    |
| [**CVideoTransformFilter**](cvideotransformfilter-cvideotransformfilter.md)    | Método constructor.                                                                            |
| [**EndFlush**](cvideotransformfilter-endflush.md)                              | Finaliza una operación de vaciado.                                                                        |



 

 

 



