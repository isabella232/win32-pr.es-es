---
description: Define un par de algoritmos de cifrado y autenticación 802,11 que se pueden habilitar al mismo tiempo en la estación 802,11.
ms.assetid: 5fbe23f6-7902-46d4-a1f0-57f045d78662
title: DOT11_AUTH_CIPHER_PAIR estructura (Wlantypes. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DOT11_AUTH_CIPHER_PAIR
api_type:
- HeaderDef
api_location:
- wlantypes.h
ms.openlocfilehash: fd1a8ef03d5c5cb897d95b768f8ab48705098d74
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687763"
---
# <a name="dot11_auth_cipher_pair-structure"></a><span data-ttu-id="3bc29-103">\_Estructura del \_ par de cifrado de autenticación de DOT11 \_</span><span class="sxs-lookup"><span data-stu-id="3bc29-103">DOT11\_AUTH\_CIPHER\_PAIR structure</span></span>

<span data-ttu-id="3bc29-104">La estructura de **\_ \_ \_ pares de cifrado de autenticación de DOT11** define un par de algoritmos de autenticación y cifrado 802,11 que se pueden habilitar al mismo tiempo en la estación 802,11.</span><span class="sxs-lookup"><span data-stu-id="3bc29-104">The **DOT11\_AUTH\_CIPHER\_PAIR** structure defines a pair of 802.11 authentication and cipher algorithms that can be enabled at the same time on the 802.11 station.</span></span>

## <a name="syntax"></a><span data-ttu-id="3bc29-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3bc29-105">Syntax</span></span>


```C++
typedef struct _DOT11_AUTH_CIPHER_PAIR {
  DOT11_AUTH_ALGORITHM   AuthAlgoId;
  DOT11_CIPHER_ALGORITHM CipherAlgoId;
} DOT11_AUTH_CIPHER_PAIR, *PDOT11_AUTH_CIPHER_PAIR;
```



## <a name="members"></a><span data-ttu-id="3bc29-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="3bc29-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="3bc29-107">**AuthAlgoId**</span><span class="sxs-lookup"><span data-stu-id="3bc29-107">**AuthAlgoId**</span></span>
</dt> <dd>

<span data-ttu-id="3bc29-108">Un algoritmo de autenticación que usa un tipo enumerado de [**\_ \_ algoritmo**](dot11-auth-algorithm.md) de autenticación de DOT11.</span><span class="sxs-lookup"><span data-stu-id="3bc29-108">An authentication algorithm that uses a [**DOT11\_AUTH\_ALGORITHM**](dot11-auth-algorithm.md) enumerated type.</span></span>

</dd> <dt>

<span data-ttu-id="3bc29-109">**CipherAlgoId**</span><span class="sxs-lookup"><span data-stu-id="3bc29-109">**CipherAlgoId**</span></span>
</dt> <dd>

<span data-ttu-id="3bc29-110">Algoritmo de cifrado que usa un tipo enumerado de [**\_ \_ algoritmo de cifrado de DOT11**](dot11-cipher-algorithm.md) .</span><span class="sxs-lookup"><span data-stu-id="3bc29-110">A cipher algorithm that uses a [**DOT11\_CIPHER\_ALGORITHM**](dot11-cipher-algorithm.md) enumerated type.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3bc29-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3bc29-111">Remarks</span></span>

<span data-ttu-id="3bc29-112">La estructura de pares de cifrado de autenticación de DOT11 \_ \_ \_ define un algoritmo de autenticación y cifrado que se puede habilitar conjuntamente para las conexiones de red de Basic Service Set (BSS).</span><span class="sxs-lookup"><span data-stu-id="3bc29-112">The DOT11\_AUTH\_CIPHER\_PAIR structure defines an authentication and cipher algorithm that can be enabled together for basic service set (BSS) network connections.</span></span>

## <a name="requirements"></a><span data-ttu-id="3bc29-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3bc29-113">Requirements</span></span>



| <span data-ttu-id="3bc29-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="3bc29-114">Requirement</span></span> | <span data-ttu-id="3bc29-115">Value</span><span class="sxs-lookup"><span data-stu-id="3bc29-115">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3bc29-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3bc29-116">Minimum supported client</span></span><br/> | <span data-ttu-id="3bc29-117">Windows Vista, Windows XP con SP3 \[ solo aplicaciones de escritorio\]</span><span class="sxs-lookup"><span data-stu-id="3bc29-117">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="3bc29-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3bc29-118">Minimum supported server</span></span><br/> | <span data-ttu-id="3bc29-119">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="3bc29-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                        |
| <span data-ttu-id="3bc29-120">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="3bc29-120">Redistributable</span></span><br/>          | <span data-ttu-id="3bc29-121">API de LAN inalámbrica para Windows XP con SP2</span><span class="sxs-lookup"><span data-stu-id="3bc29-121">Wireless LAN API for Windows XP with SP2</span></span><br/>                                                         |
| <span data-ttu-id="3bc29-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3bc29-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="3bc29-123"><dt>Wlantypes. h (incluye Windot11. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3bc29-123"><dt>Wlantypes.h (include Windot11.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3bc29-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="3bc29-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3bc29-125">**\_Algoritmo de autenticación de DOT11 \_**</span><span class="sxs-lookup"><span data-stu-id="3bc29-125">**DOT11\_AUTH\_ALGORITHM**</span></span>](dot11-auth-algorithm.md)
</dt> <dt>

[<span data-ttu-id="3bc29-126">**\_Algoritmo de cifrado de DOT11 \_**</span><span class="sxs-lookup"><span data-stu-id="3bc29-126">**DOT11\_CIPHER\_ALGORITHM**</span></span>](dot11-cipher-algorithm.md)
</dt> </dl>

 

 




