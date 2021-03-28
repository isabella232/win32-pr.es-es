---
description: Esta clase es la clase de tipo de evento para los eventos de espera de respuesta de ALPC. La siguiente sintaxis se simplifica desde el código MOF.
ms.assetid: 9aaa2c93-41cc-4025-80f9-b7740a37c4d8
title: ALPC_Wait_For_Reply (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ALPC_Wait_For_Reply
- ALPC_Wait_For_Reply.MessageID
api_type:
- NA
api_location: ''
ms.openlocfilehash: 898077511db25ec7f53bc075ecb845d04e540626
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984526"
---
# <a name="alpc_wait_for_reply-class"></a><span data-ttu-id="4f07b-104">ALPC- \_ esperar \_ para la \_ clase de respuesta</span><span class="sxs-lookup"><span data-stu-id="4f07b-104">ALPC\_Wait\_For\_Reply class</span></span>

<span data-ttu-id="4f07b-105">Esta clase es la clase de tipo de evento para los eventos de espera de respuesta de ALPC.</span><span class="sxs-lookup"><span data-stu-id="4f07b-105">This class is the event type class for ALPC wait for reply events.</span></span>

<span data-ttu-id="4f07b-106">La siguiente sintaxis se simplifica desde el código MOF.</span><span class="sxs-lookup"><span data-stu-id="4f07b-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="4f07b-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4f07b-107">Syntax</span></span>

``` syntax
[EventType(35), EventTypeName("ALPC-Wait-For-Reply")]
class ALPC_Wait_For_Reply : ALPC
{
  uint32 MessageID;
};
```

## <a name="members"></a><span data-ttu-id="4f07b-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="4f07b-108">Members</span></span>

<span data-ttu-id="4f07b-109">La **clase \_ Wait \_ for \_ reply de ALPC** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="4f07b-109">The **ALPC\_Wait\_For\_Reply** class has these types of members:</span></span>

-   [<span data-ttu-id="4f07b-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="4f07b-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4f07b-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="4f07b-111">Properties</span></span>

<span data-ttu-id="4f07b-112">La **clase \_ Wait \_ for \_ reply de ALPC** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="4f07b-112">The **ALPC\_Wait\_For\_Reply** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4f07b-113">**Identificador**</span><span class="sxs-lookup"><span data-stu-id="4f07b-113">**MessageID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f07b-114">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4f07b-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4f07b-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4f07b-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4f07b-116">Identificador de mensaje.</span><span class="sxs-lookup"><span data-stu-id="4f07b-116">Message identifier.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4f07b-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4f07b-117">Requirements</span></span>



| <span data-ttu-id="4f07b-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="4f07b-118">Requirement</span></span> | <span data-ttu-id="4f07b-119">Value</span><span class="sxs-lookup"><span data-stu-id="4f07b-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="4f07b-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4f07b-120">Minimum supported client</span></span><br/> | <span data-ttu-id="4f07b-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="4f07b-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="4f07b-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4f07b-122">Minimum supported server</span></span><br/> | <span data-ttu-id="4f07b-123">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="4f07b-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




