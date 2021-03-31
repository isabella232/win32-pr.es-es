---
title: Función FreeSoHAttributeValue (NapUtil. h)
description: Libera una estructura de datos SoHAttributeValue.
ms.assetid: 21647ee6-2ea2-45fd-b1f2-fb1836196f94
keywords:
- FreeSoHAttributeValue función NAP
topic_type:
- apiref
api_name:
- FreeSoHAttributeValue
api_location:
- qutil.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3bd56049eb727554227bd5eb509969f6795670a4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079700"
---
# <a name="freesohattributevalue-function"></a><span data-ttu-id="583ae-104">FreeSoHAttributeValue función)</span><span class="sxs-lookup"><span data-stu-id="583ae-104">FreeSoHAttributeValue function</span></span>

> [!Note]  
> <span data-ttu-id="583ae-105">La plataforma de protección de acceso a redes no está disponible a partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="583ae-105">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="583ae-106">La función **FreeSoHAttributeValue** libera una estructura de datos [**SoHAttributeValue**](sohattributevalue-union.md) .</span><span class="sxs-lookup"><span data-stu-id="583ae-106">The **FreeSoHAttributeValue** function frees an [**SoHAttributeValue**](sohattributevalue-union.md) data structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="583ae-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="583ae-107">Syntax</span></span>


```C++
NAPAPI VOID WINAPI FreeSoHAttributeValue(
  _In_ SoHAttributeType  type,
  _In_ SoHAttributeValue *value
);
```



## <a name="parameters"></a><span data-ttu-id="583ae-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="583ae-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="583ae-109">*tipo* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="583ae-109">*type* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="583ae-110">Valor [**SoHAttributeType**](sohattributetype-enum.md) que especifica el tipo de valor del atributo SOH que se va a liberar.</span><span class="sxs-lookup"><span data-stu-id="583ae-110">A [**SoHAttributeType**](sohattributetype-enum.md) value that specifies the type of SoH attribute value to free.</span></span>

</dd> <dt>

<span data-ttu-id="583ae-111">*valor* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="583ae-111">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="583ae-112">Puntero al [**SoHAttributeValue**](sohattributevalue-union.md) que se va a liberar.</span><span class="sxs-lookup"><span data-stu-id="583ae-112">A pointer to the [**SoHAttributeValue**](sohattributevalue-union.md) to free.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="583ae-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="583ae-113">Remarks</span></span>

<span data-ttu-id="583ae-114">Todas las interfaces COM que admite el sistema NAP usan reglas estándar de administración de memoria COM y los asignadores de memoria COM (**CoTaskMemAlloc** y **CoTaskMemFree**):</span><span class="sxs-lookup"><span data-stu-id="583ae-114">All the COM interfaces supported by the NAP system use standard COM memory management rules and the COM memory allocators (**CoTaskMemAlloc** and **CoTaskMemFree**):</span></span>

-   <span data-ttu-id="583ae-115">El autor de la llamada asigna y libera los parámetros **in** .</span><span class="sxs-lookup"><span data-stu-id="583ae-115">**In** parameters are allocated and freed by the caller.</span></span>
-   <span data-ttu-id="583ae-116">El destinatario asigna los parámetros **out** y el llamador los libera mediante **CoTaskMem**.</span><span class="sxs-lookup"><span data-stu-id="583ae-116">**Out** parameters are allocated by the callee and freed by the caller using **CoTaskMem**.</span></span>
-   <span data-ttu-id="583ae-117">Los parámetros **in/out** son asignados por el autor de la llamada, liberados y reasignados por el destinatario y, en última instancia, liberados por el llamador, mediante **CoTaskMem**.</span><span class="sxs-lookup"><span data-stu-id="583ae-117">**In/out** parameters are allocated by the caller, freed and reallocated by the callee, and ultimately freed by the caller, using **CoTaskMem**.</span></span>

<span data-ttu-id="583ae-118">Todas las funciones NAP para liberar memoria también liberan todos los punteros incrustados.</span><span class="sxs-lookup"><span data-stu-id="583ae-118">All NAP functions for freeing memory also free all embedded pointers.</span></span>

## <a name="requirements"></a><span data-ttu-id="583ae-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="583ae-119">Requirements</span></span>



| <span data-ttu-id="583ae-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="583ae-120">Requirement</span></span> | <span data-ttu-id="583ae-121">Value</span><span class="sxs-lookup"><span data-stu-id="583ae-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="583ae-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="583ae-122">Minimum supported client</span></span><br/> | <span data-ttu-id="583ae-123">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="583ae-123">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="583ae-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="583ae-124">Minimum supported server</span></span><br/> | <span data-ttu-id="583ae-125">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="583ae-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="583ae-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="583ae-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="583ae-127"><dt>NapUtil. h</dt></span><span class="sxs-lookup"><span data-stu-id="583ae-127"><dt>NapUtil.h</dt></span></span> </dl> |
| <span data-ttu-id="583ae-128">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="583ae-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="583ae-129"><dt>Qutil.dll</dt></span><span class="sxs-lookup"><span data-stu-id="583ae-129"><dt>Qutil.dll</dt></span></span> </dl> |



 

 





