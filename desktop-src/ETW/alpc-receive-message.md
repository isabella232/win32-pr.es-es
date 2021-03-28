---
description: Esta clase es la clase de tipo de evento de los eventos de recepción de mensajes de ALPC. La siguiente sintaxis se simplifica desde el código MOF.
ms.assetid: 6aa98240-e559-47b6-ae55-5a6379e08077
title: ALPC_Receive_Message (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ALPC_Receive_Message
- ALPC_Receive_Message.MessageID
api_type:
- NA
api_location: ''
ms.openlocfilehash: 886d3595caa283d5b09939a506952633d2350d41
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984534"
---
# <a name="alpc_receive_message-class"></a><span data-ttu-id="8bbfd-104">ALPC \_ Receive ( \_ clase de mensaje)</span><span class="sxs-lookup"><span data-stu-id="8bbfd-104">ALPC\_Receive\_Message class</span></span>

<span data-ttu-id="8bbfd-105">Esta clase es la clase de tipo de evento de los eventos de recepción de mensajes de ALPC.</span><span class="sxs-lookup"><span data-stu-id="8bbfd-105">This class is the event type class for ALPC receive message events.</span></span>

<span data-ttu-id="8bbfd-106">La siguiente sintaxis se simplifica desde el código MOF.</span><span class="sxs-lookup"><span data-stu-id="8bbfd-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="8bbfd-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8bbfd-107">Syntax</span></span>

``` syntax
[EventType(34), EventTypeName("ALPC-Receive-Message")]
class ALPC_Receive_Message : ALPC
{
  uint32 MessageID;
};
```

## <a name="members"></a><span data-ttu-id="8bbfd-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="8bbfd-108">Members</span></span>

<span data-ttu-id="8bbfd-109">La clase de **\_ \_ mensaje ALPC Receive** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="8bbfd-109">The **ALPC\_Receive\_Message** class has these types of members:</span></span>

-   [<span data-ttu-id="8bbfd-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="8bbfd-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8bbfd-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="8bbfd-111">Properties</span></span>

<span data-ttu-id="8bbfd-112">La clase de **\_ \_ mensaje ALPC Receive** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="8bbfd-112">The **ALPC\_Receive\_Message** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8bbfd-113">**Identificador**</span><span class="sxs-lookup"><span data-stu-id="8bbfd-113">**MessageID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8bbfd-114">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8bbfd-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8bbfd-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8bbfd-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8bbfd-116">Identificador de mensaje.</span><span class="sxs-lookup"><span data-stu-id="8bbfd-116">Message identifier.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8bbfd-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8bbfd-117">Requirements</span></span>



| <span data-ttu-id="8bbfd-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="8bbfd-118">Requirement</span></span> | <span data-ttu-id="8bbfd-119">Value</span><span class="sxs-lookup"><span data-stu-id="8bbfd-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="8bbfd-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8bbfd-120">Minimum supported client</span></span><br/> | <span data-ttu-id="8bbfd-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="8bbfd-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="8bbfd-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8bbfd-122">Minimum supported server</span></span><br/> | <span data-ttu-id="8bbfd-123">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="8bbfd-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




