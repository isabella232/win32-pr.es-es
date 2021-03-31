---
title: IMsRdpDevice FriendlyName (propiedad)
description: Recupera el nombre para mostrar del dispositivo.
ms.assetid: ed27eacd-1d39-484c-8217-62ed608db050
ms.tgt_platform: multiple
keywords:
- FriendlyName (propiedad) Servicios de Escritorio remoto
- Propiedad FriendlyName Servicios de Escritorio remoto, interfaz IMsRdpDevice
- IMsRdpDevice interface Servicios de Escritorio remoto, FriendlyName (propiedad)
topic_type:
- apiref
api_name:
- IMsRdpDevice.FriendlyName
- IMsRdpDevice.get_FriendlyName
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6bf7963cf49945b886d72a622b517438e24d148f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801556"
---
# <a name="imsrdpdevicefriendlyname-property"></a><span data-ttu-id="113bc-106">IMsRdpDevice:: FriendlyName (propiedad)</span><span class="sxs-lookup"><span data-stu-id="113bc-106">IMsRdpDevice::FriendlyName property</span></span>

<span data-ttu-id="113bc-107">Recupera el nombre para mostrar del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="113bc-107">Retrieves the display name for the device.</span></span>

<span data-ttu-id="113bc-108">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="113bc-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="113bc-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="113bc-109">Syntax</span></span>


```C++
HRESULT get_FriendlyName(
  [out] BSTR *pFriendlyName
);
```



## <a name="property-value"></a><span data-ttu-id="113bc-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="113bc-110">Property value</span></span>

<span data-ttu-id="113bc-111">El nombre para mostrar.</span><span class="sxs-lookup"><span data-stu-id="113bc-111">The display name.</span></span>

## <a name="error-codes"></a><span data-ttu-id="113bc-112">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="113bc-112">Error codes</span></span>

<span data-ttu-id="113bc-113">Si el método se ejecuta correctamente, se devuelve **S \_ OK** .</span><span class="sxs-lookup"><span data-stu-id="113bc-113">If the method succeeds, **S\_OK** is returned.</span></span> <span data-ttu-id="113bc-114">Cualquier otro valor **HRESULT** indica que se produjo un error en la llamada.</span><span class="sxs-lookup"><span data-stu-id="113bc-114">Any other **HRESULT** value indicates that the call failed.</span></span>

## <a name="requirements"></a><span data-ttu-id="113bc-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="113bc-115">Requirements</span></span>



| <span data-ttu-id="113bc-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="113bc-116">Requirement</span></span> | <span data-ttu-id="113bc-117">Value</span><span class="sxs-lookup"><span data-stu-id="113bc-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="113bc-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="113bc-118">Minimum supported client</span></span><br/> | <span data-ttu-id="113bc-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="113bc-119">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="113bc-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="113bc-120">Minimum supported server</span></span><br/> | <span data-ttu-id="113bc-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="113bc-121">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="113bc-122">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="113bc-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="113bc-123"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="113bc-123"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="113bc-124">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="113bc-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="113bc-125"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="113bc-125"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="113bc-126">IID</span><span class="sxs-lookup"><span data-stu-id="113bc-126">IID</span></span><br/>                      | <span data-ttu-id="113bc-127">IID \_ IMsRdpDevice se define como 60c3b9c8-9e92-4f5e-a3e7-604a912093ea</span><span class="sxs-lookup"><span data-stu-id="113bc-127">IID\_IMsRdpDevice is defined as 60c3b9c8-9e92-4f5e-a3e7-604a912093ea</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="113bc-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="113bc-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="113bc-129">**IMsRdpDevice**</span><span class="sxs-lookup"><span data-stu-id="113bc-129">**IMsRdpDevice**</span></span>](imsrdpdevice.md)
</dt> </dl>

 

 





