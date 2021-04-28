---
description: 'Método IRTC::Connect: el método Connect conecta el NPP a la red mediante una NIC especificada y proporciona información de configuración para la conexión.'
ms.assetid: d017c2a3-a832-4084-b21b-0cca428c5360
title: Método IRTC::Connect (Netmon.h)
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
ms.openlocfilehash: ba62f3341b18ddfdbf09af4eec701322d901ab79
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110749"
---
# <a name="irtcconnect-method"></a><span data-ttu-id="9874f-103">IRTC::Connect (método)</span><span class="sxs-lookup"><span data-stu-id="9874f-103">IRTC::Connect method</span></span>

<span data-ttu-id="9874f-104">El **método Connect** conecta el NPP a la red mediante una NIC especificada y proporciona información de configuración para la conexión.</span><span class="sxs-lookup"><span data-stu-id="9874f-104">The **Connect** method connects the NPP to the network by using a specified NIC and provides configuration information for the connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="9874f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9874f-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Connect(
  [in]  HBLOB  hInputBlob,
  [in]  LPVOID StatusCallbackProc,
  [in]  LPVOID FramesCallbackProc,
  [in]  LPVOID UserContext,
  [out] HBLOB  hErrorBlob
);
```



## <a name="parameters"></a><span data-ttu-id="9874f-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9874f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9874f-107">*hInputBlob* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="9874f-107">*hInputBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9874f-108">Controle el BLOB que especifica la NIC a la que se va a conectar y la información de configuración de esa conexión.</span><span class="sxs-lookup"><span data-stu-id="9874f-108">Handle to the BLOB that specifies the NIC that you are connecting to and the configuration information for that connection.</span></span>

</dd> <dt>

<span data-ttu-id="9874f-109">*StatusCallbackProc* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="9874f-109">*StatusCallbackProc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9874f-110">Dirección de la función de devolución de llamada de estado del usuario, que recibe actualizaciones de estado como desencadenadores.</span><span class="sxs-lookup"><span data-stu-id="9874f-110">Address of the user's status callback function, which receives status updates such as triggers.</span></span> <span data-ttu-id="9874f-111">Este parámetro se puede establecer en **NULL.**</span><span class="sxs-lookup"><span data-stu-id="9874f-111">This parameter can be set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="9874f-112">*FramesCallbackProc* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="9874f-112">*FramesCallbackProc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9874f-113">Dirección de la función de devolución de llamada de marco del usuario, que se usa para recibir actualizaciones de estado, como desencadenadores.</span><span class="sxs-lookup"><span data-stu-id="9874f-113">Address of the user's frame callback function, which is used to receive status updates such as triggers.</span></span> <span data-ttu-id="9874f-114">Este parámetro se puede establecer en **NULL.**</span><span class="sxs-lookup"><span data-stu-id="9874f-114">This parameter can be set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="9874f-115">*UserContext* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="9874f-115">*UserContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9874f-116">Valor pasado cuando se llama a la función de devolución de llamada de marco y estado del usuario.</span><span class="sxs-lookup"><span data-stu-id="9874f-116">Value passed when the user's status and frame callback function is called.</span></span> <span data-ttu-id="9874f-117">Si se especifican ambas funciones de devolución de llamada, deben usar el mismo valor de contexto de usuario.</span><span class="sxs-lookup"><span data-stu-id="9874f-117">If both callback functions are specified, they must use the same user-context value.</span></span> <span data-ttu-id="9874f-118">El valor de este parámetro suele ser HWND o un puntero "this".</span><span class="sxs-lookup"><span data-stu-id="9874f-118">The value of this parameter is typically either HWND or a 'this' pointer.</span></span>

</dd> <dt>

<span data-ttu-id="9874f-119">*hErrorBlob* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="9874f-119">*hErrorBlob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9874f-120">Controlar un blob de error que contiene información de error adicional.</span><span class="sxs-lookup"><span data-stu-id="9874f-120">Handle to an error BLOB that contains additional error information.</span></span> <span data-ttu-id="9874f-121">Vea Comentarios en la parte inferior de este tema para obtener información sobre lo que se encuentra en el blob de errores.</span><span class="sxs-lookup"><span data-stu-id="9874f-121">See Remarks at the bottom of this topic for information about what is in the error BLOB.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9874f-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9874f-122">Return value</span></span>

<span data-ttu-id="9874f-123">Si este método es correcto, el valor devuelto es NMERR \_ SUCCESS.</span><span class="sxs-lookup"><span data-stu-id="9874f-123">If this method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="9874f-124">Si el método no se realiza correctamente, el valor devuelto es uno de los siguientes códigos de error (que incluyen los errores devueltos por la llamada **interna IRTC::Configure):**</span><span class="sxs-lookup"><span data-stu-id="9874f-124">If the method is unsuccessful, the return value is one of the following error codes (which include those errors returned by the internal **IRTC::Configure** call):</span></span>



| <span data-ttu-id="9874f-125">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="9874f-125">Return code</span></span>                                                                                                         | <span data-ttu-id="9874f-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="9874f-126">Description</span></span>                                                                                                                                                                                                                                                                                  |
|---------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="9874f-127"><dt>**NMERR \_ YA \_ CONECTADO**</dt></span><span class="sxs-lookup"><span data-stu-id="9874f-127"><dt>**NMERR\_ALREADY\_CONNECTED**</dt></span></span> </dl>            | <span data-ttu-id="9874f-128">Esta instancia del objeto COM de NPP ya está conectada a la red.</span><span class="sxs-lookup"><span data-stu-id="9874f-128">This instance of the NPP COM object is already connected to the network.</span></span><br/>                                                                                                                                                                                                          |
| <dl> <span data-ttu-id="9874f-129"><dt>**ERROR DE CONVERSIÓN \_ DE \_ BLOBS DE NMERR \_**</dt></span><span class="sxs-lookup"><span data-stu-id="9874f-129"><dt>**NMERR\_BLOB\_CONVERSION\_ERROR**</dt></span></span> </dl>       | <span data-ttu-id="9874f-130">El BLOB de configuración está dañado.</span><span class="sxs-lookup"><span data-stu-id="9874f-130">The configuration BLOB is corrupt.</span></span> <span data-ttu-id="9874f-131">La llamada **IRTC::Configure** genera este error.</span><span class="sxs-lookup"><span data-stu-id="9874f-131">This error is generated by the **IRTC::Configure** call.</span></span><br/>                                                                                                                                                                                       |
| <dl> <span data-ttu-id="9874f-132"><dt>**LA ENTRADA DE BLOB DE NMERR \_ \_ NO \_ \_ \_ EXISTE**</dt></span><span class="sxs-lookup"><span data-stu-id="9874f-132"><dt>**NMERR\_BLOB\_ENTRY\_DOES\_NOT\_EXIST**</dt></span></span> </dl> | <span data-ttu-id="9874f-133">El BLOB de entrada especificado por el *parámetro hInputBlob* carece de una entrada necesaria para realizar esta operación.</span><span class="sxs-lookup"><span data-stu-id="9874f-133">The input BLOB specified by the *hInputBlob* parameter lacks an entry needed to perform this operation.</span></span> <span data-ttu-id="9874f-134">La llamada **IRTC::Connect** o **IRTC::Configure** puede generar este error.</span><span class="sxs-lookup"><span data-stu-id="9874f-134">This error may be generated by the **IRTC::Connect** or **IRTC::Configure** call.</span></span> <span data-ttu-id="9874f-135">Mire el blob de error devuelto por *hErrorBlob para* determinar qué entrada no se encontró.</span><span class="sxs-lookup"><span data-stu-id="9874f-135">Look at the error BLOB returned by *hErrorBlob* to determine which entry was not found.</span></span><br/> |
| <dl> <span data-ttu-id="9874f-136"><dt>**BLOB DE NMERR \_ \_ NO \_ INICIALIZADO**</dt></span><span class="sxs-lookup"><span data-stu-id="9874f-136"><dt>**NMERR\_BLOB\_NOT\_INITIALIZED**</dt></span></span> </dl>        | <span data-ttu-id="9874f-137">No se ha llamado a la función **CreateBlob.**</span><span class="sxs-lookup"><span data-stu-id="9874f-137">The **CreateBlob** function has not been called.</span></span> <span data-ttu-id="9874f-138">La llamada **IRTC::Configure** genera este error.</span><span class="sxs-lookup"><span data-stu-id="9874f-138">This error is generated by the **IRTC::Configure** call.</span></span><br/>                                                                                                                                                                         |
| <dl> <span data-ttu-id="9874f-139"><dt>**CADENA DE BLOB DE NMERR \_ \_ NO \_ VÁLIDA**</dt></span><span class="sxs-lookup"><span data-stu-id="9874f-139"><dt>**NMERR\_BLOB\_STRING\_INVALID**</dt></span></span> </dl>         | <span data-ttu-id="9874f-140">La cadena no termina en NULL.</span><span class="sxs-lookup"><span data-stu-id="9874f-140">The string is not null-terminated.</span></span> <span data-ttu-id="9874f-141">La llamada **IRTC::Configure** genera este error.</span><span class="sxs-lookup"><span data-stu-id="9874f-141">This error is generated by the **IRTC::Configure** call.</span></span><br/>                                                                                                                                                                                       |
| <dl> <span data-ttu-id="9874f-142"><dt>**DESENCADENADOR NO ES DE NMERR \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="9874f-142"><dt>**NMERR\_ILLEGAL\_TRIGGER**</dt></span></span> </dl>              | <span data-ttu-id="9874f-143">La parte del desencadenador del BLOB de entrada está dañada.</span><span class="sxs-lookup"><span data-stu-id="9874f-143">The trigger portion of the input BLOB is corrupt.</span></span> <span data-ttu-id="9874f-144">La llamada **IRTC::Configure** genera este error.</span><span class="sxs-lookup"><span data-stu-id="9874f-144">This error is generated by the **IRTC::Configure** call.</span></span><br/>                                                                                                                                                                        |
| <dl> <span data-ttu-id="9874f-145"><dt>**BLOB NO VÁLIDO DE NMERR \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="9874f-145"><dt>**NMERR\_INVALID\_BLOB**</dt></span></span> </dl>                 | <span data-ttu-id="9874f-146">El objeto especificado en *hInputBlob* no es un BLOB.</span><span class="sxs-lookup"><span data-stu-id="9874f-146">The object specified in *hInputBlob* is not a BLOB.</span></span> <span data-ttu-id="9874f-147">La llamada **IRTC::Configure** genera este error.</span><span class="sxs-lookup"><span data-stu-id="9874f-147">This error is generated by the **IRTC::Configure** call.</span></span><br/>                                                                                                                                                                      |
| <dl> <span data-ttu-id="9874f-148"><dt>**MEMORIA DE NMERR \_ \_ FUERA DE \_ MEMORIA**</dt></span><span class="sxs-lookup"><span data-stu-id="9874f-148"><dt>**NMERR\_OUT\_OF\_MEMORY**</dt></span></span> </dl>               | <span data-ttu-id="9874f-149">La memoria necesaria para realizar esta operación no está disponible.</span><span class="sxs-lookup"><span data-stu-id="9874f-149">The memory needed to perform this operation is unavailable.</span></span> <span data-ttu-id="9874f-150">La llamada **IRTC::Configure** genera este error.</span><span class="sxs-lookup"><span data-stu-id="9874f-150">This error is generated by the **IRTC::Configure** call.</span></span><br/>                                                                                                                                                              |
| <dl> <span data-ttu-id="9874f-151"><dt>**TIEMPO DE ESPERA DE NMERR \_**</dt></span><span class="sxs-lookup"><span data-stu-id="9874f-151"><dt>**NMERR\_TIMEOUT**</dt></span></span> </dl>                       | <span data-ttu-id="9874f-152">Se ha pasado el tiempo de espera de la solicitud. La llamada **IRTC::Configure** genera este error.</span><span class="sxs-lookup"><span data-stu-id="9874f-152">The request has timed out. This error is generated by the **IRTC::Configure** call.</span></span><br/>                                                                                                                                                                                               |
| <dl> <span data-ttu-id="9874f-153"><dt>**BLOB DE NIVEL \_ SUPERIOR NMERR \_**</dt></span><span class="sxs-lookup"><span data-stu-id="9874f-153"><dt>**NMERR\_UPLEVEL\_BLOB**</dt></span></span> </dl>                 | <span data-ttu-id="9874f-154">El número de versión del BLOB especificado en *hInputBlob* es incorrecto.</span><span class="sxs-lookup"><span data-stu-id="9874f-154">The version number of the BLOB specified in *hInputBlob* is incorrect.</span></span> <span data-ttu-id="9874f-155">La llamada **IRTC::Configure** genera este error.</span><span class="sxs-lookup"><span data-stu-id="9874f-155">This error is generated by the **IRTC::Configure** call.</span></span><br/>                                                                                                                                                   |



 

## <a name="remarks"></a><span data-ttu-id="9874f-156">Comentarios</span><span class="sxs-lookup"><span data-stu-id="9874f-156">Remarks</span></span>

<span data-ttu-id="9874f-157">Cuando se llama al método **Connect,** el NPP llama automáticamente al método **IRTC::Configure** mediante el BLOB proporcionado por *hInputBlob*.</span><span class="sxs-lookup"><span data-stu-id="9874f-157">When the **Connect** method is called, the NPP automatically calls the **IRTC::Configure** method by using the BLOB provided by *hInputBlob*.</span></span> <span data-ttu-id="9874f-158">Tenga en cuenta que los códigos de error devueltos por la llamada **a IRTC::Configure** se devuelven y devuelven mediante la **llamada IRTC::Connect.**</span><span class="sxs-lookup"><span data-stu-id="9874f-158">Note that any error codes returned by the call to **IRTC::Configure** are passed back and returned by the **IRTC::Connect** call.</span></span>

<span data-ttu-id="9874f-159">Se debe llamar a este método para poder empezar a capturar fotogramas.</span><span class="sxs-lookup"><span data-stu-id="9874f-159">This method must be called before you can start capturing frames.</span></span> <span data-ttu-id="9874f-160">Tenga en cuenta que cuando se conecta a la red mediante este método, debe seguir usando la **interfaz IRTC** para capturar fotogramas.</span><span class="sxs-lookup"><span data-stu-id="9874f-160">Note that when you connect to the network using this method, you must continue to use the **IRTC** interface to capture frames.</span></span>

<span data-ttu-id="9874f-161">Al llamar a esta función, debe especificar una función de devolución de llamada de estado o marco, incluso si solo actúa como marcador de posición.</span><span class="sxs-lookup"><span data-stu-id="9874f-161">When calling this function, you must specify a status or frame callback function, even if it only acts as a placeholder.</span></span>

<span data-ttu-id="9874f-162">El BLOB de entrada especificado por *hInputBlob* se puede obtener llamando a los métodos **GetNPPBlobFromUI**, **GetNPPBlobTable** y **SelectNPPBlobFromTable.**</span><span class="sxs-lookup"><span data-stu-id="9874f-162">The input BLOB specified by *hInputBlob* can be obtained by calling the **GetNPPBlobFromUI**, **GetNPPBlobTable**, and **SelectNPPBlobFromTable** methods.</span></span>

<span data-ttu-id="9874f-163">El blob de error devuelto en *hErrorBlob* contiene información de error que el desarrollador o la aplicación pueden usar para solucionar problemas.</span><span class="sxs-lookup"><span data-stu-id="9874f-163">The error BLOB returned in *hErrorBlob* contains error information that the developer or the application can use for troubleshooting.</span></span> <span data-ttu-id="9874f-164">El blob de error devuelto por *hErrorBlob* contiene entradas que Monitor de red no se pudieron comprender o encontrar en el BLOB de entrada especificado en *hInputBlob*.</span><span class="sxs-lookup"><span data-stu-id="9874f-164">The error BLOB returned by *hErrorBlob* contains entries that Network Monitor could not understand or find in the input BLOB specified in *hInputBlob*.</span></span> <span data-ttu-id="9874f-165">Por ejemplo, si se devuelve NMERR BLOB ENTRY DOES NOT EXIST, la entrada Monitor de red no se encuentra se incluye en el \_ \_ blob de error \_ \_ \_ devuelto.</span><span class="sxs-lookup"><span data-stu-id="9874f-165">For example, if NMERR\_BLOB\_ENTRY\_DOES\_NOT\_EXIST is returned, the entry Network Monitor could not find is included in the returned error BLOB.</span></span>



| <span data-ttu-id="9874f-166">Para información acerca de</span><span class="sxs-lookup"><span data-stu-id="9874f-166">For information about</span></span>                          | <span data-ttu-id="9874f-167">Vea</span><span class="sxs-lookup"><span data-stu-id="9874f-167">See</span></span>                                                                          |
|------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="9874f-168">Obtención del BLOB de entrada que representa una NIC</span><span class="sxs-lookup"><span data-stu-id="9874f-168">Obtaining the input BLOB that represents a NIC</span></span> | [<span data-ttu-id="9874f-169">Selección de una tarjeta de interfaz de red</span><span class="sxs-lookup"><span data-stu-id="9874f-169">Selecting a Network Interface Card</span></span>](selecting-a-network-interface-card.md) |



 

## <a name="requirements"></a><span data-ttu-id="9874f-170">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9874f-170">Requirements</span></span>



| <span data-ttu-id="9874f-171">Requisito</span><span class="sxs-lookup"><span data-stu-id="9874f-171">Requirement</span></span> | <span data-ttu-id="9874f-172">Valor</span><span class="sxs-lookup"><span data-stu-id="9874f-172">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9874f-173">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9874f-173">Minimum supported client</span></span><br/> | <span data-ttu-id="9874f-174">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="9874f-174">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="9874f-175">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9874f-175">Minimum supported server</span></span><br/> | <span data-ttu-id="9874f-176">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="9874f-176">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="9874f-177">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9874f-177">Header</span></span><br/>                   | <dl> <span data-ttu-id="9874f-178"><dt>Netmon.h</dt></span><span class="sxs-lookup"><span data-stu-id="9874f-178"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="9874f-179">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="9874f-179">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9874f-180"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9874f-180"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9874f-181">Consulte también</span><span class="sxs-lookup"><span data-stu-id="9874f-181">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9874f-182">IRTC</span><span class="sxs-lookup"><span data-stu-id="9874f-182">IRTC</span></span>](irtc.md)
</dt> <dt>

[<span data-ttu-id="9874f-183">IRTC::Configure</span><span class="sxs-lookup"><span data-stu-id="9874f-183">IRTC::Configure</span></span>](irtc-configure.md)
</dt> <dt>

[<span data-ttu-id="9874f-184">IRTC::D isconnect</span><span class="sxs-lookup"><span data-stu-id="9874f-184">IRTC::Disconnect</span></span>](irtc-disconnect.md)
</dt> <dt>

[<span data-ttu-id="9874f-185">IRTC::Start</span><span class="sxs-lookup"><span data-stu-id="9874f-185">IRTC::Start</span></span>](irtc-start.md)
</dt> </dl>

 

 




