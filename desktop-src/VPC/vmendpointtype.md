---
title: Enumeración VMEndpointType (VPCCOMInterfaces. h)
description: Especifica el tipo de extremo.
ms.assetid: b48bd860-50dc-4c8c-b65b-69c407d4612a
keywords:
- Enumeración de VMEndpointType Virtual PC
topic_type:
- apiref
api_name:
- VMEndpointType
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 912eb43147af03dd2b9923c4bdb778044f40d023
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905212"
---
# <a name="vmendpointtype-enumeration"></a><span data-ttu-id="c07d3-104">Enumeración VMEndpointType</span><span class="sxs-lookup"><span data-stu-id="c07d3-104">VMEndpointType enumeration</span></span>

<span data-ttu-id="c07d3-105">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="c07d3-105">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="c07d3-106">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="c07d3-106">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="c07d3-107">Especifica el tipo de extremo.</span><span class="sxs-lookup"><span data-stu-id="c07d3-107">Specifies the endpoint type.</span></span>

## <a name="syntax"></a><span data-ttu-id="c07d3-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c07d3-108">Syntax</span></span>


```C++
typedef enum  { 
  vmEndpoint_NamedPipe  = 0,
  vmEndpoint_TCPIP      = 1
} VMEndpointType;
```



## <a name="constants"></a><span data-ttu-id="c07d3-109">Constantes</span><span class="sxs-lookup"><span data-stu-id="c07d3-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="c07d3-110"><span id="vmEndpoint_NamedPipe"></span><span id="vmendpoint_namedpipe"></span><span id="VMENDPOINT_NAMEDPIPE"></span>**vmEndpoint \_ NamedPipe**</span><span class="sxs-lookup"><span data-stu-id="c07d3-110"><span id="vmEndpoint_NamedPipe"></span><span id="vmendpoint_namedpipe"></span><span id="VMENDPOINT_NAMEDPIPE"></span>**vmEndpoint\_NamedPipe**</span></span>
</dt> <dd>

<span data-ttu-id="c07d3-111">El lado del host.</span><span class="sxs-lookup"><span data-stu-id="c07d3-111">The host side.</span></span>

</dd> <dt>

<span data-ttu-id="c07d3-112"><span id="vmEndpoint_TCPIP"></span><span id="vmendpoint_tcpip"></span><span id="VMENDPOINT_TCPIP"></span>**vmEndpoint \_ TCPIP**</span><span class="sxs-lookup"><span data-stu-id="c07d3-112"><span id="vmEndpoint_TCPIP"></span><span id="vmendpoint_tcpip"></span><span id="VMENDPOINT_TCPIP"></span>**vmEndpoint\_TCPIP**</span></span>
</dt> <dd>

<span data-ttu-id="c07d3-113">El lado invitado.</span><span class="sxs-lookup"><span data-stu-id="c07d3-113">The guest side.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c07d3-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c07d3-114">Requirements</span></span>



| <span data-ttu-id="c07d3-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="c07d3-115">Requirement</span></span> | <span data-ttu-id="c07d3-116">Value</span><span class="sxs-lookup"><span data-stu-id="c07d3-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="c07d3-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c07d3-117">Minimum supported client</span></span><br/> | <span data-ttu-id="c07d3-118">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="c07d3-118">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c07d3-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c07d3-119">Minimum supported server</span></span><br/> | <span data-ttu-id="c07d3-120">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="c07d3-120">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="c07d3-121">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="c07d3-121">End of client support</span></span><br/>    | <span data-ttu-id="c07d3-122">Windows 7</span><span class="sxs-lookup"><span data-stu-id="c07d3-122">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="c07d3-123">Producto</span><span class="sxs-lookup"><span data-stu-id="c07d3-123">Product</span></span><br/>                  | <span data-ttu-id="c07d3-124">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="c07d3-124">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="c07d3-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c07d3-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="c07d3-126"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="c07d3-126"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c07d3-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="c07d3-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c07d3-128">**IVMVirtualMachine::StartCommunicationChannel**</span><span class="sxs-lookup"><span data-stu-id="c07d3-128">**IVMVirtualMachine::StartCommunicationChannel**</span></span>](ivmvirtualmachine-startcommunicationchannel.md)
</dt> </dl>

 

