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
# <a name="wm_gesture-message"></a><span data-ttu-id="35e13-104">Mensaje de gesto de WM \_</span><span class="sxs-lookup"><span data-stu-id="35e13-104">WM\_GESTURE message</span></span>

<span data-ttu-id="35e13-105">Pasa información sobre un gesto.</span><span class="sxs-lookup"><span data-stu-id="35e13-105">Passes information about a gesture.</span></span>

## <a name="parameters"></a><span data-ttu-id="35e13-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="35e13-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="35e13-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="35e13-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="35e13-108">Proporciona información que identifica el comando de gestos y los valores de argumento específicos de gestos.</span><span class="sxs-lookup"><span data-stu-id="35e13-108">Provides information identifying the gesture command and gesture-specific argument values.</span></span> <span data-ttu-id="35e13-109">Esta información es la misma que se pasa en el miembro **ullArguments** de la estructura [**GESTUREINFO**](/windows/win32/api/winuser/ns-winuser-gestureinfo) .</span><span class="sxs-lookup"><span data-stu-id="35e13-109">This information is the same information passed in the **ullArguments** member of the [**GESTUREINFO**](/windows/win32/api/winuser/ns-winuser-gestureinfo) structure.</span></span>

</dd> <dt>

<span data-ttu-id="35e13-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="35e13-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="35e13-111">Proporciona un identificador para la información que identifica el comando de gesto y los valores de argumento específicos de gestos.</span><span class="sxs-lookup"><span data-stu-id="35e13-111">Provides a handle to information identifying the gesture command and gesture-specific argument values.</span></span> <span data-ttu-id="35e13-112">Esta información se recupera llamando a [**GetGestureInfo**](/windows/desktop/api/winuser/nf-winuser-getgestureinfo).</span><span class="sxs-lookup"><span data-stu-id="35e13-112">This information is retrieved by calling [**GetGestureInfo**](/windows/desktop/api/winuser/nf-winuser-getgestureinfo).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="35e13-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="35e13-113">Return value</span></span>

<span data-ttu-id="35e13-114">Si una aplicación procesa este mensaje, debe devolver 0.</span><span class="sxs-lookup"><span data-stu-id="35e13-114">If an application processes this message, it should return 0.</span></span>

<span data-ttu-id="35e13-115">Si la aplicación no procesa el mensaje, debe llamar a [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span><span class="sxs-lookup"><span data-stu-id="35e13-115">If the application does not process the message, it must call [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span></span> <span data-ttu-id="35e13-116">Si no lo hace, la aplicación perderá memoria porque no se cerrará el identificador de entrada táctil y no se liberará la memoria de proceso asociada.</span><span class="sxs-lookup"><span data-stu-id="35e13-116">Not doing so will cause the application to leak memory because the touch input handle will not be closed and associated process memory will not be freed.</span></span>

## <a name="remarks"></a><span data-ttu-id="35e13-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="35e13-117">Remarks</span></span>

<span data-ttu-id="35e13-118">En la tabla siguiente se enumeran los comandos de gestos compatibles.</span><span class="sxs-lookup"><span data-stu-id="35e13-118">The following table lists the supported gesture commands.</span></span>



| <span data-ttu-id="35e13-119">IDENTIFICADOR de gesto</span><span class="sxs-lookup"><span data-stu-id="35e13-119">Gesture ID</span></span>            | <span data-ttu-id="35e13-120">Valor (*dwID*)</span><span class="sxs-lookup"><span data-stu-id="35e13-120">Value (*dwID*)</span></span> | <span data-ttu-id="35e13-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="35e13-121">Description</span></span>                                                                                                                                                                                                                                                                          |
|-----------------------|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="35e13-122">**Inicio de GID \_**</span><span class="sxs-lookup"><span data-stu-id="35e13-122">**GID\_BEGIN**</span></span>        | <span data-ttu-id="35e13-123">1</span><span class="sxs-lookup"><span data-stu-id="35e13-123">1</span></span>              | <span data-ttu-id="35e13-124">Indica que se está iniciando un gesto genérico.</span><span class="sxs-lookup"><span data-stu-id="35e13-124">Indicates a generic gesture is beginning.</span></span>                                                                                                                                                                                                                                            |
| <span data-ttu-id="35e13-125">**fin de GID \_**</span><span class="sxs-lookup"><span data-stu-id="35e13-125">**GID\_END**</span></span>          | <span data-ttu-id="35e13-126">2</span><span class="sxs-lookup"><span data-stu-id="35e13-126">2</span></span>              | <span data-ttu-id="35e13-127">Indica un fin de movimiento genérico.</span><span class="sxs-lookup"><span data-stu-id="35e13-127">Indicates a generic gesture end.</span></span>                                                                                                                                                                                                                                                     |
| <span data-ttu-id="35e13-128">**ZOOM de GID \_**</span><span class="sxs-lookup"><span data-stu-id="35e13-128">**GID\_ZOOM**</span></span>         | <span data-ttu-id="35e13-129">3</span><span class="sxs-lookup"><span data-stu-id="35e13-129">3</span></span>              | <span data-ttu-id="35e13-130">Indica inicio de zoom, movimiento de zoom o detención de zoom.</span><span class="sxs-lookup"><span data-stu-id="35e13-130">Indicates zoom start, zoom move, or zoom stop.</span></span> <span data-ttu-id="35e13-131">El primer mensaje del comando **\_ zoom de Gid** comienza un zoom pero no produce ningún zoom.</span><span class="sxs-lookup"><span data-stu-id="35e13-131">The first **GID\_ZOOM** command message begins a zoom but does not cause any zooming.</span></span> <span data-ttu-id="35e13-132">El segundo **comando \_ zoom de Gid** desencadena un zoom relativo al estado contenido en el primer **\_ zoom de Gid**.</span><span class="sxs-lookup"><span data-stu-id="35e13-132">The second **GID\_ZOOM** command triggers a zoom relative to the state contained in the first **GID\_ZOOM**.</span></span>                                    |
| <span data-ttu-id="35e13-133">**PAN de GID \_**</span><span class="sxs-lookup"><span data-stu-id="35e13-133">**GID\_PAN**</span></span>          | <span data-ttu-id="35e13-134">4</span><span class="sxs-lookup"><span data-stu-id="35e13-134">4</span></span>              | <span data-ttu-id="35e13-135">Indica movimiento de la panorámica o inicio de la panorámica.</span><span class="sxs-lookup"><span data-stu-id="35e13-135">Indicates pan move or pan start.</span></span> <span data-ttu-id="35e13-136">El primer comando de **\_ pan de Gid** indica un inicio de pan pero no realiza ningún movimiento panorámico.</span><span class="sxs-lookup"><span data-stu-id="35e13-136">The first **GID\_PAN** command indicates a pan start but does not perform any panning.</span></span> <span data-ttu-id="35e13-137">Con el segundo mensaje de comando **\_ pan de Gid** , la aplicación iniciará el movimiento panorámico.</span><span class="sxs-lookup"><span data-stu-id="35e13-137">With the second **GID\_PAN** command message, the application will begin panning.</span></span>                                                                            |
| <span data-ttu-id="35e13-138">**GID- \_ girar**</span><span class="sxs-lookup"><span data-stu-id="35e13-138">**GID\_ROTATE**</span></span>       | <span data-ttu-id="35e13-139">5</span><span class="sxs-lookup"><span data-stu-id="35e13-139">5</span></span>              | <span data-ttu-id="35e13-140">Indica el cambio de giro o el inicio de giro.</span><span class="sxs-lookup"><span data-stu-id="35e13-140">Indicates rotate move or rotate start.</span></span> <span data-ttu-id="35e13-141">El primer mensaje de comando de **\_ girar GID** indica un movimiento de giro o un inicio de giro, pero no gira.</span><span class="sxs-lookup"><span data-stu-id="35e13-141">The first **GID\_ROTATE** command message indicates a rotate move or rotate start but will not rotate.</span></span> <span data-ttu-id="35e13-142">El segundo mensaje de comando de **\_ girar GID** desencadenará una operación de rotación en relación con el estado contenido en el primer **GID \_**.</span><span class="sxs-lookup"><span data-stu-id="35e13-142">The second **GID\_ROTATE** command message will trigger a rotation operation relative to state contained in the first **GID\_ROTATE**.</span></span> |
| <span data-ttu-id="35e13-143">**GID \_ TWOFINGERTAP**</span><span class="sxs-lookup"><span data-stu-id="35e13-143">**GID\_TWOFINGERTAP**</span></span> | <span data-ttu-id="35e13-144">6</span><span class="sxs-lookup"><span data-stu-id="35e13-144">6</span></span>              | <span data-ttu-id="35e13-145">Indica el gesto de puntear dos dedos.</span><span class="sxs-lookup"><span data-stu-id="35e13-145">Indicates two-finger tap gesture.</span></span>                                                                                                                                                                                                                                                    |
| <span data-ttu-id="35e13-146">**GID \_ PRESSANDTAP**</span><span class="sxs-lookup"><span data-stu-id="35e13-146">**GID\_PRESSANDTAP**</span></span>  | <span data-ttu-id="35e13-147">7</span><span class="sxs-lookup"><span data-stu-id="35e13-147">7</span></span>              | <span data-ttu-id="35e13-148">Indica el gesto de presionar y tocar.</span><span class="sxs-lookup"><span data-stu-id="35e13-148">Indicates the press and tap gesture.</span></span>                                                                                                                                                                                                                                                 |



 

> [!Note]  
> <span data-ttu-id="35e13-149">Para habilitar la compatibilidad heredada, se deben reenviar los mensajes con los comandos de gestos de **\_ Inicio** y de **\_ fin** de Gid con [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span><span class="sxs-lookup"><span data-stu-id="35e13-149">In order to enable legacy support, messages with the **GID\_BEGIN** and **GID\_END** gesture commands need to be forwarded using [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span></span>

 

<span data-ttu-id="35e13-150">En la tabla siguiente se indican los argumentos de gestos pasados en los parámetros *lParam* y *wParam* .</span><span class="sxs-lookup"><span data-stu-id="35e13-150">The following table indicates the gesture arguments passed in the *lParam* and *wParam* parameters.</span></span>



| <span data-ttu-id="35e13-151">IDENTIFICADOR de gesto</span><span class="sxs-lookup"><span data-stu-id="35e13-151">Gesture ID</span></span>            | <span data-ttu-id="35e13-152">Gesto</span><span class="sxs-lookup"><span data-stu-id="35e13-152">Gesture</span></span>        | <span data-ttu-id="35e13-153">*ullArgument*</span><span class="sxs-lookup"><span data-stu-id="35e13-153">*ullArgument*</span></span>                                                                                                                                                                                                                                                                                                                                                                                            | <span data-ttu-id="35e13-154">*ptsLocation* en la estructura [**GestureInfo**](/windows/desktop/api/winuser/nf-winuser-getgestureinfo)</span><span class="sxs-lookup"><span data-stu-id="35e13-154">*ptsLocation* in [**GestureInfo**](/windows/desktop/api/winuser/nf-winuser-getgestureinfo) structure</span></span>                                                  |
|-----------------------|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="35e13-155">**ZOOM de GID \_**</span><span class="sxs-lookup"><span data-stu-id="35e13-155">**GID\_ZOOM**</span></span>         | <span data-ttu-id="35e13-156">Acercar/alejar</span><span class="sxs-lookup"><span data-stu-id="35e13-156">Zoom In/Out</span></span>    | <span data-ttu-id="35e13-157">Indica la distancia entre los dos puntos.</span><span class="sxs-lookup"><span data-stu-id="35e13-157">Indicates the distance between the two points.</span></span>                                                                                                                                                                                                                                                                                                                                                           | <span data-ttu-id="35e13-158">Indica el centro del zoom.</span><span class="sxs-lookup"><span data-stu-id="35e13-158">Indicates the center of the zoom.</span></span>                                                                                 |
| <span data-ttu-id="35e13-159">**PAN de GID \_**</span><span class="sxs-lookup"><span data-stu-id="35e13-159">**GID\_PAN**</span></span>          | <span data-ttu-id="35e13-160">Movimiento panorámico</span><span class="sxs-lookup"><span data-stu-id="35e13-160">Pan</span></span>            | <span data-ttu-id="35e13-161">Indica la distancia entre los dos puntos.</span><span class="sxs-lookup"><span data-stu-id="35e13-161">Indicates the distance between the two points.</span></span>                                                                                                                                                                                                                                                                                                                                                           | <span data-ttu-id="35e13-162">Indica la posición actual de la panorámica.</span><span class="sxs-lookup"><span data-stu-id="35e13-162">Indicates the current position of the pan.</span></span>                                                                        |
| <span data-ttu-id="35e13-163">**GID- \_ girar**</span><span class="sxs-lookup"><span data-stu-id="35e13-163">**GID\_ROTATE**</span></span>       | <span data-ttu-id="35e13-164">Girar (dinamizar)</span><span class="sxs-lookup"><span data-stu-id="35e13-164">Rotate (pivot)</span></span> | <span data-ttu-id="35e13-165">Indica el ángulo de rotación si se establece la marca de **\_ Inicio GF** .</span><span class="sxs-lookup"><span data-stu-id="35e13-165">Indicates the angle of rotation if the **GF\_BEGIN** flag is set.</span></span> <span data-ttu-id="35e13-166">De lo contrario, este es el cambio de ángulo desde que se ha iniciado la rotación.</span><span class="sxs-lookup"><span data-stu-id="35e13-166">Otherwise, this is the angle change since the rotation has started.</span></span> <span data-ttu-id="35e13-167">Está firmado para indicar la dirección de la rotación.</span><span class="sxs-lookup"><span data-stu-id="35e13-167">This is signed to indicate the direction of the rotation.</span></span> <span data-ttu-id="35e13-168">Use el [**\_ \_ ángulo de rotación \_ de Gid desde el \_ argumento**](/windows/desktop/api/winuser/nf-winuser-gid_rotate_angle_from_argument) y el ángulo de rotación de Gid a las macros de [**\_ \_ \_ \_ argumento**](/windows/desktop/api/winuser/nf-winuser-gid_rotate_angle_to_argument) para obtener y establecer el valor del ángulo.</span><span class="sxs-lookup"><span data-stu-id="35e13-168">Use the [**GID\_ROTATE\_ANGLE\_FROM\_ARGUMENT**](/windows/desktop/api/winuser/nf-winuser-gid_rotate_angle_from_argument) and [**GID\_ROTATE\_ANGLE\_TO\_ARGUMENT**](/windows/desktop/api/winuser/nf-winuser-gid_rotate_angle_to_argument) macros to get and set the angle value.</span></span> | <span data-ttu-id="35e13-169">Indica el centro del giro, que es el punto estacionario en el que se gira el objeto de destino.</span><span class="sxs-lookup"><span data-stu-id="35e13-169">This indicates the center of the rotation which is the stationary point that the target object is rotated around.</span></span> |
| <span data-ttu-id="35e13-170">**GID \_ TWOFINGERTAP**</span><span class="sxs-lookup"><span data-stu-id="35e13-170">**GID\_TWOFINGERTAP**</span></span> | <span data-ttu-id="35e13-171">Tap con dos dedos</span><span class="sxs-lookup"><span data-stu-id="35e13-171">Two-finger Tap</span></span> | <span data-ttu-id="35e13-172">Indica la distancia entre los dos dedos.</span><span class="sxs-lookup"><span data-stu-id="35e13-172">Indicates the distance between the two fingers.</span></span>                                                                                                                                                                                                                                                                                                                                                          | <span data-ttu-id="35e13-173">Indica el centro de los dos dedos.</span><span class="sxs-lookup"><span data-stu-id="35e13-173">Indicates the center of the two fingers.</span></span>                                                                          |
| <span data-ttu-id="35e13-174">**GID \_ PRESSANDTAP**</span><span class="sxs-lookup"><span data-stu-id="35e13-174">**GID\_PRESSANDTAP**</span></span>  | <span data-ttu-id="35e13-175">Pulse y haga clic en</span><span class="sxs-lookup"><span data-stu-id="35e13-175">Press and Tap</span></span>  | <span data-ttu-id="35e13-176">Indica la diferencia entre el primer dedo y el segundo dedo.</span><span class="sxs-lookup"><span data-stu-id="35e13-176">Indicates the delta between the first finger and the second finger.</span></span> <span data-ttu-id="35e13-177">Este valor se almacena en los 32 bits inferiores de *ullArgument* en una estructura **Point** .</span><span class="sxs-lookup"><span data-stu-id="35e13-177">This value is stored in the lower 32 bits of the *ullArgument* in a **POINT** structure.</span></span>                                                                                                                                                                                                                                             | <span data-ttu-id="35e13-178">Indica la posición en la que se activa el primer dedo.</span><span class="sxs-lookup"><span data-stu-id="35e13-178">Indicates the position that the first finger comes down on.</span></span>                                                       |



 

> [!Note]  
> <span data-ttu-id="35e13-179">Todas las distancias y posiciones se proporcionan en coordenadas de pantalla físicas.</span><span class="sxs-lookup"><span data-stu-id="35e13-179">All distances and positions are provided in physical screen coordinates.</span></span>

 

> [!Note]  
> <span data-ttu-id="35e13-180">Los parámetros *dwID* y *ullArgument* solo se deben considerar para acompañar a los \_ \* comandos GID y las aplicaciones no deben modificarlos.</span><span class="sxs-lookup"><span data-stu-id="35e13-180">The *dwID* and *ullArgument* parameters should only be considered to be accompanying the GID\_\* commands and should not be altered by applications.</span></span>

 

## <a name="examples"></a><span data-ttu-id="35e13-181">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="35e13-181">Examples</span></span>

<span data-ttu-id="35e13-182">En el código siguiente se muestra cómo obtener información específica del gesto asociada a este mensaje.</span><span class="sxs-lookup"><span data-stu-id="35e13-182">The following code illustrates how to obtain gesture-specific information associated with this message.</span></span>

> [!Note]  
> <span data-ttu-id="35e13-183">Siempre debe reenviar los mensajes no controlados a [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca) y debe cerrar el identificador de entrada de gestos para los mensajes que administra con una llamada a [**CloseGestureInfoHandle**](/windows/desktop/api/winuser/nf-winuser-closegestureinfohandle).</span><span class="sxs-lookup"><span data-stu-id="35e13-183">You should always forward unhandled messages to [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca) and should close the gesture input handle for messages that you do handle with a call to [**CloseGestureInfoHandle**](/windows/desktop/api/winuser/nf-winuser-closegestureinfohandle).</span></span> <span data-ttu-id="35e13-184">En este ejemplo, el comportamiento predeterminado del controlador de gestos se suprimirá porque el identificador TOUCHINPUT se cierra en cada uno de los casos de gestos.</span><span class="sxs-lookup"><span data-stu-id="35e13-184">In this example, the default gesture handler behavior will be suppressed because the TOUCHINPUT handle is closed in each of the gesture cases.</span></span> <span data-ttu-id="35e13-185">Si quitó los casos en el código anterior para mensajes no controlados, el controlador de gestos predeterminado procesaría los mensajes enviándose a [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca) en el caso predeterminado.</span><span class="sxs-lookup"><span data-stu-id="35e13-185">If you removed the cases in the above code for unhandled messages, the default gesture handler would process the messages by getting forwarded to [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca) in the default case.</span></span>

 


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



## <a name="requirements"></a><span data-ttu-id="35e13-186">Requisitos</span><span class="sxs-lookup"><span data-stu-id="35e13-186">Requirements</span></span>



| <span data-ttu-id="35e13-187">Requisito</span><span class="sxs-lookup"><span data-stu-id="35e13-187">Requirement</span></span> | <span data-ttu-id="35e13-188">Value</span><span class="sxs-lookup"><span data-stu-id="35e13-188">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="35e13-189">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="35e13-189">Minimum supported client</span></span><br/> | <span data-ttu-id="35e13-190">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="35e13-190">Windows 7 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="35e13-191">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="35e13-191">Minimum supported server</span></span><br/> | <span data-ttu-id="35e13-192">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="35e13-192">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                  |
| <span data-ttu-id="35e13-193">Encabezado</span><span class="sxs-lookup"><span data-stu-id="35e13-193">Header</span></span><br/>                   | <dl> <span data-ttu-id="35e13-194"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="35e13-194"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="35e13-195">Vea también</span><span class="sxs-lookup"><span data-stu-id="35e13-195">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35e13-196">Notificaciones</span><span class="sxs-lookup"><span data-stu-id="35e13-196">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="35e13-197">Guía de programación de gestos táctiles de Windows</span><span class="sxs-lookup"><span data-stu-id="35e13-197">Windows Touch Gestures Programming Guide</span></span>](guide-multi-touch-gestures.md)
</dt> </dl>

 

