---
title: Método StartScavenging de la clase MicrosoftDNS_Server
description: El método StartScavenging inicia la eliminación de registros obsoletos en las zonas sometidas a limpieza.
ms.assetid: ee1bc0e0-9334-4971-a524-4bb8a9015b5b
keywords:
- StartScavenging el método DNS
- Método StartScavenging DNS, clase MicrosoftDNS_Server
- MicrosoftDNS_Server de clase DNS, método StartScavenging
topic_type:
- apiref
api_name:
- MicrosoftDNS_Server.StartScavenging
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c8e1927ed069d3e3e3cf27fd94b1ffd54e6bb2d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996542"
---
# <a name="startscavenging-method-of-the-microsoftdns_server-class"></a><span data-ttu-id="9252c-106">Método StartScavenging de la \_ clase de servidor MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="9252c-106">StartScavenging method of the MicrosoftDNS\_Server class</span></span>

<span data-ttu-id="9252c-107">El método **StartScavenging** inicia la eliminación de registros obsoletos en las zonas sometidas a limpieza.</span><span class="sxs-lookup"><span data-stu-id="9252c-107">The **StartScavenging** method starts scavenging stale records in the zones subjected to scavenging.</span></span>

## <a name="syntax"></a><span data-ttu-id="9252c-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9252c-108">Syntax</span></span>


```mof
uint32 StartScavenging();
```



## <a name="parameters"></a><span data-ttu-id="9252c-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9252c-109">Parameters</span></span>

<span data-ttu-id="9252c-110">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="9252c-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="9252c-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9252c-111">Return value</span></span>

<span data-ttu-id="9252c-112">ERROR \_ correcto indica que la eliminación de registros obsoletos se ha iniciado correctamente.</span><span class="sxs-lookup"><span data-stu-id="9252c-112">ERROR\_SUCCESS indicates the scavenging was successfully started.</span></span> <span data-ttu-id="9252c-113">Cualquier otro valor es un código de error.</span><span class="sxs-lookup"><span data-stu-id="9252c-113">Any other value is an error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="9252c-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9252c-114">Requirements</span></span>



| <span data-ttu-id="9252c-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="9252c-115">Requirement</span></span> | <span data-ttu-id="9252c-116">Value</span><span class="sxs-lookup"><span data-stu-id="9252c-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9252c-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9252c-117">Minimum supported client</span></span><br/> | <span data-ttu-id="9252c-118">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="9252c-118">None supported</span></span><br/>                                                              |
| <span data-ttu-id="9252c-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9252c-119">Minimum supported server</span></span><br/> | <span data-ttu-id="9252c-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="9252c-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="9252c-121">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="9252c-121">Namespace</span></span><br/>                | <span data-ttu-id="9252c-122">\\MicrosoftDNS raíz</span><span class="sxs-lookup"><span data-stu-id="9252c-122">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="9252c-123">MOF</span><span class="sxs-lookup"><span data-stu-id="9252c-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9252c-124"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9252c-124"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9252c-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="9252c-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9252c-126">**\_Servidor MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="9252c-126">**MicrosoftDNS\_Server**</span></span>](microsoftdns-server.md)
</dt> <dt>

[<span data-ttu-id="9252c-127">**Método StartService de la \_ clase de servidor MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="9252c-127">**StartService Method of the MicrosoftDNS\_Server Class**</span></span>](microsoftdns-server-startservice.md)
</dt> <dt>

[<span data-ttu-id="9252c-128">**Método StopService de la \_ clase de servidor MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="9252c-128">**StopService Method of the MicrosoftDNS\_Server Class**</span></span>](microsoftdns-server-stopservice.md)
</dt> <dt>

[<span data-ttu-id="9252c-129">**Método GetDistinguishedName de la \_ clase de servidor MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="9252c-129">**GetDistinguishedName Method of the MicrosoftDNS\_Server Class**</span></span>](microsoftdns-server-getdistinguishedname.md)
</dt> </dl>

 

 





