---
description: La función de Desregistro de exportación libera los recursos usados para crear la base de datos de propiedades de protocolo. El archivo DLL del analizador debe implementar Unregister.
ms.assetid: 80852aed-07aa-440f-a537-f6cce461292e
title: Anular el registro de la función de devolución de llamada (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Deregister
api_type:
- UserDefined
api_location:
- Netmon.h
ms.openlocfilehash: 9458ff74f29cd8eb7a75da0a3628a2dd1519ba43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276695"
---
# <a name="deregister-callback-function"></a><span data-ttu-id="aae76-104">Anular la función de devolución de llamada</span><span class="sxs-lookup"><span data-stu-id="aae76-104">Deregister callback function</span></span>

<span data-ttu-id="aae76-105">La función de **Desregistro** de exportación libera los recursos usados para crear la [*base de datos de propiedades*](p.md)de protocolo.</span><span class="sxs-lookup"><span data-stu-id="aae76-105">The **Deregister** export function frees the resources used to create the protocol [*property database*](p.md).</span></span> <span data-ttu-id="aae76-106">El archivo DLL del analizador debe implementar **unregister**.</span><span class="sxs-lookup"><span data-stu-id="aae76-106">The parser DLL must implement **Deregister**.</span></span>

## <a name="syntax"></a><span data-ttu-id="aae76-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="aae76-107">Syntax</span></span>


```C++
VOID Deregister(
  _In_ HPROTOCOL hProtocol
);
```



## <a name="parameters"></a><span data-ttu-id="aae76-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="aae76-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aae76-109">*hProtocol* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="aae76-109">*hProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aae76-110">Identificador del protocolo para una base de datos específica.</span><span class="sxs-lookup"><span data-stu-id="aae76-110">Handle of the protocol for a specific database.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aae76-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="aae76-111">Return value</span></span>

<span data-ttu-id="aae76-112">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="aae76-112">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="aae76-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="aae76-113">Remarks</span></span>

<span data-ttu-id="aae76-114">Monitor de red llama a **anular registro** después de pasar toda la información de captura a la dll del analizador.</span><span class="sxs-lookup"><span data-stu-id="aae76-114">Network Monitor calls **Deregister** after passing all the capture information to the parser DLL.</span></span> <span data-ttu-id="aae76-115">El archivo DLL del analizador debe implementar una función de **eliminación de registro** para cada protocolo que admita el analizador.</span><span class="sxs-lookup"><span data-stu-id="aae76-115">The parser DLL must implement a **Deregister** function for each protocol that the parser supports.</span></span>

<span data-ttu-id="aae76-116">Al implementar **unregister**, el archivo DLL del analizador debe llamar a la función [DestroyPropertyDatabase](destroypropertydatabase.md) para liberar los recursos de la [*base de datos de propiedades*](p.md) .</span><span class="sxs-lookup"><span data-stu-id="aae76-116">When implementing **Deregister**, the parser DLL must call the [DestroyPropertyDatabase](destroypropertydatabase.md) function to release the [*property database*](p.md) resources.</span></span>



| <span data-ttu-id="aae76-117">Para obtener información acerca de</span><span class="sxs-lookup"><span data-stu-id="aae76-117">For information on</span></span>                                        | <span data-ttu-id="aae76-118">Vea</span><span class="sxs-lookup"><span data-stu-id="aae76-118">See</span></span>                                                    |
|-----------------------------------------------------------|--------------------------------------------------------|
| <span data-ttu-id="aae76-119">Qué son los analizadores y cómo funcionan con Monitor de red.</span><span class="sxs-lookup"><span data-stu-id="aae76-119">What parsers are, and how they work with Network Monitor.</span></span> | [<span data-ttu-id="aae76-120">Analizadores</span><span class="sxs-lookup"><span data-stu-id="aae76-120">Parsers</span></span>](parsers.md)                                 |
| <span data-ttu-id="aae76-121">Qué puntos de entrada se incluyen en el archivo DLL del analizador.</span><span class="sxs-lookup"><span data-stu-id="aae76-121">Which entry points are included in the parser DLL.</span></span>        | [<span data-ttu-id="aae76-122">Arquitectura de DLL de analizador</span><span class="sxs-lookup"><span data-stu-id="aae76-122">Parser DLL Architecture</span></span>](parser-dll-architecture.md) |
| <span data-ttu-id="aae76-123">Cómo implementar **unregister**  incluye un ejemplo.</span><span class="sxs-lookup"><span data-stu-id="aae76-123">How to implement **Deregister**  includes an example.</span></span>     | [<span data-ttu-id="aae76-124">Implementación de unregister</span><span class="sxs-lookup"><span data-stu-id="aae76-124">Implementing Deregister</span></span>](implementing-deregister.md) |



 

## <a name="requirements"></a><span data-ttu-id="aae76-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="aae76-125">Requirements</span></span>



| <span data-ttu-id="aae76-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="aae76-126">Requirement</span></span> | <span data-ttu-id="aae76-127">Value</span><span class="sxs-lookup"><span data-stu-id="aae76-127">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="aae76-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="aae76-128">Minimum supported client</span></span><br/> | <span data-ttu-id="aae76-129">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="aae76-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="aae76-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="aae76-130">Minimum supported server</span></span><br/> | <span data-ttu-id="aae76-131">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="aae76-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="aae76-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="aae76-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="aae76-133"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="aae76-133"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aae76-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="aae76-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aae76-135">DestroyPropertyDatabase</span><span class="sxs-lookup"><span data-stu-id="aae76-135">DestroyPropertyDatabase</span></span>](destroypropertydatabase.md)
</dt> </dl>

 

 




