---
title: VersionIndependentProgID
description: Asocia un ProgID a un CLSID. Este valor se usa para determinar la versión más reciente de una aplicación de objeto.
ms.assetid: 5d188db9-ea4f-47fe-882f-a6caa7e86a25
keywords:
- Clave del registro VersionIndependentProgID COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5774dfa5202521bb5055bab6a62aa7c6a60b3cc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076369"
---
# <a name="versionindependentprogid"></a><span data-ttu-id="17e14-105">VersionIndependentProgID</span><span class="sxs-lookup"><span data-stu-id="17e14-105">VersionIndependentProgID</span></span>

<span data-ttu-id="17e14-106">Asocia un ProgID a un CLSID.</span><span class="sxs-lookup"><span data-stu-id="17e14-106">Associates a ProgID with a CLSID.</span></span> <span data-ttu-id="17e14-107">Este valor se usa para determinar la versión más reciente de una aplicación de objeto.</span><span class="sxs-lookup"><span data-stu-id="17e14-107">This value is used to determine the latest version of an object application.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="17e14-108">Entrada del Registro</span><span class="sxs-lookup"><span data-stu-id="17e14-108">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      VersionIndependentProgID = Program.Component
```

## <a name="remarks"></a><span data-ttu-id="17e14-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="17e14-109">Remarks</span></span>

<span data-ttu-id="17e14-110">Se trata de un valor de **reg \_ SZ** que especifica la versión más reciente de la aplicación de objeto.</span><span class="sxs-lookup"><span data-stu-id="17e14-110">This is a **REG\_SZ** value that specifies the latest version of the object application.</span></span>

<span data-ttu-id="17e14-111">El ProgID independiente de la versión se almacena y mantiene únicamente en el código de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="17e14-111">The version-independent ProgID is stored and maintained solely by application code.</span></span> <span data-ttu-id="17e14-112">Cuando se proporciona el ProgID independiente de la versión, la función [**CLSIDFromProgID**](/windows/desktop/api/combaseapi/nf-combaseapi-clsidfromprogid) devuelve el CLSID de la versión actual.</span><span class="sxs-lookup"><span data-stu-id="17e14-112">When given the version-independent ProgID, the [**CLSIDFromProgID**](/windows/desktop/api/combaseapi/nf-combaseapi-clsidfromprogid) function returns the CLSID of the current version.</span></span>

<span data-ttu-id="17e14-113">Puede usar [**CLSIDFromProgID**](/windows/desktop/api/combaseapi/nf-combaseapi-clsidfromprogid) y [**ProgIDFromCLSID**](/windows/desktop/api/combaseapi/nf-combaseapi-progidfromclsid) para realizar la conversión entre estas dos representaciones.</span><span class="sxs-lookup"><span data-stu-id="17e14-113">You can use [**CLSIDFromProgID**](/windows/desktop/api/combaseapi/nf-combaseapi-clsidfromprogid) and [**ProgIDFromCLSID**](/windows/desktop/api/combaseapi/nf-combaseapi-progidfromclsid) to convert between these two representations.</span></span>

 

 




