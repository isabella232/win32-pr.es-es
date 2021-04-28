---
description: 'Método IStats::Connect: el método Connect conecta el NPP a la red mediante una NIC especificada y proporciona información de configuración para la conexión.'
ms.assetid: 29a12df7-9c81-40ff-ac12-33ce1de833b1
title: Método IStats::Connect (Netmon.h)
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
ms.openlocfilehash: 0719b6ff56aaa8c0be02f86d62ac23d4003aa3d6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098483"
---
# <a name="istatsconnect-method"></a><span data-ttu-id="7ce6e-103">IStats::Connect (método)</span><span class="sxs-lookup"><span data-stu-id="7ce6e-103">IStats::Connect method</span></span>

<span data-ttu-id="7ce6e-104">El **método Connect** conecta el NPP a la red mediante una NIC especificada y proporciona información de configuración para la conexión.</span><span class="sxs-lookup"><span data-stu-id="7ce6e-104">The **Connect** method connects the NPP to the network by using a specified NIC and provides configuration information for the connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ce6e-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7ce6e-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Connect(
  [in]  HBLOB  hInputBlob,
  [in]  LPVOID StatusCallbackProc,
  [in]  LPVOID UserContext,
  [out] HBLOB  hErrorBlob
);
```



## <a name="parameters"></a><span data-ttu-id="7ce6e-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7ce6e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7ce6e-107">*hInputBlob* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="7ce6e-107">*hInputBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7ce6e-108">Controle el BLOB que especifica la NIC a la que se conecta el NPP y la información de configuración de esa conexión.</span><span class="sxs-lookup"><span data-stu-id="7ce6e-108">Handle to the BLOB that specifies the NIC that the NPP connects to and the configuration information for that connection.</span></span>

</dd> <dt>

<span data-ttu-id="7ce6e-109">*StatusCallbackProc* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="7ce6e-109">*StatusCallbackProc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7ce6e-110">Dirección de la función de devolución de llamada del usuario, que recibe actualizaciones de estado como desencadenadores.</span><span class="sxs-lookup"><span data-stu-id="7ce6e-110">Address of the user's callback function, which receives status updates such as triggers.</span></span> <span data-ttu-id="7ce6e-111">Si no se usa una función de devolución de llamada, establezca este parámetro y el *parámetro UserContext* en **NULL.**</span><span class="sxs-lookup"><span data-stu-id="7ce6e-111">If a callback function is not used, set this parameter and the *UserContext* parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="7ce6e-112">*UserContext* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="7ce6e-112">*UserContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7ce6e-113">Valor pasado cuando se llama a la función de devolución de llamada del usuario.</span><span class="sxs-lookup"><span data-stu-id="7ce6e-113">Value passed when the user's callback function is called.</span></span> <span data-ttu-id="7ce6e-114">El valor de este parámetro suele ser HWND o un puntero "this".</span><span class="sxs-lookup"><span data-stu-id="7ce6e-114">The value of this parameter is typically either HWND or a 'this' pointer.</span></span> <span data-ttu-id="7ce6e-115">Si no se especifica una función de devolución de llamada, establezca este parámetro y el *parámetro StatusCallbackProc* en **NULL.**</span><span class="sxs-lookup"><span data-stu-id="7ce6e-115">If a callback function is not specified, set this parameter and the *StatusCallbackProc* parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="7ce6e-116">*hErrorBlob* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="7ce6e-116">*hErrorBlob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7ce6e-117">Controlar un blob de error que contiene información de error adicional.</span><span class="sxs-lookup"><span data-stu-id="7ce6e-117">Handle to an error BLOB that contains additional error information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7ce6e-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7ce6e-118">Return value</span></span>

<span data-ttu-id="7ce6e-119">Si el método es correcto, el valor devuelto es NMERR \_ SUCCESS.</span><span class="sxs-lookup"><span data-stu-id="7ce6e-119">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="7ce6e-120">Si el método no es correcto, el valor devuelto es uno de los siguientes códigos de error (que incluyen los errores devueltos por la llamada **interna IStats::Configure):**</span><span class="sxs-lookup"><span data-stu-id="7ce6e-120">If the method is unsuccessful, the return value is one of the following error codes (which include those errors returned by the internal **IStats::Configure** call):</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7ce6e-121">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="7ce6e-121">Return code</span></span></th>
<th><span data-ttu-id="7ce6e-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="7ce6e-122">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><dl> <span data-ttu-id="7ce6e-123"><dt><strong>NMERR_ALREADY_CONNECTED</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="7ce6e-123"><dt><strong>NMERR_ALREADY_CONNECTED</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="7ce6e-124">Esta instancia del objeto COM de NPP ya está conectada a la red.</span><span class="sxs-lookup"><span data-stu-id="7ce6e-124">This instance of the NPP COM object is already connected to the network.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="7ce6e-125"><dt><strong>NMERR_BLOB_CONVERSION_ERROR</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="7ce6e-125"><dt><strong>NMERR_BLOB_CONVERSION_ERROR</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="7ce6e-126">El BLOB de configuración está dañado.</span><span class="sxs-lookup"><span data-stu-id="7ce6e-126">The configuration BLOB is corrupt.</span></span> <span data-ttu-id="7ce6e-127">La llamada a <strong>IStats::Configure</strong> genera este error.</span><span class="sxs-lookup"><span data-stu-id="7ce6e-127">This error is generated by the <strong>IStats::Configure</strong> call.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="7ce6e-128"><dt><strong>NMERR_BLOB_ENTRY_DOES_NOT_EXIST</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="7ce6e-128"><dt><strong>NMERR_BLOB_ENTRY_DOES_NOT_EXIST</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="7ce6e-129">El BLOB de entrada especificado por el <em>parámetro hInputBlob</em> carece de una entrada necesaria para realizar esta operación.</span><span class="sxs-lookup"><span data-stu-id="7ce6e-129">The input BLOB specified by the <em>hInputBlob</em> parameter lacks an entry needed to perform this operation.</span></span> <span data-ttu-id="7ce6e-130">Este error puede generarse mediante la <strong>llamada IStats::Connect</strong> o <strong>IStats::Configure.</strong></span><span class="sxs-lookup"><span data-stu-id="7ce6e-130">This error might be generated by the <strong>IStats::Connect</strong> or <strong>IStats::Configure</strong> call.</span></span> <span data-ttu-id="7ce6e-131">Mire el blob de error devuelto por <em>hErrorBlob para</em> determinar qué entrada no se encontró.</span><span class="sxs-lookup"><span data-stu-id="7ce6e-131">Look at the error BLOB returned by <em>hErrorBlob</em> to determine which entry was not found.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="7ce6e-132"><dt><strong>NMERR_BLOB_NOT_INITIALIZED</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="7ce6e-132"><dt><strong>NMERR_BLOB_NOT_INITIALIZED</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="7ce6e-133">No se ha llamado a la función <strong>CreateBlob.</strong></span><span class="sxs-lookup"><span data-stu-id="7ce6e-133">The <strong>CreateBlob</strong> function has not been called.</span></span> <span data-ttu-id="7ce6e-134">La llamada a <strong>IStats::Configure</strong> genera este error.</span><span class="sxs-lookup"><span data-stu-id="7ce6e-134">This error is generated by the <strong>IStats::Configure</strong> call.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="7ce6e-135"><dt><strong>NMERR_BLOB_STRING_INVALID</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="7ce6e-135"><dt><strong>NMERR_BLOB_STRING_INVALID</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="7ce6e-136">La cadena no termina en NULL.</span><span class="sxs-lookup"><span data-stu-id="7ce6e-136">The string is not null-terminated.</span></span> <span data-ttu-id="7ce6e-137">La llamada a <strong>IStats::Configure</strong> genera este error.</span><span class="sxs-lookup"><span data-stu-id="7ce6e-137">This error is generated by the <strong>IStats::Configure</strong> call.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="7ce6e-138"><dt><strong>NMERR_ILLEGAL_TRIGGER</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="7ce6e-138"><dt><strong>NMERR_ILLEGAL_TRIGGER</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="7ce6e-139">La parte del desencadenador del BLOB de entrada está dañada.</span><span class="sxs-lookup"><span data-stu-id="7ce6e-139">The trigger portion of the input BLOB is corrupt.</span></span> <span data-ttu-id="7ce6e-140">La llamada a <strong>IStats::Configure</strong> genera este error.</span><span class="sxs-lookup"><span data-stu-id="7ce6e-140">This error is generated by the <strong>IStats::Configure</strong> call.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="7ce6e-141"><dt><strong>NMERR_INVALID_BLOB</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="7ce6e-141"><dt><strong>NMERR_INVALID_BLOB</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="7ce6e-142">El objeto especificado en <em>hInputBlob</em> no es un BLOB.</span><span class="sxs-lookup"><span data-stu-id="7ce6e-142">The object specified in <em>hInputBlob</em> is not a BLOB.</span></span> <span data-ttu-id="7ce6e-143">La llamada a <strong>IStats::Configure</strong> genera este error.</span><span class="sxs-lookup"><span data-stu-id="7ce6e-143">This error is generated by the <strong>IStats::Configure</strong> call.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="7ce6e-144"><dt><strong>NMERR_NO_DEFAULT_CAPTURE_DIRECTORY</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="7ce6e-144"><dt><strong>NMERR_NO_DEFAULT_CAPTURE_DIRECTORY</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="7ce6e-145">El directorio de captura predeterminado no se estableció en el Registro.</span><span class="sxs-lookup"><span data-stu-id="7ce6e-145">The default capture directory was not set in the registry.</span></span> <span data-ttu-id="7ce6e-146">Para establecer el directorio de captura, use la ruta de acceso siguiente.</span><span class="sxs-lookup"><span data-stu-id="7ce6e-146">To set the capture directory, use the following path.</span></span> <br/>
<pre class="syntax" data-space="preserve"><code>HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\nm\Parameters\CapturePath</code></pre></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="7ce6e-147"><dt><strong>NMERR_OUT_OF_MEMORY</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="7ce6e-147"><dt><strong>NMERR_OUT_OF_MEMORY</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="7ce6e-148">La memoria necesaria para realizar esta operación no estaba disponible.</span><span class="sxs-lookup"><span data-stu-id="7ce6e-148">The memory required to perform this operation was unavailable.</span></span> <span data-ttu-id="7ce6e-149">La llamada a <strong>IStats::Configure</strong> genera este error.</span><span class="sxs-lookup"><span data-stu-id="7ce6e-149">This error is generated by the <strong>IStats::Configure</strong> call.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="7ce6e-150"><dt><strong>NMERR_TIMEOUT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="7ce6e-150"><dt><strong>NMERR_TIMEOUT</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="7ce6e-151">Se ha pasado el tiempo de espera de la solicitud. La llamada a <strong>IStats::Configure</strong> genera este error.</span><span class="sxs-lookup"><span data-stu-id="7ce6e-151">The request has timed out. This error is generated by the <strong>IStats::Configure</strong> call.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="7ce6e-152"><dt><strong>NMERR_UPLEVEL_BLOB</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="7ce6e-152"><dt><strong>NMERR_UPLEVEL_BLOB</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="7ce6e-153">El número de versión del BLOB especificado en <em>hInputBlob</em> es incorrecto.</span><span class="sxs-lookup"><span data-stu-id="7ce6e-153">The version number of the BLOB specified in <em>hInputBlob</em> is incorrect.</span></span> <span data-ttu-id="7ce6e-154">La llamada a <strong>IStats::Configure</strong> genera este error.</span><span class="sxs-lookup"><span data-stu-id="7ce6e-154">This error is generated by the <strong>IStats::Configure</strong> call.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="7ce6e-155">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7ce6e-155">Remarks</span></span>

<span data-ttu-id="7ce6e-156">Cuando se llama al método **Connect,** Monitor de red llama automáticamente al método **IStats::Configure** mediante el blob proporcionado por el *parámetro hInputBlob.*</span><span class="sxs-lookup"><span data-stu-id="7ce6e-156">When the **Connect** method is called, Network Monitor automatically calls the **IStats::Configure** method by using the BLOB provided by the *hInputBlob* parameter.</span></span> <span data-ttu-id="7ce6e-157">Tenga en cuenta que los códigos de error devueltos por la llamada a **IStats::Configure** se devuelven y devuelven mediante la **llamada IStats::Connect.**</span><span class="sxs-lookup"><span data-stu-id="7ce6e-157">Note that any error codes returned by the call to **IStats::Configure** are passed back and returned by the **IStats::Connect** call.</span></span>

<span data-ttu-id="7ce6e-158">Se debe llamar a este método para poder empezar a capturar fotogramas.</span><span class="sxs-lookup"><span data-stu-id="7ce6e-158">This method must be called before you can start capturing frames.</span></span> <span data-ttu-id="7ce6e-159">Tenga en cuenta que cuando se conecta a la red mediante este método, debe seguir usando la **interfaz IStats** para capturar fotogramas.</span><span class="sxs-lookup"><span data-stu-id="7ce6e-159">Note that when you connect to the network by using this method, you must continue to use the **IStats** interface to capture frames.</span></span>

<span data-ttu-id="7ce6e-160">El BLOB de entrada especificado por *hInputBlob* se puede obtener llamando a los métodos **GetNPPBlobFromUI**, **GetNPPBlobTable** y **SelectNPPBlobFromTable.**</span><span class="sxs-lookup"><span data-stu-id="7ce6e-160">The input BLOB specified by *hInputBlob* can be obtained by calling the **GetNPPBlobFromUI**, **GetNPPBlobTable**, and **SelectNPPBlobFromTable** methods.</span></span>

<span data-ttu-id="7ce6e-161">El blob de error devuelto por el parámetro *hErrorBlob* contiene entradas que Monitor de red no se pudieron comprender o encontrar en el BLOB de entrada especificado en *hInputBlob*.</span><span class="sxs-lookup"><span data-stu-id="7ce6e-161">The error BLOB returned by the *hErrorBlob* parameter contains entries that Network Monitor could not understand or find in the input BLOB specified in *hInputBlob*.</span></span> <span data-ttu-id="7ce6e-162">El blob de error devuelto contiene información de error que la aplicación puede usar para solucionar problemas.</span><span class="sxs-lookup"><span data-stu-id="7ce6e-162">The returned error BLOB contains error information that the application can use for troubleshooting.</span></span> <span data-ttu-id="7ce6e-163">Por ejemplo, si se devuelve NMERR BLOB ENTRY DOES NOT EXIST, la entrada que no Monitor de red encuentra se incluye en el \_ \_ blob de error \_ \_ \_ devuelto.</span><span class="sxs-lookup"><span data-stu-id="7ce6e-163">For example, if NMERR\_BLOB\_ENTRY\_DOES\_NOT\_EXIST is returned, the entry that Network Monitor could not find is included in the returned error BLOB.</span></span>



| <span data-ttu-id="7ce6e-164">Para información acerca de</span><span class="sxs-lookup"><span data-stu-id="7ce6e-164">For information about</span></span>                                             | <span data-ttu-id="7ce6e-165">Vea</span><span class="sxs-lookup"><span data-stu-id="7ce6e-165">See</span></span>                                                                          |
|-------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="7ce6e-166">Obtención del BLOB de entrada que representa una tarjeta de interfaz de red</span><span class="sxs-lookup"><span data-stu-id="7ce6e-166">Obtaining the input BLOB that represents a network interface card</span></span> | [<span data-ttu-id="7ce6e-167">Selección de una tarjeta de interfaz de red</span><span class="sxs-lookup"><span data-stu-id="7ce6e-167">Selecting a Network Interface Card</span></span>](selecting-a-network-interface-card.md) |



 

## <a name="requirements"></a><span data-ttu-id="7ce6e-168">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7ce6e-168">Requirements</span></span>



| <span data-ttu-id="7ce6e-169">Requisito</span><span class="sxs-lookup"><span data-stu-id="7ce6e-169">Requirement</span></span> | <span data-ttu-id="7ce6e-170">Valor</span><span class="sxs-lookup"><span data-stu-id="7ce6e-170">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7ce6e-171">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7ce6e-171">Minimum supported client</span></span><br/> | <span data-ttu-id="7ce6e-172">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="7ce6e-172">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="7ce6e-173">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7ce6e-173">Minimum supported server</span></span><br/> | <span data-ttu-id="7ce6e-174">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="7ce6e-174">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="7ce6e-175">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7ce6e-175">Header</span></span><br/>                   | <dl> <span data-ttu-id="7ce6e-176"><dt>Netmon.h</dt></span><span class="sxs-lookup"><span data-stu-id="7ce6e-176"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="7ce6e-177">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="7ce6e-177">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7ce6e-178"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7ce6e-178"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7ce6e-179">Consulte también</span><span class="sxs-lookup"><span data-stu-id="7ce6e-179">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ce6e-180">IStats</span><span class="sxs-lookup"><span data-stu-id="7ce6e-180">IStats</span></span>](istats.md)
</dt> <dt>

[<span data-ttu-id="7ce6e-181">IStats::Configure</span><span class="sxs-lookup"><span data-stu-id="7ce6e-181">IStats::Configure</span></span>](istats-configure.md)
</dt> <dt>

[<span data-ttu-id="7ce6e-182">IStats::D isconnect</span><span class="sxs-lookup"><span data-stu-id="7ce6e-182">IStats::Disconnect</span></span>](istats-disconnect.md)
</dt> <dt>

[<span data-ttu-id="7ce6e-183">Monitor de red BLOBS</span><span class="sxs-lookup"><span data-stu-id="7ce6e-183">Network Monitor BLOBS</span></span>](network-monitor-blobs.md)
</dt> </dl>

 

 




