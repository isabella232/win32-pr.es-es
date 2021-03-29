---
title: IMsRdpClientSecuredSettings2 (propiedad de PCB)
description: Especifica la configuración del BLOB de preconexión (PCB) que se va a usar antes de la conexión para la transmisión al servidor. | IMsRdpClientSecuredSettings2 (propiedad de PCB)
ms.assetid: e2ddd9fd-d868-4fc5-835d-0f4db5da71e3
ms.tgt_platform: multiple
keywords:
- Propiedad PCB Servicios de Escritorio remoto
- Propiedad PCB Servicios de Escritorio remoto, interfaz IMsRdpClientSecuredSettings2
- Servicios de Escritorio remoto de la interfaz IMsRdpClientSecuredSettings2, propiedad PCB
topic_type:
- apiref
api_name:
- IMsRdpClientSecuredSettings2.PCB
- IMsRdpClientSecuredSettings2.get_PCB
- IMsRdpClientSecuredSettings2.put_PCB
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c99b9a04a854f218fcbe1735ec6271aa4a58edba
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105678751"
---
# <a name="imsrdpclientsecuredsettings2pcb-property"></a><span data-ttu-id="c058d-107">IMsRdpClientSecuredSettings2::P propiedad CB</span><span class="sxs-lookup"><span data-stu-id="c058d-107">IMsRdpClientSecuredSettings2::PCB property</span></span>

<span data-ttu-id="c058d-108">Especifica la configuración del BLOB de preconexión (PCB) que se va a usar antes de la conexión para la transmisión al servidor.</span><span class="sxs-lookup"><span data-stu-id="c058d-108">Specifies the preconnection BLOB (PCB) setting to use prior to connecting for transmission to the server.</span></span>

<span data-ttu-id="c058d-109">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="c058d-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="c058d-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c058d-110">Syntax</span></span>


```C++
HRESULT put_PCB(
  [in]          BSTR bstrPCB
);

HRESULT get_PCB(
  [out, retval] BSTR *bstrPCB
);
```



## <a name="property-value"></a><span data-ttu-id="c058d-111">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="c058d-111">Property value</span></span>

<span data-ttu-id="c058d-112">La configuración de PCB.</span><span class="sxs-lookup"><span data-stu-id="c058d-112">The PCB setting.</span></span>

## <a name="requirements"></a><span data-ttu-id="c058d-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c058d-113">Requirements</span></span>



| <span data-ttu-id="c058d-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="c058d-114">Requirement</span></span> | <span data-ttu-id="c058d-115">Value</span><span class="sxs-lookup"><span data-stu-id="c058d-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c058d-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c058d-116">Minimum supported client</span></span><br/> | <span data-ttu-id="c058d-117">Windows 7</span><span class="sxs-lookup"><span data-stu-id="c058d-117">Windows 7</span></span><br/>                                                                   |
| <span data-ttu-id="c058d-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c058d-118">Minimum supported server</span></span><br/> | <span data-ttu-id="c058d-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c058d-119">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="c058d-120">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="c058d-120">Type library</span></span><br/>             | <dl> <span data-ttu-id="c058d-121"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c058d-121"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="c058d-122">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c058d-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c058d-123"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c058d-123"><dt>MsTscAx.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c058d-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="c058d-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c058d-125">**IMsRdpClientSecuredSettings2**</span><span class="sxs-lookup"><span data-stu-id="c058d-125">**IMsRdpClientSecuredSettings2**</span></span>](imsrdpclientsecuredsettings2.md)
</dt> </dl>

 

 





