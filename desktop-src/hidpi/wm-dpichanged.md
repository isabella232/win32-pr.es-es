---
title: WM_DPICHANGED mensaje (WinUser.h)
description: Se envía cuando han cambiado los puntos efectivos por pulgada (ppp) de una ventana.
ms.assetid: 97C458F2-89CD-45FF-ABEE-F158A3BCE0B8
keywords:
- WM_DPICHANGED mensaje Valores altos de PPP
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
ms.openlocfilehash: d77a7d7608e9facc1e0fc6973b19a3d9db36900fa8d550896cc3058389f367bc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119666385"
---
# <a name="wm_dpichanged-message"></a>Mensaje \_ DE PPPCHANGED de WM

Se envía cuando han cambiado los puntos efectivos por pulgada (ppp) de una ventana. El valor de PPP es el factor de escala de una ventana. Hay varios eventos que pueden hacer que cambie el valor de PPP. En la lista siguiente se indican las posibles causas del cambio en PPP.

-   La ventana se mueve a un nuevo monitor que tiene un PPP diferente.
-   Cambia el valor de PPP del monitor que hospeda la ventana.

El valor de PPP actual de una ventana siempre es igual al último PPP enviado por **WM \_ PPPCHANGED.** Este es el factor de escala al que se debe escalar la ventana para los subprocesos que conocen los cambios de PPP.


```C++
#define WM_DPICHANGED       0x02E0
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

HiWORD [**del**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) *wParam* contiene el valor del eje Y del nuevo ppp de la ventana. El [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) del *wParam* contiene el valor del eje X del nuevo PPP de la ventana. Por ejemplo, 96, 120, 144 o 192. Los valores del eje X y el eje Y son idénticos para Windows aplicaciones.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura RECT**](/windows/desktop/api/windef/ns-windef-rect) que proporciona un tamaño y una posición sugeridos de la ventana actual escalada para el nuevo PPP. La expectativa es que las aplicaciones cambien la posición y cambien el tamaño de las ventanas en función de las sugerencias proporcionadas por *lParam* al controlar este mensaje.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si una aplicación procesa este mensaje, debe devolver cero.

## <a name="remarks"></a>Comentarios

Este mensaje solo es relevante para los subprocesos **PROCESS PER MONITOR DPI AWARE \_ \_ \_ \_ o** **DPI AWARENESS PER MONITOR \_ \_ \_ \_ AWARE.** Se puede recibir en determinados cambios de PPP si el proceso o ventana de nivel superior se ejecuta como **PPP** no consciente o compatible con **PPP** del sistema, pero en esas situaciones se puede omitir de forma segura. Para obtener más información sobre los distintos tipos de reconocimiento, vea PROCESAR RECONOCIMIENTO [**\_ de PPP \_ y**](/windows/desktop/api/ShellScalingApi/ne-shellscalingapi-process_dpi_awareness) [**RECONOCIMIENTO DE \_ PPP.**](/windows/desktop/api/windef/ne-windef-dpi_awareness) Las versiones anteriores de Windows que el reconocimiento de PPP se vinculase en el nivel de una aplicación. Esas aplicaciones usan **PROCESS \_ DPI \_ AWARENESS**. Actualmente, el reconocimiento de PPP está vinculado a subprocesos y ventanas individuales en lugar de a toda la aplicación. Estas aplicaciones usan **RECONOCIMIENTO DE \_ PPP.**

Solo tiene que usar el eje X o el valor del eje Y al escalar la aplicación, ya que son los mismos.

Para controlar este mensaje correctamente, deberá cambiar el tamaño y la posición de la ventana en función de las sugerencias proporcionadas por *lParam* y el uso [**de SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos). Si no lo hace, la ventana crecerá o se reducirá con respecto a todo lo demás en el nuevo monitor. Por ejemplo, si un usuario usa varios monitores y arrastra la ventana desde un monitor de 96 PPP a un monitor de 192 PPP, la ventana parecerá ser la mitad de grande con respecto a otros elementos del monitor de 192 PPP.

El valor base de PPP se define como PPP DE PANTALLA PREDETERMINADO DEL USUARIO, que se establece en 96. **\_ \_ \_** Para determinar el factor de escalado de un monitor, tome el valor de PPP y divida por PPP **DE PANTALLA PREDETERMINADA DEL \_ \_ \_ USUARIO.** En la tabla siguiente se proporcionan algunos valores de PPP de ejemplo y factores de escalado asociados.



| Valor de PPP | Porcentaje de escalado |
|-----------|--------------------|
| 96        | 100 %               |
| 120       | 125%               |
| 144       | 150%               |
| 192       | 200%               |



 

En el ejemplo siguiente se proporciona un controlador de cambios de PPP de ejemplo.


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



El código siguiente escala linealmente un valor del 100 % (96 PPP) a un PPP arbitrario definido por *g \_ ppp*.


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



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8.1 solo aplicaciones de escritorio\]<br/>                                         |
| Servidor mínimo compatible<br/> | Windows Server 2012 Solo aplicaciones \[ de escritorio R2\]<br/>                              |
| Header<br/>                   | <dl> <dt>WinUser.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**RECONOCIMIENTO DE \_ PPP**](/windows/desktop/api/windef/ne-windef-dpi_awareness)
</dt> <dt>

[**RECONOCIMIENTO DE \_ PPP \_ DE PROCESO**](/windows/desktop/api/ShellScalingApi/ne-shellscalingapi-process_dpi_awareness)
</dt> </dl>

 

