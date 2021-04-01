---
description: El método Connect conecta el NPP a la red mediante una NIC especificada y proporciona información de configuración para la conexión.
ms.assetid: 29a12df7-9c81-40ff-ac12-33ce1de833b1
title: 'IStas:: Connect (método) (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IStats.Connect
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 7705600c3ce68b719014c928ac4d02c62cba64cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913854"
---
# <a name="istatsconnect-method"></a><span data-ttu-id="2a16c-103">IStas:: Connect (método)</span><span class="sxs-lookup"><span data-stu-id="2a16c-103">IStats::Connect method</span></span>

<span data-ttu-id="2a16c-104">El método **Connect** conecta el NPP a la red mediante una NIC especificada y proporciona información de configuración para la conexión.</span><span class="sxs-lookup"><span data-stu-id="2a16c-104">The **Connect** method connects the NPP to the network by using a specified NIC and provides configuration information for the connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="2a16c-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2a16c-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Connect(
  [in]  HBLOB  hInputBlob,
  [in]  LPVOID StatusCallbackProc,
  [in]  LPVOID UserContext,
  [out] HBLOB  hErrorBlob
);
```



## <a name="parameters"></a><span data-ttu-id="2a16c-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2a16c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2a16c-107">*hInputBlob* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2a16c-107">*hInputBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2a16c-108">Identificador del BLOB que especifica la NIC a la que se conecta el NPP y la información de configuración para esa conexión.</span><span class="sxs-lookup"><span data-stu-id="2a16c-108">Handle to the BLOB that specifies the NIC that the NPP connects to and the configuration information for that connection.</span></span>

</dd> <dt>

<span data-ttu-id="2a16c-109">*StatusCallbackProc* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2a16c-109">*StatusCallbackProc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2a16c-110">Dirección de la función de devolución de llamada del usuario, que recibe actualizaciones de estado, como los desencadenadores.</span><span class="sxs-lookup"><span data-stu-id="2a16c-110">Address of the user's callback function, which receives status updates such as triggers.</span></span> <span data-ttu-id="2a16c-111">Si no se utiliza una función de devolución de llamada, establezca este parámetro y el parámetro *UserContext* en **null**.</span><span class="sxs-lookup"><span data-stu-id="2a16c-111">If a callback function is not used, set this parameter and the *UserContext* parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="2a16c-112">*UserContext* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2a16c-112">*UserContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2a16c-113">Valor que se pasa cuando se llama a la función de devolución de llamada del usuario.</span><span class="sxs-lookup"><span data-stu-id="2a16c-113">Value passed when the user's callback function is called.</span></span> <span data-ttu-id="2a16c-114">El valor de este parámetro suele ser HWND o un puntero ' this '.</span><span class="sxs-lookup"><span data-stu-id="2a16c-114">The value of this parameter is typically either HWND or a 'this' pointer.</span></span> <span data-ttu-id="2a16c-115">Si no se especifica una función de devolución de llamada, establezca este parámetro y el parámetro *StatusCallbackProc* en **null**.</span><span class="sxs-lookup"><span data-stu-id="2a16c-115">If a callback function is not specified, set this parameter and the *StatusCallbackProc* parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="2a16c-116">*hErrorBlob* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="2a16c-116">*hErrorBlob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2a16c-117">Identificador de un BLOB de error que contiene información de error adicional.</span><span class="sxs-lookup"><span data-stu-id="2a16c-117">Handle to an error BLOB that contains additional error information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2a16c-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2a16c-118">Return value</span></span>

<span data-ttu-id="2a16c-119">Si el método se realiza correctamente, el valor devuelto es NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="2a16c-119">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="2a16c-120">Si el método no se realiza correctamente, el valor devuelto es uno de los siguientes códigos de error (que incluyen los errores devueltos por las llamadas internas **:: configure** ):</span><span class="sxs-lookup"><span data-stu-id="2a16c-120">If the method is unsuccessful, the return value is one of the following error codes (which include those errors returned by the internal **IStats::Configure** call):</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2a16c-121">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="2a16c-121">Return code</span></span></th>
<th><span data-ttu-id="2a16c-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="2a16c-122">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><dl> <span data-ttu-id="2a16c-123"><dt><strong>NMERR_ALREADY_CONNECTED</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="2a16c-123"><dt><strong>NMERR_ALREADY_CONNECTED</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="2a16c-124">Esta instancia del objeto COM NPP ya está conectada a la red.</span><span class="sxs-lookup"><span data-stu-id="2a16c-124">This instance of the NPP COM object is already connected to the network.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="2a16c-125"><dt><strong>NMERR_BLOB_CONVERSION_ERROR</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="2a16c-125"><dt><strong>NMERR_BLOB_CONVERSION_ERROR</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="2a16c-126">El BLOB de configuración está dañado.</span><span class="sxs-lookup"><span data-stu-id="2a16c-126">The configuration BLOB is corrupt.</span></span> <span data-ttu-id="2a16c-127">Este error lo genera la llamada a la función <strong>istas:: configure</strong> .</span><span class="sxs-lookup"><span data-stu-id="2a16c-127">This error is generated by the <strong>IStats::Configure</strong> call.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="2a16c-128"><dt><strong>NMERR_BLOB_ENTRY_DOES_NOT_EXIST</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="2a16c-128"><dt><strong>NMERR_BLOB_ENTRY_DOES_NOT_EXIST</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="2a16c-129">Falta una entrada necesaria para realizar esta operación en el BLOB de entrada especificado por el parámetro <em>hInputBlob</em> .</span><span class="sxs-lookup"><span data-stu-id="2a16c-129">The input BLOB specified by the <em>hInputBlob</em> parameter lacks an entry needed to perform this operation.</span></span> <span data-ttu-id="2a16c-130">Este error lo puede generar la llamada a los <strong>istas:: Connect</strong> o <strong>istas:: configure</strong> .</span><span class="sxs-lookup"><span data-stu-id="2a16c-130">This error might be generated by the <strong>IStats::Connect</strong> or <strong>IStats::Configure</strong> call.</span></span> <span data-ttu-id="2a16c-131">Observe el BLOB de error devuelto por <em>hErrorBlob</em> para determinar qué entrada no se encontró.</span><span class="sxs-lookup"><span data-stu-id="2a16c-131">Look at the error BLOB returned by <em>hErrorBlob</em> to determine which entry was not found.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="2a16c-132"><dt><strong>NMERR_BLOB_NOT_INITIALIZED</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="2a16c-132"><dt><strong>NMERR_BLOB_NOT_INITIALIZED</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="2a16c-133">No se ha llamado a la función <strong>CreateBlob</strong> .</span><span class="sxs-lookup"><span data-stu-id="2a16c-133">The <strong>CreateBlob</strong> function has not been called.</span></span> <span data-ttu-id="2a16c-134">Este error lo genera la llamada a la función <strong>istas:: configure</strong> .</span><span class="sxs-lookup"><span data-stu-id="2a16c-134">This error is generated by the <strong>IStats::Configure</strong> call.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="2a16c-135"><dt><strong>NMERR_BLOB_STRING_INVALID</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="2a16c-135"><dt><strong>NMERR_BLOB_STRING_INVALID</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="2a16c-136">La cadena no termina en NULL.</span><span class="sxs-lookup"><span data-stu-id="2a16c-136">The string is not null-terminated.</span></span> <span data-ttu-id="2a16c-137">Este error lo genera la llamada a la función <strong>istas:: configure</strong> .</span><span class="sxs-lookup"><span data-stu-id="2a16c-137">This error is generated by the <strong>IStats::Configure</strong> call.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="2a16c-138"><dt><strong>NMERR_ILLEGAL_TRIGGER</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="2a16c-138"><dt><strong>NMERR_ILLEGAL_TRIGGER</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="2a16c-139">La parte del desencadenador del BLOB de entrada está dañada.</span><span class="sxs-lookup"><span data-stu-id="2a16c-139">The trigger portion of the input BLOB is corrupt.</span></span> <span data-ttu-id="2a16c-140">Este error lo genera la llamada a la función <strong>istas:: configure</strong> .</span><span class="sxs-lookup"><span data-stu-id="2a16c-140">This error is generated by the <strong>IStats::Configure</strong> call.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="2a16c-141"><dt><strong>NMERR_INVALID_BLOB</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="2a16c-141"><dt><strong>NMERR_INVALID_BLOB</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="2a16c-142">El objeto especificado en <em>hInputBlob</em> no es un BLOB.</span><span class="sxs-lookup"><span data-stu-id="2a16c-142">The object specified in <em>hInputBlob</em> is not a BLOB.</span></span> <span data-ttu-id="2a16c-143">Este error lo genera la llamada a la función <strong>istas:: configure</strong> .</span><span class="sxs-lookup"><span data-stu-id="2a16c-143">This error is generated by the <strong>IStats::Configure</strong> call.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="2a16c-144"><dt><strong>NMERR_NO_DEFAULT_CAPTURE_DIRECTORY</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="2a16c-144"><dt><strong>NMERR_NO_DEFAULT_CAPTURE_DIRECTORY</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="2a16c-145">No se estableció el directorio de captura predeterminado en el registro.</span><span class="sxs-lookup"><span data-stu-id="2a16c-145">The default capture directory was not set in the registry.</span></span> <span data-ttu-id="2a16c-146">Para establecer el directorio de captura, use la siguiente ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="2a16c-146">To set the capture directory, use the following path.</span></span> <br/>
<pre class="syntax" data-space="preserve"><code>HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\nm\Parameters\CapturePath</code></pre></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="2a16c-147"><dt><strong>NMERR_OUT_OF_MEMORY</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="2a16c-147"><dt><strong>NMERR_OUT_OF_MEMORY</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="2a16c-148">La memoria necesaria para realizar esta operación no estaba disponible.</span><span class="sxs-lookup"><span data-stu-id="2a16c-148">The memory required to perform this operation was unavailable.</span></span> <span data-ttu-id="2a16c-149">Este error lo genera la llamada a la función <strong>istas:: configure</strong> .</span><span class="sxs-lookup"><span data-stu-id="2a16c-149">This error is generated by the <strong>IStats::Configure</strong> call.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="2a16c-150"><dt><strong>NMERR_TIMEOUT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="2a16c-150"><dt><strong>NMERR_TIMEOUT</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="2a16c-151">La solicitud ha agotado el tiempo de espera. Este error lo genera la llamada a la función <strong>istas:: configure</strong> .</span><span class="sxs-lookup"><span data-stu-id="2a16c-151">The request has timed out. This error is generated by the <strong>IStats::Configure</strong> call.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="2a16c-152"><dt><strong>NMERR_UPLEVEL_BLOB</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="2a16c-152"><dt><strong>NMERR_UPLEVEL_BLOB</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="2a16c-153">El número de versión del BLOB especificado en <em>hInputBlob</em> es incorrecto.</span><span class="sxs-lookup"><span data-stu-id="2a16c-153">The version number of the BLOB specified in <em>hInputBlob</em> is incorrect.</span></span> <span data-ttu-id="2a16c-154">Este error lo genera la llamada a la función <strong>istas:: configure</strong> .</span><span class="sxs-lookup"><span data-stu-id="2a16c-154">This error is generated by the <strong>IStats::Configure</strong> call.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="2a16c-155">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2a16c-155">Remarks</span></span>

<span data-ttu-id="2a16c-156">Cuando se llama al método **Connect** , monitor de red llama automáticamente al método **istas:: configure** mediante el BLOB proporcionado por el parámetro *hInputBlob* .</span><span class="sxs-lookup"><span data-stu-id="2a16c-156">When the **Connect** method is called, Network Monitor automatically calls the **IStats::Configure** method by using the BLOB provided by the *hInputBlob* parameter.</span></span> <span data-ttu-id="2a16c-157">Tenga en cuenta que los códigos de error devueltos por la llamada a los **ISTA:: configure** se devuelven y se devuelven mediante la llamada a los **ISTA:: Connect** .</span><span class="sxs-lookup"><span data-stu-id="2a16c-157">Note that any error codes returned by the call to **IStats::Configure** are passed back and returned by the **IStats::Connect** call.</span></span>

<span data-ttu-id="2a16c-158">Se debe llamar a este método antes de poder iniciar la captura de fotogramas.</span><span class="sxs-lookup"><span data-stu-id="2a16c-158">This method must be called before you can start capturing frames.</span></span> <span data-ttu-id="2a16c-159">Tenga en cuenta que cuando se conecta a la red mediante este método, debe seguir usando la interfaz **istas** para capturar fotogramas.</span><span class="sxs-lookup"><span data-stu-id="2a16c-159">Note that when you connect to the network by using this method, you must continue to use the **IStats** interface to capture frames.</span></span>

<span data-ttu-id="2a16c-160">El BLOB de entrada especificado por *hInputBlob* se puede obtener llamando a los métodos **GetNPPBlobFromUI**, **GetNPPBlobTable** y **SelectNPPBlobFromTable** .</span><span class="sxs-lookup"><span data-stu-id="2a16c-160">The input BLOB specified by *hInputBlob* can be obtained by calling the **GetNPPBlobFromUI**, **GetNPPBlobTable**, and **SelectNPPBlobFromTable** methods.</span></span>

<span data-ttu-id="2a16c-161">El BLOB de error devuelto por el parámetro *hErrorBlob* contiene entradas que monitor de red no pudieron comprender o encontrar en el BLOB de entrada especificado en *hInputBlob*.</span><span class="sxs-lookup"><span data-stu-id="2a16c-161">The error BLOB returned by the *hErrorBlob* parameter contains entries that Network Monitor could not understand or find in the input BLOB specified in *hInputBlob*.</span></span> <span data-ttu-id="2a16c-162">El BLOB de error devuelto contiene información de error que la aplicación puede usar para solucionar problemas.</span><span class="sxs-lookup"><span data-stu-id="2a16c-162">The returned error BLOB contains error information that the application can use for troubleshooting.</span></span> <span data-ttu-id="2a16c-163">Por ejemplo, si \_ \_ se devuelve la entrada de BLOB NMERR \_ \_ \_ , la entrada que monitor de red no pudo encontrar se incluye en el BLOB de error devuelto.</span><span class="sxs-lookup"><span data-stu-id="2a16c-163">For example, if NMERR\_BLOB\_ENTRY\_DOES\_NOT\_EXIST is returned, the entry that Network Monitor could not find is included in the returned error BLOB.</span></span>



| <span data-ttu-id="2a16c-164">Para información acerca de</span><span class="sxs-lookup"><span data-stu-id="2a16c-164">For information about</span></span>                                             | <span data-ttu-id="2a16c-165">Vea</span><span class="sxs-lookup"><span data-stu-id="2a16c-165">See</span></span>                                                                          |
|-------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="2a16c-166">Obtener el BLOB de entrada que representa una tarjeta de interfaz de red</span><span class="sxs-lookup"><span data-stu-id="2a16c-166">Obtaining the input BLOB that represents a network interface card</span></span> | [<span data-ttu-id="2a16c-167">Seleccionar una tarjeta de interfaz de red</span><span class="sxs-lookup"><span data-stu-id="2a16c-167">Selecting a Network Interface Card</span></span>](selecting-a-network-interface-card.md) |



 

## <a name="requirements"></a><span data-ttu-id="2a16c-168">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2a16c-168">Requirements</span></span>



| <span data-ttu-id="2a16c-169">Requisito</span><span class="sxs-lookup"><span data-stu-id="2a16c-169">Requirement</span></span> | <span data-ttu-id="2a16c-170">Value</span><span class="sxs-lookup"><span data-stu-id="2a16c-170">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2a16c-171">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2a16c-171">Minimum supported client</span></span><br/> | <span data-ttu-id="2a16c-172">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="2a16c-172">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="2a16c-173">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2a16c-173">Minimum supported server</span></span><br/> | <span data-ttu-id="2a16c-174">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="2a16c-174">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="2a16c-175">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2a16c-175">Header</span></span><br/>                   | <dl> <span data-ttu-id="2a16c-176"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="2a16c-176"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="2a16c-177">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="2a16c-177">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2a16c-178"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2a16c-178"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2a16c-179">Vea también</span><span class="sxs-lookup"><span data-stu-id="2a16c-179">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a16c-180">IStas</span><span class="sxs-lookup"><span data-stu-id="2a16c-180">IStats</span></span>](istats.md)
</dt> <dt>

[<span data-ttu-id="2a16c-181">ISta:: configurar</span><span class="sxs-lookup"><span data-stu-id="2a16c-181">IStats::Configure</span></span>](istats-configure.md)
</dt> <dt>

[<span data-ttu-id="2a16c-182">IStas::D Ulta</span><span class="sxs-lookup"><span data-stu-id="2a16c-182">IStats::Disconnect</span></span>](istats-disconnect.md)
</dt> <dt>

[<span data-ttu-id="2a16c-183">BLOBs Monitor de red</span><span class="sxs-lookup"><span data-stu-id="2a16c-183">Network Monitor BLOBS</span></span>](network-monitor-blobs.md)
</dt> </dl>

 

 




