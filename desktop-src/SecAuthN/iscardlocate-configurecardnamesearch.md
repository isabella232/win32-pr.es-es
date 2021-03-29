---
description: El método ConfigureCardNameSearch especifica los nombres de tarjeta que se van a usar en la búsqueda de la tarjeta inteligente.
ms.assetid: fb406696-0cf0-4d67-8125-8888ee1b8213
title: 'ISCardLocate:: ConfigureCardNameSearch (método) (Scardmgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardLocate.ConfigureCardNameSearch
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 4af451bea1f08df2af0a673b26e84c9df2a0954b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277340"
---
# <a name="iscardlocateconfigurecardnamesearch-method"></a><span data-ttu-id="6220a-103">ISCardLocate:: ConfigureCardNameSearch (método)</span><span class="sxs-lookup"><span data-stu-id="6220a-103">ISCardLocate::ConfigureCardNameSearch method</span></span>

<span data-ttu-id="6220a-104">\[El método **ConfigureCardNameSearch** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="6220a-104">\[The **ConfigureCardNameSearch** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="6220a-105">No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="6220a-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="6220a-106">Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="6220a-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="6220a-107">El método **ConfigureCardNameSearch** especifica los nombres de tarjeta que se van a usar en la búsqueda de la [*tarjeta inteligente*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="6220a-107">The **ConfigureCardNameSearch** method specifies the card names to be used in the search for the [*smart card*](../secgloss/s-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="6220a-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6220a-108">Syntax</span></span>


```C++
HRESULT ConfigureCardNameSearch(
  [in] LPSAFEARRAY pCardNames,
  [in] LPSAFEARRAY pGroupNames,
  [in] BSTR        bstrTitle,
  [in] LONG        lFlags
);
```



## <a name="parameters"></a><span data-ttu-id="6220a-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6220a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6220a-110">*pCardNames* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6220a-110">*pCardNames* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6220a-111">Puntero a una matriz segura de automatización de nombres de tarjeta en formato BSTR.</span><span class="sxs-lookup"><span data-stu-id="6220a-111">A pointer to an Automation safe array of card names in BSTR form.</span></span>

</dd> <dt>

<span data-ttu-id="6220a-112">*pGroupNames* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6220a-112">*pGroupNames* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6220a-113">Puntero a una matriz segura de automatización de nombres de grupos de tarjetas o lectores en formato BSTR que se va a agregar a la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="6220a-113">A pointer to an Automation safe array of names of card/reader groups in BSTR form to add to the search.</span></span>

</dd> <dt>

<span data-ttu-id="6220a-114">*bstrTitle* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6220a-114">*bstrTitle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6220a-115">Título del cuadro de diálogo para el control común de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="6220a-115">Dialog box title for the search common control.</span></span>

</dd> <dt>

<span data-ttu-id="6220a-116">*lFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6220a-116">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6220a-117">Especifica cuándo se muestra la [*interfaz de usuario*](../secgloss/u-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="6220a-117">Specifies when [*user interface*](../secgloss/u-gly.md) is displayed.</span></span>



| <span data-ttu-id="6220a-118">Value</span><span class="sxs-lookup"><span data-stu-id="6220a-118">Value</span></span>                                                                                                                                                                       | <span data-ttu-id="6220a-119">Significado</span><span class="sxs-lookup"><span data-stu-id="6220a-119">Meaning</span></span>                                                                                                                                                                                                                                                                                                                             |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SC_DLG_MINIMAL_UI"></span><span id="sc_dlg_minimal_ui"></span><dl> <span data-ttu-id="6220a-120"><dt>**\_interfaz de \_ \_ usuario mínima de SC Dlg**</dt></span><span class="sxs-lookup"><span data-stu-id="6220a-120"><dt>**SC\_DLG\_MINIMAL\_UI**</dt></span></span> </dl> | <span data-ttu-id="6220a-121">Muestra el cuadro de diálogo solo si la tarjeta que se está buscando en la aplicación que realiza la llamada no está ubicada y disponible para su uso en un lector.</span><span class="sxs-lookup"><span data-stu-id="6220a-121">Displays the dialog box only if the card being searched for by the calling application is not located and available for use in a reader.</span></span> <span data-ttu-id="6220a-122">Esto permite que la tarjeta se encuentre, conectada (ya sea a través de un mecanismo de cuadros de diálogo interno o mediante las funciones de devolución de llamada de usuario) y se devuelva a la aplicación que realiza la llamada.</span><span class="sxs-lookup"><span data-stu-id="6220a-122">This allows the card to be found, connected (either through an internal dialog box mechanism or by using the user callback functions), and returned to the calling application.</span></span><br/> |
| <span id="SC_DLG_NO_UI"></span><span id="sc_dlg_no_ui"></span><dl> <span data-ttu-id="6220a-123"><dt>**SC \_ Dlg \_ sin \_ interfaz de usuario**</dt></span><span class="sxs-lookup"><span data-stu-id="6220a-123"><dt>**SC\_DLG\_NO\_UI**</dt></span></span> </dl>                | <span data-ttu-id="6220a-124">No provoca ninguna presentación de la interfaz de usuario, independientemente del resultado de la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="6220a-124">Causes no UI display, regardless of the search outcome.</span></span><br/>                                                                                                                                                                                                                                                                  |
| <span id="SC_DLG_FORCE_UI"></span><span id="sc_dlg_force_ui"></span><dl> <span data-ttu-id="6220a-125"><dt>**fuerza de IU de SC \_ Dlg \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="6220a-125"><dt>**SC\_DLG\_FORCE\_UI**</dt></span></span> </dl>       | <span data-ttu-id="6220a-126">Provoca la presentación de la interfaz de usuario independientemente del resultado de la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="6220a-126">Causes UI display regardless of the search outcome.</span></span><br/>                                                                                                                                                                                                                                                                      |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6220a-127">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6220a-127">Return value</span></span>

<span data-ttu-id="6220a-128">El método devuelve uno de los siguientes valores posibles.</span><span class="sxs-lookup"><span data-stu-id="6220a-128">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="6220a-129">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="6220a-129">Return code</span></span>                                                                                   | <span data-ttu-id="6220a-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="6220a-130">Description</span></span>                                                           |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <dl> <span data-ttu-id="6220a-131"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="6220a-131"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="6220a-132">Operación completada correctamente.</span><span class="sxs-lookup"><span data-stu-id="6220a-132">Operation completed successfully.</span></span><br/>                          |
| <dl> <span data-ttu-id="6220a-133"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="6220a-133"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="6220a-134">Parámetro no válido.</span><span class="sxs-lookup"><span data-stu-id="6220a-134">Invalid parameter.</span></span><br/>                                         |
| <dl> <span data-ttu-id="6220a-135"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="6220a-135"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="6220a-136">Se pasó un puntero no válido en *pCardNames* o *pGroupNames*.</span><span class="sxs-lookup"><span data-stu-id="6220a-136">A bad pointer was passed in *pCardNames* or *pGroupNames*.</span></span><br/> |
| <dl> <span data-ttu-id="6220a-137"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="6220a-137"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="6220a-138">Memoria insuficiente</span><span class="sxs-lookup"><span data-stu-id="6220a-138">Out of memory.</span></span><br/>                                             |



 

## <a name="remarks"></a><span data-ttu-id="6220a-139">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6220a-139">Remarks</span></span>

<span data-ttu-id="6220a-140">Para buscar la [*tarjeta inteligente*](../secgloss/s-gly.md), llame a [**FindCard**](iscardlocate-findcard.md).</span><span class="sxs-lookup"><span data-stu-id="6220a-140">To locate the [*smart card*](../secgloss/s-gly.md), call [**FindCard**](iscardlocate-findcard.md).</span></span>

<span data-ttu-id="6220a-141">Para obtener una lista de todos los métodos proporcionados por esta interfaz, vea [**ISCardLocate**](iscardlocate.md).</span><span class="sxs-lookup"><span data-stu-id="6220a-141">For a list of all the methods provided by this interface, see [**ISCardLocate**](iscardlocate.md).</span></span>

<span data-ttu-id="6220a-142">Además de los códigos de error COM enumerados anteriormente, esta interfaz puede devolver un código de error de tarjeta inteligente si se llamó a una función de tarjeta inteligente para completar la solicitud.</span><span class="sxs-lookup"><span data-stu-id="6220a-142">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="6220a-143">Para obtener más información, vea [valores devueltos de tarjeta inteligente](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="6220a-143">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6220a-144">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6220a-144">Requirements</span></span>



| <span data-ttu-id="6220a-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="6220a-145">Requirement</span></span> | <span data-ttu-id="6220a-146">Value</span><span class="sxs-lookup"><span data-stu-id="6220a-146">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6220a-147">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6220a-147">Minimum supported client</span></span><br/> | <span data-ttu-id="6220a-148">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="6220a-148">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="6220a-149">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6220a-149">Minimum supported server</span></span><br/> | <span data-ttu-id="6220a-150">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="6220a-150">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="6220a-151">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="6220a-151">End of client support</span></span><br/>    | <span data-ttu-id="6220a-152">Windows XP</span><span class="sxs-lookup"><span data-stu-id="6220a-152">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="6220a-153">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="6220a-153">End of server support</span></span><br/>    | <span data-ttu-id="6220a-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="6220a-154">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="6220a-155">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6220a-155">Header</span></span><br/>                   | <dl> <span data-ttu-id="6220a-156"><dt>Scardmgr. h</dt></span><span class="sxs-lookup"><span data-stu-id="6220a-156"><dt>Scardmgr.h</dt></span></span> </dl>   |
| <span data-ttu-id="6220a-157">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="6220a-157">Type library</span></span><br/>             | <dl> <span data-ttu-id="6220a-158"><dt>Scardmgr. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="6220a-158"><dt>Scardmgr.tlb</dt></span></span> </dl> |
| <span data-ttu-id="6220a-159">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="6220a-159">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6220a-160"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6220a-160"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="6220a-161">IID</span><span class="sxs-lookup"><span data-stu-id="6220a-161">IID</span></span><br/>                      | <span data-ttu-id="6220a-162">IID \_ ISCardLocate se define como 1461AACD-6810-11D0-918F-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="6220a-162">IID\_ISCardLocate is defined as 1461AACD-6810-11D0-918F-00AA00C18068</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="6220a-163">Vea también</span><span class="sxs-lookup"><span data-stu-id="6220a-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6220a-164">**FindCard**</span><span class="sxs-lookup"><span data-stu-id="6220a-164">**FindCard**</span></span>](iscardlocate-findcard.md)
</dt> <dt>

[<span data-ttu-id="6220a-165">**ISCardLocate**</span><span class="sxs-lookup"><span data-stu-id="6220a-165">**ISCardLocate**</span></span>](iscardlocate.md)
</dt> </dl>

 

 
