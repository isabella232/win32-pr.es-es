---
title: Propiedad AdvancedSettings8 de IMsRdpClient7
description: Recupera un objeto que admite la interfaz IMsRdpClientAdvancedSettings7.
ms.assetid: e3bb3b74-52db-4ec2-999c-9d12c24f65be
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad AdvancedSettings8
- Propiedad AdvancedSettings8 Servicios de Escritorio remoto, interfaz IMsRdpClient7
- Servicios de Escritorio remoto de la interfaz IMsRdpClient7, propiedad AdvancedSettings8
- Propiedad AdvancedSettings8 Servicios de Escritorio remoto, interfaz IMsRdpClient8
- Servicios de Escritorio remoto de la interfaz IMsRdpClient8, propiedad AdvancedSettings8
- Propiedad AdvancedSettings8 Servicios de Escritorio remoto, interfaz IMsRdpClient9
- Servicios de Escritorio remoto de la interfaz IMsRdpClient9, propiedad AdvancedSettings8
- Propiedad AdvancedSettings8 Servicios de Escritorio remoto, interfaz IMsRdpClient10
- Servicios de Escritorio remoto de la interfaz IMsRdpClient10, propiedad AdvancedSettings8
topic_type:
- apiref
api_name:
- IMsRdpClient7.AdvancedSettings8
- IMsRdpClient7.get_AdvancedSettings8
- IMsRdpClient8.AdvancedSettings8
- IMsRdpClient8.get_AdvancedSettings8
- IMsRdpClient9.AdvancedSettings8
- IMsRdpClient9.get_AdvancedSettings8
- IMsRdpClient10.AdvancedSettings8
- IMsRdpClient10.get_AdvancedSettings8
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 887306216682ba1555739a4258b8337694fabe0d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104149998"
---
# <a name="imsrdpclient7advancedsettings8-property"></a><span data-ttu-id="54725-112">IMsRdpClient7:: AdvancedSettings8 (propiedad)</span><span class="sxs-lookup"><span data-stu-id="54725-112">IMsRdpClient7::AdvancedSettings8 property</span></span>

<span data-ttu-id="54725-113">Recupera un objeto que admite la interfaz [**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md) .</span><span class="sxs-lookup"><span data-stu-id="54725-113">Retrieves an object that supports the [**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md) interface.</span></span>

<span data-ttu-id="54725-114">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="54725-114">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="54725-115">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="54725-115">Syntax</span></span>


```C++
HRESULT get_AdvancedSettings8(
  [out, retval] IMsRdpClientAdvancedSettings7 **ppAdvSettings
);
```



## <a name="property-value"></a><span data-ttu-id="54725-116">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="54725-116">Property value</span></span>

<span data-ttu-id="54725-117">Dirección de un puntero de interfaz [**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md) que recibe el objeto.</span><span class="sxs-lookup"><span data-stu-id="54725-117">The address of an [**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md) interface pointer that receives the object.</span></span>

## <a name="requirements"></a><span data-ttu-id="54725-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="54725-118">Requirements</span></span>



| <span data-ttu-id="54725-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="54725-119">Requirement</span></span> | <span data-ttu-id="54725-120">Value</span><span class="sxs-lookup"><span data-stu-id="54725-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="54725-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="54725-121">Minimum supported client</span></span><br/> | <span data-ttu-id="54725-122">Windows 7</span><span class="sxs-lookup"><span data-stu-id="54725-122">Windows 7</span></span><br/>                                                                   |
| <span data-ttu-id="54725-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="54725-123">Minimum supported server</span></span><br/> | <span data-ttu-id="54725-124">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="54725-124">Windows Server 2008 R2</span></span><br/>                                                      |
| <span data-ttu-id="54725-125">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="54725-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="54725-126"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="54725-126"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="54725-127">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="54725-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="54725-128"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="54725-128"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="54725-129">IID</span><span class="sxs-lookup"><span data-stu-id="54725-129">IID</span></span><br/>                      | <span data-ttu-id="54725-130">IID \_ IMsRdpClient7 se define como b2a5b5ce-3461-444A-91d4-add26d070638</span><span class="sxs-lookup"><span data-stu-id="54725-130">IID\_IMsRdpClient7 is defined as b2a5b5ce-3461-444a-91d4-add26d070638</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="54725-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="54725-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54725-132">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="54725-132">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="54725-133">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="54725-133">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="54725-134">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="54725-134">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="54725-135">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="54725-135">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> </dl>

 

 





