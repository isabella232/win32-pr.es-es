---
description: Contiene datos de entrada para un \_ comando D3DAUTHENTICATEDCONFIGURE CRYPTOSESSION.
ms.assetid: eed5591d-20b0-495c-8c05-b9cb3b91deab
title: D3DAUTHENTICATEDCHANNEL_CONFIGURECRYPTOSESSION estructura (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_CONFIGURECRYPTOSESSION
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 2b1cca13bcd37e488cd0ed455098afa62492579f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696161"
---
# <a name="d3dauthenticatedchannel_configurecryptosession-structure"></a><span data-ttu-id="66723-103">D3DAUTHENTICATEDCHANNEL \_ estructura CONFIGURECRYPTOSESSION</span><span class="sxs-lookup"><span data-stu-id="66723-103">D3DAUTHENTICATEDCHANNEL\_CONFIGURECRYPTOSESSION structure</span></span>

<span data-ttu-id="66723-104">Contiene datos de entrada para un comando [**D3DAUTHENTICATEDCONFIGURE \_ CRYPTOSESSION**](d3dauthenticatedconfigure-cryptosession.md) .</span><span class="sxs-lookup"><span data-stu-id="66723-104">Contains input data for a [**D3DAUTHENTICATEDCONFIGURE\_CRYPTOSESSION**](d3dauthenticatedconfigure-cryptosession.md) command.</span></span>

<span data-ttu-id="66723-105">Para enviar esta consulta, llame a [**IDirect3DAuthenticatedChannel9:: configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure).</span><span class="sxs-lookup"><span data-stu-id="66723-105">To send this query, call [**IDirect3DAuthenticatedChannel9::Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure).</span></span>

## <a name="syntax"></a><span data-ttu-id="66723-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="66723-106">Syntax</span></span>


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_CONFIGURECRYPTOSESSION {
  D3DAUTHENTICATEDCHANNEL_CONFIGURE_INPUT Parameters;
  HANDLE                                  DXVA2DecodeHandle;
  HANDLE                                  CryptoSessionHandle;
  HANDLE                                  DeviceHandle;
} D3DAUTHENTICATEDCHANNEL_CONFIGURECRYPTOSESSION;
```



## <a name="members"></a><span data-ttu-id="66723-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="66723-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="66723-108">**Parámetros**</span><span class="sxs-lookup"><span data-stu-id="66723-108">**Parameters**</span></span>
</dt> <dd>

<span data-ttu-id="66723-109">[**D3DAUTHENTICATEDCHANNEL \_ configure \_**](d3dauthenticatedchannel-configure-input.md) la estructura de entrada que contiene el GUID del comando y otros datos.</span><span class="sxs-lookup"><span data-stu-id="66723-109">A [**D3DAUTHENTICATEDCHANNEL\_CONFIGURE\_INPUT**](d3dauthenticatedchannel-configure-input.md) structure that contains the command GUID and other data.</span></span>

</dd> <dt>

<span data-ttu-id="66723-110">**DXVA2DecodeHandle**</span><span class="sxs-lookup"><span data-stu-id="66723-110">**DXVA2DecodeHandle**</span></span>
</dt> <dd>

<span data-ttu-id="66723-111">Un identificador para el dispositivo descodificador DirectX video Acceleration 2 (DXVA-2).</span><span class="sxs-lookup"><span data-stu-id="66723-111">A handle to the DirectX Video Acceleration 2 (DXVA-2) decoder device.</span></span>

</dd> <dt>

<span data-ttu-id="66723-112">**CryptoSessionHandle**</span><span class="sxs-lookup"><span data-stu-id="66723-112">**CryptoSessionHandle**</span></span>
</dt> <dd>

<span data-ttu-id="66723-113">Identificador de la sesión criptográfica.</span><span class="sxs-lookup"><span data-stu-id="66723-113">A handle to the cryptographic session.</span></span>

</dd> <dt>

<span data-ttu-id="66723-114">**DeviceHandle**</span><span class="sxs-lookup"><span data-stu-id="66723-114">**DeviceHandle**</span></span>
</dt> <dd>

<span data-ttu-id="66723-115">Identificador del dispositivo Direct3D.</span><span class="sxs-lookup"><span data-stu-id="66723-115">A handle to the Direct3D device.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="66723-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="66723-116">Requirements</span></span>



| <span data-ttu-id="66723-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="66723-117">Requirement</span></span> | <span data-ttu-id="66723-118">Value</span><span class="sxs-lookup"><span data-stu-id="66723-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="66723-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="66723-119">Minimum supported client</span></span><br/> | <span data-ttu-id="66723-120">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="66723-120">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="66723-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="66723-121">Minimum supported server</span></span><br/> | <span data-ttu-id="66723-122">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="66723-122">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="66723-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="66723-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="66723-124"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="66723-124"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="66723-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="66723-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66723-126">Estructuras de vídeo de Direct3D</span><span class="sxs-lookup"><span data-stu-id="66723-126">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> <dt>

[<span data-ttu-id="66723-127">**IDirect3DAuthenticatedChannel9:: configure**</span><span class="sxs-lookup"><span data-stu-id="66723-127">**IDirect3DAuthenticatedChannel9::Configure**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure)
</dt> </dl>

 

 




