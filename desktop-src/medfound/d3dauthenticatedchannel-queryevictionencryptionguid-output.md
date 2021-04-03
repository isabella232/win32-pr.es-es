---
description: Contiene la respuesta a una consulta de D3DAUTHENTICATEDQUERY \_ ENCRYPTIONWHENACCESSIBLEGUID.
ms.assetid: afe73f8e-3304-470c-a37a-17b6c767b2c0
title: D3DAUTHENTICATEDCHANNEL_QUERYEVICTIONENCRYPTIONGUID_OUTPUT estructura (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_QUERYEVICTIONENCRYPTIONGUID_OUTPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 8fa46095c5075b0a36ed691978b73de1e7b8cade
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907568"
---
# <a name="d3dauthenticatedchannel_queryevictionencryptionguid_output-structure"></a><span data-ttu-id="32e5f-103">Estructura de salida de D3DAUTHENTICATEDCHANNEL \_ QUERYEVICTIONENCRYPTIONGUID \_</span><span class="sxs-lookup"><span data-stu-id="32e5f-103">D3DAUTHENTICATEDCHANNEL\_QUERYEVICTIONENCRYPTIONGUID\_OUTPUT structure</span></span>

<span data-ttu-id="32e5f-104">Contiene la respuesta a una consulta de [**D3DAUTHENTICATEDQUERY \_ ENCRYPTIONWHENACCESSIBLEGUID**](d3dauthenticatedquery-encryptionwhenaccessibleguid.md) .</span><span class="sxs-lookup"><span data-stu-id="32e5f-104">Contains the response to a [**D3DAUTHENTICATEDQUERY\_ENCRYPTIONWHENACCESSIBLEGUID**](d3dauthenticatedquery-encryptionwhenaccessibleguid.md) query.</span></span>

<span data-ttu-id="32e5f-105">Para enviar esta consulta, llame a [**IDirect3DAuthenticatedChannel9:: query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span><span class="sxs-lookup"><span data-stu-id="32e5f-105">To send this query, call [**IDirect3DAuthenticatedChannel9::Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span></span>

## <a name="syntax"></a><span data-ttu-id="32e5f-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="32e5f-106">Syntax</span></span>


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_QUERYEVICTIONENCRYPTIONGUID_OUTPUT {
  Output D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT;
  UINT   EncryptionGuidIndex;
  GUID   EncryptionGuid;
} D3DAUTHENTICATEDCHANNEL_QUERYEVICTIONENCRYPTIONGUID_OUTPUT;
```



## <a name="members"></a><span data-ttu-id="32e5f-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="32e5f-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="32e5f-108">**Resultado de la \_ consulta D3DAUTHENTICATEDCHANNEL \_**</span><span class="sxs-lookup"><span data-stu-id="32e5f-108">**D3DAUTHENTICATEDCHANNEL\_QUERY\_OUTPUT**</span></span>
</dt> <dd>

<span data-ttu-id="32e5f-109">Una estructura de [**\_ \_ salida de consulta de D3DAUTHENTICATEDCHANNEL**](d3dauthenticatedchannel-query-output.md) que contiene un código de autentificación de mensajes (Mac) (Mac) y otros datos.</span><span class="sxs-lookup"><span data-stu-id="32e5f-109">A [**D3DAUTHENTICATEDCHANNEL\_QUERY\_OUTPUT**](d3dauthenticatedchannel-query-output.md) structure that contains a Message Authentication Code (MAC) and other data.</span></span>

</dd> <dt>

<span data-ttu-id="32e5f-110">**EncryptionGuidIndex**</span><span class="sxs-lookup"><span data-stu-id="32e5f-110">**EncryptionGuidIndex**</span></span>
</dt> <dd>

<span data-ttu-id="32e5f-111">Índice del GUID de cifrado.</span><span class="sxs-lookup"><span data-stu-id="32e5f-111">The index of the encryption GUID.</span></span>

</dd> <dt>

<span data-ttu-id="32e5f-112">**EncryptionGuid**</span><span class="sxs-lookup"><span data-stu-id="32e5f-112">**EncryptionGuid**</span></span>
</dt> <dd>

<span data-ttu-id="32e5f-113">GUID que especifica un tipo de cifrado admitido.</span><span class="sxs-lookup"><span data-stu-id="32e5f-113">A GUID that specifies a supported encryption type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="32e5f-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="32e5f-114">Requirements</span></span>



| <span data-ttu-id="32e5f-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="32e5f-115">Requirement</span></span> | <span data-ttu-id="32e5f-116">Value</span><span class="sxs-lookup"><span data-stu-id="32e5f-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="32e5f-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="32e5f-117">Minimum supported client</span></span><br/> | <span data-ttu-id="32e5f-118">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="32e5f-118">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="32e5f-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="32e5f-119">Minimum supported server</span></span><br/> | <span data-ttu-id="32e5f-120">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="32e5f-120">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="32e5f-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="32e5f-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="32e5f-122"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="32e5f-122"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="32e5f-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="32e5f-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32e5f-124">Estructuras de vídeo de Direct3D</span><span class="sxs-lookup"><span data-stu-id="32e5f-124">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> <dt>

[<span data-ttu-id="32e5f-125">**IDirect3DAuthenticatedChannel9:: Query**</span><span class="sxs-lookup"><span data-stu-id="32e5f-125">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




