---
title: Mensaje de WM_GETDPISCALEDSIZE (Winuser. h)
description: Este mensaje indica al sistema operativo que el tamaño de la ventana se ajustará a dimensiones distintas de las predeterminadas.
ms.assetid: 038CAA21-0944-45D3-8C40-A6498F36D9E4
keywords:
- WM_GETDPISCALEDSIZE máximo de PPP del mensaje
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
ms.openlocfilehash: b95631e51247d7919307f36dd0af10c72621a612
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490750"
---
# <a name="wm_getdpiscaledsize-message"></a>Mensaje de GETDPISCALEDSIZE de WM \_

Este mensaje indica al sistema operativo que el tamaño de la ventana se ajustará a dimensiones distintas de las predeterminadas.

Este mensaje se envía a ventanas de nivel superior con un [ \_ \_ contexto de reconocimiento de PPP](dpi-awareness-context.md) de por monitor V2 antes de que se envíe un mensaje de [**\_ DPICHANGED de WM**](wm-dpichanged.md) y permite que la ventana calcule su tamaño deseado para el cambio de PPP pendiente. Como el ajuste de escala lineal de PPP es el comportamiento predeterminado, esto solo resulta útil en escenarios donde la ventana desea escalar de forma no lineal. Si la aplicación responde a este mensaje, el tamaño resultante será el rectángulo candidato enviado a **WM \_ DPICHANGED**.

Use este mensaje para modificar el tamaño del rectángulo que se proporciona con [**WM \_ DPICHANGED**](wm-dpichanged.md).


```C++
#define WM_GETDPISCALEDSIZE       0x02E4
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

WPARAM contiene un valor de PPP. El tamaño de la ventana escalada que establecería la aplicación debe calcularse como si la ventana cambiara a este valor de PPP.

</dd> <dt>

*lParam* 
</dt> <dd>

LPARAM es un puntero de in/out a una estructura de tamaño. El \_ valor de in \_ de lParam es el tamaño pendiente de la ventana después de un movimiento iniciado por el usuario o una llamada a [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos). Si se cambia el tamaño de la ventana, este tamaño no es necesariamente el mismo que el tamaño actual de la ventana en el momento en que se recibe este mensaje.

El \_ \_ valor out en lParam debe escribirse en la aplicación para especificar el tamaño de ventana escalado deseado correspondiente al valor de PPP proporcionado en el wParam.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

La función devuelve un BOOLEANO. Si devuelve TRUE, indica que se ha calculado un nuevo tamaño. Si devuelve FALSE, indica que el mensaje no se controlará y el ajuste de escala lineal de PPP se aplicará a la ventana.

## <a name="remarks"></a>Observaciones

Este mensaje solo se envía a las ventanas de nivel superior que tienen un contexto de reconocimiento de PPP de por monitor V2.

Este evento es necesario para facilitar el escalado no lineal estable y garantiza que la posición de Windows permanezca constante en relación con el cursor y al avanzar y retroceder por los monitores.

No hay ningún control predeterminado específico de este mensaje en [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca). En cuanto a todos los mensajes que no controla explícitamente, [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca) devolverá cero para este mensaje. Como se indicó anteriormente, este valor devuelto indica al sistema que use el comportamiento lineal predeterminado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 10, versión 1703 \[\]<br/>                            |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2016 \[\]<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>Winuser. h</dt> </dl> |



 

