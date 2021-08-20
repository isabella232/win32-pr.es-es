---
title: WM/WMADRCPeakReference
description: El atributo WM/WMADRCPeakReference contiene el nivel de volumen máximo del archivo como codificado. Este valor lo usa Reproductor de Windows Media control de intervalo dinámico. Este valor lo establece el códec y es de solo lectura.
ms.assetid: c732ee88-437b-4970-8f17-61aed2d91022
keywords:
- Formato multimedia windows WM/WMADRCPeakReference
topic_type:
- apiref
api_name:
- WM/WMADRCPeakReference
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2e5abf41b52b615030c07b532fc3d75e40bd898a409e0f5ecd2b15541c8c0df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118027537"
---
# <a name="wmwmadrcpeakreference"></a>WM/WMADRCPeakReference

El **atributo WM/WMADRCPeakReference** contiene el nivel de volumen máximo del archivo como codificado. Este valor lo usa Reproductor de Windows Media control de intervalo dinámico. Este valor lo establece el códec y es de solo lectura.

## <a name="global-constant"></a>Constante global

g \_ wszWMWMADRCPeakReference

## <a name="data-type"></a>Tipo de datos

**DWORD \_ DE TIPO \_ WMT**

## <a name="remarks"></a>Comentarios

Hay cuatro atributos usados por Reproductor de Windows Media para el control de intervalo dinámico: **WM/WMADRCAverageReference**, **WM/WMADRCPeakReference,** **WM/WMADRCAverageTarget** y **WM/WMADRCPeakTarget**. El escritor establece todos estos valores en función de la información del códec al escribir secuencias con el códec Windows Media Audio 9 o el códec Windows Media Audio 9 Professional. Los valores medios se establecen en el nivel medio de volumen de la secuencia y los valores máximos se establecen en el nivel de volumen máximo de la secuencia. Los valores de referencia son de solo lectura. Los valores de destino se establecen Reproductor de Windows Media cuando el archivo se reproduce para registrar las preferencias de control de intervalo dinámico del usuario.

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Lista de atributos**](attribute-list.md)
</dt> <dt>

[**WM/WMADRCAverageReference**](wm-wmadrcaveragereference.md)
</dt> <dt>

[**WM/WMADRCAverageTarget**](wm-wmadrcaveragetarget.md)
</dt> <dt>

[**WM/WMADRCPeakTarget**](wm-wmadrcpeaktarget.md)
</dt> </dl>

 

 




