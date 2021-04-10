---
title: Función FreeNapComponentRegistrationInfoArray (NapUtil. h)
description: Libera un número especificado de estructuras de datos NapComponentRegistrationInfo de una matriz.
ms.assetid: 6fcb1394-04dd-4d8a-87f7-6b69b6ef29ff
keywords:
- FreeNapComponentRegistrationInfoArray función NAP
topic_type:
- apiref
api_name:
- FreeNapComponentRegistrationInfoArray
api_location:
- qutil.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df823ad8086c57a6ee193bd0d58678786cfe325b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150865"
---
# <a name="freenapcomponentregistrationinfoarray-function"></a><span data-ttu-id="6cad4-104">FreeNapComponentRegistrationInfoArray función)</span><span class="sxs-lookup"><span data-stu-id="6cad4-104">FreeNapComponentRegistrationInfoArray function</span></span>

> [!Note]  
> <span data-ttu-id="6cad4-105">La plataforma de protección de acceso a redes no está disponible a partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="6cad4-105">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="6cad4-106">La función **FreeNapComponentRegistrationInfoArray** libera un número especificado de estructuras de datos [**NapComponentRegistrationInfo**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) de una matriz.</span><span class="sxs-lookup"><span data-stu-id="6cad4-106">The **FreeNapComponentRegistrationInfoArray** function frees a specified number of [**NapComponentRegistrationInfo**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) data structures from an array.</span></span>

## <a name="syntax"></a><span data-ttu-id="6cad4-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6cad4-107">Syntax</span></span>


```C++
NAPAPI VOID WINAPI FreeNapComponentRegistrationInfoArray(
  _In_ UINT16                       count,
  _In_ NapComponentRegistrationInfo **info
);
```



## <a name="parameters"></a><span data-ttu-id="6cad4-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6cad4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6cad4-109">*recuento* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6cad4-109">*count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6cad4-110">El número de estructuras [**NapComponentRegistrationInfo**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) en *info* que se van a liberar.</span><span class="sxs-lookup"><span data-stu-id="6cad4-110">The number of [**NapComponentRegistrationInfo**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) structures in *info* to free.</span></span>

</dd> <dt>

<span data-ttu-id="6cad4-111">*información* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="6cad4-111">*info* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6cad4-112">Puntero a una matriz de estructuras de datos [**NapComponentRegistrationInfo**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) que se va a liberar.</span><span class="sxs-lookup"><span data-stu-id="6cad4-112">A pointer to an array of [**NapComponentRegistrationInfo**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) data structures to be freed.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6cad4-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6cad4-113">Remarks</span></span>

<span data-ttu-id="6cad4-114">Todas las interfaces COM que admite el sistema NAP usan reglas estándar de administración de memoria COM y los asignadores de memoria COM (**CoTaskMemAlloc** y **CoTaskMemFree**):</span><span class="sxs-lookup"><span data-stu-id="6cad4-114">All the COM interfaces supported by the NAP system use standard COM memory management rules and the COM memory allocators (**CoTaskMemAlloc** and **CoTaskMemFree**):</span></span>

-   <span data-ttu-id="6cad4-115">El autor de la llamada asigna y libera los parámetros **in** .</span><span class="sxs-lookup"><span data-stu-id="6cad4-115">**In** parameters are allocated and freed by the caller.</span></span>
-   <span data-ttu-id="6cad4-116">El destinatario asigna los parámetros **out** y el llamador los libera mediante **CoTaskMem**.</span><span class="sxs-lookup"><span data-stu-id="6cad4-116">**Out** parameters are allocated by the callee and freed by the caller using **CoTaskMem**.</span></span>
-   <span data-ttu-id="6cad4-117">Los parámetros **in/out** son asignados por el autor de la llamada, liberados y reasignados por el destinatario y, en última instancia, liberados por el llamador, mediante **CoTaskMem**.</span><span class="sxs-lookup"><span data-stu-id="6cad4-117">**In/out** parameters are allocated by the caller, freed and reallocated by the callee, and ultimately freed by the caller, using **CoTaskMem**.</span></span>

<span data-ttu-id="6cad4-118">Todas las funciones NAP para liberar memoria también liberan todos los punteros incrustados.</span><span class="sxs-lookup"><span data-stu-id="6cad4-118">All NAP functions for freeing memory also free all embedded pointers.</span></span>

## <a name="requirements"></a><span data-ttu-id="6cad4-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6cad4-119">Requirements</span></span>



| <span data-ttu-id="6cad4-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="6cad4-120">Requirement</span></span> | <span data-ttu-id="6cad4-121">Value</span><span class="sxs-lookup"><span data-stu-id="6cad4-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="6cad4-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6cad4-122">Minimum supported client</span></span><br/> | <span data-ttu-id="6cad4-123">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="6cad4-123">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="6cad4-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6cad4-124">Minimum supported server</span></span><br/> | <span data-ttu-id="6cad4-125">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="6cad4-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="6cad4-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6cad4-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="6cad4-127"><dt>NapUtil. h</dt></span><span class="sxs-lookup"><span data-stu-id="6cad4-127"><dt>NapUtil.h</dt></span></span> </dl> |
| <span data-ttu-id="6cad4-128">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="6cad4-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6cad4-129"><dt>Qutil.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6cad4-129"><dt>Qutil.dll</dt></span></span> </dl> |



 

 





