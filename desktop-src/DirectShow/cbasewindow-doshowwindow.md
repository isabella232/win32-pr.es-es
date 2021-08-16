---
description: El método DoShowWindow establece el estado de presentación de la ventana.
ms.assetid: 4180de9d-ef40-40e3-aa37-be54283b1f97
title: Método CBaseWindow.DoShowWindow (Winutil.h)
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
ms.openlocfilehash: 7fef63e04d0e04f2fe0daa78cd6b33a22fa7c8fa14c57b1e022703dea0914dab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119074638"
---
# <a name="cbasewindowdoshowwindow-method"></a>Método CBaseWindow.DoShowWindow

El **método DoShowWindow** establece el estado de presentación de la ventana.

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

Marca que especifica cómo se va a mostrar la ventana. El valor puede ser cualquier constante definida para el *parámetro nCmdShow* de la [**función ShowWindow.**](/windows/desktop/api/winuser/nf-winuser-showwindow)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Winutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CBaseWindow (clase)**](cbasewindow.md)
</dt> </dl>

 

