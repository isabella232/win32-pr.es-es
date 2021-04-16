---
description: Inicializa el canal autenticado.
ms.assetid: a74edbaa-af57-4f8e-9974-f6053f59377f
title: D3DAUTHENTICATEDCONFIGURE_INITIALIZE (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCONFIGURE_INITIALIZE
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 2cd3238b7a7eea27356ce76ec9c83bf8aea4d7f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696149"
---
# <a name="d3dauthenticatedconfigure_initialize"></a><span data-ttu-id="b5e77-103">D3DAUTHENTICATEDCONFIGURE \_ inicializar</span><span class="sxs-lookup"><span data-stu-id="b5e77-103">D3DAUTHENTICATEDCONFIGURE\_INITIALIZE</span></span>

<span data-ttu-id="b5e77-104">Inicializa el canal autenticado.</span><span class="sxs-lookup"><span data-stu-id="b5e77-104">Initializes the authenticated channel.</span></span>



| <span data-ttu-id="b5e77-105">Requisito</span><span class="sxs-lookup"><span data-stu-id="b5e77-105">Requirement</span></span> | <span data-ttu-id="b5e77-106">Value</span><span class="sxs-lookup"><span data-stu-id="b5e77-106">Value</span></span> |
|--------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b5e77-107">GUID de comando</span><span class="sxs-lookup"><span data-stu-id="b5e77-107">Command GUID</span></span> | <span data-ttu-id="b5e77-108">**D3DAUTHENTICATEDCONFIGURE \_ inicializar**</span><span class="sxs-lookup"><span data-stu-id="b5e77-108">**D3DAUTHENTICATEDCONFIGURE\_INITIALIZE**</span></span>                                                           |
| <span data-ttu-id="b5e77-109">Datos de entrada</span><span class="sxs-lookup"><span data-stu-id="b5e77-109">Input data</span></span>   | [<span data-ttu-id="b5e77-110">**D3DAUTHENTICATEDCHANNEL \_ CONFIGUREINITIALIZE**</span><span class="sxs-lookup"><span data-stu-id="b5e77-110">**D3DAUTHENTICATEDCHANNEL\_CONFIGUREINITIALIZE**</span></span>](d3dauthenticatedchannel-configureinitialize.md) |



 

## <a name="remarks"></a><span data-ttu-id="b5e77-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b5e77-111">Remarks</span></span>

<span data-ttu-id="b5e77-112">Envíe este comando una vez, al principio de la sesión.</span><span class="sxs-lookup"><span data-stu-id="b5e77-112">Send this command once, at the start of the session.</span></span> <span data-ttu-id="b5e77-113">Este comando solo se puede enviar una vez por cada canal autenticado.</span><span class="sxs-lookup"><span data-stu-id="b5e77-113">This command can be sent only one time for each authenticated channel.</span></span> <span data-ttu-id="b5e77-114">El número de secuencia de entrada se omite para este comando.</span><span class="sxs-lookup"><span data-stu-id="b5e77-114">The input sequence number is ignored for this command.</span></span>

<span data-ttu-id="b5e77-115">Los siguientes tipos de canal admiten este comando:</span><span class="sxs-lookup"><span data-stu-id="b5e77-115">The following channel types support this command:</span></span>

-   <span data-ttu-id="b5e77-116">**\_Hardware del controlador D3DAUTHENTICATEDCHANNEL \_**</span><span class="sxs-lookup"><span data-stu-id="b5e77-116">**D3DAUTHENTICATEDCHANNEL\_DRIVER\_HARDWARE**</span></span>
-   <span data-ttu-id="b5e77-117">**\_Software de controlador D3DAUTHENTICATEDCHANNEL \_**</span><span class="sxs-lookup"><span data-stu-id="b5e77-117">**D3DAUTHENTICATEDCHANNEL\_DRIVER\_SOFTWARE**</span></span>

## <a name="requirements"></a><span data-ttu-id="b5e77-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b5e77-118">Requirements</span></span>



| <span data-ttu-id="b5e77-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="b5e77-119">Requirement</span></span> | <span data-ttu-id="b5e77-120">Value</span><span class="sxs-lookup"><span data-stu-id="b5e77-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b5e77-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b5e77-121">Minimum supported client</span></span><br/> | <span data-ttu-id="b5e77-122">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="b5e77-122">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="b5e77-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b5e77-123">Minimum supported server</span></span><br/> | <span data-ttu-id="b5e77-124">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="b5e77-124">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="b5e77-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b5e77-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="b5e77-126"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="b5e77-126"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b5e77-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="b5e77-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5e77-128">Content Protection comandos</span><span class="sxs-lookup"><span data-stu-id="b5e77-128">Content Protection Commands</span></span>](content-protection-commands.md)
</dt> <dt>

[<span data-ttu-id="b5e77-129">Content Protection basados en GPU</span><span class="sxs-lookup"><span data-stu-id="b5e77-129">GPU-Based Content Protection</span></span>](gpu-based-content-protection.md)
</dt> <dt>

[<span data-ttu-id="b5e77-130">**IDirect3DAuthenticatedChannel9:: configure**</span><span class="sxs-lookup"><span data-stu-id="b5e77-130">**IDirect3DAuthenticatedChannel9::Configure**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure)
</dt> </dl>

 

 




