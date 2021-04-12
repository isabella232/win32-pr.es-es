---
description: El método SWbemRefresher. Item devuelve el SWbemRefreshableItem especificado de la colección. SWbemRefreshableItem de la colección.
ms.assetid: 8ae3dea5-0582-422e-9cd8-b6d91b41588a
ms.tgt_platform: multiple
title: Método SWbemRefresher. Item (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemRefresher.Item
- ISWbemRefresher.Item
- ISWbemRefresher.Item
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: cfdbb592e6358fb1f8c5f3d45bb7e6bb780641c3
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "104279796"
---
# <a name="swbemrefresheritem-method"></a><span data-ttu-id="c7477-103">SWbemRefresher. Item (método)</span><span class="sxs-lookup"><span data-stu-id="c7477-103">SWbemRefresher.Item method</span></span>

<span data-ttu-id="c7477-104">El método **SWbemRefresher. Item** devuelve el [**SWbemRefreshableItem**](swbemrefreshableitem.md) especificado de la colección.</span><span class="sxs-lookup"><span data-stu-id="c7477-104">The **SWbemRefresher.Item** method returns the specified [**SWbemRefreshableItem**](swbemrefreshableitem.md) from the collection.</span></span>

<span data-ttu-id="c7477-105">Para obtener una explicación de esta sintaxis, vea [convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="c7477-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="c7477-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c7477-106">Syntax</span></span>


```VB
objItem = .Item( _
  ByVal lIndex _
)
```



## <a name="parameters"></a><span data-ttu-id="c7477-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c7477-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c7477-108">*lIndex*</span><span class="sxs-lookup"><span data-stu-id="c7477-108">*lIndex*</span></span> 
</dt> <dd>

<span data-ttu-id="c7477-109">Valor de índice del elemento de la colección.</span><span class="sxs-lookup"><span data-stu-id="c7477-109">Index value of the item in the collection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c7477-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c7477-110">Return value</span></span>

<span data-ttu-id="c7477-111">Si la llamada se realiza correctamente, se devuelve el objeto [**SWbemRefreshableItem**](swbemrefreshableitem.md) especificado.</span><span class="sxs-lookup"><span data-stu-id="c7477-111">If the call is successful, the specified [**SWbemRefreshableItem**](swbemrefreshableitem.md) object is returned.</span></span>

## <a name="error-codes"></a><span data-ttu-id="c7477-112">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="c7477-112">Error codes</span></span>

<span data-ttu-id="c7477-113">Si el actualizador no tiene ningún elemento con el índice especificado, se genera **wbemErrNotFound** .</span><span class="sxs-lookup"><span data-stu-id="c7477-113">If the refresher has no item with the specified index, **wbemErrNotFound** is generated.</span></span>

## <a name="requirements"></a><span data-ttu-id="c7477-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c7477-114">Requirements</span></span>



| <span data-ttu-id="c7477-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="c7477-115">Requirement</span></span> | <span data-ttu-id="c7477-116">Value</span><span class="sxs-lookup"><span data-stu-id="c7477-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c7477-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c7477-117">Minimum supported client</span></span><br/> | <span data-ttu-id="c7477-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c7477-118">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c7477-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c7477-119">Minimum supported server</span></span><br/> | <span data-ttu-id="c7477-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c7477-120">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c7477-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c7477-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="c7477-122"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="c7477-122"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="c7477-123">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="c7477-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="c7477-124"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="c7477-124"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="c7477-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c7477-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c7477-126"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c7477-126"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="c7477-127">CLSID</span><span class="sxs-lookup"><span data-stu-id="c7477-127">CLSID</span></span><br/>                    | <span data-ttu-id="c7477-128">CLSID \_ SWbemRefresher</span><span class="sxs-lookup"><span data-stu-id="c7477-128">CLSID\_SWbemRefresher</span></span><br/>                                                        |
| <span data-ttu-id="c7477-129">IID</span><span class="sxs-lookup"><span data-stu-id="c7477-129">IID</span></span><br/>                      | <span data-ttu-id="c7477-130">\_ISWBEMREFRESHER IID</span><span class="sxs-lookup"><span data-stu-id="c7477-130">IID\_ISWbemRefresher</span></span><br/>                                                         |



## <a name="see-also"></a><span data-ttu-id="c7477-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="c7477-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7477-132">**SWbemRefresher**</span><span class="sxs-lookup"><span data-stu-id="c7477-132">**SWbemRefresher**</span></span>](swbemrefresher.md)
</dt> </dl>

 

 




