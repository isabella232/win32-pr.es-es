---
title: IMsTscAxEvents unwarning (método)
description: Se llama cuando el control de cliente encuentra una condición de error que no es grave.
ms.assetid: af43d3aa-0ae8-4721-b85d-bb043b20dc40
ms.tgt_platform: multiple
keywords:
- Método de advertencia Servicios de Escritorio remoto
- Método de advertencia Servicios de Escritorio remoto, interfaz IMsTscAxEvents
- Interfaz IMsTscAxEvents Servicios de Escritorio remoto, método de advertencia
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnWarning
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aadc7013f34c93406f93841896a9041bbb1b7cfb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802713"
---
# <a name="imstscaxeventsonwarning-method"></a><span data-ttu-id="4f02b-106">IMsTscAxEvents:: unwarning (método)</span><span class="sxs-lookup"><span data-stu-id="4f02b-106">IMsTscAxEvents::OnWarning method</span></span>

<span data-ttu-id="4f02b-107">Se llama cuando el control de cliente encuentra una condición de error que no es grave.</span><span class="sxs-lookup"><span data-stu-id="4f02b-107">Called when the client control encounters an error condition that is not fatal.</span></span>

## <a name="syntax"></a><span data-ttu-id="4f02b-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4f02b-108">Syntax</span></span>


```C++
void OnWarning(
  [in] long warningCode
);
```



## <a name="parameters"></a><span data-ttu-id="4f02b-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4f02b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4f02b-110">*warningCode* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4f02b-110">*warningCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4f02b-111">Código de error.</span><span class="sxs-lookup"><span data-stu-id="4f02b-111">The error code.</span></span>

<dt>

<span id="1"></span>

<span data-ttu-id="4f02b-112"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="4f02b-112"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="4f02b-113">La caché de mapas de bits está dañada.</span><span class="sxs-lookup"><span data-stu-id="4f02b-113">Bitmap cache is corrupt.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4f02b-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4f02b-114">Return value</span></span>

<span data-ttu-id="4f02b-115">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="4f02b-115">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4f02b-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4f02b-116">Remarks</span></span>

<span data-ttu-id="4f02b-117">Para obtener más información acerca de Conexión web a Escritorio remoto, consulte [Requirements for conexión web a escritorio remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="4f02b-117">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4f02b-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4f02b-118">Requirements</span></span>



| <span data-ttu-id="4f02b-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="4f02b-119">Requirement</span></span> | <span data-ttu-id="4f02b-120">Value</span><span class="sxs-lookup"><span data-stu-id="4f02b-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4f02b-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4f02b-121">Minimum supported client</span></span><br/> | <span data-ttu-id="4f02b-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4f02b-122">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="4f02b-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4f02b-123">Minimum supported server</span></span><br/> | <span data-ttu-id="4f02b-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4f02b-124">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="4f02b-125">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="4f02b-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="4f02b-126"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4f02b-126"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="4f02b-127">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="4f02b-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4f02b-128"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4f02b-128"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="4f02b-129">IID</span><span class="sxs-lookup"><span data-stu-id="4f02b-129">IID</span></span><br/>                      | <span data-ttu-id="4f02b-130">IMsTscAxEvents se define como 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span><span class="sxs-lookup"><span data-stu-id="4f02b-130">IMsTscAxEvents is defined as 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="4f02b-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="4f02b-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f02b-132">**IMsTscAxEvents**</span><span class="sxs-lookup"><span data-stu-id="4f02b-132">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

 





