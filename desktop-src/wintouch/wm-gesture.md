---
title: Mensaje de WM_GESTURE (Winuser. h)
description: Pasa información sobre un gesto.
ms.assetid: 4167aeb0-2c31-4b7b-ad1b-e6d37da09ef8
keywords:
- Mensaje de WM_GESTURE de Windows Touch
topic_type:
- apiref
api_name:
- WM_GESTURE
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d1184d1f54d110f84630a727decb91ad28e6c08
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422453"
---
# <a name="wm_gesture-message"></a>Mensaje de gesto de WM \_

Pasa información sobre un gesto.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Proporciona información que identifica el comando de gestos y los valores de argumento específicos de gestos. Esta información es la misma que se pasa en el miembro **ullArguments** de la estructura [**GESTUREINFO**](/windows/win32/api/winuser/ns-winuser-gestureinfo) .

</dd> <dt>

*lParam* 
</dt> <dd>

Proporciona un identificador para la información que identifica el comando de gesto y los valores de argumento específicos de gestos. Esta información se recupera llamando a [**GetGestureInfo**](/windows/desktop/api/winuser/nf-winuser-getgestureinfo).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si una aplicación procesa este mensaje, debe devolver 0.

Si la aplicación no procesa el mensaje, debe llamar a [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca). Si no lo hace, la aplicación perderá memoria porque no se cerrará el identificador de entrada táctil y no se liberará la memoria de proceso asociada.

## <a name="remarks"></a>Observaciones

En la tabla siguiente se enumeran los comandos de gestos compatibles.



| IDENTIFICADOR de gesto            | Valor (*dwID*) | Descripción                                                                                                                                                                                                                                                                          |
|-----------------------|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Inicio de GID \_**        | 1              | Indica que se está iniciando un gesto genérico.                                                                                                                                                                                                                                            |
| **fin de GID \_**          | 2              | Indica un fin de movimiento genérico.                                                                                                                                                                                                                                                     |
| **ZOOM de GID \_**         | 3              | Indica inicio de zoom, movimiento de zoom o detención de zoom. El primer mensaje del comando **\_ zoom de Gid** comienza un zoom pero no produce ningún zoom. El segundo **comando \_ zoom de Gid** desencadena un zoom relativo al estado contenido en el primer **\_ zoom de Gid**.                                    |
| **PAN de GID \_**          | 4              | Indica movimiento de la panorámica o inicio de la panorámica. El primer comando de **\_ pan de Gid** indica un inicio de pan pero no realiza ningún movimiento panorámico. Con el segundo mensaje de comando **\_ pan de Gid** , la aplicación iniciará el movimiento panorámico.                                                                            |
| **GID- \_ girar**       | 5              | Indica el cambio de giro o el inicio de giro. El primer mensaje de comando de **\_ girar GID** indica un movimiento de giro o un inicio de giro, pero no gira. El segundo mensaje de comando de **\_ girar GID** desencadenará una operación de rotación en relación con el estado contenido en el primer **GID \_**. |
| **GID \_ TWOFINGERTAP** | 6              | Indica el gesto de puntear dos dedos.                                                                                                                                                                                                                                                    |
| **GID \_ PRESSANDTAP**  | 7              | Indica el gesto de presionar y tocar.                                                                                                                                                                                                                                                 |



 

> [!Note]  
> Para habilitar la compatibilidad heredada, se deben reenviar los mensajes con los comandos de gestos de **\_ Inicio** y de **\_ fin** de Gid con [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca).

 

En la tabla siguiente se indican los argumentos de gestos pasados en los parámetros *lParam* y *wParam* .



| IDENTIFICADOR de gesto            | Gesto        | *ullArgument*                                                                                                                                                                                                                                                                                                                                                                                            | *ptsLocation* en la estructura [**GestureInfo**](/windows/desktop/api/winuser/nf-winuser-getgestureinfo)                                                  |
|-----------------------|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| **ZOOM de GID \_**         | Acercar/alejar    | Indica la distancia entre los dos puntos.                                                                                                                                                                                                                                                                                                                                                           | Indica el centro del zoom.                                                                                 |
| **PAN de GID \_**          | Movimiento panorámico            | Indica la distancia entre los dos puntos.                                                                                                                                                                                                                                                                                                                                                           | Indica la posición actual de la panorámica.                                                                        |
| **GID- \_ girar**       | Girar (dinamizar) | Indica el ángulo de rotación si se establece la marca de **\_ Inicio GF** . De lo contrario, este es el cambio de ángulo desde que se ha iniciado la rotación. Está firmado para indicar la dirección de la rotación. Use el [**\_ \_ ángulo de rotación \_ de Gid desde el \_ argumento**](/windows/desktop/api/winuser/nf-winuser-gid_rotate_angle_from_argument) y el ángulo de rotación de Gid a las macros de [**\_ \_ \_ \_ argumento**](/windows/desktop/api/winuser/nf-winuser-gid_rotate_angle_to_argument) para obtener y establecer el valor del ángulo. | Indica el centro del giro, que es el punto estacionario en el que se gira el objeto de destino. |
| **GID \_ TWOFINGERTAP** | Tap con dos dedos | Indica la distancia entre los dos dedos.                                                                                                                                                                                                                                                                                                                                                          | Indica el centro de los dos dedos.                                                                          |
| **GID \_ PRESSANDTAP**  | Pulse y haga clic en  | Indica la diferencia entre el primer dedo y el segundo dedo. Este valor se almacena en los 32 bits inferiores de *ullArgument* en una estructura **Point** .                                                                                                                                                                                                                                             | Indica la posición en la que se activa el primer dedo.                                                       |



 

> [!Note]  
> Todas las distancias y posiciones se proporcionan en coordenadas de pantalla físicas.

 

> [!Note]  
> Los parámetros *dwID* y *ullArgument* solo se deben considerar para acompañar a los \_ \* comandos GID y las aplicaciones no deben modificarlos.

 

## <a name="examples"></a>Ejemplos

En el código siguiente se muestra cómo obtener información específica del gesto asociada a este mensaje.

> [!Note]  
> Siempre debe reenviar los mensajes no controlados a [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca) y debe cerrar el identificador de entrada de gestos para los mensajes que administra con una llamada a [**CloseGestureInfoHandle**](/windows/desktop/api/winuser/nf-winuser-closegestureinfohandle). En este ejemplo, el comportamiento predeterminado del controlador de gestos se suprimirá porque el identificador TOUCHINPUT se cierra en cada uno de los casos de gestos. Si quitó los casos en el código anterior para mensajes no controlados, el controlador de gestos predeterminado procesaría los mensajes enviándose a [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca) en el caso predeterminado.

 


```C++
  LRESULT DecodeGesture(HWND hWnd, UINT message, WPARAM wParam, LPARAM lParam){
    // Create a structure to populate and retrieve the extra message info.
    GESTUREINFO gi;  
    
    ZeroMemory(&gi, sizeof(GESTUREINFO));
    
    gi.cbSize = sizeof(GESTUREINFO);

    BOOL bResult  = GetGestureInfo((HGESTUREINFO)lParam, &gi);
    BOOL bHandled = FALSE;

    if (bResult){
        // now interpret the gesture
        switch (gi.dwID){
           case GID_ZOOM:
               // Code for zooming goes here     
               bHandled = TRUE;
               break;
           case GID_PAN:
               // Code for panning goes here
               bHandled = TRUE;
               break;
           case GID_ROTATE:
               // Code for rotation goes here
               bHandled = TRUE;
               break;
           case GID_TWOFINGERTAP:
               // Code for two-finger tap goes here
               bHandled = TRUE;
               break;
           case GID_PRESSANDTAP:
               // Code for roll over goes here
               bHandled = TRUE;
               break;
           default:
               // A gesture was not recognized
               break;
        }
    }else{
        DWORD dwErr = GetLastError();
        if (dwErr > 0){
            //MessageBoxW(hWnd, L"Error!", L"Could not retrieve a GESTUREINFO structure.", MB_OK);
        }
    }
    if (bHandled){
        return 0;
    }else{
        return DefWindowProc(hWnd, message, wParam, lParam);
    }
  }
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                                               |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]<br/>                                                  |
| Encabezado<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Notificaciones](notifications.md)
</dt> <dt>

[Guía de programación de gestos táctiles de Windows](guide-multi-touch-gestures.md)
</dt> </dl>

 

