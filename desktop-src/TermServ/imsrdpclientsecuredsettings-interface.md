---
title: Interfaz IMsRdpClientSecuredSettings
description: Incluye métodos para recuperar y establecer las propiedades del control ActiveX Escritorio remoto que están restringidas a zonas de seguridad de direcciones URL específicas de Internet Explorer. | Interfaz IMsRdpClientSecuredSettings
ms.assetid: 56d3193d-a0fb-468a-9fb3-c080db5500b7
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la interfaz IMsRdpClientSecuredSettings
- Servicios de Escritorio remoto de la interfaz IMsRdpClientSecuredSettings, descrito
topic_type:
- apiref
api_name:
- IMsRdpClientSecuredSettings
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 396e6b58b2be0122076b5529b910423377417fa6
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105678711"
---
# <a name="imsrdpclientsecuredsettings-interface"></a><span data-ttu-id="a04dc-106">Interfaz IMsRdpClientSecuredSettings</span><span class="sxs-lookup"><span data-stu-id="a04dc-106">IMsRdpClientSecuredSettings interface</span></span>

<span data-ttu-id="a04dc-107">Incluye métodos para recuperar y establecer las propiedades del control ActiveX Escritorio remoto que están restringidas a zonas de seguridad de direcciones URL específicas de Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="a04dc-107">Includes methods to retrieve and set properties of the Remote Desktop ActiveX control that are restricted to specific Internet Explorer URL security zones.</span></span>

## <a name="members"></a><span data-ttu-id="a04dc-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="a04dc-108">Members</span></span>

<span data-ttu-id="a04dc-109">La interfaz **IMsRdpClientSecuredSettings** hereda de [**IMsTscSecuredSettings**](imstscsecuredsettings-interface.md).</span><span class="sxs-lookup"><span data-stu-id="a04dc-109">The **IMsRdpClientSecuredSettings** interface inherits from [**IMsTscSecuredSettings**](imstscsecuredsettings-interface.md).</span></span> <span data-ttu-id="a04dc-110">**IMsRdpClientSecuredSettings** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="a04dc-110">**IMsRdpClientSecuredSettings** also has these types of members:</span></span>

-   [<span data-ttu-id="a04dc-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a04dc-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a04dc-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a04dc-112">Properties</span></span>

<span data-ttu-id="a04dc-113">La interfaz **IMsRdpClientSecuredSettings** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="a04dc-113">The **IMsRdpClientSecuredSettings** interface has these properties.</span></span>



| <span data-ttu-id="a04dc-114">Propiedad</span><span class="sxs-lookup"><span data-stu-id="a04dc-114">Property</span></span>                                                                                   | <span data-ttu-id="a04dc-115">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="a04dc-115">Access type</span></span>           | <span data-ttu-id="a04dc-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="a04dc-116">Description</span></span>                                   |
|:-------------------------------------------------------------------------------------------|:----------------------|:----------------------------------------------|
| [<span data-ttu-id="a04dc-117">**AudioRedirectionMode**</span><span class="sxs-lookup"><span data-stu-id="a04dc-117">**AudioRedirectionMode**</span></span>](imsrdpclientsecuredsettings-autoredirectionmode.md)<br/> | <span data-ttu-id="a04dc-118">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="a04dc-118">Read/write</span></span><br/> | <span data-ttu-id="a04dc-119">La configuración de redirección de audio.</span><span class="sxs-lookup"><span data-stu-id="a04dc-119">The audio redirection settings.</span></span><br/>    |
| [<span data-ttu-id="a04dc-120">**KeyboardHookMode**</span><span class="sxs-lookup"><span data-stu-id="a04dc-120">**KeyboardHookMode**</span></span>](imsrdpclientsecuredsettings-keyboardhookmode.md)<br/>        | <span data-ttu-id="a04dc-121">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="a04dc-121">Read/write</span></span><br/> | <span data-ttu-id="a04dc-122">La configuración de redirección del teclado.</span><span class="sxs-lookup"><span data-stu-id="a04dc-122">The keyboard redirection settings.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="a04dc-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a04dc-123">Remarks</span></span>

<span data-ttu-id="a04dc-124">Estas propiedades no se pueden establecer cuando el control está conectado.</span><span class="sxs-lookup"><span data-stu-id="a04dc-124">These properties cannot be set when the control is connected.</span></span>

<span data-ttu-id="a04dc-125">Consulte [proporcionar seguridad de cliente RDP](providing-for-rdp-client-security.md) para obtener más información sobre los métodos de esta interfaz.</span><span class="sxs-lookup"><span data-stu-id="a04dc-125">Refer to [Providing for RDP Client Security](providing-for-rdp-client-security.md) for more information about the methods of this interface.</span></span>

<span data-ttu-id="a04dc-126">Para obtener más información acerca de Conexión web a Escritorio remoto, consulte [Requirements for conexión web a escritorio remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="a04dc-126">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a04dc-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a04dc-127">Requirements</span></span>



| <span data-ttu-id="a04dc-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="a04dc-128">Requirement</span></span> | <span data-ttu-id="a04dc-129">Value</span><span class="sxs-lookup"><span data-stu-id="a04dc-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a04dc-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a04dc-130">Minimum supported client</span></span><br/> | <span data-ttu-id="a04dc-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a04dc-131">Windows Vista</span></span><br/>                                                                       |
| <span data-ttu-id="a04dc-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a04dc-132">Minimum supported server</span></span><br/> | <span data-ttu-id="a04dc-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a04dc-133">Windows Server 2008</span></span><br/>                                                                 |
| <span data-ttu-id="a04dc-134">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="a04dc-134">Type library</span></span><br/>             | <dl> <span data-ttu-id="a04dc-135"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a04dc-135"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="a04dc-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a04dc-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a04dc-137"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a04dc-137"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="a04dc-138">IID</span><span class="sxs-lookup"><span data-stu-id="a04dc-138">IID</span></span><br/>                      | <span data-ttu-id="a04dc-139">IID \_ IMsRdpClientSecuredSettings se define como 605befcf-39c1-45cc-A811-068fb7be346d</span><span class="sxs-lookup"><span data-stu-id="a04dc-139">IID\_IMsRdpClientSecuredSettings is defined as 605befcf-39c1-45cc-a811-068fb7be346d</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a04dc-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="a04dc-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a04dc-141">**IMsTscSecuredSettings**</span><span class="sxs-lookup"><span data-stu-id="a04dc-141">**IMsTscSecuredSettings**</span></span>](imstscsecuredsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="a04dc-142">Referencia de Conexión web a Escritorio remoto</span><span class="sxs-lookup"><span data-stu-id="a04dc-142">Remote Desktop Web Connection Reference</span></span>](remote-desktop-web-connection-reference.md)
</dt> </dl>

 

 





