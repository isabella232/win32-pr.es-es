---
title: Propiedad AuthenticationServiceClass de IMsRdpClientAdvancedSettings6
description: Especifica el nombre de entidad de seguridad de servicio (SPN) que se va a usar para la autenticación en el servidor.
ms.assetid: 65d10b1f-295a-44b8-a790-306ae4e3e5e2
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad AuthenticationServiceClass
- Propiedad AuthenticationServiceClass Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings6
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings6, propiedad AuthenticationServiceClass
- Propiedad AuthenticationServiceClass Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings7
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings7, propiedad AuthenticationServiceClass
- Propiedad AuthenticationServiceClass Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings8
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings8, propiedad AuthenticationServiceClass
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings6.AuthenticationServiceClass
- IMsRdpClientAdvancedSettings6.get_AuthenticationServiceClass
- IMsRdpClientAdvancedSettings6.put_AuthenticationServiceClass
- IMsRdpClientAdvancedSettings7.AuthenticationServiceClass
- IMsRdpClientAdvancedSettings7.get_AuthenticationServiceClass
- IMsRdpClientAdvancedSettings7.put_AuthenticationServiceClass
- IMsRdpClientAdvancedSettings8.AuthenticationServiceClass
- IMsRdpClientAdvancedSettings8.get_AuthenticationServiceClass
- IMsRdpClientAdvancedSettings8.put_AuthenticationServiceClass
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 618b55d1489f46e0e1119186bd5003fb68dbfebb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802288"
---
# <a name="imsrdpclientadvancedsettings6authenticationserviceclass-property"></a><span data-ttu-id="8975b-110">IMsRdpClientAdvancedSettings6:: AuthenticationServiceClass (propiedad)</span><span class="sxs-lookup"><span data-stu-id="8975b-110">IMsRdpClientAdvancedSettings6::AuthenticationServiceClass property</span></span>

<span data-ttu-id="8975b-111">Especifica el nombre de entidad de seguridad de servicio (SPN) que se va a usar para la autenticación en el servidor.</span><span class="sxs-lookup"><span data-stu-id="8975b-111">Specifies the service principal name (SPN) to use for authentication to the server.</span></span>

<span data-ttu-id="8975b-112">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="8975b-112">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="8975b-113">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8975b-113">Syntax</span></span>


```C++
HRESULT put_AuthenticationServiceClass(
  [in]          BSTR bstrAuthServiceClass
);

HRESULT get_AuthenticationServiceClass(
  [out, retval] BSTR *pbstrAuthServiceClass
);
```



## <a name="property-value"></a><span data-ttu-id="8975b-114">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="8975b-114">Property value</span></span>

<span data-ttu-id="8975b-115">Especifica el nombre de la entidad de seguridad de servicio que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="8975b-115">Specifies the service principal name to use.</span></span>

## <a name="remarks"></a><span data-ttu-id="8975b-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8975b-116">Remarks</span></span>

<span data-ttu-id="8975b-117">Esta propiedad solo es compatible con clientes Conexión a Escritorio remoto 6,1 y 7,0.</span><span class="sxs-lookup"><span data-stu-id="8975b-117">This property is only supported by Remote Desktop Connection 6.1 and 7.0 clients.</span></span>

<span data-ttu-id="8975b-118">Los nombres principales de servicio (SPN) están asociados a la entidad de seguridad (usuarios o grupos) en cuyo contexto de seguridad se ejecuta el servicio.</span><span class="sxs-lookup"><span data-stu-id="8975b-118">Service principal names (SPNs) are associated with the security principal (user or groups) in whose security context the service executes.</span></span> <span data-ttu-id="8975b-119">Los SPN se usan para admitir la autenticación mutua entre una aplicación cliente y un servicio.</span><span class="sxs-lookup"><span data-stu-id="8975b-119">SPNs are used to support mutual authentication between a client application and a service.</span></span>

## <a name="requirements"></a><span data-ttu-id="8975b-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8975b-120">Requirements</span></span>



| <span data-ttu-id="8975b-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="8975b-121">Requirement</span></span> | <span data-ttu-id="8975b-122">Value</span><span class="sxs-lookup"><span data-stu-id="8975b-122">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8975b-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8975b-123">Minimum supported client</span></span><br/> | <span data-ttu-id="8975b-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8975b-124">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="8975b-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8975b-125">Minimum supported server</span></span><br/> | <span data-ttu-id="8975b-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8975b-126">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="8975b-127">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="8975b-127">Type library</span></span><br/>             | <dl> <span data-ttu-id="8975b-128"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8975b-128"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="8975b-129">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="8975b-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8975b-130"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8975b-130"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="8975b-131">IID</span><span class="sxs-lookup"><span data-stu-id="8975b-131">IID</span></span><br/>                      | <span data-ttu-id="8975b-132">IID \_ IMsRdpClientAdvancedSettings6 se define como 222c4b5d-45d9-4df0-a7c6-60cf9089d285</span><span class="sxs-lookup"><span data-stu-id="8975b-132">IID\_IMsRdpClientAdvancedSettings6 is defined as 222c4b5d-45d9-4df0-a7c6-60cf9089d285</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8975b-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="8975b-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8975b-134">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="8975b-134">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="8975b-135">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="8975b-135">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="8975b-136">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="8975b-136">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> </dl>

 

 





