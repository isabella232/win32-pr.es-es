---
Description: Se envía a una ventana después de cambiar su tamaño.
ms.assetid: e3e14dcd-9236-48bd-a692-6985d8146f81
title: WM_SIZE mensaje (Winuser.h)
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/27/2020
ms.openlocfilehash: 473e4e63523c7b97968e54349e5882b7e589fc7238d717ccf96563b5ce93388e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119548225"
---
# <a name="wm_size-message"></a>Mensaje \_ WM SIZE

Se envía a una ventana después de cambiar su tamaño.

Una ventana recibe este mensaje a través de su [**función WindowProc.**](/windows/win32/api/winuser/nf-winuser-defwindowproca)


```C++
#define WM_SIZE                         0x0005
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Tipo de tamaño solicitado. Este parámetro puede ser uno de los valores siguientes.



| Valor                                                                                                                                                                                                                   | Significado                                                                                                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span id="SIZE_MAXHIDE"></span><span id="size_maxhide"></span><dl> <dt>**TAMAÑO \_ MAXHIDE**</dt> <dt>4</dt> </dl>       | El mensaje se envía a todas las ventanas emergentes cuando se maximiza alguna otra ventana.<br/>                              |
| <span id="SIZE_MAXIMIZED"></span><span id="size_maximized"></span><dl> <dt>**TAMAÑO \_ MAXIMIZADO**</dt> <dt>2</dt> </dl> | La ventana se ha maximizado.<br/>                                                                          |
| <span id="SIZE_MAXSHOW"></span><span id="size_maxshow"></span><dl> <dt>**TAMAÑO \_ MAXSHOW**</dt> <dt>3</dt> </dl>       | El mensaje se envía a todas las ventanas emergentes cuando alguna otra ventana se ha restaurado a su tamaño anterior.<br/>      |
| <span id="SIZE_MINIMIZED"></span><span id="size_minimized"></span><dl> <dt>**TAMAÑO \_ MINIMIZADO**</dt> <dt>1</dt> </dl> | La ventana se ha minimizado.<br/>                                                                          |
| <span id="SIZE_RESTORED"></span><span id="size_restored"></span><dl> <dt>**TAMAÑO \_ RESTAURADO**</dt> <dt>0</dt> </dl>    | Se ha cambiado el tamaño de la ventana, pero no se aplica el valor **\_ SIZE MINIMIZED** ni **SIZE \_ MAXIMIZED.**<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

La palabra de orden bajo *de lParam* especifica el nuevo ancho del área de cliente.

La palabra de orden superior *de lParam* especifica el nuevo alto del área cliente.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **LRESULT**

Si una aplicación procesa este mensaje, debe devolver cero.

## <a name="example"></a>Ejemplo

```cpp
/******************************************************************
*                                                                 *
*  SimpleText::OnResize                                           *
*                                                                 *
*  If the application receives a WM_SIZE message, this method     *
*  resize the render target appropriately.                        *
*                                                                 *
******************************************************************/

void SimpleText::OnResize(UINT width, UINT height)
{
    if (pRT_)
    {
        D2D1_SIZE_U size;
        size.width = width;
        size.height = height;
        pRT_->Resize(size);
    }
}

LRESULT CALLBACK SimpleText::WndProc(HWND hwnd, UINT message, WPARAM wParam, LPARAM lParam)
{
   
    SimpleText *pSimpleText = reinterpret_cast<SimpleText *>(
                ::GetWindowLongPtr(hwnd, GWLP_USERDATA));

    if (pSimpleText)
    {
        switch(message)
        {
        case WM_SIZE:
            {
                UINT width = LOWORD(lParam);
                UINT height = HIWORD(lParam);
                pSimpleText->OnResize(width, height);
            }
            return 0;

// ...

```

Ejemplo de [Windows ejemplos clásicos](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/Win7Samples/multimedia/DirectWrite/HelloWorld/SimpleText.cpp) en GitHub.

## <a name="remarks"></a>Comentarios

Si se llama a la función [**SetScrollPos**](https://msdn.microsoft.com/library/Cc411085(v=MSDN.10).aspx) o [**MoveWindow**](/windows/win32/api/winuser/nf-winuser-movewindow) para una ventana secundaria como resultado del mensaje **WM \_ SIZE,** el parámetro *bRedraw* o *bRepaint* debe ser distinto de cero para hacer que la ventana se vuelva a dibujar.

Aunque el ancho y alto de una ventana son valores de 32 bits, el parámetro *lParam* contiene solo los 16 bits de orden inferior de cada uno.

La [**función DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) envía los mensajes **WM \_ SIZE** y **WM \_ MOVE** cuando procesa el [**mensaje \_ WINDOWPOSCHANGED de WM.**](wm-windowposchanged.md)
Los **mensajes WM \_ SIZE** y **WM \_ MOVE** no se envían si una aplicación controla el mensaje **\_ WINDOWPOSCHANGED** de WM sin llamar **a DefWindowProc**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

[**MoveWindow**](/windows/win32/api/winuser/nf-winuser-movewindow)
</dt> <dt>

[**VENTANA \_ WMPOSCHANGED**](wm-windowposchanged.md)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Windows](windows.md)
</dt> <dt>

**Otros recursos**
</dt> <dt>

[**SetScrollPos**](https://msdn.microsoft.com/library/Cc411085(v=MSDN.10).aspx)
</dt> </dl>

 

 
