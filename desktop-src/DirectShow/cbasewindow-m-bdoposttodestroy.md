---
description: Marca que especifica si la ventana publica o envía su mensaje de destrucción.
ms.assetid: 553a372e-1abe-4661-bfa5-b8a63be63c72
title: CBaseWindow::m_bDoPostToDestroy miembro (Winutil.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126973938"
---
# <a name="cbasewindowm_bdoposttodestroy-member"></a>Miembro CBaseWindow::m \_ bDoPostToDestroy

Marca que especifica si la ventana publica o envía su mensaje de destrucción. Si **es TRUE,** [**el método CBaseWindow::D oneWithWindow**](cbasewindow-donewithwindow.md) usa la **función PostMessage** para enviarse a sí mismo un mensaje de destrucción privado. Si **es FALSE,** **DoneWithWindow** usa la **función SendMessage** para enviar el mensaje. De forma predeterminada, el valor es **FALSE.**

## <a name="syntax"></a>Sintaxis


```C++
BOOL m_bDoPostToDestroy;
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Winutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CBaseWindow (clase)**](cbasewindow.md)
</dt> </dl>

 

 




