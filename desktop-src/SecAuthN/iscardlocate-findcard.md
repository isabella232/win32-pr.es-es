---
description: El método FindCard busca la tarjeta inteligente y abre una conexión válida con ella.
ms.assetid: ab97eff2-0f41-4a6f-98b3-d5ad5883fa07
title: 'ISCardLocate:: FindCard (método) (Scardmgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardLocate.FindCard
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: bf3cf05ff6e6040d5cac2bde161fa2eea07d5297
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105648371"
---
# <a name="iscardlocatefindcard-method"></a><span data-ttu-id="7021b-103">ISCardLocate:: FindCard (método)</span><span class="sxs-lookup"><span data-stu-id="7021b-103">ISCardLocate::FindCard method</span></span>

<span data-ttu-id="7021b-104">\[El método **FindCard** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="7021b-104">\[The **FindCard** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="7021b-105">No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="7021b-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="7021b-106">Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="7021b-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="7021b-107">El método **FindCard** busca la [*tarjeta inteligente*](../secgloss/s-gly.md) y abre una conexión válida con ella.</span><span class="sxs-lookup"><span data-stu-id="7021b-107">The **FindCard** method searches for the [*smart card*](../secgloss/s-gly.md) and opens a valid connection to it.</span></span>

## <a name="syntax"></a><span data-ttu-id="7021b-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7021b-108">Syntax</span></span>


```C++
HRESULT FindCard(
  [in]  SCARD_SHARE_MODES ShareMode,
  [in]  SCARD_PROTOCOLS   Protocols,
  [in]  LONG              lFlags,
  [out] LPSCARDINFO       *ppCardInfo
);
```



## <a name="parameters"></a><span data-ttu-id="7021b-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7021b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7021b-110">*ShareMode* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="7021b-110">*ShareMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7021b-111">Modo en el que se va a compartir o no la tarjeta inteligente cuando se abre una conexión a ella.</span><span class="sxs-lookup"><span data-stu-id="7021b-111">Mode in which to share or not share the smart card when a connection is opened to it.</span></span>



| <span data-ttu-id="7021b-112">Value</span><span class="sxs-lookup"><span data-stu-id="7021b-112">Value</span></span>                                                                                                                                            | <span data-ttu-id="7021b-113">Significado</span><span class="sxs-lookup"><span data-stu-id="7021b-113">Meaning</span></span>                                                       |
|--------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span id="EXCLUSIVE"></span><span id="exclusive"></span><dl> <span data-ttu-id="7021b-114"><dt>**ÚNICO**</dt></span><span class="sxs-lookup"><span data-stu-id="7021b-114"><dt>**EXCLUSIVE**</dt></span></span> </dl> | <span data-ttu-id="7021b-115">Nadie más usa esta conexión con la tarjeta inteligente.</span><span class="sxs-lookup"><span data-stu-id="7021b-115">No one else use this connection to the smart card.</span></span><br/> |
| <span id="SHARED"></span><span id="shared"></span><dl> <span data-ttu-id="7021b-116"><dt>**RECURSO**</dt></span><span class="sxs-lookup"><span data-stu-id="7021b-116"><dt>**SHARED**</dt></span></span> </dl>          | <span data-ttu-id="7021b-117">Otras aplicaciones pueden usar esta conexión.</span><span class="sxs-lookup"><span data-stu-id="7021b-117">Other applications can use this connection.</span></span><br/>        |



 

</dd> <dt>

<span data-ttu-id="7021b-118">*Protocolos* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="7021b-118">*Protocols* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7021b-119">Protocolo que se utilizará al conectarse a la tarjeta.</span><span class="sxs-lookup"><span data-stu-id="7021b-119">Protocol to use when connecting to the card.</span></span>

<span data-ttu-id="7021b-120">T0</span><span class="sxs-lookup"><span data-stu-id="7021b-120">T0</span></span>

<span data-ttu-id="7021b-121">T1</span><span class="sxs-lookup"><span data-stu-id="7021b-121">T1</span></span>

<span data-ttu-id="7021b-122">RAW</span><span class="sxs-lookup"><span data-stu-id="7021b-122">RAW</span></span>

<span data-ttu-id="7021b-123">T0 \| T1</span><span class="sxs-lookup"><span data-stu-id="7021b-123">T0\|T1</span></span>

</dd> <dt>

<span data-ttu-id="7021b-124">*lFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="7021b-124">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7021b-125">Especifica cuándo se muestra la [*interfaz de usuario*](../secgloss/u-gly.md) :</span><span class="sxs-lookup"><span data-stu-id="7021b-125">Specifies when [*user interface*](../secgloss/u-gly.md) is displayed:</span></span>



| <span data-ttu-id="7021b-126">Value</span><span class="sxs-lookup"><span data-stu-id="7021b-126">Value</span></span>                                                                                                                                                                       | <span data-ttu-id="7021b-127">Significado</span><span class="sxs-lookup"><span data-stu-id="7021b-127">Meaning</span></span>                                                                                                                                                                                                                                                                                                                             |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SC_DLG_MINIMAL_UI"></span><span id="sc_dlg_minimal_ui"></span><dl> <span data-ttu-id="7021b-128"><dt>**\_interfaz de \_ \_ usuario mínima de SC Dlg**</dt></span><span class="sxs-lookup"><span data-stu-id="7021b-128"><dt>**SC\_DLG\_MINIMAL\_UI**</dt></span></span> </dl> | <span data-ttu-id="7021b-129">Muestra el cuadro de diálogo solo si la tarjeta que se está buscando en la aplicación que realiza la llamada no está ubicada y disponible para su uso en un lector.</span><span class="sxs-lookup"><span data-stu-id="7021b-129">Displays the dialog box only if the card being searched for by the calling application is not located and available for use in a reader.</span></span> <span data-ttu-id="7021b-130">Esto permite que la tarjeta se encuentre, conectada (ya sea a través de un mecanismo de cuadros de diálogo interno o mediante las funciones de devolución de llamada de usuario) y se devuelva a la aplicación que realiza la llamada.</span><span class="sxs-lookup"><span data-stu-id="7021b-130">This allows the card to be found, connected (either through an internal dialog box mechanism or by using the user callback functions), and returned to the calling application.</span></span><br/> |
| <span id="SC_DLG_NO_UI"></span><span id="sc_dlg_no_ui"></span><dl> <span data-ttu-id="7021b-131"><dt>**SC \_ Dlg \_ sin \_ interfaz de usuario**</dt></span><span class="sxs-lookup"><span data-stu-id="7021b-131"><dt>**SC\_DLG\_NO\_UI**</dt></span></span> </dl>                | <span data-ttu-id="7021b-132">No provoca ninguna presentación de la interfaz de usuario, independientemente del resultado de la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="7021b-132">Causes no UI display, regardless of the search outcome.</span></span><br/>                                                                                                                                                                                                                                                                  |
| <span id="SC_DLG_FORCE_UI"></span><span id="sc_dlg_force_ui"></span><dl> <span data-ttu-id="7021b-133"><dt>**fuerza de IU de SC \_ Dlg \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="7021b-133"><dt>**SC\_DLG\_FORCE\_UI**</dt></span></span> </dl>       | <span data-ttu-id="7021b-134">Provoca la presentación de la interfaz de usuario independientemente del resultado de la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="7021b-134">Causes UI display regardless of the search outcome.</span></span><br/>                                                                                                                                                                                                                                                                      |



 

</dd> <dt>

<span data-ttu-id="7021b-135">*ppCardInfo* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="7021b-135">*ppCardInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7021b-136">Puntero a un puntero a una estructura de datos que contiene o devuelve información acerca de la [*tarjeta inteligente*](../secgloss/s-gly.md)abierta, si se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="7021b-136">Pointer to a pointer to a data structure that contains or returns information about the opened [*smart card*](../secgloss/s-gly.md), if successful.</span></span> <span data-ttu-id="7021b-137">Será **null** si se produce un error en la operación.</span><span class="sxs-lookup"><span data-stu-id="7021b-137">Will be **NULL** if operation has failed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7021b-138">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7021b-138">Return value</span></span>

<span data-ttu-id="7021b-139">El método devuelve uno de los siguientes valores posibles.</span><span class="sxs-lookup"><span data-stu-id="7021b-139">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="7021b-140">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="7021b-140">Return code</span></span>                                                                                   | <span data-ttu-id="7021b-141">Descripción</span><span class="sxs-lookup"><span data-stu-id="7021b-141">Description</span></span>                                          |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="7021b-142"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="7021b-142"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="7021b-143">Operación completada correctamente.</span><span class="sxs-lookup"><span data-stu-id="7021b-143">Operation completed successfully.</span></span><br/>         |
| <dl> <span data-ttu-id="7021b-144"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="7021b-144"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="7021b-145">Parámetro no válido.</span><span class="sxs-lookup"><span data-stu-id="7021b-145">Invalid parameter.</span></span><br/>                        |
| <dl> <span data-ttu-id="7021b-146"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="7021b-146"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="7021b-147">Se pasó un puntero no válido en *ppCardInfo*.</span><span class="sxs-lookup"><span data-stu-id="7021b-147">A bad pointer was passed in *ppCardInfo*.</span></span><br/> |
| <dl> <span data-ttu-id="7021b-148"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="7021b-148"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="7021b-149">Memoria insuficiente</span><span class="sxs-lookup"><span data-stu-id="7021b-149">Out of memory.</span></span><br/>                            |



 

## <a name="remarks"></a><span data-ttu-id="7021b-150">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7021b-150">Remarks</span></span>

<span data-ttu-id="7021b-151">Para establecer los criterios de búsqueda de la búsqueda, llame a [**ConfigureCardNameSearch**](iscardlocate-configurecardnamesearch.md) para especificar los nombres de tarjeta de una tarjeta inteligente.</span><span class="sxs-lookup"><span data-stu-id="7021b-151">To set the search criteria of the search, call [**ConfigureCardNameSearch**](iscardlocate-configurecardnamesearch.md) to specify a smart card's card names.</span></span>

<span data-ttu-id="7021b-152">Para obtener una lista de todos los métodos proporcionados por esta interfaz, vea [**ISCardLocate**](iscardlocate.md).</span><span class="sxs-lookup"><span data-stu-id="7021b-152">For a list of all the methods provided by this interface, see [**ISCardLocate**](iscardlocate.md).</span></span>

<span data-ttu-id="7021b-153">Además de los códigos de error COM enumerados anteriormente, esta interfaz puede devolver un código de error de tarjeta inteligente si se llamó a una función de tarjeta inteligente para completar la solicitud.</span><span class="sxs-lookup"><span data-stu-id="7021b-153">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="7021b-154">Para obtener más información, vea [valores devueltos de tarjeta inteligente](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="7021b-154">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7021b-155">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7021b-155">Requirements</span></span>



| <span data-ttu-id="7021b-156">Requisito</span><span class="sxs-lookup"><span data-stu-id="7021b-156">Requirement</span></span> | <span data-ttu-id="7021b-157">Value</span><span class="sxs-lookup"><span data-stu-id="7021b-157">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7021b-158">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7021b-158">Minimum supported client</span></span><br/> | <span data-ttu-id="7021b-159">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="7021b-159">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="7021b-160">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7021b-160">Minimum supported server</span></span><br/> | <span data-ttu-id="7021b-161">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="7021b-161">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="7021b-162">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="7021b-162">End of client support</span></span><br/>    | <span data-ttu-id="7021b-163">Windows XP</span><span class="sxs-lookup"><span data-stu-id="7021b-163">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="7021b-164">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="7021b-164">End of server support</span></span><br/>    | <span data-ttu-id="7021b-165">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="7021b-165">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="7021b-166">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7021b-166">Header</span></span><br/>                   | <dl> <span data-ttu-id="7021b-167"><dt>Scardmgr. h</dt></span><span class="sxs-lookup"><span data-stu-id="7021b-167"><dt>Scardmgr.h</dt></span></span> </dl>   |
| <span data-ttu-id="7021b-168">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="7021b-168">Type library</span></span><br/>             | <dl> <span data-ttu-id="7021b-169"><dt>Scardmgr. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="7021b-169"><dt>Scardmgr.tlb</dt></span></span> </dl> |
| <span data-ttu-id="7021b-170">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="7021b-170">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7021b-171"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7021b-171"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="7021b-172">IID</span><span class="sxs-lookup"><span data-stu-id="7021b-172">IID</span></span><br/>                      | <span data-ttu-id="7021b-173">IID \_ ISCardLocate se define como 1461AACD-6810-11D0-918F-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="7021b-173">IID\_ISCardLocate is defined as 1461AACD-6810-11D0-918F-00AA00C18068</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="7021b-174">Vea también</span><span class="sxs-lookup"><span data-stu-id="7021b-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7021b-175">**ConfigureCardNameSearch**</span><span class="sxs-lookup"><span data-stu-id="7021b-175">**ConfigureCardNameSearch**</span></span>](iscardlocate-configurecardnamesearch.md)
</dt> <dt>

[<span data-ttu-id="7021b-176">**ISCardLocate**</span><span class="sxs-lookup"><span data-stu-id="7021b-176">**ISCardLocate**</span></span>](iscardlocate.md)
</dt> </dl>

 

 
