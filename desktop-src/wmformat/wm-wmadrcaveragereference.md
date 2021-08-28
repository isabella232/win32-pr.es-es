---
title: WM/WMADRCAverageReference
description: El atributo WM/WMADRCAverageReference contiene el nivel medio de volumen del archivo como codificado.
ms.assetid: 994614e3-06e2-48f0-bdac-6de5ab0c0eff
keywords:
- Formato multimedia de windows WM/WMADRCAverageReference
topic_type:
- apiref
api_name:
- WM/WMADRCAverageReference
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9948d71739aaee4f5f24f54701f8e335f8b7b79486c8820f7a5fdf48c068e37
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119026953"
---
# <a name="wmwmadrcaveragereference"></a>WM/WMADRCAverageReference

El **atributo WM/WMADRCAverageReference** contiene el nivel medio de volumen del archivo como codificado.

## <a name="global-constant"></a>Constante global

g \_ wszWMWMADRCAverageReference

## <a name="data-type"></a>Tipo de datos

**DWORD \_ DE TIPO \_ WMT**

## <a name="remarks"></a>Comentarios

Hay cuatro atributos usados por Reproductor de Windows Media para el control de intervalo dinámico: **WM/WMADRCAverageReference,** **WM/WMADRCPeakReference,** **WM/WMADRCAverageTarget** y **WM/WMADRCPeakTarget**. Todos estos valores los establece el escritor en función de la información del códec al escribir secuencias con el códec Windows Media Audio 9 o el códec Windows Media Audio 9 Professional. Los valores medios se establecen en el nivel medio de volumen de la secuencia y los valores máximos se establecen en el nivel de volumen máximo de la secuencia. Los valores de referencia son de solo lectura. Los valores de destino se establecen Reproductor de Windows Media cuando se reproduce el archivo para registrar las preferencias de control de intervalo dinámico del usuario.

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Lista de atributos**](attribute-list.md)
</dt> <dt>

[**WM/WMADRCAverageTarget**](wm-wmadrcaveragetarget.md)
</dt> <dt>

[**WM/WMADRCPeakReference**](wm-wmadrcpeakreference.md)
</dt> <dt>

[**WM/WMADRCPeakTarget**](wm-wmadrcpeaktarget.md)
</dt> </dl>

 

 




