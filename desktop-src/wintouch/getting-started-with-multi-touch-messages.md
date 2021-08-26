---
title: Tareas iniciales con Windows touch messages
description: En esta sección se explican las tareas asociadas a la Windows entrada táctil para funcionar en la aplicación.
ms.assetid: cd4e140e-a0b8-494f-82d9-bc0bfba55ecd
keywords:
- Windows Touch,messages
- Windows Touch,registering for touch input
- Windows Digitalizadores de entrada táctiles y de prueba
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d3f1daac2aacf8ac4c34ccbf9b1ab8be63058c45096e181c8b2eecf4f5d2de6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120055905"
---
# <a name="getting-started-with-windows-touch-messages"></a>Tareas iniciales con Windows touch messages

En esta sección se explican las tareas asociadas a la Windows entrada táctil para funcionar en la aplicación.

Normalmente, los pasos siguientes se realizan al trabajar con Windows touch:

1.  Pruebe las funcionalidades del digitalizador de entrada.
2.  Regístrese para recibir Windows touch.
3.  Controle los mensajes.

El mensaje usado para Windows Touch es [**WM \_ TOUCH.**](wm-touchdown.md) Este mensaje indica los distintos estados de contacto con un digitalizador.

## <a name="testing-the-capabilities-of-the-input-digitizer"></a>Prueba de las funcionalidades del digitalizador de entrada

La [función GetSystemMetrics](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) se puede usar para consultar las funciones del digitalizador de entrada pasando el *valor nIndex* de SM **\_ DIGITALIZADOR.** [GetSystemMetrics](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) devuelve un campo de bits que indica si el dispositivo está listo, si el dispositivo admite lápiz o táctil, si el dispositivo de entrada está integrado o externo, y si el dispositivo admite varias entradas (Windows Touch). En la tabla siguiente se muestran los bits de los distintos campos.



| bit   | 8           | 7           | 6        | 5        | 4            | 3              | 2              | 1                |
|-------|-------------|-------------|----------|----------|--------------|----------------|----------------|------------------|
| Value | Listo para la pila | Multi-input | Reservado | Reservado | Lápiz externo | Lápiz integrado | External Touch | Integrated Touch |



 

Para probar el resultado del comando para una característica determinada, puede usar el operador de & bit a bit y el bit concreto que está probando. Por ejemplo, para probar Windows touch, probaría que el bit de séptimo orden está establecido (0x40 en hexadecimal). En el ejemplo de código siguiente se muestra cómo se podrían probar estos valores.


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



En la tabla siguiente se enumeran las constantes definidas en windows.h para probar las funcionalidades táctiles del digitalizador de entrada.



| Nombre                   | Value      | Descripción                                                                                                                                                                                   |
|------------------------|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CONFIGURACIÓN \_ DE TABLETA \_ NONE   | 0x00000000 | El digitalizador de entrada no tiene funcionalidades táctiles.                                                                                                                                         |
| NID \_ INTEGRATED \_ TOUCH | 0x00000001 | Se usa un digitalizador táctil integrado para la entrada.                                                                                                                                              |
| NID \_ EXTERNAL \_ TOUCH   | 0x00000002 | Se usa un digitalizador táctil externo para la entrada.                                                                                                                                                |
| NID \_ INTEGRATED \_ PEN   | 0x00000004 | Se usa un digitalizador de lápiz integrado para la entrada.                                                                                                                                                |
| NID \_ EXTERNAL \_ PEN     | 0x00000008 | Se usa un digitalizador de lápiz externo para la entrada.                                                                                                                                                  |
| ENTRADA MÚLTIPLE DE NID \_ \_      | 0x00000040 | Para la entrada se usa un digitalizador de entrada compatible con varias entradas.                                                                                                                        |
| LISTO PARA \_ NID             | 0x00000080 | El digitalizador de entrada está listo para la entrada. Si este valor no está predeterminado, puede significar que se detiene el servicio de tabletas, que no se admite el digitalizador o que no se han instalado los controladores del digitalizador. |



 

Comprobar los valores de NID es una manera útil de comprobar las funcionalidades del equipo de un usuario para configurar la aplicación para entrada táctil, de lápiz o que no \_ \* sea de tableta. Por ejemplo, si tiene una interfaz de usuario dinámica (UI) y desea configurar automáticamente parte de ella, puede comprobar si tiene NID \_ INTEGRATED \_ TOUCH, NID MULTITOUCH y podría obtener el número máximo de toques la primera vez que un usuario ejecuta \_ la aplicación.

> [!Note]  
> Existen algunas limitaciones inherentes para SM \_ GETSYSTEMMETRICS. Por ejemplo, no hay compatibilidad con plug and play. Por este motivo, tenga cuidado al usar esta función como medio para la configuración permanente.

 

## <a name="registering-to-receive-windows-touch-input"></a>Registro para recibir datos Windows entrada táctil

Antes de recibir Windows entrada táctil, las aplicaciones deben registrarse primero para recibir Windows entrada táctil. Al registrar la ventana de la aplicación, la aplicación indica que es compatible con la pantalla táctil. Una vez que la aplicación registra su ventana, las notificaciones del controlador Windows Touch se reenvía a la aplicación cuando se realiza la entrada en la ventana. Cuando la aplicación se cierra, anula el registro de su ventana para deshabilitar las notificaciones.

> [!Note]  
> [**WM \_ Los**](wm-touchdown.md) mensajes TOUCH son actualmente "expansión". Después de recibir el primer mensaje táctil en una ventana, todos los mensajes táctiles se envían a esa ventana hasta que otra ventana recibe el foco.

 

> [!Note]  
> De forma predeterminada, recibe mensajes [**WM \_ GESTURE**](wm-gesture.md) en lugar de [**mensajes WM \_ TOUCH.**](wm-touchdown.md) Si llama a [**RegisterTouchWindow**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow), dejará de recibir mensajes **\_ WM GESTURE.**

 

El código siguiente muestra cómo una aplicación podría registrarse para recibir Windows touch en una aplicación Win32.


```C++
RegisterTouchWindow(hWnd, 0);
```



## <a name="handling-windows-touch-messages"></a>Control de Windows touch messages

Puede controlar los mensajes Windows Touch de las aplicaciones de Windows sistemas operativos de muchas maneras. Si está programando una aplicación gui, agregue código dentro de la `WndProc` función para controlar los mensajes de interés. Si está programando una aplicación de Microsoft Foundation Class (MFC) o administrada, agregue controladores para los mensajes de interés. En el ejemplo de código siguiente se muestra cómo se podrían controlar los mensajes táctiles desde WndProc en una Windows basada en aplicaciones.


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





El código siguiente muestra cómo puede implementar la asignación de mensajes y un controlador de mensajes. Tenga en cuenta que los mensajes deben declararse en la asignación de mensajes y, a continuación, se debe implementar el controlador del mensaje. Por ejemplo, en una aplicación MFC, esto se podría declarar en el código del cuadro de diálogo. Tenga en cuenta también que la función de la ventana de diálogo tendría que incluir `OnInitDialog` una llamada a [**RegisterTouchWindow**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow) como `RegisterTouchWindow(m_hWnd, 0)` .


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

[Windows Entrada táctil](guide-multi-touch-input.md)
</dt> </dl>

 

 