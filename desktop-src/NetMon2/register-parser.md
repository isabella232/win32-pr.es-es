---
description: La función de exportación de registros debe implementarse en todos los archivos dll de analizador. La implementación de Register crea y rellena en una base de datos de propiedades para un protocolo. Monitor de red usa la base de datos para determinar las propiedades que admite el protocolo.
ms.assetid: b8a2752d-30a6-48f2-90b3-b1430ae983d2
title: Función de devolución de llamada del analizador de registro (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Register
api_type:
- UserDefined
api_location:
- Netmon.h
ms.openlocfilehash: bc49cc083cf6ba46594473a041d9a1ad138efa22
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677642"
---
# <a name="register-parser-callback-function"></a><span data-ttu-id="5fc2e-105">Registrar función de devolución de llamada del analizador</span><span class="sxs-lookup"><span data-stu-id="5fc2e-105">Register Parser callback function</span></span>

<span data-ttu-id="5fc2e-106">La función de exportación de **registros** debe implementarse en todos los archivos dll de analizador.</span><span class="sxs-lookup"><span data-stu-id="5fc2e-106">The **Register** export function must be implemented in all parser DLLs.</span></span> <span data-ttu-id="5fc2e-107">La implementación de **Register** crea y rellena en una base de [*datos de propiedades*](p.md) para un protocolo.</span><span class="sxs-lookup"><span data-stu-id="5fc2e-107">The implementation of **Register** creates and fills-in a [*property database*](p.md) for a protocol.</span></span> <span data-ttu-id="5fc2e-108">Monitor de red usa la base de datos para determinar las propiedades que admite el protocolo.</span><span class="sxs-lookup"><span data-stu-id="5fc2e-108">Network Monitor uses the database to determine which properties the protocol supports.</span></span>

## <a name="syntax"></a><span data-ttu-id="5fc2e-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5fc2e-109">Syntax</span></span>


```C++
VOID Register(
  _In_ HPROTOCOL hProtocol
);
```



## <a name="parameters"></a><span data-ttu-id="5fc2e-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5fc2e-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5fc2e-111">*hProtocol* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="5fc2e-111">*hProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5fc2e-112">Identificador del protocolo que Monitor de red proporciona al llamar a **Register**.</span><span class="sxs-lookup"><span data-stu-id="5fc2e-112">The handle of the protocol that Network Monitor provides when calling **Register**.</span></span> <span data-ttu-id="5fc2e-113">El identificador *hProtocol* es necesario cuando se llama a funciones auxiliares de exportación.</span><span class="sxs-lookup"><span data-stu-id="5fc2e-113">The *hProtocol* handle is needed when calling export helper functions.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5fc2e-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5fc2e-114">Return value</span></span>

<span data-ttu-id="5fc2e-115">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="5fc2e-115">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="5fc2e-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5fc2e-116">Remarks</span></span>

<span data-ttu-id="5fc2e-117">Monitor de red comienza a llamar a la función **Register** en cuanto se carga una captura.</span><span class="sxs-lookup"><span data-stu-id="5fc2e-117">Network Monitor starts calling the **Register** function as soon as a capture is loaded.</span></span> <span data-ttu-id="5fc2e-118">Monitor de red llama a la función de **registro** para cada protocolo que puede identificar.</span><span class="sxs-lookup"><span data-stu-id="5fc2e-118">Network Monitor calls the **Register** function for each protocol it can identify.</span></span> <span data-ttu-id="5fc2e-119">La función [CreateProtocol](createprotocol.md) pasa un puntero a la función de **registro** .</span><span class="sxs-lookup"><span data-stu-id="5fc2e-119">The [CreateProtocol](createprotocol.md) function passes a pointer to the **Register** function.</span></span>

<span data-ttu-id="5fc2e-120">La implementación de **Register** incluye llamadas a las siguientes funciones.</span><span class="sxs-lookup"><span data-stu-id="5fc2e-120">The implementation of **Register** includes calls to the following functions.</span></span>

-   <span data-ttu-id="5fc2e-121">Una llamada a las funciones [CreatePropertyDatabase](createpropertydatabase.md) y [AddProperty](/previous-versions/bb251873(v=msdn.10)) para crear una base de datos de todas las propiedades que admite el protocolo.</span><span class="sxs-lookup"><span data-stu-id="5fc2e-121">A call to the [CreatePropertyDatabase](createpropertydatabase.md) and [AddProperty](/previous-versions/bb251873(v=msdn.10)) functions to create a database of all the properties that the protocol supports.</span></span>
-   <span data-ttu-id="5fc2e-122">Se requiere una llamada a la función [CreateHandoffTable](createhandofftable.md) si el protocolo utiliza un [*conjunto de entrega*](h.md).</span><span class="sxs-lookup"><span data-stu-id="5fc2e-122">A call to the [CreateHandoffTable](createhandofftable.md) function is required if the protocol uses a [*handoff set*](h.md).</span></span>

<span data-ttu-id="5fc2e-123">Si el archivo DLL del analizador contiene varios analizadores y el analizador puede detectar más de un protocolo, debe implementar una función de **registro** para cada protocolo.</span><span class="sxs-lookup"><span data-stu-id="5fc2e-123">If the parser DLL contains multiple parsers, and the parser can detect more than one protocol, you must implement a **Register** function for each protocol.</span></span>



| <span data-ttu-id="5fc2e-124">Para obtener información sobre</span><span class="sxs-lookup"><span data-stu-id="5fc2e-124">For Information on</span></span>                                        | <span data-ttu-id="5fc2e-125">Vea</span><span class="sxs-lookup"><span data-stu-id="5fc2e-125">See</span></span>                                                    |
|-----------------------------------------------------------|--------------------------------------------------------|
| <span data-ttu-id="5fc2e-126">Qué son los analizadores y cómo funcionan con Monitor de red.</span><span class="sxs-lookup"><span data-stu-id="5fc2e-126">What parsers are, and how they work with Network Monitor.</span></span> | [<span data-ttu-id="5fc2e-127">Analizadores</span><span class="sxs-lookup"><span data-stu-id="5fc2e-127">Parsers</span></span>](parsers.md)                                 |
| <span data-ttu-id="5fc2e-128">Qué puntos de entrada se incluyen en el archivo DLL del analizador.</span><span class="sxs-lookup"><span data-stu-id="5fc2e-128">Which entry points are included in the parser DLL.</span></span>        | [<span data-ttu-id="5fc2e-129">Arquitectura de DLL de analizador</span><span class="sxs-lookup"><span data-stu-id="5fc2e-129">Parser DLL Architecture</span></span>](parser-dll-architecture.md) |
| <span data-ttu-id="5fc2e-130">Cómo implementar **el registro**  incluye un ejemplo.</span><span class="sxs-lookup"><span data-stu-id="5fc2e-130">How to implement **Register**  includes an example.</span></span>       | [<span data-ttu-id="5fc2e-131">Implementación del registro</span><span class="sxs-lookup"><span data-stu-id="5fc2e-131">Implementing Register</span></span>](implementing-register.md)     |



 

## <a name="requirements"></a><span data-ttu-id="5fc2e-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5fc2e-132">Requirements</span></span>



| <span data-ttu-id="5fc2e-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="5fc2e-133">Requirement</span></span> | <span data-ttu-id="5fc2e-134">Value</span><span class="sxs-lookup"><span data-stu-id="5fc2e-134">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="5fc2e-135">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5fc2e-135">Minimum supported client</span></span><br/> | <span data-ttu-id="5fc2e-136">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="5fc2e-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="5fc2e-137">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5fc2e-137">Minimum supported server</span></span><br/> | <span data-ttu-id="5fc2e-138">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="5fc2e-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="5fc2e-139">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5fc2e-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="5fc2e-140"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="5fc2e-140"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5fc2e-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="5fc2e-141">See also</span></span>

<dl> <dt>

<span data-ttu-id="5fc2e-142">[AddProperty](/previous-versions/bb251873(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="5fc2e-142">[AddProperty](/previous-versions/bb251873(v=msdn.10))</span></span>
</dt> <dt>

[<span data-ttu-id="5fc2e-143">CreateHandoffTable</span><span class="sxs-lookup"><span data-stu-id="5fc2e-143">CreateHandoffTable</span></span>](createhandofftable.md)
</dt> <dt>

[<span data-ttu-id="5fc2e-144">CreatePropertyDatabase</span><span class="sxs-lookup"><span data-stu-id="5fc2e-144">CreatePropertyDatabase</span></span>](createpropertydatabase.md)
</dt> <dt>

[<span data-ttu-id="5fc2e-145">CreateProtocol</span><span class="sxs-lookup"><span data-stu-id="5fc2e-145">CreateProtocol</span></span>](createprotocol.md)
</dt> </dl>

 

