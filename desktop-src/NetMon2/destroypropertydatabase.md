---
description: La función DestroyPropertyDatabase libera los recursos usados para crear la base de datos de propiedades de protocolo.
ms.assetid: a0d1c416-8b08-47ca-a88e-e70588574376
title: Función DestroyPropertyDatabase (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DestroyPropertyDatabase
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: baedae22e948b38d9ff162942269ac4529896826
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002853"
---
# <a name="destroypropertydatabase-function"></a><span data-ttu-id="9d21d-103">DestroyPropertyDatabase función)</span><span class="sxs-lookup"><span data-stu-id="9d21d-103">DestroyPropertyDatabase function</span></span>

<span data-ttu-id="9d21d-104">La función **DestroyPropertyDatabase** libera los recursos usados para crear la [*base de datos de propiedades*](p.md)de protocolo.</span><span class="sxs-lookup"><span data-stu-id="9d21d-104">The **DestroyPropertyDatabase** function releases the resources used to create the protocol [*property database*](p.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="9d21d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9d21d-105">Syntax</span></span>


```C++
DWORD WINAPI DestroyPropertyDatabase(
  _In_ HPROTOCOL hProtocol
);
```



## <a name="parameters"></a><span data-ttu-id="9d21d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9d21d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9d21d-107">*hProtocol* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="9d21d-107">*hProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9d21d-108">Identificador de la base de datos de propiedades que se va a destruir.</span><span class="sxs-lookup"><span data-stu-id="9d21d-108">Handle to the property database to be destroyed.</span></span> <span data-ttu-id="9d21d-109">El identificador se pasa a la DLL del analizador cuando Monitor de red llama a la función de [anulación del registro](deregister.md) .</span><span class="sxs-lookup"><span data-stu-id="9d21d-109">The handle is passed to the parser DLL when Network Monitor calls the [Deregister](deregister.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9d21d-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9d21d-110">Return value</span></span>

<span data-ttu-id="9d21d-111">Si la función se realiza correctamente, el valor devuelto es NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="9d21d-111">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="9d21d-112">Si la función no es correcta, el valor devuelto es un código de error.</span><span class="sxs-lookup"><span data-stu-id="9d21d-112">If the function is unsuccessful, the return value is an error code.</span></span>



| <span data-ttu-id="9d21d-113">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="9d21d-113">Return code</span></span>                                                                                              | <span data-ttu-id="9d21d-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="9d21d-114">Description</span></span>                                |
|----------------------------------------------------------------------------------------------------------|--------------------------------------------|
| <dl> <span data-ttu-id="9d21d-115"><dt>**\_error interno de NMERR \_**</dt></span><span class="sxs-lookup"><span data-stu-id="9d21d-115"><dt>**NMERR\_INTERNAL\_ERROR**</dt></span></span> </dl>    | <span data-ttu-id="9d21d-116">Se ha producido un error interno.</span><span class="sxs-lookup"><span data-stu-id="9d21d-116">An internal error occurred.</span></span> <br/>    |
| <dl> <span data-ttu-id="9d21d-117"><dt>**NMERR \_ no válido \_ HPROTOCOL**</dt></span><span class="sxs-lookup"><span data-stu-id="9d21d-117"><dt>**NMERR\_INVALID\_HPROTOCOL**</dt></span></span> </dl> | <span data-ttu-id="9d21d-118">Identificador no válido en *hProtocol*.</span><span class="sxs-lookup"><span data-stu-id="9d21d-118">Invalid handle in *hProtocol*.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="9d21d-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9d21d-119">Remarks</span></span>

<span data-ttu-id="9d21d-120">Solo se debe llamar a la función **DestroyPropertyDatabase** cuando se implementa la función de exportación de [anulación del registro](deregister.md) para el protocolo.</span><span class="sxs-lookup"><span data-stu-id="9d21d-120">The **DestroyPropertyDatabase** function should be called only when implementing the [Deregister](deregister.md) export function for the protocol.</span></span> <span data-ttu-id="9d21d-121">En el caso de los archivos dll de analizador que admiten varios protocolos, se llama a la función **DestroyPropertyDatabase** para cada implementación de **unregister**.</span><span class="sxs-lookup"><span data-stu-id="9d21d-121">For parser DLLs that support multiple protocols, the **DestroyPropertyDatabase** function is called for each implementation of **Deregister**.</span></span>



| <span data-ttu-id="9d21d-122">Para obtener información acerca de</span><span class="sxs-lookup"><span data-stu-id="9d21d-122">For information on</span></span>                                        | <span data-ttu-id="9d21d-123">Vea</span><span class="sxs-lookup"><span data-stu-id="9d21d-123">See</span></span>                                                    |
|-----------------------------------------------------------|--------------------------------------------------------|
| <span data-ttu-id="9d21d-124">Qué son los analizadores y cómo funcionan con Monitor de red.</span><span class="sxs-lookup"><span data-stu-id="9d21d-124">What parsers are, and how they work with Network Monitor.</span></span> | [<span data-ttu-id="9d21d-125">Analizadores</span><span class="sxs-lookup"><span data-stu-id="9d21d-125">Parsers</span></span>](parsers.md)                                 |
| <span data-ttu-id="9d21d-126">Qué puntos de entrada se incluyen en el archivo DLL del analizador.</span><span class="sxs-lookup"><span data-stu-id="9d21d-126">Which entry points are included in the parser DLL.</span></span>        | [<span data-ttu-id="9d21d-127">Arquitectura de DLL de analizador</span><span class="sxs-lookup"><span data-stu-id="9d21d-127">Parser DLL Architecture</span></span>](parser-dll-architecture.md) |
| <span data-ttu-id="9d21d-128">Cómo implementar **unregister**  incluye un ejemplo.</span><span class="sxs-lookup"><span data-stu-id="9d21d-128">How to implement **Deregister**  includes an example.</span></span>     | [<span data-ttu-id="9d21d-129">Implementación de unregister</span><span class="sxs-lookup"><span data-stu-id="9d21d-129">Implementing Deregister</span></span>](implementing-deregister.md) |



 

## <a name="requirements"></a><span data-ttu-id="9d21d-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9d21d-130">Requirements</span></span>



| <span data-ttu-id="9d21d-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="9d21d-131">Requirement</span></span> | <span data-ttu-id="9d21d-132">Value</span><span class="sxs-lookup"><span data-stu-id="9d21d-132">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="9d21d-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9d21d-133">Minimum supported client</span></span><br/> | <span data-ttu-id="9d21d-134">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="9d21d-134">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="9d21d-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9d21d-135">Minimum supported server</span></span><br/> | <span data-ttu-id="9d21d-136">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="9d21d-136">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="9d21d-137">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9d21d-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="9d21d-138"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="9d21d-138"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="9d21d-139">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9d21d-139">Library</span></span><br/>                  | <dl> <span data-ttu-id="9d21d-140"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9d21d-140"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="9d21d-141">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="9d21d-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9d21d-142"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9d21d-142"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9d21d-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="9d21d-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d21d-144">Eliminar registro</span><span class="sxs-lookup"><span data-stu-id="9d21d-144">Deregister</span></span>](deregister.md)
</dt> </dl>

 

 




