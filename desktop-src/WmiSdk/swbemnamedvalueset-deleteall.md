---
description: El método DeleteAll del objeto SWbemNamedValueSet quita todos los valores con nombre de la colección, con lo que se vacía.
ms.assetid: db5d2e68-028e-4902-ad42-0b46e1a96bcb
ms.tgt_platform: multiple
title: Método SWbemNamedValueSet. DeleteAll (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemNamedValueSet.DeleteAll
- ISWbemNamedValueSet.DeleteAll
- ISWbemNamedValueSet.DeleteAll
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 9df7b08dddf4cf9f1a687a262721452c0780267a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277322"
---
# <a name="swbemnamedvaluesetdeleteall-method"></a><span data-ttu-id="26d0c-103">SWbemNamedValueSet. DeleteAll, método</span><span class="sxs-lookup"><span data-stu-id="26d0c-103">SWbemNamedValueSet.DeleteAll method</span></span>

<span data-ttu-id="26d0c-104">El método **DeleteAll** del objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) quita todos los valores con nombre de la colección, con lo que se vacía.</span><span class="sxs-lookup"><span data-stu-id="26d0c-104">The **DeleteAll** method of the [**SWbemNamedValueSet**](swbemnamedvalueset.md) object removes all named values from the collection, thus emptying it.</span></span>

## <a name="syntax"></a><span data-ttu-id="26d0c-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="26d0c-105">Syntax</span></span>


```VB
SWbemNamedValueSet.DeleteAll()
```



## <a name="parameters"></a><span data-ttu-id="26d0c-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="26d0c-106">Parameters</span></span>

<span data-ttu-id="26d0c-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="26d0c-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="26d0c-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="26d0c-108">Return value</span></span>

<span data-ttu-id="26d0c-109">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="26d0c-109">This method does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="26d0c-110">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="26d0c-110">Error codes</span></span>

<span data-ttu-id="26d0c-111">Al completarse el método **DeleteAll** , el objeto **Err** puede contener el código de error siguiente.</span><span class="sxs-lookup"><span data-stu-id="26d0c-111">Upon completion of the **DeleteAll** method, the **Err** object may contain the error code below.</span></span>

<dl> <dt>

<span data-ttu-id="26d0c-112">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="26d0c-112">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="26d0c-113">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="26d0c-113">Unspecified error.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="26d0c-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="26d0c-114">Requirements</span></span>



| <span data-ttu-id="26d0c-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="26d0c-115">Requirement</span></span> | <span data-ttu-id="26d0c-116">Value</span><span class="sxs-lookup"><span data-stu-id="26d0c-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="26d0c-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="26d0c-117">Minimum supported client</span></span><br/> | <span data-ttu-id="26d0c-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="26d0c-118">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="26d0c-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="26d0c-119">Minimum supported server</span></span><br/> | <span data-ttu-id="26d0c-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="26d0c-120">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="26d0c-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="26d0c-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="26d0c-122"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="26d0c-122"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="26d0c-123">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="26d0c-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="26d0c-124"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="26d0c-124"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="26d0c-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="26d0c-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="26d0c-126"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="26d0c-126"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="26d0c-127">CLSID</span><span class="sxs-lookup"><span data-stu-id="26d0c-127">CLSID</span></span><br/>                    | <span data-ttu-id="26d0c-128">CLSID \_ SWbemNamedValueSet</span><span class="sxs-lookup"><span data-stu-id="26d0c-128">CLSID\_SWbemNamedValueSet</span></span><br/>                                                    |
| <span data-ttu-id="26d0c-129">IID</span><span class="sxs-lookup"><span data-stu-id="26d0c-129">IID</span></span><br/>                      | <span data-ttu-id="26d0c-130">\_ISWBEMNAMEDVALUESET IID</span><span class="sxs-lookup"><span data-stu-id="26d0c-130">IID\_ISWbemNamedValueSet</span></span><br/>                                                     |



## <a name="see-also"></a><span data-ttu-id="26d0c-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="26d0c-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26d0c-132">**SWbemNamedValueSet**</span><span class="sxs-lookup"><span data-stu-id="26d0c-132">**SWbemNamedValueSet**</span></span>](swbemnamedvalueset.md)
</dt> <dt>

[<span data-ttu-id="26d0c-133">**SWbemNamedValueSet. Remove**</span><span class="sxs-lookup"><span data-stu-id="26d0c-133">**SWbemNamedValueSet.Remove**</span></span>](swbemnamedvalueset-remove.md)
</dt> </dl>

 

 




