---
description: La función ExpertSubmitEvent indica que existe una condición de evento y proporciona una estructura de datos que describe la condición.
ms.assetid: 2339b530-427b-4028-aef6-c2cdd1353f77
title: Función ExpertSubmitEvent (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExpertSubmitEvent
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 448d77e9cb009b8aced0aba752526dc08b503066
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360151"
---
# <a name="expertsubmitevent-function"></a><span data-ttu-id="e87cb-103">ExpertSubmitEvent función)</span><span class="sxs-lookup"><span data-stu-id="e87cb-103">ExpertSubmitEvent function</span></span>

<span data-ttu-id="e87cb-104">La función **ExpertSubmitEvent** indica que existe una condición de evento y proporciona una estructura de datos que describe la condición.</span><span class="sxs-lookup"><span data-stu-id="e87cb-104">The **ExpertSubmitEvent** function indicates that an event condition exists and provides a data structure that describes the condition.</span></span>

## <a name="syntax"></a><span data-ttu-id="e87cb-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e87cb-105">Syntax</span></span>


```C++
DWORD WINAPI ExpertSubmitEvent(
  _In_ HEXPERTKEY   hExpertKey,
  _In_ PNMEVENTDATA pExpertEvent
);
```



## <a name="parameters"></a><span data-ttu-id="e87cb-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e87cb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e87cb-107">*hExpertKey* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e87cb-107">*hExpertKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e87cb-108">Identificador único del experto.</span><span class="sxs-lookup"><span data-stu-id="e87cb-108">Unique identifier of the expert.</span></span> <span data-ttu-id="e87cb-109">Monitor de red pasa *hExpertKey* al experto cuando llama a la función [Run](run.md) .</span><span class="sxs-lookup"><span data-stu-id="e87cb-109">Network Monitor passes *hExpertKey* to the expert when it calls the [Run](run.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="e87cb-110">*pExpertEvent* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e87cb-110">*pExpertEvent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e87cb-111">Puntero a una estructura **NMEVENTDATA** que describe la condición del evento.</span><span class="sxs-lookup"><span data-stu-id="e87cb-111">A pointer to an **NMEVENTDATA** structure that describes the event condition.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e87cb-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e87cb-112">Return value</span></span>

<span data-ttu-id="e87cb-113">Si la función se realiza correctamente, el valor devuelto es NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="e87cb-113">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="e87cb-114">Si la función no se realiza correctamente, el valor devuelto indica la razón del error.</span><span class="sxs-lookup"><span data-stu-id="e87cb-114">If the function is unsuccessful, the return value indicates the reason for the failure.</span></span> <span data-ttu-id="e87cb-115">Si el valor devuelto es NMERR \_ Expert \_ Terminate, el experto limpia y devuelve inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="e87cb-115">If the return value is NMERR\_EXPERT\_TERMINATE, the expert immediately cleans up and returns.</span></span>

## <a name="requirements"></a><span data-ttu-id="e87cb-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e87cb-116">Requirements</span></span>



| <span data-ttu-id="e87cb-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="e87cb-117">Requirement</span></span> | <span data-ttu-id="e87cb-118">Value</span><span class="sxs-lookup"><span data-stu-id="e87cb-118">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="e87cb-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e87cb-119">Minimum supported client</span></span><br/> | <span data-ttu-id="e87cb-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="e87cb-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="e87cb-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e87cb-121">Minimum supported server</span></span><br/> | <span data-ttu-id="e87cb-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="e87cb-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="e87cb-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e87cb-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="e87cb-124"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="e87cb-124"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="e87cb-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e87cb-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="e87cb-126"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e87cb-126"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="e87cb-127">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e87cb-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e87cb-128"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e87cb-128"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




