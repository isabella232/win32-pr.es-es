---
Description: Se envía a una ventana después de cambiar su tamaño.
ms.assetid: e3e14dcd-9236-48bd-a692-6985d8146f81
title: Mensaje de WM_SIZE (Winuser. h)
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/27/2020
ms.openlocfilehash: 04afafd3faafc4ea8c400472254dcf4ec4afa050
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105650195"
---
# <a name="wm_size-message"></a>Mensaje de tamaño de WM \_

Se envía a una ventana después de cambiar su tamaño.

Una ventana recibe este mensaje a través de su función [**WindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca) .


```C++
#define WM_SIZE                         0x0005
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Tipo de cambio de tamaño solicitado. Este parámetro puede ser uno de los valores siguientes.



| Valor                                                                                                                                                                                                                   | Significado                                                                                                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span id="SIZE_MAXHIDE"></span><span id="size_maxhide"></span><dl> <dt>**Tamaño \_ de MAXHIDE**</dt> <dt>4</dt> </dl>       | El mensaje se envía a todas las ventanas emergentes cuando se maximiza otra ventana.<br/>                              |
| <span id="SIZE_MAXIMIZED"></span><span id="size_maximized"></span><dl> <dt>**Tamaño \_ de MAXIMIZAdo**</dt> <dt>2</dt> </dl> | La ventana se ha maximizado.<br/>                                                                          |
| <span id="SIZE_MAXSHOW"></span><span id="size_maxshow"></span><dl> <dt>**Tamaño \_ de MAXSHOW**</dt> <dt>3</dt> </dl>       | El mensaje se envía a todas las ventanas emergentes cuando otra ventana se ha restaurado a su tamaño anterior.<br/>      |
| <span id="SIZE_MINIMIZED"></span><span id="size_minimized"></span><dl> <dt>**Tamaño \_ de MINIMIZAda**</dt> <dt>1</dt> </dl> | La ventana está minimizada.<br/>                                                                          |
| <span id="SIZE_RESTORED"></span><span id="size_restored"></span><dl> <dt>**Tamaño \_ de RESTAURAdo**</dt> <dt>0</dt> </dl>    | Se ha cambiado el tamaño de la ventana, pero no se aplica el valor de **tamaño \_ minimizado** ni **tamaño \_ maximizado** .<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

La palabra de orden inferior de *lParam* especifica el nuevo ancho del área cliente.

La palabra de orden superior de *lParam* especifica el nuevo alto del área cliente.

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

Ejemplo de [ejemplos clásicos de Windows](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/Win7Samples/multimedia/DirectWrite/HelloWorld/SimpleText.cpp) en github.

## <a name="remarks"></a>Observaciones

Si se llama a la función [**SetScrollPos**](https://msdn.microsoft.com/library/Cc411085(v=MSDN.10).aspx) o [**MoveWindow**](/windows/win32/api/winuser/nf-winuser-movewindow) para una ventana secundaria como resultado del mensaje **de \_ tamaño de WM** , el parámetro *bRedraw* o *bRepaint* debe ser distinto de cero para que la ventana se vuelva a dibujar.

Aunque el ancho y el alto de una ventana son valores de 32 bits, el parámetro *lParam* solo contiene los 16 bits de orden inferior de cada uno.

La función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) envía los mensajes de **\_ tamaño de WM** y **\_ movimiento de WM** cuando procesa el mensaje de [**\_ WINDOWPOSCHANGED de WM**](wm-windowposchanged.md) .
Los mensajes de **\_ tamaño de WM** y **\_ movimiento de WM** no se envían si una aplicación controla el mensaje de **\_ WINDOWPOSCHANGED de WM** sin llamar a **DefWindowProc**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



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

[**WINDOWPOSCHANGED de WM \_**](wm-windowposchanged.md)
</dt> <dt>

**Vista**
</dt> <dt>

[Windows](windows.md)
</dt> <dt>

**Otros recursos**
</dt> <dt>

[**SetScrollPos**](https://msdn.microsoft.com/library/Cc411085(v=MSDN.10).aspx)
</dt> </dl>

 

 
