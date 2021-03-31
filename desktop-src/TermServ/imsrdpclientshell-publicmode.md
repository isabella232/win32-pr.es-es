---
title: Propiedad PublicMode de IMsRdpClientShell
description: Especifica o recupera si está habilitado el modo público.
ms.assetid: 983d3e46-f09e-4425-88a1-9d4ae0d9c70a
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad PublicMode
- Propiedad PublicMode Servicios de Escritorio remoto, interfaz IMsRdpClientShell
- Servicios de Escritorio remoto de la interfaz IMsRdpClientShell, propiedad PublicMode
topic_type:
- apiref
api_name:
- IMsRdpClientShell.PublicMode
- IMsRdpClientShell.get_PublicMode
- IMsRdpClientShell.put_PublicMode
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4129b3a9eeb62af0fa6e970c812ea6adf9670c55
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491651"
---
# <a name="imsrdpclientshellpublicmode-property"></a><span data-ttu-id="9d66f-106">IMsRdpClientShell::P propiedad ublicMode</span><span class="sxs-lookup"><span data-stu-id="9d66f-106">IMsRdpClientShell::PublicMode property</span></span>

<span data-ttu-id="9d66f-107">Especifica o recupera si está habilitado el modo público.</span><span class="sxs-lookup"><span data-stu-id="9d66f-107">Specifies or retrieves whether public mode is enabled.</span></span>

<span data-ttu-id="9d66f-108">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="9d66f-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d66f-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9d66f-109">Syntax</span></span>


```C++
HRESULT put_PublicMode(
  [in]  VARIANT_BOOL fPublicMode
);

HRESULT get_PublicMode(
  [out] VARIANT_BOOL *pfPublicMode
);
```



## <a name="property-value"></a><span data-ttu-id="9d66f-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="9d66f-110">Property value</span></span>

<span data-ttu-id="9d66f-111">Especifica si está habilitado el modo público.</span><span class="sxs-lookup"><span data-stu-id="9d66f-111">Specifies whether public mode is enabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="9d66f-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9d66f-112">Requirements</span></span>



| <span data-ttu-id="9d66f-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="9d66f-113">Requirement</span></span> | <span data-ttu-id="9d66f-114">Value</span><span class="sxs-lookup"><span data-stu-id="9d66f-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9d66f-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9d66f-115">Minimum supported client</span></span><br/> | <span data-ttu-id="9d66f-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9d66f-116">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="9d66f-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9d66f-117">Minimum supported server</span></span><br/> | <span data-ttu-id="9d66f-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9d66f-118">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="9d66f-119">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="9d66f-119">Type library</span></span><br/>             | <dl> <span data-ttu-id="9d66f-120"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9d66f-120"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="9d66f-121">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="9d66f-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9d66f-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9d66f-122"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="9d66f-123">IID</span><span class="sxs-lookup"><span data-stu-id="9d66f-123">IID</span></span><br/>                      | <span data-ttu-id="9d66f-124">IID \_ IMsRdpClientShell se define como d012ae6d-c19a-4bfe-B367-201f8911f134</span><span class="sxs-lookup"><span data-stu-id="9d66f-124">IID\_IMsRdpClientShell is defined as d012ae6d-c19a-4bfe-b367-201f8911f134</span></span><br/>   |



## <a name="see-also"></a><span data-ttu-id="9d66f-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="9d66f-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d66f-126">**IMsRdpClientShell**</span><span class="sxs-lookup"><span data-stu-id="9d66f-126">**IMsRdpClientShell**</span></span>](imsrdpclientshell.md)
</dt> </dl>

 

 





