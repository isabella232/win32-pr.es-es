---
title: Interfaz INapSoHConstructor (NapProtocol. h)
description: Los Sha usan para construir SoHRequests y SHV para construir SoHResponses.
ms.assetid: ad79c80a-3003-4465-b350-77890c217d63
keywords:
- Interfaz INapSoHConstructor NAP
- Interfaz INapSoHConstructor NAP, descripción
topic_type:
- apiref
api_name:
- INapSoHConstructor
api_location:
- qutil.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 546a6d3b4ec262fdd725af24211338e848b2b848
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103995993"
---
# <a name="inapsohconstructor-interface"></a><span data-ttu-id="3cf85-105">Interfaz INapSoHConstructor</span><span class="sxs-lookup"><span data-stu-id="3cf85-105">INapSoHConstructor interface</span></span>

> [!Note]  
> <span data-ttu-id="3cf85-106">La plataforma de protección de acceso a redes no está disponible a partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="3cf85-106">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="3cf85-107">**INapSoHConstructor** proporciona métodos que los Sha usan para construir [**SoHRequests**](/windows/win32/api/naptypes/ns-naptypes-soh) y SHV para construir **SoHResponses**.</span><span class="sxs-lookup"><span data-stu-id="3cf85-107">The **INapSoHConstructor** provides methods that are used by SHAs to construct [**SoHRequests**](/windows/win32/api/naptypes/ns-naptypes-soh) and by SHVs to construct **SoHResponses**.</span></span>

## <a name="members"></a><span data-ttu-id="3cf85-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="3cf85-108">Members</span></span>

<span data-ttu-id="3cf85-109">La interfaz **INapSoHConstructor** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="3cf85-109">The **INapSoHConstructor** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="3cf85-110">**INapSoHConstructor** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="3cf85-110">**INapSoHConstructor** also has these types of members:</span></span>

-   [<span data-ttu-id="3cf85-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="3cf85-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="3cf85-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="3cf85-112">Methods</span></span>

<span data-ttu-id="3cf85-113">La interfaz **INapSoHConstructor** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="3cf85-113">The **INapSoHConstructor** interface has these methods.</span></span>



| <span data-ttu-id="3cf85-114">Método</span><span class="sxs-lookup"><span data-stu-id="3cf85-114">Method</span></span>                                                                                   | <span data-ttu-id="3cf85-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="3cf85-115">Description</span></span>                                         |
|:-----------------------------------------------------------------------------------------|:----------------------------------------------------|
| [<span data-ttu-id="3cf85-116">**INapSoHConstructor::AppendAttribute**</span><span class="sxs-lookup"><span data-stu-id="3cf85-116">**INapSoHConstructor::AppendAttribute**</span></span>](inapsohconstructor-appendattribute-method.md) | <span data-ttu-id="3cf85-117">Agrega un TLV al final del búfer de SoH.</span><span class="sxs-lookup"><span data-stu-id="3cf85-117">Adds a TLV to the end of the SoH buffer.</span></span><br/> |
| [<span data-ttu-id="3cf85-118">**INapSoHConstructor::GetSoH**</span><span class="sxs-lookup"><span data-stu-id="3cf85-118">**INapSoHConstructor::GetSoH**</span></span>](inapsohconstructor-getsoh-method.md)                   | <span data-ttu-id="3cf85-119">Recupera el paquete SoH construido.</span><span class="sxs-lookup"><span data-stu-id="3cf85-119">Retrieves the constructed SoH packet.</span></span><br/>    |
| [<span data-ttu-id="3cf85-120">**INapSoHConstructor:: Initialize**</span><span class="sxs-lookup"><span data-stu-id="3cf85-120">**INapSoHConstructor::Initialize**</span></span>](inapsohconstructor-initialize-method.md)           | <span data-ttu-id="3cf85-121">Inicializa el paquete SoH.</span><span class="sxs-lookup"><span data-stu-id="3cf85-121">Initializes the SoH packet.</span></span><br/>              |
| [<span data-ttu-id="3cf85-122">**INapSoHConstructor:: Validate**</span><span class="sxs-lookup"><span data-stu-id="3cf85-122">**INapSoHConstructor::Validate**</span></span>](inapsohconstructor-validate-method.md)               | <span data-ttu-id="3cf85-123">Comprueba la validez del paquete SoH.</span><span class="sxs-lookup"><span data-stu-id="3cf85-123">Checks the validity of the SoH packet.</span></span><br/>   |



 

## <a name="requirements"></a><span data-ttu-id="3cf85-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3cf85-124">Requirements</span></span>



| <span data-ttu-id="3cf85-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="3cf85-125">Requirement</span></span> | <span data-ttu-id="3cf85-126">Value</span><span class="sxs-lookup"><span data-stu-id="3cf85-126">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="3cf85-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3cf85-127">Minimum supported client</span></span><br/> | <span data-ttu-id="3cf85-128">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="3cf85-128">Windows Vista \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="3cf85-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3cf85-129">Minimum supported server</span></span><br/> | <span data-ttu-id="3cf85-130">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="3cf85-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="3cf85-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3cf85-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="3cf85-132"><dt>NapProtocol. h</dt></span><span class="sxs-lookup"><span data-stu-id="3cf85-132"><dt>NapProtocol.h</dt></span></span> </dl>   |
| <span data-ttu-id="3cf85-133">IDL</span><span class="sxs-lookup"><span data-stu-id="3cf85-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="3cf85-134"><dt>NapProtocol. idl</dt></span><span class="sxs-lookup"><span data-stu-id="3cf85-134"><dt>NapProtocol.idl</dt></span></span> </dl> |
| <span data-ttu-id="3cf85-135">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3cf85-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3cf85-136"><dt>Qutil.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3cf85-136"><dt>Qutil.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="3cf85-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="3cf85-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3cf85-138">Interfaces NAP</span><span class="sxs-lookup"><span data-stu-id="3cf85-138">NAP Interfaces</span></span>](nap-interfaces.md)
</dt> <dt>

[<span data-ttu-id="3cf85-139">Referencia de NAP</span><span class="sxs-lookup"><span data-stu-id="3cf85-139">NAP Reference</span></span>](nap-reference.md)
</dt> </dl>

 

