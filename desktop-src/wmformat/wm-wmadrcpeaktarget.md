---
title: WM/WMADRCPeakTarget
description: El atributo WM/WMADRCPeakTarget contiene el nivel de volumen máximo solicitado por el usuario. Windows Media Player usa este valor para el control de intervalo dinámico.
ms.assetid: 94ef5db1-34f4-4cf8-ac56-c85cca10536b
keywords:
- Formato de Windows Media WM/WMADRCPeakTarget
topic_type:
- apiref
api_name:
- WM/WMADRCPeakTarget
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55eac4ea68cd61e2cfa0b5c185dc1a4ad17e5ce8
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "103784145"
---
# <a name="wmwmadrcpeaktarget"></a>WM/WMADRCPeakTarget

El atributo **WM/WMADRCPeakTarget** contiene el nivel de volumen máximo solicitado por el usuario. Windows Media Player usa este valor para el control de intervalo dinámico.

## <a name="global-constant"></a>Constante global

g \_ wszWMWMADRCPeakTarget

## <a name="data-type"></a>Tipo de datos

**tipo de WMT \_ \_ DWORD**

## <a name="remarks"></a>Observaciones

Windows Media Player usa cuatro atributos para el control de intervalo dinámico: **WM/WMADRCAverageReference**, **WM/WMADRCPeakReference**, **WM/WMADRCAverageTarget** y **WM/WMADRCPeakTarget**. El escritor establece todos estos valores en función de la información del códec al escribir secuencias con el códec Windows Media Audio 9 o Windows Media Audio 9 Professional. Los valores medios se establecen en el nivel de volumen medio de la secuencia y los valores máximos se establecen en el nivel de volumen máximo en la secuencia. Los valores de referencia son de solo lectura. Los valores de destino se establecen mediante Windows Media Player cuando se reproduce el archivo para registrar las preferencias de control de intervalo dinámico del usuario.

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

 

 




