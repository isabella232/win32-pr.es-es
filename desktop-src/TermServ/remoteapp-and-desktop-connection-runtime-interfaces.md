---
title: Interfaces en tiempo de ejecución Conexión de RemoteApp y Escritorio
description: Admite interfaces que permiten el desarrollo de clientes personalizados en Conexión de RemoteApp y Escritorio.
ms.assetid: 4580df05-5e44-40d0-8765-5d9b4e1d339e
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto Servicios de Escritorio remoto, Conexión de RemoteApp y Escritorio referencia de la API en tiempo de ejecución
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6b7c3c2fd3841cfe797fc559ba1aa30d3479436
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104148923"
---
# <a name="remoteapp-and-desktop-connection-runtime-interfaces"></a><span data-ttu-id="2f649-104">Interfaces en tiempo de ejecución Conexión de RemoteApp y Escritorio</span><span class="sxs-lookup"><span data-stu-id="2f649-104">RemoteApp and Desktop Connection Runtime interfaces</span></span>

<span data-ttu-id="2f649-105">La API de tiempo de ejecución de Conexión de RemoteApp y Escritorio admite interfaces que permiten el desarrollo de clientes personalizados en Conexión de RemoteApp y Escritorio.</span><span class="sxs-lookup"><span data-stu-id="2f649-105">The RemoteApp and Desktop Connection Runtime API supports interfaces that allow the development of custom clients in RemoteApp and Desktop Connection.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="2f649-106">En esta sección</span><span class="sxs-lookup"><span data-stu-id="2f649-106">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="2f649-107">**IWorkspace**</span><span class="sxs-lookup"><span data-stu-id="2f649-107">**IWorkspace**</span></span>](/windows/desktop/api/workspaceruntime/nn-workspaceruntime-iworkspace)
</dt> <dd>

<span data-ttu-id="2f649-108">Expone métodos que proporcionan información sobre una conexión en Conexión de RemoteApp y Escritorio.</span><span class="sxs-lookup"><span data-stu-id="2f649-108">Exposes methods that provide information about a connection in RemoteApp and Desktop Connection.</span></span>

</dd> <dt>

[<span data-ttu-id="2f649-109">**IWorkspace2**</span><span class="sxs-lookup"><span data-stu-id="2f649-109">**IWorkspace2**</span></span>](/windows/desktop/api/workspaceruntime/nn-workspaceruntime-iworkspace2)
</dt> <dd>

<span data-ttu-id="2f649-110">Expone métodos adicionales que proporcionan información sobre una conexión en Conexión de RemoteApp y Escritorio.</span><span class="sxs-lookup"><span data-stu-id="2f649-110">Exposes additional methods that provide information about a connection in RemoteApp and Desktop Connection.</span></span>

</dd> <dt>

[<span data-ttu-id="2f649-111">**IWorkspace3**</span><span class="sxs-lookup"><span data-stu-id="2f649-111">**IWorkspace3**</span></span>](/windows/desktop/api/workspaceruntime/nn-workspaceruntime-iworkspace3)
</dt> <dd>

<span data-ttu-id="2f649-112">Expone métodos que proporcionan información sobre una conexión en Conexión de RemoteApp y Escritorio y agregan la capacidad de recuperar o establecer un token de notificaciones.</span><span class="sxs-lookup"><span data-stu-id="2f649-112">Exposes methods that provide information about a connection in RemoteApp and Desktop Connection, and adds the ability to retrieve or set a claims token.</span></span>

</dd> <dt>

[<span data-ttu-id="2f649-113">**IWorkspaceClientExt**</span><span class="sxs-lookup"><span data-stu-id="2f649-113">**IWorkspaceClientExt**</span></span>](/windows/desktop/api/Workspaceruntimeclientext/nn-workspaceruntimeclientext-iworkspaceclientext)
</dt> <dd>

<span data-ttu-id="2f649-114">Expone métodos que permiten al tiempo de ejecución desconectar un cliente personalizado en Conexión de RemoteApp y Escritorio.</span><span class="sxs-lookup"><span data-stu-id="2f649-114">Exposes methods that allow the runtime to disconnect a custom client in RemoteApp and Desktop Connection.</span></span>

</dd> <dt>

[<span data-ttu-id="2f649-115">**IWorkspaceRegistration**</span><span class="sxs-lookup"><span data-stu-id="2f649-115">**IWorkspaceRegistration**</span></span>](/windows/desktop/api/workspaceruntime/nn-workspaceruntime-iworkspaceregistration)
</dt> <dd>

<span data-ttu-id="2f649-116">Expone métodos que agregan y quitan referencias a clientes personalizados en Conexión de RemoteApp y Escritorio.</span><span class="sxs-lookup"><span data-stu-id="2f649-116">Exposes methods that add and remove references to custom clients in RemoteApp and Desktop Connection.</span></span>

</dd> <dt>

[<span data-ttu-id="2f649-117">**IWorkspaceRegistration2**</span><span class="sxs-lookup"><span data-stu-id="2f649-117">**IWorkspaceRegistration2**</span></span>](/windows/desktop/api/workspaceruntime/nn-workspaceruntime-iworkspaceregistration2)
</dt> <dd>

<span data-ttu-id="2f649-118">Expone métodos que agregan y quitan referencias a clientes personalizados en Conexión de RemoteApp y Escritorio.</span><span class="sxs-lookup"><span data-stu-id="2f649-118">Exposes methods that add and remove references to custom clients in RemoteApp and Desktop Connection.</span></span>

</dd> <dt>

[<span data-ttu-id="2f649-119">**IWorkspaceReportMessage**</span><span class="sxs-lookup"><span data-stu-id="2f649-119">**IWorkspaceReportMessage**</span></span>](/windows/desktop/api/workspaceruntime/nn-workspaceruntime-iworkspacereportmessage)
</dt> <dd>

<span data-ttu-id="2f649-120">Expone métodos que admiten el control de mensajes de error para áreas de trabajo remotas.</span><span class="sxs-lookup"><span data-stu-id="2f649-120">Exposes methods that support error message handling for remote workspaces.</span></span>

</dd> <dt>

[<span data-ttu-id="2f649-121">**IWorkspaceResTypeRegistry**</span><span class="sxs-lookup"><span data-stu-id="2f649-121">**IWorkspaceResTypeRegistry**</span></span>](/windows/desktop/api/Workspaceax/nn-workspaceax-iworkspacerestyperegistry)
</dt> <dd>

<span data-ttu-id="2f649-122">Expone métodos que permiten a un complemento administrar extensiones de nombre de archivo de terceros en Conexión de RemoteApp y Escritorio en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="2f649-122">Exposes methods that allow a plug-in to manage third-party file name extensions in RemoteApp and Desktop Connection runtime.</span></span>

</dd> <dt>

[<span data-ttu-id="2f649-123">**IWorkspaceScriptable**</span><span class="sxs-lookup"><span data-stu-id="2f649-123">**IWorkspaceScriptable**</span></span>](/windows/desktop/api/workspaceruntime/nn-workspaceruntime-iworkspacescriptable)
</dt> <dd>

<span data-ttu-id="2f649-124">Expone métodos que administran Conexión de RemoteApp y Escritorio las credenciales y las conexiones.</span><span class="sxs-lookup"><span data-stu-id="2f649-124">Exposes methods that manage RemoteApp and Desktop Connection credentials and connections.</span></span>

</dd> <dt>

[<span data-ttu-id="2f649-125">**IWorkspaceScriptable2**</span><span class="sxs-lookup"><span data-stu-id="2f649-125">**IWorkspaceScriptable2**</span></span>](/windows/desktop/api/workspaceruntime/nn-workspaceruntime-iworkspacescriptable2)
</dt> <dd>

<span data-ttu-id="2f649-126">Expone métodos que administran Conexión de RemoteApp y Escritorio las credenciales y las conexiones.</span><span class="sxs-lookup"><span data-stu-id="2f649-126">Exposes methods that manage RemoteApp and Desktop Connection credentials and connections.</span></span>

</dd> <dt>

[<span data-ttu-id="2f649-127">**IWorkspaceScriptable3**</span><span class="sxs-lookup"><span data-stu-id="2f649-127">**IWorkspaceScriptable3**</span></span>](/windows/desktop/api/workspaceruntime/nn-workspaceruntime-iworkspacescriptable3)
</dt> <dd>

<span data-ttu-id="2f649-128">Expone métodos que administran Conexión de RemoteApp y Escritorio las credenciales y las conexiones.</span><span class="sxs-lookup"><span data-stu-id="2f649-128">Exposes methods that manage RemoteApp and Desktop Connection credentials and connections.</span></span>

</dd> </dl>

 

 




