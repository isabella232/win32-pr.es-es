---
title: PeapServerAcceptAllPurposeCert
description: La clave del registro PeapServerAcceptAllPurposeCert determina si se aceptan certificados para la autenticación PEAP.
ms.assetid: 59C58459-7735-4733-9F95-646864802D70
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b291696c6bee90b4f980d8f96ad96faf40fe3376
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2019
ms.locfileid: "105695518"
---
# <a name="peapserveracceptallpurposecert"></a><span data-ttu-id="4fa32-103">PeapServerAcceptAllPurposeCert</span><span class="sxs-lookup"><span data-stu-id="4fa32-103">PeapServerAcceptAllPurposeCert</span></span>

<span data-ttu-id="4fa32-104">La clave del registro PeapServerAcceptAllPurposeCert determina si se aceptan certificados para la autenticación PEAP.</span><span class="sxs-lookup"><span data-stu-id="4fa32-104">The PeapServerAcceptAllPurposeCert registry key determines if all-purpose certificates are accepted for PEAP authentication.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="4fa32-105">Entrada del Registro</span><span class="sxs-lookup"><span data-stu-id="4fa32-105">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\Rasman\PPP\EAP\25
   PeapServerAcceptAllPurposeCert = value
```

## <a name="remarks"></a><span data-ttu-id="4fa32-106">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4fa32-106">Remarks</span></span>

<span data-ttu-id="4fa32-107">Se trata de un valor de **Registro \_ DWORD** .</span><span class="sxs-lookup"><span data-stu-id="4fa32-107">This is a **REG\_DWORD** value.</span></span>



| <span data-ttu-id="4fa32-108">Value</span><span class="sxs-lookup"><span data-stu-id="4fa32-108">Value</span></span>        | <span data-ttu-id="4fa32-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="4fa32-109">Description</span></span>                                                                                                 |
|--------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4fa32-110">1</span><span class="sxs-lookup"><span data-stu-id="4fa32-110">1</span></span>            | <span data-ttu-id="4fa32-111">El servidor y el cliente aceptan certificados para todos los fines enviados por la otra parte para la autenticación EAP-TLS.</span><span class="sxs-lookup"><span data-stu-id="4fa32-111">Server and client accept all-purpose certificates sent by the other party for EAP-TLS authentication.</span></span>       |
| <span data-ttu-id="4fa32-112">Otros valores</span><span class="sxs-lookup"><span data-stu-id="4fa32-112">Other values</span></span> | <span data-ttu-id="4fa32-113">El servidor y el cliente no aceptan certificados para todos los fines enviados por la otra parte para la autenticación EAP-TLS</span><span class="sxs-lookup"><span data-stu-id="4fa32-113">Server and client do not accept all-purpose certificates sent by the other party for EAP-TLS authentication</span></span> |



 

<span data-ttu-id="4fa32-114">Si este valor del registro no está presente, el servidor y el cliente aceptan los certificados de propósito único enviados por la otra parte para la autenticación PEAP.</span><span class="sxs-lookup"><span data-stu-id="4fa32-114">If this registry value is not present, the server and client accept all-purpose certificates sent by the other party for PEAP authentication.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4fa32-115">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4fa32-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4fa32-116">Configuración del registro de EAPHost</span><span class="sxs-lookup"><span data-stu-id="4fa32-116">EAPHost Registry Settings</span></span>](eaphost-registry-settings.md)
</dt> </dl>

 

 




