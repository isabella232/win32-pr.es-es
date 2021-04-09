---
description: Contiene los datos de entrada para un \_ comando D3DAUTHENTICATEDCONFIGURE Initialize.
ms.assetid: 08677cb3-6f08-49d5-a3b6-c48c88516273
title: D3DAUTHENTICATEDCHANNEL_CONFIGUREINITIALIZE estructura (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_CONFIGUREINITIALIZE
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 072d7886a024b1c28e8c3b7f0609dc8dd3e6add8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080323"
---
# <a name="d3dauthenticatedchannel_configureinitialize-structure"></a><span data-ttu-id="23656-103">D3DAUTHENTICATEDCHANNEL \_ estructura CONFIGUREINITIALIZE</span><span class="sxs-lookup"><span data-stu-id="23656-103">D3DAUTHENTICATEDCHANNEL\_CONFIGUREINITIALIZE structure</span></span>

<span data-ttu-id="23656-104">Contiene los datos de entrada para un comando [**D3DAUTHENTICATEDCONFIGURE \_ Initialize**](d3dauthenticatedconfigure-initialize.md) .</span><span class="sxs-lookup"><span data-stu-id="23656-104">Contains input data for a [**D3DAUTHENTICATEDCONFIGURE\_INITIALIZE**](d3dauthenticatedconfigure-initialize.md) command.</span></span>

<span data-ttu-id="23656-105">Para enviar esta consulta, llame a [**IDirect3DAuthenticatedChannel9:: configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure).</span><span class="sxs-lookup"><span data-stu-id="23656-105">To send this query, call [**IDirect3DAuthenticatedChannel9::Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure).</span></span>

## <a name="syntax"></a><span data-ttu-id="23656-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="23656-106">Syntax</span></span>


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_CONFIGUREINITIALIZE {
  D3DAUTHENTICATEDCHANNEL_CONFIGURE_INPUT Parameters;
  UINT                                    StartSequenceQuery;
  UINT                                    StartSequenceConfigure;
} D3DAUTHENTICATEDCHANNEL_CONFIGUREINITIALIZE;
```



## <a name="members"></a><span data-ttu-id="23656-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="23656-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="23656-108">**Parámetros**</span><span class="sxs-lookup"><span data-stu-id="23656-108">**Parameters**</span></span>
</dt> <dd>

<span data-ttu-id="23656-109">[**D3DAUTHENTICATEDCHANNEL \_ configure \_**](d3dauthenticatedchannel-configure-input.md) la estructura de entrada que contiene el GUID del comando y otros datos.</span><span class="sxs-lookup"><span data-stu-id="23656-109">A [**D3DAUTHENTICATEDCHANNEL\_CONFIGURE\_INPUT**](d3dauthenticatedchannel-configure-input.md) structure that contains the command GUID and other data.</span></span>

</dd> <dt>

<span data-ttu-id="23656-110">**StartSequenceQuery**</span><span class="sxs-lookup"><span data-stu-id="23656-110">**StartSequenceQuery**</span></span>
</dt> <dd>

<span data-ttu-id="23656-111">Número de secuencia inicial para las consultas.</span><span class="sxs-lookup"><span data-stu-id="23656-111">The initial sequence number for queries.</span></span>

</dd> <dt>

<span data-ttu-id="23656-112">**StartSequenceConfigure**</span><span class="sxs-lookup"><span data-stu-id="23656-112">**StartSequenceConfigure**</span></span>
</dt> <dd>

<span data-ttu-id="23656-113">El número de secuencia inicial para los comandos.</span><span class="sxs-lookup"><span data-stu-id="23656-113">The initial sequence number for commands.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="23656-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="23656-114">Remarks</span></span>

<span data-ttu-id="23656-115">Cada uno de los miembros **StartSequenceQuery** y **StartSequenceConfigure** contiene un número aleatorio de 32 bits criptográficamente seguro.</span><span class="sxs-lookup"><span data-stu-id="23656-115">The **StartSequenceQuery** and **StartSequenceConfigure** members each contain a cryptographically secure 32-bit random number.</span></span>

## <a name="requirements"></a><span data-ttu-id="23656-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="23656-116">Requirements</span></span>



| <span data-ttu-id="23656-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="23656-117">Requirement</span></span> | <span data-ttu-id="23656-118">Value</span><span class="sxs-lookup"><span data-stu-id="23656-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="23656-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="23656-119">Minimum supported client</span></span><br/> | <span data-ttu-id="23656-120">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="23656-120">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="23656-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="23656-121">Minimum supported server</span></span><br/> | <span data-ttu-id="23656-122">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="23656-122">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="23656-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="23656-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="23656-124"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="23656-124"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="23656-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="23656-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23656-126">Estructuras de vídeo de Direct3D</span><span class="sxs-lookup"><span data-stu-id="23656-126">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> <dt>

[<span data-ttu-id="23656-127">**IDirect3DAuthenticatedChannel9:: configure**</span><span class="sxs-lookup"><span data-stu-id="23656-127">**IDirect3DAuthenticatedChannel9::Configure**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure)
</dt> </dl>

 

 




