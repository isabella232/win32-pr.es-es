---
title: Interfaz IConnectionBrokerRequest (Cbclient. h)
description: Proporciona los métodos necesarios para obtener los resultados del método asincrónico IConnectionBrokerClient GetTargetInfo.
ms.assetid: 20F42FDC-7026-468E-9B8D-25DFFBE229C1
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la interfaz IConnectionBrokerRequest
- Servicios de Escritorio remoto de la interfaz IConnectionBrokerRequest, descrito
topic_type:
- apiref
api_name:
- IConnectionBrokerRequest
api_location:
- Cbclient.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb95427aee37053b6979cb1a12ce7b5d1942c2fe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803896"
---
# <a name="iconnectionbrokerrequest-interface"></a><span data-ttu-id="bf77b-105">Interfaz IConnectionBrokerRequest</span><span class="sxs-lookup"><span data-stu-id="bf77b-105">IConnectionBrokerRequest interface</span></span>

<span data-ttu-id="bf77b-106">Proporciona los métodos necesarios para obtener los resultados del método [**IConnectionBrokerClient:: GetTargetInfo**](iconnectionbrokerclient-gettargetinfo.md) asincrónico.</span><span class="sxs-lookup"><span data-stu-id="bf77b-106">Provides the methods needed to obtain the results of the asynchronous [**IConnectionBrokerClient::GetTargetInfo**](iconnectionbrokerclient-gettargetinfo.md) method.</span></span>

<span data-ttu-id="bf77b-107">El sistema implementa esta interfaz.</span><span class="sxs-lookup"><span data-stu-id="bf77b-107">This interface is implemented by the system.</span></span> <span data-ttu-id="bf77b-108">Se proporciona una instancia de esta interfaz al llamador con el método [**IConnectionBrokerClient:: GetTargetInfo**](iconnectionbrokerclient-gettargetinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="bf77b-108">An instance of this interface is provided to the caller with the [**IConnectionBrokerClient::GetTargetInfo**](iconnectionbrokerclient-gettargetinfo.md) method.</span></span>

## <a name="members"></a><span data-ttu-id="bf77b-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="bf77b-109">Members</span></span>

<span data-ttu-id="bf77b-110">La interfaz **IConnectionBrokerRequest** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="bf77b-110">The **IConnectionBrokerRequest** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="bf77b-111">**IConnectionBrokerRequest** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="bf77b-111">**IConnectionBrokerRequest** also has these types of members:</span></span>

-   [<span data-ttu-id="bf77b-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="bf77b-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="bf77b-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="bf77b-113">Methods</span></span>

<span data-ttu-id="bf77b-114">La interfaz **IConnectionBrokerRequest** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="bf77b-114">The **IConnectionBrokerRequest** interface has these methods.</span></span>



| <span data-ttu-id="bf77b-115">Método</span><span class="sxs-lookup"><span data-stu-id="bf77b-115">Method</span></span>                                                      | <span data-ttu-id="bf77b-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="bf77b-116">Description</span></span>                                                           |
|:------------------------------------------------------------|:----------------------------------------------------------------------|
| [<span data-ttu-id="bf77b-117">**CheckStatus**</span><span class="sxs-lookup"><span data-stu-id="bf77b-117">**CheckStatus**</span></span>](iconnectionbrokerrequest-checkstatus.md) | <span data-ttu-id="bf77b-118">Se llama para determinar el estado de una solicitud asincrónica.</span><span class="sxs-lookup"><span data-stu-id="bf77b-118">Called to determine the status of an asynchronous request.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="bf77b-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bf77b-119">Requirements</span></span>



| <span data-ttu-id="bf77b-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="bf77b-120">Requirement</span></span> | <span data-ttu-id="bf77b-121">Value</span><span class="sxs-lookup"><span data-stu-id="bf77b-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="bf77b-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bf77b-122">Minimum supported client</span></span><br/> | <span data-ttu-id="bf77b-123">Windows 8</span><span class="sxs-lookup"><span data-stu-id="bf77b-123">Windows 8</span></span><br/>                                                                        |
| <span data-ttu-id="bf77b-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bf77b-124">Minimum supported server</span></span><br/> | <span data-ttu-id="bf77b-125">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="bf77b-125">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="bf77b-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bf77b-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="bf77b-127"><dt>Cbclient. h</dt></span><span class="sxs-lookup"><span data-stu-id="bf77b-127"><dt>Cbclient.h</dt></span></span> </dl>       |
| <span data-ttu-id="bf77b-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="bf77b-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="bf77b-129"><dt>Cbclient. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bf77b-129"><dt>Cbclient.lib</dt></span></span> </dl>     |
| <span data-ttu-id="bf77b-130">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="bf77b-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bf77b-131"><dt>Cbclient.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bf77b-131"><dt>Cbclient.dll</dt></span></span> </dl>     |
| <span data-ttu-id="bf77b-132">IID</span><span class="sxs-lookup"><span data-stu-id="bf77b-132">IID</span></span><br/>                      | <span data-ttu-id="bf77b-133">IID \_ IConnectionBrokerRequest se define como 25114427-ED5D-46A6-AF53-C62D33A4108E</span><span class="sxs-lookup"><span data-stu-id="bf77b-133">IID\_IConnectionBrokerRequest is defined as 25114427-ED5D-46A6-AF53-C62D33A4108E</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="bf77b-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="bf77b-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf77b-135">**IConnectionBrokerClient::GetTargetInfo**</span><span class="sxs-lookup"><span data-stu-id="bf77b-135">**IConnectionBrokerClient::GetTargetInfo**</span></span>](iconnectionbrokerclient-gettargetinfo.md)
</dt> </dl>

 

