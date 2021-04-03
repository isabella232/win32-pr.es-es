---
description: Contiene datos de entrada para un \_ comando de protección de D3DAUTHENTICATEDCONFIGURE.
ms.assetid: 44f37e78-7218-42be-a07a-5ab911f2ba21
title: D3DAUTHENTICATEDCHANNEL_CONFIGUREPROTECTION estructura (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_CONFIGUREPROTECTION
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: b3fc1daee7bfd9320539a03974ab431c4ba588d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907570"
---
# <a name="d3dauthenticatedchannel_configureprotection-structure"></a><span data-ttu-id="31641-103">D3DAUTHENTICATEDCHANNEL \_ estructura CONFIGUREPROTECTION</span><span class="sxs-lookup"><span data-stu-id="31641-103">D3DAUTHENTICATEDCHANNEL\_CONFIGUREPROTECTION structure</span></span>

<span data-ttu-id="31641-104">Contiene datos de entrada para un comando de [**\_ protección de D3DAUTHENTICATEDCONFIGURE**](d3dauthenticatedconfigure-protection.md) .</span><span class="sxs-lookup"><span data-stu-id="31641-104">Contains input data for a [**D3DAUTHENTICATEDCONFIGURE\_PROTECTION**](d3dauthenticatedconfigure-protection.md) command.</span></span>

<span data-ttu-id="31641-105">Para enviar esta consulta, llame a [**IDirect3DAuthenticatedChannel9:: configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure).</span><span class="sxs-lookup"><span data-stu-id="31641-105">To send this query, call [**IDirect3DAuthenticatedChannel9::Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure).</span></span>

## <a name="syntax"></a><span data-ttu-id="31641-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="31641-106">Syntax</span></span>


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_CONFIGUREPROTECTION {
  D3DAUTHENTICATEDCHANNEL_CONFIGURE_INPUT  Parameters;
  D3DAUTHENTICATEDCHANNEL_PROTECTION_FLAGS Protections;
} D3DAUTHENTICATEDCHANNEL_CONFIGUREPROTECTION;
```



## <a name="members"></a><span data-ttu-id="31641-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="31641-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="31641-108">**Parámetros**</span><span class="sxs-lookup"><span data-stu-id="31641-108">**Parameters**</span></span>
</dt> <dd>

<span data-ttu-id="31641-109">[**D3DAUTHENTICATEDCHANNEL \_ configure \_**](d3dauthenticatedchannel-configure-input.md) la estructura de entrada que contiene el GUID del comando y otros datos.</span><span class="sxs-lookup"><span data-stu-id="31641-109">A [**D3DAUTHENTICATEDCHANNEL\_CONFIGURE\_INPUT**](d3dauthenticatedchannel-configure-input.md) structure that contains the command GUID and other data.</span></span>

</dd> <dt>

<span data-ttu-id="31641-110">**Protecciones**</span><span class="sxs-lookup"><span data-stu-id="31641-110">**Protections**</span></span>
</dt> <dd>

<span data-ttu-id="31641-111">Una estructura de [**\_ \_ marcas de protección de D3DAUTHENTICATEDCHANNEL**](d3dauthenticatedchannel-protection-flags.md) que especifica el nivel de protección.</span><span class="sxs-lookup"><span data-stu-id="31641-111">A [**D3DAUTHENTICATEDCHANNEL\_PROTECTION\_FLAGS**](d3dauthenticatedchannel-protection-flags.md) structure that specifies the protection level.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="31641-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="31641-112">Requirements</span></span>



| <span data-ttu-id="31641-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="31641-113">Requirement</span></span> | <span data-ttu-id="31641-114">Value</span><span class="sxs-lookup"><span data-stu-id="31641-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="31641-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="31641-115">Minimum supported client</span></span><br/> | <span data-ttu-id="31641-116">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="31641-116">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="31641-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="31641-117">Minimum supported server</span></span><br/> | <span data-ttu-id="31641-118">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="31641-118">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="31641-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="31641-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="31641-120"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="31641-120"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="31641-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="31641-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31641-122">Estructuras de vídeo de Direct3D</span><span class="sxs-lookup"><span data-stu-id="31641-122">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> <dt>

[<span data-ttu-id="31641-123">**IDirect3DAuthenticatedChannel9:: configure**</span><span class="sxs-lookup"><span data-stu-id="31641-123">**IDirect3DAuthenticatedChannel9::Configure**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure)
</dt> </dl>

 

 




