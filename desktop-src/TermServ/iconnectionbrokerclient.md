---
title: Interfaz IConnectionBrokerClient (Cbclient. h)
description: Proporciona los métodos necesarios para utilizar el cliente del agente de Conexión a Escritorio remoto.
ms.assetid: AFFE0157-DEF5-480D-8CE0-D89E9EF70EAF
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la interfaz IConnectionBrokerClient
- Servicios de Escritorio remoto de la interfaz IConnectionBrokerClient, descrito
topic_type:
- apiref
api_name:
- IConnectionBrokerClient
api_location:
- Cbclient.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a062059f7aa1f16e32514b3bacbfb31dc0a350f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492784"
---
# <a name="iconnectionbrokerclient-interface"></a><span data-ttu-id="8b451-105">Interfaz IConnectionBrokerClient</span><span class="sxs-lookup"><span data-stu-id="8b451-105">IConnectionBrokerClient interface</span></span>

<span data-ttu-id="8b451-106">Proporciona los métodos necesarios para utilizar el cliente del agente de Conexión a Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="8b451-106">Provides the methods needed to use the Remote Desktop Connection Broker client.</span></span>

<span data-ttu-id="8b451-107">El sistema implementa esta interfaz.</span><span class="sxs-lookup"><span data-stu-id="8b451-107">This interface is implemented by the system.</span></span> <span data-ttu-id="8b451-108">Para obtener una instancia de esta interfaz, utilice la función [**CBCreateClientInstance**](cbcreateclientinstance.md) .</span><span class="sxs-lookup"><span data-stu-id="8b451-108">To obtain an instance of this interface, use the [**CBCreateClientInstance**](cbcreateclientinstance.md) function.</span></span>

## <a name="members"></a><span data-ttu-id="8b451-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="8b451-109">Members</span></span>

<span data-ttu-id="8b451-110">La interfaz **IConnectionBrokerClient** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="8b451-110">The **IConnectionBrokerClient** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="8b451-111">**IConnectionBrokerClient** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="8b451-111">**IConnectionBrokerClient** also has these types of members:</span></span>

-   [<span data-ttu-id="8b451-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="8b451-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="8b451-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="8b451-113">Methods</span></span>

<span data-ttu-id="8b451-114">La interfaz **IConnectionBrokerClient** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="8b451-114">The **IConnectionBrokerClient** interface has these methods.</span></span>



| <span data-ttu-id="8b451-115">Método</span><span class="sxs-lookup"><span data-stu-id="8b451-115">Method</span></span>                                                         | <span data-ttu-id="8b451-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="8b451-116">Description</span></span>                                                                                          |
|:---------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8b451-117">**GetTargetInfo**</span><span class="sxs-lookup"><span data-stu-id="8b451-117">**GetTargetInfo**</span></span>](iconnectionbrokerclient-gettargetinfo.md) | <span data-ttu-id="8b451-118">Solicita información sobre el equipo de destino al que se debe redirigir la conexión.</span><span class="sxs-lookup"><span data-stu-id="8b451-118">Requests information about the target computer where the connection should be redirected.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="8b451-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8b451-119">Requirements</span></span>



| <span data-ttu-id="8b451-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="8b451-120">Requirement</span></span> | <span data-ttu-id="8b451-121">Value</span><span class="sxs-lookup"><span data-stu-id="8b451-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="8b451-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8b451-122">Minimum supported client</span></span><br/> | <span data-ttu-id="8b451-123">Windows 8</span><span class="sxs-lookup"><span data-stu-id="8b451-123">Windows 8</span></span><br/>                                                                       |
| <span data-ttu-id="8b451-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8b451-124">Minimum supported server</span></span><br/> | <span data-ttu-id="8b451-125">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="8b451-125">Windows Server 2012</span></span><br/>                                                             |
| <span data-ttu-id="8b451-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8b451-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="8b451-127"><dt>Cbclient. h</dt></span><span class="sxs-lookup"><span data-stu-id="8b451-127"><dt>Cbclient.h</dt></span></span> </dl>      |
| <span data-ttu-id="8b451-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8b451-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="8b451-129"><dt>Cbclient. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8b451-129"><dt>Cbclient.lib</dt></span></span> </dl>    |
| <span data-ttu-id="8b451-130">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="8b451-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8b451-131"><dt>Cbclient.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8b451-131"><dt>Cbclient.dll</dt></span></span> </dl>    |
| <span data-ttu-id="8b451-132">IID</span><span class="sxs-lookup"><span data-stu-id="8b451-132">IID</span></span><br/>                      | <span data-ttu-id="8b451-133">IID \_ IConnectionBrokerClient se define como D6818DF2-8338-4EB7-AD77-DE210817987C</span><span class="sxs-lookup"><span data-stu-id="8b451-133">IID\_IConnectionBrokerClient is defined as D6818DF2-8338-4EB7-AD77-DE210817987C</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8b451-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="8b451-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b451-135">**CBCreateClientInstance**</span><span class="sxs-lookup"><span data-stu-id="8b451-135">**CBCreateClientInstance**</span></span>](cbcreateclientinstance.md)
</dt> </dl>

 

