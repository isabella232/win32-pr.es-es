---
description: El método Delete elimina un archivo en una ubicación determinada dentro del sistema de archivos de la tarjeta inteligente.
ms.assetid: f51b0329-c5dc-4f70-a92e-19dc0dbc55f8
title: ISCardFileAccess::D iminar (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardFileAccess.Delete
api_type:
- COM
api_location: ''
ms.openlocfilehash: 6331225cd3baf105682e2d275ad6be53f16f5b64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360319"
---
# <a name="iscardfileaccessdelete-method"></a><span data-ttu-id="fe5b4-103">ISCardFileAccess::D iminar (método)</span><span class="sxs-lookup"><span data-stu-id="fe5b4-103">ISCardFileAccess::Delete method</span></span>

<span data-ttu-id="fe5b4-104">\[El método **Delete** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="fe5b4-104">\[The **Delete** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="fe5b4-105">No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="fe5b4-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="fe5b4-106">Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="fe5b4-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="fe5b4-107">El método **Delete** elimina un archivo en una ubicación determinada dentro del sistema de archivos de la [*tarjeta inteligente*](../secgloss/s-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="fe5b4-107">The **Delete** method deletes a file at a given location within the [*smart card*](../secgloss/s-gly.md) file system.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe5b4-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fe5b4-108">Syntax</span></span>


```C++
HRESULT Delete(
  [in] REFTYPE     refType,
  [in] BSTR        bstrPathSpec,
  [in] SCARD_FLAGS flags
);
```



## <a name="parameters"></a><span data-ttu-id="fe5b4-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fe5b4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fe5b4-110">*refType* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="fe5b4-110">*refType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe5b4-111">Tipo de referencia que se usa en *bstrPathSpec*.</span><span class="sxs-lookup"><span data-stu-id="fe5b4-111">Type of reference used in *bstrPathSpec*.</span></span>

<dl><span id="SC_TYPE_BY_NAME"></span><span id="sc_type_by_name"></span><dt>

<span data-ttu-id="fe5b4-112">**\_tipo SC \_ por \_ nombre**</span><span class="sxs-lookup"><span data-stu-id="fe5b4-112">**SC\_TYPE\_BY\_NAME**</span></span>
</dt><span id="SC_TYPE_BY_ID"></span><span id="sc_type_by_id"></span><dt>

<span data-ttu-id="fe5b4-113">**\_tipo SC \_ por \_ identificador**</span><span class="sxs-lookup"><span data-stu-id="fe5b4-113">**SC\_TYPE\_BY\_ID**</span></span>
</dt><span id="SC_TYPE_BY_SHORT"></span><span id="sc_type_by_short"></span><dt>

<span data-ttu-id="fe5b4-114">**\_tipo SC \_ por \_ corto**</span><span class="sxs-lookup"><span data-stu-id="fe5b4-114">**SC\_TYPE\_BY\_SHORT**</span></span>
</dt><span id="SC_TYPE_BY_ANY"></span><span id="sc_type_by_any"></span><dt>

<span data-ttu-id="fe5b4-115">**\_tipo SC \_ por \_ cualquier**</span><span class="sxs-lookup"><span data-stu-id="fe5b4-115">**SC\_TYPE\_BY\_ANY**</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="fe5b4-116">*bstrPathSpec* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="fe5b4-116">*bstrPathSpec* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe5b4-117">Identificador del archivo que se va a eliminar.</span><span class="sxs-lookup"><span data-stu-id="fe5b4-117">Identifier of the file to be deleted.</span></span>

</dd> <dt>

<span data-ttu-id="fe5b4-118">*marcas* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="fe5b4-118">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe5b4-119">Especifica si se debe usar la mensajería segura y los datos preasignados.</span><span class="sxs-lookup"><span data-stu-id="fe5b4-119">Specifies whether secure messaging has to be used and data preallocated.</span></span>

<dl><span id="SC_FL_SECURE_MESSAGING"></span><span id="sc_fl_secure_messaging"></span><dt>

<span data-ttu-id="fe5b4-120">**\_ \_ mensajería segura de SC FL \_**</span><span class="sxs-lookup"><span data-stu-id="fe5b4-120">**SC\_FL\_SECURE\_MESSAGING**</span></span>
</dt><span id="SC_FL_PREALLOCATED"></span><span id="sc_fl_preallocated"></span><dt>

<span data-ttu-id="fe5b4-121">**SC \_ FL \_ preasignado**</span><span class="sxs-lookup"><span data-stu-id="fe5b4-121">**SC\_FL\_PREALLOCATED**</span></span>
</dt> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fe5b4-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fe5b4-122">Return value</span></span>

<span data-ttu-id="fe5b4-123">El método devuelve uno de los siguientes valores posibles.</span><span class="sxs-lookup"><span data-stu-id="fe5b4-123">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="fe5b4-124">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="fe5b4-124">Return code</span></span>                                                                                  | <span data-ttu-id="fe5b4-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="fe5b4-125">Description</span></span>                                               |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <dl> <span data-ttu-id="fe5b4-126"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="fe5b4-126"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="fe5b4-127">La operación se completó correctamente.</span><span class="sxs-lookup"><span data-stu-id="fe5b4-127">Operation was completed successfully.</span></span><br/>          |
| <dl> <span data-ttu-id="fe5b4-128"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="fe5b4-128"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="fe5b4-129">Parámetro no válido.</span><span class="sxs-lookup"><span data-stu-id="fe5b4-129">Invalid parameter.</span></span><br/>                             |
| <dl> <span data-ttu-id="fe5b4-130"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="fe5b4-130"><dt>**E\_NOTIMPL**</dt></span></span> </dl>    | <span data-ttu-id="fe5b4-131">La interfaz no ha implementado este método.</span><span class="sxs-lookup"><span data-stu-id="fe5b4-131">The interface has not implemented this method.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="fe5b4-132">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fe5b4-132">Remarks</span></span>

<span data-ttu-id="fe5b4-133">Para obtener una lista de todos los métodos definidos por esta interfaz, vea [**ISCardFileAccess**](iscardfileaccess.md).</span><span class="sxs-lookup"><span data-stu-id="fe5b4-133">For a list of all the methods defined by this interface, see [**ISCardFileAccess**](iscardfileaccess.md).</span></span>

<span data-ttu-id="fe5b4-134">Además de los códigos de error COM enumerados anteriormente, esta interfaz puede devolver un código de error de tarjeta inteligente si se llamó a una función de tarjeta inteligente para completar la solicitud.</span><span class="sxs-lookup"><span data-stu-id="fe5b4-134">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="fe5b4-135">Para obtener más información, vea [valores devueltos de tarjeta inteligente](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="fe5b4-135">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="fe5b4-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fe5b4-136">Requirements</span></span>



| <span data-ttu-id="fe5b4-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="fe5b4-137">Requirement</span></span> | <span data-ttu-id="fe5b4-138">Value</span><span class="sxs-lookup"><span data-stu-id="fe5b4-138">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="fe5b4-139">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fe5b4-139">Minimum supported client</span></span><br/> | <span data-ttu-id="fe5b4-140">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="fe5b4-140">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="fe5b4-141">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fe5b4-141">Minimum supported server</span></span><br/> | <span data-ttu-id="fe5b4-142">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="fe5b4-142">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="fe5b4-143">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="fe5b4-143">End of client support</span></span><br/>    | <span data-ttu-id="fe5b4-144">Windows XP</span><span class="sxs-lookup"><span data-stu-id="fe5b4-144">Windows XP</span></span><br/>                                |
| <span data-ttu-id="fe5b4-145">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="fe5b4-145">End of server support</span></span><br/>    | <span data-ttu-id="fe5b4-146">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="fe5b4-146">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="fe5b4-147">Vea también</span><span class="sxs-lookup"><span data-stu-id="fe5b4-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe5b4-148">**A**</span><span class="sxs-lookup"><span data-stu-id="fe5b4-148">**Create**</span></span>](iscardfileaccess-create.md)
</dt> <dt>

[<span data-ttu-id="fe5b4-149">**ISCardFileAccess**</span><span class="sxs-lookup"><span data-stu-id="fe5b4-149">**ISCardFileAccess**</span></span>](iscardfileaccess.md)
</dt> </dl>

 

 
