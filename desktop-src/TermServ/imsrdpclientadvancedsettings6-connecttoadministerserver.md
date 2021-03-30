---
title: Propiedad ConnectToAdministerServer de IMsRdpClientAdvancedSettings6
description: Recupera o especifica si el control ActiveX debe intentar conectarse al servidor con fines administrativos.
ms.assetid: b98f9b9b-a3e7-4a3c-a7e3-e388ce53c5c9
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad ConnectToAdministerServer
- Propiedad ConnectToAdministerServer Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings6
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings6, propiedad ConnectToAdministerServer
- Propiedad ConnectToAdministerServer Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings7
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings7, propiedad ConnectToAdministerServer
- Propiedad ConnectToAdministerServer Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings8
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings8, propiedad ConnectToAdministerServer
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings6.ConnectToAdministerServer
- IMsRdpClientAdvancedSettings6.get_ConnectToAdministerServer
- IMsRdpClientAdvancedSettings6.put_ConnectToAdministerServer
- IMsRdpClientAdvancedSettings7.ConnectToAdministerServer
- IMsRdpClientAdvancedSettings7.get_ConnectToAdministerServer
- IMsRdpClientAdvancedSettings7.put_ConnectToAdministerServer
- IMsRdpClientAdvancedSettings8.ConnectToAdministerServer
- IMsRdpClientAdvancedSettings8.get_ConnectToAdministerServer
- IMsRdpClientAdvancedSettings8.put_ConnectToAdministerServer
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d9cad8d50e2e0a4c1ec18fbd33733dc394101a8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079378"
---
# <a name="imsrdpclientadvancedsettings6connecttoadministerserver-property"></a><span data-ttu-id="87844-110">IMsRdpClientAdvancedSettings6:: ConnectToAdministerServer (propiedad)</span><span class="sxs-lookup"><span data-stu-id="87844-110">IMsRdpClientAdvancedSettings6::ConnectToAdministerServer property</span></span>

<span data-ttu-id="87844-111">Recupera o especifica si el control ActiveX debe intentar conectarse al servidor con fines administrativos.</span><span class="sxs-lookup"><span data-stu-id="87844-111">Retrieves or specifies whether the ActiveX control should attempt to connect to the server for administrative purposes.</span></span>

<span data-ttu-id="87844-112">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="87844-112">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="87844-113">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="87844-113">Syntax</span></span>


```C++
HRESULT put_ConnectToAdministerServer(
  [in]  VARIANT_BOOL connectToAdministerServer
);

HRESULT get_ConnectToAdministerServer(
  [out] VARIANT_BOOL *pConnectToAdministerServer
);
```



## <a name="property-value"></a><span data-ttu-id="87844-114">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="87844-114">Property value</span></span>

<span data-ttu-id="87844-115">**Variante \_ TRUE** para hacer que el control ActiveX intente conectarse al servidor con fines administrativos; de lo contrario, **Variant \_ false**.</span><span class="sxs-lookup"><span data-stu-id="87844-115">**VARIANT\_TRUE** to cause the ActiveX control to attempt to connect to the server for administrative purposes; otherwise **VARIANT\_FALSE**.</span></span> <span data-ttu-id="87844-116">El valor predeterminado es **Variant \_ false**.</span><span class="sxs-lookup"><span data-stu-id="87844-116">The default value is **VARIANT\_FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="87844-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="87844-117">Remarks</span></span>

<span data-ttu-id="87844-118">Para usar **ConnectToAdministerServer**, debe ejecutar el cliente conexión A escritorio remoto (RDC) versión 6,1 o posterior.</span><span class="sxs-lookup"><span data-stu-id="87844-118">To use **ConnectToAdministerServer**, you must be running Remote Desktop Connection (RDC) client version 6.1 or later.</span></span>

> [!Note]  
> <span data-ttu-id="87844-119">La versión de RDC 6,1 (6.0.6001) admite Protocolo de escritorio remoto 6,1.</span><span class="sxs-lookup"><span data-stu-id="87844-119">RDC version 6.1 (6.0.6001) supports Remote Desktop Protocol 6.1.</span></span> <span data-ttu-id="87844-120">RDC 6,1 se incluye con Windows Server 2008 y Windows Vista con Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="87844-120">RDC 6.1 is included with Windows Server 2008 and Windows Vista with Service Pack 1 (SP1).</span></span>

 

<span data-ttu-id="87844-121">**ConnectToAdministerServer** se conecta a una sesión que se usa con fines administrativos en el servidor remoto.</span><span class="sxs-lookup"><span data-stu-id="87844-121">**ConnectToAdministerServer** connects you to a session that is used for administrative purposes on the remote server.</span></span> <span data-ttu-id="87844-122">Si el servicio de rol host de sesión de Escritorio remoto (host de sesión de escritorio remoto) está instalado en el servidor remoto, **ConnectToAdministerServer** hace lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="87844-122">If the Remote Desktop Session Host (RD Session Host) role service is installed on the remote server, **ConnectToAdministerServer** does the following:</span></span>

-   <span data-ttu-id="87844-123">Deshabilita la concesión de licencias de acceso de cliente de Servicios de Escritorio remoto para la sesión.</span><span class="sxs-lookup"><span data-stu-id="87844-123">Disables Remote Desktop Services client access licensing for the session.</span></span>
-   <span data-ttu-id="87844-124">Deshabilita el redireccionamiento de zona horaria para la sesión.</span><span class="sxs-lookup"><span data-stu-id="87844-124">Disables time zone redirection for the session.</span></span>
-   <span data-ttu-id="87844-125">Deshabilita el redireccionamiento de Conexión a Escritorio remoto Broker (agente de conexión a escritorio remoto) de la sesión.</span><span class="sxs-lookup"><span data-stu-id="87844-125">Disables Remote Desktop Connection Broker (RD Connection Broker) redirection for the session.</span></span>
-   <span data-ttu-id="87844-126">Deshabilita la redirección de dispositivos Plug and Play para la sesión.</span><span class="sxs-lookup"><span data-stu-id="87844-126">Disables Plug and Play device redirection for the session.</span></span>
-   <span data-ttu-id="87844-127">Cambia el tema de la sesión remota a Windows clásico para la sesión.</span><span class="sxs-lookup"><span data-stu-id="87844-127">Changes the remote session theme to Windows Classic for the session.</span></span>

## <a name="requirements"></a><span data-ttu-id="87844-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="87844-128">Requirements</span></span>



| <span data-ttu-id="87844-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="87844-129">Requirement</span></span> | <span data-ttu-id="87844-130">Value</span><span class="sxs-lookup"><span data-stu-id="87844-130">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="87844-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="87844-131">Minimum supported client</span></span><br/> | <span data-ttu-id="87844-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="87844-132">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="87844-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="87844-133">Minimum supported server</span></span><br/> | <span data-ttu-id="87844-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="87844-134">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="87844-135">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="87844-135">Type library</span></span><br/>             | <dl> <span data-ttu-id="87844-136"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="87844-136"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="87844-137">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="87844-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="87844-138"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="87844-138"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="87844-139">IID</span><span class="sxs-lookup"><span data-stu-id="87844-139">IID</span></span><br/>                      | <span data-ttu-id="87844-140">IID \_ IMsRdpClientAdvancedSettings6 se define como 222c4b5d-45d9-4df0-a7c6-60cf9089d285</span><span class="sxs-lookup"><span data-stu-id="87844-140">IID\_IMsRdpClientAdvancedSettings6 is defined as 222c4b5d-45d9-4df0-a7c6-60cf9089d285</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="87844-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="87844-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87844-142">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="87844-142">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="87844-143">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="87844-143">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="87844-144">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="87844-144">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> </dl>

 

 





