---
description: Marca que especifica si la ventana envía o envía su mensaje de destrucción.
ms.assetid: 553a372e-1abe-4661-bfa5-b8a63be63c72
title: 'Miembro CBaseWindow:: m_bDoPostToDestroy (Winutil. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bDoPostToDestroy
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 804d0910760ddac5ea4d74979293f43e5b189225
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660972"
---
# <a name="cbasewindowm_bdoposttodestroy-member"></a>Miembro bDoPostToDestroy CBaseWindow:: m \_

Marca que especifica si la ventana envía o envía su mensaje de destrucción. Si **es true**, el método [**CBaseWindow::D onewithwindow**](cbasewindow-donewithwindow.md) usa la función **PostMessage** para enviarse a sí mismo un mensaje de destrucción privado. Si **es false**, **DoneWithWindow** usa la función **SendMessage** para enviar el mensaje. De forma predeterminada, el valor es **false**.

## <a name="syntax"></a>Sintaxis


```C++
BOOL m_bDoPostToDestroy;
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Winutil. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseWindow**](cbasewindow.md)
</dt> </dl>

 

 




