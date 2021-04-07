---
description: El método SWbemRefresher. Remove quita el objeto SWbemRefreshableItem con el índice especificado del actualizador.
ms.assetid: db5ac740-e2b3-4667-b511-d750cb092e0f
ms.tgt_platform: multiple
title: Método SWbemRefresher. Remove (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemRefresher.Remove
- ISWbemRefresher.Remove
- ISWbemRefresher.Remove
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 9504b81ce83a91695765e75e74de374437c188d4
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "104003394"
---
# <a name="swbemrefresherremove-method"></a><span data-ttu-id="9aeee-103">SWbemRefresher. Remove (método)</span><span class="sxs-lookup"><span data-stu-id="9aeee-103">SWbemRefresher.Remove method</span></span>

<span data-ttu-id="9aeee-104">El método **SWbemRefresher. Remove** quita el objeto [**SWbemRefreshableItem**](swbemrefreshableitem.md) con el índice especificado del actualizador.</span><span class="sxs-lookup"><span data-stu-id="9aeee-104">The **SWbemRefresher.Remove** method removes the [**SWbemRefreshableItem**](swbemrefreshableitem.md) object with the specified index from the refresher.</span></span> <span data-ttu-id="9aeee-105">El objeto **SWbemRefreshableItem** puede representar un solo objeto o un conjunto de objetos.</span><span class="sxs-lookup"><span data-stu-id="9aeee-105">The **SWbemRefreshableItem** object can represent either a single object or an object set.</span></span>

<span data-ttu-id="9aeee-106">Para obtener una explicación de esta sintaxis, vea [convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="9aeee-106">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="9aeee-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9aeee-107">Syntax</span></span>


```VB
objRefresher = .Remove( _
  ByVal LIndex, _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedvalueSet ] _
)
```



## <a name="parameters"></a><span data-ttu-id="9aeee-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9aeee-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9aeee-109">*LIndex*</span><span class="sxs-lookup"><span data-stu-id="9aeee-109">*LIndex*</span></span> 
</dt> <dd>

<span data-ttu-id="9aeee-110">Índice del elemento en el objeto [**SWbemRefresher**](swbemrefresher.md) .</span><span class="sxs-lookup"><span data-stu-id="9aeee-110">Index of the item in the [**SWbemRefresher**](swbemrefresher.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="9aeee-111">*iFlags* \[ opta\]</span><span class="sxs-lookup"><span data-stu-id="9aeee-111">*iFlags* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9aeee-112">Las marcas deben establecer T0 (cero).</span><span class="sxs-lookup"><span data-stu-id="9aeee-112">Flags must be set t0 (zero).</span></span>

</dd> <dt>

<span data-ttu-id="9aeee-113">*objWbemNamedvalueSet* \[ opta\]</span><span class="sxs-lookup"><span data-stu-id="9aeee-113">*objWbemNamedvalueSet* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9aeee-114">NULL.</span><span class="sxs-lookup"><span data-stu-id="9aeee-114">Null.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9aeee-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9aeee-115">Return value</span></span>

<span data-ttu-id="9aeee-116">Este método no tiene ningún valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="9aeee-116">This method has no return values.</span></span>

## <a name="remarks"></a><span data-ttu-id="9aeee-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9aeee-117">Remarks</span></span>

<span data-ttu-id="9aeee-118">**Códigos de error** Si el actualizador no tiene ningún elemento con el índice especificado, se genera **wbemErrNotFound** .</span><span class="sxs-lookup"><span data-stu-id="9aeee-118">**Error codes** If the refresher has no item with the specified index, **wbemErrNotFound** is generated.</span></span>

## <a name="requirements"></a><span data-ttu-id="9aeee-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9aeee-119">Requirements</span></span>



| <span data-ttu-id="9aeee-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="9aeee-120">Requirement</span></span> | <span data-ttu-id="9aeee-121">Value</span><span class="sxs-lookup"><span data-stu-id="9aeee-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9aeee-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9aeee-122">Minimum supported client</span></span><br/> | <span data-ttu-id="9aeee-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9aeee-123">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9aeee-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9aeee-124">Minimum supported server</span></span><br/> | <span data-ttu-id="9aeee-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9aeee-125">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9aeee-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9aeee-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="9aeee-127"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="9aeee-127"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="9aeee-128">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="9aeee-128">Type library</span></span><br/>             | <dl> <span data-ttu-id="9aeee-129"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="9aeee-129"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="9aeee-130">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="9aeee-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9aeee-131"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9aeee-131"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="9aeee-132">CLSID</span><span class="sxs-lookup"><span data-stu-id="9aeee-132">CLSID</span></span><br/>                    | <span data-ttu-id="9aeee-133">CLSID \_ SWbemRefresher</span><span class="sxs-lookup"><span data-stu-id="9aeee-133">CLSID\_SWbemRefresher</span></span><br/>                                                        |
| <span data-ttu-id="9aeee-134">IID</span><span class="sxs-lookup"><span data-stu-id="9aeee-134">IID</span></span><br/>                      | <span data-ttu-id="9aeee-135">\_ISWBEMREFRESHER IID</span><span class="sxs-lookup"><span data-stu-id="9aeee-135">IID\_ISWbemRefresher</span></span><br/>                                                         |



## <a name="see-also"></a><span data-ttu-id="9aeee-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="9aeee-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9aeee-137">**SWbemRefresher**</span><span class="sxs-lookup"><span data-stu-id="9aeee-137">**SWbemRefresher**</span></span>](swbemrefresher.md)
</dt> </dl>

 

 




