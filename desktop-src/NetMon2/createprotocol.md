---
description: La función CreateProtocol notifica a Monitor de red que existe un analizador de protocolo específico.
ms.assetid: 13ae261f-b1c0-4afc-b718-d64b3d4ec5ee
title: Función CreateProtocol (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreateProtocol
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 0b35f9505758256750ae02d24d6c2a84ed0646b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104156704"
---
# <a name="createprotocol-function"></a><span data-ttu-id="649f2-103">CreateProtocol función)</span><span class="sxs-lookup"><span data-stu-id="649f2-103">CreateProtocol function</span></span>

<span data-ttu-id="649f2-104">La función **CreateProtocol** notifica a monitor de red que existe un analizador de protocolo específico.</span><span class="sxs-lookup"><span data-stu-id="649f2-104">The **CreateProtocol** function notifies Network Monitor that a specific protocol parser exists.</span></span>

## <a name="syntax"></a><span data-ttu-id="649f2-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="649f2-105">Syntax</span></span>


```C++
HPROTOCOL WINAPI CreateProtocol(
  _In_ LPSTR         ProtocolName,
  _In_ LPENTRYPOINTS lpEntryPoints,
  _In_ DWORD         cbEntryPoints
);
```



## <a name="parameters"></a><span data-ttu-id="649f2-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="649f2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="649f2-107">*ProtocolName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="649f2-107">*ProtocolName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="649f2-108">Nombre del protocolo que el analizador detectará.</span><span class="sxs-lookup"><span data-stu-id="649f2-108">Name of the protocol the parser will detect.</span></span>

</dd> <dt>

<span data-ttu-id="649f2-109">*lpEntryPoints* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="649f2-109">*lpEntryPoints* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="649f2-110">Una estructura [ENTRYPOINTS](entrypoints.md) que contiene los puntos de entrada del archivo DLL del analizador restantes.</span><span class="sxs-lookup"><span data-stu-id="649f2-110">An [ENTRYPOINTS](entrypoints.md) structure that contains the remaining parser DLL entry points.</span></span> <span data-ttu-id="649f2-111">Vea la sección Comentarios para obtener una lista de las funciones de exportación a las que cada punto de entrada hace referencia.</span><span class="sxs-lookup"><span data-stu-id="649f2-111">See Remarks for a list of the export functions that each entry point references.</span></span> <span data-ttu-id="649f2-112">Los puntos de entrada se deben proporcionar en el orden especificado por la estructura **ENTRYPOINTS** .</span><span class="sxs-lookup"><span data-stu-id="649f2-112">Entry points must be provided in the order that the **ENTRYPOINTS** structure specifies.</span></span>

</dd> <dt>

<span data-ttu-id="649f2-113">*cbEntryPoints* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="649f2-113">*cbEntryPoints* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="649f2-114">Tamaño de la estructura **ENTRYPOINTS** .</span><span class="sxs-lookup"><span data-stu-id="649f2-114">The size of the **ENTRYPOINTS** structure.</span></span> <span data-ttu-id="649f2-115">Monitor de red proporciona una \_ macro de tamaño de ENTRYPOINTS que puede usar para especificar el tamaño de la estructura.</span><span class="sxs-lookup"><span data-stu-id="649f2-115">Network Monitor provides an ENTRYPOINTS\_SIZE macro that you can use to specify the size of the structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="649f2-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="649f2-116">Return value</span></span>

<span data-ttu-id="649f2-117">Si la función se realiza correctamente, el valor devuelto es un identificador del protocolo.</span><span class="sxs-lookup"><span data-stu-id="649f2-117">If the function is successful, the return value is a handle to the protocol.</span></span>

<span data-ttu-id="649f2-118">Si la función no se realiza correctamente, el valor devuelto es **null**.</span><span class="sxs-lookup"><span data-stu-id="649f2-118">If the function is unsuccessful, the return value is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="649f2-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="649f2-119">Remarks</span></span>

<span data-ttu-id="649f2-120">La DLL del analizador llama a **CreateProtocol** durante su implementación de [DllMain](dllmain-parser.md).</span><span class="sxs-lookup"><span data-stu-id="649f2-120">The parser DLL calls **CreateProtocol** during its implementation of [DllMain](dllmain-parser.md).</span></span> <span data-ttu-id="649f2-121">Se llama a la función **CreateProtocol** cuando el sistema operativo carga el archivo DLL del analizador por primera vez.</span><span class="sxs-lookup"><span data-stu-id="649f2-121">The **CreateProtocol** function is called when the operating system loads the parser DLL for the first time.</span></span>

<span data-ttu-id="649f2-122">Los puntos de entrada a los que se hace referencia en el parámetro *lpEntryPoints* incluyen punteros a las siguientes funciones de exportación que se deben proporcionar en el orden que se muestra aquí.</span><span class="sxs-lookup"><span data-stu-id="649f2-122">The entry points referenced in the *lpEntryPoints* parameter include pointers to the following export functions that must be provided in the order presented here.</span></span>

-   [<span data-ttu-id="649f2-123">Registro</span><span class="sxs-lookup"><span data-stu-id="649f2-123">Register</span></span>](register-parser.md)
-   [<span data-ttu-id="649f2-124">Eliminar registro</span><span class="sxs-lookup"><span data-stu-id="649f2-124">Deregister</span></span>](deregister.md)
-   [<span data-ttu-id="649f2-125">RecognizeFrame</span><span class="sxs-lookup"><span data-stu-id="649f2-125">RecognizeFrame</span></span>](recognizeframe.md)
-   [<span data-ttu-id="649f2-126">AttachProperties</span><span class="sxs-lookup"><span data-stu-id="649f2-126">AttachProperties</span></span>](attachproperties.md)
-   [<span data-ttu-id="649f2-127">FormatProperties</span><span class="sxs-lookup"><span data-stu-id="649f2-127">FormatProperties</span></span>](formatproperties.md)



| <span data-ttu-id="649f2-128">Para obtener información acerca de</span><span class="sxs-lookup"><span data-stu-id="649f2-128">For information on</span></span>                                                                                 | <span data-ttu-id="649f2-129">Vea</span><span class="sxs-lookup"><span data-stu-id="649f2-129">See</span></span>                                                     |
|----------------------------------------------------------------------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="649f2-130">Qué son los analizadores y cómo funcionan con Monitor de red.</span><span class="sxs-lookup"><span data-stu-id="649f2-130">What parsers are, and how they work with Network Monitor.</span></span>                                          | [<span data-ttu-id="649f2-131">Analizadores</span><span class="sxs-lookup"><span data-stu-id="649f2-131">Parsers</span></span>](parsers.md)                                  |
| <span data-ttu-id="649f2-132">Cómo implementar **DllMain** incluye un ejemplo de llamada a **CreateProtocol** dentro de **DllMain**.</span><span class="sxs-lookup"><span data-stu-id="649f2-132">How to implement **DllMain** includes an example of calling **CreateProtocol** within **DllMain**.</span></span> | [<span data-ttu-id="649f2-133">Implementar DllMain</span><span class="sxs-lookup"><span data-stu-id="649f2-133">Implementing DllMain</span></span>](implementing-dllmain-parser.md) |



 

## <a name="requirements"></a><span data-ttu-id="649f2-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="649f2-134">Requirements</span></span>



| <span data-ttu-id="649f2-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="649f2-135">Requirement</span></span> | <span data-ttu-id="649f2-136">Value</span><span class="sxs-lookup"><span data-stu-id="649f2-136">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="649f2-137">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="649f2-137">Minimum supported client</span></span><br/> | <span data-ttu-id="649f2-138">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="649f2-138">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="649f2-139">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="649f2-139">Minimum supported server</span></span><br/> | <span data-ttu-id="649f2-140">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="649f2-140">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="649f2-141">Encabezado</span><span class="sxs-lookup"><span data-stu-id="649f2-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="649f2-142"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="649f2-142"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="649f2-143">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="649f2-143">Library</span></span><br/>                  | <dl> <span data-ttu-id="649f2-144"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="649f2-144"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="649f2-145">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="649f2-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="649f2-146"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="649f2-146"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="649f2-147">Vea también</span><span class="sxs-lookup"><span data-stu-id="649f2-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="649f2-148">DllMain</span><span class="sxs-lookup"><span data-stu-id="649f2-148">DllMain</span></span>](/windows/desktop/Dlls/dllmain)
</dt> </dl>

 

