---
title: DoNotAddAllApplicationPackagesToRestrictions
description: Determina si RPCSS anexa automáticamente un \_ \_ SID de todos los paquetes de aplicación a las restricciones de com de forma predeterminada.
ms.assetid: 4DC1237E-F3EF-40EA-8E64-57320F0C4CC5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 800077c61e01cf0b3f76d5a92f8282c7ecca12e4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418428"
---
# <a name="donotaddallapplicationpackagestorestrictions"></a><span data-ttu-id="ddbbd-103">DoNotAddAllApplicationPackagesToRestrictions</span><span class="sxs-lookup"><span data-stu-id="ddbbd-103">DoNotAddAllApplicationPackagesToRestrictions</span></span>

<span data-ttu-id="ddbbd-104">Determina si RPCSS anexa automáticamente un \_ \_ SID de todos los paquetes de aplicación a las restricciones de com de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="ddbbd-104">Determines whether RPCSS automatically appends an ALL\_APPLICATION\_PACKAGES SID to COM restrictions by default.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="ddbbd-105">Entrada del Registro</span><span class="sxs-lookup"><span data-stu-id="ddbbd-105">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   DoNotAddAllApplicationPackagesToRestrictions = value
```

## <a name="remarks"></a><span data-ttu-id="ddbbd-106">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ddbbd-106">Remarks</span></span>

<span data-ttu-id="ddbbd-107">Se trata de un valor de **Registro \_ DWORD** .</span><span class="sxs-lookup"><span data-stu-id="ddbbd-107">This is a **REG\_DWORD** value.</span></span>



| <span data-ttu-id="ddbbd-108">Value</span><span class="sxs-lookup"><span data-stu-id="ddbbd-108">Value</span></span> | <span data-ttu-id="ddbbd-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="ddbbd-109">Description</span></span>                                                                               |
|-------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="ddbbd-110">0</span><span class="sxs-lookup"><span data-stu-id="ddbbd-110">0</span></span>     | <span data-ttu-id="ddbbd-111">Deshabilita las aplicaciones de la tienda Windows tras la migración de Windows 7 a Windows 8.</span><span class="sxs-lookup"><span data-stu-id="ddbbd-111">Disables Windows Store apps upon migration from Windows 7 to Windows 8.</span></span>                   |
| <span data-ttu-id="ddbbd-112">1</span><span class="sxs-lookup"><span data-stu-id="ddbbd-112">1</span></span>     | <span data-ttu-id="ddbbd-113">No agrega el SID todos \_ los \_ paquetes de aplicación a las restricciones com.</span><span class="sxs-lookup"><span data-stu-id="ddbbd-113">Does not add the ALL\_APPLICATION\_PACKAGES SID to COM restrictions.</span></span> <span data-ttu-id="ddbbd-114">Este es el valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="ddbbd-114">This is the default.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="ddbbd-115">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ddbbd-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ddbbd-116">Establecer la seguridad de las aplicaciones COM</span><span class="sxs-lookup"><span data-stu-id="ddbbd-116">Setting Security for COM Applications</span></span>](setting-security-for-com-applications.md)
</dt> </dl>

 

 




