---
description: Representa un identificador de una respuesta de OCSP asociada con una cadena de certificados de servidor.
ms.assetid: baf173f1-99dc-49f9-9a17-fee79b393db7
title: HCERT_SERVER_OCSP_RESPONSE (Wincrypt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ceab319b5d8370dd15ef3dcd288124e4f2adf9ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912033"
---
# <a name="hcert_server_ocsp_response"></a><span data-ttu-id="7ada5-103">\_respuesta de \_ OCSP del servidor de HCERT \_</span><span class="sxs-lookup"><span data-stu-id="7ada5-103">HCERT\_SERVER\_OCSP\_RESPONSE</span></span>

<span data-ttu-id="7ada5-104">El tipo de datos de respuesta de OCSP del servidor de HCERT representa un identificador de una respuesta de OCSP asociada con una cadena de certificados de servidor. **\_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="7ada5-104">The **HCERT\_SERVER\_OCSP\_RESPONSE** data type represents a handle to an OCSP response associated with a server certificate chain.</span></span>

<span data-ttu-id="7ada5-105">Este tipo lo usan las siguientes API.</span><span class="sxs-lookup"><span data-stu-id="7ada5-105">This type is used by the following APIs.</span></span>

-   [<span data-ttu-id="7ada5-106">**CertOpenServerOcspResponse**</span><span class="sxs-lookup"><span data-stu-id="7ada5-106">**CertOpenServerOcspResponse**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenserverocspresponse)
-   [<span data-ttu-id="7ada5-107">**CertAddRefServerOcspResponse**</span><span class="sxs-lookup"><span data-stu-id="7ada5-107">**CertAddRefServerOcspResponse**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddrefserverocspresponse)
-   [<span data-ttu-id="7ada5-108">**CertCloseServerOcspResponse**</span><span class="sxs-lookup"><span data-stu-id="7ada5-108">**CertCloseServerOcspResponse**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certcloseserverocspresponse)
-   [<span data-ttu-id="7ada5-109">**CertGetServerOcspResponseContext**</span><span class="sxs-lookup"><span data-stu-id="7ada5-109">**CertGetServerOcspResponseContext**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetserverocspresponsecontext)


```C++
typedef VOID* HCERT_SERVER_OCSP_RESPONSE;
```



## <a name="requirements"></a><span data-ttu-id="7ada5-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7ada5-110">Requirements</span></span>



| <span data-ttu-id="7ada5-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="7ada5-111">Requirement</span></span> | <span data-ttu-id="7ada5-112">Value</span><span class="sxs-lookup"><span data-stu-id="7ada5-112">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7ada5-113">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7ada5-113">Minimum supported client</span></span><br/> | <span data-ttu-id="7ada5-114">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="7ada5-114">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7ada5-115">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7ada5-115">Minimum supported server</span></span><br/> | <span data-ttu-id="7ada5-116">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="7ada5-116">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7ada5-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7ada5-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="7ada5-118"><dt>Wincrypt. h</dt></span><span class="sxs-lookup"><span data-stu-id="7ada5-118"><dt>Wincrypt.h</dt></span></span> </dl> |



 

 




