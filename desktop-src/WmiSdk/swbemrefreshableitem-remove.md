---
description: El método SWbemRefreshableItem. Remove quita el objeto SWbemRefreshableItem del objeto SWbemRefresher primario. Objeto SWbemRefreshableItem del objeto primario SWbemRefresher.
ms.assetid: 8d3f5e22-c343-4191-a20a-6bca2ec9b01a
ms.tgt_platform: multiple
title: Método SWbemRefreshableItem. Remove (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemRefreshableItem.Remove
- ISWbemRefreshableItem.Remove
- ISWbemRefreshableItem.Remove
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 028bff202108481ce498be02c6014141313f27cc
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105697934"
---
# <a name="swbemrefreshableitemremove-method"></a><span data-ttu-id="fab00-103">SWbemRefreshableItem. Remove (método)</span><span class="sxs-lookup"><span data-stu-id="fab00-103">SWbemRefreshableItem.Remove method</span></span>

<span data-ttu-id="fab00-104">El método **SWbemRefreshableItem. Remove** quita el objeto [**SWbemRefreshableItem**](swbemrefreshableitem.md) del objeto [**SWbemRefresher**](swbemrefresher.md) primario.</span><span class="sxs-lookup"><span data-stu-id="fab00-104">The **SWbemRefreshableItem.Remove** method removes the [**SWbemRefreshableItem**](swbemrefreshableitem.md) object from the parent [**SWbemRefresher**](swbemrefresher.md) object.</span></span>

<span data-ttu-id="fab00-105">Para obtener una explicación de esta sintaxis, vea [convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="fab00-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="fab00-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fab00-106">Syntax</span></span>


```VB
SWbemRefreshableItem.Remove( _
  [ ByVal lFlags ] _
)
```



## <a name="parameters"></a><span data-ttu-id="fab00-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fab00-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fab00-108">*lFlags* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="fab00-108">*lFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="fab00-109">Este parámetro debe establecerse en 0 (cero).</span><span class="sxs-lookup"><span data-stu-id="fab00-109">This parameter must be set to 0 (zero).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fab00-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fab00-110">Return value</span></span>

<span data-ttu-id="fab00-111">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="fab00-111">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="fab00-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fab00-112">Remarks</span></span>

<span data-ttu-id="fab00-113">**Códigos de error** Si el actualizador no tiene ningún elemento con el índice especificado, se genera **wbemErrNotFound** .</span><span class="sxs-lookup"><span data-stu-id="fab00-113">**Error Codes** If the refresher has no item with the specified index, **wbemErrNotFound** is generated.</span></span>

## <a name="requirements"></a><span data-ttu-id="fab00-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fab00-114">Requirements</span></span>



| <span data-ttu-id="fab00-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="fab00-115">Requirement</span></span> | <span data-ttu-id="fab00-116">Value</span><span class="sxs-lookup"><span data-stu-id="fab00-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fab00-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fab00-117">Minimum supported client</span></span><br/> | <span data-ttu-id="fab00-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fab00-118">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="fab00-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fab00-119">Minimum supported server</span></span><br/> | <span data-ttu-id="fab00-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fab00-120">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="fab00-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fab00-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="fab00-122"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="fab00-122"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="fab00-123">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="fab00-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="fab00-124"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="fab00-124"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="fab00-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="fab00-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fab00-126"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fab00-126"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="fab00-127">CLSID</span><span class="sxs-lookup"><span data-stu-id="fab00-127">CLSID</span></span><br/>                    | <span data-ttu-id="fab00-128">CLSID \_ SWbemRefreshableItem</span><span class="sxs-lookup"><span data-stu-id="fab00-128">CLSID\_SWbemRefreshableItem</span></span><br/>                                                  |
| <span data-ttu-id="fab00-129">IID</span><span class="sxs-lookup"><span data-stu-id="fab00-129">IID</span></span><br/>                      | <span data-ttu-id="fab00-130">\_ISWBEMREFRESHABLEITEM IID</span><span class="sxs-lookup"><span data-stu-id="fab00-130">IID\_ISWbemRefreshableItem</span></span><br/>                                                   |



## <a name="see-also"></a><span data-ttu-id="fab00-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="fab00-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fab00-132">**SWbemRefreshableItem**</span><span class="sxs-lookup"><span data-stu-id="fab00-132">**SWbemRefreshableItem**</span></span>](swbemrefreshableitem.md)
</dt> <dt>

[<span data-ttu-id="fab00-133">**SWbemRefresher**</span><span class="sxs-lookup"><span data-stu-id="fab00-133">**SWbemRefresher**</span></span>](swbemrefresher.md)
</dt> </dl>

 

 




