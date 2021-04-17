---
title: PeapServerUseAllPurposeCert
description: La clave del registro PeapServerUseAllPurposeCert determina si se usan certificados para la autenticación PEAP.
ms.assetid: e239fb88-4bf3-49b6-a95c-67a8c060a50d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc90f083f9020ad02960d7620a2ab54706df203e
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2019
ms.locfileid: "104358538"
---
# <a name="peapserveruseallpurposecert"></a><span data-ttu-id="d9dcb-103">PeapServerUseAllPurposeCert</span><span class="sxs-lookup"><span data-stu-id="d9dcb-103">PeapServerUseAllPurposeCert</span></span>

<span data-ttu-id="d9dcb-104">La clave del registro PeapServerUseAllPurposeCert determina si se usan certificados para la autenticación PEAP.</span><span class="sxs-lookup"><span data-stu-id="d9dcb-104">The PeapServerUseAllPurposeCert registry key determines if all-purpose certificates are used for PEAP authentication.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="d9dcb-105">Entrada del Registro</span><span class="sxs-lookup"><span data-stu-id="d9dcb-105">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\Rasman\PPP\EAP\25
   PeapServerUseAllPurposeCert = value
```

## <a name="remarks"></a><span data-ttu-id="d9dcb-106">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d9dcb-106">Remarks</span></span>

<span data-ttu-id="d9dcb-107">Se trata de un valor de **Registro \_ DWORD** .</span><span class="sxs-lookup"><span data-stu-id="d9dcb-107">This is a **REG\_DWORD** value.</span></span>



| <span data-ttu-id="d9dcb-108">Value</span><span class="sxs-lookup"><span data-stu-id="d9dcb-108">Value</span></span>        | <span data-ttu-id="d9dcb-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="d9dcb-109">Description</span></span>                                                                                                      |
|--------------|------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d9dcb-110">1</span><span class="sxs-lookup"><span data-stu-id="d9dcb-110">1</span></span>            | <span data-ttu-id="d9dcb-111">Los certificados para todos los propósitos del almacén de certificados del cliente o del servidor se seleccionan para la autenticación PEAP.</span><span class="sxs-lookup"><span data-stu-id="d9dcb-111">All-purpose certificates in the client's or server's certificate store are selected for PEAP authentication.</span></span>     |
| <span data-ttu-id="d9dcb-112">Otros valores</span><span class="sxs-lookup"><span data-stu-id="d9dcb-112">Other values</span></span> | <span data-ttu-id="d9dcb-113">Los certificados de todos los propósitos del almacén de certificados del cliente o del servidor no se seleccionan para la autenticación PEAP.</span><span class="sxs-lookup"><span data-stu-id="d9dcb-113">All-purpose certificates in the client's or server's certificate store are not selected for PEAP authentication.</span></span> |



 

<span data-ttu-id="d9dcb-114">Si este valor del registro no está presente, se seleccionan los certificados de todos los propósitos en el almacén de certificados del cliente o del servidor para la autenticación PEAP.</span><span class="sxs-lookup"><span data-stu-id="d9dcb-114">If this registry value is not present, all-purpose certificates in the client's or server's certificate store are selected for PEAP authentication.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d9dcb-115">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d9dcb-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d9dcb-116">Configuración del registro de EAPHost</span><span class="sxs-lookup"><span data-stu-id="d9dcb-116">EAPHost Registry Settings</span></span>](eaphost-registry-settings.md)
</dt> </dl>

 

 




