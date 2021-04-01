---
title: Propiedad AuthenticationType IMsRdpClientAdvancedSettings6
description: Especifica el tipo de autenticación utilizado para esta conexión.
ms.assetid: A6DAAE0A-5045-4C2C-B065-AB5BFB39F955
ms.tgt_platform: multiple
keywords:
- Propiedad AuthenticationType Servicios de Escritorio remoto
- Propiedad AuthenticationType Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings6
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings6, propiedad AuthenticationType
- Propiedad AuthenticationType Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings7
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings7, propiedad AuthenticationType
- Propiedad AuthenticationType Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings8
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings8, propiedad AuthenticationType
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings6.AuthenticationType
- IMsRdpClientAdvancedSettings6.get_AuthenticationType
- IMsRdpClientAdvancedSettings7.AuthenticationType
- IMsRdpClientAdvancedSettings7.get_AuthenticationType
- IMsRdpClientAdvancedSettings8.AuthenticationType
- IMsRdpClientAdvancedSettings8.get_AuthenticationType
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08c59239570538b690866e499ee942b6635055c9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150289"
---
# <a name="imsrdpclientadvancedsettings6authenticationtype-property"></a><span data-ttu-id="63ecf-110">IMsRdpClientAdvancedSettings6:: AuthenticationType (propiedad)</span><span class="sxs-lookup"><span data-stu-id="63ecf-110">IMsRdpClientAdvancedSettings6::AuthenticationType property</span></span>

<span data-ttu-id="63ecf-111">Especifica el tipo de autenticación utilizado para esta conexión.</span><span class="sxs-lookup"><span data-stu-id="63ecf-111">Specifies the type of authentication used for this connection.</span></span>

<span data-ttu-id="63ecf-112">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="63ecf-112">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="63ecf-113">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="63ecf-113">Syntax</span></span>


```C++
HRESULT get_AuthenticationType(
  [out] UINT *puiAuthType
);
```



## <a name="property-value"></a><span data-ttu-id="63ecf-114">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="63ecf-114">Property value</span></span>

<span data-ttu-id="63ecf-115">Recibe un valor que especifica el tipo de autenticación utilizado para esta conexión.</span><span class="sxs-lookup"><span data-stu-id="63ecf-115">Receives a value that specifies the type of authentication used for this connection.</span></span> <span data-ttu-id="63ecf-116">Puede ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="63ecf-116">This can be one of the following values.</span></span>

<dt>

<span data-ttu-id="63ecf-117">0</span><span class="sxs-lookup"><span data-stu-id="63ecf-117">0</span></span>
</dt> <dd>

<span data-ttu-id="63ecf-118">No se usa autenticación.</span><span class="sxs-lookup"><span data-stu-id="63ecf-118">No authentication is used.</span></span>

</dd> <dt>

<span data-ttu-id="63ecf-119">1</span><span class="sxs-lookup"><span data-stu-id="63ecf-119">1</span></span>
</dt> <dd>

<span data-ttu-id="63ecf-120">Se usa la autenticación de certificado.</span><span class="sxs-lookup"><span data-stu-id="63ecf-120">Certificate authentication is used.</span></span>

</dd> <dt>

<span data-ttu-id="63ecf-121">2</span><span class="sxs-lookup"><span data-stu-id="63ecf-121">2</span></span>
</dt> <dd>

<span data-ttu-id="63ecf-122">Se usa la autenticación Kerberos.</span><span class="sxs-lookup"><span data-stu-id="63ecf-122">Kerberos authentication is used.</span></span>

</dd> <dt>

<span data-ttu-id="63ecf-123">3</span><span class="sxs-lookup"><span data-stu-id="63ecf-123">3</span></span>
</dt> <dd>

<span data-ttu-id="63ecf-124">Se usan la autenticación de certificados y Kerberos.</span><span class="sxs-lookup"><span data-stu-id="63ecf-124">Both certificate and Kerberos authentication are used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="63ecf-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="63ecf-125">Requirements</span></span>



| <span data-ttu-id="63ecf-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="63ecf-126">Requirement</span></span> | <span data-ttu-id="63ecf-127">Value</span><span class="sxs-lookup"><span data-stu-id="63ecf-127">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="63ecf-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="63ecf-128">Minimum supported client</span></span><br/> | <span data-ttu-id="63ecf-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="63ecf-129">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="63ecf-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="63ecf-130">Minimum supported server</span></span><br/> | <span data-ttu-id="63ecf-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="63ecf-131">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="63ecf-132">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="63ecf-132">Type library</span></span><br/>             | <dl> <span data-ttu-id="63ecf-133"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="63ecf-133"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="63ecf-134">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="63ecf-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="63ecf-135"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="63ecf-135"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="63ecf-136">IID</span><span class="sxs-lookup"><span data-stu-id="63ecf-136">IID</span></span><br/>                      | <span data-ttu-id="63ecf-137">IID \_ IMsRdpClientAdvancedSettings6 se define como 222c4b5d-45d9-4df0-a7c6-60cf9089d285</span><span class="sxs-lookup"><span data-stu-id="63ecf-137">IID\_IMsRdpClientAdvancedSettings6 is defined as 222c4b5d-45d9-4df0-a7c6-60cf9089d285</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="63ecf-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="63ecf-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63ecf-139">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="63ecf-139">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="63ecf-140">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="63ecf-140">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="63ecf-141">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="63ecf-141">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> </dl>

 

 





