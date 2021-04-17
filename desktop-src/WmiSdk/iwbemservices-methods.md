---
description: La interfaz IWbemServices expone los métodos siguientes.
ms.assetid: B4A2048E-6C2F-43E0-97BD-E6D37D8E4657
ms.tgt_platform: multiple
title: Métodos IWbemServices
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a960ec223d16bd9258ba2d9d56518d88beab50c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706459"
---
# <a name="iwbemservices-methods"></a><span data-ttu-id="212de-103">Métodos IWbemServices</span><span class="sxs-lookup"><span data-stu-id="212de-103">IWbemServices Methods</span></span>

<span data-ttu-id="212de-104">La interfaz [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) expone los métodos siguientes.</span><span class="sxs-lookup"><span data-stu-id="212de-104">The [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) interface exposes the following methods.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="212de-105">En esta sección</span><span class="sxs-lookup"><span data-stu-id="212de-105">In this section</span></span>

-   [<span data-ttu-id="212de-106">**Método CancelAsyncCall**</span><span class="sxs-lookup"><span data-stu-id="212de-106">**CancelAsyncCall method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-cancelasynccall)
-   [<span data-ttu-id="212de-107">**Método CreateClassEnum**</span><span class="sxs-lookup"><span data-stu-id="212de-107">**CreateClassEnum method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenum)
-   [<span data-ttu-id="212de-108">**Método CreateClassEnumAsync**</span><span class="sxs-lookup"><span data-stu-id="212de-108">**CreateClassEnumAsync method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync)
-   [<span data-ttu-id="212de-109">**CreateInstanceEnum (método)**</span><span class="sxs-lookup"><span data-stu-id="212de-109">**CreateInstanceEnum method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenum)
-   [<span data-ttu-id="212de-110">**Método CreateInstanceEnumAsync**</span><span class="sxs-lookup"><span data-stu-id="212de-110">**CreateInstanceEnumAsync method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync)
-   [<span data-ttu-id="212de-111">**Método DeleteClass**</span><span class="sxs-lookup"><span data-stu-id="212de-111">**DeleteClass method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclass)
-   [<span data-ttu-id="212de-112">**Método DeleteClassAsync**</span><span class="sxs-lookup"><span data-stu-id="212de-112">**DeleteClassAsync method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync)
-   [<span data-ttu-id="212de-113">**Método DeleteInstance**</span><span class="sxs-lookup"><span data-stu-id="212de-113">**DeleteInstance method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstance)
-   [<span data-ttu-id="212de-114">**Método DeleteInstanceAsync**</span><span class="sxs-lookup"><span data-stu-id="212de-114">**DeleteInstanceAsync method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync)
-   [<span data-ttu-id="212de-115">**ExecMethod (método)**</span><span class="sxs-lookup"><span data-stu-id="212de-115">**ExecMethod method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod)
-   [<span data-ttu-id="212de-116">**Método ExecMethodAsync**</span><span class="sxs-lookup"><span data-stu-id="212de-116">**ExecMethodAsync method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync)
-   [<span data-ttu-id="212de-117">**Método ExecNotificationQuery**</span><span class="sxs-lookup"><span data-stu-id="212de-117">**ExecNotificationQuery method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery)
-   [<span data-ttu-id="212de-118">**Método ExecNotificationQueryAsync**</span><span class="sxs-lookup"><span data-stu-id="212de-118">**ExecNotificationQueryAsync method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationqueryasync)
-   [<span data-ttu-id="212de-119">**ExecQuery (método)**</span><span class="sxs-lookup"><span data-stu-id="212de-119">**ExecQuery method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery)
-   [<span data-ttu-id="212de-120">**ExecQueryAsync (método)**</span><span class="sxs-lookup"><span data-stu-id="212de-120">**ExecQueryAsync method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync)
-   [<span data-ttu-id="212de-121">**GetObject (método)**</span><span class="sxs-lookup"><span data-stu-id="212de-121">**GetObject method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject)
-   [<span data-ttu-id="212de-122">**Método GetObjectAsync**</span><span class="sxs-lookup"><span data-stu-id="212de-122">**GetObjectAsync method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync)
-   [<span data-ttu-id="212de-123">**Método Opennamespace (**</span><span class="sxs-lookup"><span data-stu-id="212de-123">**OpenNamespace method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-opennamespace)
-   [<span data-ttu-id="212de-124">**Método PutClass**</span><span class="sxs-lookup"><span data-stu-id="212de-124">**PutClass method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclass)
-   [<span data-ttu-id="212de-125">**Método PutClassAsync**</span><span class="sxs-lookup"><span data-stu-id="212de-125">**PutClassAsync method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclassasync)
-   [<span data-ttu-id="212de-126">**PutInstance (método)**</span><span class="sxs-lookup"><span data-stu-id="212de-126">**PutInstance method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance)
-   [<span data-ttu-id="212de-127">**Método PutInstanceAsync**</span><span class="sxs-lookup"><span data-stu-id="212de-127">**PutInstanceAsync method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync)
-   [<span data-ttu-id="212de-128">**Método QueryObjectSink**</span><span class="sxs-lookup"><span data-stu-id="212de-128">**QueryObjectSink method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-queryobjectsink)

 

 



