---
title: ODJ_SID
description: Definición de ODJ_SID IDL
ms.assetid: 1d06f725-6cd4-42cf-b171-c78a095690cb
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: dd51f2e8a54eaf5be566e5a25f013ca1d87b9341
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/14/2020
ms.locfileid: "104078559"
---
# <a name="odj_sid-structure"></a><span data-ttu-id="e0a07-103">Estructura de ODJ_SID</span><span class="sxs-lookup"><span data-stu-id="e0a07-103">ODJ_SID structure</span></span>

<span data-ttu-id="e0a07-104">Contiene un identificador de seguridad (SID).</span><span class="sxs-lookup"><span data-stu-id="e0a07-104">Contains a Security Identifier (SID).</span></span>

## <a name="syntax"></a><span data-ttu-id="e0a07-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e0a07-105">Syntax</span></span>

```C++
typedef struct _ODJ_SID
{
    UCHAR Revision;
    UCHAR SubAuthorityCount;
    SID_IDENTIFIER_AUTHORITY IdentifierAuthority;
    [size_is(SubAuthorityCount)] ULONG SubAuthority[*];
}   ODJ_SID, *PODJ_SID;
```

## <a name="members"></a><span data-ttu-id="e0a07-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="e0a07-106">Members</span></span>

### <a name="revision"></a><span data-ttu-id="e0a07-107">Revisión</span><span class="sxs-lookup"><span data-stu-id="e0a07-107">Revision</span></span>

<span data-ttu-id="e0a07-108">Debe establecerse en la revisión del SID.</span><span class="sxs-lookup"><span data-stu-id="e0a07-108">Must be set to the SID revision.</span></span>

### <a name="subauthoritycount"></a><span data-ttu-id="e0a07-109">SubAuthorityCount</span><span class="sxs-lookup"><span data-stu-id="e0a07-109">SubAuthorityCount</span></span>

<span data-ttu-id="e0a07-110">Debe establecerse en el número de elementos de la subautoridad.</span><span class="sxs-lookup"><span data-stu-id="e0a07-110">Must be set to the number of elements in SubAuthority.</span></span>

### <a name="identifierauthority"></a><span data-ttu-id="e0a07-111">IdentifierAuthority</span><span class="sxs-lookup"><span data-stu-id="e0a07-111">IdentifierAuthority</span></span>

<span data-ttu-id="e0a07-112">Debe establecerse en el identificador de la entidad de SID.</span><span class="sxs-lookup"><span data-stu-id="e0a07-112">Must be set to the SID authority identifier.</span></span>

### <a name="subauthority"></a><span data-ttu-id="e0a07-113">Subautoridad</span><span class="sxs-lookup"><span data-stu-id="e0a07-113">SubAuthority</span></span>

<span data-ttu-id="e0a07-114">Debe contener una matriz de subentidades de SID.</span><span class="sxs-lookup"><span data-stu-id="e0a07-114">Must contain an array of SID sub authorities.</span></span>

## <a name="see-also"></a><span data-ttu-id="e0a07-115">Vea también</span><span class="sxs-lookup"><span data-stu-id="e0a07-115">See also</span></span>

[<span data-ttu-id="e0a07-116">**Definiciones IDL de unión a dominio sin conexión**</span><span class="sxs-lookup"><span data-stu-id="e0a07-116">**Offline Domain Join IDL Definitions**</span></span>](odj-idl.md)

[<span data-ttu-id="e0a07-117">**ODJ \_ \_ entidad de identificación \_ SID**</span><span class="sxs-lookup"><span data-stu-id="e0a07-117">**ODJ\_SID\_IDENTIFIER\_AUTHORITY**</span></span>](odj-sid_identifier_authority.md)
