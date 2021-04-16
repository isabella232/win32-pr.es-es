---
description: La función CreatePropertyDatabase crea una base de datos de propiedades que almacena las propiedades de un protocolo.
ms.assetid: 0a3be6ae-d7ce-4315-b4f2-b46bcfa25b69
title: Función CreatePropertyDatabase (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreatePropertyDatabase
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 2955aa3367648c4e9e23fd748fa27d6343ef78a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677736"
---
# <a name="createpropertydatabase-function"></a><span data-ttu-id="5b047-103">CreatePropertyDatabase función)</span><span class="sxs-lookup"><span data-stu-id="5b047-103">CreatePropertyDatabase function</span></span>

<span data-ttu-id="5b047-104">La función **CreatePropertyDatabase** crea una base de datos de propiedades que almacena las propiedades de un protocolo.</span><span class="sxs-lookup"><span data-stu-id="5b047-104">The **CreatePropertyDatabase** function creates a property database that stores the properties of a protocol.</span></span>

## <a name="syntax"></a><span data-ttu-id="5b047-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5b047-105">Syntax</span></span>


```C++
DWORD WINAPI CreatePropertyDatabase(
  _In_ HPROTOCOL hProtocol,
  _In_ DWORD     nProperties
);
```



## <a name="parameters"></a><span data-ttu-id="5b047-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5b047-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5b047-107">*hProtocol* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="5b047-107">*hProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5b047-108">Identificador del protocolo asociado a la base de datos.</span><span class="sxs-lookup"><span data-stu-id="5b047-108">Handle of the protocol that is associated with the database.</span></span> <span data-ttu-id="5b047-109">Cuando Monitor de red llama a la función [Register](register-parser.md) , monitor de red pasa el identificador de protocolo a la dll del analizador.</span><span class="sxs-lookup"><span data-stu-id="5b047-109">When Network Monitor calls the [Register](register-parser.md) function, Network Monitor passes the protocol handle to the parser DLL.</span></span>

</dd> <dt>

<span data-ttu-id="5b047-110">*nProperties* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="5b047-110">*nProperties* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5b047-111">Número de propiedades almacenadas en la base de datos.</span><span class="sxs-lookup"><span data-stu-id="5b047-111">Number of properties stored in the database.</span></span> <span data-ttu-id="5b047-112">Establezca este parámetro en el número de propiedades que admite el protocolo.</span><span class="sxs-lookup"><span data-stu-id="5b047-112">Set this parameter to the number of properties that the protocol supports.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5b047-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5b047-113">Return value</span></span>

<span data-ttu-id="5b047-114">Si la función se realiza correctamente, el valor devuelto es NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="5b047-114">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="5b047-115">Si la función no es correcta, el valor devuelto es un código de error.</span><span class="sxs-lookup"><span data-stu-id="5b047-115">If the function is unsuccessful, the return value is an error code.</span></span>



| <span data-ttu-id="5b047-116">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="5b047-116">Return code</span></span>                                                                                             | <span data-ttu-id="5b047-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="5b047-117">Description</span></span>                                                                    |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="5b047-118"><dt>**\_error interno de NMERR \_**</dt></span><span class="sxs-lookup"><span data-stu-id="5b047-118"><dt>**NMERR\_INTERNAL\_ERROR**</dt></span></span> </dl>   | <span data-ttu-id="5b047-119">Se ha producido un error interno.</span><span class="sxs-lookup"><span data-stu-id="5b047-119">An internal error has occurred.</span></span><br/>                                     |
| <dl> <span data-ttu-id="5b047-120"><dt>**NMERR \_ no válido \_ HPOTOCOL**</dt></span><span class="sxs-lookup"><span data-stu-id="5b047-120"><dt>**NMERR\_INVALID\_HPOTOCOL**</dt></span></span> </dl> | <span data-ttu-id="5b047-121">El identificador del protocolo especificado en *hProtocol* no es válido.</span><span class="sxs-lookup"><span data-stu-id="5b047-121">The handle to the protocol specified in *hProtocol* is invalid.</span></span><br/>     |
| <dl> <span data-ttu-id="5b047-122"><dt>**NMERR \_ \_ de \_ memoria insuficiente**</dt></span><span class="sxs-lookup"><span data-stu-id="5b047-122"><dt>**NMERR\_OUT\_OF\_MEMORY**</dt></span></span> </dl>   | <span data-ttu-id="5b047-123">Monitor de red no tiene suficiente memoria para crear la base de datos.</span><span class="sxs-lookup"><span data-stu-id="5b047-123">Network Monitor does not have enough memory to create the database.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="5b047-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5b047-124">Remarks</span></span>

<span data-ttu-id="5b047-125">Solo se debe llamar a la función **CreatePropertyDatabase** cuando se implementa la función [Register](register-parser.md) .</span><span class="sxs-lookup"><span data-stu-id="5b047-125">The **CreatePropertyDatabase** function should be called only when implementing the [Register](register-parser.md) function.</span></span> <span data-ttu-id="5b047-126">El analizador usa **CreatePropertyDatabase** para crear una base de datos de propiedades que describe las propiedades de un protocolo.</span><span class="sxs-lookup"><span data-stu-id="5b047-126">The parser uses **CreatePropertyDatabase** to create a property database that describes the properties of a protocol.</span></span> <span data-ttu-id="5b047-127">Monitor de red usa la base de datos para interpretar la información incluida en el protocolo.</span><span class="sxs-lookup"><span data-stu-id="5b047-127">Network Monitor uses the database to interpret the information within the protocol.</span></span>

<span data-ttu-id="5b047-128">La función **CreatePropertyDatabase** asigna las estructuras que monitor de red necesita para mantener una base de datos de propiedades.</span><span class="sxs-lookup"><span data-stu-id="5b047-128">The **CreatePropertyDatabase** function allocates the structures that Network Monitor needs to maintain a property database.</span></span>

## <a name="requirements"></a><span data-ttu-id="5b047-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5b047-129">Requirements</span></span>



| <span data-ttu-id="5b047-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="5b047-130">Requirement</span></span> | <span data-ttu-id="5b047-131">Value</span><span class="sxs-lookup"><span data-stu-id="5b047-131">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="5b047-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5b047-132">Minimum supported client</span></span><br/> | <span data-ttu-id="5b047-133">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="5b047-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="5b047-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5b047-134">Minimum supported server</span></span><br/> | <span data-ttu-id="5b047-135">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="5b047-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="5b047-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5b047-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="5b047-137"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="5b047-137"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="5b047-138">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5b047-138">Library</span></span><br/>                  | <dl> <span data-ttu-id="5b047-139"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5b047-139"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="5b047-140">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="5b047-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5b047-141"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5b047-141"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5b047-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="5b047-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b047-143">Registro</span><span class="sxs-lookup"><span data-stu-id="5b047-143">Register</span></span>](register-parser.md)
</dt> </dl>

 

 




