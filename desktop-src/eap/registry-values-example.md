---
title: Ejemplo de valores del registro
description: En el ejemplo siguiente se muestran los datos posibles para algunos de los valores del registro del Protocolo de autenticación.
ms.assetid: 07772af0-db56-4cc6-ad72-cf79d3813883
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7bcbc3d4ca10a3e9298177a5eea240d0d34ade04
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2019
ms.locfileid: "104077160"
---
# <a name="registry-values-example"></a><span data-ttu-id="09429-103">Ejemplo de valores del registro</span><span class="sxs-lookup"><span data-stu-id="09429-103">Registry Values Example</span></span>

<span data-ttu-id="09429-104">En el ejemplo siguiente se muestran los datos posibles para algunos de los valores del registro del Protocolo de autenticación.</span><span class="sxs-lookup"><span data-stu-id="09429-104">The following example shows possible data for some of the authentication protocol registry values.</span></span>

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Services
            Rasman
               PPP
                  EAP
                     40
                        Path
                        FriendlyName
                        ConfigUIPath
                        IdentityPath
                        InteractiveUIPath
                        RequireConfigUI
                        ConfigCLSID
                        StandaloneSupported
```



| <span data-ttu-id="09429-105">Nombre de clave</span><span class="sxs-lookup"><span data-stu-id="09429-105">Key Name</span></span>            | <span data-ttu-id="09429-106">Datatype</span><span class="sxs-lookup"><span data-stu-id="09429-106">Datatype</span></span>        | <span data-ttu-id="09429-107">Value</span><span class="sxs-lookup"><span data-stu-id="09429-107">Value</span></span>                                  |
|---------------------|-----------------|----------------------------------------|
| <span data-ttu-id="09429-108">Ruta</span><span class="sxs-lookup"><span data-stu-id="09429-108">Path</span></span>                | <span data-ttu-id="09429-109">REG \_ expandir \_ SZ</span><span class="sxs-lookup"><span data-stu-id="09429-109">REG\_EXPAND\_SZ</span></span> | <span data-ttu-id="09429-110">% SystemRoot% \\ system32 \\sample.dll</span><span class="sxs-lookup"><span data-stu-id="09429-110">%SystemRoot%\\system32\\sample.dll</span></span>     |
| <span data-ttu-id="09429-111">FriendlyName</span><span class="sxs-lookup"><span data-stu-id="09429-111">FriendlyName</span></span>        | <span data-ttu-id="09429-112">Registro \_ SZ</span><span class="sxs-lookup"><span data-stu-id="09429-112">REG\_SZ</span></span>         | <span data-ttu-id="09429-113">Protocolo EAP de ejemplo</span><span class="sxs-lookup"><span data-stu-id="09429-113">Sample EAP Protocol</span></span>                    |
| <span data-ttu-id="09429-114">ConfigUIPath</span><span class="sxs-lookup"><span data-stu-id="09429-114">ConfigUIPath</span></span>        | <span data-ttu-id="09429-115">REG \_ expandir \_ SZ</span><span class="sxs-lookup"><span data-stu-id="09429-115">REG\_EXPAND\_SZ</span></span> | <span data-ttu-id="09429-116">% SystemRoot% \\ system32 \\sample.dll</span><span class="sxs-lookup"><span data-stu-id="09429-116">%SystemRoot%\\system32\\sample.dll</span></span>     |
| <span data-ttu-id="09429-117">IdentityPath</span><span class="sxs-lookup"><span data-stu-id="09429-117">IdentityPath</span></span>        | <span data-ttu-id="09429-118">REG \_ expandir \_ SZ</span><span class="sxs-lookup"><span data-stu-id="09429-118">REG\_EXPAND\_SZ</span></span> | <span data-ttu-id="09429-119">% SystemRoot% \\ system32 \\sample.dll</span><span class="sxs-lookup"><span data-stu-id="09429-119">%SystemRoot%\\system32\\sample.dll</span></span>     |
| <span data-ttu-id="09429-120">InteractiveUIPath</span><span class="sxs-lookup"><span data-stu-id="09429-120">InteractiveUIPath</span></span>   | <span data-ttu-id="09429-121">REG \_ expandir \_ SZ</span><span class="sxs-lookup"><span data-stu-id="09429-121">REG\_EXPAND\_SZ</span></span> | <span data-ttu-id="09429-122">% SystemRoot% \\ system32 \\sample.dll</span><span class="sxs-lookup"><span data-stu-id="09429-122">%SystemRoot%\\system32\\sample.dll</span></span>     |
| <span data-ttu-id="09429-123">RequireConfigUI</span><span class="sxs-lookup"><span data-stu-id="09429-123">RequireConfigUI</span></span>     | <span data-ttu-id="09429-124">\_valor DWORD reg</span><span class="sxs-lookup"><span data-stu-id="09429-124">REG\_DWORD</span></span>      | <span data-ttu-id="09429-125">1</span><span class="sxs-lookup"><span data-stu-id="09429-125">1</span></span>                                      |
| <span data-ttu-id="09429-126">ConfigCLSID</span><span class="sxs-lookup"><span data-stu-id="09429-126">ConfigCLSID</span></span>         | <span data-ttu-id="09429-127">Registro \_ SZ</span><span class="sxs-lookup"><span data-stu-id="09429-127">REG\_SZ</span></span>         | <span data-ttu-id="09429-128">{0000031A-0000-0000-C000-000000000046}</span><span class="sxs-lookup"><span data-stu-id="09429-128">{0000031A-0000-0000-C000-000000000046}</span></span> |
| <span data-ttu-id="09429-129">StandaloneSupported</span><span class="sxs-lookup"><span data-stu-id="09429-129">StandaloneSupported</span></span> | <span data-ttu-id="09429-130">\_valor DWORD reg</span><span class="sxs-lookup"><span data-stu-id="09429-130">REG\_DWORD</span></span>      | <span data-ttu-id="09429-131">1</span><span class="sxs-lookup"><span data-stu-id="09429-131">1</span></span>                                      |



 

 

 




