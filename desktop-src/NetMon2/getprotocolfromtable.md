---
description: La función GetProtocolFromTable devuelve un identificador a un protocolo&\# 8212; basándose en una tabla de entrega y un valor determinados.
ms.assetid: 34b07079-0b20-40d8-a529-4179ecc68ebf
title: Función GetProtocolFromTable (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetProtocolFromTable
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 498892fc2cc5ada2e177b8fb3f70f40a1ef10dfe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000923"
---
# <a name="getprotocolfromtable-function"></a><span data-ttu-id="9cc25-103">GetProtocolFromTable función)</span><span class="sxs-lookup"><span data-stu-id="9cc25-103">GetProtocolFromTable function</span></span>

<span data-ttu-id="9cc25-104">La función **GetProtocolFromTable** devuelve un identificador a un protocolo basado en una tabla de entrega y un valor determinados.</span><span class="sxs-lookup"><span data-stu-id="9cc25-104">The **GetProtocolFromTable** function returns a handle to a protocol based on a given handoff table and value.</span></span>

## <a name="syntax"></a><span data-ttu-id="9cc25-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9cc25-105">Syntax</span></span>


```C++
HPROTOCOL WINAPI GetProtocolFromTable(
  _In_  LPHANDOFFTABLE hTable,
  _In_  DWORD          ItemToFind,
  _Out_ PDWORD_PTR     lpInstData
);
```



## <a name="parameters"></a><span data-ttu-id="9cc25-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9cc25-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9cc25-107">*hTable* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="9cc25-107">*hTable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9cc25-108">Identificador de una tabla de entrega.</span><span class="sxs-lookup"><span data-stu-id="9cc25-108">Handle to a handoff table.</span></span>

</dd> <dt>

<span data-ttu-id="9cc25-109">*ItemToFind* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="9cc25-109">*ItemToFind* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9cc25-110">Valor usado para buscar el protocolo en una tabla de entrega.</span><span class="sxs-lookup"><span data-stu-id="9cc25-110">Value used to locate the protocol in a handoff table.</span></span> <span data-ttu-id="9cc25-111">El valor debe estar disponible en los datos del protocolo.</span><span class="sxs-lookup"><span data-stu-id="9cc25-111">The value must be available in the protocol data.</span></span>

</dd> <dt>

<span data-ttu-id="9cc25-112">*lpInstData* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="9cc25-112">*lpInstData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9cc25-113">Si está disponible en la tabla de entrega, datos de instancia para el protocolo siguiente.</span><span class="sxs-lookup"><span data-stu-id="9cc25-113">If available in the handoff table, instance data for the next protocol.</span></span> <span data-ttu-id="9cc25-114">Los datos de instancia no pueden tener más de una \_ longitud de DWORD PTR.</span><span class="sxs-lookup"><span data-stu-id="9cc25-114">Instance data cannot be longer than a DWORD\_PTR in length.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9cc25-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9cc25-115">Return value</span></span>

<span data-ttu-id="9cc25-116">Si la función se realiza correctamente, el valor devuelto es un identificador de protocolo.</span><span class="sxs-lookup"><span data-stu-id="9cc25-116">If the function is successful, the return value is a protocol handle.</span></span>

<span data-ttu-id="9cc25-117">Si la función no se realiza correctamente, el valor devuelto es **null**.</span><span class="sxs-lookup"><span data-stu-id="9cc25-117">If the function is unsuccessful, the return value is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="9cc25-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9cc25-118">Remarks</span></span>

<span data-ttu-id="9cc25-119">Al implementar la función de exportación [RecognizeFrame](recognizeframe.md) , se usa la función **GetProtocolFromTable** para obtener un identificador del protocolo siguiente.</span><span class="sxs-lookup"><span data-stu-id="9cc25-119">When implementing the [RecognizeFrame](recognizeframe.md) export function, the **GetProtocolFromTable** function is used to obtain a handle to the next protocol.</span></span> <span data-ttu-id="9cc25-120">Se llama a la función **GetProtocolFromTable** para recuperar un identificador del protocolo siguiente si el protocolo identifica el protocolo que sigue.</span><span class="sxs-lookup"><span data-stu-id="9cc25-120">The **GetProtocolFromTable** function is called to retrieve a handle from the next protocol if the protocol identifies which protocol follows.</span></span>

<span data-ttu-id="9cc25-121">**Datos de instancia**</span><span class="sxs-lookup"><span data-stu-id="9cc25-121">**Instance data**</span></span>

<span data-ttu-id="9cc25-122">Los datos de instancia pueden ser cualquier dato que sea menor o igual que \_ la longitud de un valor DWORD PTR, o un puntero a los datos, como los datos de fotogramas sin formato, que no es necesario que el analizador asigne o libere.</span><span class="sxs-lookup"><span data-stu-id="9cc25-122">Instance data can be any data that is less than or equal to a DWORD\_PTR in length, or a pointer to data, such as raw frame data, that does not need to be allocated by or freed by the parser.</span></span>

## <a name="requirements"></a><span data-ttu-id="9cc25-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9cc25-123">Requirements</span></span>



| <span data-ttu-id="9cc25-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="9cc25-124">Requirement</span></span> | <span data-ttu-id="9cc25-125">Value</span><span class="sxs-lookup"><span data-stu-id="9cc25-125">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="9cc25-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9cc25-126">Minimum supported client</span></span><br/> | <span data-ttu-id="9cc25-127">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="9cc25-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="9cc25-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9cc25-128">Minimum supported server</span></span><br/> | <span data-ttu-id="9cc25-129">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="9cc25-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="9cc25-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9cc25-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="9cc25-131"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="9cc25-131"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="9cc25-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9cc25-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="9cc25-133"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9cc25-133"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="9cc25-134">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="9cc25-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9cc25-135"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9cc25-135"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9cc25-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="9cc25-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9cc25-137">RecognizeFrame</span><span class="sxs-lookup"><span data-stu-id="9cc25-137">RecognizeFrame</span></span>](recognizeframe.md)
</dt> </dl>

 

 




