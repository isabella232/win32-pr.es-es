---
title: WM/WMADRCAverageTarget
description: El atributo WM/WMADRCAverageTarget contiene el nivel medio de volumen solicitado por el usuario. Este valor lo usa Reproductor de Windows Media para el control de intervalo dinámico.
ms.assetid: 8173b5ab-27e4-4af9-aea8-6c1310f065f5
keywords:
- WM/WMADRCAverageTarget windows Media Format
topic_type:
- apiref
api_name:
- WM/WMADRCAverageTarget
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2bd08dd09b6db671a0af1d816162923624cb781148f557ce4bee21fe2dc9a933
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119083919"
---
# <a name="wmwmadrcaveragetarget"></a>WM/WMADRCAverageTarget

El **atributo WM/WMADRCAverageTarget** contiene el nivel medio de volumen solicitado por el usuario. Este valor lo usa Reproductor de Windows Media para el control de intervalo dinámico.

## <a name="global-constant"></a>Constante global

g \_ wszWMWMADRCAverageTarget

## <a name="data-type"></a>Tipo de datos

**DWORD \_ DE TIPO \_ WMT**

## <a name="remarks"></a>Comentarios

Hay cuatro atributos usados por Reproductor de Windows Media para el control de intervalo dinámico: **WM/WMADRCAverageReference**, **WM/WMADRCPeakReference,** **WM/WMADRCAverageTarget** y **WM/WMADRCPeakTarget**. El escritor establece todos estos valores en función de la información del códec al escribir secuencias con el códec Windows Media Audio 9 o el códec Windows Media Audio 9 Professional. Los valores medios se establecen en el nivel medio de volumen de la secuencia y los valores máximos se establecen en el nivel de volumen máximo de la secuencia. Los valores de referencia son de solo lectura. Los valores de destino se establecen Reproductor de Windows Media cuando el archivo se reproduce para registrar las preferencias de control de intervalo dinámico del usuario.

## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Lista de atributos**](attribute-list.md)
</dt> <dt>

[**WM/WMADRCAverageReference**](wm-wmadrcaveragereference.md)
</dt> <dt>

[**WM/WMADRCPeakReference**](wm-wmadrcpeakreference.md)
</dt> <dt>

[**WM/WMADRCPeakTarget**](wm-wmadrcpeaktarget.md)
</dt> </dl>

 

 




