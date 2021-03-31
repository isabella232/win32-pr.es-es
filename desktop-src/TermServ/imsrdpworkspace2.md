---
title: Interfaz IMsRdpWorkspace2
description: Expone un método que asocia Conexión de RemoteApp y Escritorio credenciales a una conexión.
ms.assetid: 7E09AF14-2D6C-4D6E-8033-C691D9DC8057
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la interfaz IMsRdpWorkspace
- Servicios de Escritorio remoto de la interfaz IMsRdpWorkspace, descrito
topic_type:
- apiref
api_name:
- IMsRdpWorkspace
api_location:
- MsRdpWebAccess.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d6b5ff193eec393b67029d355a0f0c1bc67c0ad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079299"
---
# <a name="imsrdpworkspace2-interface"></a><span data-ttu-id="61731-105">Interfaz IMsRdpWorkspace2</span><span class="sxs-lookup"><span data-stu-id="61731-105">IMsRdpWorkspace2 interface</span></span>

<span data-ttu-id="61731-106">Expone un método que asocia Conexión de RemoteApp y Escritorio credenciales a una conexión.</span><span class="sxs-lookup"><span data-stu-id="61731-106">Exposes a method that associates RemoteApp and Desktop Connection credentials with a connection.</span></span> <span data-ttu-id="61731-107">La Access Control Web Servicios de Escritorio remoto implementa esta interfaz.</span><span class="sxs-lookup"><span data-stu-id="61731-107">This interface is implemented by the Remote Desktop Services Web Access Control.</span></span> <span data-ttu-id="61731-108">Este control es un contenedor alrededor del cliente de Conexión a Escritorio remoto (MsTscAx.dll) y el proxy en tiempo de ejecución de conexiones de RemoteApp y escritorio (Tswbprxy.exe).</span><span class="sxs-lookup"><span data-stu-id="61731-108">This control is a wrapper around the Remote Desktop Connection client (MsTscAx.dll) and the RemoteApp and Desktop Connections runtime proxy (Tswbprxy.exe).</span></span>

## <a name="members"></a><span data-ttu-id="61731-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="61731-109">Members</span></span>

<span data-ttu-id="61731-110">La interfaz **IMsRdpWorkspace** hereda de [**IMsRdpWorkspace**](imsrdpworkspace.md).</span><span class="sxs-lookup"><span data-stu-id="61731-110">The **IMsRdpWorkspace** interface inherits from [**IMsRdpWorkspace**](imsrdpworkspace.md).</span></span> <span data-ttu-id="61731-111">**IMsRdpWorkspace2** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="61731-111">**IMsRdpWorkspace2** also has these types of members:</span></span>

-   [<span data-ttu-id="61731-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="61731-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="61731-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="61731-113">Methods</span></span>

<span data-ttu-id="61731-114">La interfaz **IMsRdpWorkspace** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="61731-114">The **IMsRdpWorkspace** interface has these methods.</span></span>



| <span data-ttu-id="61731-115">Método</span><span class="sxs-lookup"><span data-stu-id="61731-115">Method</span></span>                                                        | <span data-ttu-id="61731-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="61731-116">Description</span></span>                                                                    |
|:--------------------------------------------------------------|:-------------------------------------------------------------------------------|
| <span data-ttu-id="61731-117">[**StartWorkspaceEx**](/previous-versions/windows/desktop/legacy/dn123459(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="61731-117">[**StartWorkspaceEx**](/previous-versions/windows/desktop/legacy/dn123459(v=vs.85))</span></span> | <span data-ttu-id="61731-118">Asocia las credenciales de usuario y los certificados con un identificador de conexión.</span><span class="sxs-lookup"><span data-stu-id="61731-118">Associates user credentials and certificates with a connection ID.</span></span> <br/> |



 

## <a name="requirements"></a><span data-ttu-id="61731-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="61731-119">Requirements</span></span>



| <span data-ttu-id="61731-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="61731-120">Requirement</span></span> | <span data-ttu-id="61731-121">Value</span><span class="sxs-lookup"><span data-stu-id="61731-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="61731-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="61731-122">Minimum supported client</span></span><br/> | <span data-ttu-id="61731-123">Windows 8</span><span class="sxs-lookup"><span data-stu-id="61731-123">Windows 8</span></span><br/>                                                                          |
| <span data-ttu-id="61731-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="61731-124">Minimum supported server</span></span><br/> | <span data-ttu-id="61731-125">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="61731-125">Windows Server 2012</span></span><br/>                                                                |
| <span data-ttu-id="61731-126">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="61731-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="61731-127"><dt>MsRdpWebAccess.dll</dt></span><span class="sxs-lookup"><span data-stu-id="61731-127"><dt>MsRdpWebAccess.dll</dt></span></span> </dl> |
| <span data-ttu-id="61731-128">IID</span><span class="sxs-lookup"><span data-stu-id="61731-128">IID</span></span><br/>                      | <span data-ttu-id="61731-129">IID \_ IMsRdpWorkspace2 se define como 145D0622-04CF-4FC3-A776-A82A9169CDF8</span><span class="sxs-lookup"><span data-stu-id="61731-129">IID\_IMsRdpWorkspace2 is defined as 145D0622-04CF-4FC3-A776-A82A9169CDF8</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="61731-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="61731-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61731-131">**IMsRdpClientShell2**</span><span class="sxs-lookup"><span data-stu-id="61731-131">**IMsRdpClientShell2**</span></span>](imsrdpclientshell2.md)
</dt> <dt>

[<span data-ttu-id="61731-132">**IMsRdpWorkspace**</span><span class="sxs-lookup"><span data-stu-id="61731-132">**IMsRdpWorkspace**</span></span>](imsrdpworkspace.md)
</dt> </dl>

 

