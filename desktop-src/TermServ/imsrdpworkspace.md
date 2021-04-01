---
title: Interfaz IMsRdpWorkspace
description: Expone métodos que administran Conexión de RemoteApp y Escritorio las credenciales y las conexiones.
ms.assetid: cddcdfc2-b30a-4d00-84c2-ad036ab6288f
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
ms.openlocfilehash: 0ba55a02c5d984bc87aa05caffd42b3a3b965c43
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996014"
---
# <a name="imsrdpworkspace-interface"></a><span data-ttu-id="a83e0-105">Interfaz IMsRdpWorkspace</span><span class="sxs-lookup"><span data-stu-id="a83e0-105">IMsRdpWorkspace interface</span></span>

<span data-ttu-id="a83e0-106">Expone métodos que administran Conexión de RemoteApp y Escritorio las credenciales y las conexiones.</span><span class="sxs-lookup"><span data-stu-id="a83e0-106">Exposes methods that manage RemoteApp and Desktop Connection credentials and connections.</span></span> <span data-ttu-id="a83e0-107">La Access Control Web Servicios de Escritorio remoto implementa esta interfaz.</span><span class="sxs-lookup"><span data-stu-id="a83e0-107">This interface is implemented by the Remote Desktop Services Web Access Control.</span></span> <span data-ttu-id="a83e0-108">Este control es un contenedor alrededor del cliente de Conexión a Escritorio remoto (MsTscAx.dll) y el proxy en tiempo de ejecución de conexiones de RemoteApp y escritorio (Tswbprxy.exe).</span><span class="sxs-lookup"><span data-stu-id="a83e0-108">This control is a wrapper around the Remote Desktop Connection client (MsTscAx.dll) and the RemoteApp and Desktop Connections runtime proxy (Tswbprxy.exe).</span></span>

## <a name="members"></a><span data-ttu-id="a83e0-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="a83e0-109">Members</span></span>

<span data-ttu-id="a83e0-110">La interfaz **IMsRdpWorkspace** hereda de la interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="a83e0-110">The **IMsRdpWorkspace** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="a83e0-111">**IMsRdpWorkspace** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="a83e0-111">**IMsRdpWorkspace** also has these types of members:</span></span>

-   [<span data-ttu-id="a83e0-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="a83e0-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="a83e0-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="a83e0-113">Methods</span></span>

<span data-ttu-id="a83e0-114">La interfaz **IMsRdpWorkspace** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="a83e0-114">The **IMsRdpWorkspace** interface has these methods.</span></span>



| <span data-ttu-id="a83e0-115">Método</span><span class="sxs-lookup"><span data-stu-id="a83e0-115">Method</span></span>                                                                                   | <span data-ttu-id="a83e0-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="a83e0-116">Description</span></span>                                                                                                                                                           |
|:-----------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a83e0-117">[**ClearWorkspaceCredential**](/previous-versions/windows/desktop/legacy/ee351596(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a83e0-117">[**ClearWorkspaceCredential**](/previous-versions/windows/desktop/legacy/ee351596(v=vs.85))</span></span>             | <span data-ttu-id="a83e0-118">Elimina las credenciales de usuario asociadas con el identificador de conexión especificado.</span><span class="sxs-lookup"><span data-stu-id="a83e0-118">Deletes the user credentials associated with the specified connection ID.</span></span><br/>                                                                                  |
| <span data-ttu-id="a83e0-119">[**DisconnectWorkspace**](/previous-versions/windows/desktop/legacy/ee351597(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a83e0-119">[**DisconnectWorkspace**](/previous-versions/windows/desktop/legacy/ee351597(v=vs.85))</span></span>                       | <span data-ttu-id="a83e0-120">Desconecta todas las conexiones existentes asociadas con el identificador de conexión especificado y elimina las credenciales de usuario correspondientes del almacén de credenciales.</span><span class="sxs-lookup"><span data-stu-id="a83e0-120">Disconnects all existing connections associated with the specified connection ID and deletes the corresponding user credentials from the credential store.</span></span><br/> |
| <span data-ttu-id="a83e0-121">[**IsWorkspaceCredentialSpecified**](/previous-versions/windows/desktop/legacy/ee351598(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a83e0-121">[**IsWorkspaceCredentialSpecified**](/previous-versions/windows/desktop/legacy/ee351598(v=vs.85))</span></span> | <span data-ttu-id="a83e0-122">Determina si existen credenciales de usuario para el identificador de conexión especificado.</span><span class="sxs-lookup"><span data-stu-id="a83e0-122">Determines whether user credentials exist for the specified connection ID.</span></span><br/>                                                                                 |
| <span data-ttu-id="a83e0-123">[**IsWorkspaceSSOEnabled**](/previous-versions/windows/desktop/legacy/ee351599(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a83e0-123">[**IsWorkspaceSSOEnabled**](/previous-versions/windows/desktop/legacy/ee351599(v=vs.85))</span></span>                   | <span data-ttu-id="a83e0-124">Determina si el inicio de sesión único (SSO) está habilitado para Conexión de RemoteApp y Escritorio.</span><span class="sxs-lookup"><span data-stu-id="a83e0-124">Determines whether single sign on (SSO) is enabled for RemoteApp and Desktop Connection.</span></span><br/>                                                                   |
| <span data-ttu-id="a83e0-125">[**Autenticado**](/previous-versions/windows/desktop/legacy/ee351600(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a83e0-125">[**OnAuthenticated**](/previous-versions/windows/desktop/legacy/ee351600(v=vs.85))</span></span>                               | <span data-ttu-id="a83e0-126">Marca la autenticación de las credenciales de usuario para el identificador de conexión y, posteriormente, muestra la notificación de conexión en el área de notificación de la barra de tareas.</span><span class="sxs-lookup"><span data-stu-id="a83e0-126">Marks the authentication of user credentials for the connection ID, and subsequently shows the connect notification in the taskbar notification area.</span></span> <br/>     |
| <span data-ttu-id="a83e0-127">[**StartWorkspace**](/previous-versions/windows/desktop/legacy/ee351601(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a83e0-127">[**StartWorkspace**](/previous-versions/windows/desktop/legacy/ee351601(v=vs.85))</span></span>                                 | <span data-ttu-id="a83e0-128">Asocia las credenciales de usuario y los certificados con un identificador de conexión.</span><span class="sxs-lookup"><span data-stu-id="a83e0-128">Associates user credentials and certificates with a connection ID.</span></span><br/>                                                                                         |



 

## <a name="requirements"></a><span data-ttu-id="a83e0-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a83e0-129">Requirements</span></span>



| <span data-ttu-id="a83e0-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="a83e0-130">Requirement</span></span> | <span data-ttu-id="a83e0-131">Value</span><span class="sxs-lookup"><span data-stu-id="a83e0-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="a83e0-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a83e0-132">Minimum supported client</span></span><br/> | <span data-ttu-id="a83e0-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="a83e0-133">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="a83e0-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a83e0-134">Minimum supported server</span></span><br/> | <span data-ttu-id="a83e0-135">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a83e0-135">Windows Server 2008 R2</span></span><br/>                                                             |
| <span data-ttu-id="a83e0-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a83e0-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a83e0-137"><dt>MsRdpWebAccess.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a83e0-137"><dt>MsRdpWebAccess.dll</dt></span></span> </dl> |
| <span data-ttu-id="a83e0-138">IID</span><span class="sxs-lookup"><span data-stu-id="a83e0-138">IID</span></span><br/>                      | <span data-ttu-id="a83e0-139">IID \_ IMsRdpWorkspace se define como 145D0621-04CF-4FC2-A766-A81A9069CDF8</span><span class="sxs-lookup"><span data-stu-id="a83e0-139">IID\_IMsRdpWorkspace is defined as 145D0621-04CF-4FC2-A766-A81A9069CDF8</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="a83e0-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="a83e0-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a83e0-141">**IMsRdpClientShell2**</span><span class="sxs-lookup"><span data-stu-id="a83e0-141">**IMsRdpClientShell2**</span></span>](imsrdpclientshell2.md)
</dt> </dl>

 

