---
title: UUID
description: Proporciona una designación única de un objeto como, por ejemplo, una interfaz, un vector de punto de entrada de administrador o un objeto de cliente.
ms.localizationpriority: low
ms.topic: reference
ms.date: 09/09/2019
ms.openlocfilehash: 95d2d420502a5d92af64c902ffa82c709639d872
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104148983"
---
# <a name="uuid-structure"></a><span data-ttu-id="ac1c3-103">UUID (estructura)</span><span class="sxs-lookup"><span data-stu-id="ac1c3-103">UUID structure</span></span>

<span data-ttu-id="ac1c3-104">La estructura de **UUID** define un identificador único universal (UUID).</span><span class="sxs-lookup"><span data-stu-id="ac1c3-104">The **UUID** structure defines a Universally Unique Identifier (UUID).</span></span> <span data-ttu-id="ac1c3-105">Un **UUID** proporciona una designación única de un objeto como una interfaz, un vector de punto de entrada de administrador o un objeto de cliente.</span><span class="sxs-lookup"><span data-stu-id="ac1c3-105">A **UUID** provides a unique designation of an object such as an interface, a manager entry-point vector, or a client object.</span></span>

<span data-ttu-id="ac1c3-106">La estructura de **UUID** es un `typedef` sinónimo de la estructura [GUID](/windows/win32/api/guiddef/ns-guiddef-guid) .</span><span class="sxs-lookup"><span data-stu-id="ac1c3-106">The **UUID** structure is a `typedef`'d synonym for the [GUID](/windows/win32/api/guiddef/ns-guiddef-guid) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac1c3-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ac1c3-107">Syntax</span></span>

```cpp
typedef GUID UUID;
```

## <a name="remarks"></a><span data-ttu-id="ac1c3-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ac1c3-108">Remarks</span></span>

<span data-ttu-id="ac1c3-109">Las bibliotecas en tiempo de ejecución de RPC usan **UUID** para comprobar la compatibilidad entre los clientes y los servidores, y para seleccionar entre varias implementaciones de una interfaz.</span><span class="sxs-lookup"><span data-stu-id="ac1c3-109">The RPC run-time libraries use **UUID** s to check for compatibility between clients and servers, and to select among multiple implementations of an interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="ac1c3-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ac1c3-110">Requirements</span></span>

| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="ac1c3-111">**Header**</span><span class="sxs-lookup"><span data-stu-id="ac1c3-111">**Header**</span></span> | <span data-ttu-id="ac1c3-112">Definido en rpcdce. h; incluir RPC. h</span><span class="sxs-lookup"><span data-stu-id="ac1c3-112">Defined in rpcdce.h; include rpc.h</span></span> |

## <a name="see-also"></a><span data-ttu-id="ac1c3-113">Vea también</span><span class="sxs-lookup"><span data-stu-id="ac1c3-113">See also</span></span>

<span data-ttu-id="ac1c3-114">[GUID](/windows/win32/api/guiddef/ns-guiddef-guid) 
 de [UUID \_ VECTOR](/windows/win32/api/rpcdce/ns-rpcdce-uuid_vector)</span><span class="sxs-lookup"><span data-stu-id="ac1c3-114">[GUID](/windows/win32/api/guiddef/ns-guiddef-guid)
[UUID\_VECTOR](/windows/win32/api/rpcdce/ns-rpcdce-uuid_vector)</span></span>