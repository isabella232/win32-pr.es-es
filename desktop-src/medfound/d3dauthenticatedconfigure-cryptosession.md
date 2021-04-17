---
description: Asocia una sesión criptográfica a un dispositivo descodificador DirectX video Acceleration 2 (DXVA-2) y un dispositivo Direct3D.
ms.assetid: d40fead7-8a86-426e-933e-13df21cdf50b
title: D3DAUTHENTICATEDCONFIGURE_CRYPTOSESSION (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCONFIGURE_CRYPTOSESSION
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 4b6fda19aef9629214aaa410fd43c4d64f16dd29
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659781"
---
# <a name="d3dauthenticatedconfigure_cryptosession"></a><span data-ttu-id="709cf-103">D3DAUTHENTICATEDCONFIGURE \_ CRYPTOSESSION</span><span class="sxs-lookup"><span data-stu-id="709cf-103">D3DAUTHENTICATEDCONFIGURE\_CRYPTOSESSION</span></span>

<span data-ttu-id="709cf-104">Asocia una sesión criptográfica a un dispositivo descodificador DirectX video Acceleration 2 (DXVA-2) y un dispositivo Direct3D.</span><span class="sxs-lookup"><span data-stu-id="709cf-104">Associates a cryptographic session with a DirectX Video Acceleration 2 (DXVA-2) decoder device and a Direct3D device.</span></span>



| <span data-ttu-id="709cf-105">Requisito</span><span class="sxs-lookup"><span data-stu-id="709cf-105">Requirement</span></span> | <span data-ttu-id="709cf-106">Value</span><span class="sxs-lookup"><span data-stu-id="709cf-106">Value</span></span> |
|--------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="709cf-107">GUID de comando</span><span class="sxs-lookup"><span data-stu-id="709cf-107">Command GUID</span></span> | <span data-ttu-id="709cf-108">**D3DAUTHENTICATEDCONFIGURE \_ CRYPTOSESSION**</span><span class="sxs-lookup"><span data-stu-id="709cf-108">**D3DAUTHENTICATEDCONFIGURE\_CRYPTOSESSION**</span></span>                                                              |
| <span data-ttu-id="709cf-109">Datos de entrada</span><span class="sxs-lookup"><span data-stu-id="709cf-109">Input data</span></span>   | [<span data-ttu-id="709cf-110">**D3DAUTHENTICATEDCHANNEL \_ CONFIGURECRYPTOSESSION**</span><span class="sxs-lookup"><span data-stu-id="709cf-110">**D3DAUTHENTICATEDCHANNEL\_CONFIGURECRYPTOSESSION**</span></span>](d3dauthenticatedchannel-configurecryptosession.md) |



 

## <a name="remarks"></a><span data-ttu-id="709cf-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="709cf-111">Remarks</span></span>

<span data-ttu-id="709cf-112">Después de enviar este comando, puede enviar la consulta [D3DAUTHENTICATEDQUERY \_ OUTPUTID](d3dauthenticatedquery-outputid.md) para averiguar qué salidas de vídeo están asociadas a la sesión criptográfica.</span><span class="sxs-lookup"><span data-stu-id="709cf-112">After this command is sent, you can send the [D3DAUTHENTICATEDQUERY\_OUTPUTID](d3dauthenticatedquery-outputid.md) query to find out which video outputs are associated with the cryptographic session.</span></span>

<span data-ttu-id="709cf-113">Los siguientes tipos de canal admiten este comando:</span><span class="sxs-lookup"><span data-stu-id="709cf-113">The following channel types support this command:</span></span>

-   <span data-ttu-id="709cf-114">**D3DAUTHENTICATEDCHANNEL \_ D3D9**</span><span class="sxs-lookup"><span data-stu-id="709cf-114">**D3DAUTHENTICATEDCHANNEL\_D3D9**</span></span>
-   <span data-ttu-id="709cf-115">**\_Software de controlador D3DAUTHENTICATEDCHANNEL \_**</span><span class="sxs-lookup"><span data-stu-id="709cf-115">**D3DAUTHENTICATEDCHANNEL\_DRIVER\_SOFTWARE**</span></span>

## <a name="requirements"></a><span data-ttu-id="709cf-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="709cf-116">Requirements</span></span>



| <span data-ttu-id="709cf-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="709cf-117">Requirement</span></span> | <span data-ttu-id="709cf-118">Value</span><span class="sxs-lookup"><span data-stu-id="709cf-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="709cf-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="709cf-119">Minimum supported client</span></span><br/> | <span data-ttu-id="709cf-120">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="709cf-120">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="709cf-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="709cf-121">Minimum supported server</span></span><br/> | <span data-ttu-id="709cf-122">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="709cf-122">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="709cf-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="709cf-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="709cf-124"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="709cf-124"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="709cf-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="709cf-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="709cf-126">Content Protection comandos</span><span class="sxs-lookup"><span data-stu-id="709cf-126">Content Protection Commands</span></span>](content-protection-commands.md)
</dt> <dt>

[<span data-ttu-id="709cf-127">Content Protection basados en GPU</span><span class="sxs-lookup"><span data-stu-id="709cf-127">GPU-Based Content Protection</span></span>](gpu-based-content-protection.md)
</dt> <dt>

[<span data-ttu-id="709cf-128">**IDirect3DAuthenticatedChannel9:: configure**</span><span class="sxs-lookup"><span data-stu-id="709cf-128">**IDirect3DAuthenticatedChannel9::Configure**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure)
</dt> </dl>

 

 




