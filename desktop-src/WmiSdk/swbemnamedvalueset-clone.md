---
description: El método Clone del objeto SWbemNamedValueSet devuelve un nuevo objeto que es un clon de la colección actual.
ms.assetid: 0e7fab2e-8175-45e5-aa70-1109502e2b3f
ms.tgt_platform: multiple
title: Método SWbemNamedValueSet. Clone (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemNamedValueSet.Clone
- ISWbemNamedValueSet.Clone
- ISWbemNamedValueSet.Clone
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 17678d36a553c84c008f606c647d7ff1fa9dfadc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103814323"
---
# <a name="swbemnamedvaluesetclone-method"></a><span data-ttu-id="7e720-103">SWbemNamedValueSet. Clone (método)</span><span class="sxs-lookup"><span data-stu-id="7e720-103">SWbemNamedValueSet.Clone method</span></span>

<span data-ttu-id="7e720-104">El método **Clone** del objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) devuelve un nuevo objeto que es un clon de la colección actual.</span><span class="sxs-lookup"><span data-stu-id="7e720-104">The **Clone** method of the [**SWbemNamedValueSet**](swbemnamedvalueset.md) object returns a new object that is a clone of the current collection.</span></span>

<span data-ttu-id="7e720-105">Para obtener una explicación de esta sintaxis, vea [convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="7e720-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="7e720-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7e720-106">Syntax</span></span>


```VB
objwbemNamedValueSet = .Clone( _
)
```



## <a name="parameters"></a><span data-ttu-id="7e720-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7e720-107">Parameters</span></span>

<span data-ttu-id="7e720-108">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="7e720-108">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7e720-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7e720-109">Return value</span></span>

<span data-ttu-id="7e720-110">Si se realiza correctamente, se devuelve un nuevo objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) .</span><span class="sxs-lookup"><span data-stu-id="7e720-110">If successful, a new [**SWbemNamedValueSet**](swbemnamedvalueset.md) object returns.</span></span>

## <a name="error-codes"></a><span data-ttu-id="7e720-111">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="7e720-111">Error codes</span></span>

<span data-ttu-id="7e720-112">Al finalizar el método **Clone** , el objeto **Err** puede contener uno de los códigos de error siguientes.</span><span class="sxs-lookup"><span data-stu-id="7e720-112">Upon completion of the **Clone** method, the **Err** object may contain one of the error codes below.</span></span>

<dl> <dt>

<span data-ttu-id="7e720-113">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="7e720-113">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="7e720-114">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="7e720-114">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="7e720-115">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="7e720-115">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="7e720-116">No hay suficiente memoria para clonar el objeto.</span><span class="sxs-lookup"><span data-stu-id="7e720-116">Not enough memory to clone the object.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7e720-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7e720-117">Remarks</span></span>

<span data-ttu-id="7e720-118">Use este método para duplicar una colección [**SWbemNamedValueSet**](swbemnamedvalueset.md) .</span><span class="sxs-lookup"><span data-stu-id="7e720-118">Use this method to duplicate an [**SWbemNamedValueSet**](swbemnamedvalueset.md) collection.</span></span>

## <a name="requirements"></a><span data-ttu-id="7e720-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7e720-119">Requirements</span></span>



| <span data-ttu-id="7e720-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="7e720-120">Requirement</span></span> | <span data-ttu-id="7e720-121">Value</span><span class="sxs-lookup"><span data-stu-id="7e720-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7e720-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7e720-122">Minimum supported client</span></span><br/> | <span data-ttu-id="7e720-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7e720-123">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="7e720-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7e720-124">Minimum supported server</span></span><br/> | <span data-ttu-id="7e720-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7e720-125">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="7e720-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7e720-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="7e720-127"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="7e720-127"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="7e720-128">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="7e720-128">Type library</span></span><br/>             | <dl> <span data-ttu-id="7e720-129"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="7e720-129"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="7e720-130">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="7e720-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7e720-131"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7e720-131"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="7e720-132">CLSID</span><span class="sxs-lookup"><span data-stu-id="7e720-132">CLSID</span></span><br/>                    | <span data-ttu-id="7e720-133">CLSID \_ SWbemNamedValueSet</span><span class="sxs-lookup"><span data-stu-id="7e720-133">CLSID\_SWbemNamedValueSet</span></span><br/>                                                    |
| <span data-ttu-id="7e720-134">IID</span><span class="sxs-lookup"><span data-stu-id="7e720-134">IID</span></span><br/>                      | <span data-ttu-id="7e720-135">\_ISWBEMNAMEDVALUESET IID</span><span class="sxs-lookup"><span data-stu-id="7e720-135">IID\_ISWbemNamedValueSet</span></span><br/>                                                     |



## <a name="see-also"></a><span data-ttu-id="7e720-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="7e720-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e720-137">**SWbemNamedValueSet**</span><span class="sxs-lookup"><span data-stu-id="7e720-137">**SWbemNamedValueSet**</span></span>](swbemnamedvalueset.md)
</dt> </dl>

 

 




