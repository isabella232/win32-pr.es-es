---
title: TlsServerUseAllPurposeCert
description: La clave del registro TlsServerUseAllPurposeCert determina si se usan certificados para la autenticación EAP-TLS.
ms.assetid: a672cecb-6bba-4ba6-b362-f6d5a220184b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b7cb767a8f6c8f40b377cca84d948b384170486
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2019
ms.locfileid: "104358531"
---
# <a name="tlsserveruseallpurposecert"></a><span data-ttu-id="f81e9-103">TlsServerUseAllPurposeCert</span><span class="sxs-lookup"><span data-stu-id="f81e9-103">TlsServerUseAllPurposeCert</span></span>

<span data-ttu-id="f81e9-104">La clave del registro TlsServerUseAllPurposeCert determina si se usan certificados para la autenticación EAP-TLS.</span><span class="sxs-lookup"><span data-stu-id="f81e9-104">The TlsServerUseAllPurposeCert registry key determines if all-purpose certificates are used for EAP-TLS authentication.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="f81e9-105">Entrada del Registro</span><span class="sxs-lookup"><span data-stu-id="f81e9-105">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\Rasman\PPP\EAP\13
   TlsServerUseAllPurposeCert = value
```

## <a name="remarks"></a><span data-ttu-id="f81e9-106">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f81e9-106">Remarks</span></span>

<span data-ttu-id="f81e9-107">Se trata de un valor de **Registro \_ DWORD** .</span><span class="sxs-lookup"><span data-stu-id="f81e9-107">This is a **REG\_DWORD** value.</span></span>



| <span data-ttu-id="f81e9-108">Value</span><span class="sxs-lookup"><span data-stu-id="f81e9-108">Value</span></span>        | <span data-ttu-id="f81e9-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="f81e9-109">Description</span></span>                                                                                                      |
|--------------|------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f81e9-110">1</span><span class="sxs-lookup"><span data-stu-id="f81e9-110">1</span></span>            | <span data-ttu-id="f81e9-111">Los certificados para todos los propósitos del almacén de certificados del cliente o del servidor se seleccionan para la autenticación PEAP.</span><span class="sxs-lookup"><span data-stu-id="f81e9-111">All-purpose certificates in the client's or server's certificate store are selected for PEAP authentication.</span></span>     |
| <span data-ttu-id="f81e9-112">Otros valores</span><span class="sxs-lookup"><span data-stu-id="f81e9-112">Other values</span></span> | <span data-ttu-id="f81e9-113">Los certificados de todos los propósitos del almacén de certificados del cliente o del servidor no se seleccionan para la autenticación PEAP.</span><span class="sxs-lookup"><span data-stu-id="f81e9-113">All-purpose certificates in the client's or server's certificate store are not selected for PEAP authentication.</span></span> |



 

<span data-ttu-id="f81e9-114">Si este valor del registro no está presente, se seleccionan los certificados de todos los propósitos en el almacén de certificados del cliente o del servidor para la autenticación EAP-TLS.</span><span class="sxs-lookup"><span data-stu-id="f81e9-114">If this registry value is not present, all-purpose certificates in the client's or server's certificate store are selected for EAP-TLS authentication.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f81e9-115">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f81e9-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f81e9-116">Configuración del registro de EAPHost</span><span class="sxs-lookup"><span data-stu-id="f81e9-116">EAPHost Registry Settings</span></span>](eaphost-registry-settings.md)
</dt> </dl>

 

 




