---
description: Establece el nivel de cifrado que se realiza antes de que el contenido protegido sea accesible para la CPU o el bus.
ms.assetid: 6de6c4a3-705a-4420-b9f4-8d4d442b23bf
title: D3DAUTHENTICATEDCONFIGURE_ENCRYPTIONWHENACCESSIBLE (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCONFIGURE_ENCRYPTIONWHENACCESSIBLE
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 8b624c26c81549372e0e09b4a08ce73f6cd3dd27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539597"
---
# <a name="d3dauthenticatedconfigure_encryptionwhenaccessible"></a><span data-ttu-id="25edf-103">D3DAUTHENTICATEDCONFIGURE \_ ENCRYPTIONWHENACCESSIBLE</span><span class="sxs-lookup"><span data-stu-id="25edf-103">D3DAUTHENTICATEDCONFIGURE\_ENCRYPTIONWHENACCESSIBLE</span></span>

<span data-ttu-id="25edf-104">Establece el nivel de cifrado que se realiza antes de que el contenido protegido sea accesible para la CPU o el bus.</span><span class="sxs-lookup"><span data-stu-id="25edf-104">Sets the level of encryption that is performed before protected content becomes accessible to the CPU or bus.</span></span>



| <span data-ttu-id="25edf-105">Requisito</span><span class="sxs-lookup"><span data-stu-id="25edf-105">Requirement</span></span> | <span data-ttu-id="25edf-106">Value</span><span class="sxs-lookup"><span data-stu-id="25edf-106">Value</span></span> |
|--------------|-----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="25edf-107">GUID de comando</span><span class="sxs-lookup"><span data-stu-id="25edf-107">Command GUID</span></span> | <span data-ttu-id="25edf-108">**D3DAUTHENTICATEDCONFIGURE \_ ENCRYPTIONWHENACCESSIBLE**</span><span class="sxs-lookup"><span data-stu-id="25edf-108">**D3DAUTHENTICATEDCONFIGURE\_ENCRYPTIONWHENACCESSIBLE**</span></span>                                                                     |
| <span data-ttu-id="25edf-109">Datos de entrada</span><span class="sxs-lookup"><span data-stu-id="25edf-109">Input data</span></span>   | [<span data-ttu-id="25edf-110">**D3DAUTHENTICATEDCHANNEL \_ CONFIGUREUNCOMPRESSEDENCRYPTION**</span><span class="sxs-lookup"><span data-stu-id="25edf-110">**D3DAUTHENTICATEDCHANNEL\_CONFIGUREUNCOMPRESSEDENCRYPTION**</span></span>](d3dauthenticatedchannel-configureuncompressedencryption.md) |



 

## <a name="remarks"></a><span data-ttu-id="25edf-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="25edf-111">Remarks</span></span>

<span data-ttu-id="25edf-112">Los siguientes tipos de canal admiten esta consulta:</span><span class="sxs-lookup"><span data-stu-id="25edf-112">The following channel types support this query:</span></span>

-   <span data-ttu-id="25edf-113">**\_Hardware del controlador D3DAUTHENTICATEDCHANNEL \_**</span><span class="sxs-lookup"><span data-stu-id="25edf-113">**D3DAUTHENTICATEDCHANNEL\_DRIVER\_HARDWARE**</span></span>
-   <span data-ttu-id="25edf-114">**\_Software de controlador D3DAUTHENTICATEDCHANNEL \_**</span><span class="sxs-lookup"><span data-stu-id="25edf-114">**D3DAUTHENTICATEDCHANNEL\_DRIVER\_SOFTWARE**</span></span>

## <a name="requirements"></a><span data-ttu-id="25edf-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="25edf-115">Requirements</span></span>



| <span data-ttu-id="25edf-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="25edf-116">Requirement</span></span> | <span data-ttu-id="25edf-117">Value</span><span class="sxs-lookup"><span data-stu-id="25edf-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="25edf-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="25edf-118">Minimum supported client</span></span><br/> | <span data-ttu-id="25edf-119">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="25edf-119">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="25edf-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="25edf-120">Minimum supported server</span></span><br/> | <span data-ttu-id="25edf-121">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="25edf-121">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="25edf-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="25edf-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="25edf-123"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="25edf-123"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="25edf-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="25edf-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25edf-125">Content Protection comandos</span><span class="sxs-lookup"><span data-stu-id="25edf-125">Content Protection Commands</span></span>](content-protection-commands.md)
</dt> <dt>

[<span data-ttu-id="25edf-126">Content Protection basados en GPU</span><span class="sxs-lookup"><span data-stu-id="25edf-126">GPU-Based Content Protection</span></span>](gpu-based-content-protection.md)
</dt> <dt>

[<span data-ttu-id="25edf-127">**IDirect3DAuthenticatedChannel9:: configure**</span><span class="sxs-lookup"><span data-stu-id="25edf-127">**IDirect3DAuthenticatedChannel9::Configure**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure)
</dt> </dl>

 

 




