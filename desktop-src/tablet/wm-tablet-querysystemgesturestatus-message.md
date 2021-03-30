---
description: Se envía cuando el sistema pide a una ventana qué gestos del sistema desea recibir.
ms.assetid: 5b747b3c-3b77-4913-932f-182114d1f674
title: Mensaje de WM_TABLET_QUERYSYSTEMGESTURESTATUS (Tpcshrd. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 395196f963cae9b8d18697276e546f1eba05b245
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907908"
---
# <a name="wm_tablet_querysystemgesturestatus-message"></a>\_Mensaje de QUERYSYSTEMGESTURESTATUS de Tablet PC de WM \_

Se envía cuando el sistema pide a una ventana qué gestos del sistema desea recibir.


```C++
#define WM_TABLET_DEFBASE                    0x02C0
#define WM_TABLET_QUERYSYSTEMGESTURESTATUS   (WM_TABLET_DEFBASE + 12)       
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

No se utiliza.

</dd> <dt>

*lParam* 
</dt> <dd>

Un valor de punto que representa las coordenadas de la pantalla.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Al controlar este mensaje, puede deshabilitar los gestos de forma dinámica para las regiones de una ventana.

> [!Note]  
> *LParam* se puede convertir en coordenadas x e y mediante las `GET_X_LPARAM` `GET_Y_LPARAM` macros y.

 

De forma predeterminada, la ventana recibirá todos los eventos de gestos del sistema. Puede elegir los eventos que desea que reciba la ventana y los eventos que desea deshabilitar al responder al mensaje de **\_ \_ QUERYSYSTEMGESTURESTATUS** de la tableta de WM en el **WndProc**. El mensaje de **\_ \_ QUERYSYSTEMGESTURESTATUS** de la tableta de WM se define en tpcshrd. h. Los valores para habilitar y deshabilitar los gestos del sistema de la tableta del sistema también se definen en tpcshrd. h de la siguiente manera:

``` syntax
#define TABLET_DISABLE_PRESSANDHOLD        0x00000001
#define TABLET_DISABLE_PENTAPFEEDBACK      0x00000008
#define TABLET_DISABLE_PENBARRELFEEDBACK   0x00000010
#define TABLET_DISABLE_TOUCHUIFORCEON      0x00000100
#define TABLET_DISABLE_TOUCHUIFORCEOFF     0x00000200
#define TABLET_DISABLE_TOUCHSWITCH         0x00008000
#define TABLET_DISABLE_FLICKS              0x00010000
#define TABLET_ENABLE_FLICKSONCONTEXT      0x00020000
#define TABLET_ENABLE_FLICKLEARNINGMODE    0x00040000
#define TABLET_DISABLE_SMOOTHSCROLLING     0x00080000
#define TABLET_DISABLE_FLICKFALLBACKKEYS   0x00100000
#define TABLET_ENABLE_MULTITOUCHDATA       0x01000000
```

> [!Note]
>
> Al deshabilitar la función de mantener presionado se mejora la capacidad de respuesta de los clics del mouse porque esta funcionalidad crea un tiempo de espera para distinguir entre las dos operaciones.

 

Tenga precaución al controlar el mensaje de **\_ \_ QUERYSYSTEMGESTURESTATUS** de la tableta de WM. **WM \_ TABLET \_ QUERYSYSTEMGESTURESTATUS** se pasa mediante la función [**SendMessageTimeout**](/windows/win32/api/winuser/nf-winuser-sendmessagetimeouta) . Si llama a métodos en una interfaz COM, ese objeto debe estar dentro del mismo proceso. De lo contrario, COM produce una excepción.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra cómo deshabilitar los gestos para una región mediante WM \_ Tablet \_ QUERYSYSTEMGESTURESTATUS.


```C++
#include <windowsx.h>        

(...)        
        
LRESULT CALLBACK WndProc(HWND hWnd, UINT message, WPARAM wParam, LPARAM lParam){
    case WM_TABLET_QUERYSYSTEMGESTURESTATUS:
        int x = GET_X_LPARAM(lParam);
        int y = GET_Y_LPARAM(lParam);
        if (x < xThreashold && y < yThreshold){
            // no flicks in the region specified by the threashold
            return TABLET_DISABLE_FLICKS;
        }
        // flicks will happen otherwise
        return 0;
}        
        
```



En el ejemplo siguiente se muestra cómo deshabilitar varias características de gestos para una ventana completa.


```C++
const DWORD dwHwndTabletProperty = 
    TABLET_DISABLE_PRESSANDHOLD | // disables press and hold (right-click) gesture
    TABLET_DISABLE_PENTAPFEEDBACK | // disables UI feedback on pen up (waves)
    TABLET_DISABLE_PENBARRELFEEDBACK | // disables UI feedback on pen button down (circle)
    TABLET_DISABLE_FLICKS; // disables pen flicks (back, forward, drag down, drag up)
        
void SetTabletpenserviceProperties(HWND hWnd){
    ATOM atom = ::GlobalAddAtom(MICROSOFT_TABLETPENSERVICE_PROPERTY);    
    ::SetProp(hWnd, MICROSOFT_TABLETPENSERVICE_PROPERTY, reinterpret_cast<HANDLE>(dwHwndTabletProperty));
    ::GlobalDeleteAtom(atom);
}        
        
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>Tpcshrd. h</dt> </dl> |



 

 
