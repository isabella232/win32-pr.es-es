---
description: Recupera los datos primitivos a los que hace referencia TLVs (TAG, length, Value) del objeto especificado.
ms.assetid: 135aeb9a-b851-4522-862f-02a7e020c36b
title: 'ISCardFileAccess:: GetProperties (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardFileAccess.GetProperties
api_type:
- COM
api_location: ''
ms.openlocfilehash: 25e6ae1ab657d92dda0ad421b650eaaa7076bd63
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105648491"
---
# <a name="iscardfileaccessgetproperties-method"></a><span data-ttu-id="b0d56-103">ISCardFileAccess:: GetProperties (método)</span><span class="sxs-lookup"><span data-stu-id="b0d56-103">ISCardFileAccess::GetProperties method</span></span>

<span data-ttu-id="b0d56-104">\[El método **GetProperties** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="b0d56-104">\[The **GetProperties** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="b0d56-105">No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="b0d56-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="b0d56-106">Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="b0d56-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="b0d56-107">El método **GetProperties** recupera los datos primitivos a los que hace referencia TLVs (etiqueta, longitud, valor) para el objeto especificado.</span><span class="sxs-lookup"><span data-stu-id="b0d56-107">The **GetProperties** method retrieves the primitive data referred by TLVs (tag, length, value) for the specified object.</span></span>

## <a name="syntax"></a><span data-ttu-id="b0d56-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b0d56-108">Syntax</span></span>


```C++
HRESULT GetProperties(
  [in]      REFTYPE     refType,
  [in]      BSTR        bstrPathSpec,
  [in]      SCARD_FLAGS flags,
  [in, out] LPTLV_TABLE *ppTLV
);
```



## <a name="parameters"></a><span data-ttu-id="b0d56-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b0d56-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b0d56-110">*refType* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b0d56-110">*refType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b0d56-111">Tipo de referencia que se usa en *bstrNewDir*.</span><span class="sxs-lookup"><span data-stu-id="b0d56-111">Type of reference used in *bstrNewDir*.</span></span>

<dl><span id="SC_TYPE_BY_NAME"></span><span id="sc_type_by_name"></span><dt>

<span data-ttu-id="b0d56-112">**\_tipo SC \_ por \_ nombre**</span><span class="sxs-lookup"><span data-stu-id="b0d56-112">**SC\_TYPE\_BY\_NAME**</span></span>
</dt><span id="SC_TYPE_BY_ID"></span><span id="sc_type_by_id"></span><dt>

<span data-ttu-id="b0d56-113">**\_tipo SC \_ por \_ identificador**</span><span class="sxs-lookup"><span data-stu-id="b0d56-113">**SC\_TYPE\_BY\_ID**</span></span>
</dt><span id="SC_TYPE_BY_SHORT"></span><span id="sc_type_by_short"></span><dt>

<span data-ttu-id="b0d56-114">**\_tipo SC \_ por \_ corto**</span><span class="sxs-lookup"><span data-stu-id="b0d56-114">**SC\_TYPE\_BY\_SHORT**</span></span>
</dt><span id="SC_TYPE_BY_ANY"></span><span id="sc_type_by_any"></span><dt>

<span data-ttu-id="b0d56-115">**\_tipo SC \_ por \_ cualquier**</span><span class="sxs-lookup"><span data-stu-id="b0d56-115">**SC\_TYPE\_BY\_ANY**</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="b0d56-116">*bstrPathSpec* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b0d56-116">*bstrPathSpec* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b0d56-117">Archivo:</span><span class="sxs-lookup"><span data-stu-id="b0d56-117">File.</span></span>

</dd> <dt>

<span data-ttu-id="b0d56-118">*marcas* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="b0d56-118">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b0d56-119">Especifica si se debe usar la mensajería segura.</span><span class="sxs-lookup"><span data-stu-id="b0d56-119">Specifies whether secure messaging should be used.</span></span>

<dl><span id="SC_FL_SECURE_MESSAGING"></span><span id="sc_fl_secure_messaging"></span><dt>

<span data-ttu-id="b0d56-120">**\_ \_ mensajería segura de SC FL \_**</span><span class="sxs-lookup"><span data-stu-id="b0d56-120">**SC\_FL\_SECURE\_MESSAGING**</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="b0d56-121">*ppTLV* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="b0d56-121">*ppTLV* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="b0d56-122">Puntero a las estructuras TLV cuyo valor se ha recuperado.</span><span class="sxs-lookup"><span data-stu-id="b0d56-122">Pointer to TLV structures whose value has been retrieved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b0d56-123">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b0d56-123">Return value</span></span>

<span data-ttu-id="b0d56-124">El método devuelve uno de los siguientes valores posibles.</span><span class="sxs-lookup"><span data-stu-id="b0d56-124">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="b0d56-125">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="b0d56-125">Return code</span></span>                                                                                   | <span data-ttu-id="b0d56-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="b0d56-126">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="b0d56-127"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="b0d56-127"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="b0d56-128">Operación completada correctamente.</span><span class="sxs-lookup"><span data-stu-id="b0d56-128">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="b0d56-129"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="b0d56-129"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="b0d56-130">Parámetro no válido.</span><span class="sxs-lookup"><span data-stu-id="b0d56-130">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="b0d56-131"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="b0d56-131"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="b0d56-132">Se pasó un puntero no válido.</span><span class="sxs-lookup"><span data-stu-id="b0d56-132">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="b0d56-133"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="b0d56-133"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="b0d56-134">Memoria insuficiente</span><span class="sxs-lookup"><span data-stu-id="b0d56-134">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="b0d56-135">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b0d56-135">Remarks</span></span>

<span data-ttu-id="b0d56-136">Para obtener una lista de todos los métodos definidos por esta interfaz, vea [**ISCardFileAccess**](iscardfileaccess.md).</span><span class="sxs-lookup"><span data-stu-id="b0d56-136">For a list of all the methods defined by this interface, see [**ISCardFileAccess**](iscardfileaccess.md).</span></span>

<span data-ttu-id="b0d56-137">Además de los códigos de error COM enumerados anteriormente, esta interfaz puede devolver un código de error de [*tarjeta inteligente*](../secgloss/s-gly.md) si se llamó a una función de tarjeta inteligente para completar la solicitud.</span><span class="sxs-lookup"><span data-stu-id="b0d56-137">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="b0d56-138">Para obtener más información, vea [valores devueltos de tarjeta inteligente](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="b0d56-138">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b0d56-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b0d56-139">Requirements</span></span>



| <span data-ttu-id="b0d56-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="b0d56-140">Requirement</span></span> | <span data-ttu-id="b0d56-141">Value</span><span class="sxs-lookup"><span data-stu-id="b0d56-141">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="b0d56-142">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b0d56-142">Minimum supported client</span></span><br/> | <span data-ttu-id="b0d56-143">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="b0d56-143">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="b0d56-144">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b0d56-144">Minimum supported server</span></span><br/> | <span data-ttu-id="b0d56-145">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="b0d56-145">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="b0d56-146">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="b0d56-146">End of client support</span></span><br/>    | <span data-ttu-id="b0d56-147">Windows XP</span><span class="sxs-lookup"><span data-stu-id="b0d56-147">Windows XP</span></span><br/>                                |
| <span data-ttu-id="b0d56-148">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="b0d56-148">End of server support</span></span><br/>    | <span data-ttu-id="b0d56-149">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b0d56-149">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="b0d56-150">Vea también</span><span class="sxs-lookup"><span data-stu-id="b0d56-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0d56-151">**ISCardFileAccess**</span><span class="sxs-lookup"><span data-stu-id="b0d56-151">**ISCardFileAccess**</span></span>](iscardfileaccess.md)
</dt> </dl>

 

 
