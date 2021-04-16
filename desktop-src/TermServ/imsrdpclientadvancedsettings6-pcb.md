---
title: IMsRdpClientAdvancedSettings6 (propiedad de PCB)
description: Especifica la configuración del BLOB de preconexión (PCB) que se va a usar antes de la conexión para la transmisión al servidor. | IMsRdpClientAdvancedSettings6 (propiedad de PCB)
ms.assetid: 3f3e6f09-2c26-44ab-9bcc-2636b71b57e2
ms.tgt_platform: multiple
keywords:
- Propiedad PCB Servicios de Escritorio remoto
- Propiedad PCB Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings6
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings6, propiedad PCB
- Propiedad PCB Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings7
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings7, propiedad PCB
- Propiedad PCB Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings8
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings8, propiedad PCB
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings6.PCB
- IMsRdpClientAdvancedSettings6.get_PCB
- IMsRdpClientAdvancedSettings6.put_PCB
- IMsRdpClientAdvancedSettings7.PCB
- IMsRdpClientAdvancedSettings7.get_PCB
- IMsRdpClientAdvancedSettings7.put_PCB
- IMsRdpClientAdvancedSettings8.PCB
- IMsRdpClientAdvancedSettings8.get_PCB
- IMsRdpClientAdvancedSettings8.put_PCB
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7da9cfa12ec944ea8f745ec3399c2a53f6b7c6b5
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105678676"
---
# <a name="imsrdpclientadvancedsettings6pcb-property"></a><span data-ttu-id="75921-111">IMsRdpClientAdvancedSettings6::P propiedad CB</span><span class="sxs-lookup"><span data-stu-id="75921-111">IMsRdpClientAdvancedSettings6::PCB property</span></span>

<span data-ttu-id="75921-112">Especifica la configuración del BLOB de preconexión (PCB) que se va a usar antes de la conexión para la transmisión al servidor.</span><span class="sxs-lookup"><span data-stu-id="75921-112">Specifies the preconnection BLOB (PCB) setting to use prior to connecting for transmission to the server.</span></span>

<span data-ttu-id="75921-113">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="75921-113">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="75921-114">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="75921-114">Syntax</span></span>


```C++
HRESULT put_PCB(
  [in]          BSTR bstrPCB
);

HRESULT get_PCB(
  [out, retval] BSTR *pbstrPCB
);
```



## <a name="property-value"></a><span data-ttu-id="75921-115">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="75921-115">Property value</span></span>

<span data-ttu-id="75921-116">Especifica la configuración de BLOB que se va a usar antes de la conexión.</span><span class="sxs-lookup"><span data-stu-id="75921-116">Specifies the BLOB setting to use prior to connecting.</span></span>

## <a name="remarks"></a><span data-ttu-id="75921-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="75921-117">Remarks</span></span>

<span data-ttu-id="75921-118">Esta propiedad solo es compatible con clientes Conexión a Escritorio remoto 6,1 y 7,0.</span><span class="sxs-lookup"><span data-stu-id="75921-118">This property is only supported by Remote Desktop Connection 6.1 and 7.0 clients.</span></span>

<span data-ttu-id="75921-119">El servidor usa la configuración de BLOB para identificar el proceso de destino de la conexión.</span><span class="sxs-lookup"><span data-stu-id="75921-119">The server uses the BLOB setting to identify the target process for the connection.</span></span>

## <a name="requirements"></a><span data-ttu-id="75921-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="75921-120">Requirements</span></span>



| <span data-ttu-id="75921-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="75921-121">Requirement</span></span> | <span data-ttu-id="75921-122">Value</span><span class="sxs-lookup"><span data-stu-id="75921-122">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="75921-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="75921-123">Minimum supported client</span></span><br/> | <span data-ttu-id="75921-124">Windows 7</span><span class="sxs-lookup"><span data-stu-id="75921-124">Windows 7</span></span><br/>                                                                             |
| <span data-ttu-id="75921-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="75921-125">Minimum supported server</span></span><br/> | <span data-ttu-id="75921-126">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="75921-126">Windows Server 2008 R2</span></span><br/>                                                                |
| <span data-ttu-id="75921-127">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="75921-127">Type library</span></span><br/>             | <dl> <span data-ttu-id="75921-128"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="75921-128"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="75921-129">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="75921-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="75921-130"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="75921-130"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="75921-131">IID</span><span class="sxs-lookup"><span data-stu-id="75921-131">IID</span></span><br/>                      | <span data-ttu-id="75921-132">IID \_ IMsRdpClientAdvancedSettings6 se define como 222c4b5d-45d9-4df0-a7c6-60cf9089d285</span><span class="sxs-lookup"><span data-stu-id="75921-132">IID\_IMsRdpClientAdvancedSettings6 is defined as 222c4b5d-45d9-4df0-a7c6-60cf9089d285</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="75921-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="75921-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75921-134">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="75921-134">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="75921-135">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="75921-135">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="75921-136">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="75921-136">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> </dl>

 

 





