---
title: IMsRdpClient RequestClose, método
description: Solicita un cierre estable del control ActiveX Escritorio remoto.
ms.assetid: 0b930a00-f134-4da2-a752-8fd131a22043
ms.tgt_platform: multiple
keywords:
- Método RequestClose Servicios de Escritorio remoto
- Método RequestClose Servicios de Escritorio remoto, interfaz IMsRdpClient
- Interfaz IMsRdpClient Servicios de Escritorio remoto, método RequestClose
- Método RequestClose Servicios de Escritorio remoto, interfaz IMsRdpClient2
- Interfaz IMsRdpClient2 Servicios de Escritorio remoto, método RequestClose
- Método RequestClose Servicios de Escritorio remoto, interfaz IMsRdpClient3
- Interfaz IMsRdpClient3 Servicios de Escritorio remoto, método RequestClose
- Método RequestClose Servicios de Escritorio remoto, interfaz IMsRdpClient4
- Interfaz IMsRdpClient4 Servicios de Escritorio remoto, método RequestClose
- Método RequestClose Servicios de Escritorio remoto, interfaz IMsRdpClient5
- Interfaz IMsRdpClient5 Servicios de Escritorio remoto, método RequestClose
- Método RequestClose Servicios de Escritorio remoto, interfaz IMsRdpClient6
- Interfaz IMsRdpClient6 Servicios de Escritorio remoto, método RequestClose
- Método RequestClose Servicios de Escritorio remoto, interfaz IMsRdpClient7
- Interfaz IMsRdpClient7 Servicios de Escritorio remoto, método RequestClose
- Método RequestClose Servicios de Escritorio remoto, interfaz IMsRdpClient8
- Interfaz IMsRdpClient8 Servicios de Escritorio remoto, método RequestClose
- Método RequestClose Servicios de Escritorio remoto, interfaz IMsRdpClient9
- Interfaz IMsRdpClient9 Servicios de Escritorio remoto, método RequestClose
- Método RequestClose Servicios de Escritorio remoto, interfaz IMsRdpClient10
- Interfaz IMsRdpClient10 Servicios de Escritorio remoto, método RequestClose
topic_type:
- apiref
api_name:
- IMsRdpClient.RequestClose
- IMsRdpClient2.RequestClose
- IMsRdpClient3.RequestClose
- IMsRdpClient4.RequestClose
- IMsRdpClient5.RequestClose
- IMsRdpClient6.RequestClose
- IMsRdpClient7.RequestClose
- IMsRdpClient8.RequestClose
- IMsRdpClient9.RequestClose
- IMsRdpClient10.RequestClose
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1679b08680b962cdbff57e9bbbd1c392607d8709
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801580"
---
# <a name="imsrdpclientrequestclose-method"></a><span data-ttu-id="5c03e-124">IMsRdpClient:: RequestClose (método)</span><span class="sxs-lookup"><span data-stu-id="5c03e-124">IMsRdpClient::RequestClose method</span></span>

<span data-ttu-id="5c03e-125">Solicita un cierre estable del control ActiveX Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="5c03e-125">Requests a graceful shutdown of the Remote Desktop ActiveX control.</span></span> <span data-ttu-id="5c03e-126">Un cierre estable puede incluir la finalización de la sesión de Servicios de Escritorio remoto del usuario, pero no apaga el servidor host de sesión Escritorio remoto (host de sesión de escritorio remoto).</span><span class="sxs-lookup"><span data-stu-id="5c03e-126">A graceful shutdown can include ending the user's Remote Desktop Services session but it does not shut down the Remote Desktop Session Host (RD Session Host) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c03e-127">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5c03e-127">Syntax</span></span>


```C++
HRESULT RequestClose(
  [out] ControlCloseStatus *pCloseStatus
);
```



## <a name="parameters"></a><span data-ttu-id="5c03e-128">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5c03e-128">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5c03e-129">*pCloseStatus* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="5c03e-129">*pCloseStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5c03e-130">Valor de la enumeración [**ControlCloseStatus**](controlclosestatus.md) que indica si la aplicación puede cerrar el control inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="5c03e-130">Value from the [**ControlCloseStatus**](controlclosestatus.md) enumeration that indicates whether the application can close the control immediately.</span></span> <span data-ttu-id="5c03e-131">A continuación se muestra una lista de los valores posibles.</span><span class="sxs-lookup"><span data-stu-id="5c03e-131">Following is a list of possible values.</span></span>

<dt>

<span id="controlCloseCanProceed"></span><span id="controlclosecanproceed"></span><span id="CONTROLCLOSECANPROCEED"></span>

<span data-ttu-id="5c03e-132"><span id="controlCloseCanProceed"></span><span id="controlclosecanproceed"></span><span id="CONTROLCLOSECANPROCEED"></span>**controlCloseCanProceed** (0x0000)</span><span class="sxs-lookup"><span data-stu-id="5c03e-132"><span id="controlCloseCanProceed"></span><span id="controlclosecanproceed"></span><span id="CONTROLCLOSECANPROCEED"></span>**controlCloseCanProceed** (0x0000)</span></span>


</dt> <dd>

<span data-ttu-id="5c03e-133">La aplicación contenedora puede continuar para cerrar el control inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="5c03e-133">The container application can proceed to close the control immediately.</span></span> <span data-ttu-id="5c03e-134">Este valor también puede indicar que la conexión ya ha finalizado.</span><span class="sxs-lookup"><span data-stu-id="5c03e-134">This value can also indicate that the connection has already terminated.</span></span>

</dd> <dt>

<span id="controlCloseWaitForEvents"></span><span id="controlclosewaitforevents"></span><span id="CONTROLCLOSEWAITFOREVENTS"></span>

<span data-ttu-id="5c03e-135"><span id="controlCloseWaitForEvents"></span><span id="controlclosewaitforevents"></span><span id="CONTROLCLOSEWAITFOREVENTS"></span>**controlCloseWaitForEvents** (0x0001)</span><span class="sxs-lookup"><span data-stu-id="5c03e-135"><span id="controlCloseWaitForEvents"></span><span id="controlclosewaitforevents"></span><span id="CONTROLCLOSEWAITFOREVENTS"></span>**controlCloseWaitForEvents** (0x0001)</span></span>


</dt> <dd>

<span data-ttu-id="5c03e-136">La aplicación contenedora no debe cerrar el control inmediatamente; la aplicación debe esperar a que se produzca uno de los eventos descritos en la siguiente sección de comentarios antes de cerrar.</span><span class="sxs-lookup"><span data-stu-id="5c03e-136">The container application should not close the control immediately; the application should wait for one of the events described in the following Remarks section to occur before closing.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5c03e-137">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5c03e-137">Return value</span></span>

<span data-ttu-id="5c03e-138">Vuelva **a \_ Aceptar si es** correcto.</span><span class="sxs-lookup"><span data-stu-id="5c03e-138">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="5c03e-139">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5c03e-139">Remarks</span></span>

<span data-ttu-id="5c03e-140">Si el parámetro *pCloseStatus* es igual a **controlCloseWaitForEvents**, la aplicación debe esperar a que se produzca uno de los siguientes eventos antes de que la aplicación cierre el control:</span><span class="sxs-lookup"><span data-stu-id="5c03e-140">If the *pCloseStatus* parameter is equal to **controlCloseWaitForEvents**, the application should wait for one of the following events to occur before the application closes the control:</span></span>

-   <span data-ttu-id="5c03e-141">[**IMsTscAxEvents:: OnDisconnection**](imstscaxevents-ondisconnected.md).</span><span class="sxs-lookup"><span data-stu-id="5c03e-141">[**IMsTscAxEvents::OnDisconnected**](imstscaxevents-ondisconnected.md).</span></span> <span data-ttu-id="5c03e-142">Si el usuario no ha iniciado sesión en la sesión de Servicios de Escritorio remoto, la aplicación puede llamar a la función [**DestroyWindow**](/windows/desktop/api/winuser/nf-winuser-destroywindow) para destruir todas las ventanas y, a continuación, cerrar el control.</span><span class="sxs-lookup"><span data-stu-id="5c03e-142">If the user is not logged on to the Remote Desktop Services session, the application can call the [**DestroyWindow**](/windows/desktop/api/winuser/nf-winuser-destroywindow) function to destroy all windows and then close the control.</span></span>
-   <span data-ttu-id="5c03e-143">[**IMsTscAxEvents:: OnConfirmClose**](imstscaxevents-onconfirmclose.md).</span><span class="sxs-lookup"><span data-stu-id="5c03e-143">[**IMsTscAxEvents::OnConfirmClose**](imstscaxevents-onconfirmclose.md).</span></span> <span data-ttu-id="5c03e-144">Si el usuario ha iniciado sesión en la sesión de Servicios de Escritorio remoto, el control activa un evento **OnConfirmClose** .</span><span class="sxs-lookup"><span data-stu-id="5c03e-144">If the user is logged on to the Remote Desktop Services session, the control fires an **OnConfirmClose** event.</span></span> <span data-ttu-id="5c03e-145">Este evento permite a la aplicación preguntar al usuario si desea cerrar la conexión.</span><span class="sxs-lookup"><span data-stu-id="5c03e-145">This event allows the application to prompt the user about whether to close the connection.</span></span> <span data-ttu-id="5c03e-146">Si el usuario responde afirmativamente al mensaje, la aplicación contenedora puede llamar a [**DestroyWindow**](/windows/desktop/api/winuser/nf-winuser-destroywindow) para destruir todas las ventanas y cerrar el control.</span><span class="sxs-lookup"><span data-stu-id="5c03e-146">If the user replies yes to the prompt, the container application can call [**DestroyWindow**](/windows/desktop/api/winuser/nf-winuser-destroywindow) to destroy all windows, and close the control.</span></span>

<span data-ttu-id="5c03e-147">**RequestClose** permite a una aplicación contenedora preguntar al usuario si desea cerrar una conexión.</span><span class="sxs-lookup"><span data-stu-id="5c03e-147">**RequestClose** allows a container application to prompt the user about whether to close a connection.</span></span> <span data-ttu-id="5c03e-148">Para obtener más información, vea [**IMsTscAxEvents:: OnConfirmClose**](imstscaxevents-onconfirmclose.md).</span><span class="sxs-lookup"><span data-stu-id="5c03e-148">For more information, see [**IMsTscAxEvents::OnConfirmClose**](imstscaxevents-onconfirmclose.md).</span></span>

<span data-ttu-id="5c03e-149">Para obtener más información acerca de Conexión web a Escritorio remoto, consulte [Requirements for conexión web a escritorio remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="5c03e-149">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5c03e-150">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5c03e-150">Requirements</span></span>



| <span data-ttu-id="5c03e-151">Requisito</span><span class="sxs-lookup"><span data-stu-id="5c03e-151">Requirement</span></span> | <span data-ttu-id="5c03e-152">Value</span><span class="sxs-lookup"><span data-stu-id="5c03e-152">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5c03e-153">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5c03e-153">Minimum supported client</span></span><br/> | <span data-ttu-id="5c03e-154">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5c03e-154">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="5c03e-155">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5c03e-155">Minimum supported server</span></span><br/> | <span data-ttu-id="5c03e-156">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5c03e-156">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="5c03e-157">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="5c03e-157">Type library</span></span><br/>             | <dl> <span data-ttu-id="5c03e-158"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5c03e-158"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="5c03e-159">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="5c03e-159">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5c03e-160"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5c03e-160"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="5c03e-161">IID</span><span class="sxs-lookup"><span data-stu-id="5c03e-161">IID</span></span><br/>                      | <span data-ttu-id="5c03e-162">IID \_ IMsRdpClient se define como 92b4a539-7115-4b7c-a5a9-e5d9efc2780a</span><span class="sxs-lookup"><span data-stu-id="5c03e-162">IID\_IMsRdpClient is defined as 92b4a539-7115-4b7c-a5a9-e5d9efc2780a</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="5c03e-163">Vea también</span><span class="sxs-lookup"><span data-stu-id="5c03e-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c03e-164">**IMsRdpClient**</span><span class="sxs-lookup"><span data-stu-id="5c03e-164">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="5c03e-165">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="5c03e-165">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="5c03e-166">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="5c03e-166">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="5c03e-167">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="5c03e-167">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="5c03e-168">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="5c03e-168">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="5c03e-169">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="5c03e-169">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="5c03e-170">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="5c03e-170">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="5c03e-171">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="5c03e-171">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="5c03e-172">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="5c03e-172">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="5c03e-173">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="5c03e-173">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> <dt>

[<span data-ttu-id="5c03e-174">**IMsTscAxEvents::OnConfirmClose**</span><span class="sxs-lookup"><span data-stu-id="5c03e-174">**IMsTscAxEvents::OnConfirmClose**</span></span>](imstscaxevents-onconfirmclose.md)
</dt> <dt>

[<span data-ttu-id="5c03e-175">**IMsTscAxEvents:: OnDisconnection**</span><span class="sxs-lookup"><span data-stu-id="5c03e-175">**IMsTscAxEvents::OnDisconnected**</span></span>](imstscaxevents-ondisconnected.md)
</dt> </dl>

 

