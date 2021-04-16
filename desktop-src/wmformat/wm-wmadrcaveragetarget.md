---
title: WM/WMADRCAverageTarget
description: El atributo WM/WMADRCAverageTarget contiene el nivel de volumen medio solicitado por el usuario. Windows Media Player usa este valor para el control de intervalo dinámico.
ms.assetid: 8173b5ab-27e4-4af9-aea8-6c1310f065f5
keywords:
- Formato de Windows Media WM/WMADRCAverageTarget
topic_type:
- apiref
api_name:
- WM/WMADRCAverageTarget
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 387eed9112e8e0d79943b99bf326b07f42f425d1
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "105695514"
---
# <a name="wmwmadrcaveragetarget"></a>WM/WMADRCAverageTarget

El atributo **WM/WMADRCAverageTarget** contiene el nivel de volumen medio solicitado por el usuario. Windows Media Player usa este valor para el control de intervalo dinámico.

## <a name="global-constant"></a>Constante global

g \_ wszWMWMADRCAverageTarget

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

[**WM/WMADRCPeakReference**](wm-wmadrcpeakreference.md)
</dt> <dt>

[**WM/WMADRCPeakTarget**](wm-wmadrcpeaktarget.md)
</dt> </dl>

 

 




