---
description: El método GetClassWindowStyles recupera los estilos de clase y de ventana de la ventana.
ms.assetid: 6eec7912-c654-4e4f-b6f1-ec94c7284575
title: Método CBaseWindow.GetClassWindowStyles (Winutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.GetClassWindowStyles
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ba7042069d4f1190a88b25ea4cc349e8230c149dd61d2d06fc91fa3439a9e55f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119074639"
---
# <a name="cbasewindowgetclasswindowstyles-method"></a>Método CBaseWindow.GetClassWindowStyles

El método recupera los estilos de clase y de ventana de `GetClassWindowStyles` la ventana.

## <a name="syntax"></a>Sintaxis


```C++
virtual LPTSTR GetClassWindowStyles(
   DWORD *pClassStyles,
   DWORD *pWindowStyles,
   DWORD *pWindowStylesEx
) = 0;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pClassStyles* 
</dt> <dd>

Puntero a una variable que recibe los estilos de clase.

</dd> <dt>

*pWindowStyles* 
</dt> <dd>

Puntero a una variable que recibe los estilos de ventana.

</dd> <dt>

*pWindowStylesEx* 
</dt> <dd>

Puntero a una variable que recibe los estilos de ventana extendidos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve una cadena de texto estático que contiene el nombre de clase.

## <a name="remarks"></a>Comentarios

El [**método CBaseWindow::P repareWindow**](cbasewindow-preparewindow.md) llama a este método para recuperar los estilos de clase y de ventana de la ventana.

Este método es virtual puro; la clase derivada debe implementarla. En el ejemplo siguiente se muestra una posible implementación:


```C++
LPTSTR CMyWindowClass::GetClassWindowStyles(DWORD *pClassStyles,
                                            DWORD *pWindowStyles,
                                            DWORD *pWindowStylesEx)
{
    *pClassStyles = CS_HREDRAW | CS_VREDRAW;
    *pWindowStyles = WS_OVERLAPPEDWINDOW | WS_CLIPCHILDREN;
    *pWindowStylesEx = WS_EX_WINDOWEDGE;
    return TEXT("MyWindowClass");
}
```



El objeto usa el estilo de clase para el **miembro lpszClassName** de una estructura WNDCLASS, que pasa a la **función RegisterClass.** El objeto usa los estilos de ventana para los *parámetros dwExStyle* y *dwStyle* de la **función CreateWindowEx.** Para obtener más información, consulte el SDK de plataforma.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Winutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseWindow (clase)**](cbasewindow.md)
</dt> </dl>

 

 




