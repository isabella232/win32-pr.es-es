---
title: Propiedad RedirectionState de IMsRdpDrive
description: Indica el estado de redireccionamiento de la unidad.
ms.assetid: 05333671-460d-4c07-8b7e-fbb7bc215353
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad RedirectionState
- Propiedad RedirectionState Servicios de Escritorio remoto, interfaz IMsRdpDrive
- Servicios de Escritorio remoto de la interfaz IMsRdpDrive, propiedad RedirectionState
topic_type:
- apiref
api_name:
- IMsRdpDrive.RedirectionState
- IMsRdpDrive.get_RedirectionState
- IMsRdpDrive.put_RedirectionState
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7561190e976e0b8190553376f5e9f7a5b2de2550
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422476"
---
# <a name="imsrdpdriveredirectionstate-property"></a><span data-ttu-id="521fe-106">IMsRdpDrive:: RedirectionState (propiedad)</span><span class="sxs-lookup"><span data-stu-id="521fe-106">IMsRdpDrive::RedirectionState property</span></span>

<span data-ttu-id="521fe-107">Indica el estado de redireccionamiento de la unidad.</span><span class="sxs-lookup"><span data-stu-id="521fe-107">Indicates the redirection state of the drive.</span></span>

<span data-ttu-id="521fe-108">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="521fe-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="521fe-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="521fe-109">Syntax</span></span>


```C++
HRESULT put_RedirectionState(
  [in]  VARIANT_BOOL vboolRedirState
);

HRESULT get_RedirectionState(
  [out] VARIANT_BOOL *pvboolRedirState
);
```



## <a name="property-value"></a><span data-ttu-id="521fe-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="521fe-110">Property value</span></span>

<span data-ttu-id="521fe-111">Establezca este parámetro en **Variant \_ false**.</span><span class="sxs-lookup"><span data-stu-id="521fe-111">Set this parameter to **VARIANT\_FALSE**.</span></span> <span data-ttu-id="521fe-112">para deshabilitar la redirección o la **variante \_ verdadera**.</span><span class="sxs-lookup"><span data-stu-id="521fe-112">to disable redirection or **VARIANT\_TRUE**.</span></span> <span data-ttu-id="521fe-113">para habilitar la redirección.</span><span class="sxs-lookup"><span data-stu-id="521fe-113">to enable redirection.</span></span>

## <a name="error-codes"></a><span data-ttu-id="521fe-114">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="521fe-114">Error codes</span></span>

<span data-ttu-id="521fe-115">Si el método se ejecuta correctamente, se devuelve **S \_ OK** .</span><span class="sxs-lookup"><span data-stu-id="521fe-115">If the method succeeds, **S\_OK** is returned.</span></span> <span data-ttu-id="521fe-116">Cualquier otro valor **HRESULT** indica que se produjo un error en la llamada.</span><span class="sxs-lookup"><span data-stu-id="521fe-116">Any other **HRESULT** value indicates that the call failed.</span></span>

## <a name="requirements"></a><span data-ttu-id="521fe-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="521fe-117">Requirements</span></span>



| <span data-ttu-id="521fe-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="521fe-118">Requirement</span></span> | <span data-ttu-id="521fe-119">Value</span><span class="sxs-lookup"><span data-stu-id="521fe-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="521fe-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="521fe-120">Minimum supported client</span></span><br/> | <span data-ttu-id="521fe-121">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="521fe-121">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="521fe-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="521fe-122">Minimum supported server</span></span><br/> | <span data-ttu-id="521fe-123">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="521fe-123">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="521fe-124">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="521fe-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="521fe-125"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="521fe-125"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="521fe-126">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="521fe-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="521fe-127"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="521fe-127"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="521fe-128">IID</span><span class="sxs-lookup"><span data-stu-id="521fe-128">IID</span></span><br/>                      | <span data-ttu-id="521fe-129">IID \_ IMsRdpDrive se define como d28b5458-f694-47a8-8e61-40356a767e46</span><span class="sxs-lookup"><span data-stu-id="521fe-129">IID\_IMsRdpDrive is defined as d28b5458-f694-47a8-8e61-40356a767e46</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="521fe-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="521fe-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="521fe-131">**IMsRdpDrive**</span><span class="sxs-lookup"><span data-stu-id="521fe-131">**IMsRdpDrive**</span></span>](imsrdpdrive.md)
</dt> </dl>

 

 





