---
title: Interfaz IMsRdpClientShell2
description: Expone propiedades que inician el cliente de Conexión a Escritorio remoto desde Escritorio remoto Web Access (acceso web de escritorio remoto) o desde otros portales web.
ms.assetid: cc8ef78f-b7d6-42cd-bb67-8a8e1f33be08
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la interfaz IMsRdpClientShell2
- Servicios de Escritorio remoto de la interfaz IMsRdpClientShell2, descrito
topic_type:
- apiref
api_name:
- IMsRdpClientShell2
api_location:
- MsRdpWebAccess.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb93fd938602b195f60877be884dbe0bd458a598
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801562"
---
# <a name="imsrdpclientshell2-interface"></a><span data-ttu-id="1fcab-105">Interfaz IMsRdpClientShell2</span><span class="sxs-lookup"><span data-stu-id="1fcab-105">IMsRdpClientShell2 interface</span></span>

<span data-ttu-id="1fcab-106">Expone propiedades que inician el cliente de Conexión a Escritorio remoto desde Escritorio remoto Web Access (acceso web de escritorio remoto) o desde otros portales web.</span><span class="sxs-lookup"><span data-stu-id="1fcab-106">Exposes properties that launch the Remote Desktop Connection client from Remote Desktop Web Access (RD Web Access) or from other web portals.</span></span>

<span data-ttu-id="1fcab-107">Esta interfaz la implementa Servicios de Escritorio remoto Web Access Control, que es un contenedor alrededor del cliente de Conexión a Escritorio remoto (MsTscAx.dll) y el proxy en tiempo de ejecución de conexiones de RemoteApp y escritorio (Tswbprxy.exe).</span><span class="sxs-lookup"><span data-stu-id="1fcab-107">This interface is implemented by the Remote Desktop Services Web Access Control, which is a wrapper around the Remote Desktop Connection client (MsTscAx.dll) and the RemoteApp and Desktop Connections runtime proxy (Tswbprxy.exe).</span></span>

## <a name="members"></a><span data-ttu-id="1fcab-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="1fcab-108">Members</span></span>

<span data-ttu-id="1fcab-109">La interfaz **IMsRdpClientShell2** hereda de **IMsRdpClientShell**.</span><span class="sxs-lookup"><span data-stu-id="1fcab-109">The **IMsRdpClientShell2** interface inherits from **IMsRdpClientShell**.</span></span> <span data-ttu-id="1fcab-110">**IMsRdpClientShell2** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="1fcab-110">**IMsRdpClientShell2** also has these types of members:</span></span>

-   [<span data-ttu-id="1fcab-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="1fcab-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1fcab-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="1fcab-112">Properties</span></span>

<span data-ttu-id="1fcab-113">La interfaz **IMsRdpClientShell2** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="1fcab-113">The **IMsRdpClientShell2** interface has these properties.</span></span>



| <span data-ttu-id="1fcab-114">Propiedad</span><span class="sxs-lookup"><span data-stu-id="1fcab-114">Property</span></span>                                                                               | <span data-ttu-id="1fcab-115">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="1fcab-115">Access type</span></span>          | <span data-ttu-id="1fcab-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="1fcab-116">Description</span></span>                                                                                                                                                                       |
|:---------------------------------------------------------------------------------------|:---------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1fcab-117">**MsRdpWorkspace**</span><span class="sxs-lookup"><span data-stu-id="1fcab-117">**MsRdpWorkspace**</span></span>](imsrdpclientshell2-msrdpworkspace.md)<br/>                 | <span data-ttu-id="1fcab-118">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="1fcab-118">Read-only</span></span><br/> | <span data-ttu-id="1fcab-119">Recupera un puntero a la interfaz [**IMsRdpWorkspace**](imsrdpworkspace.md) , que se usa para administrar conexión de RemoteApp y escritorio credenciales y conexiones.</span><span class="sxs-lookup"><span data-stu-id="1fcab-119">Retrieves a pointer to the [**IMsRdpWorkspace**](imsrdpworkspace.md) interface, which is used to manage RemoteApp and Desktop Connection credentials and connections.</span></span><br/> |
| [<span data-ttu-id="1fcab-120">**SecuredSettingsEnabled**</span><span class="sxs-lookup"><span data-stu-id="1fcab-120">**SecuredSettingsEnabled**</span></span>](imsrdpclientshell2-securedsettingsenabled.md)<br/> | <span data-ttu-id="1fcab-121">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="1fcab-121">Read-only</span></span><br/> | <span data-ttu-id="1fcab-122">Recupera un valor que indica si la página web actual está en una zona de seguridad de direcciones URL de Internet Explorer de confianza.</span><span class="sxs-lookup"><span data-stu-id="1fcab-122">Retrieves a value that indicates whether the current webpage is in a trusted Internet Explorer URL security zone.</span></span><br/>                                                      |



 

## <a name="requirements"></a><span data-ttu-id="1fcab-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1fcab-123">Requirements</span></span>



| <span data-ttu-id="1fcab-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="1fcab-124">Requirement</span></span> | <span data-ttu-id="1fcab-125">Value</span><span class="sxs-lookup"><span data-stu-id="1fcab-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="1fcab-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1fcab-126">Minimum supported client</span></span><br/> | <span data-ttu-id="1fcab-127">Windows 7</span><span class="sxs-lookup"><span data-stu-id="1fcab-127">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="1fcab-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1fcab-128">Minimum supported server</span></span><br/> | <span data-ttu-id="1fcab-129">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="1fcab-129">Windows Server 2008 R2</span></span><br/>                                                             |
| <span data-ttu-id="1fcab-130">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="1fcab-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1fcab-131"><dt>MsRdpWebAccess.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1fcab-131"><dt>MsRdpWebAccess.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1fcab-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="1fcab-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1fcab-133">**IMsRdpWorkspace**</span><span class="sxs-lookup"><span data-stu-id="1fcab-133">**IMsRdpWorkspace**</span></span>](imsrdpworkspace.md)
</dt> </dl>

 

 





