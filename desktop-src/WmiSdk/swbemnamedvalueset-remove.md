---
description: El método Remove del objeto SWbemNamedValueSet elimina un valor con nombre del contexto.
ms.assetid: 8cb353fb-c6d7-41d9-a2d0-ff1ad37264e4
ms.tgt_platform: multiple
title: Método SWbemNamedValueSet. Remove (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemNamedValueSet.Remove
- ISWbemNamedValueSet.Remove
- ISWbemNamedValueSet.Remove
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: d41ecd7d28b95534c8e6d88d1c57756c269cf790
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706927"
---
# <a name="swbemnamedvaluesetremove-method"></a><span data-ttu-id="13438-103">SWbemNamedValueSet. Remove (método)</span><span class="sxs-lookup"><span data-stu-id="13438-103">SWbemNamedValueSet.Remove method</span></span>

<span data-ttu-id="13438-104">El método **Remove** del objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) elimina un valor con nombre del contexto.</span><span class="sxs-lookup"><span data-stu-id="13438-104">The **Remove** method of the [**SWbemNamedValueSet**](swbemnamedvalueset.md) object deletes a named value from the context.</span></span>

<span data-ttu-id="13438-105">Para obtener una explicación de esta sintaxis, vea [convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="13438-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="13438-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="13438-106">Syntax</span></span>


```VB
SWbemNamedValueSet.Remove( _
  ByVal strName, _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a><span data-ttu-id="13438-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="13438-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="13438-108">*strName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="13438-108">*strName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="13438-109">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="13438-109">Required.</span></span> <span data-ttu-id="13438-110">Nombre del valor que se va a quitar.</span><span class="sxs-lookup"><span data-stu-id="13438-110">Name of the value to remove.</span></span>

</dd> <dt>

<span data-ttu-id="13438-111">*iFlags* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="13438-111">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="13438-112">Reservado.</span><span class="sxs-lookup"><span data-stu-id="13438-112">Reserved.</span></span> <span data-ttu-id="13438-113">Este valor debe ser cero si se especifica.</span><span class="sxs-lookup"><span data-stu-id="13438-113">This value must be zero if specified.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="13438-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="13438-114">Return value</span></span>

<span data-ttu-id="13438-115">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="13438-115">This method does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="13438-116">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="13438-116">Error codes</span></span>

<span data-ttu-id="13438-117">Al completarse el método **Remove** , el objeto **Err** puede contener uno de los códigos de error de la lista siguiente.</span><span class="sxs-lookup"><span data-stu-id="13438-117">Upon completion of the **Remove** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="13438-118">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="13438-118">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="13438-119">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="13438-119">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="13438-120">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="13438-120">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="13438-121">Se especificó un parámetro no válido o no se pudo analizar el espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="13438-121">An invalid parameter was specified, or the namespace could not be parsed.</span></span>

</dd> <dt>

<span data-ttu-id="13438-122">**wbemErrNotFound** -2147749890 (0x80041002)</span><span class="sxs-lookup"><span data-stu-id="13438-122">**wbemErrNotFound** - 2147749890 (0x80041002)</span></span>
</dt> <dd>

<span data-ttu-id="13438-123">No se encontró el elemento solicitado.</span><span class="sxs-lookup"><span data-stu-id="13438-123">The requested item was not found.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="13438-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="13438-124">Requirements</span></span>



| <span data-ttu-id="13438-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="13438-125">Requirement</span></span> | <span data-ttu-id="13438-126">Value</span><span class="sxs-lookup"><span data-stu-id="13438-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="13438-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="13438-127">Minimum supported client</span></span><br/> | <span data-ttu-id="13438-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="13438-128">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="13438-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="13438-129">Minimum supported server</span></span><br/> | <span data-ttu-id="13438-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="13438-130">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="13438-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="13438-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="13438-132"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="13438-132"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="13438-133">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="13438-133">Type library</span></span><br/>             | <dl> <span data-ttu-id="13438-134"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="13438-134"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="13438-135">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="13438-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="13438-136"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="13438-136"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="13438-137">CLSID</span><span class="sxs-lookup"><span data-stu-id="13438-137">CLSID</span></span><br/>                    | <span data-ttu-id="13438-138">CLSID \_ SWbemNamedValueSet</span><span class="sxs-lookup"><span data-stu-id="13438-138">CLSID\_SWbemNamedValueSet</span></span><br/>                                                    |
| <span data-ttu-id="13438-139">IID</span><span class="sxs-lookup"><span data-stu-id="13438-139">IID</span></span><br/>                      | <span data-ttu-id="13438-140">\_ISWBEMNAMEDVALUESET IID</span><span class="sxs-lookup"><span data-stu-id="13438-140">IID\_ISWbemNamedValueSet</span></span><br/>                                                     |



## <a name="see-also"></a><span data-ttu-id="13438-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="13438-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13438-142">**SWbemNamedValueSet**</span><span class="sxs-lookup"><span data-stu-id="13438-142">**SWbemNamedValueSet**</span></span>](swbemnamedvalueset.md)
</dt> </dl>

 

 




