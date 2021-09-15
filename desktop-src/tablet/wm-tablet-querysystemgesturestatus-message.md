---
description: Se envía cuando el sistema pregunta a una ventana qué gestos del sistema le gustaría recibir.
ms.assetid: 5b747b3c-3b77-4913-932f-182114d1f674
title: WM_TABLET_QUERYSYSTEMGESTURESTATUS mensaje (Tpcshrd.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 395196f963cae9b8d18697276e546f1eba05b245
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127247707"
---
# <a name="wm_tablet_querysystemgesturestatus-message"></a>Mensaje \_ WM TABLET \_ QUERYSYSTEMGESTURESTATUS

Se envía cuando el sistema pregunta a una ventana qué gestos del sistema le gustaría recibir.


```C++
#define WM_TABLET_DEFBASE                    0x02C0
#define WM_TABLET_QUERYSYSTEMGESTURESTATUS   (WM_TABLET_DEFBASE + 12)       
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

No se usa.

</dd> <dt>

*lParam* 
</dt> <dd>

Valor de punto que representa las coordenadas de la pantalla.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Al controlar este mensaje, puede deshabilitar dinámicamente los gestos para las regiones de una ventana.

> [!Note]  
> *LParam se* puede convertir en coordenadas x e y mediante las `GET_X_LPARAM` macros y `GET_Y_LPARAM` .

 

De forma predeterminada, la ventana recibirá todos los eventos de gesto del sistema. Puede elegir qué eventos desea que reciba la ventana y qué eventos desea deshabilitar respondiendo al mensaje **WM \_ TABLET \_ QUERYSYSTEMGESTURESTATUS** en **WndProc**. El **mensaje WM TABLET \_ \_ QUERYSYSTEMGESTURESTATUS** se define en tpcshrd.h. Los valores para habilitar y deshabilitar los gestos del sistema de tabletas del sistema también se definen en tpcshrd.h como se muestra a continuación:

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
> La deshabilitación de la presión y la retención mejorará la capacidad de respuesta de los clics del mouse, ya que esta funcionalidad crea un tiempo de espera para distinguir entre las dos operaciones.

 

Tenga cuidado al controlar el **mensaje WM \_ TABLET \_ QUERYSYSTEMGESTURESTATUS.** **WM \_ TABLET \_ QUERYSYSTEMGESTURESTATUS se** pasa mediante la función [**SendMessageTimeout.**](/windows/win32/api/winuser/nf-winuser-sendmessagetimeouta) Si llama a métodos en una interfaz COM, ese objeto debe estar dentro del mismo proceso. Si no es así, COM produce una excepción.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra cómo deshabilitar los gestos de una región mediante WM \_ TABLET \_ QUERYSYSTEMGESTURESTATUS.


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
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>Tpcshrd.h</dt> </dl> |



 

 
