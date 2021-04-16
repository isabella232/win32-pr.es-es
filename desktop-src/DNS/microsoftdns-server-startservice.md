---
title: Método StartService de la clase MicrosoftDNS_Server
description: El método StartService inicia el servidor DNS.
ms.assetid: f6343a34-9d1b-4f82-897e-289650af6be9
keywords:
- DNS del método StartService
- Método StartService DNS, clase MicrosoftDNS_Server
- MicrosoftDNS_Server de clase DNS, StartService
topic_type:
- apiref
api_name:
- MicrosoftDNS_Server.StartService
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2e103b3d2648bf2c061eb047090cfdfeb907518
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105658223"
---
# <a name="startservice-method-of-the-microsoftdns_server-class"></a><span data-ttu-id="25df6-106">Método StartService de la \_ clase de servidor MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="25df6-106">StartService method of the MicrosoftDNS\_Server class</span></span>

<span data-ttu-id="25df6-107">El método **StartService** inicia el servidor DNS.</span><span class="sxs-lookup"><span data-stu-id="25df6-107">The **StartService** method starts the DNS Server.</span></span>

## <a name="syntax"></a><span data-ttu-id="25df6-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="25df6-108">Syntax</span></span>


```mof
uint32 StartService();
```



## <a name="parameters"></a><span data-ttu-id="25df6-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="25df6-109">Parameters</span></span>

<span data-ttu-id="25df6-110">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="25df6-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="25df6-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="25df6-111">Return value</span></span>

<span data-ttu-id="25df6-112">ERROR \_ correcto indica que el servicio se ha iniciado correctamente.</span><span class="sxs-lookup"><span data-stu-id="25df6-112">ERROR\_SUCCESS indicates the service was successfully started.</span></span> <span data-ttu-id="25df6-113">Cualquier otro valor es un código de error.</span><span class="sxs-lookup"><span data-stu-id="25df6-113">Any other value is an error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="25df6-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="25df6-114">Requirements</span></span>



| <span data-ttu-id="25df6-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="25df6-115">Requirement</span></span> | <span data-ttu-id="25df6-116">Value</span><span class="sxs-lookup"><span data-stu-id="25df6-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="25df6-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="25df6-117">Minimum supported client</span></span><br/> | <span data-ttu-id="25df6-118">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="25df6-118">None supported</span></span><br/>                                                              |
| <span data-ttu-id="25df6-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="25df6-119">Minimum supported server</span></span><br/> | <span data-ttu-id="25df6-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="25df6-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="25df6-121">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="25df6-121">Namespace</span></span><br/>                | <span data-ttu-id="25df6-122">\\MicrosoftDNS raíz</span><span class="sxs-lookup"><span data-stu-id="25df6-122">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="25df6-123">MOF</span><span class="sxs-lookup"><span data-stu-id="25df6-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="25df6-124"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="25df6-124"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="25df6-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="25df6-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25df6-126">**\_Servidor MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="25df6-126">**MicrosoftDNS\_Server**</span></span>](microsoftdns-server.md)
</dt> <dt>

[<span data-ttu-id="25df6-127">**Método StopService de la \_ clase de servidor MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="25df6-127">**StopService Method of the MicrosoftDNS\_Server Class**</span></span>](microsoftdns-server-stopservice.md)
</dt> <dt>

[<span data-ttu-id="25df6-128">**Método StartScavenging de la \_ clase de servidor MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="25df6-128">**StartScavenging Method of the MicrosoftDNS\_Server Class**</span></span>](microsoftdns-server-startscavenging.md)
</dt> <dt>

[<span data-ttu-id="25df6-129">**Método GetDistinguishedName de la \_ clase de servidor MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="25df6-129">**GetDistinguishedName Method of the MicrosoftDNS\_Server Class**</span></span>](microsoftdns-server-getdistinguishedname.md)
</dt> </dl>

 

 





