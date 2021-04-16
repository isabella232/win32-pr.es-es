---
title: Enumeración ClientSpec
description: Se usa con la propiedad ClientProtocolSpec para especificar el protocolo de escritorio remoto usado entre el cliente y el servidor.
ms.assetid: BFB2CD3C-04BF-4CB3-B156-8B08AE697327
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto enumeración ClientSpec
topic_type:
- apiref
api_name:
- ClientSpec
api_location:
- MsTscAx.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f52fbdbaa37c392de727dd2640580800d813d51
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676614"
---
# <a name="clientspec-enumeration"></a><span data-ttu-id="f9be2-104">Enumeración ClientSpec</span><span class="sxs-lookup"><span data-stu-id="f9be2-104">ClientSpec enumeration</span></span>

<span data-ttu-id="f9be2-105">Se usa con la propiedad [**ClientProtocolSpec**](imsrdpclientadvancedsettings8-clientprotocolspec.md) para especificar el protocolo de escritorio remoto usado entre el cliente y el servidor.</span><span class="sxs-lookup"><span data-stu-id="f9be2-105">Used with the [**ClientProtocolSpec**](imsrdpclientadvancedsettings8-clientprotocolspec.md) property to specify the remote desktop protocol used between the client and the server.</span></span>

## <a name="syntax"></a><span data-ttu-id="f9be2-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f9be2-106">Syntax</span></span>


```C++
typedef enum  { 
  FullMode        = 0,
  ThinClientMode,
  SmallCacheMode
} ClientSpec;
```



## <a name="constants"></a><span data-ttu-id="f9be2-107">Constantes</span><span class="sxs-lookup"><span data-stu-id="f9be2-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="f9be2-108"><span id="FullMode"></span><span id="fullmode"></span><span id="FULLMODE"></span>**FullMode**</span><span class="sxs-lookup"><span data-stu-id="f9be2-108"><span id="FullMode"></span><span id="fullmode"></span><span id="FULLMODE"></span>**FullMode**</span></span>
</dt> <dd>

<span data-ttu-id="f9be2-109">El protocolo es el protocolo de Escritorio remoto de Windows 8 completo.</span><span class="sxs-lookup"><span data-stu-id="f9be2-109">The protocol is full Windows 8 Remote Desktop protocol.</span></span>

</dd> <dt>

<span data-ttu-id="f9be2-110"><span id="ThinClientMode"></span><span id="thinclientmode"></span><span id="THINCLIENTMODE"></span>**ThinClientMode**</span><span class="sxs-lookup"><span data-stu-id="f9be2-110"><span id="ThinClientMode"></span><span id="thinclientmode"></span><span id="THINCLIENTMODE"></span>**ThinClientMode**</span></span>
</dt> <dd>

<span data-ttu-id="f9be2-111">El protocolo se limita al uso del códec de Windows 7 con SP1 RemoteFX y una caché más pequeña.</span><span class="sxs-lookup"><span data-stu-id="f9be2-111">The protocol is limited to using the Windows 7 with SP1 RemoteFX codec and a smaller cache.</span></span> <span data-ttu-id="f9be2-112">El resto de los códecs están deshabilitados.</span><span class="sxs-lookup"><span data-stu-id="f9be2-112">All other codecs are disabled.</span></span> <span data-ttu-id="f9be2-113">Este protocolo tiene la superficie de memoria más pequeña.</span><span class="sxs-lookup"><span data-stu-id="f9be2-113">This protocol has the smallest memory footprint.</span></span>

</dd> <dt>

<span data-ttu-id="f9be2-114"><span id="SmallCacheMode"></span><span id="smallcachemode"></span><span id="SMALLCACHEMODE"></span>**SmallCacheMode**</span><span class="sxs-lookup"><span data-stu-id="f9be2-114"><span id="SmallCacheMode"></span><span id="smallcachemode"></span><span id="SMALLCACHEMODE"></span>**SmallCacheMode**</span></span>
</dt> <dd>

<span data-ttu-id="f9be2-115">El protocolo es el mismo que **FullMode**, salvo que usa una caché más pequeña.</span><span class="sxs-lookup"><span data-stu-id="f9be2-115">The protocol is the same as **FullMode**, except it uses a smaller cache.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f9be2-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f9be2-116">Requirements</span></span>



| <span data-ttu-id="f9be2-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="f9be2-117">Requirement</span></span> | <span data-ttu-id="f9be2-118">Value</span><span class="sxs-lookup"><span data-stu-id="f9be2-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f9be2-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f9be2-119">Minimum supported client</span></span><br/> | <span data-ttu-id="f9be2-120">Windows 8</span><span class="sxs-lookup"><span data-stu-id="f9be2-120">Windows 8</span></span><br/>                                                                   |
| <span data-ttu-id="f9be2-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f9be2-121">Minimum supported server</span></span><br/> | <span data-ttu-id="f9be2-122">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f9be2-122">Windows Server 2012</span></span><br/>                                                         |
| <span data-ttu-id="f9be2-123">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="f9be2-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="f9be2-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f9be2-124"><dt>MsTscAx.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f9be2-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="f9be2-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9be2-126">**IMsRdpClientAdvancedSettings8::ClientProtocolSpec**</span><span class="sxs-lookup"><span data-stu-id="f9be2-126">**IMsRdpClientAdvancedSettings8::ClientProtocolSpec**</span></span>](imsrdpclientadvancedsettings8-clientprotocolspec.md)
</dt> </dl>

 

 





