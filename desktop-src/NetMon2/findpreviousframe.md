---
description: La función FindPreviousFrame busca el fotograma anterior en el contexto de captura actual que coincida con el filtro.
ms.assetid: 16c5b981-a9f4-41e5-bb97-2caa3e9d8512
title: Función FindPreviousFrame (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FindPreviousFrame
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: deabf10702ca41c23101c5f60c9459e094e567fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000939"
---
# <a name="findpreviousframe-function"></a><span data-ttu-id="68a9a-103">FindPreviousFrame función)</span><span class="sxs-lookup"><span data-stu-id="68a9a-103">FindPreviousFrame function</span></span>

<span data-ttu-id="68a9a-104">La función **FindPreviousFrame** busca el fotograma anterior en el contexto de captura actual que coincida con el filtro.</span><span class="sxs-lookup"><span data-stu-id="68a9a-104">The **FindPreviousFrame** function finds the previous frame in the current capture context that matches the filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="68a9a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="68a9a-105">Syntax</span></span>


```C++
HFRAME WINAPI FindPreviousFrame(
   HFRAME    hCurrentFrame,
   LPSTR     ProtocolName,
   LPADDRESS DestinationAddress,
   LPADDRESS SourceAddress,
   LPWORD    ProtocolOffset,
   DWORD     OriginalFrameNumber,
   DWORD     LowestFrame
);
```



## <a name="parameters"></a><span data-ttu-id="68a9a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="68a9a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="68a9a-107">*hCurrentFrame*</span><span class="sxs-lookup"><span data-stu-id="68a9a-107">*hCurrentFrame*</span></span> 
</dt> <dd>

<span data-ttu-id="68a9a-108">Identificador del marco.</span><span class="sxs-lookup"><span data-stu-id="68a9a-108">Handle to the frame.</span></span>

</dd> <dt>

<span data-ttu-id="68a9a-109">*ProtocolName*</span><span class="sxs-lookup"><span data-stu-id="68a9a-109">*ProtocolName*</span></span> 
</dt> <dd>

<span data-ttu-id="68a9a-110">Nombre del Protocolo, como TCP.</span><span class="sxs-lookup"><span data-stu-id="68a9a-110">Protocol name, such as TCP.</span></span>

</dd> <dt>

<span data-ttu-id="68a9a-111">*DestinationAddress*</span><span class="sxs-lookup"><span data-stu-id="68a9a-111">*DestinationAddress*</span></span> 
</dt> <dd>

<span data-ttu-id="68a9a-112">Dirección de destino del fotograma que se busca.</span><span class="sxs-lookup"><span data-stu-id="68a9a-112">Destination address of the frame that is searched for.</span></span>

</dd> <dt>

<span data-ttu-id="68a9a-113">*SourceAddress*</span><span class="sxs-lookup"><span data-stu-id="68a9a-113">*SourceAddress*</span></span> 
</dt> <dd>

<span data-ttu-id="68a9a-114">Dirección de origen del marco que se busca.</span><span class="sxs-lookup"><span data-stu-id="68a9a-114">Source address of the frame that is searched for.</span></span>

</dd> <dt>

<span data-ttu-id="68a9a-115">*ProtocolOffset*</span><span class="sxs-lookup"><span data-stu-id="68a9a-115">*ProtocolOffset*</span></span> 
</dt> <dd>

<span data-ttu-id="68a9a-116">Puntero a una **palabra** que recibe el desplazamiento del protocolo.</span><span class="sxs-lookup"><span data-stu-id="68a9a-116">Pointer to a **WORD** that receives the protocol offset.</span></span>

</dd> <dt>

<span data-ttu-id="68a9a-117">*OriginalFrameNumber*</span><span class="sxs-lookup"><span data-stu-id="68a9a-117">*OriginalFrameNumber*</span></span> 
</dt> <dd>

<span data-ttu-id="68a9a-118">Punto de inicio de la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="68a9a-118">Starting point of the search.</span></span> <span data-ttu-id="68a9a-119">De forma predeterminada, esta función busca fotogramas hacia atrás 1.000 desde el punto inicial de *OriginalFrameNumber* .</span><span class="sxs-lookup"><span data-stu-id="68a9a-119">By default, this function searches backward 1,000 frames from *OriginalFrameNumber* starting point.</span></span> <span data-ttu-id="68a9a-120">Puede cambiar la distancia de la búsqueda mediante la adición de esta línea al archivo Nmapi.ini, que se encuentra en el \\ directorio monitor de red.</span><span class="sxs-lookup"><span data-stu-id="68a9a-120">You can change the search-back distance by adding this line to the Nmapi.ini file, which is located in the \\Network Monitor directory.</span></span>

<span data-ttu-id="68a9a-121">MAXLOOKBACK =<new lookback distance></span><span class="sxs-lookup"><span data-stu-id="68a9a-121">MAXLOOKBACK=<new lookback distance></span></span>

</dd> <dt>

<span data-ttu-id="68a9a-122">*LowestFrame*</span><span class="sxs-lookup"><span data-stu-id="68a9a-122">*LowestFrame*</span></span> 
</dt> <dd>

<span data-ttu-id="68a9a-123">Número de fotograma más bajo de la captura en el que se busca.</span><span class="sxs-lookup"><span data-stu-id="68a9a-123">Lowest frame number in the capture that is searched.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="68a9a-124">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="68a9a-124">Return value</span></span>

<span data-ttu-id="68a9a-125">Si la función es correcta, el valor devuelto es un identificador del fotograma anterior.</span><span class="sxs-lookup"><span data-stu-id="68a9a-125">If the function is successful, the return value is a handle to the previous frame.</span></span>

<span data-ttu-id="68a9a-126">Si la función no es correcta, el valor devuelto es **null**.</span><span class="sxs-lookup"><span data-stu-id="68a9a-126">If the function is not successful, the return value is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="68a9a-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="68a9a-127">Remarks</span></span>

<span data-ttu-id="68a9a-128">El filtro de captura se define principalmente mediante *ProtocolName*, que es la única entrada de filtro necesaria; puede agregar información de *DestinationAddress* y *SourceAddress* para aumentar la velocidad de captura.</span><span class="sxs-lookup"><span data-stu-id="68a9a-128">The capture filter is defined primarily by *ProtocolName*, which is the only required filter input; you can add *DestinationAddress* and *SourceAddress* information to increase the capture speed.</span></span>

<span data-ttu-id="68a9a-129">*ProtocolOffset* se devuelve al analizador que realiza la llamada, que agrega este **valor DWORD** al puntero devuelto al bloquear el marco (con [PARSERTEMPORARYLOCKFRAME](parsertemporarylockframe.md)) para obtener el LPBYTE del protocolo que se está buscando.</span><span class="sxs-lookup"><span data-stu-id="68a9a-129">*ProtocolOffset* is returned to the calling parser, which adds this **DWORD** to the pointer returned by locking the frame (with [ParserTemporaryLockFrame](parsertemporarylockframe.md)) to get the LPBYTE of the protocol that is being searched for.</span></span> <span data-ttu-id="68a9a-130">En la devolución, se proporciona al analizador el HFRAME que pasó el filtro.</span><span class="sxs-lookup"><span data-stu-id="68a9a-130">On return, the HFRAME that passed the filter is given to the parser.</span></span> <span data-ttu-id="68a9a-131">Si el analizador encuentra que el fotograma no es el que se está buscando, el analizador puede volver a HFRAME a la función **FindPreviousFrame** para recuperar el fotograma siguiente.</span><span class="sxs-lookup"><span data-stu-id="68a9a-131">If the parser finds that the frame is not the one that is being sought, the parser can hand this HFRAME back to the **FindPreviousFrame** function to retrieve the next frame.</span></span> <span data-ttu-id="68a9a-132">Las direcciones de origen y de destino, que no son necesarias, se pueden pasar como **null**.</span><span class="sxs-lookup"><span data-stu-id="68a9a-132">The source and destination addresses, which are not required, can be passed in as **NULL**.</span></span> <span data-ttu-id="68a9a-133">Cuando se utiliza, estas direcciones pueden ser de tipo \_ dirección \_ IP, etc., no solo tipos Mac.</span><span class="sxs-lookup"><span data-stu-id="68a9a-133">When used, these addresses can be of type ADDRESS\_TYPE\_IP, and so on, not just MAC types.</span></span>

## <a name="requirements"></a><span data-ttu-id="68a9a-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="68a9a-134">Requirements</span></span>



| <span data-ttu-id="68a9a-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="68a9a-135">Requirement</span></span> | <span data-ttu-id="68a9a-136">Value</span><span class="sxs-lookup"><span data-stu-id="68a9a-136">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="68a9a-137">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="68a9a-137">Minimum supported client</span></span><br/> | <span data-ttu-id="68a9a-138">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="68a9a-138">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="68a9a-139">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="68a9a-139">Minimum supported server</span></span><br/> | <span data-ttu-id="68a9a-140">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="68a9a-140">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="68a9a-141">Encabezado</span><span class="sxs-lookup"><span data-stu-id="68a9a-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="68a9a-142"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="68a9a-142"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="68a9a-143">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="68a9a-143">Library</span></span><br/>                  | <dl> <span data-ttu-id="68a9a-144"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="68a9a-144"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="68a9a-145">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="68a9a-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="68a9a-146"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="68a9a-146"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




