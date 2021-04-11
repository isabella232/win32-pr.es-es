---
description: La función DestroyProtocol destruye el protocolo que crea la función CreateProtocol.
ms.assetid: f7621c2a-1905-4748-b8e3-7b49f3f2bf03
title: Función DestroyProtocol (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DestroyProtocol
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: be96a13816a6a35bdd554380dacd5e8e2f5d5450
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276694"
---
# <a name="destroyprotocol-function"></a><span data-ttu-id="075d0-103">DestroyProtocol función)</span><span class="sxs-lookup"><span data-stu-id="075d0-103">DestroyProtocol function</span></span>

<span data-ttu-id="075d0-104">La función **DestroyProtocol** destruye el protocolo que crea la función **CreateProtocol** .</span><span class="sxs-lookup"><span data-stu-id="075d0-104">The **DestroyProtocol** function destroys the protocol that the **CreateProtocol** function creates.</span></span>

## <a name="syntax"></a><span data-ttu-id="075d0-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="075d0-105">Syntax</span></span>


```C++
VOID WINAPI DestroyProtocol(
  _In_ HPROTOCOL hProtocol
);
```



## <a name="parameters"></a><span data-ttu-id="075d0-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="075d0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="075d0-107">*hProtocol* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="075d0-107">*hProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="075d0-108">Identificador del protocolo que se va a destruir.</span><span class="sxs-lookup"><span data-stu-id="075d0-108">Handle to the protocol to be destroyed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="075d0-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="075d0-109">Return value</span></span>

<span data-ttu-id="075d0-110">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="075d0-110">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="075d0-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="075d0-111">Remarks</span></span>

<span data-ttu-id="075d0-112">El archivo DLL del analizador llama a la función **DestroyProtocol** durante su implementación de [DllMain](dllmain-parser.md).</span><span class="sxs-lookup"><span data-stu-id="075d0-112">The parser DLL calls the **DestroyProtocol** function during its implementation of [DllMain](dllmain-parser.md).</span></span> <span data-ttu-id="075d0-113">Se llama a **DestroyProtocol** cuando el sistema operativo va a descargar el archivo dll.</span><span class="sxs-lookup"><span data-stu-id="075d0-113">**DestroyProtocol** is called when the operating system is going to unload the DLL.</span></span>



| <span data-ttu-id="075d0-114">Para obtener información acerca de</span><span class="sxs-lookup"><span data-stu-id="075d0-114">For information on</span></span>                                        | <span data-ttu-id="075d0-115">Vea</span><span class="sxs-lookup"><span data-stu-id="075d0-115">See</span></span>                                                     |
|-----------------------------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="075d0-116">Qué son los analizadores y cómo funcionan con Monitor de red.</span><span class="sxs-lookup"><span data-stu-id="075d0-116">What parsers are, and how they work with Network Monitor.</span></span> | [<span data-ttu-id="075d0-117">Analizadores</span><span class="sxs-lookup"><span data-stu-id="075d0-117">Parsers</span></span>](parsers.md)                                  |
| <span data-ttu-id="075d0-118">Cómo implementar **DllMain** incluye un ejemplo.</span><span class="sxs-lookup"><span data-stu-id="075d0-118">How to implement **DllMain** includes an example.</span></span>         | [<span data-ttu-id="075d0-119">Implementar DllMain</span><span class="sxs-lookup"><span data-stu-id="075d0-119">Implementing DllMain</span></span>](implementing-dllmain-parser.md) |



 

## <a name="requirements"></a><span data-ttu-id="075d0-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="075d0-120">Requirements</span></span>



| <span data-ttu-id="075d0-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="075d0-121">Requirement</span></span> | <span data-ttu-id="075d0-122">Value</span><span class="sxs-lookup"><span data-stu-id="075d0-122">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="075d0-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="075d0-123">Minimum supported client</span></span><br/> | <span data-ttu-id="075d0-124">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="075d0-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="075d0-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="075d0-125">Minimum supported server</span></span><br/> | <span data-ttu-id="075d0-126">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="075d0-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="075d0-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="075d0-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="075d0-128"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="075d0-128"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="075d0-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="075d0-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="075d0-130"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="075d0-130"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="075d0-131">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="075d0-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="075d0-132"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="075d0-132"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="075d0-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="075d0-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="075d0-134">DllMain</span><span class="sxs-lookup"><span data-stu-id="075d0-134">DllMain</span></span>](dllmain-parser.md)
</dt> </dl>

 

 




