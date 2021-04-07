---
description: Constantes predefinidas para los protocolos de criptografía. Estos valores se definen en Wincrypt. h.
ms.assetid: 61dc0eff-2033-464a-a558-1798a92d48a2
title: Marcas de protocolo (Wincrypt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c25804763e407ff2a12e5657878e343f483d353e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002587"
---
# <a name="protocol-flags"></a><span data-ttu-id="e8aba-104">Marcas de protocolo</span><span class="sxs-lookup"><span data-stu-id="e8aba-104">Protocol Flags</span></span>

<span data-ttu-id="e8aba-105">A continuación se enumeran las constantes predefinidas para los protocolos de criptografía.</span><span class="sxs-lookup"><span data-stu-id="e8aba-105">The following are predefined constants for cryptography protocols.</span></span> <span data-ttu-id="e8aba-106">Estos valores se definen en Wincrypt. h.</span><span class="sxs-lookup"><span data-stu-id="e8aba-106">These values are defined in Wincrypt.h.</span></span>



| <span data-ttu-id="e8aba-107">Constante o valor</span><span class="sxs-lookup"><span data-stu-id="e8aba-107">Constant/value</span></span>                                                                                                                                                                                                                            | <span data-ttu-id="e8aba-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="e8aba-108">Description</span></span>                                                           |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------|
| <span id="CRYPT_FLAG_IPSEC"></span><span id="crypt_flag_ipsec"></span><dl> <span data-ttu-id="e8aba-109"><dt>**Cifrado \_ MARCAR \_ IPSec**</dt> <dt>0x0010</dt></span><span class="sxs-lookup"><span data-stu-id="e8aba-109"><dt>**CRYPT\_FLAG\_IPSEC**</dt> <dt>0x0010</dt></span></span> </dl>       | <span data-ttu-id="e8aba-110">Protocolo de seguridad de Internet (IPsec).</span><span class="sxs-lookup"><span data-stu-id="e8aba-110">Internet protocol security (IPsec) protocol.</span></span><br/>               |
| <span id="CRYPT_FLAG_PCT1"></span><span id="crypt_flag_pct1"></span><dl> <span data-ttu-id="e8aba-111"><dt>**Cifrado \_ MARCA \_ PCT1**</dt> <dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="e8aba-111"><dt>**CRYPT\_FLAG\_PCT1**</dt> <dt>0x0001</dt></span></span> </dl>          | <span data-ttu-id="e8aba-112">Protocolo de transporte de comunicaciones privadas (PCT) versión 1.</span><span class="sxs-lookup"><span data-stu-id="e8aba-112">Private communications transport (PCT) version 1 protocol.</span></span><br/> |
| <span id="CRYPT_FLAG_SIGNING"></span><span id="crypt_flag_signing"></span><dl> <span data-ttu-id="e8aba-113"><dt>**Cifrado \_ 0x0020 de \_ firma de marca**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="e8aba-113"><dt>**CRYPT\_FLAG\_SIGNING**</dt> <dt>0x0020</dt></span></span> </dl> | <span data-ttu-id="e8aba-114">Protocolo de firma.</span><span class="sxs-lookup"><span data-stu-id="e8aba-114">Signing protocol.</span></span><br/>                                          |
| <span id="CRYPT_FLAG_SSL2"></span><span id="crypt_flag_ssl2"></span><dl> <span data-ttu-id="e8aba-115"><dt>**Cifrado \_ MARCA \_ SSL2**</dt> <dt>0x0002</dt></span><span class="sxs-lookup"><span data-stu-id="e8aba-115"><dt>**CRYPT\_FLAG\_SSL2**</dt> <dt>0x0002</dt></span></span> </dl>          | <span data-ttu-id="e8aba-116">Protocolo de capa de sockets seguros (SSL) versión 2.</span><span class="sxs-lookup"><span data-stu-id="e8aba-116">Secure sockets layer (SSL) version 2 protocol.</span></span><br/>             |
| <span id="CRYPT_FLAG_SSL3"></span><span id="crypt_flag_ssl3"></span><dl> <span data-ttu-id="e8aba-117"><dt>**Cifrado \_ MARCA \_ SSL3**</dt> <dt>0x0004</dt></span><span class="sxs-lookup"><span data-stu-id="e8aba-117"><dt>**CRYPT\_FLAG\_SSL3**</dt> <dt>0x0004</dt></span></span> </dl>          | <span data-ttu-id="e8aba-118">Protocolo SSL versión 3.</span><span class="sxs-lookup"><span data-stu-id="e8aba-118">SSL version 3 protocol.</span></span><br/>                                    |
| <span id="CRYPT_FLAG_TLS1"></span><span id="crypt_flag_tls1"></span><dl> <span data-ttu-id="e8aba-119"><dt>**Cifrado \_ MARCA \_ TLS1**</dt> <dt>0x0008</dt></span><span class="sxs-lookup"><span data-stu-id="e8aba-119"><dt>**CRYPT\_FLAG\_TLS1**</dt> <dt>0x0008</dt></span></span> </dl>          | <span data-ttu-id="e8aba-120">Protocolo de seguridad de la capa de transporte (TLS) versión 1.</span><span class="sxs-lookup"><span data-stu-id="e8aba-120">Transport layer security (TLS) version 1 protocol.</span></span><br/>         |



## <a name="requirements"></a><span data-ttu-id="e8aba-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e8aba-121">Requirements</span></span>



| <span data-ttu-id="e8aba-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="e8aba-122">Requirement</span></span> | <span data-ttu-id="e8aba-123">Value</span><span class="sxs-lookup"><span data-stu-id="e8aba-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e8aba-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e8aba-124">Minimum supported client</span></span><br/> | <span data-ttu-id="e8aba-125">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="e8aba-125">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="e8aba-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e8aba-126">Minimum supported server</span></span><br/> | <span data-ttu-id="e8aba-127">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="e8aba-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e8aba-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e8aba-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="e8aba-129"><dt>Wincrypt. h</dt></span><span class="sxs-lookup"><span data-stu-id="e8aba-129"><dt>Wincrypt.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e8aba-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="e8aba-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8aba-131">**PROV \_ ENUMALGS \_ ex**</span><span class="sxs-lookup"><span data-stu-id="e8aba-131">**PROV\_ENUMALGS\_EX**</span></span>](/windows/desktop/api/Wincrypt/ns-wincrypt-prov_enumalgs_ex)
</dt> </dl>

 

 




