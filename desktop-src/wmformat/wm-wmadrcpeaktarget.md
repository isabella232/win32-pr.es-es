---
title: WM/WMADRCPeakTarget
description: El atributo WM/WMADRCPeakTarget contiene el nivel de volumen máximo solicitado por el usuario. Este valor lo usa Reproductor de Windows Media para el control de intervalo dinámico.
ms.assetid: 94ef5db1-34f4-4cf8-ac56-c85cca10536b
keywords:
- Formato multimedia de Windows WM/WMADRCPeakTarget
topic_type:
- apiref
api_name:
- WM/WMADRCPeakTarget
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9c87c8d62316bfa3e732d0cdc00e0fcb5295c30e675fd9c21fcd5ac766f239f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119590685"
---
# <a name="wmwmadrcpeaktarget"></a>WM/WMADRCPeakTarget

El **atributo WM/WMADRCPeakTarget** contiene el nivel de volumen máximo solicitado por el usuario. Este valor lo usa Reproductor de Windows Media para el control de intervalo dinámico.

## <a name="global-constant"></a>Constante global

g \_ wszWMWMADRCPeakTarget

## <a name="data-type"></a>Tipo de datos

**DWORD \_ DE TIPO \_ WMT**

## <a name="remarks"></a>Comentarios

Hay cuatro atributos usados por Reproductor de Windows Media para el control de intervalo dinámico: **WM/WMADRCAverageReference**, **WM/WMADRCPeakReference**, **WM/WMADRCAverageTarget** y **WM/WMADRCPeakTarget**. El escritor establece todos estos valores en función de la información del códec al escribir secuencias con el códec Windows Media Audio 9 o el códec Windows Media Audio 9 Professional. Los valores medios se establecen en el nivel medio de volumen de la secuencia y los valores máximos se establecen en el nivel de volumen máximo de la secuencia. Los valores de referencia son de solo lectura. Los valores de destino se establecen Reproductor de Windows Media cuando el archivo se reproduce para registrar las preferencias de control de intervalo dinámico del usuario.

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Lista de atributos**](attribute-list.md)
</dt> <dt>

[**WM/WMADRCAverageReference**](wm-wmadrcaveragereference.md)
</dt> <dt>

[**WM/WMADRCAverageTarget**](wm-wmadrcaveragetarget.md)
</dt> <dt>

[**WM/WMADRCPeakReference**](wm-wmadrcpeakreference.md)
</dt> </dl>

 

 




