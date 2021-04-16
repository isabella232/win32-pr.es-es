---
description: Busca el siguiente fotograma en el contexto de captura actual que coincida con el filtro.
ms.assetid: cc99b4a0-b6b0-43b4-8121-0e402d024009
title: Función FindNextFrame (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FindNextFrame
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 2e303f7f9031ad451ad19be8bc8cbcd3abae3f46
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540227"
---
# <a name="findnextframe-function"></a><span data-ttu-id="a2bbb-103">FindNextFrame función)</span><span class="sxs-lookup"><span data-stu-id="a2bbb-103">FindNextFrame function</span></span>

<span data-ttu-id="a2bbb-104">La función **FindNextFrame** busca el siguiente fotograma en el contexto de captura actual que coincida con el filtro.</span><span class="sxs-lookup"><span data-stu-id="a2bbb-104">The **FindNextFrame** function finds the next frame in the current capture context that matches the filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="a2bbb-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a2bbb-105">Syntax</span></span>


```C++
HFRAME WINAPI FindNextFrame(
   HFRAME    hCurrentFrame,
   LPSTR     ProtocolName,
   LPADDRESS DestinationAddress,
   LPADDRESS SourceAddress,
   LPWORD    ProtocolOffset,
   DWORD     OriginalFrameNumber,
   DWORD     HighestFrame
);
```



## <a name="parameters"></a><span data-ttu-id="a2bbb-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a2bbb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a2bbb-107">*hCurrentFrame*</span><span class="sxs-lookup"><span data-stu-id="a2bbb-107">*hCurrentFrame*</span></span> 
</dt> <dd>

<span data-ttu-id="a2bbb-108">Identificador del marco.</span><span class="sxs-lookup"><span data-stu-id="a2bbb-108">A handle to the frame.</span></span>

</dd> <dt>

<span data-ttu-id="a2bbb-109">*ProtocolName*</span><span class="sxs-lookup"><span data-stu-id="a2bbb-109">*ProtocolName*</span></span> 
</dt> <dd>

<span data-ttu-id="a2bbb-110">El nombre del Protocolo, como TCP.</span><span class="sxs-lookup"><span data-stu-id="a2bbb-110">The protocol name, such as TCP.</span></span>

</dd> <dt>

<span data-ttu-id="a2bbb-111">*DestinationAddress*</span><span class="sxs-lookup"><span data-stu-id="a2bbb-111">*DestinationAddress*</span></span> 
</dt> <dd>

<span data-ttu-id="a2bbb-112">Dirección de destino.</span><span class="sxs-lookup"><span data-stu-id="a2bbb-112">The destination address.</span></span>

</dd> <dt>

<span data-ttu-id="a2bbb-113">*SourceAddress*</span><span class="sxs-lookup"><span data-stu-id="a2bbb-113">*SourceAddress*</span></span> 
</dt> <dd>

<span data-ttu-id="a2bbb-114">Dirección de origen.</span><span class="sxs-lookup"><span data-stu-id="a2bbb-114">The source address.</span></span>

</dd> <dt>

<span data-ttu-id="a2bbb-115">*ProtocolOffset*</span><span class="sxs-lookup"><span data-stu-id="a2bbb-115">*ProtocolOffset*</span></span> 
</dt> <dd>

<span data-ttu-id="a2bbb-116">Puntero a una **palabra** que recibirá el desplazamiento del protocolo.</span><span class="sxs-lookup"><span data-stu-id="a2bbb-116">A pointer to a **WORD** that will receive the protocol offset.</span></span>

</dd> <dt>

<span data-ttu-id="a2bbb-117">*OriginalFrameNumber*</span><span class="sxs-lookup"><span data-stu-id="a2bbb-117">*OriginalFrameNumber*</span></span> 
</dt> <dd>

<span data-ttu-id="a2bbb-118">Punto inicial de la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="a2bbb-118">The starting point of the search.</span></span> <span data-ttu-id="a2bbb-119">De forma predeterminada, esta función realiza búsquedas hacia delante 1.000 fotogramas desde el punto de inicio *OriginalFrameNumber* .</span><span class="sxs-lookup"><span data-stu-id="a2bbb-119">By default, this function searches forward 1,000 frames from the *OriginalFrameNumber* starting point.</span></span> <span data-ttu-id="a2bbb-120">Para cambiar la distancia de búsqueda, agregue esta línea al archivo Nmapi.ini, situado en el \\ directorio monitor de red.</span><span class="sxs-lookup"><span data-stu-id="a2bbb-120">To change the search-forward distance, add this line to the Nmapi.ini file, located in the \\Network Monitor directory.</span></span>

<span data-ttu-id="a2bbb-121">MAXLOOKBACK =<new lookforward distance></span><span class="sxs-lookup"><span data-stu-id="a2bbb-121">MAXLOOKBACK=<new lookforward distance></span></span>

</dd> <dt>

<span data-ttu-id="a2bbb-122">*HighestFrame*</span><span class="sxs-lookup"><span data-stu-id="a2bbb-122">*HighestFrame*</span></span> 
</dt> <dd>

<span data-ttu-id="a2bbb-123">Número de fotograma más alto de la captura en el que se busca.</span><span class="sxs-lookup"><span data-stu-id="a2bbb-123">The highest frame number in the capture that is searched.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a2bbb-124">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a2bbb-124">Return value</span></span>

<span data-ttu-id="a2bbb-125">Si la función es correcta, el valor devuelto es un identificador del fotograma siguiente.</span><span class="sxs-lookup"><span data-stu-id="a2bbb-125">If the function is successful, the return value is a handle to the next frame.</span></span>

<span data-ttu-id="a2bbb-126">Si la función no es correcta, el valor devuelto es **null**.</span><span class="sxs-lookup"><span data-stu-id="a2bbb-126">If the function is not successful, the return value is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="a2bbb-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a2bbb-127">Remarks</span></span>

<span data-ttu-id="a2bbb-128">El filtro de captura se define principalmente mediante el parámetro *ProtocolName* , que es la única entrada de filtro necesaria; puede agregar datos de *DestinationAddress* y *SourceAddress* para aumentar la velocidad de captura.</span><span class="sxs-lookup"><span data-stu-id="a2bbb-128">The capture filter is defined primarily by the *ProtocolName* parameter, which is the only required filter input; you can add *DestinationAddress* and *SourceAddress* data to increase the capture speed.</span></span>

<span data-ttu-id="a2bbb-129">El puntero *ProtocolOffset* se devuelve al analizador que realiza la llamada, que agrega la **palabra** al puntero devuelto al bloquear el marco (con [ParserTemporaryLockFrame](parsertemporarylockframe.md)) para obtener el **LPBYTE** del protocolo que se busca.</span><span class="sxs-lookup"><span data-stu-id="a2bbb-129">The *ProtocolOffset* pointer is returned to the calling parser, which adds the **WORD** to the pointer returned by locking the frame (with [ParserTemporaryLockFrame](parsertemporarylockframe.md)) to get the **LPBYTE** of the protocol searched for.</span></span> <span data-ttu-id="a2bbb-130">En la devolución, se proporciona al analizador el HFRAME que pasó el filtro.</span><span class="sxs-lookup"><span data-stu-id="a2bbb-130">On return, the HFRAME that passed the filter is given to the parser.</span></span> <span data-ttu-id="a2bbb-131">Si el analizador encuentra que este fotograma no es el que se busca, el analizador puede volver a HFRAME a la función **FindNextFrame** para obtener el fotograma siguiente.</span><span class="sxs-lookup"><span data-stu-id="a2bbb-131">If the parser finds that this frame is not the one sought, the parser can hand the HFRAME back to the **FindNextFrame** function to get the next frame.</span></span> <span data-ttu-id="a2bbb-132">Las direcciones de origen y de destino no son necesarias y se pueden pasar como **null**.</span><span class="sxs-lookup"><span data-stu-id="a2bbb-132">The source and destination addresses are not required and can be passed as **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="a2bbb-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a2bbb-133">Requirements</span></span>



| <span data-ttu-id="a2bbb-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="a2bbb-134">Requirement</span></span> | <span data-ttu-id="a2bbb-135">Value</span><span class="sxs-lookup"><span data-stu-id="a2bbb-135">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="a2bbb-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a2bbb-136">Minimum supported client</span></span><br/> | <span data-ttu-id="a2bbb-137">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="a2bbb-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="a2bbb-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a2bbb-138">Minimum supported server</span></span><br/> | <span data-ttu-id="a2bbb-139">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="a2bbb-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="a2bbb-140">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a2bbb-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="a2bbb-141"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="a2bbb-141"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="a2bbb-142">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a2bbb-142">Library</span></span><br/>                  | <dl> <span data-ttu-id="a2bbb-143"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a2bbb-143"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="a2bbb-144">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a2bbb-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a2bbb-145"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a2bbb-145"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




