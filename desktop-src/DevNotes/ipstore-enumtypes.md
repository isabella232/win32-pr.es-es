---
description: Devuelve una interfaz para enumerar los tipos que están registrados actualmente en la base de datos protegida.
ms.assetid: 0c0c2ad7-90b0-4fc0-8972-82eb159653be
title: 'IPStore:: EnumTypes (método) (pstore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.EnumTypes
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 73166a9fc1d76ae9f67528636eda567b9fa190a2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649477"
---
# <a name="ipstoreenumtypes-method"></a><span data-ttu-id="73ee9-103">IPStore:: EnumTypes (método)</span><span class="sxs-lookup"><span data-stu-id="73ee9-103">IPStore::EnumTypes method</span></span>

<span data-ttu-id="73ee9-104">\[El almacenamiento protegido (pstore) está disponible para su uso en Windows Server 2003 y Windows XP.</span><span class="sxs-lookup"><span data-stu-id="73ee9-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="73ee9-105">Solo está disponible para las operaciones de solo lectura en Windows Server 2008 y Windows Vista, pero puede no estar disponible en las versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="73ee9-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="73ee9-106">Pstore usa una implementación anterior de la protección de datos.</span><span class="sxs-lookup"><span data-stu-id="73ee9-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="73ee9-107">Se recomienda encarecidamente a los desarrolladores que aprovechen la protección de datos más segura proporcionada por las funciones [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) y [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="73ee9-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="73ee9-108">Devuelve una interfaz para enumerar los tipos que están registrados actualmente en la base de datos protegida.</span><span class="sxs-lookup"><span data-stu-id="73ee9-108">Returns an interface for enumerating types that are currently registered in the protected database.</span></span>

## <a name="syntax"></a><span data-ttu-id="73ee9-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="73ee9-109">Syntax</span></span>


```C++
HRESULT EnumTypes(
  [in] PST_KEY          Key,
  [in] DWORD            dwFlags,
  [in] IEnumPStoreTypes **ppenum
);
```



## <a name="parameters"></a><span data-ttu-id="73ee9-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="73ee9-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="73ee9-111">*Clave* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="73ee9-111">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="73ee9-112">Especifica si el tipo es local en el equipo o solo está asociado con el usuario que crea.</span><span class="sxs-lookup"><span data-stu-id="73ee9-112">Specifies whether the type is local to the computer or associated only with the creating user.</span></span>



| <span data-ttu-id="73ee9-113">Value</span><span class="sxs-lookup"><span data-stu-id="73ee9-113">Value</span></span>                                                                                                                                                                                                                                                   | <span data-ttu-id="73ee9-114">Significado</span><span class="sxs-lookup"><span data-stu-id="73ee9-114">Meaning</span></span>                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="PST_KEY_CURRENT_USER"></span><span id="pst_key_current_user"></span><dl> <span data-ttu-id="73ee9-115"><dt>**Archivo pst \_ \_ \_ Usuario actual clave**</dt> <dt>0x00000000</dt></span><span class="sxs-lookup"><span data-stu-id="73ee9-115"><dt>**PST\_KEY\_CURRENT\_USER**</dt> <dt>0x00000000</dt></span></span> </dl>    | <span data-ttu-id="73ee9-116">El almacenamiento se mantiene en la sección usuario actual del registro.</span><span class="sxs-lookup"><span data-stu-id="73ee9-116">The storage is maintained in the current user section of the registry.</span></span><br/>  |
| <span id="PST_KEY_LOCAL_MACHINE"></span><span id="pst_key_local_machine"></span><dl> <span data-ttu-id="73ee9-117"><dt>**Archivo pst \_ \_ \_ Máquina local de claves**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="73ee9-117"><dt>**PST\_KEY\_LOCAL\_MACHINE**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="73ee9-118">El almacenamiento se mantiene en la sección del equipo local del registro.</span><span class="sxs-lookup"><span data-stu-id="73ee9-118">The storage is maintained in the local machine section of the registry.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="73ee9-119">*dwFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="73ee9-119">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="73ee9-120">Reserved: debe establecerse en cero.</span><span class="sxs-lookup"><span data-stu-id="73ee9-120">Reserved: Must be set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="73ee9-121">*ppenum* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="73ee9-121">*ppenum* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="73ee9-122">Puntero a una interfaz [**IEnumPStoreTypes**](ienumpstoretypes.md) que se usa para realizar las tareas de enumeración.</span><span class="sxs-lookup"><span data-stu-id="73ee9-122">A pointer to an [**IEnumPStoreTypes**](ienumpstoretypes.md) interface that is used to perform the enumeration tasks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="73ee9-123">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="73ee9-123">Return value</span></span>

<span data-ttu-id="73ee9-124">El valor devuelto es un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="73ee9-124">The return value is an **HRESULT** value.</span></span> <span data-ttu-id="73ee9-125">Un valor de **PST \_ E \_ OK** indica que la función se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="73ee9-125">A value of **PST\_E\_OK** indicates the function was successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="73ee9-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="73ee9-126">Requirements</span></span>



| <span data-ttu-id="73ee9-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="73ee9-127">Requirement</span></span> | <span data-ttu-id="73ee9-128">Value</span><span class="sxs-lookup"><span data-stu-id="73ee9-128">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="73ee9-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="73ee9-129">Header</span></span><br/> | <dl> <span data-ttu-id="73ee9-130"><dt>Pstore. h</dt></span><span class="sxs-lookup"><span data-stu-id="73ee9-130"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="73ee9-131">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="73ee9-131">DLL</span></span><br/>    | <dl> <span data-ttu-id="73ee9-132"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="73ee9-132"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="73ee9-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="73ee9-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73ee9-134">**IPStore**</span><span class="sxs-lookup"><span data-stu-id="73ee9-134">**IPStore**</span></span>](ipstore.md)
</dt> </dl>

 

 
