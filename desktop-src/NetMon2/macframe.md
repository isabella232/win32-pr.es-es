---
description: La estructura MACFRAME es una Unión de los protocolos iniciales más comunes.
ms.assetid: ec7e3a54-a47f-4390-a137-9574c63c9a11
title: MACFRAME Union (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MACFRAME
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: a7901daf467a63586543c52ca8a214d5d0094982
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666544"
---
# <a name="macframe-union"></a><span data-ttu-id="16a2a-103">Unión MACFRAME</span><span class="sxs-lookup"><span data-stu-id="16a2a-103">MACFRAME union</span></span>

<span data-ttu-id="16a2a-104">La estructura **MACFRAME** es una Unión de los protocolos iniciales más comunes.</span><span class="sxs-lookup"><span data-stu-id="16a2a-104">The **MACFRAME** structure is a union of the most common initial protocols.</span></span>

## <a name="syntax"></a><span data-ttu-id="16a2a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="16a2a-105">Syntax</span></span>


```C++
typedef union {
  LPBYTE      MacHeader;
  LPETHERNET  Ethernet;
  LPTOKENRING Tokenring;
  LPFDDI      Fddi;
} MACFRAME, *LPMACFRAME;
```



## <a name="members"></a><span data-ttu-id="16a2a-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="16a2a-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="16a2a-107">**MacHeader**</span><span class="sxs-lookup"><span data-stu-id="16a2a-107">**MacHeader**</span></span>
</dt> <dd>

<span data-ttu-id="16a2a-108">Puntero genérico a un marco.</span><span class="sxs-lookup"><span data-stu-id="16a2a-108">Generic pointer to a frame.</span></span>

</dd> <dt>

<span data-ttu-id="16a2a-109">**Ethernet**</span><span class="sxs-lookup"><span data-stu-id="16a2a-109">**Ethernet**</span></span>
</dt> <dd>

<span data-ttu-id="16a2a-110">Puntero Ethernet a un marco.</span><span class="sxs-lookup"><span data-stu-id="16a2a-110">Ethernet pointer to a frame.</span></span>

</dd> <dt>

<span data-ttu-id="16a2a-111">**Tokenring**</span><span class="sxs-lookup"><span data-stu-id="16a2a-111">**Tokenring**</span></span>
</dt> <dd>

<span data-ttu-id="16a2a-112">Puntero de token ring a un marco.</span><span class="sxs-lookup"><span data-stu-id="16a2a-112">Token ring pointer to a frame.</span></span>

</dd> <dt>

<span data-ttu-id="16a2a-113">**FDDI**</span><span class="sxs-lookup"><span data-stu-id="16a2a-113">**Fddi**</span></span>
</dt> <dd>

<span data-ttu-id="16a2a-114">Puntero FDDI a un marco.</span><span class="sxs-lookup"><span data-stu-id="16a2a-114">FDDI pointer to a frame.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="16a2a-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="16a2a-115">Remarks</span></span>

<span data-ttu-id="16a2a-116">Esta estructura se usa con más frecuencia como una superposición.</span><span class="sxs-lookup"><span data-stu-id="16a2a-116">This structure is most frequently used as an overlay.</span></span> <span data-ttu-id="16a2a-117">Para que se pueda tener acceso a las propiedades del primer Protocolo, convierta el marco en el mismo tipo que el protocolo.</span><span class="sxs-lookup"><span data-stu-id="16a2a-117">To make the properties of the first protocol accessible, cast the frame as the same type as the protocol.</span></span>

## <a name="requirements"></a><span data-ttu-id="16a2a-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="16a2a-118">Requirements</span></span>



| <span data-ttu-id="16a2a-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="16a2a-119">Requirement</span></span> | <span data-ttu-id="16a2a-120">Value</span><span class="sxs-lookup"><span data-stu-id="16a2a-120">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="16a2a-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="16a2a-121">Minimum supported client</span></span><br/> | <span data-ttu-id="16a2a-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="16a2a-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="16a2a-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="16a2a-123">Minimum supported server</span></span><br/> | <span data-ttu-id="16a2a-124">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="16a2a-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="16a2a-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="16a2a-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="16a2a-126"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="16a2a-126"><dt>Netmon.h</dt></span></span> </dl> |



 

 




