---
title: Mensaje de WM_DPICHANGED (WinUser. h)
description: Se envía cuando cambian los puntos por pulgada (PPP) efectivos de una ventana.
ms.assetid: 97C458F2-89CD-45FF-ABEE-F158A3BCE0B8
keywords:
- WM_DPICHANGED máximo de PPP del mensaje
topic_type:
- apiref
api_name:
- WM_DPICHANGED
api_location:
- WinUser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aafbce1e784e1f205f0d32e045785125c1fb5aaa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802527"
---
# <a name="wm_dpichanged-message"></a>Mensaje de DPICHANGED de WM \_

Se envía cuando cambian los puntos por pulgada (PPP) efectivos de una ventana. El PPP es el factor de escala de una ventana. Hay varios eventos que pueden hacer que el PPP cambie. En la lista siguiente se indican las posibles causas del cambio en PPP.

-   La ventana se mueve a un nuevo monitor que tiene un PPP diferente.
-   El PPP del monitor que hospeda la ventana cambia.

Los PPP actuales de una ventana siempre son iguales a los últimos PPP enviados por **WM \_ DPICHANGED**. Este es el factor de escala al que se debe ajustar la ventana para los subprocesos que tienen en cuenta los cambios de PPP.


```C++
#define WM_DPICHANGED       0x02E0
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

El [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) del *wParam* contiene el valor del eje Y del nuevo PPP de la ventana. El [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) del *wParam* contiene el valor del eje X del nuevo PPP de la ventana. Por ejemplo, 96, 120, 144 o 192. Los valores de los ejes X y y son idénticos para las aplicaciones de Windows.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**Rect**](/windows/desktop/api/windef/ns-windef-rect) que proporciona un tamaño sugerido y una posición de la ventana actual escalada para el nuevo ppp. La expectativa es que las aplicaciones cambien la posición y el tamaño de las ventanas en función de las sugerencias proporcionadas por *lParam* al controlar este mensaje.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si una aplicación procesa este mensaje, debe devolver cero.

## <a name="remarks"></a>Observaciones

Este mensaje solo es relevante para el proceso por las aplicaciones con reconocimiento de **\_ \_ \_ PPP \_ de monitor** o el reconocimiento de PPP por subprocesos que **\_ \_ \_ \_ reconocen el monitor** . Puede que se reciba en determinados cambios de PPP si el proceso o la ventana de nivel superior se ejecutan con reconocimiento de **PPP** o con **PPP del sistema**, pero en esas situaciones se puede pasar por alto sin ningún problema. Para obtener más información acerca de los diferentes tipos de reconocimiento, vea reconocimiento de [**PPP de proceso \_ \_**](/windows/desktop/api/ShellScalingApi/ne-shellscalingapi-process_dpi_awareness) y [**\_ reconocimiento de PPP**](/windows/desktop/api/windef/ne-windef-dpi_awareness). Las versiones anteriores de Windows requerían que el reconocimiento de PPP se asociara en el nivel de una aplicación. Esas aplicaciones usan **el \_ \_ reconocimiento de PPP de proceso**. Actualmente, el reconocimiento de PPP está asociado a los subprocesos y a las ventanas individuales en lugar de a toda la aplicación. Estas aplicaciones usan **\_ reconocimiento de PPP**.

Solo tiene que usar el eje X o el valor del eje Y al escalar la aplicación, ya que son iguales.

Para controlar este mensaje correctamente, tendrá que cambiar el tamaño y la posición de la ventana en función de las sugerencias proporcionadas por *lParam* y el uso de [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos). Si no lo hace, la ventana aumentará o disminuirá con respecto a todo lo demás en el nuevo monitor. Por ejemplo, si un usuario usa varios monitores y arrastra la ventana desde un monitor de 96 PPP a un monitor de 192 PPP, parecerá que la ventana es la mitad del tamaño con respecto a otros elementos del monitor de 192 ppp.

El valor base de DPI se define como **\_ PPP de \_ pantalla \_ predeterminada del usuario** , que se establece en 96. Para determinar el factor de escala de un monitor, tome el valor de PPP y divida según los **\_ \_ \_ PPP de pantalla predeterminados del usuario**. En la tabla siguiente se proporcionan algunos valores de PPP de ejemplo y los factores de escala asociados.



| Valor de PPP | Porcentaje de escalado |
|-----------|--------------------|
| 96        | 100%               |
| 120       | 125%               |
| 144       | 150%               |
| 192       | 200%               |



 

En el ejemplo siguiente se proporciona un controlador de cambio de PPP de ejemplo.


```C++
    case WM_DPICHANGED:
    {
        g_dpi = HIWORD(wParam);
        UpdateDpiDependentFontsAndResources();

        RECT* const prcNewWindow = (RECT*)lParam;
        SetWindowPos(hWnd,
            NULL,
            prcNewWindow ->left,
            prcNewWindow ->top,
            prcNewWindow->right - prcNewWindow->left,
            prcNewWindow->bottom - prcNewWindow->top,
            SWP_NOZORDER | SWP_NOACTIVATE);
        break;
    }
```



El código siguiente escala linealmente un valor del 100% (96 PPP) a un DPI arbitrario definido por *g \_ DPI*.


```C++
    INT iBorderWidth100 = 5;
    iBorderWidth = MulDiv(iBorderWidth100, g_dpi, USER_DEFAULT_SCREEN_DPI);
```



Una manera alternativa de escalar un valor es convertir el valor de PPP en un factor de escala y usarlo.


```C++
    INT iBorderWidth100 = 5;
    FLOAT fscale = (float) g_dpi / USER_DEFAULT_SCREEN_DPI;
    iBorderWidth = iBorderWidth100 * fscale;
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio Windows 8.1\]<br/>                                         |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 R2 \[\]<br/>                              |
| Encabezado<br/>                   | <dl> <dt>WinUser. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**reconocimiento de PPP \_**](/windows/desktop/api/windef/ne-windef-dpi_awareness)
</dt> <dt>

[**\_reconocimiento de PPP de proceso \_**](/windows/desktop/api/ShellScalingApi/ne-shellscalingapi-process_dpi_awareness)
</dt> </dl>

 

