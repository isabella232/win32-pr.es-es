---
description: El método Item del objeto SWbemNamedValueSet obtiene un objeto SWbemNamedValue de la colección.
ms.assetid: ccebe65e-6032-43d5-9004-2247c3b96d6d
ms.tgt_platform: multiple
title: Método SWbemNamedValueSet. Item (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemNamedValueSet.Item
- ISWbemNamedValueSet.Item
- ISWbemNamedValueSet.Item
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: a4932409fa7b8ac9e0f326e5de7e8ecf0f89c2b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544662"
---
# <a name="swbemnamedvaluesetitem-method"></a><span data-ttu-id="6ec52-103">SWbemNamedValueSet. Item (método)</span><span class="sxs-lookup"><span data-stu-id="6ec52-103">SWbemNamedValueSet.Item method</span></span>

<span data-ttu-id="6ec52-104">El método **Item** del objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) obtiene un objeto [**SWbemNamedValue**](swbemnamedvalue.md) de la colección.</span><span class="sxs-lookup"><span data-stu-id="6ec52-104">The **Item** method of the [**SWbemNamedValueSet**](swbemnamedvalueset.md) object gets an [**SWbemNamedValue**](swbemnamedvalue.md) object from the collection.</span></span>

<span data-ttu-id="6ec52-105">Para obtener una explicación de esta sintaxis, vea [convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="6ec52-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="6ec52-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6ec52-106">Syntax</span></span>


```VB
objNamedValue = .Item( _
  ByVal strName, _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a><span data-ttu-id="6ec52-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6ec52-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6ec52-108">*strName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6ec52-108">*strName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6ec52-109">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="6ec52-109">Required.</span></span> <span data-ttu-id="6ec52-110">Nombre del valor que se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="6ec52-110">Name of the value to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="6ec52-111">*iFlags* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="6ec52-111">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="6ec52-112">Reservado.</span><span class="sxs-lookup"><span data-stu-id="6ec52-112">Reserved.</span></span> <span data-ttu-id="6ec52-113">Este valor debe ser cero si se especifica.</span><span class="sxs-lookup"><span data-stu-id="6ec52-113">This value must be zero if specified.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6ec52-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6ec52-114">Return value</span></span>

<span data-ttu-id="6ec52-115">Si se realiza correctamente, se devuelve el objeto [**SWbemNamedValue**](swbemnamedvalue.md) solicitado.</span><span class="sxs-lookup"><span data-stu-id="6ec52-115">If successful, the requested [**SWbemNamedValue**](swbemnamedvalue.md) object is returned.</span></span>

## <a name="error-codes"></a><span data-ttu-id="6ec52-116">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="6ec52-116">Error codes</span></span>

<span data-ttu-id="6ec52-117">Al completarse el método **Item** , el objeto **Err** puede contener uno de los códigos de error de la lista siguiente.</span><span class="sxs-lookup"><span data-stu-id="6ec52-117">Upon completion of the **Item** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="6ec52-118">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="6ec52-118">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="6ec52-119">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="6ec52-119">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="6ec52-120">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="6ec52-120">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="6ec52-121">Se especificó un parámetro no válido o no se pudo analizar el espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="6ec52-121">An invalid parameter was specified, or the namespace could not be parsed.</span></span>

</dd> <dt>

<span data-ttu-id="6ec52-122">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="6ec52-122">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="6ec52-123">Memoria insuficiente para completar la operación.</span><span class="sxs-lookup"><span data-stu-id="6ec52-123">Not enough memory to complete the operation.</span></span>

</dd> <dt>

<span data-ttu-id="6ec52-124">**wbemErrNotFound** -2147749890 (0x80041002)</span><span class="sxs-lookup"><span data-stu-id="6ec52-124">**wbemErrNotFound** - 2147749890 (0x80041002)</span></span>
</dt> <dd>

<span data-ttu-id="6ec52-125">No se encontró el elemento solicitado.</span><span class="sxs-lookup"><span data-stu-id="6ec52-125">The requested item was not found.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6ec52-126">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6ec52-126">Remarks</span></span>

<span data-ttu-id="6ec52-127">Para obtener ejemplos de cómo agregar y recuperar valores con nombre, vea [**SWbemNamedValue. Value**](swbemnamedvalue-value.md).</span><span class="sxs-lookup"><span data-stu-id="6ec52-127">For examples of adding and retrieving named values, see [**SWbemNamedValue.Value**](swbemnamedvalue-value.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6ec52-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6ec52-128">Requirements</span></span>



| <span data-ttu-id="6ec52-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="6ec52-129">Requirement</span></span> | <span data-ttu-id="6ec52-130">Value</span><span class="sxs-lookup"><span data-stu-id="6ec52-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6ec52-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6ec52-131">Minimum supported client</span></span><br/> | <span data-ttu-id="6ec52-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6ec52-132">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6ec52-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6ec52-133">Minimum supported server</span></span><br/> | <span data-ttu-id="6ec52-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6ec52-134">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6ec52-135">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6ec52-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="6ec52-136"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="6ec52-136"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="6ec52-137">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="6ec52-137">Type library</span></span><br/>             | <dl> <span data-ttu-id="6ec52-138"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="6ec52-138"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="6ec52-139">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="6ec52-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6ec52-140"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6ec52-140"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="6ec52-141">CLSID</span><span class="sxs-lookup"><span data-stu-id="6ec52-141">CLSID</span></span><br/>                    | <span data-ttu-id="6ec52-142">CLSID \_ SWbemNamedValueSet</span><span class="sxs-lookup"><span data-stu-id="6ec52-142">CLSID\_SWbemNamedValueSet</span></span><br/>                                                    |
| <span data-ttu-id="6ec52-143">IID</span><span class="sxs-lookup"><span data-stu-id="6ec52-143">IID</span></span><br/>                      | <span data-ttu-id="6ec52-144">\_ISWBEMNAMEDVALUESET IID</span><span class="sxs-lookup"><span data-stu-id="6ec52-144">IID\_ISWbemNamedValueSet</span></span><br/>                                                     |



## <a name="see-also"></a><span data-ttu-id="6ec52-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="6ec52-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ec52-146">**SWbemNamedValueSet**</span><span class="sxs-lookup"><span data-stu-id="6ec52-146">**SWbemNamedValueSet**</span></span>](swbemnamedvalueset.md)
</dt> </dl>

 

 




