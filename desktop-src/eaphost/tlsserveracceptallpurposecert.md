---
title: TlsServerAcceptAllPurposeCert
description: La clave del registro TlsServerAcceptAllPurposeCert determina si se aceptan certificados de todos los propósitos para la autenticación EAP-TLS.
ms.assetid: F0881397-5D8C-4C8F-8EB5-6D59454C55B7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c6561418d8d9cb06fb9618e6b93189cbd28e408
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2019
ms.locfileid: "105665769"
---
# <a name="tlsserveracceptallpurposecert"></a><span data-ttu-id="7d9f2-103">TlsServerAcceptAllPurposeCert</span><span class="sxs-lookup"><span data-stu-id="7d9f2-103">TlsServerAcceptAllPurposeCert</span></span>

<span data-ttu-id="7d9f2-104">La clave del registro TlsServerAcceptAllPurposeCert determina si se aceptan certificados de todos los propósitos para la autenticación EAP-TLS.</span><span class="sxs-lookup"><span data-stu-id="7d9f2-104">The TlsServerAcceptAllPurposeCert registry key determines if all-purpose certificates are accepted for EAP-TLS authentication.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="7d9f2-105">Entrada del Registro</span><span class="sxs-lookup"><span data-stu-id="7d9f2-105">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\Rasman\PPP\EAP\13
   TlsServerAcceptAllPurposeCert = value
```

## <a name="remarks"></a><span data-ttu-id="7d9f2-106">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7d9f2-106">Remarks</span></span>

<span data-ttu-id="7d9f2-107">Se trata de un valor de **Registro \_ DWORD** .</span><span class="sxs-lookup"><span data-stu-id="7d9f2-107">This is a **REG\_DWORD** value.</span></span>



| <span data-ttu-id="7d9f2-108">Value</span><span class="sxs-lookup"><span data-stu-id="7d9f2-108">Value</span></span>        | <span data-ttu-id="7d9f2-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="7d9f2-109">Description</span></span>                                                                                                 |
|--------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7d9f2-110">1</span><span class="sxs-lookup"><span data-stu-id="7d9f2-110">1</span></span>            | <span data-ttu-id="7d9f2-111">El servidor y el cliente aceptan certificados para todos los fines enviados por la otra parte para la autenticación EAP-TLS.</span><span class="sxs-lookup"><span data-stu-id="7d9f2-111">Server and client accept all-purpose certificates sent by the other party for EAP-TLS authentication.</span></span>       |
| <span data-ttu-id="7d9f2-112">Otros valores</span><span class="sxs-lookup"><span data-stu-id="7d9f2-112">Other values</span></span> | <span data-ttu-id="7d9f2-113">El servidor y el cliente no aceptan certificados para todos los fines enviados por la otra parte para la autenticación EAP-TLS</span><span class="sxs-lookup"><span data-stu-id="7d9f2-113">Server and client do not accept all-purpose certificates sent by the other party for EAP-TLS authentication</span></span> |



 

<span data-ttu-id="7d9f2-114">Si este valor del registro no está presente, el servidor y el cliente aceptan los certificados de propósito único enviados por la otra entidad para la autenticación EAP-TLS.</span><span class="sxs-lookup"><span data-stu-id="7d9f2-114">If this registry value is not present, the server and client accept all-purpose certificates sent by the other party for EAP-TLS authentication.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7d9f2-115">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7d9f2-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7d9f2-116">Configuración del registro de EAPHost</span><span class="sxs-lookup"><span data-stu-id="7d9f2-116">EAPHost Registry Settings</span></span>](eaphost-registry-settings.md)
</dt> </dl>

 

 




