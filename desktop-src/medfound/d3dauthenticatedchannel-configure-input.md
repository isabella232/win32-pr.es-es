---
description: 'Contiene datos de entrada para el método IDirect3DAuthenticatedChannel9:: configure.'
ms.assetid: 7646100e-f768-4935-9e71-1d9db0d69c52
title: D3DAUTHENTICATEDCHANNEL_CONFIGURE_INPUT estructura (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_CONFIGURE_INPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 82cd60dbb65517beb65a3a7cb413e1d93ac72062
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275134"
---
# <a name="d3dauthenticatedchannel_configure_input-structure"></a><span data-ttu-id="41e2f-103">D3DAUTHENTICATEDCHANNEL \_ configurar la \_ estructura de entrada</span><span class="sxs-lookup"><span data-stu-id="41e2f-103">D3DAUTHENTICATEDCHANNEL\_CONFIGURE\_INPUT structure</span></span>

<span data-ttu-id="41e2f-104">Contiene datos de entrada para el método [**IDirect3DAuthenticatedChannel9:: configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure) .</span><span class="sxs-lookup"><span data-stu-id="41e2f-104">Contains input data for the [**IDirect3DAuthenticatedChannel9::Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="41e2f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="41e2f-105">Syntax</span></span>


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_CONFIGURE_INPUT {
  D3D_OMAC omac;
  GUID     ConfigureType;
  HANDLE   hChannel;
  UINT     SequenceNumber;
} D3DAUTHENTICATEDCHANNEL_CONFIGURE_INPUT;
```



## <a name="members"></a><span data-ttu-id="41e2f-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="41e2f-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="41e2f-107">**omac**</span><span class="sxs-lookup"><span data-stu-id="41e2f-107">**omac**</span></span>
</dt> <dd>

<span data-ttu-id="41e2f-108">Una estructura [**D3D \_ OMAC**](d3d-omac.md) que contiene un código de autentificación de mensajes (Mac) (Mac) de los datos.</span><span class="sxs-lookup"><span data-stu-id="41e2f-108">A [**D3D\_OMAC**](d3d-omac.md) structure that contains a Message Authentication Code (MAC) of the data.</span></span> <span data-ttu-id="41e2f-109">El controlador utiliza una clave CBC MAC (OMAC) basada en AES para calcular este valor para el bloque de datos que aparece después de este miembro de estructura.</span><span class="sxs-lookup"><span data-stu-id="41e2f-109">The driver uses AES-based one-key CBC MAC (OMAC) to calculate this value for the block of data that appears after this structure member.</span></span>

</dd> <dt>

<span data-ttu-id="41e2f-110">**ConfigureType**</span><span class="sxs-lookup"><span data-stu-id="41e2f-110">**ConfigureType**</span></span>
</dt> <dd>

<span data-ttu-id="41e2f-111">GUID que especifica el comando.</span><span class="sxs-lookup"><span data-stu-id="41e2f-111">A GUID that specifies the command.</span></span> <span data-ttu-id="41e2f-112">Para obtener una lista de valores, vea [comandos Content Protection](content-protection-commands.md).</span><span class="sxs-lookup"><span data-stu-id="41e2f-112">For a list of values, see [Content Protection Commands](content-protection-commands.md).</span></span>

</dd> <dt>

<span data-ttu-id="41e2f-113">**hChannel**</span><span class="sxs-lookup"><span data-stu-id="41e2f-113">**hChannel**</span></span>
</dt> <dd>

<span data-ttu-id="41e2f-114">Identificador del canal autenticado.</span><span class="sxs-lookup"><span data-stu-id="41e2f-114">A handle to the authenticated channel.</span></span> <span data-ttu-id="41e2f-115">Para obtener el identificador, llame a [**IDirect3DDevice9Video:: CreateAuthenticatedChannel**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9video-createauthenticatedchannel).</span><span class="sxs-lookup"><span data-stu-id="41e2f-115">To get the handle, call [**IDirect3DDevice9Video::CreateAuthenticatedChannel**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9video-createauthenticatedchannel).</span></span>

</dd> <dt>

<span data-ttu-id="41e2f-116">**SequenceNumber**</span><span class="sxs-lookup"><span data-stu-id="41e2f-116">**SequenceNumber**</span></span>
</dt> <dd>

<span data-ttu-id="41e2f-117">El número de secuencia de la consulta.</span><span class="sxs-lookup"><span data-stu-id="41e2f-117">The query sequence number.</span></span> <span data-ttu-id="41e2f-118">Al inicio de la sesión, genere un número aleatorio de 32 bits criptográficamente seguro para usarlo como el número de secuencia inicial.</span><span class="sxs-lookup"><span data-stu-id="41e2f-118">At the start of the session, generate a cryptographically secure 32-bit random number to use as the starting sequence number.</span></span> <span data-ttu-id="41e2f-119">Para cada comando, incremente el número de secuencia en 1.</span><span class="sxs-lookup"><span data-stu-id="41e2f-119">For each command, increment the sequence number by 1.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="41e2f-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="41e2f-120">Requirements</span></span>



| <span data-ttu-id="41e2f-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="41e2f-121">Requirement</span></span> | <span data-ttu-id="41e2f-122">Value</span><span class="sxs-lookup"><span data-stu-id="41e2f-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="41e2f-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="41e2f-123">Minimum supported client</span></span><br/> | <span data-ttu-id="41e2f-124">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="41e2f-124">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="41e2f-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="41e2f-125">Minimum supported server</span></span><br/> | <span data-ttu-id="41e2f-126">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="41e2f-126">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="41e2f-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="41e2f-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="41e2f-128"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="41e2f-128"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="41e2f-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="41e2f-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41e2f-130">Estructuras de vídeo de Direct3D</span><span class="sxs-lookup"><span data-stu-id="41e2f-130">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> <dt>

[<span data-ttu-id="41e2f-131">**IDirect3DAuthenticatedChannel9:: configure**</span><span class="sxs-lookup"><span data-stu-id="41e2f-131">**IDirect3DAuthenticatedChannel9::Configure**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure)
</dt> </dl>

 

 




