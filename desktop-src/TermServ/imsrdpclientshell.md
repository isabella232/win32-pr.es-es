---
title: Interfaz IMsRdpClientShell
description: La configuración de cliente Conexión a Escritorio remoto (RDC) que se usa para iniciar el cliente desde Escritorio remoto Web Access (acceso web de escritorio remoto) o desde otros portales web.
ms.assetid: 05ca2e90-656a-40a3-a438-29d7985e9feb
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la interfaz IMsRdpClientShell
- Servicios de Escritorio remoto de la interfaz IMsRdpClientShell, descrito
topic_type:
- apiref
api_name:
- IMsRdpClientShell
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b529ed1819864e5fc6106472b33ddd00312560c1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491650"
---
# <a name="imsrdpclientshell-interface"></a><span data-ttu-id="4c533-105">Interfaz IMsRdpClientShell</span><span class="sxs-lookup"><span data-stu-id="4c533-105">IMsRdpClientShell interface</span></span>

<span data-ttu-id="4c533-106">La configuración de cliente Conexión a Escritorio remoto (RDC) que se usa para iniciar el cliente desde Escritorio remoto Web Access (acceso web de escritorio remoto) o desde otros portales web.</span><span class="sxs-lookup"><span data-stu-id="4c533-106">Remote Desktop Connection (RDC) client settings that are used to launch the client from Remote Desktop Web Access (RD Web Access) or from other web portals.</span></span>

## <a name="members"></a><span data-ttu-id="4c533-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="4c533-107">Members</span></span>

<span data-ttu-id="4c533-108">La interfaz **IMsRdpClientShell** hereda de la interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="4c533-108">The **IMsRdpClientShell** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="4c533-109">**IMsRdpClientShell** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="4c533-109">**IMsRdpClientShell** also has these types of members:</span></span>

-   [<span data-ttu-id="4c533-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="4c533-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="4c533-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="4c533-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="4c533-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="4c533-112">Methods</span></span>

<span data-ttu-id="4c533-113">La interfaz **IMsRdpClientShell** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="4c533-113">The **IMsRdpClientShell** interface has these methods.</span></span>



| <span data-ttu-id="4c533-114">Método</span><span class="sxs-lookup"><span data-stu-id="4c533-114">Method</span></span>                                                     | <span data-ttu-id="4c533-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="4c533-115">Description</span></span>                                                  |
|:-----------------------------------------------------------|:-------------------------------------------------------------|
| <span data-ttu-id="4c533-116">[**GetRdpProperty**](/previous-versions/windows/desktop/legacy/aa381303(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="4c533-116">[**GetRdpProperty**](/previous-versions/windows/desktop/legacy/aa381303(v=vs.85))</span></span> | <span data-ttu-id="4c533-117">Recupera una sola propiedad de RDP.</span><span class="sxs-lookup"><span data-stu-id="4c533-117">Retrieves a single RDP property.</span></span><br/>                  |
| [<span data-ttu-id="4c533-118">**Launch**</span><span class="sxs-lookup"><span data-stu-id="4c533-118">**Launch**</span></span>](imsrdpclientshell-launch.md)                 | <span data-ttu-id="4c533-119">Inicia el contenido del archivo remoto desde el portal web.</span><span class="sxs-lookup"><span data-stu-id="4c533-119">Launches remote file content from the web portal.</span></span><br/> |
| <span data-ttu-id="4c533-120">[**SetRdpProperty**](/previous-versions/windows/desktop/legacy/aa381312(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="4c533-120">[**SetRdpProperty**](/previous-versions/windows/desktop/legacy/aa381312(v=vs.85))</span></span> | <span data-ttu-id="4c533-121">Establece una única propiedad de RDP.</span><span class="sxs-lookup"><span data-stu-id="4c533-121">Sets a single RDP property.</span></span><br/>                       |



 

### <a name="properties"></a><span data-ttu-id="4c533-122">Propiedades</span><span class="sxs-lookup"><span data-stu-id="4c533-122">Properties</span></span>

<span data-ttu-id="4c533-123">La interfaz **IMsRdpClientShell** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="4c533-123">The **IMsRdpClientShell** interface has these properties.</span></span>



| <span data-ttu-id="4c533-124">Propiedad</span><span class="sxs-lookup"><span data-stu-id="4c533-124">Property</span></span>                                                                                              | <span data-ttu-id="4c533-125">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="4c533-125">Access type</span></span>           | <span data-ttu-id="4c533-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="4c533-126">Description</span></span>                                                                                               |
|:------------------------------------------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4c533-127">**IsRemoteProgramClientInstalled**</span><span class="sxs-lookup"><span data-stu-id="4c533-127">**IsRemoteProgramClientInstalled**</span></span>](imsrdpclientshell-isremoteprogramclientinstalled.md)<br/> | <span data-ttu-id="4c533-128">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="4c533-128">Read-only</span></span><br/>  | <span data-ttu-id="4c533-129">Recupera si el cliente Conexión a Escritorio remoto (RDC) admite la funcionalidad de RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="4c533-129">Retrieves whether the Remote Desktop Connection (RDC) client supports RemoteApp functionality.</span></span><br/> |
| [<span data-ttu-id="4c533-130">**PublicMode**</span><span class="sxs-lookup"><span data-stu-id="4c533-130">**PublicMode**</span></span>](imsrdpclientshell-publicmode.md)<br/>                                         | <span data-ttu-id="4c533-131">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="4c533-131">Read/write</span></span><br/> | <span data-ttu-id="4c533-132">Recupera si está habilitado el modo público.</span><span class="sxs-lookup"><span data-stu-id="4c533-132">Retrieves whether public mode is enabled.</span></span><br/>                                                      |
| [<span data-ttu-id="4c533-133">**RdpFileContents**</span><span class="sxs-lookup"><span data-stu-id="4c533-133">**RdpFileContents**</span></span>](imsrdpclientshell-rdpfilecontents.md)<br/>                               | <span data-ttu-id="4c533-134">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="4c533-134">Read/write</span></span><br/> | <span data-ttu-id="4c533-135">Versión de Stream del archivo de configuración de RDP.</span><span class="sxs-lookup"><span data-stu-id="4c533-135">Stream version of the RDP configuration file.</span></span><br/>                                                  |



 

## <a name="requirements"></a><span data-ttu-id="4c533-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4c533-136">Requirements</span></span>



| <span data-ttu-id="4c533-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="4c533-137">Requirement</span></span> | <span data-ttu-id="4c533-138">Value</span><span class="sxs-lookup"><span data-stu-id="4c533-138">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4c533-139">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4c533-139">Minimum supported client</span></span><br/> | <span data-ttu-id="4c533-140">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4c533-140">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="4c533-141">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4c533-141">Minimum supported server</span></span><br/> | <span data-ttu-id="4c533-142">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4c533-142">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="4c533-143">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="4c533-143">Type library</span></span><br/>             | <dl> <span data-ttu-id="4c533-144"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4c533-144"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="4c533-145">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="4c533-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4c533-146"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4c533-146"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="4c533-147">IID</span><span class="sxs-lookup"><span data-stu-id="4c533-147">IID</span></span><br/>                      | <span data-ttu-id="4c533-148">IID \_ IMsRdpClientShell se define como d012ae6d-c19a-4bfe-B367-201f8911f134</span><span class="sxs-lookup"><span data-stu-id="4c533-148">IID\_IMsRdpClientShell is defined as d012ae6d-c19a-4bfe-b367-201f8911f134</span></span><br/>   |



## <a name="see-also"></a><span data-ttu-id="4c533-149">Vea también</span><span class="sxs-lookup"><span data-stu-id="4c533-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c533-150">**IDispatch**</span><span class="sxs-lookup"><span data-stu-id="4c533-150">**IDispatch**</span></span>](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[<span data-ttu-id="4c533-151">Referencia de Conexión web a Escritorio remoto</span><span class="sxs-lookup"><span data-stu-id="4c533-151">Remote Desktop Web Connection Reference</span></span>](remote-desktop-web-connection-reference.md)
</dt> </dl>

 

