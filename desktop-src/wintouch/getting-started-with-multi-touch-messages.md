---
title: Introducción con mensajes táctiles de Windows
description: En esta sección se explican las tareas asociadas a la entrada táctil de Windows para que funcionen en la aplicación.
ms.assetid: cd4e140e-a0b8-494f-82d9-bc0bfba55ecd
keywords:
- Windows Touch, mensajes
- Windows Touch, registro para entrada táctil
- Windows Touch, probar digitalizadores de entrada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b39048a4f9d643026396328093ae554c0eaa5d08
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104420852"
---
# <a name="getting-started-with-windows-touch-messages"></a>Introducción con mensajes táctiles de Windows

En esta sección se explican las tareas asociadas a la entrada táctil de Windows para que funcionen en la aplicación.

Los pasos siguientes se realizan normalmente al trabajar con mensajes de Windows Touch:

1.  Probar las capacidades del digitalizador de entrada.
2.  Regístrese para recibir mensajes de Windows Touch.
3.  Controle los mensajes.

El mensaje que se usa para Windows Touch es el [**\_ toque de WM**](wm-touchdown.md). Este mensaje indica los distintos Estados de contacto con un digitalizador.

## <a name="testing-the-capabilities-of-the-input-digitizer"></a>Probar las capacidades del digitalizador de entrada

La función [GetSystemMetrics](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) se puede usar para consultar las funciones del digitalizador de entrada pasando el valor *NINDEX* del **\_ digitalizador SM**. [GetSystemMetrics](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) devuelve un campo de bits que indica si el dispositivo está listo, si el dispositivo admite el lápiz o el toque, si el dispositivo de entrada está integrado o externo, y si el dispositivo admite varias entradas (Windows Touch). En la tabla siguiente se muestran los bits de los distintos campos.



| bit   | 8           | 7           | 6        | 5        | 4            | 3              | 2              | 1                |
|-------|-------------|-------------|----------|----------|--------------|----------------|----------------|------------------|
| Value | Pila preparada | Entrada múltiple | Reservado | Reservado | Lápiz externo | Lápiz integrado | Interacción externa | Interacción táctil integrada |



 

Para probar el resultado del comando para una característica determinada, puede utilizar el operador bit a bit & y el bit determinado que está probando. Por ejemplo, para probar la función táctil de Windows, probaría que se establece el bit de séptima orden (0x40 en hex). En el ejemplo de código siguiente se muestra cómo se pueden probar estos valores.


```C++
#include <windows.h>
```




```C++
// test for touch
int value = GetSystemMetrics(SM_DIGITIZER);
if (value & NID_READY){ /* stack ready */}
if (value  & NID_MULTI_INPUT){
    /* digitizer is multitouch */ 
    MessageBoxW(hWnd, L"Multitouch found", L"IsMulti!", MB_OK);
}
if (value & NID_INTEGRATED_TOUCH){ /* Integrated touch */}
```



En la tabla siguiente se enumeran las constantes definidas en Windows. h para probar las capacidades táctiles del digitalizador de entrada.



| Nombre                   | Value      | Descripción                                                                                                                                                                                   |
|------------------------|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| configuración de TABLET PC \_ \_ ninguno   | 0x00000000 | El digitalizador de entrada no tiene capacidades táctiles.                                                                                                                                         |
| \_Touch Integrated de Nid \_ | 0x00000001 | Se usa un digitalizador táctil integrado para la entrada.                                                                                                                                              |
| \_táctil externa de Nid \_   | 0x00000002 | Un digitalizador táctil externo se usa para la entrada.                                                                                                                                                |
| \_lápiz integrado de Nid \_   | 0x00000004 | Se usa un digitalizador de lápiz integrado para la entrada.                                                                                                                                                |
| \_lápiz externo de Nid \_     | 0x00000008 | Un digitalizador de lápiz externo se usa para la entrada.                                                                                                                                                  |
| \_entrada múltiple de Nid \_      | 0x00000040 | Se usa un digitalizador de entrada compatible con varias entradas para la entrada.                                                                                                                        |
| NID \_ preparado             | 0x00000080 | El digitalizador de entrada está listo para la entrada. Si este valor no está establecido, puede significar que se ha detenido el servicio de tableta, que el digitalizador no es compatible o que no se han instalado controladores de digitalizador. |



 

La comprobación de los \_ \* valores de Nid es una manera útil de comprobar las capacidades del equipo de un usuario para configurar la aplicación para la entrada táctil, manuscrita o no de Tablet PC. Por ejemplo, si tiene una interfaz de usuario (UI) dinámica y desea configurar automáticamente algunas de ellas, podría comprobar la \_ interacción táctil integrada de Nid \_ , Nid \_ multitoque y podría obtener el número máximo de retoques la primera vez que un usuario ejecute la aplicación.

> [!Note]  
> Hay algunas limitaciones inherentes para SM \_ GETSYSTEMMETRICS. Por ejemplo, no se admiten plug and Play. Por esta razón, tenga cuidado al usar esta función como un medio para la configuración permanente.

 

## <a name="registering-to-receive-windows-touch-input"></a>Registro para recibir entradas táctiles de Windows

Antes de recibir la entrada táctil de Windows, las aplicaciones deben registrarse primero para recibir la entrada táctil de Windows. Al registrar la ventana de la aplicación, la aplicación indica que es compatible con funciones táctiles. Una vez que la aplicación registra su ventana, las notificaciones del controlador de Windows Touch se reenvían a la aplicación cuando se realiza la entrada en la ventana. Cuando se cierra la aplicación, anula el registro de su ventana para deshabilitar las notificaciones.

> [!Note]  
> [**WM \_ Los mensajes TÁCTILes**](wm-touchdown.md) son actualmente "expansivos". Una vez recibido el primer mensaje táctil en una ventana, todos los mensajes táctiles se envían a esa ventana hasta que otra ventana recibe el foco.

 

> [!Note]  
> De forma predeterminada, recibe mensajes de [**\_ gestos de WM**](wm-gesture.md) en lugar de mensajes [**\_ táctiles de WM**](wm-touchdown.md) . Si llama a [**RegisterTouchWindow**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow), dejará de recibir mensajes de **\_ gestos de WM** .

 

En el código siguiente se muestra cómo una aplicación podría registrarse para recibir mensajes de Windows Touch en una aplicación Win32.


```C++
RegisterTouchWindow(hWnd, 0);
```



## <a name="handling-windows-touch-messages"></a>Controlar mensajes de Windows Touch

Puede controlar los mensajes táctiles de Windows desde las aplicaciones de los sistemas operativos Windows de muchas maneras. Si está programando una aplicación de GUI, agregue código dentro de la `WndProc` función para controlar los mensajes de interés. Si está programando un Microsoft Foundation Class (MFC) o una aplicación administrada, agregue Controladores para los mensajes de interés. En el ejemplo de código siguiente se muestra cómo se pueden controlar los mensajes Touch desde WndProc en una aplicación basada en Windows.


```C++
  LRESULT OnTouch(HWND hWnd, WPARAM wParam, LPARAM lParam ){
    BOOL bHandled = FALSE;
    UINT cInputs = LOWORD(wParam);
    PTOUCHINPUT pInputs = new TOUCHINPUT[cInputs];
    if (pInputs){
        if (GetTouchInputInfo((HTOUCHINPUT)lParam, cInputs, pInputs, sizeof(TOUCHINPUT))){
            for (UINT i=0; i < cInputs; i++){
                TOUCHINPUT ti = pInputs[i];
                //do something with each touch input entry
            }            
            bHandled = TRUE;
        }else{
             /* handle the error here */
        }
        delete [] pInputs;
    }else{
        /* handle the error here, probably out of memory */
    }
    if (bHandled){
        // if you handled the message, close the touch input handle and return
        CloseTouchInputHandle((HTOUCHINPUT)lParam);
        return 0;
    }else{
        // if you didn't handle the message, let DefWindowProc handle it
        return DefWindowProc(hWnd, WM_TOUCH, wParam, lParam);
    }
  }


LRESULT CALLBACK WndProc(HWND hWnd, UINT message, WPARAM wParam, LPARAM lParam)
{
    int wmId, wmEvent;
    PAINTSTRUCT ps;
    HDC hdc;

    switch (message)
    {
      // pass touch messages to the touch handler 
      case WM_TOUCH:
        OnTouch(hWnd, wParam, lParam);
        break;
```





En el código siguiente se muestra cómo puede implementar el mapa de mensajes y un controlador de mensajes. Tenga en cuenta que los mensajes se deben declarar en el mapa de mensajes y, a continuación, se debe implementar el controlador del mensaje. Por ejemplo, en una aplicación MFC, se podría declarar en el código del cuadro de diálogo. Tenga en cuenta también que la `OnInitDialog` función de la ventana de cuadro de diálogo tendría que incluir una llamada a [**RegisterTouchWindow**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow) como `RegisterTouchWindow(m_hWnd, 0)` .


```C++
  // Class implementations within a dialog
  LRESULT TestDlg::OnTouch( WPARAM wParam, LPARAM lParam ){
    //Insert handler code here to do something with the message or uncomment the following line to test
    //MessageBox(L"touch!", L"touch!", MB_OK);
    return 0;
  }
  // The message map
  BEGIN_MESSAGE_MAP()
    ON_WM_CREATE()
    ... ... ...
    ON_MESSAGE(WM_TOUCH, OnTouch)
  END_MESSAGE_MAP()  
 
  BOOL TestDlg::OnInitDialog()
  {
    CDialog::OnInitDialog();    

    RegisterTouchWindow(m_hWnd, 0);
     ... ... ...
  }  
  
```



Al tocar la ventana, se indicarán los toques de una ventana emergente.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Entrada táctil de Windows](guide-multi-touch-input.md)
</dt> </dl>

 

 