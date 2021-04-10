---
description: Habilita un proceso para abrir un recurso compartido o deshabilita un proceso para abrir recursos compartidos.
ms.assetid: 5fa2b88f-e946-436c-953e-04e0e338146c
title: D3DAUTHENTICATEDCONFIGURE_SHAREDRESOURCE (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCONFIGURE_SHAREDRESOURCE
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 7404a4bed3ac3b1d4002bb03c45d7732500b77e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275128"
---
# <a name="d3dauthenticatedconfigure_sharedresource"></a><span data-ttu-id="a7c9a-103">D3DAUTHENTICATEDCONFIGURE \_ SHAREDRESOURCE</span><span class="sxs-lookup"><span data-stu-id="a7c9a-103">D3DAUTHENTICATEDCONFIGURE\_SHAREDRESOURCE</span></span>

<span data-ttu-id="a7c9a-104">Habilita un proceso para abrir un recurso compartido o deshabilita un proceso para abrir recursos compartidos.</span><span class="sxs-lookup"><span data-stu-id="a7c9a-104">Enables a process to open a shared resource, or disables a process from opening shared resources.</span></span>



| <span data-ttu-id="a7c9a-105">Requisito</span><span class="sxs-lookup"><span data-stu-id="a7c9a-105">Requirement</span></span> | <span data-ttu-id="a7c9a-106">Value</span><span class="sxs-lookup"><span data-stu-id="a7c9a-106">Value</span></span> |
|--------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a7c9a-107">GUID de comando</span><span class="sxs-lookup"><span data-stu-id="a7c9a-107">Command GUID</span></span> | <span data-ttu-id="a7c9a-108">**D3DAUTHENTICATEDCONFIGURE \_ SHAREDRESOURCE**</span><span class="sxs-lookup"><span data-stu-id="a7c9a-108">**D3DAUTHENTICATEDCONFIGURE\_SHAREDRESOURCE**</span></span>                                                               |
| <span data-ttu-id="a7c9a-109">Datos de entrada</span><span class="sxs-lookup"><span data-stu-id="a7c9a-109">Input data</span></span>   | [<span data-ttu-id="a7c9a-110">**D3DAUTHENTICATEDCHANNEL \_ CONFIGURESHAREDRESOURCE**</span><span class="sxs-lookup"><span data-stu-id="a7c9a-110">**D3DAUTHENTICATEDCHANNEL\_CONFIGURESHAREDRESOURCE**</span></span>](d3dauthenticatedchannel-configuresharedresource.md) |



 

## <a name="remarks"></a><span data-ttu-id="a7c9a-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a7c9a-111">Remarks</span></span>

<span data-ttu-id="a7c9a-112">Los siguientes tipos de canal admiten esta consulta:</span><span class="sxs-lookup"><span data-stu-id="a7c9a-112">The following channel types support this query:</span></span>

-   <span data-ttu-id="a7c9a-113">**\_D3D9 del controlador D3DAUTHENTICATEDCHANNEL \_**</span><span class="sxs-lookup"><span data-stu-id="a7c9a-113">**D3DAUTHENTICATEDCHANNEL\_DRIVER\_D3D9**</span></span>
-   <span data-ttu-id="a7c9a-114">**\_Software de controlador D3DAUTHENTICATEDCHANNEL \_**</span><span class="sxs-lookup"><span data-stu-id="a7c9a-114">**D3DAUTHENTICATEDCHANNEL\_DRIVER\_SOFTWARE**</span></span>

## <a name="requirements"></a><span data-ttu-id="a7c9a-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a7c9a-115">Requirements</span></span>



| <span data-ttu-id="a7c9a-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="a7c9a-116">Requirement</span></span> | <span data-ttu-id="a7c9a-117">Value</span><span class="sxs-lookup"><span data-stu-id="a7c9a-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a7c9a-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a7c9a-118">Minimum supported client</span></span><br/> | <span data-ttu-id="a7c9a-119">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="a7c9a-119">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="a7c9a-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a7c9a-120">Minimum supported server</span></span><br/> | <span data-ttu-id="a7c9a-121">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="a7c9a-121">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="a7c9a-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a7c9a-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="a7c9a-123"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="a7c9a-123"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a7c9a-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="a7c9a-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7c9a-125">Content Protection comandos</span><span class="sxs-lookup"><span data-stu-id="a7c9a-125">Content Protection Commands</span></span>](content-protection-commands.md)
</dt> <dt>

[<span data-ttu-id="a7c9a-126">Content Protection basados en GPU</span><span class="sxs-lookup"><span data-stu-id="a7c9a-126">GPU-Based Content Protection</span></span>](gpu-based-content-protection.md)
</dt> <dt>

[<span data-ttu-id="a7c9a-127">**IDirect3DAuthenticatedChannel9:: configure**</span><span class="sxs-lookup"><span data-stu-id="a7c9a-127">**IDirect3DAuthenticatedChannel9::Configure**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure)
</dt> </dl>

 

 




