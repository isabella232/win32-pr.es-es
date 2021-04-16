---
description: Escribe las reglas de acceso para el tipo dado.
ms.assetid: d5cfd782-8d87-45ae-a574-0a294a30ca71
title: 'IPStore:: WriteAccessRuleset (método) (pstore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.WriteAccessRuleset
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 7399ff800087720d65cb45e80ccab080a7df9baf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671545"
---
# <a name="ipstorewriteaccessruleset-method"></a><span data-ttu-id="6e6ea-103">IPStore:: WriteAccessRuleset (método)</span><span class="sxs-lookup"><span data-stu-id="6e6ea-103">IPStore::WriteAccessRuleset method</span></span>

<span data-ttu-id="6e6ea-104">\[El almacenamiento protegido (pstore) está disponible para su uso en Windows Server 2003 y Windows XP.</span><span class="sxs-lookup"><span data-stu-id="6e6ea-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="6e6ea-105">Solo está disponible para las operaciones de solo lectura en Windows Server 2008 y Windows Vista, pero puede no estar disponible en las versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="6e6ea-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="6e6ea-106">Pstore usa una implementación anterior de la protección de datos.</span><span class="sxs-lookup"><span data-stu-id="6e6ea-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="6e6ea-107">Se recomienda encarecidamente a los desarrolladores que aprovechen la protección de datos más segura proporcionada por las funciones [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) y [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="6e6ea-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="6e6ea-108">\[Este método no se implementa.\]</span><span class="sxs-lookup"><span data-stu-id="6e6ea-108">\[This method is not implemented.\]</span></span>

<span data-ttu-id="6e6ea-109">Escribe las reglas de acceso para el tipo dado.</span><span class="sxs-lookup"><span data-stu-id="6e6ea-109">Writes the access rules for the given type.</span></span>

## <a name="syntax"></a><span data-ttu-id="6e6ea-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6e6ea-110">Syntax</span></span>


```C++
HRESULT WriteAccessRuleset(
  [in]       PST_KEY            Key,
  [in] const GUID               *pType,
  [in] const GUID               *pSubtype,
  [in]       PPST_TYPEINFO      pInfo,
  [in]       PPST_ACCESSRULESET pRules,
  [in]       DWORD              dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="6e6ea-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6e6ea-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6e6ea-112">*Clave* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="6e6ea-112">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6e6ea-113">Reservado.</span><span class="sxs-lookup"><span data-stu-id="6e6ea-113">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="6e6ea-114">*pType* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6e6ea-114">*pType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6e6ea-115">Reservado.</span><span class="sxs-lookup"><span data-stu-id="6e6ea-115">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="6e6ea-116">*pSubtype* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6e6ea-116">*pSubtype* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6e6ea-117">Reservado.</span><span class="sxs-lookup"><span data-stu-id="6e6ea-117">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="6e6ea-118">*Pinfo* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6e6ea-118">*pInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6e6ea-119">Reservado.</span><span class="sxs-lookup"><span data-stu-id="6e6ea-119">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="6e6ea-120">*pRules* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6e6ea-120">*pRules* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6e6ea-121">Reservado.</span><span class="sxs-lookup"><span data-stu-id="6e6ea-121">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="6e6ea-122">*dwFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6e6ea-122">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6e6ea-123">Reservado.</span><span class="sxs-lookup"><span data-stu-id="6e6ea-123">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6e6ea-124">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6e6ea-124">Return value</span></span>

<span data-ttu-id="6e6ea-125">Siempre se producirá un error en las llamadas a este método.</span><span class="sxs-lookup"><span data-stu-id="6e6ea-125">Calls to this method will always fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="6e6ea-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6e6ea-126">Requirements</span></span>



| <span data-ttu-id="6e6ea-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="6e6ea-127">Requirement</span></span> | <span data-ttu-id="6e6ea-128">Value</span><span class="sxs-lookup"><span data-stu-id="6e6ea-128">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6e6ea-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6e6ea-129">Header</span></span><br/> | <dl> <span data-ttu-id="6e6ea-130"><dt>Pstore. h</dt></span><span class="sxs-lookup"><span data-stu-id="6e6ea-130"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="6e6ea-131">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="6e6ea-131">DLL</span></span><br/>    | <dl> <span data-ttu-id="6e6ea-132"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6e6ea-132"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6e6ea-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="6e6ea-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e6ea-134">**IPStore**</span><span class="sxs-lookup"><span data-stu-id="6e6ea-134">**IPStore**</span></span>](ipstore.md)
</dt> </dl>

 

 
