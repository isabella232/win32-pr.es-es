---
title: WM_GETDPISCALEDSIZE mensaje (Winuser.h)
description: Este mensaje indica al sistema operativo que la ventana tendrá un tamaño distinto del predeterminado.
ms.assetid: 038CAA21-0944-45D3-8C40-A6498F36D9E4
keywords:
- WM_GETDPISCALEDSIZE con valores altos de PPP
topic_type:
- apiref
api_name:
- WM_GETDPISCALEDSIZE
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3386a0f38187e375f9dae0e390a413a1e64565f15d39e1e9f1e436c9238bea99
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118759296"
---
# <a name="wm_getdpiscaledsize-message"></a>Mensaje \_ GETDPISCALEDSIZE de WM

Este mensaje indica al sistema operativo que la ventana tendrá un tamaño distinto del predeterminado.

Este mensaje se envía a ventanas de nivel superior con un CONTEXTO DE RECONOCIMIENTO DE [PPP \_ \_](dpi-awareness-context.md) de Por monitor v2 antes de enviar un mensaje [**WM \_ PPPCHANGED**](wm-dpichanged.md) y permite que la ventana calcule el tamaño deseado para el cambio de PPP pendiente. Como el ajuste de escala de PPP lineal es el comportamiento predeterminado, esto solo es útil en escenarios en los que la ventana quiere escalar de forma no lineal. Si la aplicación responde a este mensaje, el tamaño resultante será el rectángulo candidato que se enviará a **WM \_ PPPCHANGED.**

Use este mensaje para modificar el tamaño del rect que se proporciona con [**WM \_ PPPCHANGED**](wm-dpichanged.md).


```C++
#define WM_GETDPISCALEDSIZE       0x02E4
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

WPARAM contiene un valor de PPP. El tamaño de ventana escalado que establecería la aplicación debe calcularse como si la ventana cambiara a este valor de PPP.

</dd> <dt>

*lParam* 
</dt> <dd>

El LPARAM es un puntero de entrada y salida a una estructura SIZE. El valor In del LPARAM es el tamaño pendiente de la ventana después de un movimiento iniciado por el usuario o una llamada \_ \_ a [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos). Si se cambia el tamaño de la ventana, este tamaño no es necesariamente el mismo que el tamaño actual de la ventana en el momento en que se recibe este mensaje.

La aplicación debe escribir el valor Out del LPARAM para especificar el tamaño de ventana escalado deseado correspondiente al valor de PPP proporcionado \_ \_ en WPARAM.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

La función devuelve un valor BOOL. Devolver TRUE indica que se ha calculado un nuevo tamaño. Devolver FALSE indica que el mensaje no se controlará y el escalado de PPP lineal predeterminado se aplicará a la ventana.

## <a name="remarks"></a>Comentarios

Este mensaje solo se envía a ventanas de nivel superior que tienen un contexto de reconocimiento de PPP por monitor v2.

Este evento es necesario para facilitar el escalado no lineal estable y garantiza que la posición de las ventanas permanece constante en relación con el cursor y al moverse de un lado a otro entre monitores.

No hay ningún control predeterminado específico de este mensaje en [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca). Al igual que para todos los mensajes que no controla explícitamente, [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca) devolverá cero para este mensaje. Como se indicó anteriormente, esta devolución indica al sistema que use el comportamiento lineal predeterminado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 10, solo aplicaciones de escritorio de la versión 1703 \[\]<br/>                            |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2016 \[\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Winuser.h</dt> </dl> |



 

