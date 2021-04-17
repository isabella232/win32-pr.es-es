---
description: El método DoShowWindow establece el estado de presentación de la ventana.
ms.assetid: 4180de9d-ef40-40e3-aa37-be54283b1f97
title: Método CBaseWindow. DoShowWindow (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.DoShowWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a2a1f7d4cd9bc4600733d5d33f9df6d3b6998f57
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679574"
---
# <a name="cbasewindowdoshowwindow-method"></a>CBaseWindow. DoShowWindow, método

El método **DoShowWindow** establece el estado de presentación de la ventana.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT DoShowWindow(
   LONG ShowCmd
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ShowCmd* 
</dt> <dd>

Marca que especifica cómo se mostrará la ventana. El valor puede ser cualquier constante definida para el parámetro *nCmdShow* de la función [**ShowWindow**](/windows/desktop/api/winuser/nf-winuser-showwindow) .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Winutil. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseWindow**](cbasewindow.md)
</dt> </dl>

 

