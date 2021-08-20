---
description: Mensaje privado que establece el estilo de ventana en WS \_ EX \_ TOPMOST.
ms.assetid: 4934400e-4ca5-4ace-b9b9-3889f4cf610e
title: CBaseWindow::m_ShowStageTop miembro (Winutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_ShowStageTop
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: dbd8943b297d6e33f3b86a62c7e67dd2039a6b99d316061be30a4c3016711c41
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119016523"
---
# <a name="cbasewindowm_showstagetop-member"></a>Miembro CBaseWindow::m \_ ShowStageTop

Mensaje privado que establece el estilo de ventana en WS \_ EX \_ TOPMOST.

## <a name="syntax"></a>Sintaxis


```C++
UINT m_ShowStageTop;
```



## <a name="remarks"></a>Comentarios

Los representadores de vídeo deben enviar este mensaje a la ventana si cambian al modo de pantalla completa.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Winutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseWindow (clase)**](cbasewindow.md)
</dt> </dl>

 

 




