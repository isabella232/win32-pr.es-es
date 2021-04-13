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
# <a name="getting-started-with-windows-touch-messages"></a><span data-ttu-id="5d830-106">Introducción con mensajes táctiles de Windows</span><span class="sxs-lookup"><span data-stu-id="5d830-106">Getting Started with Windows Touch Messages</span></span>

<span data-ttu-id="5d830-107">En esta sección se explican las tareas asociadas a la entrada táctil de Windows para que funcionen en la aplicación.</span><span class="sxs-lookup"><span data-stu-id="5d830-107">This section explains the tasks associated with getting Windows Touch input to function in your application.</span></span>

<span data-ttu-id="5d830-108">Los pasos siguientes se realizan normalmente al trabajar con mensajes de Windows Touch:</span><span class="sxs-lookup"><span data-stu-id="5d830-108">The following steps are typically performed when working with Windows Touch messages:</span></span>

1.  <span data-ttu-id="5d830-109">Probar las capacidades del digitalizador de entrada.</span><span class="sxs-lookup"><span data-stu-id="5d830-109">Test the capabilities of the input digitizer.</span></span>
2.  <span data-ttu-id="5d830-110">Regístrese para recibir mensajes de Windows Touch.</span><span class="sxs-lookup"><span data-stu-id="5d830-110">Register to receive Windows Touch messages.</span></span>
3.  <span data-ttu-id="5d830-111">Controle los mensajes.</span><span class="sxs-lookup"><span data-stu-id="5d830-111">Handle the messages.</span></span>

<span data-ttu-id="5d830-112">El mensaje que se usa para Windows Touch es el [**\_ toque de WM**](wm-touchdown.md).</span><span class="sxs-lookup"><span data-stu-id="5d830-112">The message used for Windows Touch is [**WM\_TOUCH**](wm-touchdown.md).</span></span> <span data-ttu-id="5d830-113">Este mensaje indica los distintos Estados de contacto con un digitalizador.</span><span class="sxs-lookup"><span data-stu-id="5d830-113">This message indicates the various states of contact with a digitizer.</span></span>

## <a name="testing-the-capabilities-of-the-input-digitizer"></a><span data-ttu-id="5d830-114">Probar las capacidades del digitalizador de entrada</span><span class="sxs-lookup"><span data-stu-id="5d830-114">Testing the Capabilities of the Input Digitizer</span></span>

<span data-ttu-id="5d830-115">La función [GetSystemMetrics](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) se puede usar para consultar las funciones del digitalizador de entrada pasando el valor *NINDEX* del **\_ digitalizador SM**.</span><span class="sxs-lookup"><span data-stu-id="5d830-115">The [GetSystemMetrics](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) function can be used to query the capabilities of the input digitizer by passing in the *nIndex* value of **SM\_DIGITIZER**.</span></span> <span data-ttu-id="5d830-116">[GetSystemMetrics](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) devuelve un campo de bits que indica si el dispositivo está listo, si el dispositivo admite el lápiz o el toque, si el dispositivo de entrada está integrado o externo, y si el dispositivo admite varias entradas (Windows Touch).</span><span class="sxs-lookup"><span data-stu-id="5d830-116">[GetSystemMetrics](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) returns a bit field that indicates whether the device is ready, whether the device supports pen or touch, whether the input device is integrated or external, and whether the device supports multiple inputs (Windows Touch).</span></span> <span data-ttu-id="5d830-117">En la tabla siguiente se muestran los bits de los distintos campos.</span><span class="sxs-lookup"><span data-stu-id="5d830-117">The following table shows the bits for the various fields.</span></span>



| <span data-ttu-id="5d830-118">bit</span><span class="sxs-lookup"><span data-stu-id="5d830-118">Bit</span></span>   | <span data-ttu-id="5d830-119">8</span><span class="sxs-lookup"><span data-stu-id="5d830-119">8</span></span>           | <span data-ttu-id="5d830-120">7</span><span class="sxs-lookup"><span data-stu-id="5d830-120">7</span></span>           | <span data-ttu-id="5d830-121">6</span><span class="sxs-lookup"><span data-stu-id="5d830-121">6</span></span>        | <span data-ttu-id="5d830-122">5</span><span class="sxs-lookup"><span data-stu-id="5d830-122">5</span></span>        | <span data-ttu-id="5d830-123">4</span><span class="sxs-lookup"><span data-stu-id="5d830-123">4</span></span>            | <span data-ttu-id="5d830-124">3</span><span class="sxs-lookup"><span data-stu-id="5d830-124">3</span></span>              | <span data-ttu-id="5d830-125">2</span><span class="sxs-lookup"><span data-stu-id="5d830-125">2</span></span>              | <span data-ttu-id="5d830-126">1</span><span class="sxs-lookup"><span data-stu-id="5d830-126">1</span></span>                |
|-------|-------------|-------------|----------|----------|--------------|----------------|----------------|------------------|
| <span data-ttu-id="5d830-127">Value</span><span class="sxs-lookup"><span data-stu-id="5d830-127">Value</span></span> | <span data-ttu-id="5d830-128">Pila preparada</span><span class="sxs-lookup"><span data-stu-id="5d830-128">Stack Ready</span></span> | <span data-ttu-id="5d830-129">Entrada múltiple</span><span class="sxs-lookup"><span data-stu-id="5d830-129">Multi-input</span></span> | <span data-ttu-id="5d830-130">Reservado</span><span class="sxs-lookup"><span data-stu-id="5d830-130">Reserved</span></span> | <span data-ttu-id="5d830-131">Reservado</span><span class="sxs-lookup"><span data-stu-id="5d830-131">Reserved</span></span> | <span data-ttu-id="5d830-132">Lápiz externo</span><span class="sxs-lookup"><span data-stu-id="5d830-132">External Pen</span></span> | <span data-ttu-id="5d830-133">Lápiz integrado</span><span class="sxs-lookup"><span data-stu-id="5d830-133">Integrated Pen</span></span> | <span data-ttu-id="5d830-134">Interacción externa</span><span class="sxs-lookup"><span data-stu-id="5d830-134">External Touch</span></span> | <span data-ttu-id="5d830-135">Interacción táctil integrada</span><span class="sxs-lookup"><span data-stu-id="5d830-135">Integrated Touch</span></span> |



 

<span data-ttu-id="5d830-136">Para probar el resultado del comando para una característica determinada, puede utilizar el operador bit a bit & y el bit determinado que está probando.</span><span class="sxs-lookup"><span data-stu-id="5d830-136">To test the result from the command for a particular feature, you can use the bitwise & operator and the particular bit you are testing.</span></span> <span data-ttu-id="5d830-137">Por ejemplo, para probar la función táctil de Windows, probaría que se establece el bit de séptima orden (0x40 en hex).</span><span class="sxs-lookup"><span data-stu-id="5d830-137">For example, to test for Windows Touch, you would test that the seventh-order bit is set (0x40 in hex).</span></span> <span data-ttu-id="5d830-138">En el ejemplo de código siguiente se muestra cómo se pueden probar estos valores.</span><span class="sxs-lookup"><span data-stu-id="5d830-138">The following code example shows how these values could be tested.</span></span>


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



<span data-ttu-id="5d830-139">En la tabla siguiente se enumeran las constantes definidas en Windows. h para probar las capacidades táctiles del digitalizador de entrada.</span><span class="sxs-lookup"><span data-stu-id="5d830-139">The following table lists the constants defined in windows.h for testing touch capabilities of the input digitizer.</span></span>



| <span data-ttu-id="5d830-140">Nombre</span><span class="sxs-lookup"><span data-stu-id="5d830-140">Name</span></span>                   | <span data-ttu-id="5d830-141">Value</span><span class="sxs-lookup"><span data-stu-id="5d830-141">Value</span></span>      | <span data-ttu-id="5d830-142">Descripción</span><span class="sxs-lookup"><span data-stu-id="5d830-142">Description</span></span>                                                                                                                                                                                   |
|------------------------|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5d830-143">configuración de TABLET PC \_ \_ ninguno</span><span class="sxs-lookup"><span data-stu-id="5d830-143">TABLET\_CONFIG\_NONE</span></span>   | <span data-ttu-id="5d830-144">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5d830-144">0x00000000</span></span> | <span data-ttu-id="5d830-145">El digitalizador de entrada no tiene capacidades táctiles.</span><span class="sxs-lookup"><span data-stu-id="5d830-145">The input digitizer does not have touch capabilities.</span></span>                                                                                                                                         |
| <span data-ttu-id="5d830-146">\_Touch Integrated de Nid \_</span><span class="sxs-lookup"><span data-stu-id="5d830-146">NID\_INTEGRATED\_TOUCH</span></span> | <span data-ttu-id="5d830-147">0x00000001</span><span class="sxs-lookup"><span data-stu-id="5d830-147">0x00000001</span></span> | <span data-ttu-id="5d830-148">Se usa un digitalizador táctil integrado para la entrada.</span><span class="sxs-lookup"><span data-stu-id="5d830-148">An integrated touch digitizer is used for input.</span></span>                                                                                                                                              |
| <span data-ttu-id="5d830-149">\_táctil externa de Nid \_</span><span class="sxs-lookup"><span data-stu-id="5d830-149">NID\_EXTERNAL\_TOUCH</span></span>   | <span data-ttu-id="5d830-150">0x00000002</span><span class="sxs-lookup"><span data-stu-id="5d830-150">0x00000002</span></span> | <span data-ttu-id="5d830-151">Un digitalizador táctil externo se usa para la entrada.</span><span class="sxs-lookup"><span data-stu-id="5d830-151">An external touch digitizer is used for input.</span></span>                                                                                                                                                |
| <span data-ttu-id="5d830-152">\_lápiz integrado de Nid \_</span><span class="sxs-lookup"><span data-stu-id="5d830-152">NID\_INTEGRATED\_PEN</span></span>   | <span data-ttu-id="5d830-153">0x00000004</span><span class="sxs-lookup"><span data-stu-id="5d830-153">0x00000004</span></span> | <span data-ttu-id="5d830-154">Se usa un digitalizador de lápiz integrado para la entrada.</span><span class="sxs-lookup"><span data-stu-id="5d830-154">An integrated pen digitizer is used for input.</span></span>                                                                                                                                                |
| <span data-ttu-id="5d830-155">\_lápiz externo de Nid \_</span><span class="sxs-lookup"><span data-stu-id="5d830-155">NID\_EXTERNAL\_PEN</span></span>     | <span data-ttu-id="5d830-156">0x00000008</span><span class="sxs-lookup"><span data-stu-id="5d830-156">0x00000008</span></span> | <span data-ttu-id="5d830-157">Un digitalizador de lápiz externo se usa para la entrada.</span><span class="sxs-lookup"><span data-stu-id="5d830-157">An external pen digitizer is used for input.</span></span>                                                                                                                                                  |
| <span data-ttu-id="5d830-158">\_entrada múltiple de Nid \_</span><span class="sxs-lookup"><span data-stu-id="5d830-158">NID\_MULTI\_INPUT</span></span>      | <span data-ttu-id="5d830-159">0x00000040</span><span class="sxs-lookup"><span data-stu-id="5d830-159">0x00000040</span></span> | <span data-ttu-id="5d830-160">Se usa un digitalizador de entrada compatible con varias entradas para la entrada.</span><span class="sxs-lookup"><span data-stu-id="5d830-160">An input digitizer with support for multiple inputs is used for input.</span></span>                                                                                                                        |
| <span data-ttu-id="5d830-161">NID \_ preparado</span><span class="sxs-lookup"><span data-stu-id="5d830-161">NID\_READY</span></span>             | <span data-ttu-id="5d830-162">0x00000080</span><span class="sxs-lookup"><span data-stu-id="5d830-162">0x00000080</span></span> | <span data-ttu-id="5d830-163">El digitalizador de entrada está listo para la entrada.</span><span class="sxs-lookup"><span data-stu-id="5d830-163">The input digitizer is ready for input.</span></span> <span data-ttu-id="5d830-164">Si este valor no está establecido, puede significar que se ha detenido el servicio de tableta, que el digitalizador no es compatible o que no se han instalado controladores de digitalizador.</span><span class="sxs-lookup"><span data-stu-id="5d830-164">If this value is unset, it may mean that the tablet service is stopped, the digitizer is not supported, or digitizer drivers have not been installed.</span></span> |



 

<span data-ttu-id="5d830-165">La comprobación de los \_ \* valores de Nid es una manera útil de comprobar las capacidades del equipo de un usuario para configurar la aplicación para la entrada táctil, manuscrita o no de Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="5d830-165">Checking the NID\_\* values is a useful way of checking the capabilities of a user's computer to configure your application for touch, pen, or non-tablet input.</span></span> <span data-ttu-id="5d830-166">Por ejemplo, si tiene una interfaz de usuario (UI) dinámica y desea configurar automáticamente algunas de ellas, podría comprobar la \_ interacción táctil integrada de Nid \_ , Nid \_ multitoque y podría obtener el número máximo de retoques la primera vez que un usuario ejecute la aplicación.</span><span class="sxs-lookup"><span data-stu-id="5d830-166">For example, if you have a dynamic user interface (UI) and want to automatically configure some of it, you could check for NID\_INTEGRATED\_TOUCH, NID\_MULTITOUCH, and could get the maximum number of touches the first time that a user runs your application.</span></span>

> [!Note]  
> <span data-ttu-id="5d830-167">Hay algunas limitaciones inherentes para SM \_ GETSYSTEMMETRICS.</span><span class="sxs-lookup"><span data-stu-id="5d830-167">There are some inherent limitations for SM\_GETSYSTEMMETRICS.</span></span> <span data-ttu-id="5d830-168">Por ejemplo, no se admiten plug and Play.</span><span class="sxs-lookup"><span data-stu-id="5d830-168">For example, there is no support for plug and play.</span></span> <span data-ttu-id="5d830-169">Por esta razón, tenga cuidado al usar esta función como un medio para la configuración permanente.</span><span class="sxs-lookup"><span data-stu-id="5d830-169">For this reason, use caution when using this function as a means for permanent configuration.</span></span>

 

## <a name="registering-to-receive-windows-touch-input"></a><span data-ttu-id="5d830-170">Registro para recibir entradas táctiles de Windows</span><span class="sxs-lookup"><span data-stu-id="5d830-170">Registering to Receive Windows Touch Input</span></span>

<span data-ttu-id="5d830-171">Antes de recibir la entrada táctil de Windows, las aplicaciones deben registrarse primero para recibir la entrada táctil de Windows.</span><span class="sxs-lookup"><span data-stu-id="5d830-171">Before receiving Windows Touch input, applications must first register to receive Windows Touch input.</span></span> <span data-ttu-id="5d830-172">Al registrar la ventana de la aplicación, la aplicación indica que es compatible con funciones táctiles.</span><span class="sxs-lookup"><span data-stu-id="5d830-172">By registering the application window, the application indicates that it is touch compatible.</span></span> <span data-ttu-id="5d830-173">Una vez que la aplicación registra su ventana, las notificaciones del controlador de Windows Touch se reenvían a la aplicación cuando se realiza la entrada en la ventana.</span><span class="sxs-lookup"><span data-stu-id="5d830-173">After the application registers its window, notifications from the Windows Touch driver are forwarded to the application when input is made on the window.</span></span> <span data-ttu-id="5d830-174">Cuando se cierra la aplicación, anula el registro de su ventana para deshabilitar las notificaciones.</span><span class="sxs-lookup"><span data-stu-id="5d830-174">When the application shuts down, it unregisters its window to disable notifications.</span></span>

> [!Note]  
> <span data-ttu-id="5d830-175">[**WM \_ Los mensajes TÁCTILes**](wm-touchdown.md) son actualmente "expansivos".</span><span class="sxs-lookup"><span data-stu-id="5d830-175">[**WM\_TOUCH**](wm-touchdown.md) messages are currently "greedy."</span></span> <span data-ttu-id="5d830-176">Una vez recibido el primer mensaje táctil en una ventana, todos los mensajes táctiles se envían a esa ventana hasta que otra ventana recibe el foco.</span><span class="sxs-lookup"><span data-stu-id="5d830-176">After the first touch message is received on a window, all touch messages are sent to that window until another window receives focus.</span></span>

 

> [!Note]  
> <span data-ttu-id="5d830-177">De forma predeterminada, recibe mensajes de [**\_ gestos de WM**](wm-gesture.md) en lugar de mensajes [**\_ táctiles de WM**](wm-touchdown.md) .</span><span class="sxs-lookup"><span data-stu-id="5d830-177">By default, you receive [**WM\_GESTURE**](wm-gesture.md) messages instead of [**WM\_TOUCH**](wm-touchdown.md) messages.</span></span> <span data-ttu-id="5d830-178">Si llama a [**RegisterTouchWindow**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow), dejará de recibir mensajes de **\_ gestos de WM** .</span><span class="sxs-lookup"><span data-stu-id="5d830-178">If you call [**RegisterTouchWindow**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow), you will stop receiving **WM\_GESTURE** messages.</span></span>

 

<span data-ttu-id="5d830-179">En el código siguiente se muestra cómo una aplicación podría registrarse para recibir mensajes de Windows Touch en una aplicación Win32.</span><span class="sxs-lookup"><span data-stu-id="5d830-179">The following code demonstrates how an application could register to receive Windows Touch messages in a Win32 application.</span></span>


```C++
RegisterTouchWindow(hWnd, 0);
```



## <a name="handling-windows-touch-messages"></a><span data-ttu-id="5d830-180">Controlar mensajes de Windows Touch</span><span class="sxs-lookup"><span data-stu-id="5d830-180">Handling Windows Touch Messages</span></span>

<span data-ttu-id="5d830-181">Puede controlar los mensajes táctiles de Windows desde las aplicaciones de los sistemas operativos Windows de muchas maneras.</span><span class="sxs-lookup"><span data-stu-id="5d830-181">You can handle the Windows Touch messages from applications in Windows operating systems in many ways.</span></span> <span data-ttu-id="5d830-182">Si está programando una aplicación de GUI, agregue código dentro de la `WndProc` función para controlar los mensajes de interés.</span><span class="sxs-lookup"><span data-stu-id="5d830-182">If you are programming a GUI application, you add code within the `WndProc` function to handle the messages of interest.</span></span> <span data-ttu-id="5d830-183">Si está programando un Microsoft Foundation Class (MFC) o una aplicación administrada, agregue Controladores para los mensajes de interés.</span><span class="sxs-lookup"><span data-stu-id="5d830-183">If you are programming a Microsoft Foundation Class (MFC) or managed application, you add handlers for the messages of interest.</span></span> <span data-ttu-id="5d830-184">En el ejemplo de código siguiente se muestra cómo se pueden controlar los mensajes Touch desde WndProc en una aplicación basada en Windows.</span><span class="sxs-lookup"><span data-stu-id="5d830-184">The following code example shows how touch messages could be handled from WndProc in a Windows-based application.</span></span>


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





<span data-ttu-id="5d830-185">En el código siguiente se muestra cómo puede implementar el mapa de mensajes y un controlador de mensajes.</span><span class="sxs-lookup"><span data-stu-id="5d830-185">The following code shows how you can implement the message map and a message handler.</span></span> <span data-ttu-id="5d830-186">Tenga en cuenta que los mensajes se deben declarar en el mapa de mensajes y, a continuación, se debe implementar el controlador del mensaje.</span><span class="sxs-lookup"><span data-stu-id="5d830-186">Note that the messages must be declared in the message map and then the handler for the message should be implemented.</span></span> <span data-ttu-id="5d830-187">Por ejemplo, en una aplicación MFC, se podría declarar en el código del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="5d830-187">For example, in an MFC application, this could be declared in the dialog code.</span></span> <span data-ttu-id="5d830-188">Tenga en cuenta también que la `OnInitDialog` función de la ventana de cuadro de diálogo tendría que incluir una llamada a [**RegisterTouchWindow**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow) como `RegisterTouchWindow(m_hWnd, 0)` .</span><span class="sxs-lookup"><span data-stu-id="5d830-188">Note also, that the `OnInitDialog` function for your dialog window would have to include a call to [**RegisterTouchWindow**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow) such as `RegisterTouchWindow(m_hWnd, 0)`.</span></span>


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



<span data-ttu-id="5d830-189">Al tocar la ventana, se indicarán los toques de una ventana emergente.</span><span class="sxs-lookup"><span data-stu-id="5d830-189">Touching the window will indicate touches from a pop-up window.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5d830-190">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5d830-190">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5d830-191">Entrada táctil de Windows</span><span class="sxs-lookup"><span data-stu-id="5d830-191">Windows Touch Input</span></span>](guide-multi-touch-input.md)
</dt> </dl>

 

 