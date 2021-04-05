---
description: La estructura ENTRYPOINTS define los puntos de entrada a las funciones de exportación que Monitor de red utiliza para operar el analizador.
ms.assetid: e2ac118d-e04b-489f-877f-84cc9888f8af
title: Estructura ENTRYPOINTS (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ENTRYPOINTS
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 3eebee878cd907ee20674224a969c82038f4ac6b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000946"
---
# <a name="entrypoints-structure"></a><span data-ttu-id="4ce55-103">Estructura ENTRYPOINTS</span><span class="sxs-lookup"><span data-stu-id="4ce55-103">ENTRYPOINTS structure</span></span>

<span data-ttu-id="4ce55-104">La estructura **ENTRYPOINTS** define los puntos de entrada a las funciones de exportación que monitor de red utiliza para operar el analizador.</span><span class="sxs-lookup"><span data-stu-id="4ce55-104">The **ENTRYPOINTS** structure defines the entry points to the export functions that Network Monitor uses to operate the parser.</span></span>

## <a name="syntax"></a><span data-ttu-id="4ce55-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4ce55-105">Syntax</span></span>


```C++
typedef struct __ENTRYPOINTS {
  REGISTER         Register;
  DEREGISTER       Deregister;
  RECOGNIZEFRAME   RecognizeFrame;
  ATTACHPROPERTIES AttachProperties;
  FORMATPROPERTIES FormatProperties;
} ENTRYPOINTS, *LPENTRYPOINTS;
```



## <a name="members"></a><span data-ttu-id="4ce55-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="4ce55-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="4ce55-107">**Registro**</span><span class="sxs-lookup"><span data-stu-id="4ce55-107">**Register**</span></span>
</dt> <dd>

<span data-ttu-id="4ce55-108">Puntero a la implementación de la función [*Register Expert*](register-expert.md) .</span><span class="sxs-lookup"><span data-stu-id="4ce55-108">Pointer to the implementation of the [*Register expert*](register-expert.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="4ce55-109">**Eliminar registro**</span><span class="sxs-lookup"><span data-stu-id="4ce55-109">**Deregister**</span></span>
</dt> <dd>

<span data-ttu-id="4ce55-110">Puntero a la implementación de la función de [**eliminación de registro**](deregister.md) .</span><span class="sxs-lookup"><span data-stu-id="4ce55-110">Pointer to the implementation of the [**Deregister**](deregister.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="4ce55-111">**RecognizeFrame**</span><span class="sxs-lookup"><span data-stu-id="4ce55-111">**RecognizeFrame**</span></span>
</dt> <dd>

<span data-ttu-id="4ce55-112">Puntero a la implementación de la función de exportación [**RecognizeFrame**](recognizeframe.md) .</span><span class="sxs-lookup"><span data-stu-id="4ce55-112">Pointer to the implementation of the [**RecognizeFrame**](recognizeframe.md) export function.</span></span>

</dd> <dt>

<span data-ttu-id="4ce55-113">**AttachProperties**</span><span class="sxs-lookup"><span data-stu-id="4ce55-113">**AttachProperties**</span></span>
</dt> <dd>

<span data-ttu-id="4ce55-114">Puntero a la implementación de la función de exportación [**AttachProperties**](attachproperties.md) .</span><span class="sxs-lookup"><span data-stu-id="4ce55-114">Pointer to the implementation of the [**AttachProperties**](attachproperties.md) export function.</span></span>

</dd> <dt>

<span data-ttu-id="4ce55-115">**FormatProperties**</span><span class="sxs-lookup"><span data-stu-id="4ce55-115">**FormatProperties**</span></span>
</dt> <dd>

<span data-ttu-id="4ce55-116">Puntero a la implementación de la función de exportación [**FormatProperties**](formatproperties.md) .</span><span class="sxs-lookup"><span data-stu-id="4ce55-116">Pointer to the implementation of the [**FormatProperties**](formatproperties.md) export function.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4ce55-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4ce55-117">Remarks</span></span>

<span data-ttu-id="4ce55-118">La función **CreateProtocol** utiliza la estructura **ENTRYPOINTS** para proporcionar punteros a monitor de red.</span><span class="sxs-lookup"><span data-stu-id="4ce55-118">The **CreateProtocol** function uses the **ENTRYPOINTS** structure to provide pointers to Network Monitor.</span></span> <span data-ttu-id="4ce55-119">Los punteros se deben especificar en el orden identificado en la sección de miembros anteriores.</span><span class="sxs-lookup"><span data-stu-id="4ce55-119">The pointers must be specified in the order identified in the previous Members section.</span></span>

<span data-ttu-id="4ce55-120">No es necesario implementar la función [**FormatProperties**](formatproperties.md) si monitor de red nunca mostrará los datos del protocolo.</span><span class="sxs-lookup"><span data-stu-id="4ce55-120">The [**FormatProperties**](formatproperties.md) function does not need to be implemented if Network Monitor will never display the protocol data.</span></span> <span data-ttu-id="4ce55-121">Por ejemplo, no es necesario implementar **FormatProperties** si una aplicación de exportación usa la salida del analizador y monitor de red no muestra la salida.</span><span class="sxs-lookup"><span data-stu-id="4ce55-121">For example, **FormatProperties** does not need to be implemented if an export application uses the output from the parser, and Network Monitor does not display the output.</span></span>



| <span data-ttu-id="4ce55-122">Para obtener información acerca de</span><span class="sxs-lookup"><span data-stu-id="4ce55-122">For information on</span></span>                                        | <span data-ttu-id="4ce55-123">Vea</span><span class="sxs-lookup"><span data-stu-id="4ce55-123">See</span></span>                                                     |
|-----------------------------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="4ce55-124">Qué son los analizadores y cómo funcionan con Monitor de red.</span><span class="sxs-lookup"><span data-stu-id="4ce55-124">What parsers are, and how they work with Network Monitor.</span></span> | [<span data-ttu-id="4ce55-125">Analizadores</span><span class="sxs-lookup"><span data-stu-id="4ce55-125">Parsers</span></span>](parsers.md)                                  |
| <span data-ttu-id="4ce55-126">Cómo implementar **DllMain**  incluye un ejemplo.</span><span class="sxs-lookup"><span data-stu-id="4ce55-126">How to implement **DllMain**  includes an example.</span></span>        | [<span data-ttu-id="4ce55-127">Implementar DllMain</span><span class="sxs-lookup"><span data-stu-id="4ce55-127">Implementing DllMain</span></span>](implementing-dllmain-parser.md) |



 

## <a name="requirements"></a><span data-ttu-id="4ce55-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4ce55-128">Requirements</span></span>



| <span data-ttu-id="4ce55-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="4ce55-129">Requirement</span></span> | <span data-ttu-id="4ce55-130">Value</span><span class="sxs-lookup"><span data-stu-id="4ce55-130">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="4ce55-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4ce55-131">Minimum supported client</span></span><br/> | <span data-ttu-id="4ce55-132">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="4ce55-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="4ce55-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4ce55-133">Minimum supported server</span></span><br/> | <span data-ttu-id="4ce55-134">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="4ce55-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="4ce55-135">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4ce55-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="4ce55-136"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="4ce55-136"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4ce55-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="4ce55-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ce55-138">AttachProperties</span><span class="sxs-lookup"><span data-stu-id="4ce55-138">AttachProperties</span></span>](attachproperties.md)
</dt> <dt>

[<span data-ttu-id="4ce55-139">CreateProtocol</span><span class="sxs-lookup"><span data-stu-id="4ce55-139">CreateProtocol</span></span>](createprotocol.md)
</dt> <dt>

[<span data-ttu-id="4ce55-140">Eliminar registro</span><span class="sxs-lookup"><span data-stu-id="4ce55-140">Deregister</span></span>](deregister.md)
</dt> <dt>

[<span data-ttu-id="4ce55-141">FormatProperties</span><span class="sxs-lookup"><span data-stu-id="4ce55-141">FormatProperties</span></span>](formatproperties.md)
</dt> <dt>

[<span data-ttu-id="4ce55-142">RecognizeFrame</span><span class="sxs-lookup"><span data-stu-id="4ce55-142">RecognizeFrame</span></span>](recognizeframe.md)
</dt> <dt>

[<span data-ttu-id="4ce55-143">Registro</span><span class="sxs-lookup"><span data-stu-id="4ce55-143">Register</span></span>](register-parser.md)
</dt> </dl>

 

 




