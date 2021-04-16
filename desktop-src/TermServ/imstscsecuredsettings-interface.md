---
title: Interfaz IMsTscSecuredSettings
description: Incluye métodos para recuperar y establecer las propiedades del control ActiveX Escritorio remoto que están restringidas a zonas de seguridad de direcciones URL específicas de Internet Explorer. | Interfaz IMsTscSecuredSettings
ms.assetid: 1136dbc5-abe6-40e0-b44f-700a1460fbd2
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la interfaz IMsTscSecuredSettings
- Servicios de Escritorio remoto de la interfaz IMsTscSecuredSettings, descrito
topic_type:
- apiref
api_name:
- IMsTscSecuredSettings
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2037393147bd5a2e35d6eb803951890c9b5e7de5
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105689760"
---
# <a name="imstscsecuredsettings-interface"></a><span data-ttu-id="8eae8-106">Interfaz IMsTscSecuredSettings</span><span class="sxs-lookup"><span data-stu-id="8eae8-106">IMsTscSecuredSettings interface</span></span>

<span data-ttu-id="8eae8-107">Incluye métodos para recuperar y establecer las propiedades del control ActiveX Escritorio remoto que están restringidas a zonas de seguridad de direcciones URL específicas de Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="8eae8-107">Includes methods to retrieve and set properties of the Remote Desktop ActiveX control that are restricted to specific Internet Explorer URL security zones.</span></span> <span data-ttu-id="8eae8-108">Las propiedades incluyen las que especifican el modo del control de cliente (modo de pantalla completa o modo de ventana) y el programa que se va a iniciar tras la conexión al servidor de host de sesión de Escritorio remoto (host de sesión de escritorio remoto).</span><span class="sxs-lookup"><span data-stu-id="8eae8-108">Properties include those that specify the mode of the client control (full-screen mode or window mode) and the program to start upon connection to the Remote Desktop Session Host (RD Session Host) server.</span></span> <span data-ttu-id="8eae8-109">Estos métodos también están disponibles a través de la interfaz [**IMsRdpClientSecuredSettings**](imsrdpclientsecuredsettings-interface.md) .</span><span class="sxs-lookup"><span data-stu-id="8eae8-109">These methods are also available through the [**IMsRdpClientSecuredSettings**](imsrdpclientsecuredsettings-interface.md) interface.</span></span>

## <a name="members"></a><span data-ttu-id="8eae8-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="8eae8-110">Members</span></span>

<span data-ttu-id="8eae8-111">La interfaz **IMsTscSecuredSettings** hereda de la interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="8eae8-111">The **IMsTscSecuredSettings** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="8eae8-112">**IMsTscSecuredSettings** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="8eae8-112">**IMsTscSecuredSettings** also has these types of members:</span></span>

-   [<span data-ttu-id="8eae8-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="8eae8-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8eae8-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="8eae8-114">Properties</span></span>

<span data-ttu-id="8eae8-115">La interfaz **IMsTscSecuredSettings** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="8eae8-115">The **IMsTscSecuredSettings** interface has these properties.</span></span>



| <span data-ttu-id="8eae8-116">Propiedad</span><span class="sxs-lookup"><span data-stu-id="8eae8-116">Property</span></span>                                                              | <span data-ttu-id="8eae8-117">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="8eae8-117">Access type</span></span>           | <span data-ttu-id="8eae8-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="8eae8-118">Description</span></span>                                                                |
|:----------------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------|
| [<span data-ttu-id="8eae8-119">**FullScreen**</span><span class="sxs-lookup"><span data-stu-id="8eae8-119">**FullScreen**</span></span>](imstscsecuredsettings-fullscreen.md)<br/>     | <span data-ttu-id="8eae8-120">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="8eae8-120">Read/write</span></span><br/> | <span data-ttu-id="8eae8-121">El estado de pantalla completa del control de cliente.</span><span class="sxs-lookup"><span data-stu-id="8eae8-121">The full-screen state of the client control.</span></span><br/>                    |
| [<span data-ttu-id="8eae8-122">**StartProgram**</span><span class="sxs-lookup"><span data-stu-id="8eae8-122">**StartProgram**</span></span>](imstscsecuredsettings-startprogram.md)<br/> | <span data-ttu-id="8eae8-123">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="8eae8-123">Read/write</span></span><br/> | <span data-ttu-id="8eae8-124">Programa que se va a iniciar en el servidor remoto después de la conexión.</span><span class="sxs-lookup"><span data-stu-id="8eae8-124">The program to be started on the remote server upon connection.</span></span><br/> |
| [<span data-ttu-id="8eae8-125">**WorkDir**</span><span class="sxs-lookup"><span data-stu-id="8eae8-125">**WorkDir**</span></span>](imstscsecuredsettings-workdir.md)<br/>           | <span data-ttu-id="8eae8-126">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="8eae8-126">Read/write</span></span><br/> | <span data-ttu-id="8eae8-127">Directorio de trabajo del programa de inicio.</span><span class="sxs-lookup"><span data-stu-id="8eae8-127">The working directory of the start program.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="8eae8-128">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8eae8-128">Remarks</span></span>

<span data-ttu-id="8eae8-129">Consulte [proporcionar seguridad de cliente RDP](providing-for-rdp-client-security.md) para obtener más información sobre los métodos de esta interfaz.</span><span class="sxs-lookup"><span data-stu-id="8eae8-129">Refer to [Providing for RDP Client Security](providing-for-rdp-client-security.md) for more information about the methods of this interface.</span></span>

<span data-ttu-id="8eae8-130">Para obtener más información acerca de Conexión web a Escritorio remoto, consulte [Requirements for conexión web a escritorio remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="8eae8-130">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8eae8-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8eae8-131">Requirements</span></span>



| <span data-ttu-id="8eae8-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="8eae8-132">Requirement</span></span> | <span data-ttu-id="8eae8-133">Value</span><span class="sxs-lookup"><span data-stu-id="8eae8-133">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8eae8-134">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8eae8-134">Minimum supported client</span></span><br/> | <span data-ttu-id="8eae8-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8eae8-135">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="8eae8-136">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8eae8-136">Minimum supported server</span></span><br/> | <span data-ttu-id="8eae8-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8eae8-137">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="8eae8-138">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="8eae8-138">Type library</span></span><br/>             | <dl> <span data-ttu-id="8eae8-139"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8eae8-139"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="8eae8-140">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="8eae8-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8eae8-141"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8eae8-141"><dt>MsTscAx.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8eae8-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="8eae8-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8eae8-143">**IDispatch**</span><span class="sxs-lookup"><span data-stu-id="8eae8-143">**IDispatch**</span></span>](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[<span data-ttu-id="8eae8-144">Referencia de Conexión web a Escritorio remoto</span><span class="sxs-lookup"><span data-stu-id="8eae8-144">Remote Desktop Web Connection Reference</span></span>](remote-desktop-web-connection-reference.md)
</dt> </dl>

 

