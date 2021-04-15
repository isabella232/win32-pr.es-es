---
description: El método SetBandwidthInfo establece la información de ancho de banda.
ms.assetid: bf5db456-ea67-4a65-a681-df0741f73fc9
title: 'ITConnection:: SetBandwidthInfo (método) (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c17054743f6d47775e994dbfe3b80c7afe1ab68
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690198"
---
# <a name="itconnectionsetbandwidthinfo-method"></a><span data-ttu-id="8e6cb-103">ITConnection:: SetBandwidthInfo (método)</span><span class="sxs-lookup"><span data-stu-id="8e6cb-103">ITConnection::SetBandwidthInfo method</span></span>

<span data-ttu-id="8e6cb-104">\[ Las interfaces y controles de conferencias de telefonía IP de encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y las versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="8e6cb-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="8e6cb-105">La API de cliente de RTC proporciona una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="8e6cb-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="8e6cb-106">El método **SetBandwidthInfo** establece la información de ancho de banda.</span><span class="sxs-lookup"><span data-stu-id="8e6cb-106">The **SetBandwidthInfo** method sets the bandwidth information.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e6cb-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8e6cb-107">Syntax</span></span>


```C++
HRESULT SetBandwidthInfo(
  [in] BSTR   pModifier,
  [in] DOUBLE Bandwidth
);
```



## <a name="parameters"></a><span data-ttu-id="8e6cb-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8e6cb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8e6cb-109">*pModifier* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8e6cb-109">*pModifier* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8e6cb-110">Puntero a un **BSTR** que indica el ámbito del ancho de banda que se establece.</span><span class="sxs-lookup"><span data-stu-id="8e6cb-110">Pointer to a **BSTR** indicating the scope of the bandwidth being set.</span></span> <span data-ttu-id="8e6cb-111">Para obtener más información, vea la sección Comentarios que se muestra más adelante.</span><span class="sxs-lookup"><span data-stu-id="8e6cb-111">For more information, see the following Remarks section.</span></span>

</dd> <dt>

<span data-ttu-id="8e6cb-112">*Ancho de banda* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8e6cb-112">*Bandwidth* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8e6cb-113">Consumo.</span><span class="sxs-lookup"><span data-stu-id="8e6cb-113">Bandwidth.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8e6cb-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8e6cb-114">Return value</span></span>

<span data-ttu-id="8e6cb-115">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="8e6cb-115">This method can return one of these values.</span></span>



| <span data-ttu-id="8e6cb-116">Value</span><span class="sxs-lookup"><span data-stu-id="8e6cb-116">Value</span></span>                                                                                         | <span data-ttu-id="8e6cb-117">Significado</span><span class="sxs-lookup"><span data-stu-id="8e6cb-117">Meaning</span></span>                                                           |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| <dl> <span data-ttu-id="8e6cb-118"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="8e6cb-118"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="8e6cb-119">El método se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="8e6cb-119">Method succeeded.</span></span><br/>                                      |
| <dl> <span data-ttu-id="8e6cb-120"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="8e6cb-120"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="8e6cb-121">El parámetro *pModifier* o *Bandwidth* no es válido.</span><span class="sxs-lookup"><span data-stu-id="8e6cb-121">The *pModifier* or *Bandwidth* parameter is not valid.</span></span><br/> |
| <dl> <span data-ttu-id="8e6cb-122"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="8e6cb-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="8e6cb-123">No hay memoria suficiente para realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="8e6cb-123">Insufficient memory exists to perform the operation.</span></span><br/>   |
| <dl> <span data-ttu-id="8e6cb-124"><dt>**E \_ FAIL**</dt></span><span class="sxs-lookup"><span data-stu-id="8e6cb-124"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="8e6cb-125">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="8e6cb-125">Unspecified error.</span></span><br/>                                     |
| <dl> <span data-ttu-id="8e6cb-126"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="8e6cb-126"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="8e6cb-127">Este método aún no se ha implementado.</span><span class="sxs-lookup"><span data-stu-id="8e6cb-127">This method is not yet implemented.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="8e6cb-128">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8e6cb-128">Remarks</span></span>

<span data-ttu-id="8e6cb-129">La aplicación debe usar [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) para asignar memoria para el parámetro *PModifier* y usar [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) para liberar memoria cuando la variable ya no se necesite.</span><span class="sxs-lookup"><span data-stu-id="8e6cb-129">The application must use [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) to allocate memory for the *pModifier* parameter and use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory when the variable is no longer needed.</span></span>

<span data-ttu-id="8e6cb-130">Referencia: RFC 2327.</span><span class="sxs-lookup"><span data-stu-id="8e6cb-130">Reference: RFC 2327.</span></span>

<span data-ttu-id="8e6cb-131">Normalmente, el modificador de ancho de banda será CT o como:</span><span class="sxs-lookup"><span data-stu-id="8e6cb-131">The bandwidth modifier will normally be either CT or AS:</span></span>

<span data-ttu-id="8e6cb-132">**Total de la Conferencia CT:** Un ancho de banda máximo implícito se asocia a cada [*período*](t-tapgloss.md) de vida (TTL) en MBONE o en una región de ámbito administrativo de multidifusión determinada (las preguntas más frecuentes sobre el ancho de banda de MBONE en comparación con los límites de TTL).</span><span class="sxs-lookup"><span data-stu-id="8e6cb-132">**CT Conference Total:** An implicit maximum bandwidth is associated with each [*time to live*](t-tapgloss.md) (TTL) on the Mbone or within a particular multicast administrative scope region (the Mbone bandwidth versus TTL limits are given in the MBone FAQ).</span></span> <span data-ttu-id="8e6cb-133">Si el ancho de banda de una sesión o un medio en una sesión es diferente del ancho de banda implícito del ámbito, a \` b = CT:... debe proporcionarse la línea para la sesión y proporcionar el límite superior propuesto al ancho de banda usado.</span><span class="sxs-lookup"><span data-stu-id="8e6cb-133">If the bandwidth of a session or media in a session is different from the bandwidth implicit from the scope, a \`b=CT:...' line should be supplied for the session giving the proposed upper limit to the bandwidth used.</span></span> <span data-ttu-id="8e6cb-134">El objetivo principal de esto es dar una idea aproximada de si dos o más conferencias pueden coexistir simultáneamente.</span><span class="sxs-lookup"><span data-stu-id="8e6cb-134">The primary purpose of this is to give an approximate idea as to whether two or more conferences can coexist simultaneously.</span></span>

<span data-ttu-id="8e6cb-135">**Como Application-Specific máximo:** El ancho de banda se interpreta como específico de la aplicación, es decir, será el concepto de ancho de banda máximo de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="8e6cb-135">**AS Application-Specific Maximum:** The bandwidth is interpreted to be application-specific, i.e., will be the application's concept of maximum bandwidth.</span></span> <span data-ttu-id="8e6cb-136">Normalmente, esto coincidirá con lo que se establece en el control de "ancho de banda máximo" de la aplicación, si procede.</span><span class="sxs-lookup"><span data-stu-id="8e6cb-136">Normally this will coincide with what is set on the application's "maximum bandwidth" control, if applicable.</span></span>

<span data-ttu-id="8e6cb-137">Tenga en cuenta que CT proporciona una figura de ancho de banda total para todos los medios en todos los sitios.</span><span class="sxs-lookup"><span data-stu-id="8e6cb-137">Note that CT gives a total bandwidth figure for all the media at all sites.</span></span> <span data-ttu-id="8e6cb-138">COMO proporciona una figura de ancho de banda para un solo medio en un único sitio, aunque puede haber muchos sitios que se envíen simultáneamente.</span><span class="sxs-lookup"><span data-stu-id="8e6cb-138">AS gives a bandwidth figure for a single media at a single site, although there may be many sites sending simultaneously.</span></span>

<span data-ttu-id="8e6cb-139">**Mecanismo de extensión:** Los escritores de herramientas pueden definir modificadores de ancho de banda experimental al prefijar los modificadores con "X-".</span><span class="sxs-lookup"><span data-stu-id="8e6cb-139">**Extension Mechanism:** Tool writers can define experimental bandwidth modifiers by prefixing their modifiers with "X-".</span></span>

## <a name="requirements"></a><span data-ttu-id="8e6cb-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8e6cb-140">Requirements</span></span>



| <span data-ttu-id="8e6cb-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="8e6cb-141">Requirement</span></span> | <span data-ttu-id="8e6cb-142">Value</span><span class="sxs-lookup"><span data-stu-id="8e6cb-142">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8e6cb-143">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="8e6cb-143">TAPI version</span></span><br/> | <span data-ttu-id="8e6cb-144">Requiere TAPI 3,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="8e6cb-144">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="8e6cb-145">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8e6cb-145">Header</span></span><br/>       | <dl> <span data-ttu-id="8e6cb-146"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="8e6cb-146"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="8e6cb-147">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8e6cb-147">Library</span></span><br/>      | <dl> <span data-ttu-id="8e6cb-148"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8e6cb-148"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="8e6cb-149">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="8e6cb-149">DLL</span></span><br/>          | <dl> <span data-ttu-id="8e6cb-150"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8e6cb-150"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8e6cb-151">Vea también</span><span class="sxs-lookup"><span data-stu-id="8e6cb-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e6cb-152">**ITConnection**</span><span class="sxs-lookup"><span data-stu-id="8e6cb-152">**ITConnection**</span></span>](itconnection.md)
</dt> </dl>

 

