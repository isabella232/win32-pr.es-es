---
title: Propiedad AdvancedSettings9 de IMsRdpClient8
description: Contiene un objeto que admite la interfaz IMsRdpClientAdvancedSettings8.
ms.assetid: eb7bf118-15e7-4a11-91b1-e48f18afb436
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad AdvancedSettings9
- Propiedad AdvancedSettings9 Servicios de Escritorio remoto, interfaz IMsRdpClient8
- Servicios de Escritorio remoto de la interfaz IMsRdpClient8, propiedad AdvancedSettings9
- Propiedad AdvancedSettings9 Servicios de Escritorio remoto, interfaz IMsRdpClient9
- Servicios de Escritorio remoto de la interfaz IMsRdpClient9, propiedad AdvancedSettings9
- Propiedad AdvancedSettings9 Servicios de Escritorio remoto, interfaz IMsRdpClient10
- Servicios de Escritorio remoto de la interfaz IMsRdpClient10, propiedad AdvancedSettings9
topic_type:
- apiref
api_name:
- IMsRdpClient8.AdvancedSettings9
- IMsRdpClient8.get_AdvancedSettings9
- IMsRdpClient9.AdvancedSettings9
- IMsRdpClient9.get_AdvancedSettings9
- IMsRdpClient10.AdvancedSettings9
- IMsRdpClient10.get_AdvancedSettings9
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5fce4c6f07b0c6c798d613e5312b3ae2b258c9c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686242"
---
# <a name="imsrdpclient8advancedsettings9-property"></a><span data-ttu-id="7efaf-110">IMsRdpClient8:: AdvancedSettings9 (propiedad)</span><span class="sxs-lookup"><span data-stu-id="7efaf-110">IMsRdpClient8::AdvancedSettings9 property</span></span>

<span data-ttu-id="7efaf-111">Contiene un objeto que admite la interfaz [**IMsRdpClientAdvancedSettings8**](imsrdpclientadvancedsettings8.md) .</span><span class="sxs-lookup"><span data-stu-id="7efaf-111">Contains an object that supports the [**IMsRdpClientAdvancedSettings8**](imsrdpclientadvancedsettings8.md) interface.</span></span>

<span data-ttu-id="7efaf-112">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="7efaf-112">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="7efaf-113">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7efaf-113">Syntax</span></span>


```C++
HRESULT get_AdvancedSettings9(
  [out, retval] IMsRdpClientAdvancedSettings8 **ppAdvSettings
);
```



## <a name="property-value"></a><span data-ttu-id="7efaf-114">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="7efaf-114">Property value</span></span>

<span data-ttu-id="7efaf-115">Una interfaz [**IMsRdpClientAdvancedSettings8**](imsrdpclientadvancedsettings8.md) que representa el objeto de configuración.</span><span class="sxs-lookup"><span data-stu-id="7efaf-115">An [**IMsRdpClientAdvancedSettings8**](imsrdpclientadvancedsettings8.md) interface that represents the settings object.</span></span>

## <a name="requirements"></a><span data-ttu-id="7efaf-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7efaf-116">Requirements</span></span>



| <span data-ttu-id="7efaf-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="7efaf-117">Requirement</span></span> | <span data-ttu-id="7efaf-118">Value</span><span class="sxs-lookup"><span data-stu-id="7efaf-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7efaf-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7efaf-119">Minimum supported client</span></span><br/> | <span data-ttu-id="7efaf-120">Windows 8</span><span class="sxs-lookup"><span data-stu-id="7efaf-120">Windows 8</span></span><br/>                                                                   |
| <span data-ttu-id="7efaf-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7efaf-121">Minimum supported server</span></span><br/> | <span data-ttu-id="7efaf-122">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7efaf-122">Windows Server 2012</span></span><br/>                                                         |
| <span data-ttu-id="7efaf-123">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="7efaf-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="7efaf-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7efaf-124"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="7efaf-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="7efaf-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7efaf-126"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7efaf-126"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="7efaf-127">IID</span><span class="sxs-lookup"><span data-stu-id="7efaf-127">IID</span></span><br/>                      | <span data-ttu-id="7efaf-128">IID \_ IMsRdpClient8 se define como 4247E044-9271-43A9-BC49-E2AD9E855D62</span><span class="sxs-lookup"><span data-stu-id="7efaf-128">IID\_IMsRdpClient8 is defined as 4247E044-9271-43A9-BC49-E2AD9E855D62</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="7efaf-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="7efaf-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7efaf-130">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="7efaf-130">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="7efaf-131">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="7efaf-131">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="7efaf-132">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="7efaf-132">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> </dl>

 

 





