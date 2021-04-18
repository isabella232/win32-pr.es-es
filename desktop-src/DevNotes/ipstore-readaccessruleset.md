---
description: Lee las reglas de acceso para un tipo determinado.
ms.assetid: fd569e7f-ca5c-4571-bbaa-c669e8780a97
title: 'IPStore:: ReadAccessRuleSet (método) (pstore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.ReadAccessRuleSet
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: f69c206bde67c2ddf9ed87ba0c50633ab9c15bc3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649962"
---
# <a name="ipstorereadaccessruleset-method"></a><span data-ttu-id="ca70c-103">IPStore:: ReadAccessRuleSet (método)</span><span class="sxs-lookup"><span data-stu-id="ca70c-103">IPStore::ReadAccessRuleSet method</span></span>

<span data-ttu-id="ca70c-104">\[El almacenamiento protegido (pstore) está disponible para su uso en Windows Server 2003 y Windows XP.</span><span class="sxs-lookup"><span data-stu-id="ca70c-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="ca70c-105">Solo está disponible para las operaciones de solo lectura en Windows Server 2008 y Windows Vista, pero puede no estar disponible en las versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="ca70c-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="ca70c-106">Pstore usa una implementación anterior de la protección de datos.</span><span class="sxs-lookup"><span data-stu-id="ca70c-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="ca70c-107">Se recomienda encarecidamente a los desarrolladores que aprovechen la protección de datos más segura proporcionada por las funciones [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) y [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="ca70c-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="ca70c-108">\[Este método no se implementa.\]</span><span class="sxs-lookup"><span data-stu-id="ca70c-108">\[This method is not implemented.\]</span></span>

<span data-ttu-id="ca70c-109">Lee las reglas de acceso para un tipo determinado.</span><span class="sxs-lookup"><span data-stu-id="ca70c-109">Reads the access rules for a given type.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca70c-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ca70c-110">Syntax</span></span>


```C++
HRESULT ReadAccessRuleSet(
  [in]       PST_KEY            Key,
  [in] const GUID               *pType,
  [in] const GUID               *pSubtype,
  [in]       PPST_TYPEINFO      pInfo,
  [in]       PPST_ACCESSRULESET **ppRules,
  [in]       DWORD              dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="ca70c-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ca70c-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ca70c-112">*Clave* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="ca70c-112">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ca70c-113">Reservado.</span><span class="sxs-lookup"><span data-stu-id="ca70c-113">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="ca70c-114">*pType* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ca70c-114">*pType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ca70c-115">Reservado.</span><span class="sxs-lookup"><span data-stu-id="ca70c-115">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="ca70c-116">*pSubtype* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ca70c-116">*pSubtype* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ca70c-117">Reservado.</span><span class="sxs-lookup"><span data-stu-id="ca70c-117">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="ca70c-118">*Pinfo* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ca70c-118">*pInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ca70c-119">Reservado.</span><span class="sxs-lookup"><span data-stu-id="ca70c-119">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="ca70c-120">*ppRules* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ca70c-120">*ppRules* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ca70c-121">Reservado.</span><span class="sxs-lookup"><span data-stu-id="ca70c-121">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="ca70c-122">*dwFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ca70c-122">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ca70c-123">Reservado.</span><span class="sxs-lookup"><span data-stu-id="ca70c-123">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ca70c-124">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ca70c-124">Return value</span></span>

<span data-ttu-id="ca70c-125">Siempre se producirá un error en las llamadas a este método.</span><span class="sxs-lookup"><span data-stu-id="ca70c-125">Calls to this method will always fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="ca70c-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ca70c-126">Requirements</span></span>



| <span data-ttu-id="ca70c-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="ca70c-127">Requirement</span></span> | <span data-ttu-id="ca70c-128">Value</span><span class="sxs-lookup"><span data-stu-id="ca70c-128">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ca70c-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ca70c-129">Header</span></span><br/> | <dl> <span data-ttu-id="ca70c-130"><dt>Pstore. h</dt></span><span class="sxs-lookup"><span data-stu-id="ca70c-130"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="ca70c-131">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ca70c-131">DLL</span></span><br/>    | <dl> <span data-ttu-id="ca70c-132"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ca70c-132"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ca70c-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="ca70c-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca70c-134">**IPStore**</span><span class="sxs-lookup"><span data-stu-id="ca70c-134">**IPStore**</span></span>](ipstore.md)
</dt> </dl>

 

 
