---
description: El método Item del objeto SWbemQualifierSet devuelve un objeto SWbemQualifier con nombre de la colección. Este es el método predeterminado de este objeto.
ms.assetid: 5ed3a336-c06f-446d-85d4-243daddc82a5
ms.tgt_platform: multiple
title: Método SWbemQualifierSet. Item (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemQualifierSet.Item
- ISWbemQualifierSet.Item
- ISWbemQualifierSet.Item
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 9c89ff554b049e6730a64ebf7e5f017fc8a5652f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913190"
---
# <a name="swbemqualifiersetitem-method"></a><span data-ttu-id="d1531-104">SWbemQualifierSet. Item (método)</span><span class="sxs-lookup"><span data-stu-id="d1531-104">SWbemQualifierSet.Item method</span></span>

<span data-ttu-id="d1531-105">El método **Item** del objeto [**SWbemQualifierSet**](swbemqualifierset.md) devuelve un objeto [**SWbemQualifier**](swbemqualifier.md) con nombre de la colección.</span><span class="sxs-lookup"><span data-stu-id="d1531-105">The **Item** method of the [**SWbemQualifierSet**](swbemqualifierset.md) object returns a named [**SWbemQualifier**](swbemqualifier.md) object from the collection.</span></span> <span data-ttu-id="d1531-106">Este es el método predeterminado de este objeto.</span><span class="sxs-lookup"><span data-stu-id="d1531-106">This is the default method of this object.</span></span>

<span data-ttu-id="d1531-107">Para obtener una explicación de esta sintaxis, vea [convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="d1531-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="d1531-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d1531-108">Syntax</span></span>


```VB
objQualifier = .Item( _
  ByVal strName, _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a><span data-ttu-id="d1531-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d1531-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d1531-110">*strName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d1531-110">*strName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d1531-111">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="d1531-111">Required.</span></span> <span data-ttu-id="d1531-112">Nombre del calificador que se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="d1531-112">Name of the qualifier to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="d1531-113">*iFlags* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="d1531-113">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d1531-114">Reservado.</span><span class="sxs-lookup"><span data-stu-id="d1531-114">Reserved.</span></span> <span data-ttu-id="d1531-115">El valor predeterminado es 0 (cero).</span><span class="sxs-lookup"><span data-stu-id="d1531-115">The default value is 0 (zero).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d1531-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d1531-116">Return value</span></span>

<span data-ttu-id="d1531-117">Si se realiza correctamente, se devuelve el objeto [**SWbemQualifier**](swbemqualifier.md) solicitado.</span><span class="sxs-lookup"><span data-stu-id="d1531-117">If successful, the requested [**SWbemQualifier**](swbemqualifier.md) object is returned.</span></span>

## <a name="error-codes"></a><span data-ttu-id="d1531-118">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="d1531-118">Error codes</span></span>

<span data-ttu-id="d1531-119">Una vez finalizado el método **Item** , el objeto **Err** puede contener uno de los códigos de error de la lista siguiente.</span><span class="sxs-lookup"><span data-stu-id="d1531-119">After completion of the **Item** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="d1531-120">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="d1531-120">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="d1531-121">El parámetro *iFlags* no era válido.</span><span class="sxs-lookup"><span data-stu-id="d1531-121">The *iFlags* parameter was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="d1531-122">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="d1531-122">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="d1531-123">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="d1531-123">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="d1531-124">**wbemErrNotFound** -2147749890 (0x80041002)</span><span class="sxs-lookup"><span data-stu-id="d1531-124">**wbemErrNotFound** - 2147749890 (0x80041002)</span></span>
</dt> <dd>

<span data-ttu-id="d1531-125">El calificador especificado no existe.</span><span class="sxs-lookup"><span data-stu-id="d1531-125">Specified qualifier does not exist.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d1531-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d1531-126">Requirements</span></span>



| <span data-ttu-id="d1531-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="d1531-127">Requirement</span></span> | <span data-ttu-id="d1531-128">Value</span><span class="sxs-lookup"><span data-stu-id="d1531-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d1531-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d1531-129">Minimum supported client</span></span><br/> | <span data-ttu-id="d1531-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d1531-130">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d1531-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d1531-131">Minimum supported server</span></span><br/> | <span data-ttu-id="d1531-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d1531-132">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d1531-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d1531-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="d1531-134"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="d1531-134"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="d1531-135">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="d1531-135">Type library</span></span><br/>             | <dl> <span data-ttu-id="d1531-136"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="d1531-136"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="d1531-137">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d1531-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d1531-138"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d1531-138"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="d1531-139">CLSID</span><span class="sxs-lookup"><span data-stu-id="d1531-139">CLSID</span></span><br/>                    | <span data-ttu-id="d1531-140">CLSID \_ SWbemQualifierSet</span><span class="sxs-lookup"><span data-stu-id="d1531-140">CLSID\_SWbemQualifierSet</span></span><br/>                                                     |
| <span data-ttu-id="d1531-141">IID</span><span class="sxs-lookup"><span data-stu-id="d1531-141">IID</span></span><br/>                      | <span data-ttu-id="d1531-142">\_ISWBEMQUALIFIERSET IID</span><span class="sxs-lookup"><span data-stu-id="d1531-142">IID\_ISWbemQualifierSet</span></span><br/>                                                      |



## <a name="see-also"></a><span data-ttu-id="d1531-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="d1531-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1531-144">**SWbemQualifierSet**</span><span class="sxs-lookup"><span data-stu-id="d1531-144">**SWbemQualifierSet**</span></span>](swbemqualifierset.md)
</dt> <dt>

[<span data-ttu-id="d1531-145">**SWbemQualifier**</span><span class="sxs-lookup"><span data-stu-id="d1531-145">**SWbemQualifier**</span></span>](swbemqualifier.md)
</dt> </dl>

 

 




