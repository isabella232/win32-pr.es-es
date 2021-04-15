---
title: OP_JOINPROV3_PART
description: Definición de OP_JOINPROV3_PART IDL
ms.assetid: 1d8bbfcf-c08e-4bc8-b569-0496703f2d67
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: 81c8f53f55a8d5a284f969cbde539b0c34406903
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/14/2020
ms.locfileid: "104421566"
---
# <a name="op_joinprov3_part-structure"></a><span data-ttu-id="ff6d1-103">Estructura de OP_JOINPROV3_PART</span><span class="sxs-lookup"><span data-stu-id="ff6d1-103">OP_JOINPROV3_PART structure</span></span>

<span data-ttu-id="ff6d1-104">Contiene información adicional que se usa para configurar un cliente unido a un dominio.</span><span class="sxs-lookup"><span data-stu-id="ff6d1-104">Contains additional information used for configuring a client joined to a domain.</span></span>

## <a name="syntax"></a><span data-ttu-id="ff6d1-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ff6d1-105">Syntax</span></span>

```C++
typedef struct _OP_JOINPROV3_PART
{
    DWORD Rid;
    [string] wchar_t *lpSid;
} OP_JOINPROV3_PART, *POP_JOINPROV3_PART;
```

## <a name="members"></a><span data-ttu-id="ff6d1-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="ff6d1-106">Members</span></span>

### <a name="rid"></a><span data-ttu-id="ff6d1-107">Libra</span><span class="sxs-lookup"><span data-stu-id="ff6d1-107">Rid</span></span>

<span data-ttu-id="ff6d1-108">Debe establecerse en el identificador relativo del SID de la cuenta de la máquina.</span><span class="sxs-lookup"><span data-stu-id="ff6d1-108">Must be set to the Relative Identifier of the machine account’s SID</span></span>

### <a name="lpsid"></a><span data-ttu-id="ff6d1-109">lpSid</span><span class="sxs-lookup"><span data-stu-id="ff6d1-109">lpSid</span></span>

<span data-ttu-id="ff6d1-110">Debe establecerse en el SID de la cuenta de la máquina en forma de cadena.</span><span class="sxs-lookup"><span data-stu-id="ff6d1-110">Must be set to the SID of the machine account in string form.</span></span>

## <a name="see-also"></a><span data-ttu-id="ff6d1-111">Vea también</span><span class="sxs-lookup"><span data-stu-id="ff6d1-111">See also</span></span>

[<span data-ttu-id="ff6d1-112">**Definiciones IDL de unión a dominio sin conexión**</span><span class="sxs-lookup"><span data-stu-id="ff6d1-112">**Offline Domain Join IDL Definitions**</span></span>](odj-idl.md)
