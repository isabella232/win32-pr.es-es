---
title: Control
description: Identifica un objeto como un control ActiveX.
ms.assetid: 2487e642-1d21-4811-87dd-b280be98a44b
keywords:
- Control COM de la clave del registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3722d85b38399d7e95f226749bda45ccc82d1369
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104419143"
---
# <a name="control"></a><span data-ttu-id="65211-104">Control</span><span class="sxs-lookup"><span data-stu-id="65211-104">Control</span></span>

<span data-ttu-id="65211-105">Identifica un objeto como un control ActiveX.</span><span class="sxs-lookup"><span data-stu-id="65211-105">Identifies an object as an ActiveX Control.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="65211-106">Entrada del Registro</span><span class="sxs-lookup"><span data-stu-id="65211-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      Control
```

## <a name="remarks"></a><span data-ttu-id="65211-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="65211-107">Remarks</span></span>

<span data-ttu-id="65211-108">Los contenedores usan esta entrada opcional para rellenar los cuadros de diálogo.</span><span class="sxs-lookup"><span data-stu-id="65211-108">This optional entry is used by containers to fill in dialog boxes.</span></span> <span data-ttu-id="65211-109">El contenedor usa esta subclave para determinar si se debe incluir un objeto en un cuadro de diálogo que muestre controles ActiveX.</span><span class="sxs-lookup"><span data-stu-id="65211-109">The container uses this subkey to determine whether to include an object in a dialog box that displays ActiveX Controls.</span></span> <span data-ttu-id="65211-110">Un control puede omitir esta entrada si está diseñada para funcionar solo con un contenedor específico y, por tanto, no está diseñada para insertarse en otros contenedores.</span><span class="sxs-lookup"><span data-stu-id="65211-110">A control can omit this entry if it is designed to work only with a specific container and therefore does is not intended to be inserted in other containers.</span></span>

 

 




