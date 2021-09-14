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
ms.openlocfilehash: 8ed0069c5c65f2bb1a113c899e2d90de0cabcd10
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126973924"
---
# <a name="cbasewindowm_showstagetop-member"></a>Miembro CBaseWindow::m \_ ShowStageTop

Mensaje privado que establece el estilo de ventana en WS \_ EX \_ TOPMOST.

## <a name="syntax"></a>Sintaxis


```C++
UINT m_ShowStageTop;
```



## <a name="remarks"></a>Observaciones

Los representadores de vídeo deben enviar este mensaje a la ventana si cambian al modo de pantalla completa.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Winutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CBaseWindow (clase)**](cbasewindow.md)
</dt> </dl>

 

 




