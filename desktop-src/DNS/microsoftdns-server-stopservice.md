---
title: Método StopService de la clase MicrosoftDNS_Server
description: El método StopService detiene el servidor DNS.
ms.assetid: 80637d5b-e43a-4710-b3ab-eec246587788
keywords:
- StopService (método) DNS
- Método StopService DNS, clase MicrosoftDNS_Server
- MicrosoftDNS_Server de clase DNS, StopService (método)
topic_type:
- apiref
api_name:
- MicrosoftDNS_Server.StopService
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f811533c66185304c5c674fdfff2eda8cf5bef69
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491159"
---
# <a name="stopservice-method-of-the-microsoftdns_server-class"></a><span data-ttu-id="44029-106">Método StopService de la \_ clase de servidor MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="44029-106">StopService method of the MicrosoftDNS\_Server class</span></span>

<span data-ttu-id="44029-107">El método **StopService** detiene el servidor DNS.</span><span class="sxs-lookup"><span data-stu-id="44029-107">The **StopService** method stops the DNS Server.</span></span>

## <a name="syntax"></a><span data-ttu-id="44029-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="44029-108">Syntax</span></span>


```mof
uint32 StopService();
```



## <a name="parameters"></a><span data-ttu-id="44029-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="44029-109">Parameters</span></span>

<span data-ttu-id="44029-110">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="44029-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="44029-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="44029-111">Return value</span></span>

<span data-ttu-id="44029-112">ERROR \_ correcto indica que el servicio se detuvo correctamente.</span><span class="sxs-lookup"><span data-stu-id="44029-112">ERROR\_SUCCESS indicates the service was successfully stopped.</span></span> <span data-ttu-id="44029-113">Cualquier otro valor es un código de error.</span><span class="sxs-lookup"><span data-stu-id="44029-113">Any other value is an error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="44029-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="44029-114">Requirements</span></span>



| <span data-ttu-id="44029-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="44029-115">Requirement</span></span> | <span data-ttu-id="44029-116">Value</span><span class="sxs-lookup"><span data-stu-id="44029-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="44029-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="44029-117">Minimum supported client</span></span><br/> | <span data-ttu-id="44029-118">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="44029-118">None supported</span></span><br/>                                                              |
| <span data-ttu-id="44029-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="44029-119">Minimum supported server</span></span><br/> | <span data-ttu-id="44029-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="44029-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="44029-121">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="44029-121">Namespace</span></span><br/>                | <span data-ttu-id="44029-122">\\MicrosoftDNS raíz</span><span class="sxs-lookup"><span data-stu-id="44029-122">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="44029-123">MOF</span><span class="sxs-lookup"><span data-stu-id="44029-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="44029-124"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="44029-124"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="44029-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="44029-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44029-126">**\_Servidor MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="44029-126">**MicrosoftDNS\_Server**</span></span>](microsoftdns-server.md)
</dt> <dt>

[<span data-ttu-id="44029-127">**Método StartService de la \_ clase de servidor MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="44029-127">**StartService Method of the MicrosoftDNS\_Server Class**</span></span>](microsoftdns-server-startservice.md)
</dt> <dt>

[<span data-ttu-id="44029-128">**Método StartScavenging de la \_ clase de servidor MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="44029-128">**StartScavenging Method of the MicrosoftDNS\_Server Class**</span></span>](microsoftdns-server-startscavenging.md)
</dt> <dt>

[<span data-ttu-id="44029-129">**Método GetDistinguishedName de la \_ clase de servidor MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="44029-129">**GetDistinguishedName Method of the MicrosoftDNS\_Server Class**</span></span>](microsoftdns-server-getdistinguishedname.md)
</dt> </dl>

 

 





