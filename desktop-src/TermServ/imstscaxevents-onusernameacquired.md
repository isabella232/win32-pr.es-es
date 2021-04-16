---
title: IMsTscAxEvents OnUserNameAcquired, método
description: Se llama cuando el control ha adquirido el nombre de usuario.
ms.assetid: 0653B28B-2D46-429F-8A36-5656786C0B26
ms.tgt_platform: multiple
keywords:
- Método OnUserNameAcquired Servicios de Escritorio remoto
- Método OnUserNameAcquired Servicios de Escritorio remoto, interfaz IMsTscAxEvents
- Interfaz IMsTscAxEvents Servicios de Escritorio remoto, método OnUserNameAcquired
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnUserNameAcquired
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf5d77f0eb739daa54f8385112b79f67f279eae9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686020"
---
# <a name="imstscaxeventsonusernameacquired-method"></a><span data-ttu-id="e6bb5-106">IMsTscAxEvents:: OnUserNameAcquired (método)</span><span class="sxs-lookup"><span data-stu-id="e6bb5-106">IMsTscAxEvents::OnUserNameAcquired method</span></span>

<span data-ttu-id="e6bb5-107">Se llama cuando el control ha adquirido el nombre de usuario.</span><span class="sxs-lookup"><span data-stu-id="e6bb5-107">Called when the user name has been acquired by the control.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6bb5-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e6bb5-108">Syntax</span></span>


```C++
void OnUserNameAcquired(
   BSTR bstrUserName
);
```



## <a name="parameters"></a><span data-ttu-id="e6bb5-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e6bb5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e6bb5-110">*bstrUserName*</span><span class="sxs-lookup"><span data-stu-id="e6bb5-110">*bstrUserName*</span></span> 
</dt> <dd>

<span data-ttu-id="e6bb5-111">Nombre de usuario.</span><span class="sxs-lookup"><span data-stu-id="e6bb5-111">The user name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e6bb5-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e6bb5-112">Return value</span></span>

<span data-ttu-id="e6bb5-113">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="e6bb5-113">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="e6bb5-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e6bb5-114">Requirements</span></span>



| <span data-ttu-id="e6bb5-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="e6bb5-115">Requirement</span></span> | <span data-ttu-id="e6bb5-116">Value</span><span class="sxs-lookup"><span data-stu-id="e6bb5-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e6bb5-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e6bb5-117">Minimum supported client</span></span><br/> | <span data-ttu-id="e6bb5-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e6bb5-118">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="e6bb5-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e6bb5-119">Minimum supported server</span></span><br/> | <span data-ttu-id="e6bb5-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e6bb5-120">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="e6bb5-121">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="e6bb5-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="e6bb5-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e6bb5-122"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="e6bb5-123">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e6bb5-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e6bb5-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e6bb5-124"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="e6bb5-125">IID</span><span class="sxs-lookup"><span data-stu-id="e6bb5-125">IID</span></span><br/>                      | <span data-ttu-id="e6bb5-126">IMsTscAxEvents se define como 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span><span class="sxs-lookup"><span data-stu-id="e6bb5-126">IMsTscAxEvents is defined as 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="e6bb5-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="e6bb5-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6bb5-128">**IMsTscAxEvents**</span><span class="sxs-lookup"><span data-stu-id="e6bb5-128">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

 





