---
description: El método Connect conecta el NPP a la red mediante una NIC especificada y proporciona información de configuración sobre la conexión.
ms.assetid: 48189b2b-9889-4bd8-8972-26005fb7c341
title: 'IESP:: Connect (método) (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IESP.Connect
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 4fc9c88b0eb4671c61f268c5857dceba3dc500f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153852"
---
# <a name="iespconnect-method"></a><span data-ttu-id="27027-103">IESP:: Connect (método)</span><span class="sxs-lookup"><span data-stu-id="27027-103">IESP::Connect method</span></span>

<span data-ttu-id="27027-104">El método **Connect** conecta el NPP a la red mediante una NIC especificada y proporciona información de configuración sobre la conexión.</span><span class="sxs-lookup"><span data-stu-id="27027-104">The **Connect** method connects the NPP to the network by using a specified NIC and provides configuration information about the connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="27027-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="27027-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Connect(
  [in]  HBLOB hInputBlob,
  [in]  DWORD StatusCallbackProc,
  [in]  DWORD UserContext,
  [out] HBLOB hErrorBlob
);
```



## <a name="parameters"></a><span data-ttu-id="27027-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="27027-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="27027-107">*hInputBlob* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="27027-107">*hInputBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="27027-108">Identificador del BLOB que especifica la NIC a la que se conecta el NPP y la información de configuración para esa conexión.</span><span class="sxs-lookup"><span data-stu-id="27027-108">Handle to the BLOB that specifies the NIC that the NPP connects to and the configuration information for that connection.</span></span>

</dd> <dt>

<span data-ttu-id="27027-109">*StatusCallbackProc* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="27027-109">*StatusCallbackProc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="27027-110">Dirección de la función de devolución de llamada del usuario, que recibe actualizaciones de estado, como los desencadenadores.</span><span class="sxs-lookup"><span data-stu-id="27027-110">Address of the user's callback function, which receives status updates such as triggers.</span></span> <span data-ttu-id="27027-111">Si no se utiliza una función de devolución de llamada, establezca este parámetro y el parámetro *UserContext* en **null**.</span><span class="sxs-lookup"><span data-stu-id="27027-111">If a callback function is not used, set this parameter and the *UserContext* parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="27027-112">*UserContext* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="27027-112">*UserContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="27027-113">Valor que se pasa cuando se llama a la función de devolución de llamada del usuario.</span><span class="sxs-lookup"><span data-stu-id="27027-113">Value passed when the user's callback function is called.</span></span> <span data-ttu-id="27027-114">El valor de este parámetro suele ser HWND o un puntero ' this '.</span><span class="sxs-lookup"><span data-stu-id="27027-114">The value of this parameter is typically either HWND or a 'this' pointer.</span></span> <span data-ttu-id="27027-115">Si no se especifica una función de devolución de llamada, establezca este parámetro y el parámetro *StatusCallbackProc* en **null**.</span><span class="sxs-lookup"><span data-stu-id="27027-115">If a callback function is not specified, set this parameter and the *StatusCallbackProc* parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="27027-116">*hErrorBlob* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="27027-116">*hErrorBlob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="27027-117">Identificador de un BLOB de error que contiene información de error adicional.</span><span class="sxs-lookup"><span data-stu-id="27027-117">Handle to an error BLOB that contains additional error information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="27027-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="27027-118">Return value</span></span>

<span data-ttu-id="27027-119">Si el método se realiza correctamente, el valor devuelto es NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="27027-119">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="27027-120">Si el método no se realiza correctamente, el valor devuelto es uno de los siguientes códigos de error (que incluyen los errores devueltos por la llamada interna **iesp:: configure** ):</span><span class="sxs-lookup"><span data-stu-id="27027-120">If the method is unsuccessful, the return value is one of the following error codes (which include those errors returned by the internal **IESP::Configure** call):</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="27027-121">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="27027-121">Return code</span></span></th>
<th><span data-ttu-id="27027-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="27027-122">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><dl> <span data-ttu-id="27027-123"><dt><strong>NMERR_ALREADY_CONNECTED</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="27027-123"><dt><strong>NMERR_ALREADY_CONNECTED</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="27027-124">Esta instancia del objeto COM NPP ya está conectada a la red.</span><span class="sxs-lookup"><span data-stu-id="27027-124">This instance of the NPP COM object is already connected to the network.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="27027-125"><dt><strong>NMERR_BLOB_CONVERSION_ERROR</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="27027-125"><dt><strong>NMERR_BLOB_CONVERSION_ERROR</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="27027-126">El BLOB de configuración está dañado.</span><span class="sxs-lookup"><span data-stu-id="27027-126">The configuration BLOB is corrupt.</span></span> <span data-ttu-id="27027-127">Este error se genera mediante la llamada a <strong>iesp:: configure</strong> .</span><span class="sxs-lookup"><span data-stu-id="27027-127">This error is generated by the <strong>IESP::Configure</strong> call.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="27027-128"><dt><strong>NMERR_BLOB_ENTRY_DOES_NOT_EXIST</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="27027-128"><dt><strong>NMERR_BLOB_ENTRY_DOES_NOT_EXIST</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="27027-129">Falta una entrada necesaria para realizar esta operación en el BLOB de entrada especificado por el parámetro <em>hInputBlob</em> .</span><span class="sxs-lookup"><span data-stu-id="27027-129">The input BLOB specified by the <em>hInputBlob</em> parameter lacks an entry needed to perform this operation.</span></span> <span data-ttu-id="27027-130">Este error puede ser generado por la llamada a <strong>iesp:: Connect</strong> o <strong>iesp:: configure</strong> .</span><span class="sxs-lookup"><span data-stu-id="27027-130">This error might be generated by the <strong>IESP::Connect</strong> or <strong>IESP::Configure</strong> call.</span></span> <span data-ttu-id="27027-131">Observe el BLOB de error devuelto por <em>hErrorBlob</em> para determinar qué entrada no se encontró.</span><span class="sxs-lookup"><span data-stu-id="27027-131">Look at the error BLOB returned by <em>hErrorBlob</em> to determine which entry was not found.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="27027-132"><dt><strong>NMERR_BLOB_NOT_INITIALIZED</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="27027-132"><dt><strong>NMERR_BLOB_NOT_INITIALIZED</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="27027-133">No se ha llamado a la función <strong>CreateBlob</strong> .</span><span class="sxs-lookup"><span data-stu-id="27027-133">The <strong>CreateBlob</strong> function has not been called.</span></span> <span data-ttu-id="27027-134">Este error se genera mediante la llamada a <strong>iesp:: configure</strong> .</span><span class="sxs-lookup"><span data-stu-id="27027-134">This error is generated by the <strong>IESP::Configure</strong> call.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="27027-135"><dt><strong>NMERR_BLOB_STRING_INVALID</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="27027-135"><dt><strong>NMERR_BLOB_STRING_INVALID</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="27027-136">La cadena no termina en NULL.</span><span class="sxs-lookup"><span data-stu-id="27027-136">The string is not null-terminated.</span></span> <span data-ttu-id="27027-137">Este error se genera mediante la llamada a <strong>iesp:: configure</strong> .</span><span class="sxs-lookup"><span data-stu-id="27027-137">This error is generated by the <strong>IESP::Configure</strong> call.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="27027-138"><dt><strong>NMERR_ILLEGAL_TRIGGER</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="27027-138"><dt><strong>NMERR_ILLEGAL_TRIGGER</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="27027-139">La parte del desencadenador del BLOB de entrada está dañada.</span><span class="sxs-lookup"><span data-stu-id="27027-139">The trigger portion of the input BLOB is corrupt.</span></span> <span data-ttu-id="27027-140">Este error se genera mediante la llamada a <strong>iesp:: configure</strong> .</span><span class="sxs-lookup"><span data-stu-id="27027-140">This error is generated by the <strong>IESP::Configure</strong> call.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="27027-141"><dt><strong>NMERR_INVALID_BLOB</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="27027-141"><dt><strong>NMERR_INVALID_BLOB</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="27027-142">El objeto especificado en <em>hInputBlob</em> no es un BLOB.</span><span class="sxs-lookup"><span data-stu-id="27027-142">The object specified in <em>hInputBlob</em> is not a BLOB.</span></span> <span data-ttu-id="27027-143">Este error se genera mediante la llamada a <strong>iesp:: configure</strong> .</span><span class="sxs-lookup"><span data-stu-id="27027-143">This error is generated by the <strong>IESP::Configure</strong> call.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="27027-144"><dt><strong>NMERR_NO_DEFAULT_CAPTURE_DIRECTORY</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="27027-144"><dt><strong>NMERR_NO_DEFAULT_CAPTURE_DIRECTORY</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="27027-145">No se estableció el directorio de captura predeterminado en el registro.</span><span class="sxs-lookup"><span data-stu-id="27027-145">The default capture directory was not set in the registry.</span></span> <span data-ttu-id="27027-146">Use la siguiente ruta de acceso para establecer el directorio de captura.</span><span class="sxs-lookup"><span data-stu-id="27027-146">Use the following path to set the capture directory.</span></span> <br/>
<pre class="syntax" data-space="preserve"><code>HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\nm\Parameters\CapturePath</code></pre></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="27027-147"><dt><strong>NMERR_OUT_OF_MEMORY</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="27027-147"><dt><strong>NMERR_OUT_OF_MEMORY</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="27027-148">La memoria necesaria para realizar esta operación no está disponible.</span><span class="sxs-lookup"><span data-stu-id="27027-148">The memory needed to perform this operation is unavailable.</span></span> <span data-ttu-id="27027-149">Este error se genera mediante la llamada a <strong>iesp:: configure</strong> .</span><span class="sxs-lookup"><span data-stu-id="27027-149">This error is generated by the <strong>IESP::Configure</strong> call.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="27027-150"><dt><strong>NMERR_TIMEOUT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="27027-150"><dt><strong>NMERR_TIMEOUT</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="27027-151">La solicitud ha agotado el tiempo de espera. Este error se genera mediante la llamada a <strong>iesp:: configure</strong> .</span><span class="sxs-lookup"><span data-stu-id="27027-151">The request has timed out. This error is generated by the <strong>IESP::Configure</strong> call.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="27027-152"><dt><strong>NMERR_UPLEVEL_BLOB</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="27027-152"><dt><strong>NMERR_UPLEVEL_BLOB</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="27027-153">El número de versión del BLOB especificado en <em>hInputBlob</em> es incorrecto.</span><span class="sxs-lookup"><span data-stu-id="27027-153">The version number of the BLOB specified in <em>hInputBlob</em> is incorrect.</span></span> <span data-ttu-id="27027-154">Este error se genera mediante la llamada a <strong>iesp:: configure</strong> .</span><span class="sxs-lookup"><span data-stu-id="27027-154">This error is generated by the <strong>IESP::Configure</strong> call.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="27027-155">Observaciones</span><span class="sxs-lookup"><span data-stu-id="27027-155">Remarks</span></span>

<span data-ttu-id="27027-156">Cuando se llama al método **Connect** , monitor de red llama automáticamente a **iesp:: configure** mediante el BLOB proporcionado por el parámetro *hInputBlob* .</span><span class="sxs-lookup"><span data-stu-id="27027-156">When the **Connect** method is called, Network Monitor automatically calls **IESP::Configure** by using the BLOB provided by the *hInputBlob* parameter.</span></span> <span data-ttu-id="27027-157">Tenga en cuenta que los códigos de error devueltos por la llamada a **iesp:: configure** se devuelven y se devuelven mediante la llamada a **iesp:: Connect** .</span><span class="sxs-lookup"><span data-stu-id="27027-157">Note that any error codes returned by the call to **IESP::Configure** are passed back and returned by the **IESP::Connect** call.</span></span>

<span data-ttu-id="27027-158">Se debe llamar a este método antes de poder iniciar la captura de fotogramas.</span><span class="sxs-lookup"><span data-stu-id="27027-158">This method must be called before you can start capturing frames.</span></span> <span data-ttu-id="27027-159">Tenga en cuenta que cuando se conecta a la red mediante este método, debe seguir usando la interfaz **iesp** para capturar fotogramas.</span><span class="sxs-lookup"><span data-stu-id="27027-159">Note that when you connect to the network by using this method, you must continue to use the **IESP** interface to capture frames.</span></span>

<span data-ttu-id="27027-160">El BLOB de entrada especificado por *hInputBlob* se puede obtener llamando a **GetNPPBlobFromUI**, **GetNPPBlobTable** y **SelectNPPBlobFromTable**.</span><span class="sxs-lookup"><span data-stu-id="27027-160">The input BLOB specified by *hInputBlob* can be obtained by calling **GetNPPBlobFromUI**, **GetNPPBlobTable**, and **SelectNPPBlobFromTable**.</span></span>

<span data-ttu-id="27027-161">El BLOB de error devuelto por *hErrorBlob* contiene entradas que monitor de red no pudo comprender o encontrar en el BLOB de entrada especificado en *hInputBlob*.</span><span class="sxs-lookup"><span data-stu-id="27027-161">The error BLOB returned by *hErrorBlob* contains entries that Network Monitor could not understand or find in the input BLOB specified in *hInputBlob*.</span></span> <span data-ttu-id="27027-162">El BLOB de error devuelto contiene información de error que la aplicación puede usar para solucionar problemas.</span><span class="sxs-lookup"><span data-stu-id="27027-162">The returned error BLOB contains error information that the application can use for troubleshooting.</span></span> <span data-ttu-id="27027-163">Por ejemplo, si \_ \_ se devuelve la entrada de BLOB NMERR \_ \_ \_ , la entrada que monitor de red no pudo encontrar se incluye en el BLOB de error devuelto.</span><span class="sxs-lookup"><span data-stu-id="27027-163">For example, if NMERR\_BLOB\_ENTRY\_DOES\_NOT\_EXIST is returned, the entry that Network Monitor could not find is included in the returned error BLOB.</span></span>



| <span data-ttu-id="27027-164">Para información acerca de</span><span class="sxs-lookup"><span data-stu-id="27027-164">For information about</span></span>                          | <span data-ttu-id="27027-165">Vea</span><span class="sxs-lookup"><span data-stu-id="27027-165">See</span></span>                                                                          |
|------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="27027-166">Obtener el BLOB de entrada que representa una NIC</span><span class="sxs-lookup"><span data-stu-id="27027-166">Obtaining the input BLOB that represents a NIC</span></span> | [<span data-ttu-id="27027-167">Seleccionar una tarjeta de interfaz de red</span><span class="sxs-lookup"><span data-stu-id="27027-167">Selecting a Network Interface Card</span></span>](selecting-a-network-interface-card.md) |



 

## <a name="requirements"></a><span data-ttu-id="27027-168">Requisitos</span><span class="sxs-lookup"><span data-stu-id="27027-168">Requirements</span></span>



| <span data-ttu-id="27027-169">Requisito</span><span class="sxs-lookup"><span data-stu-id="27027-169">Requirement</span></span> | <span data-ttu-id="27027-170">Value</span><span class="sxs-lookup"><span data-stu-id="27027-170">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="27027-171">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="27027-171">Minimum supported client</span></span><br/> | <span data-ttu-id="27027-172">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="27027-172">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="27027-173">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="27027-173">Minimum supported server</span></span><br/> | <span data-ttu-id="27027-174">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="27027-174">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="27027-175">Encabezado</span><span class="sxs-lookup"><span data-stu-id="27027-175">Header</span></span><br/>                   | <dl> <span data-ttu-id="27027-176"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="27027-176"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="27027-177">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="27027-177">DLL</span></span><br/>                      | <dl> <span data-ttu-id="27027-178"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="27027-178"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="27027-179">Vea también</span><span class="sxs-lookup"><span data-stu-id="27027-179">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27027-180">IESP</span><span class="sxs-lookup"><span data-stu-id="27027-180">IESP</span></span>](iesp.md)
</dt> <dt>

[<span data-ttu-id="27027-181">IESP:: configure</span><span class="sxs-lookup"><span data-stu-id="27027-181">IESP::Configure</span></span>](iesp-configure.md)
</dt> <dt>

[<span data-ttu-id="27027-182">IESP::D Ulta</span><span class="sxs-lookup"><span data-stu-id="27027-182">IESP::Disconnect</span></span>](iesp-disconnect.md)
</dt> <dt>

[<span data-ttu-id="27027-183">IESP:: Start</span><span class="sxs-lookup"><span data-stu-id="27027-183">IESP::Start</span></span>](iesp-start.md)
</dt> </dl>

 

 




