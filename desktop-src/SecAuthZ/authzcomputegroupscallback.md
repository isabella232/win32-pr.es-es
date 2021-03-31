---
description: Función definida por la aplicación que crea una lista de identificadores de seguridad (SID) que se aplican a un cliente. AuthzComputeGroupsCallback es un marcador de posición para el nombre de la función definida por la aplicación.
ms.assetid: c20a02a0-5303-4433-a484-5a89999b32b9
title: Función de devolución de llamada AuthzComputeGroupsCallback
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AuthzComputeGroupsCallback
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: 3728f8114d87d07ddb33dd77a6fda5db30d07cf0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103819462"
---
# <a name="authzcomputegroupscallback-callback-function"></a><span data-ttu-id="80486-104">Función de devolución de llamada AuthzComputeGroupsCallback</span><span class="sxs-lookup"><span data-stu-id="80486-104">AuthzComputeGroupsCallback callback function</span></span>

<span data-ttu-id="80486-105">La función **AuthzComputeGroupsCallback** es una función definida por la aplicación que crea una lista de [*identificadores de seguridad*](/windows/desktop/SecGloss/s-gly) (SID) que se aplican a un cliente.</span><span class="sxs-lookup"><span data-stu-id="80486-105">The **AuthzComputeGroupsCallback** function is an application-defined function that creates a list of [*security identifiers*](/windows/desktop/SecGloss/s-gly) (SIDs) that apply to a client.</span></span> <span data-ttu-id="80486-106">**AuthzComputeGroupsCallback** es un marcador de posición para el nombre de la función definida por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="80486-106">**AuthzComputeGroupsCallback** is a placeholder for the application-defined function name.</span></span>

## <a name="syntax"></a><span data-ttu-id="80486-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="80486-107">Syntax</span></span>


```C++
BOOL CALLBACK AuthzComputeGroupsCallback(
  _In_  AUTHZ_CLIENT_CONTEXT_HANDLE hAuthzClientContext,
  _In_  PVOID                       Args,
  _Out_ PSID_AND_ATTRIBUTES         *pSidAttrArray,
  _Out_ PDWORD                      pSidCount,
  _Out_ PSID_AND_ATTRIBUTES         *pRestrictedSidAttrArray,
  _Out_ PDWORD                      pRestrictedSidCount
);
```



## <a name="parameters"></a><span data-ttu-id="80486-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="80486-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="80486-109">*hAuthzClientContext* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="80486-109">*hAuthzClientContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="80486-110">Identificador de un contexto de cliente.</span><span class="sxs-lookup"><span data-stu-id="80486-110">A handle to a client context.</span></span>

</dd> <dt>

<span data-ttu-id="80486-111">*Argumentos* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="80486-111">*Args* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="80486-112">Datos pasados en el parámetro *DynamicGroupArgs* de una llamada a la función [**AuthzInitializeContextFromAuthzContext**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromauthzcontext), [**AuthzInitializeContextFromSid**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromsid)o [**AuthzInitializeContextFromToken**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromtoken) .</span><span class="sxs-lookup"><span data-stu-id="80486-112">Data passed in the *DynamicGroupArgs* parameter of a call to the [**AuthzInitializeContextFromAuthzContext**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromauthzcontext), [**AuthzInitializeContextFromSid**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromsid), or [**AuthzInitializeContextFromToken**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromtoken) function.</span></span>

</dd> <dt>

<span data-ttu-id="80486-113">*pSidAttrArray* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="80486-113">*pSidAttrArray* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="80486-114">Puntero a una variable de puntero que recibe la dirección de una matriz de estructuras de [**SID \_ y \_ atributos**](/windows/desktop/api/Winnt/ns-winnt-sid_and_attributes) .</span><span class="sxs-lookup"><span data-stu-id="80486-114">A pointer to a pointer variable that receives the address of an array of [**SID\_AND\_ATTRIBUTES**](/windows/desktop/api/Winnt/ns-winnt-sid_and_attributes) structures.</span></span> <span data-ttu-id="80486-115">Estas estructuras representan los grupos a los que pertenece el cliente.</span><span class="sxs-lookup"><span data-stu-id="80486-115">These structures represent the groups to which the client belongs.</span></span>

</dd> <dt>

<span data-ttu-id="80486-116">*pSidCount* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="80486-116">*pSidCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="80486-117">El número de estructuras en *pSidAttrArray*.</span><span class="sxs-lookup"><span data-stu-id="80486-117">The number of structures in *pSidAttrArray*.</span></span>

</dd> <dt>

<span data-ttu-id="80486-118">*pRestrictedSidAttrArray* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="80486-118">*pRestrictedSidAttrArray* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="80486-119">Puntero a una variable de puntero que recibe la dirección de una matriz de estructuras de [**SID \_ y \_ atributos**](/windows/desktop/api/Winnt/ns-winnt-sid_and_attributes) .</span><span class="sxs-lookup"><span data-stu-id="80486-119">A pointer to a pointer variable that receives the address of an array of [**SID\_AND\_ATTRIBUTES**](/windows/desktop/api/Winnt/ns-winnt-sid_and_attributes) structures.</span></span> <span data-ttu-id="80486-120">Estas estructuras representan los grupos de los que el cliente está restringido.</span><span class="sxs-lookup"><span data-stu-id="80486-120">These structures represent the groups from which the client is restricted.</span></span>

</dd> <dt>

<span data-ttu-id="80486-121">*pRestrictedSidCount* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="80486-121">*pRestrictedSidCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="80486-122">El número de estructuras en *pSidRestrictedAttrArray*.</span><span class="sxs-lookup"><span data-stu-id="80486-122">The number of structures in *pSidRestrictedAttrArray*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="80486-123">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="80486-123">Return value</span></span>

<span data-ttu-id="80486-124">Si la función devuelve correctamente una lista de SID, el valor devuelto es **true**.</span><span class="sxs-lookup"><span data-stu-id="80486-124">If the function successfully returns a list of SIDs, the return value is **TRUE**.</span></span>

<span data-ttu-id="80486-125">Si se produce un error en la función, el valor devuelto es **false**.</span><span class="sxs-lookup"><span data-stu-id="80486-125">If the function fails, the return value is **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="80486-126">Observaciones</span><span class="sxs-lookup"><span data-stu-id="80486-126">Remarks</span></span>

<span data-ttu-id="80486-127">Las aplicaciones también pueden agregar SID al contexto del cliente mediante una llamada a [**AuthzAddSidsToContext**](/windows/desktop/api/Authz/nf-authz-authzaddsidstocontext).</span><span class="sxs-lookup"><span data-stu-id="80486-127">Applications can also add SIDs to the client context by calling [**AuthzAddSidsToContext**](/windows/desktop/api/Authz/nf-authz-authzaddsidstocontext).</span></span>

<span data-ttu-id="80486-128">Las variables de atributo deben tener el formato de una expresión cuando se utilizan con operadores lógicos; de lo contrario, se evalúan como Unknown.</span><span class="sxs-lookup"><span data-stu-id="80486-128">Attribute variables must be in the form of an expression when used with logical operators; otherwise, they are evaluated as unknown.</span></span>

## <a name="requirements"></a><span data-ttu-id="80486-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="80486-129">Requirements</span></span>



| <span data-ttu-id="80486-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="80486-130">Requirement</span></span> | <span data-ttu-id="80486-131">Value</span><span class="sxs-lookup"><span data-stu-id="80486-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="80486-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="80486-132">Minimum supported client</span></span><br/> | <span data-ttu-id="80486-133">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="80486-133">Windows XP \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="80486-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="80486-134">Minimum supported server</span></span><br/> | <span data-ttu-id="80486-135">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="80486-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                   |
| <span data-ttu-id="80486-136">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="80486-136">Redistributable</span></span><br/>          | <span data-ttu-id="80486-137">Paquete de herramientas de administración de Windows Server 2003 en Windows XP</span><span class="sxs-lookup"><span data-stu-id="80486-137">Windows Server 2003 Administration Tools Pack on Windows XP</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="80486-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="80486-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80486-139">Funciones básicas de Access Control</span><span class="sxs-lookup"><span data-stu-id="80486-139">Basic Access Control Functions</span></span>](authorization-functions.md)
</dt> <dt>

[<span data-ttu-id="80486-140">**AuthzAddSidsToContext**</span><span class="sxs-lookup"><span data-stu-id="80486-140">**AuthzAddSidsToContext**</span></span>](/windows/desktop/api/Authz/nf-authz-authzaddsidstocontext)
</dt> <dt>

[<span data-ttu-id="80486-141">**AuthzCachedAccessCheck**</span><span class="sxs-lookup"><span data-stu-id="80486-141">**AuthzCachedAccessCheck**</span></span>](/windows/desktop/api/Authz/nf-authz-authzcachedaccesscheck)
</dt> <dt>

[<span data-ttu-id="80486-142">**AuthzInitializeContextFromAuthzContext**</span><span class="sxs-lookup"><span data-stu-id="80486-142">**AuthzInitializeContextFromAuthzContext**</span></span>](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromauthzcontext)
</dt> <dt>

[<span data-ttu-id="80486-143">**AuthzInitializeContextFromSid**</span><span class="sxs-lookup"><span data-stu-id="80486-143">**AuthzInitializeContextFromSid**</span></span>](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromsid)
</dt> <dt>

[<span data-ttu-id="80486-144">**AuthzInitializeContextFromToken**</span><span class="sxs-lookup"><span data-stu-id="80486-144">**AuthzInitializeContextFromToken**</span></span>](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromtoken)
</dt> <dt>

[<span data-ttu-id="80486-145">**AuthzInitializeResourceManager**</span><span class="sxs-lookup"><span data-stu-id="80486-145">**AuthzInitializeResourceManager**</span></span>](/windows/desktop/api/Authz/nf-authz-authzinitializeresourcemanager)
</dt> <dt>

[<span data-ttu-id="80486-146">**SID \_ y \_ atributos**</span><span class="sxs-lookup"><span data-stu-id="80486-146">**SID\_AND\_ATTRIBUTES**</span></span>](/windows/desktop/api/Winnt/ns-winnt-sid_and_attributes)
</dt> </dl>

 

