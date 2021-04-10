---
description: Contiene un número de Puerto usado para los protocolos IP o IPX.
ms.assetid: 730f6ee6-7b7d-4e10-91ee-a4ba87aae5aa
title: GENERIC_PORT Union (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GENERIC_PORT
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 3b684ffea65e85854d2928931f492fb247cc0b70
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000937"
---
# <a name="generic_port-union"></a><span data-ttu-id="5cdce-103">\_Unión de Puerto genérico</span><span class="sxs-lookup"><span data-stu-id="5cdce-103">GENERIC\_PORT union</span></span>

<span data-ttu-id="5cdce-104">La estructura de **\_ Puerto genérico** contiene un número de Puerto usado para los protocolos IP o IPX.</span><span class="sxs-lookup"><span data-stu-id="5cdce-104">The **GENERIC\_PORT** structure contains a port number used for IP or IPX protocols.</span></span>

## <a name="syntax"></a><span data-ttu-id="5cdce-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5cdce-105">Syntax</span></span>


```C++
typedef union {
  BYTE IPPort;
  WORD ByteSwappedIPXPort;
} GENERIC_PORT;
```



## <a name="members"></a><span data-ttu-id="5cdce-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="5cdce-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="5cdce-107">**IPPort**</span><span class="sxs-lookup"><span data-stu-id="5cdce-107">**IPPort**</span></span>
</dt> <dd>

<span data-ttu-id="5cdce-108">Número de puerto IP rellenado.</span><span class="sxs-lookup"><span data-stu-id="5cdce-108">IP port number filled in.</span></span>

</dd> <dt>

<span data-ttu-id="5cdce-109">**ByteSwappedIPXPort**</span><span class="sxs-lookup"><span data-stu-id="5cdce-109">**ByteSwappedIPXPort**</span></span>
</dt> <dd>

<span data-ttu-id="5cdce-110">Número de Puerto IPX rellenado.</span><span class="sxs-lookup"><span data-stu-id="5cdce-110">IPX port number filled in.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5cdce-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5cdce-111">Requirements</span></span>



| <span data-ttu-id="5cdce-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="5cdce-112">Requirement</span></span> | <span data-ttu-id="5cdce-113">Value</span><span class="sxs-lookup"><span data-stu-id="5cdce-113">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="5cdce-114">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5cdce-114">Minimum supported client</span></span><br/> | <span data-ttu-id="5cdce-115">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="5cdce-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="5cdce-116">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5cdce-116">Minimum supported server</span></span><br/> | <span data-ttu-id="5cdce-117">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="5cdce-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="5cdce-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5cdce-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="5cdce-119"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="5cdce-119"><dt>Netmon.h</dt></span></span> </dl> |



 

 




