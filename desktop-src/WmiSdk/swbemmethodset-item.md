---
description: El método Item del objeto SWbemMethodSet devuelve un objeto SWbemMethod con nombre de la colección.
ms.assetid: 4c1bbecc-b38b-4869-9c8c-b9321536b23e
ms.tgt_platform: multiple
title: Método SWbemMethodSet. Item (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemMethodSet.Item
- ISWbemMethodSet.Item
- ISWbemMethodSet.Item
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 89d20dc652189abe3354f5d1b51c03279d3f74c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696793"
---
# <a name="swbemmethodsetitem-method"></a><span data-ttu-id="5d81d-103">SWbemMethodSet. Item (método)</span><span class="sxs-lookup"><span data-stu-id="5d81d-103">SWbemMethodSet.Item method</span></span>

<span data-ttu-id="5d81d-104">El método **Item** del objeto [**SWbemMethodSet**](swbemmethodset.md) devuelve un objeto [**SWbemMethod**](swbemmethod.md) con nombre de la colección.</span><span class="sxs-lookup"><span data-stu-id="5d81d-104">The **Item** method of the [**SWbemMethodSet**](swbemmethodset.md) object returns a named [**SWbemMethod**](swbemmethod.md) object from the collection.</span></span>

<span data-ttu-id="5d81d-105">Para obtener una explicación de esta sintaxis, vea [convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="5d81d-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="5d81d-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5d81d-106">Syntax</span></span>


```VB
objMethod = .Item( _
  ByVal strName, _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a><span data-ttu-id="5d81d-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5d81d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5d81d-108">*strName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="5d81d-108">*strName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5d81d-109">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="5d81d-109">Required.</span></span> <span data-ttu-id="5d81d-110">Nombre del método que se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="5d81d-110">Name of the method to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="5d81d-111">*iFlags* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="5d81d-111">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="5d81d-112">Reservado.</span><span class="sxs-lookup"><span data-stu-id="5d81d-112">Reserved.</span></span> <span data-ttu-id="5d81d-113">El valor predeterminado es 0.</span><span class="sxs-lookup"><span data-stu-id="5d81d-113">The default value is 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5d81d-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5d81d-114">Return value</span></span>

<span data-ttu-id="5d81d-115">Si se realiza correctamente, el objeto [**SWbemMethod**](swbemmethod.md) solicitado devuelve.</span><span class="sxs-lookup"><span data-stu-id="5d81d-115">If successful, the requested [**SWbemMethod**](swbemmethod.md) object returns.</span></span>

## <a name="error-codes"></a><span data-ttu-id="5d81d-116">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="5d81d-116">Error codes</span></span>

<span data-ttu-id="5d81d-117">Al completarse el método **Item** , el objeto **Err** puede contener uno de los códigos de error de la lista siguiente.</span><span class="sxs-lookup"><span data-stu-id="5d81d-117">Upon completion of the **Item** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="5d81d-118">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="5d81d-118">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="5d81d-119">El parámetro *iFlags* no era válido.</span><span class="sxs-lookup"><span data-stu-id="5d81d-119">The *iFlags* parameter was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="5d81d-120">**wbemErrFailed** -2147749894</span><span class="sxs-lookup"><span data-stu-id="5d81d-120">**wbemErrFailed** - 2147749894</span></span>
</dt> <dd>

<span data-ttu-id="5d81d-121">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="5d81d-121">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="5d81d-122">**wbemErrNotFound** -2147749890 (0x80041002)</span><span class="sxs-lookup"><span data-stu-id="5d81d-122">**wbemErrNotFound** - 2147749890 (0x80041002)</span></span>
</dt> <dd>

<span data-ttu-id="5d81d-123">El método especificado no existe.</span><span class="sxs-lookup"><span data-stu-id="5d81d-123">The specified method does not exist.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5d81d-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5d81d-124">Requirements</span></span>



| <span data-ttu-id="5d81d-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="5d81d-125">Requirement</span></span> | <span data-ttu-id="5d81d-126">Value</span><span class="sxs-lookup"><span data-stu-id="5d81d-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5d81d-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5d81d-127">Minimum supported client</span></span><br/> | <span data-ttu-id="5d81d-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5d81d-128">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5d81d-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5d81d-129">Minimum supported server</span></span><br/> | <span data-ttu-id="5d81d-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5d81d-130">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5d81d-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5d81d-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="5d81d-132"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="5d81d-132"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="5d81d-133">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="5d81d-133">Type library</span></span><br/>             | <dl> <span data-ttu-id="5d81d-134"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="5d81d-134"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="5d81d-135">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="5d81d-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5d81d-136"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5d81d-136"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="5d81d-137">CLSID</span><span class="sxs-lookup"><span data-stu-id="5d81d-137">CLSID</span></span><br/>                    | <span data-ttu-id="5d81d-138">CLSID \_ SWbemMethodSet</span><span class="sxs-lookup"><span data-stu-id="5d81d-138">CLSID\_SWbemMethodSet</span></span><br/>                                                        |
| <span data-ttu-id="5d81d-139">IID</span><span class="sxs-lookup"><span data-stu-id="5d81d-139">IID</span></span><br/>                      | <span data-ttu-id="5d81d-140">\_ISWBEMMETHODSET IID</span><span class="sxs-lookup"><span data-stu-id="5d81d-140">IID\_ISWbemMethodSet</span></span><br/>                                                         |



## <a name="see-also"></a><span data-ttu-id="5d81d-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="5d81d-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d81d-142">**SWbemMethodSet**</span><span class="sxs-lookup"><span data-stu-id="5d81d-142">**SWbemMethodSet**</span></span>](swbemmethodset.md)
</dt> <dt>

[<span data-ttu-id="5d81d-143">**SWbemMethod**</span><span class="sxs-lookup"><span data-stu-id="5d81d-143">**SWbemMethod**</span></span>](swbemmethod.md)
</dt> </dl>

 

 




