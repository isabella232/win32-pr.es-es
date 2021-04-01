---
description: El método Item del objeto SWbemPropertySet obtiene un SWbemProperty con nombre de la colección. Este es el método predeterminado para este objeto.
ms.assetid: 72025676-01dd-4fd7-b000-de6b09ecc6dc
ms.tgt_platform: multiple
title: Método SWbemPropertySet. Item (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemPropertySet.Item
- ISWbemPropertySet.Item
- ISWbemPropertySet.Item
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: b4d4dcbbbcb8b5225af038bf71e67c3a14260942
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279098"
---
# <a name="swbempropertysetitem-method"></a><span data-ttu-id="7fa61-104">SWbemPropertySet. Item (método)</span><span class="sxs-lookup"><span data-stu-id="7fa61-104">SWbemPropertySet.Item method</span></span>

<span data-ttu-id="7fa61-105">El método **Item** del objeto [**SWbemPropertySet**](swbempropertyset.md) obtiene un [**SWbemProperty**](swbemproperty.md) con nombre de la colección.</span><span class="sxs-lookup"><span data-stu-id="7fa61-105">The **Item** method of the [**SWbemPropertySet**](swbempropertyset.md) object gets a named [**SWbemProperty**](swbemproperty.md) from the collection.</span></span> <span data-ttu-id="7fa61-106">Este es el método predeterminado para este objeto.</span><span class="sxs-lookup"><span data-stu-id="7fa61-106">This is the default method for this object.</span></span>

<span data-ttu-id="7fa61-107">Para obtener una explicación de esta sintaxis, vea [convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="7fa61-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="7fa61-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7fa61-108">Syntax</span></span>


```VB
objProperty = .Item( _
  ByVal strName, _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a><span data-ttu-id="7fa61-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7fa61-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7fa61-110">*strName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="7fa61-110">*strName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7fa61-111">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="7fa61-111">Required.</span></span> <span data-ttu-id="7fa61-112">Nombre de la propiedad que se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="7fa61-112">Name of the property to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="7fa61-113">*iFlags* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="7fa61-113">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="7fa61-114">Reservado.</span><span class="sxs-lookup"><span data-stu-id="7fa61-114">Reserved.</span></span> <span data-ttu-id="7fa61-115">Este valor debe ser cero si se especifica.</span><span class="sxs-lookup"><span data-stu-id="7fa61-115">This value must be zero if specified.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7fa61-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7fa61-116">Return value</span></span>

<span data-ttu-id="7fa61-117">Si se realiza correctamente, se devuelve el objeto [**SWbemProperty**](swbemproperty.md) solicitado.</span><span class="sxs-lookup"><span data-stu-id="7fa61-117">If successful, the requested [**SWbemProperty**](swbemproperty.md) object is returned.</span></span>

## <a name="error-codes"></a><span data-ttu-id="7fa61-118">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="7fa61-118">Error codes</span></span>

<span data-ttu-id="7fa61-119">Después de completar el método **Item** , el objeto **Err** puede contener uno de los códigos de error de la lista siguiente.</span><span class="sxs-lookup"><span data-stu-id="7fa61-119">After the completion of the **Item** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="7fa61-120">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="7fa61-120">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="7fa61-121">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="7fa61-121">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="7fa61-122">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="7fa61-122">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="7fa61-123">Se especificó un parámetro no válido.</span><span class="sxs-lookup"><span data-stu-id="7fa61-123">Invalid parameter was specified.</span></span>

</dd> <dt>

<span data-ttu-id="7fa61-124">**wbemErrOutOfMemory** -2147749896</span><span class="sxs-lookup"><span data-stu-id="7fa61-124">**wbemErrOutOfMemory** - 2147749896</span></span>
</dt> <dd>

<span data-ttu-id="7fa61-125">Memoria insuficiente para que se ejecute este método.</span><span class="sxs-lookup"><span data-stu-id="7fa61-125">Not enough memory for this method to execute.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7fa61-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7fa61-126">Requirements</span></span>



| <span data-ttu-id="7fa61-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="7fa61-127">Requirement</span></span> | <span data-ttu-id="7fa61-128">Value</span><span class="sxs-lookup"><span data-stu-id="7fa61-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7fa61-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7fa61-129">Minimum supported client</span></span><br/> | <span data-ttu-id="7fa61-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7fa61-130">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="7fa61-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7fa61-131">Minimum supported server</span></span><br/> | <span data-ttu-id="7fa61-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7fa61-132">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="7fa61-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7fa61-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="7fa61-134"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="7fa61-134"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="7fa61-135">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="7fa61-135">Type library</span></span><br/>             | <dl> <span data-ttu-id="7fa61-136"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="7fa61-136"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="7fa61-137">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="7fa61-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7fa61-138"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7fa61-138"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="7fa61-139">CLSID</span><span class="sxs-lookup"><span data-stu-id="7fa61-139">CLSID</span></span><br/>                    | <span data-ttu-id="7fa61-140">CLSID \_ SWbemPropertySet</span><span class="sxs-lookup"><span data-stu-id="7fa61-140">CLSID\_SWbemPropertySet</span></span><br/>                                                      |
| <span data-ttu-id="7fa61-141">IID</span><span class="sxs-lookup"><span data-stu-id="7fa61-141">IID</span></span><br/>                      | <span data-ttu-id="7fa61-142">\_ISWBEMPROPERTYSET IID</span><span class="sxs-lookup"><span data-stu-id="7fa61-142">IID\_ISWbemPropertySet</span></span><br/>                                                       |



 

 




