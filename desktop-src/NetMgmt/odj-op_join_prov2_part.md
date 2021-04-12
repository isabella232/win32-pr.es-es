---
title: OP_JOINPROV2_PART
description: Definición de OP_JOINPROV2_PART IDL
ms.assetid: c220627e-49bd-49f2-a03c-9cdef4b973ca
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: f8537b6ca9627a15470115a20f99082dae80e040
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/14/2020
ms.locfileid: "104149715"
---
# <a name="op_joinprov2_part-structure"></a><span data-ttu-id="7445b-103">Estructura de OP_JOINPROV2_PART</span><span class="sxs-lookup"><span data-stu-id="7445b-103">OP_JOINPROV2_PART structure</span></span>

<span data-ttu-id="7445b-104">Contiene información adicional que se usa para configurar un cliente unido a un dominio.</span><span class="sxs-lookup"><span data-stu-id="7445b-104">Contains additional information used for configuring a client joined to a domain.</span></span>

## <a name="syntax"></a><span data-ttu-id="7445b-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7445b-105">Syntax</span></span>

```C++
typedef struct _OP_JOINPROV2_PART
{
    DWORD     dwFlags;
    [string] wchar_t *lpNetbiosName;
    [string] wchar_t *lpSiteName;
    [string] wchar_t *lpPrimaryDNSDomain;
    DWORD             dwReserved;
    [string] wchar_t *lpReserved;
} OP_JOINPROV2_PART, *POP_JOINPROV2_PART;
```

## <a name="members"></a><span data-ttu-id="7445b-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="7445b-106">Members</span></span>

### <a name="dwflags"></a><span data-ttu-id="7445b-107">dwFlags</span><span class="sxs-lookup"><span data-stu-id="7445b-107">dwFlags</span></span>

<span data-ttu-id="7445b-108">Debe establecerse en cero o en uno de los valores siguientes:</span><span class="sxs-lookup"><span data-stu-id="7445b-108">Must be set to either zero or one of the following values:</span></span>

|<span data-ttu-id="7445b-109">Value</span><span class="sxs-lookup"><span data-stu-id="7445b-109">Value</span></span>|<span data-ttu-id="7445b-110">Significado</span><span class="sxs-lookup"><span data-stu-id="7445b-110">Meaning</span></span>|
| --- | --- |
|<span data-ttu-id="7445b-111">OP_JP2_FLAG_PERSISTENTSITE (0x00000001)</span><span class="sxs-lookup"><span data-stu-id="7445b-111">OP_JP2_FLAG_PERSISTENTSITE (0x00000001)</span></span>|<span data-ttu-id="7445b-112">El sitio especificado en lpSiteName debe considerarse como el sitio permanente para el cliente.</span><span class="sxs-lookup"><span data-stu-id="7445b-112">The site specified in lpSiteName MUST be considered the permanent site for the client.</span></span>|

### <a name="lpnetbiosname"></a><span data-ttu-id="7445b-113">lpNetbiosName</span><span class="sxs-lookup"><span data-stu-id="7445b-113">lpNetbiosName</span></span>

<span data-ttu-id="7445b-114">Contiene el nombre NetBIOS de la cuenta de equipo en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="7445b-114">Contains the Netbios name of the machine account in Unicode format.</span></span>

### <a name="lpsitename"></a><span data-ttu-id="7445b-115">lpSiteName</span><span class="sxs-lookup"><span data-stu-id="7445b-115">lpSiteName</span></span>

<span data-ttu-id="7445b-116">Contiene el nombre del sitio Active Directory que el cliente debe utilizar.</span><span class="sxs-lookup"><span data-stu-id="7445b-116">Contains the name of the Active Directory site that the client should use.</span></span>

### <a name="lpprimarydnsdomain"></a><span data-ttu-id="7445b-117">lpPrimaryDNSDomain</span><span class="sxs-lookup"><span data-stu-id="7445b-117">lpPrimaryDNSDomain</span></span>

<span data-ttu-id="7445b-118">Contiene el nombre de dominio DNS principal que debe usar el cliente.</span><span class="sxs-lookup"><span data-stu-id="7445b-118">Contains the primary DNS domain name that the client should use.</span></span>

### <a name="dwreserved"></a><span data-ttu-id="7445b-119">dwReserved</span><span class="sxs-lookup"><span data-stu-id="7445b-119">dwReserved</span></span>

<span data-ttu-id="7445b-120">Reservado para uso futuro y debe establecerse en 0.</span><span class="sxs-lookup"><span data-stu-id="7445b-120">Reserved for future use and must be set to 0.</span></span>

### <a name="lpreserved"></a><span data-ttu-id="7445b-121">lpReserved</span><span class="sxs-lookup"><span data-stu-id="7445b-121">lpReserved</span></span>

<span data-ttu-id="7445b-122">Reservado para uso futuro y debe establecerse en NULL.</span><span class="sxs-lookup"><span data-stu-id="7445b-122">Reserved for future use and must be set to NULL.</span></span>

## <a name="see-also"></a><span data-ttu-id="7445b-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="7445b-123">See also</span></span>

[<span data-ttu-id="7445b-124">**Definiciones IDL de unión a dominio sin conexión**</span><span class="sxs-lookup"><span data-stu-id="7445b-124">**Offline Domain Join IDL Definitions**</span></span>](odj-idl.md)
