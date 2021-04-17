---
description: El método SetProperties establece el primitivo al que se refiere TLVs (etiqueta, longitud, valor) para el objeto especificado.
ms.assetid: f8f75c8e-14f4-4bc4-b49d-b232ede374b0
title: 'ISCardFileAccess:: SetProperties (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardFileAccess.SetProperties
api_type:
- COM
api_location: ''
ms.openlocfilehash: b54c2193ec17bca9f9b3ba00b2c2bc133707dbb2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652577"
---
# <a name="iscardfileaccesssetproperties-method"></a><span data-ttu-id="97747-103">ISCardFileAccess:: SetProperties (método)</span><span class="sxs-lookup"><span data-stu-id="97747-103">ISCardFileAccess::SetProperties method</span></span>

<span data-ttu-id="97747-104">\[El método **SetProperties** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="97747-104">\[The **SetProperties** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="97747-105">No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="97747-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="97747-106">Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="97747-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="97747-107">El método **SetProperties** establece el primitivo al que se refiere TLVs (etiqueta, longitud, valor) para el objeto especificado.</span><span class="sxs-lookup"><span data-stu-id="97747-107">The **SetProperties** method sets the primitive referred by TLVs (tag, length, value) for the specified object.</span></span>

## <a name="syntax"></a><span data-ttu-id="97747-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="97747-108">Syntax</span></span>


```C++
HRESULT SetProperties(
  [in] REFTYPE     refType,
  [in] BSTR        bstrPathSpec,
  [in] SCARD_FLAGS flags,
  [in] LPTLV_TABLE pTable
);
```



## <a name="parameters"></a><span data-ttu-id="97747-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="97747-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="97747-110">*refType* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="97747-110">*refType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="97747-111">Tipo de referencia que se usa en *bstrPathSpec*.</span><span class="sxs-lookup"><span data-stu-id="97747-111">Type of reference used in *bstrPathSpec*.</span></span>

<dl><span id="SC_TYPE_BY_NAME"></span><span id="sc_type_by_name"></span><dt>

<span data-ttu-id="97747-112">**\_tipo SC \_ por \_ nombre**</span><span class="sxs-lookup"><span data-stu-id="97747-112">**SC\_TYPE\_BY\_NAME**</span></span>
</dt><span id="SC_TYPE_BY_ID"></span><span id="sc_type_by_id"></span><dt>

<span data-ttu-id="97747-113">**\_tipo SC \_ por \_ identificador**</span><span class="sxs-lookup"><span data-stu-id="97747-113">**SC\_TYPE\_BY\_ID**</span></span>
</dt><span id="SC_TYPE_BY_SHORT"></span><span id="sc_type_by_short"></span><dt>

<span data-ttu-id="97747-114">**\_tipo SC \_ por \_ corto**</span><span class="sxs-lookup"><span data-stu-id="97747-114">**SC\_TYPE\_BY\_SHORT**</span></span>
</dt><span id="SC_TYPE_BY_ANY"></span><span id="sc_type_by_any"></span><dt>

<span data-ttu-id="97747-115">**\_tipo SC \_ por \_ cualquier**</span><span class="sxs-lookup"><span data-stu-id="97747-115">**SC\_TYPE\_BY\_ANY**</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="97747-116">*bstrPathSpec* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="97747-116">*bstrPathSpec* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="97747-117">Archivo:</span><span class="sxs-lookup"><span data-stu-id="97747-117">File.</span></span>

</dd> <dt>

<span data-ttu-id="97747-118">*marcas* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="97747-118">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="97747-119">Especifica si se debe usar la mensajería segura.</span><span class="sxs-lookup"><span data-stu-id="97747-119">Specifies whether secure messaging should be used.</span></span>

<dl><span id="SC_FL_SECURE_MESSAGING"></span><span id="sc_fl_secure_messaging"></span><dt>

<span data-ttu-id="97747-120">**\_ \_ mensajería segura de SC FL \_**</span><span class="sxs-lookup"><span data-stu-id="97747-120">**SC\_FL\_SECURE\_MESSAGING**</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="97747-121">*pTable* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="97747-121">*pTable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="97747-122">Puntero a las estructuras TLV cuyo valor se debe establecer.</span><span class="sxs-lookup"><span data-stu-id="97747-122">Pointer to TLV structures whose value should be set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="97747-123">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="97747-123">Return value</span></span>

<span data-ttu-id="97747-124">El método devuelve uno de los siguientes valores posibles.</span><span class="sxs-lookup"><span data-stu-id="97747-124">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="97747-125">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="97747-125">Return code</span></span>                                                                                   | <span data-ttu-id="97747-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="97747-126">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="97747-127"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="97747-127"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="97747-128">Operación completada correctamente.</span><span class="sxs-lookup"><span data-stu-id="97747-128">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="97747-129"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="97747-129"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="97747-130">Parámetro no válido.</span><span class="sxs-lookup"><span data-stu-id="97747-130">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="97747-131"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="97747-131"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="97747-132">Se pasó un puntero no válido.</span><span class="sxs-lookup"><span data-stu-id="97747-132">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="97747-133"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="97747-133"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="97747-134">Memoria insuficiente</span><span class="sxs-lookup"><span data-stu-id="97747-134">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="97747-135">Observaciones</span><span class="sxs-lookup"><span data-stu-id="97747-135">Remarks</span></span>

<span data-ttu-id="97747-136">Para obtener una lista de todos los métodos definidos por esta interfaz, vea [**ISCardFileAccess**](iscardfileaccess.md).</span><span class="sxs-lookup"><span data-stu-id="97747-136">For a list of all the methods defined by this interface, see [**ISCardFileAccess**](iscardfileaccess.md).</span></span>

<span data-ttu-id="97747-137">Además de los códigos de error COM enumerados anteriormente, esta interfaz puede devolver un código de error de [*tarjeta inteligente*](../secgloss/s-gly.md) si se llamó a una función de tarjeta inteligente para completar la solicitud.</span><span class="sxs-lookup"><span data-stu-id="97747-137">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="97747-138">Para obtener más información, vea [valores devueltos de tarjeta inteligente](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="97747-138">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="97747-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="97747-139">Requirements</span></span>



| <span data-ttu-id="97747-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="97747-140">Requirement</span></span> | <span data-ttu-id="97747-141">Value</span><span class="sxs-lookup"><span data-stu-id="97747-141">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="97747-142">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="97747-142">Minimum supported client</span></span><br/> | <span data-ttu-id="97747-143">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="97747-143">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="97747-144">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="97747-144">Minimum supported server</span></span><br/> | <span data-ttu-id="97747-145">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="97747-145">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="97747-146">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="97747-146">End of client support</span></span><br/>    | <span data-ttu-id="97747-147">Windows XP</span><span class="sxs-lookup"><span data-stu-id="97747-147">Windows XP</span></span><br/>                                |
| <span data-ttu-id="97747-148">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="97747-148">End of server support</span></span><br/>    | <span data-ttu-id="97747-149">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="97747-149">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="97747-150">Vea también</span><span class="sxs-lookup"><span data-stu-id="97747-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97747-151">**ISCardFileAccess**</span><span class="sxs-lookup"><span data-stu-id="97747-151">**ISCardFileAccess**</span></span>](iscardfileaccess.md)
</dt> </dl>

 

 
