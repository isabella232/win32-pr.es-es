---
description: El método Connect conecta el NPP a la red mediante una tarjeta de interfaz de red especificada y proporciona información de configuración sobre la conexión.
ms.assetid: aae9ff9c-d077-4db2-a900-9916e4f7bb8b
title: 'IDelaydC:: Connect (método) (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDelaydC.Connect
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: b2cd1fb5ad694493c4a225aa3bf109d7775b9dd6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907665"
---
# <a name="idelaydcconnect-method"></a><span data-ttu-id="82948-103">IDelaydC:: Connect (método)</span><span class="sxs-lookup"><span data-stu-id="82948-103">IDelaydC::Connect method</span></span>

<span data-ttu-id="82948-104">El método **Connect** conecta el NPP a la red mediante una tarjeta de interfaz de red especificada y proporciona información de configuración sobre la conexión.</span><span class="sxs-lookup"><span data-stu-id="82948-104">The **Connect** method connects the NPP to the network by using a specified network interface card and provides configuration information about the connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="82948-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="82948-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Connect(
  [in]  HBLOB  hInputBlob,
  [in]  LPVOID StatusCallbackProc,
  [in]  LPVOID UserContext,
  [out] HBLOB  hErrorBlob
);
```



## <a name="parameters"></a><span data-ttu-id="82948-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="82948-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="82948-107">*hInputBlob* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="82948-107">*hInputBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="82948-108">Identificador del BLOB que especifica la NIC a la que se está conectando y la información de configuración sobre dicha conexión.</span><span class="sxs-lookup"><span data-stu-id="82948-108">Handle to the BLOB that specifies the NIC that you are connecting to and the configuration information about that connection.</span></span>

</dd> <dt>

<span data-ttu-id="82948-109">*StatusCallbackProc* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="82948-109">*StatusCallbackProc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="82948-110">Dirección de la función de devolución de llamada del usuario, que se usa para recibir las actualizaciones de estado como los desencadenadores.</span><span class="sxs-lookup"><span data-stu-id="82948-110">Address of the user's callback function, which is used to receive status updates such as triggers.</span></span> <span data-ttu-id="82948-111">Si no se usa ninguna función de devolución de llamada, establezca este parámetro y el parámetro *UserContext* en **null**.</span><span class="sxs-lookup"><span data-stu-id="82948-111">If no callback function is used, set this parameter and the *UserContext* parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="82948-112">*UserContext* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="82948-112">*UserContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="82948-113">Valor que se pasa cuando se llama a la función de devolución de llamada del usuario.</span><span class="sxs-lookup"><span data-stu-id="82948-113">Value passed when the user's callback function is called.</span></span> <span data-ttu-id="82948-114">El valor de este parámetro suele ser HWND o un puntero ' this '.</span><span class="sxs-lookup"><span data-stu-id="82948-114">The value of this parameter is typically either HWND or a 'this' pointer.</span></span> <span data-ttu-id="82948-115">Si no se especifica una función de devolución de llamada, establezca este parámetro y el parámetro *StatusCallbackProc* en **null**.</span><span class="sxs-lookup"><span data-stu-id="82948-115">If a callback function is not specified, set this parameter and the *StatusCallbackProc* parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="82948-116">*hErrorBlob* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="82948-116">*hErrorBlob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="82948-117">Identificador de un BLOB de error que contiene información de error adicional.</span><span class="sxs-lookup"><span data-stu-id="82948-117">Handle to an error BLOB that contains additional error information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="82948-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="82948-118">Return value</span></span>

<span data-ttu-id="82948-119">Si este método se realiza correctamente, el valor devuelto es NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="82948-119">If this method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="82948-120">Si el método no se realiza correctamente, el valor devuelto es uno de los siguientes códigos de error (que incluyen los errores devueltos por la llamada interna **IDelaydC:: configure** ):</span><span class="sxs-lookup"><span data-stu-id="82948-120">If the method is unsuccessful, the return value is one of the following error codes (which include those errors returned by the internal **IDelaydC::Configure** call):</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="82948-121">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="82948-121">Return code</span></span></th>
<th><span data-ttu-id="82948-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="82948-122">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><dl> <span data-ttu-id="82948-123"><dt><strong>NMERR_ALREADY_CONNECTED</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="82948-123"><dt><strong>NMERR_ALREADY_CONNECTED</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="82948-124">Esta instancia del objeto COM NPP ya está conectada a la red.</span><span class="sxs-lookup"><span data-stu-id="82948-124">This instance of the NPP COM object is already connected to the network.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="82948-125"><dt><strong>NMERR_BLOB_CONVERSION_ERROR</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="82948-125"><dt><strong>NMERR_BLOB_CONVERSION_ERROR</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="82948-126">El BLOB de configuración está dañado.</span><span class="sxs-lookup"><span data-stu-id="82948-126">The configuration BLOB is corrupt.</span></span> <span data-ttu-id="82948-127">Este error se genera mediante la llamada a <strong>IDelaydC:: configure</strong> .</span><span class="sxs-lookup"><span data-stu-id="82948-127">This error is generated by the <strong>IDelaydC::Configure</strong> call.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="82948-128"><dt><strong>NMERR_BLOB_ENTRY_DOES_NOT_EXIST</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="82948-128"><dt><strong>NMERR_BLOB_ENTRY_DOES_NOT_EXIST</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="82948-129">Falta una entrada necesaria para realizar esta operación en el BLOB de entrada especificado por <em>hInputBlob</em> .</span><span class="sxs-lookup"><span data-stu-id="82948-129">The input BLOB specified by <em>hInputBlob</em> is missing an entry needed to perform this operation.</span></span> <span data-ttu-id="82948-130">Este error puede generarse mediante la llamada a <strong>IDelaydC:: Connect</strong> o <strong>IDelaydC:: configure</strong> .</span><span class="sxs-lookup"><span data-stu-id="82948-130">This error may be generated by the <strong>IDelaydC::Connect</strong> or <strong>IDelaydC::Configure</strong> call.</span></span> <span data-ttu-id="82948-131">Observe el BLOB de error devuelto por <em>hErrorBlob</em> para determinar qué entrada no se encontró.</span><span class="sxs-lookup"><span data-stu-id="82948-131">Look at the error BLOB returned by <em>hErrorBlob</em> to determine which entry was not found.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="82948-132"><dt><strong>NMERR_BLOB_NOT_INITIALIZED</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="82948-132"><dt><strong>NMERR_BLOB_NOT_INITIALIZED</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="82948-133">No se ha llamado a la función <strong>CreateBlob</strong> .</span><span class="sxs-lookup"><span data-stu-id="82948-133">The <strong>CreateBlob</strong> function has not been called.</span></span> <span data-ttu-id="82948-134">Este error se genera mediante la llamada a <strong>IDelaydC:: configure</strong> .</span><span class="sxs-lookup"><span data-stu-id="82948-134">This error is generated by the <strong>IDelaydC::Configure</strong> call.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="82948-135"><dt><strong>NMERR_BLOB_STRING_INVALID</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="82948-135"><dt><strong>NMERR_BLOB_STRING_INVALID</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="82948-136">La cadena no termina en NULL.</span><span class="sxs-lookup"><span data-stu-id="82948-136">The string is not null-terminated.</span></span> <span data-ttu-id="82948-137">Este error se genera mediante la llamada a <strong>IDelaydC:: configure</strong> .</span><span class="sxs-lookup"><span data-stu-id="82948-137">This error is generated by the <strong>IDelaydC::Configure</strong> call.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="82948-138"><dt><strong>NMERR_ILLEGAL_TRIGGER</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="82948-138"><dt><strong>NMERR_ILLEGAL_TRIGGER</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="82948-139">La parte del desencadenador del BLOB de entrada está dañada.</span><span class="sxs-lookup"><span data-stu-id="82948-139">The trigger portion of the input BLOB is corrupt.</span></span> <span data-ttu-id="82948-140">Este error se genera mediante la llamada a <strong>IDelaydC:: configure</strong> .</span><span class="sxs-lookup"><span data-stu-id="82948-140">This error is generated by the <strong>IDelaydC::Configure</strong> call.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="82948-141"><dt><strong>NMERR_INVALID_BLOB</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="82948-141"><dt><strong>NMERR_INVALID_BLOB</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="82948-142">El objeto especificado en <em>hInputBlob</em> no es un BLOB.</span><span class="sxs-lookup"><span data-stu-id="82948-142">The object specified in <em>hInputBlob</em> is not a BLOB.</span></span> <span data-ttu-id="82948-143">Este error se genera mediante la llamada a <strong>IDelaydC:: configure</strong> .</span><span class="sxs-lookup"><span data-stu-id="82948-143">This error is generated by the <strong>IDelaydC::Configure</strong> call.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="82948-144"><dt><strong>NMERR_NO_DEFAULT_CAPTURE_DIRECTORY</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="82948-144"><dt><strong>NMERR_NO_DEFAULT_CAPTURE_DIRECTORY</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="82948-145">No se estableció el directorio de captura predeterminado en el registro.</span><span class="sxs-lookup"><span data-stu-id="82948-145">The default capture directory was not set in the registry.</span></span> <span data-ttu-id="82948-146">Use la siguiente ruta de acceso para establecer el directorio de captura.</span><span class="sxs-lookup"><span data-stu-id="82948-146">Use the following path to set the capture directory.</span></span> <br/>
<pre class="syntax" data-space="preserve"><code>HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\nm\Parameters\CapturePath</code></pre></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="82948-147"><dt><strong>NMERR_OUT_OF_MEMORY</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="82948-147"><dt><strong>NMERR_OUT_OF_MEMORY</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="82948-148">No había memoria disponible para realizar esta operación.</span><span class="sxs-lookup"><span data-stu-id="82948-148">No memory was available to perform this operation.</span></span> <span data-ttu-id="82948-149">Este error se genera mediante la llamada a <strong>IDelaydC:: configure</strong> .</span><span class="sxs-lookup"><span data-stu-id="82948-149">This error is generated by the <strong>IDelaydC::Configure</strong> call.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="82948-150"><dt><strong>NMERR_TIMEOUT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="82948-150"><dt><strong>NMERR_TIMEOUT</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="82948-151">La solicitud ha agotado el tiempo de espera. Este error se genera mediante la llamada a <strong>IDelaydC:: configure</strong> .</span><span class="sxs-lookup"><span data-stu-id="82948-151">The request has timed out. This error is generated by the <strong>IDelaydC::Configure</strong> call.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="82948-152"><dt><strong>NMERR_UPLEVEL_BLOB</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="82948-152"><dt><strong>NMERR_UPLEVEL_BLOB</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="82948-153">El número de versión del BLOB especificado en <em>hInputBlob</em> es incorrecto.</span><span class="sxs-lookup"><span data-stu-id="82948-153">The version number of the BLOB specified in <em>hInputBlob</em> is incorrect.</span></span> <span data-ttu-id="82948-154">Este error se genera mediante la llamada a <strong>IDelaydC:: configure</strong> .</span><span class="sxs-lookup"><span data-stu-id="82948-154">This error is generated by the <strong>IDelaydC::Configure</strong> call.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="82948-155">Observaciones</span><span class="sxs-lookup"><span data-stu-id="82948-155">Remarks</span></span>

<span data-ttu-id="82948-156">Cuando se llama al método **Connect** , el NPP llama automáticamente a **IDelaydC:: configure** mediante el BLOB proporcionado por *hInputBlob*.</span><span class="sxs-lookup"><span data-stu-id="82948-156">When the **Connect** method is called, the NPP automatically calls **IDelaydC::Configure** by using the BLOB provided by *hInputBlob*.</span></span> <span data-ttu-id="82948-157">Tenga en cuenta que los códigos de error devueltos por la llamada a **IDelaydC:: configure** se devuelven y se devuelven mediante la llamada a **IDelaydC:: Connect** .</span><span class="sxs-lookup"><span data-stu-id="82948-157">Note that any error codes returned by the call to **IDelaydC::Configure** are passed back and returned by the **IDelaydC::Connect** call.</span></span>

<span data-ttu-id="82948-158">Se debe llamar a este método antes de poder iniciar la captura de fotogramas.</span><span class="sxs-lookup"><span data-stu-id="82948-158">This method must be called before you can start capturing frames.</span></span> <span data-ttu-id="82948-159">Tenga en cuenta que cuando se conecta a la red mediante este método, debe seguir usando los métodos de la interfaz **IDelaydC** para capturar fotogramas.</span><span class="sxs-lookup"><span data-stu-id="82948-159">Note that when you connect to the network by using this method, you must continue to use the **IDelaydC** interface methods to capture frames.</span></span>

<span data-ttu-id="82948-160">El BLOB de entrada especificado por el parámetro *hInputBlob* se puede obtener llamando a **GetNPPBlobFromUI**, **GetNPPBlobTable** y **SelectNPPBlobFromTable**.</span><span class="sxs-lookup"><span data-stu-id="82948-160">The input BLOB specified by the *hInputBlob* parameter can be obtained by calling **GetNPPBlobFromUI**, **GetNPPBlobTable**, and **SelectNPPBlobFromTable**.</span></span>

<span data-ttu-id="82948-161">El BLOB de error devuelto en *hErrorBlob* contiene información de error que el desarrollador o la aplicación pueden usar para solucionar problemas.</span><span class="sxs-lookup"><span data-stu-id="82948-161">The error BLOB returned in *hErrorBlob* contains error information that the developer or the application can use for troubleshooting.</span></span> <span data-ttu-id="82948-162">El BLOB de error devuelto por *hErrorBlob* contiene entradas que monitor de red no pudo comprender o encontrar en el BLOB de entrada especificado en *hInputBlob*.</span><span class="sxs-lookup"><span data-stu-id="82948-162">The error BLOB returned by *hErrorBlob* contains entries that Network Monitor could not understand or find in the input BLOB specified in *hInputBlob*.</span></span> <span data-ttu-id="82948-163">Por ejemplo, si \_ \_ se devuelve la entrada de BLOB NMERR \_ \_ \_ , la entrada monitor de red no encontró se incluye en el BLOB de error devuelto.</span><span class="sxs-lookup"><span data-stu-id="82948-163">For example, if NMERR\_BLOB\_ENTRY\_DOES\_NOT\_EXIST is returned, the entry Network Monitor could not find is included in the returned error BLOB.</span></span>



| <span data-ttu-id="82948-164">Para información acerca de</span><span class="sxs-lookup"><span data-stu-id="82948-164">For information about</span></span>                          | <span data-ttu-id="82948-165">Vea</span><span class="sxs-lookup"><span data-stu-id="82948-165">See</span></span>                                                                          |
|------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="82948-166">Obtener el BLOB de entrada que representa una NIC</span><span class="sxs-lookup"><span data-stu-id="82948-166">Obtaining the input BLOB that represents a NIC</span></span> | [<span data-ttu-id="82948-167">Seleccionar una tarjeta de interfaz de red</span><span class="sxs-lookup"><span data-stu-id="82948-167">Selecting a Network Interface Card</span></span>](selecting-a-network-interface-card.md) |



 

## <a name="requirements"></a><span data-ttu-id="82948-168">Requisitos</span><span class="sxs-lookup"><span data-stu-id="82948-168">Requirements</span></span>



| <span data-ttu-id="82948-169">Requisito</span><span class="sxs-lookup"><span data-stu-id="82948-169">Requirement</span></span> | <span data-ttu-id="82948-170">Value</span><span class="sxs-lookup"><span data-stu-id="82948-170">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="82948-171">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="82948-171">Minimum supported client</span></span><br/> | <span data-ttu-id="82948-172">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="82948-172">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="82948-173">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="82948-173">Minimum supported server</span></span><br/> | <span data-ttu-id="82948-174">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="82948-174">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="82948-175">Encabezado</span><span class="sxs-lookup"><span data-stu-id="82948-175">Header</span></span><br/>                   | <dl> <span data-ttu-id="82948-176"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="82948-176"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="82948-177">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="82948-177">DLL</span></span><br/>                      | <dl> <span data-ttu-id="82948-178"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="82948-178"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="82948-179">Vea también</span><span class="sxs-lookup"><span data-stu-id="82948-179">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82948-180">IDelaydC</span><span class="sxs-lookup"><span data-stu-id="82948-180">IDelaydC</span></span>](idelaydc.md)
</dt> <dt>

[<span data-ttu-id="82948-181">IDelaydC:: configure</span><span class="sxs-lookup"><span data-stu-id="82948-181">IDelaydC::Configure</span></span>](idelaydc-configure.md)
</dt> <dt>

[<span data-ttu-id="82948-182">IDelaydC::D Ulta</span><span class="sxs-lookup"><span data-stu-id="82948-182">IDelaydC::Disconnect</span></span>](idelaydc-disconnect.md)
</dt> <dt>

[<span data-ttu-id="82948-183">IDelaydC:: Start</span><span class="sxs-lookup"><span data-stu-id="82948-183">IDelaydC::Start</span></span>](idelaydc-start.md)
</dt> </dl>

 

 




