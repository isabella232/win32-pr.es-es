---
description: Esta clase es la clase de tipo de evento para los eventos de envío de mensajes ALPC. La siguiente sintaxis se simplifica desde el código MOF.
ms.assetid: 7f12259b-f737-4bef-9dea-2ffe3517e0da
title: ALPC_Send_Message (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ALPC_Send_Message
- ALPC_Send_Message.MessageID
api_type:
- NA
api_location: ''
ms.openlocfilehash: c9437626341f0ac57136645d40a8389436e8af1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154853"
---
# <a name="alpc_send_message-class"></a><span data-ttu-id="39ae4-104">ALPC \_ send \_ Message (clase)</span><span class="sxs-lookup"><span data-stu-id="39ae4-104">ALPC\_Send\_Message class</span></span>

<span data-ttu-id="39ae4-105">Esta clase es la clase de tipo de evento para los eventos de envío de mensajes ALPC.</span><span class="sxs-lookup"><span data-stu-id="39ae4-105">This class is the event type class for ALPC send message events.</span></span>

<span data-ttu-id="39ae4-106">La siguiente sintaxis se simplifica desde el código MOF.</span><span class="sxs-lookup"><span data-stu-id="39ae4-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="39ae4-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="39ae4-107">Syntax</span></span>

``` syntax
[EventType(33), EventTypeName("ALPC-Send-Message")]
class ALPC_Send_Message : ALPC
{
  uint32 MessageID;
};
```

## <a name="members"></a><span data-ttu-id="39ae4-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="39ae4-108">Members</span></span>

<span data-ttu-id="39ae4-109">La clase de **\_ \_ mensaje ALPC Send** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="39ae4-109">The **ALPC\_Send\_Message** class has these types of members:</span></span>

-   [<span data-ttu-id="39ae4-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="39ae4-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="39ae4-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="39ae4-111">Properties</span></span>

<span data-ttu-id="39ae4-112">La clase de **\_ \_ mensaje ALPC Send** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="39ae4-112">The **ALPC\_Send\_Message** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="39ae4-113">**Identificador**</span><span class="sxs-lookup"><span data-stu-id="39ae4-113">**MessageID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39ae4-114">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="39ae4-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="39ae4-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="39ae4-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="39ae4-116">Identificador de mensaje.</span><span class="sxs-lookup"><span data-stu-id="39ae4-116">Message identifier.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="39ae4-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="39ae4-117">Requirements</span></span>



| <span data-ttu-id="39ae4-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="39ae4-118">Requirement</span></span> | <span data-ttu-id="39ae4-119">Value</span><span class="sxs-lookup"><span data-stu-id="39ae4-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="39ae4-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="39ae4-120">Minimum supported client</span></span><br/> | <span data-ttu-id="39ae4-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="39ae4-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="39ae4-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="39ae4-122">Minimum supported server</span></span><br/> | <span data-ttu-id="39ae4-123">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="39ae4-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




