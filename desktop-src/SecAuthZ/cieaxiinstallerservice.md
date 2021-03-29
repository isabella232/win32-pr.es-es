---
description: Implementa las interfaces IAxiService y IeAxiServiceCallback.
ms.assetid: 39f2ee3a-d4fd-4091-acd6-3d6b715bea75
title: Objeto CIeAxiInstallerService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIeAxiInstallerService
api_type:
- COM
api_location: ''
ms.openlocfilehash: b5ae7ec2a2c904a523f3388fa08a3bf2e44fec9d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001221"
---
# <a name="cieaxiinstallerservice-object"></a><span data-ttu-id="0ba58-103">Objeto CIeAxiInstallerService</span><span class="sxs-lookup"><span data-stu-id="0ba58-103">CIeAxiInstallerService object</span></span>

<span data-ttu-id="0ba58-104">El objeto **CIeAxiInstallerService** implementa las interfaces [**IAxiService**](ieaxiservice.md) y [**IeAxiServiceCallback**](ieaxiservicecallback.md) .</span><span class="sxs-lookup"><span data-stu-id="0ba58-104">The **CIeAxiInstallerService** object implements the [**IAxiService**](ieaxiservice.md) and [**IeAxiServiceCallback**](ieaxiservicecallback.md) interfaces.</span></span>

<span data-ttu-id="0ba58-105">Este objeto no se declara en un encabezado público.</span><span class="sxs-lookup"><span data-stu-id="0ba58-105">This object is not declared in a public header.</span></span> <span data-ttu-id="0ba58-106">Las aplicaciones deben definirla.</span><span class="sxs-lookup"><span data-stu-id="0ba58-106">Applications must define it themselves.</span></span> <span data-ttu-id="0ba58-107">El siguiente fragmento del lenguaje de definición de interfaz (IDL) describe este objeto, incluido su CLSID.</span><span class="sxs-lookup"><span data-stu-id="0ba58-107">The following Interface Definition Language (IDL) fragment describes this object, including its CLSID.</span></span>

``` syntax
[
        uuid(90F18417-F0F1-484E-9D3C-59DCEEE5DBD8)
]
    coclass CIeAxiInstallerService
    {
        [default] interface IeAxiService;
        interface IeAxiServiceCallback;
    }

```

## <a name="requirements"></a><span data-ttu-id="0ba58-108">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0ba58-108">Requirements</span></span>



| <span data-ttu-id="0ba58-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="0ba58-109">Requirement</span></span> | <span data-ttu-id="0ba58-110">Value</span><span class="sxs-lookup"><span data-stu-id="0ba58-110">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0ba58-111">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0ba58-111">Minimum supported client</span></span><br/> | <span data-ttu-id="0ba58-112">Windows Vista Business, Windows Vista Enterprise, Windows Vista Ultimate \[ solo aplicaciones de escritorio\]</span><span class="sxs-lookup"><span data-stu-id="0ba58-112">Windows Vista Business, Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="0ba58-113">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0ba58-113">Minimum supported server</span></span><br/> | <span data-ttu-id="0ba58-114">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="0ba58-114">None supported</span></span><br/>                                                                                 |



## <a name="see-also"></a><span data-ttu-id="0ba58-115">Vea también</span><span class="sxs-lookup"><span data-stu-id="0ba58-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ba58-116">**IAxiService**</span><span class="sxs-lookup"><span data-stu-id="0ba58-116">**IAxiService**</span></span>](ieaxiservice.md)
</dt> <dt>

[<span data-ttu-id="0ba58-117">**IeAxiServiceCallback**</span><span class="sxs-lookup"><span data-stu-id="0ba58-117">**IeAxiServiceCallback**</span></span>](ieaxiservicecallback.md)
</dt> </dl>

 

 




