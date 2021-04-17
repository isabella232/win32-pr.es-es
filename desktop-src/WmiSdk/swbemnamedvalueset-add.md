---
description: El método Add del objeto SWbemNamedValueSet agrega un objeto SWbemNamedValue a la colección. Si ya existe un elemento en la colección con el mismo nombre, el nuevo elemento lo reemplaza.
ms.assetid: 471b23f5-6c53-40e2-a2a9-0798044c9dfb
ms.tgt_platform: multiple
title: Método SWbemNamedValueSet. Add (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemNamedValueSet.Add
- ISWbemNamedValueSet.Add
- ISWbemNamedValueSet.Add
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 3aa1a3a982d7621c910a5afca95b26db1dd5f4d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544667"
---
# <a name="swbemnamedvaluesetadd-method"></a><span data-ttu-id="95968-104">SWbemNamedValueSet. Add (método)</span><span class="sxs-lookup"><span data-stu-id="95968-104">SWbemNamedValueSet.Add method</span></span>

<span data-ttu-id="95968-105">El método **Add** del objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) agrega un objeto [**SWbemNamedValue**](swbemnamedvalue.md) a la colección.</span><span class="sxs-lookup"><span data-stu-id="95968-105">The **Add** method of the [**SWbemNamedValueSet**](swbemnamedvalueset.md) object adds an [**SWbemNamedValue**](swbemnamedvalue.md) object to the collection.</span></span> <span data-ttu-id="95968-106">Si ya existe un elemento en la colección con el mismo nombre, el nuevo elemento lo reemplaza.</span><span class="sxs-lookup"><span data-stu-id="95968-106">If an element already exists in the collection with the same name, the new element replaces it.</span></span>

<span data-ttu-id="95968-107">Para obtener una explicación de esta sintaxis, vea [convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="95968-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="95968-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="95968-108">Syntax</span></span>


```VB
objNamedValue = .Add( _
  ByVal strName, _
  ByVal varVal, _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a><span data-ttu-id="95968-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="95968-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="95968-110">*strName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="95968-110">*strName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="95968-111">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="95968-111">Required.</span></span> <span data-ttu-id="95968-112">Nombre del nuevo valor.</span><span class="sxs-lookup"><span data-stu-id="95968-112">Name of the new value.</span></span>

</dd> <dt>

<span data-ttu-id="95968-113">*varVal* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="95968-113">*varVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="95968-114">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="95968-114">Required.</span></span> <span data-ttu-id="95968-115">Variante que representa el nuevo valor.</span><span class="sxs-lookup"><span data-stu-id="95968-115">Variant that represents the new value.</span></span>

</dd> <dt>

<span data-ttu-id="95968-116">*iFlags* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="95968-116">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="95968-117">Reserved y debe establecerse en cero si se especifica.</span><span class="sxs-lookup"><span data-stu-id="95968-117">Reserved and must be set to zero if specified.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="95968-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="95968-118">Return value</span></span>

<span data-ttu-id="95968-119">Si es correcto, este método devuelve el objeto [**SWbemNamedValue**](swbemnamedvalue.md) recién modificado o recién creado.</span><span class="sxs-lookup"><span data-stu-id="95968-119">If successful, this method returns the newly modified or newly created [**SWbemNamedValue**](swbemnamedvalue.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="95968-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="95968-120">Remarks</span></span>

<span data-ttu-id="95968-121">Para obtener ejemplos de cómo agregar y recuperar valores con nombre, vea [**SWbemNamedValue. Value**](swbemnamedvalue-value.md).</span><span class="sxs-lookup"><span data-stu-id="95968-121">For examples of adding and retrieving named values, see [**SWbemNamedValue.Value**](swbemnamedvalue-value.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="95968-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="95968-122">Requirements</span></span>



| <span data-ttu-id="95968-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="95968-123">Requirement</span></span> | <span data-ttu-id="95968-124">Value</span><span class="sxs-lookup"><span data-stu-id="95968-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="95968-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="95968-125">Minimum supported client</span></span><br/> | <span data-ttu-id="95968-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="95968-126">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="95968-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="95968-127">Minimum supported server</span></span><br/> | <span data-ttu-id="95968-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="95968-128">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="95968-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="95968-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="95968-130"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="95968-130"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="95968-131">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="95968-131">Type library</span></span><br/>             | <dl> <span data-ttu-id="95968-132"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="95968-132"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="95968-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="95968-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="95968-134"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="95968-134"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="95968-135">CLSID</span><span class="sxs-lookup"><span data-stu-id="95968-135">CLSID</span></span><br/>                    | <span data-ttu-id="95968-136">CLSID \_ SWbemNamedValueSet</span><span class="sxs-lookup"><span data-stu-id="95968-136">CLSID\_SWbemNamedValueSet</span></span><br/>                                                    |
| <span data-ttu-id="95968-137">IID</span><span class="sxs-lookup"><span data-stu-id="95968-137">IID</span></span><br/>                      | <span data-ttu-id="95968-138">\_ISWBEMNAMEDVALUESET IID</span><span class="sxs-lookup"><span data-stu-id="95968-138">IID\_ISWbemNamedValueSet</span></span><br/>                                                     |



## <a name="see-also"></a><span data-ttu-id="95968-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="95968-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95968-140">**SWbemNamedValueSet**</span><span class="sxs-lookup"><span data-stu-id="95968-140">**SWbemNamedValueSet**</span></span>](swbemnamedvalueset.md)
</dt> </dl>

 

 




