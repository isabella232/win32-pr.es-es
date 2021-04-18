---
description: Contiene datos de entrada para el \_ comando D3DAUTHENTICATEDCONFIGURE ENCRYPTIONWHENACCESSIBLE.
ms.assetid: d2d0adff-5d4d-4af3-b6b8-b8c60a506142
title: D3DAUTHENTICATEDCHANNEL_CONFIGUREUNCOMPRESSEDENCRYPTION estructura (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_CONFIGUREUNCOMPRESSEDENCRYPTION
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 6c8ea4360ff7f2bbcf2c03040671013473e9873a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696157"
---
# <a name="d3dauthenticatedchannel_configureuncompressedencryption-structure"></a><span data-ttu-id="4bb3c-103">D3DAUTHENTICATEDCHANNEL \_ estructura CONFIGUREUNCOMPRESSEDENCRYPTION</span><span class="sxs-lookup"><span data-stu-id="4bb3c-103">D3DAUTHENTICATEDCHANNEL\_CONFIGUREUNCOMPRESSEDENCRYPTION structure</span></span>

<span data-ttu-id="4bb3c-104">Contiene datos de entrada para el comando [**D3DAUTHENTICATEDCONFIGURE \_ ENCRYPTIONWHENACCESSIBLE**](d3dauthenticatedconfigure-encryptionwhenaccessible.md) .</span><span class="sxs-lookup"><span data-stu-id="4bb3c-104">Contains input data for the [**D3DAUTHENTICATEDCONFIGURE\_ENCRYPTIONWHENACCESSIBLE**](d3dauthenticatedconfigure-encryptionwhenaccessible.md) command.</span></span>

<span data-ttu-id="4bb3c-105">Para enviar esta consulta, llame a [**IDirect3DAuthenticatedChannel9:: configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure).</span><span class="sxs-lookup"><span data-stu-id="4bb3c-105">To send this query, call [**IDirect3DAuthenticatedChannel9::Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure).</span></span>

## <a name="syntax"></a><span data-ttu-id="4bb3c-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4bb3c-106">Syntax</span></span>


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_CONFIGUREUNCOMPRESSEDENCRYPTION {
  D3DAUTHENTICATEDCHANNEL_CONFIGURE_INPUT Parameters;
  GUID                                    EncryptionGuid;
} D3DAUTHENTICATEDCHANNEL_CONFIGUREUNCOMPRESSEDENCRYPTION;
```



## <a name="members"></a><span data-ttu-id="4bb3c-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="4bb3c-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="4bb3c-108">**Parámetros**</span><span class="sxs-lookup"><span data-stu-id="4bb3c-108">**Parameters**</span></span>
</dt> <dd>

<span data-ttu-id="4bb3c-109">[**D3DAUTHENTICATEDCHANNEL \_ configure \_**](d3dauthenticatedchannel-configure-input.md) la estructura de entrada que contiene el GUID del comando y otros datos.</span><span class="sxs-lookup"><span data-stu-id="4bb3c-109">A [**D3DAUTHENTICATEDCHANNEL\_CONFIGURE\_INPUT**](d3dauthenticatedchannel-configure-input.md) structure that contains the command GUID and other data.</span></span>

</dd> <dt>

<span data-ttu-id="4bb3c-110">**EncryptionGuid**</span><span class="sxs-lookup"><span data-stu-id="4bb3c-110">**EncryptionGuid**</span></span>
</dt> <dd>

<span data-ttu-id="4bb3c-111">GUID que especifica el tipo de cifrado que se va a aplicar.</span><span class="sxs-lookup"><span data-stu-id="4bb3c-111">A GUID that specifies the type of encryption to apply.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4bb3c-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4bb3c-112">Requirements</span></span>



| <span data-ttu-id="4bb3c-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="4bb3c-113">Requirement</span></span> | <span data-ttu-id="4bb3c-114">Value</span><span class="sxs-lookup"><span data-stu-id="4bb3c-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4bb3c-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4bb3c-115">Minimum supported client</span></span><br/> | <span data-ttu-id="4bb3c-116">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="4bb3c-116">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="4bb3c-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4bb3c-117">Minimum supported server</span></span><br/> | <span data-ttu-id="4bb3c-118">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="4bb3c-118">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="4bb3c-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4bb3c-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="4bb3c-120"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="4bb3c-120"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4bb3c-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="4bb3c-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4bb3c-122">Estructuras de vídeo de Direct3D</span><span class="sxs-lookup"><span data-stu-id="4bb3c-122">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> <dt>

[<span data-ttu-id="4bb3c-123">**IDirect3DAuthenticatedChannel9:: configure**</span><span class="sxs-lookup"><span data-stu-id="4bb3c-123">**IDirect3DAuthenticatedChannel9::Configure**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure)
</dt> </dl>

 

 




