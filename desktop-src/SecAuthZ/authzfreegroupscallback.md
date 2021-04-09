---
description: Una función definida por la aplicación que libera memoria asignada por la función AuthzComputeGroupsCallback. AuthzFreeGroupsCallback es un marcador de posición para el nombre de la función definida por la aplicación.
ms.assetid: 5563311c-2bd1-4e96-ba0a-5a4225050f77
title: Función de devolución de llamada AuthzFreeGroupsCallback
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AuthzFreeGroupsCallback
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: 7d8942acbc67f122ea79f0b9e98793628b5f21f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103819459"
---
# <a name="authzfreegroupscallback-callback-function"></a><span data-ttu-id="2986c-104">Función de devolución de llamada AuthzFreeGroupsCallback</span><span class="sxs-lookup"><span data-stu-id="2986c-104">AuthzFreeGroupsCallback callback function</span></span>

<span data-ttu-id="2986c-105">La función **AuthzFreeGroupsCallback** es una función definida por la aplicación que libera la memoria asignada por la función [**AuthzComputeGroupsCallback**](authzcomputegroupscallback.md) .</span><span class="sxs-lookup"><span data-stu-id="2986c-105">The **AuthzFreeGroupsCallback** function is an application-defined function that frees memory allocated by the [**AuthzComputeGroupsCallback**](authzcomputegroupscallback.md) function.</span></span> <span data-ttu-id="2986c-106">**AuthzFreeGroupsCallback** es un marcador de posición para el nombre de la función definida por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="2986c-106">**AuthzFreeGroupsCallback** is a placeholder for the application-defined function name.</span></span>

## <a name="syntax"></a><span data-ttu-id="2986c-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2986c-107">Syntax</span></span>


```C++
void CALLBACK AuthzFreeGroupsCallback(
  _In_ PSID_AND_ATTRIBUTES pSidAttrArray
);
```



## <a name="parameters"></a><span data-ttu-id="2986c-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2986c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2986c-109">*pSidAttrArray* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2986c-109">*pSidAttrArray* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2986c-110">Puntero a la memoria asignada por [**AuthzComputeGroupsCallback**](authzcomputegroupscallback.md).</span><span class="sxs-lookup"><span data-stu-id="2986c-110">A pointer to memory allocated by [**AuthzComputeGroupsCallback**](authzcomputegroupscallback.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2986c-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2986c-111">Return value</span></span>

<span data-ttu-id="2986c-112">Esta función de devolución de llamada no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="2986c-112">This callback function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2986c-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2986c-113">Remarks</span></span>

<span data-ttu-id="2986c-114">Las variables de atributo deben tener el formato de una expresión cuando se utilizan con operadores lógicos; de lo contrario, se evalúan como Unknown.</span><span class="sxs-lookup"><span data-stu-id="2986c-114">Attribute variables must be in the form of an expression when used with logical operators; otherwise, they are evaluated as unknown.</span></span>

## <a name="requirements"></a><span data-ttu-id="2986c-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2986c-115">Requirements</span></span>



| <span data-ttu-id="2986c-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="2986c-116">Requirement</span></span> | <span data-ttu-id="2986c-117">Value</span><span class="sxs-lookup"><span data-stu-id="2986c-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="2986c-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2986c-118">Minimum supported client</span></span><br/> | <span data-ttu-id="2986c-119">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="2986c-119">Windows XP \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="2986c-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2986c-120">Minimum supported server</span></span><br/> | <span data-ttu-id="2986c-121">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="2986c-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                   |
| <span data-ttu-id="2986c-122">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="2986c-122">Redistributable</span></span><br/>          | <span data-ttu-id="2986c-123">Paquete de herramientas de administración de Windows Server 2003 en Windows XP</span><span class="sxs-lookup"><span data-stu-id="2986c-123">Windows Server 2003 Administration Tools Pack on Windows XP</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2986c-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="2986c-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2986c-125">Funciones básicas de Access Control</span><span class="sxs-lookup"><span data-stu-id="2986c-125">Basic Access Control Functions</span></span>](authorization-functions.md)
</dt> <dt>

[<span data-ttu-id="2986c-126">**AuthzComputeGroupsCallback**</span><span class="sxs-lookup"><span data-stu-id="2986c-126">**AuthzComputeGroupsCallback**</span></span>](authzcomputegroupscallback.md)
</dt> </dl>

 

 




