---
description: El método Connect conecta el NPP a la red mediante una NIC especificada y proporciona información de configuración para la conexión.
ms.assetid: d017c2a3-a832-4084-b21b-0cca428c5360
title: 'IRTC:: Connect (método) (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRTC.Connect
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: a14e34aeb0be30165aa18ddc7da18028d715be01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677348"
---
# <a name="irtcconnect-method"></a><span data-ttu-id="da965-103">IRTC:: Connect (método)</span><span class="sxs-lookup"><span data-stu-id="da965-103">IRTC::Connect method</span></span>

<span data-ttu-id="da965-104">El método **Connect** conecta el NPP a la red mediante una NIC especificada y proporciona información de configuración para la conexión.</span><span class="sxs-lookup"><span data-stu-id="da965-104">The **Connect** method connects the NPP to the network by using a specified NIC and provides configuration information for the connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="da965-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="da965-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Connect(
  [in]  HBLOB  hInputBlob,
  [in]  LPVOID StatusCallbackProc,
  [in]  LPVOID FramesCallbackProc,
  [in]  LPVOID UserContext,
  [out] HBLOB  hErrorBlob
);
```



## <a name="parameters"></a><span data-ttu-id="da965-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="da965-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="da965-107">*hInputBlob* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="da965-107">*hInputBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da965-108">Identificador del BLOB que especifica la NIC a la que se está conectando y la información de configuración para esa conexión.</span><span class="sxs-lookup"><span data-stu-id="da965-108">Handle to the BLOB that specifies the NIC that you are connecting to and the configuration information for that connection.</span></span>

</dd> <dt>

<span data-ttu-id="da965-109">*StatusCallbackProc* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="da965-109">*StatusCallbackProc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da965-110">Dirección de la función de devolución de llamada de estado del usuario, que recibe actualizaciones de estado, como los desencadenadores.</span><span class="sxs-lookup"><span data-stu-id="da965-110">Address of the user's status callback function, which receives status updates such as triggers.</span></span> <span data-ttu-id="da965-111">Este parámetro se puede establecer en **null**.</span><span class="sxs-lookup"><span data-stu-id="da965-111">This parameter can be set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="da965-112">*FramesCallbackProc* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="da965-112">*FramesCallbackProc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da965-113">Dirección de la función de devolución de llamada de fotograma del usuario, que se usa para recibir actualizaciones de estado como los desencadenadores.</span><span class="sxs-lookup"><span data-stu-id="da965-113">Address of the user's frame callback function, which is used to receive status updates such as triggers.</span></span> <span data-ttu-id="da965-114">Este parámetro se puede establecer en **null**.</span><span class="sxs-lookup"><span data-stu-id="da965-114">This parameter can be set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="da965-115">*UserContext* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="da965-115">*UserContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da965-116">Valor que se pasa cuando se llama a la función de devolución de llamada del marco y el estado del usuario.</span><span class="sxs-lookup"><span data-stu-id="da965-116">Value passed when the user's status and frame callback function is called.</span></span> <span data-ttu-id="da965-117">Si se especifican ambas funciones de devolución de llamada, deben usar el mismo valor de contexto de usuario.</span><span class="sxs-lookup"><span data-stu-id="da965-117">If both callback functions are specified, they must use the same user-context value.</span></span> <span data-ttu-id="da965-118">El valor de este parámetro suele ser HWND o un puntero ' this '.</span><span class="sxs-lookup"><span data-stu-id="da965-118">The value of this parameter is typically either HWND or a 'this' pointer.</span></span>

</dd> <dt>

<span data-ttu-id="da965-119">*hErrorBlob* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="da965-119">*hErrorBlob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="da965-120">Identificador de un BLOB de error que contiene información de error adicional.</span><span class="sxs-lookup"><span data-stu-id="da965-120">Handle to an error BLOB that contains additional error information.</span></span> <span data-ttu-id="da965-121">Vea la sección Comentarios en la parte inferior de este tema para obtener información sobre lo que hay en el BLOB de error.</span><span class="sxs-lookup"><span data-stu-id="da965-121">See Remarks at the bottom of this topic for information about what is in the error BLOB.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="da965-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="da965-122">Return value</span></span>

<span data-ttu-id="da965-123">Si este método se realiza correctamente, el valor devuelto es NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="da965-123">If this method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="da965-124">Si el método no se realiza correctamente, el valor devuelto es uno de los siguientes códigos de error (que incluyen los errores devueltos por la llamada interna **IRTC:: configure** ):</span><span class="sxs-lookup"><span data-stu-id="da965-124">If the method is unsuccessful, the return value is one of the following error codes (which include those errors returned by the internal **IRTC::Configure** call):</span></span>



| <span data-ttu-id="da965-125">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="da965-125">Return code</span></span>                                                                                                         | <span data-ttu-id="da965-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="da965-126">Description</span></span>                                                                                                                                                                                                                                                                                  |
|---------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="da965-127"><dt>**NMERR \_ ya \_ conectado**</dt></span><span class="sxs-lookup"><span data-stu-id="da965-127"><dt>**NMERR\_ALREADY\_CONNECTED**</dt></span></span> </dl>            | <span data-ttu-id="da965-128">Esta instancia del objeto COM NPP ya está conectada a la red.</span><span class="sxs-lookup"><span data-stu-id="da965-128">This instance of the NPP COM object is already connected to the network.</span></span><br/>                                                                                                                                                                                                          |
| <dl> <span data-ttu-id="da965-129"><dt>**\_error de \_ conversión de BLOB NMERR \_**</dt></span><span class="sxs-lookup"><span data-stu-id="da965-129"><dt>**NMERR\_BLOB\_CONVERSION\_ERROR**</dt></span></span> </dl>       | <span data-ttu-id="da965-130">El BLOB de configuración está dañado.</span><span class="sxs-lookup"><span data-stu-id="da965-130">The configuration BLOB is corrupt.</span></span> <span data-ttu-id="da965-131">Este error se genera mediante la llamada a **IRTC:: configure** .</span><span class="sxs-lookup"><span data-stu-id="da965-131">This error is generated by the **IRTC::Configure** call.</span></span><br/>                                                                                                                                                                                       |
| <dl> <span data-ttu-id="da965-132"><dt>**la \_ entrada de BLOB NMERR \_ \_ \_ no \_ existe**</dt></span><span class="sxs-lookup"><span data-stu-id="da965-132"><dt>**NMERR\_BLOB\_ENTRY\_DOES\_NOT\_EXIST**</dt></span></span> </dl> | <span data-ttu-id="da965-133">Falta una entrada necesaria para realizar esta operación en el BLOB de entrada especificado por el parámetro *hInputBlob* .</span><span class="sxs-lookup"><span data-stu-id="da965-133">The input BLOB specified by the *hInputBlob* parameter lacks an entry needed to perform this operation.</span></span> <span data-ttu-id="da965-134">Este error puede generarse mediante la llamada a **IRTC:: Connect** o **IRTC:: configure** .</span><span class="sxs-lookup"><span data-stu-id="da965-134">This error may be generated by the **IRTC::Connect** or **IRTC::Configure** call.</span></span> <span data-ttu-id="da965-135">Observe el BLOB de error devuelto por *hErrorBlob* para determinar qué entrada no se encontró.</span><span class="sxs-lookup"><span data-stu-id="da965-135">Look at the error BLOB returned by *hErrorBlob* to determine which entry was not found.</span></span><br/> |
| <dl> <span data-ttu-id="da965-136"><dt>**\_BLOB NMERR \_ no \_ inicializado**</dt></span><span class="sxs-lookup"><span data-stu-id="da965-136"><dt>**NMERR\_BLOB\_NOT\_INITIALIZED**</dt></span></span> </dl>        | <span data-ttu-id="da965-137">No se ha llamado a la función **CreateBlob** .</span><span class="sxs-lookup"><span data-stu-id="da965-137">The **CreateBlob** function has not been called.</span></span> <span data-ttu-id="da965-138">Este error se genera mediante la llamada a **IRTC:: configure** .</span><span class="sxs-lookup"><span data-stu-id="da965-138">This error is generated by the **IRTC::Configure** call.</span></span><br/>                                                                                                                                                                         |
| <dl> <span data-ttu-id="da965-139"><dt>**NMERR \_ cadena de blob \_ \_ no válida**</dt></span><span class="sxs-lookup"><span data-stu-id="da965-139"><dt>**NMERR\_BLOB\_STRING\_INVALID**</dt></span></span> </dl>         | <span data-ttu-id="da965-140">La cadena no termina en NULL.</span><span class="sxs-lookup"><span data-stu-id="da965-140">The string is not null-terminated.</span></span> <span data-ttu-id="da965-141">Este error se genera mediante la llamada a **IRTC:: configure** .</span><span class="sxs-lookup"><span data-stu-id="da965-141">This error is generated by the **IRTC::Configure** call.</span></span><br/>                                                                                                                                                                                       |
| <dl> <span data-ttu-id="da965-142"><dt>**\_desencadenador no válido de NMERR \_**</dt></span><span class="sxs-lookup"><span data-stu-id="da965-142"><dt>**NMERR\_ILLEGAL\_TRIGGER**</dt></span></span> </dl>              | <span data-ttu-id="da965-143">La parte del desencadenador del BLOB de entrada está dañada.</span><span class="sxs-lookup"><span data-stu-id="da965-143">The trigger portion of the input BLOB is corrupt.</span></span> <span data-ttu-id="da965-144">Este error se genera mediante la llamada a **IRTC:: configure** .</span><span class="sxs-lookup"><span data-stu-id="da965-144">This error is generated by the **IRTC::Configure** call.</span></span><br/>                                                                                                                                                                        |
| <dl> <span data-ttu-id="da965-145"><dt>**NMERR \_ BLOB no válido \_**</dt></span><span class="sxs-lookup"><span data-stu-id="da965-145"><dt>**NMERR\_INVALID\_BLOB**</dt></span></span> </dl>                 | <span data-ttu-id="da965-146">El objeto especificado en *hInputBlob* no es un BLOB.</span><span class="sxs-lookup"><span data-stu-id="da965-146">The object specified in *hInputBlob* is not a BLOB.</span></span> <span data-ttu-id="da965-147">Este error se genera mediante la llamada a **IRTC:: configure** .</span><span class="sxs-lookup"><span data-stu-id="da965-147">This error is generated by the **IRTC::Configure** call.</span></span><br/>                                                                                                                                                                      |
| <dl> <span data-ttu-id="da965-148"><dt>**NMERR \_ \_ de \_ memoria insuficiente**</dt></span><span class="sxs-lookup"><span data-stu-id="da965-148"><dt>**NMERR\_OUT\_OF\_MEMORY**</dt></span></span> </dl>               | <span data-ttu-id="da965-149">La memoria necesaria para realizar esta operación no está disponible.</span><span class="sxs-lookup"><span data-stu-id="da965-149">The memory needed to perform this operation is unavailable.</span></span> <span data-ttu-id="da965-150">Este error se genera mediante la llamada a **IRTC:: configure** .</span><span class="sxs-lookup"><span data-stu-id="da965-150">This error is generated by the **IRTC::Configure** call.</span></span><br/>                                                                                                                                                              |
| <dl> <span data-ttu-id="da965-151"><dt>**tiempo de espera de NMERR \_**</dt></span><span class="sxs-lookup"><span data-stu-id="da965-151"><dt>**NMERR\_TIMEOUT**</dt></span></span> </dl>                       | <span data-ttu-id="da965-152">La solicitud ha agotado el tiempo de espera. Este error se genera mediante la llamada a **IRTC:: configure** .</span><span class="sxs-lookup"><span data-stu-id="da965-152">The request has timed out. This error is generated by the **IRTC::Configure** call.</span></span><br/>                                                                                                                                                                                               |
| <dl> <span data-ttu-id="da965-153"><dt>**\_BLOB de nivel superior de NMERR \_**</dt></span><span class="sxs-lookup"><span data-stu-id="da965-153"><dt>**NMERR\_UPLEVEL\_BLOB**</dt></span></span> </dl>                 | <span data-ttu-id="da965-154">El número de versión del BLOB especificado en *hInputBlob* es incorrecto.</span><span class="sxs-lookup"><span data-stu-id="da965-154">The version number of the BLOB specified in *hInputBlob* is incorrect.</span></span> <span data-ttu-id="da965-155">Este error se genera mediante la llamada a **IRTC:: configure** .</span><span class="sxs-lookup"><span data-stu-id="da965-155">This error is generated by the **IRTC::Configure** call.</span></span><br/>                                                                                                                                                   |



 

## <a name="remarks"></a><span data-ttu-id="da965-156">Observaciones</span><span class="sxs-lookup"><span data-stu-id="da965-156">Remarks</span></span>

<span data-ttu-id="da965-157">Cuando se llama al método **Connect** , el NPP llama automáticamente al método **IRTC:: configure** mediante el BLOB proporcionado por *hInputBlob*.</span><span class="sxs-lookup"><span data-stu-id="da965-157">When the **Connect** method is called, the NPP automatically calls the **IRTC::Configure** method by using the BLOB provided by *hInputBlob*.</span></span> <span data-ttu-id="da965-158">Tenga en cuenta que los códigos de error devueltos por la llamada a **IRTC:: configure** se devuelven y se devuelven mediante la llamada a **IRTC:: Connect** .</span><span class="sxs-lookup"><span data-stu-id="da965-158">Note that any error codes returned by the call to **IRTC::Configure** are passed back and returned by the **IRTC::Connect** call.</span></span>

<span data-ttu-id="da965-159">Se debe llamar a este método antes de poder iniciar la captura de fotogramas.</span><span class="sxs-lookup"><span data-stu-id="da965-159">This method must be called before you can start capturing frames.</span></span> <span data-ttu-id="da965-160">Tenga en cuenta que cuando se conecta a la red mediante este método, debe seguir usando la interfaz **IRTC** para capturar fotogramas.</span><span class="sxs-lookup"><span data-stu-id="da965-160">Note that when you connect to the network using this method, you must continue to use the **IRTC** interface to capture frames.</span></span>

<span data-ttu-id="da965-161">Al llamar a esta función, debe especificar una función de devolución de llamada de estado o de fotograma, incluso si solo actúa como marcador de posición.</span><span class="sxs-lookup"><span data-stu-id="da965-161">When calling this function, you must specify a status or frame callback function, even if it only acts as a placeholder.</span></span>

<span data-ttu-id="da965-162">El BLOB de entrada especificado por *hInputBlob* se puede obtener llamando a los métodos **GetNPPBlobFromUI**, **GetNPPBlobTable** y **SelectNPPBlobFromTable** .</span><span class="sxs-lookup"><span data-stu-id="da965-162">The input BLOB specified by *hInputBlob* can be obtained by calling the **GetNPPBlobFromUI**, **GetNPPBlobTable**, and **SelectNPPBlobFromTable** methods.</span></span>

<span data-ttu-id="da965-163">El BLOB de error devuelto en *hErrorBlob* contiene información de error que el desarrollador o la aplicación pueden usar para solucionar problemas.</span><span class="sxs-lookup"><span data-stu-id="da965-163">The error BLOB returned in *hErrorBlob* contains error information that the developer or the application can use for troubleshooting.</span></span> <span data-ttu-id="da965-164">El BLOB de error devuelto por *hErrorBlob* contiene entradas que monitor de red no pudo comprender o encontrar en el BLOB de entrada especificado en *hInputBlob*.</span><span class="sxs-lookup"><span data-stu-id="da965-164">The error BLOB returned by *hErrorBlob* contains entries that Network Monitor could not understand or find in the input BLOB specified in *hInputBlob*.</span></span> <span data-ttu-id="da965-165">Por ejemplo, si \_ \_ se devuelve la entrada de BLOB NMERR \_ \_ \_ , la entrada monitor de red no encontró se incluye en el BLOB de error devuelto.</span><span class="sxs-lookup"><span data-stu-id="da965-165">For example, if NMERR\_BLOB\_ENTRY\_DOES\_NOT\_EXIST is returned, the entry Network Monitor could not find is included in the returned error BLOB.</span></span>



| <span data-ttu-id="da965-166">Para información acerca de</span><span class="sxs-lookup"><span data-stu-id="da965-166">For information about</span></span>                          | <span data-ttu-id="da965-167">Vea</span><span class="sxs-lookup"><span data-stu-id="da965-167">See</span></span>                                                                          |
|------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="da965-168">Obtener el BLOB de entrada que representa una NIC</span><span class="sxs-lookup"><span data-stu-id="da965-168">Obtaining the input BLOB that represents a NIC</span></span> | [<span data-ttu-id="da965-169">Seleccionar una tarjeta de interfaz de red</span><span class="sxs-lookup"><span data-stu-id="da965-169">Selecting a Network Interface Card</span></span>](selecting-a-network-interface-card.md) |



 

## <a name="requirements"></a><span data-ttu-id="da965-170">Requisitos</span><span class="sxs-lookup"><span data-stu-id="da965-170">Requirements</span></span>



| <span data-ttu-id="da965-171">Requisito</span><span class="sxs-lookup"><span data-stu-id="da965-171">Requirement</span></span> | <span data-ttu-id="da965-172">Value</span><span class="sxs-lookup"><span data-stu-id="da965-172">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="da965-173">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="da965-173">Minimum supported client</span></span><br/> | <span data-ttu-id="da965-174">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="da965-174">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="da965-175">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="da965-175">Minimum supported server</span></span><br/> | <span data-ttu-id="da965-176">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="da965-176">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="da965-177">Encabezado</span><span class="sxs-lookup"><span data-stu-id="da965-177">Header</span></span><br/>                   | <dl> <span data-ttu-id="da965-178"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="da965-178"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="da965-179">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="da965-179">DLL</span></span><br/>                      | <dl> <span data-ttu-id="da965-180"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="da965-180"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="da965-181">Vea también</span><span class="sxs-lookup"><span data-stu-id="da965-181">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da965-182">IRTC</span><span class="sxs-lookup"><span data-stu-id="da965-182">IRTC</span></span>](irtc.md)
</dt> <dt>

[<span data-ttu-id="da965-183">IRTC:: configure</span><span class="sxs-lookup"><span data-stu-id="da965-183">IRTC::Configure</span></span>](irtc-configure.md)
</dt> <dt>

[<span data-ttu-id="da965-184">IRTC::D Ulta</span><span class="sxs-lookup"><span data-stu-id="da965-184">IRTC::Disconnect</span></span>](irtc-disconnect.md)
</dt> <dt>

[<span data-ttu-id="da965-185">IRTC:: Start</span><span class="sxs-lookup"><span data-stu-id="da965-185">IRTC::Start</span></span>](irtc-start.md)
</dt> </dl>

 

 




