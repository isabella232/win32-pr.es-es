---
description: Devuelve el desplazamiento de un protocolo especificado en el marco.
ms.assetid: bfe5f477-c9de-4bb9-99e5-b8db895b0ae6
title: Función GetProtocolStartOffset (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetProtocolStartOffset
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: ff760c4a61cb39ba897351d706c39d240389bf49
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666277"
---
# <a name="getprotocolstartoffset-function"></a><span data-ttu-id="b9a7d-103">GetProtocolStartOffset función)</span><span class="sxs-lookup"><span data-stu-id="b9a7d-103">GetProtocolStartOffset function</span></span>

<span data-ttu-id="b9a7d-104">La función **GetProtocolStartOffset** devuelve el desplazamiento de un protocolo especificado en el marco.</span><span class="sxs-lookup"><span data-stu-id="b9a7d-104">The **GetProtocolStartOffset** function returns the offset of a specified protocol in the frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="b9a7d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b9a7d-105">Syntax</span></span>


```C++
DWORD WINAPI GetProtocolStartOffset(
   HFRAME hFrame,
   LPSTR  ProtocolName
);
```



## <a name="parameters"></a><span data-ttu-id="b9a7d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b9a7d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b9a7d-107">*hFrame*</span><span class="sxs-lookup"><span data-stu-id="b9a7d-107">*hFrame*</span></span> 
</dt> <dd>

<span data-ttu-id="b9a7d-108">Identificador del marco.</span><span class="sxs-lookup"><span data-stu-id="b9a7d-108">A handle to the frame.</span></span>

</dd> <dt>

<span data-ttu-id="b9a7d-109">*ProtocolName*</span><span class="sxs-lookup"><span data-stu-id="b9a7d-109">*ProtocolName*</span></span> 
</dt> <dd>

<span data-ttu-id="b9a7d-110">El nombre del Protocolo, como TCP.</span><span class="sxs-lookup"><span data-stu-id="b9a7d-110">The Protocol name, such as TCP.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b9a7d-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b9a7d-111">Return value</span></span>

<span data-ttu-id="b9a7d-112">Si la función es correcta, el valor devuelto es un desplazamiento de **DWORD** al principio del protocolo en el que se busca un valor devuelto de cero indica que el protocolo es el primer protocolo del marco.</span><span class="sxs-lookup"><span data-stu-id="b9a7d-112">If the function is successful, the return value is a **DWORD** offset to the beginning of the protocol being searched for   a return value of zero indicates the protocol is the first protocol in the frame.</span></span>

<span data-ttu-id="b9a7d-113">Si la función no se realiza correctamente, el Protocolo no está en el marco, el valor devuelto es-1.</span><span class="sxs-lookup"><span data-stu-id="b9a7d-113">If the function is unsuccessful, the protocol is not in the frame, the return value is -1.</span></span>

## <a name="remarks"></a><span data-ttu-id="b9a7d-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b9a7d-114">Remarks</span></span>

<span data-ttu-id="b9a7d-115">Cuando se proporciona el identificador a un marco, esta función devuelve el desplazamiento a un protocolo especificado en el marco.</span><span class="sxs-lookup"><span data-stu-id="b9a7d-115">When given the handle to a frame, this function returns the offset to a specified protocol in the frame.</span></span> <span data-ttu-id="b9a7d-116">Por ejemplo, para determinar si el marco es un marco DNS, el analizador DNS requiere la dirección de puerto del protocolo TCP.</span><span class="sxs-lookup"><span data-stu-id="b9a7d-116">For example, to determine whether the frame is a DNS frame, the DNS parser requires the port address of the TCP protocol.</span></span> <span data-ttu-id="b9a7d-117">El analizador de DNS llamaría a esta función con TCP como valor de *ProtocolName* .</span><span class="sxs-lookup"><span data-stu-id="b9a7d-117">The DNS parser would call this function with TCP as the *ProtocolName* value.</span></span> <span data-ttu-id="b9a7d-118">Si el protocolo TCP reconoce el fotograma, se devuelve la **palabra** de desplazamiento desde el principio del marco hasta el principio de la trama TCP.</span><span class="sxs-lookup"><span data-stu-id="b9a7d-118">If the frame is recognized by the TCP protocol, the **WORD** offset from the beginning of the frame to the beginning of the TCP frame is returned.</span></span> <span data-ttu-id="b9a7d-119">Si no hay ningún protocolo TCP, el valor devuelto es cero.</span><span class="sxs-lookup"><span data-stu-id="b9a7d-119">If there is no TCP protocol, the return value is zero.</span></span>

<span data-ttu-id="b9a7d-120">Esta función busca el principio de un protocolo en un marco.</span><span class="sxs-lookup"><span data-stu-id="b9a7d-120">This function finds the beginning of a protocol in a frame.</span></span>

## <a name="requirements"></a><span data-ttu-id="b9a7d-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b9a7d-121">Requirements</span></span>



| <span data-ttu-id="b9a7d-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="b9a7d-122">Requirement</span></span> | <span data-ttu-id="b9a7d-123">Value</span><span class="sxs-lookup"><span data-stu-id="b9a7d-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="b9a7d-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b9a7d-124">Minimum supported client</span></span><br/> | <span data-ttu-id="b9a7d-125">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="b9a7d-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="b9a7d-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b9a7d-126">Minimum supported server</span></span><br/> | <span data-ttu-id="b9a7d-127">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="b9a7d-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="b9a7d-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b9a7d-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="b9a7d-129"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="b9a7d-129"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="b9a7d-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b9a7d-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="b9a7d-131"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b9a7d-131"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="b9a7d-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b9a7d-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b9a7d-133"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b9a7d-133"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




