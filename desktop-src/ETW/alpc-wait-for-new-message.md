---
description: Esta clase es la clase de tipo de evento para la espera ALPC para los nuevos eventos de mensaje. La siguiente sintaxis se simplifica desde el código MOF.
ms.assetid: 7f7fa4b8-ed12-49a0-a84e-37f66af4f5f1
title: ALPC_Wait_For_New_Message (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ALPC_Wait_For_New_Message
- ALPC_Wait_For_New_Message.IsServerPort
- ALPC_Wait_For_New_Message.PortName
api_type:
- NA
api_location: ''
ms.openlocfilehash: 75cbda11a2a27eec811f8ff47966d12c6a86cf07
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984527"
---
# <a name="alpc_wait_for_new_message-class"></a><span data-ttu-id="e93d3-104">ALPC- \_ esperar \_ para la \_ nueva clase de \_ mensaje</span><span class="sxs-lookup"><span data-stu-id="e93d3-104">ALPC\_Wait\_For\_New\_Message class</span></span>

<span data-ttu-id="e93d3-105">Esta clase es la clase de tipo de evento para la espera ALPC para los nuevos eventos de mensaje.</span><span class="sxs-lookup"><span data-stu-id="e93d3-105">This class is the event type class for ALPC wait for new message events.</span></span>

<span data-ttu-id="e93d3-106">La siguiente sintaxis se simplifica desde el código MOF.</span><span class="sxs-lookup"><span data-stu-id="e93d3-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="e93d3-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e93d3-107">Syntax</span></span>

``` syntax
[EventType(36), EventTypeName("ALPC-Wait-For-New-Message")]
class ALPC_Wait_For_New_Message : ALPC
{
  uint32 IsServerPort;
  string PortName;
};
```

## <a name="members"></a><span data-ttu-id="e93d3-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="e93d3-108">Members</span></span>

<span data-ttu-id="e93d3-109">La **nueva clase de \_ mensaje ALPC wait \_ for \_ New \_ Message** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="e93d3-109">The **ALPC\_Wait\_For\_New\_Message** class has these types of members:</span></span>

-   [<span data-ttu-id="e93d3-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e93d3-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e93d3-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e93d3-111">Properties</span></span>

<span data-ttu-id="e93d3-112">La **\_ nueva clase \_ de mensaje ALPC wait for \_ New \_ Message** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="e93d3-112">The **ALPC\_Wait\_For\_New\_Message** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e93d3-113">**IsServerPort**</span><span class="sxs-lookup"><span data-stu-id="e93d3-113">**IsServerPort**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e93d3-114">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e93d3-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e93d3-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e93d3-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e93d3-116">Indica si el puerto es un puerto de servidor.</span><span class="sxs-lookup"><span data-stu-id="e93d3-116">Indicates if the port is a server port.</span></span>

</dd> <dt>

<span data-ttu-id="e93d3-117">**PortName**</span><span class="sxs-lookup"><span data-stu-id="e93d3-117">**PortName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e93d3-118">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e93d3-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e93d3-119">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e93d3-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e93d3-120">Cadena que contiene el nombre del puerto en el que se está esperando ALPC.</span><span class="sxs-lookup"><span data-stu-id="e93d3-120">String that contains the name of the port on which ALPC is waiting.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e93d3-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e93d3-121">Requirements</span></span>



| <span data-ttu-id="e93d3-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="e93d3-122">Requirement</span></span> | <span data-ttu-id="e93d3-123">Value</span><span class="sxs-lookup"><span data-stu-id="e93d3-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="e93d3-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e93d3-124">Minimum supported client</span></span><br/> | <span data-ttu-id="e93d3-125">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="e93d3-125">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="e93d3-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e93d3-126">Minimum supported server</span></span><br/> | <span data-ttu-id="e93d3-127">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="e93d3-127">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




