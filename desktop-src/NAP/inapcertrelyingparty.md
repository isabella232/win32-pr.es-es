---
title: Interfaz INapCertRelyingParty (NapCertRelyingParty. h)
description: 'Certificado: los usuarios de confianza deben usar para comunicarse con el NapAgent.'
ms.assetid: e5ae0f4d-24fa-4049-82d9-1c9baeb34e32
keywords:
- Interfaz INapCertRelyingParty NAP
- Interfaz INapCertRelyingParty NAP, descripción
topic_type:
- apiref
api_name:
- INapCertRelyingParty
api_location:
- NapCertRelyingParty.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85b4439389c6ee65076f710bb6ea752c73a51ecd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079543"
---
# <a name="inapcertrelyingparty-interface"></a><span data-ttu-id="fb7c8-105">Interfaz INapCertRelyingParty</span><span class="sxs-lookup"><span data-stu-id="fb7c8-105">INapCertRelyingParty interface</span></span>

> [!Note]  
> <span data-ttu-id="fb7c8-106">La plataforma de protección de acceso a redes no está disponible a partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="fb7c8-106">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="fb7c8-107">La interfaz **INapCertRelyingParty** proporciona métodos que los usuarios de confianza de certificados deben usar para comunicarse con NapAgent.</span><span class="sxs-lookup"><span data-stu-id="fb7c8-107">The **INapCertRelyingParty** interface provides methods that certificate-relying parties must use to communicate with the NapAgent.</span></span>

## <a name="members"></a><span data-ttu-id="fb7c8-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="fb7c8-108">Members</span></span>

<span data-ttu-id="fb7c8-109">La interfaz **INapCertRelyingParty** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="fb7c8-109">The **INapCertRelyingParty** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="fb7c8-110">**INapCertRelyingParty** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="fb7c8-110">**INapCertRelyingParty** also has these types of members:</span></span>

-   [<span data-ttu-id="fb7c8-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="fb7c8-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="fb7c8-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="fb7c8-112">Methods</span></span>

<span data-ttu-id="fb7c8-113">La interfaz **INapCertRelyingParty** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="fb7c8-113">The **INapCertRelyingParty** interface has these methods.</span></span>



| <span data-ttu-id="fb7c8-114">Método</span><span class="sxs-lookup"><span data-stu-id="fb7c8-114">Method</span></span>                                                                                                        | <span data-ttu-id="fb7c8-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="fb7c8-115">Description</span></span>                                                                     |
|:--------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------|
| [<span data-ttu-id="fb7c8-116">**INapCertRelyingParty::GetSubscribedRelyingParties**</span><span class="sxs-lookup"><span data-stu-id="fb7c8-116">**INapCertRelyingParty::GetSubscribedRelyingParties**</span></span>](inapcertrelyingparty-getsubscribedrelyingparties.md) | <span data-ttu-id="fb7c8-117">Obtiene una lista de usuarios de confianza que se han suscrito.</span><span class="sxs-lookup"><span data-stu-id="fb7c8-117">Gets a list of relying parties that have subscribed.</span></span><br/>                 |
| [<span data-ttu-id="fb7c8-118">**INapCertRelyingParty::SubscribeCertByGroup**</span><span class="sxs-lookup"><span data-stu-id="fb7c8-118">**INapCertRelyingParty::SubscribeCertByGroup**</span></span>](inapcertrelyingparty-subscribecertbygroup.md)               | <span data-ttu-id="fb7c8-119">Se suscribe a un servidor de certificados de mantenimiento ya registrado (HCS).</span><span class="sxs-lookup"><span data-stu-id="fb7c8-119">Subscribes to an already-registered health certificate server (HCS).</span></span><br/> |
| [<span data-ttu-id="fb7c8-120">**INapCertRelyingParty::UnSubscribeCertByGroup**</span><span class="sxs-lookup"><span data-stu-id="fb7c8-120">**INapCertRelyingParty::UnSubscribeCertByGroup**</span></span>](inapcertrelyingparty-unsubscribecertbygroup.md)           | <span data-ttu-id="fb7c8-121">Cancela la suscripción de un servidor de HCS.</span><span class="sxs-lookup"><span data-stu-id="fb7c8-121">Unsubscribes from an HCS server.</span></span><br/>                                     |



 

## <a name="requirements"></a><span data-ttu-id="fb7c8-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fb7c8-122">Requirements</span></span>



| <span data-ttu-id="fb7c8-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="fb7c8-123">Requirement</span></span> | <span data-ttu-id="fb7c8-124">Value</span><span class="sxs-lookup"><span data-stu-id="fb7c8-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fb7c8-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fb7c8-125">Minimum supported client</span></span><br/> | <span data-ttu-id="fb7c8-126">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="fb7c8-126">Windows Vista \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="fb7c8-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fb7c8-127">Minimum supported server</span></span><br/> | <span data-ttu-id="fb7c8-128">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="fb7c8-128">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="fb7c8-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fb7c8-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="fb7c8-130"><dt>NapCertRelyingParty. h</dt></span><span class="sxs-lookup"><span data-stu-id="fb7c8-130"><dt>NapCertRelyingParty.h</dt></span></span> </dl>   |
| <span data-ttu-id="fb7c8-131">IDL</span><span class="sxs-lookup"><span data-stu-id="fb7c8-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="fb7c8-132"><dt>NapCertRelyingParty. idl</dt></span><span class="sxs-lookup"><span data-stu-id="fb7c8-132"><dt>NapCertRelyingParty.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fb7c8-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="fb7c8-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb7c8-134">Interfaces NAP</span><span class="sxs-lookup"><span data-stu-id="fb7c8-134">NAP Interfaces</span></span>](nap-interfaces.md)
</dt> <dt>

[<span data-ttu-id="fb7c8-135">Referencia de NAP</span><span class="sxs-lookup"><span data-stu-id="fb7c8-135">NAP Reference</span></span>](nap-reference.md)
</dt> </dl>

 

