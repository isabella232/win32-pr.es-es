---
description: La \_ estructura de direcciones IPX proporciona una dirección en el nivel de protocolo IPX.
ms.assetid: 06939ac3-3718-4441-b2c8-c73adfe3babe
title: Estructura de IPX_ADDRESS (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPX_ADDRESS
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 18645a455e780020037384a2df7173a019d71677
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541182"
---
# <a name="ipx_address-structure"></a><span data-ttu-id="53af0-103">\_Estructura de dirección IPX</span><span class="sxs-lookup"><span data-stu-id="53af0-103">IPX\_ADDRESS structure</span></span>

<span data-ttu-id="53af0-104">La estructura de **\_ direcciones IPX** proporciona una dirección en el nivel de protocolo IPX.</span><span class="sxs-lookup"><span data-stu-id="53af0-104">The **IPX\_ADDRESS** structure provides an address at the IPX protocol level.</span></span>

## <a name="syntax"></a><span data-ttu-id="53af0-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="53af0-105">Syntax</span></span>


```C++
typedef struct _IPX_ADDRESS {
  BYTE Subnet[4];
  BYTE Address[6];
} IPX_ADDRESS, *LPIPX_ADDRESS;
```



## <a name="members"></a><span data-ttu-id="53af0-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="53af0-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="53af0-107">**Subred**</span><span class="sxs-lookup"><span data-stu-id="53af0-107">**Subnet**</span></span>
</dt> <dd>

<span data-ttu-id="53af0-108">Identificador de subred de red.</span><span class="sxs-lookup"><span data-stu-id="53af0-108">Network subnet identifier.</span></span>

</dd> <dt>

<span data-ttu-id="53af0-109">**Dirección**</span><span class="sxs-lookup"><span data-stu-id="53af0-109">**Address**</span></span>
</dt> <dd>

<span data-ttu-id="53af0-110">Identificador de NIC de subred.</span><span class="sxs-lookup"><span data-stu-id="53af0-110">Subnet NIC identifier.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="53af0-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="53af0-111">Requirements</span></span>



| <span data-ttu-id="53af0-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="53af0-112">Requirement</span></span> | <span data-ttu-id="53af0-113">Value</span><span class="sxs-lookup"><span data-stu-id="53af0-113">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="53af0-114">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="53af0-114">Minimum supported client</span></span><br/> | <span data-ttu-id="53af0-115">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="53af0-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="53af0-116">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="53af0-116">Minimum supported server</span></span><br/> | <span data-ttu-id="53af0-117">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="53af0-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="53af0-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="53af0-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="53af0-119"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="53af0-119"><dt>Netmon.h</dt></span></span> </dl> |



 

 




