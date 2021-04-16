---
title: Propiedad EnableCredSspSupport de IMsRdpClientAdvancedSettings6
description: Especifica si el proveedor de servicios de seguridad de credenciales (CredSSP) está habilitado para esta conexión.
ms.assetid: 3BC8A265-7AEA-4C9C-9730-7710E1A3159D
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad EnableCredSspSupport
- Propiedad EnableCredSspSupport Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings6
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings6, propiedad EnableCredSspSupport
- Propiedad EnableCredSspSupport Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings7
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings7, propiedad EnableCredSspSupport
- Propiedad EnableCredSspSupport Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings8
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings8, propiedad EnableCredSspSupport
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings6.EnableCredSspSupport
- IMsRdpClientAdvancedSettings6.get_EnableCredSspSupport
- IMsRdpClientAdvancedSettings6.put_EnableCredSspSupport
- IMsRdpClientAdvancedSettings7.EnableCredSspSupport
- IMsRdpClientAdvancedSettings7.get_EnableCredSspSupport
- IMsRdpClientAdvancedSettings7.put_EnableCredSspSupport
- IMsRdpClientAdvancedSettings8.EnableCredSspSupport
- IMsRdpClientAdvancedSettings8.get_EnableCredSspSupport
- IMsRdpClientAdvancedSettings8.put_EnableCredSspSupport
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b73ad2b024cd0f8bbcafd6ba05be093c5953d54
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534143"
---
# <a name="imsrdpclientadvancedsettings6enablecredsspsupport-property"></a><span data-ttu-id="ab713-110">IMsRdpClientAdvancedSettings6:: EnableCredSspSupport (propiedad)</span><span class="sxs-lookup"><span data-stu-id="ab713-110">IMsRdpClientAdvancedSettings6::EnableCredSspSupport property</span></span>

<span data-ttu-id="ab713-111">Especifica si el proveedor de servicios de seguridad de credenciales (CredSSP) está habilitado para esta conexión.</span><span class="sxs-lookup"><span data-stu-id="ab713-111">Specifies whether the Credential Security Service Provider (CredSSP) is enabled for this connection.</span></span>

<span data-ttu-id="ab713-112">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="ab713-112">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab713-113">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ab713-113">Syntax</span></span>


```C++
HRESULT put_EnableCredSspSupport(
  [in]  VARIANT_BOOL fEnableSupport
);

HRESULT get_EnableCredSspSupport(
  [out] VARIANT_BOOL *pfEnableSupport
);
```



## <a name="property-value"></a><span data-ttu-id="ab713-114">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="ab713-114">Property value</span></span>

<span data-ttu-id="ab713-115">Especifica si CredSSP está habilitado para esta conexión.</span><span class="sxs-lookup"><span data-stu-id="ab713-115">Specifies whether CredSSP is enabled for this connection.</span></span> <span data-ttu-id="ab713-116">Establézcalo en **Variant \_ true** para habilitar CredSSP o **Variant \_ false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="ab713-116">Set to **VARIANT\_TRUE** to enable CredSSP or **VARIANT\_FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="ab713-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ab713-117">Remarks</span></span>

<span data-ttu-id="ab713-118">Esta propiedad solo es compatible con clientes Conexión a Escritorio remoto 6,1 y 7,0.</span><span class="sxs-lookup"><span data-stu-id="ab713-118">This property is only supported by Remote Desktop Connection 6.1 and 7.0 clients.</span></span>

## <a name="requirements"></a><span data-ttu-id="ab713-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ab713-119">Requirements</span></span>



| <span data-ttu-id="ab713-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="ab713-120">Requirement</span></span> | <span data-ttu-id="ab713-121">Value</span><span class="sxs-lookup"><span data-stu-id="ab713-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ab713-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ab713-122">Minimum supported client</span></span><br/> | <span data-ttu-id="ab713-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ab713-123">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="ab713-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ab713-124">Minimum supported server</span></span><br/> | <span data-ttu-id="ab713-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ab713-125">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="ab713-126">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="ab713-126">Type library</span></span><br/>             | <dl> <span data-ttu-id="ab713-127"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ab713-127"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="ab713-128">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ab713-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ab713-129"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ab713-129"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="ab713-130">IID</span><span class="sxs-lookup"><span data-stu-id="ab713-130">IID</span></span><br/>                      | <span data-ttu-id="ab713-131">IID \_ IMsRdpClientAdvancedSettings6 se define como 222c4b5d-45d9-4df0-a7c6-60cf9089d285</span><span class="sxs-lookup"><span data-stu-id="ab713-131">IID\_IMsRdpClientAdvancedSettings6 is defined as 222c4b5d-45d9-4df0-a7c6-60cf9089d285</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ab713-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="ab713-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab713-133">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="ab713-133">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="ab713-134">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="ab713-134">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="ab713-135">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="ab713-135">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> </dl>

 

 





