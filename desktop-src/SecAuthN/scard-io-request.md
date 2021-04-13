---
description: La estructura de \_ solicitud de e/s PPAC \_ comienza una estructura de información de control de protocolo.
ms.assetid: 80fd7c6e-e768-42db-8302-29e92c9552f0
title: SCARD_IO_REQUEST estructura (Winsmcrd. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SCARD_IO_REQUEST
api_type:
- HeaderDef
api_location:
- Winsmcrd.h
ms.openlocfilehash: fe3205311789ee51bb9b96b3b425b735e1fdf887
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360663"
---
# <a name="scard_io_request-structure"></a><span data-ttu-id="8397a-103">Estructura de \_ solicitud de e/s de PPAC \_</span><span class="sxs-lookup"><span data-stu-id="8397a-103">SCARD\_IO\_REQUEST structure</span></span>

<span data-ttu-id="8397a-104">La estructura de **\_ \_ solicitud de e/s PPAC** comienza una estructura de información de control de protocolo.</span><span class="sxs-lookup"><span data-stu-id="8397a-104">The **SCARD\_IO\_REQUEST** structure begins a protocol control information structure.</span></span> <span data-ttu-id="8397a-105">Cualquier información específica del protocolo sigue inmediatamente a esta estructura.</span><span class="sxs-lookup"><span data-stu-id="8397a-105">Any protocol-specific information then immediately follows this structure.</span></span> <span data-ttu-id="8397a-106">La longitud completa de la estructura debe estar alineada con el tamaño de la palabra de la arquitectura de hardware subyacente.</span><span class="sxs-lookup"><span data-stu-id="8397a-106">The entire length of the structure must be aligned with the underlying hardware architecture word size.</span></span> <span data-ttu-id="8397a-107">Por ejemplo, en Win32 la longitud de cualquier información de PCI debe ser un múltiplo de cuatro bytes para que se alinee en un límite de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="8397a-107">For example, in Win32 the length of any PCI information must be a multiple of four bytes so that it aligns on a 32-bit boundary.</span></span>

## <a name="syntax"></a><span data-ttu-id="8397a-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8397a-108">Syntax</span></span>


```C++
typedef struct {
  DWORD dwProtocol;
  DWORD cbPciLength;
} SCARD_IO_REQUEST;
```



## <a name="members"></a><span data-ttu-id="8397a-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="8397a-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="8397a-110">**dwProtocol**</span><span class="sxs-lookup"><span data-stu-id="8397a-110">**dwProtocol**</span></span>
</dt> <dd>

<span data-ttu-id="8397a-111">Protocolo en uso.</span><span class="sxs-lookup"><span data-stu-id="8397a-111">Protocol in use.</span></span>

</dd> <dt>

<span data-ttu-id="8397a-112">**cbPciLength**</span><span class="sxs-lookup"><span data-stu-id="8397a-112">**cbPciLength**</span></span>
</dt> <dd>

<span data-ttu-id="8397a-113">Longitud, en bytes, de la estructura de **\_ \_ solicitud de e/s** integrada más cualquier información específica de PCI siguiente.</span><span class="sxs-lookup"><span data-stu-id="8397a-113">Length, in bytes, of the **SCARD\_IO\_REQUEST** structure plus any following PCI-specific information.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8397a-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8397a-114">Requirements</span></span>



| <span data-ttu-id="8397a-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="8397a-115">Requirement</span></span> | <span data-ttu-id="8397a-116">Value</span><span class="sxs-lookup"><span data-stu-id="8397a-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8397a-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8397a-117">Minimum supported client</span></span><br/> | <span data-ttu-id="8397a-118">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="8397a-118">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="8397a-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8397a-119">Minimum supported server</span></span><br/> | <span data-ttu-id="8397a-120">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="8397a-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8397a-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8397a-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="8397a-122"><dt>Winsmcrd. h</dt></span><span class="sxs-lookup"><span data-stu-id="8397a-122"><dt>Winsmcrd.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8397a-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="8397a-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8397a-124">**SCardTransmit**</span><span class="sxs-lookup"><span data-stu-id="8397a-124">**SCardTransmit**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardtransmit)
</dt> </dl>

 

 




